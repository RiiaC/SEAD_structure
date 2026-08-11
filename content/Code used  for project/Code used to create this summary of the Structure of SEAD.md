> [! info] The below sets of code were used on 2025-09-19 to generate the list of  [[Structure of SEAD/Tables/index|SEAD tables]] and [[Structure of SEAD/Columns/index|SEAD columns]] as shown on this web page.

# Step 1: Generate the plain list

I used the below sql query to extract the full list of SEAD tables and save it as `SEAD-tables.csv`

`select *`  
`from sead_utility.table_columns`  
`where table_schema = 'public'`  
  `and table_name like 'tbl_%'`

# Step 2: Convert the list to files in markdown format

I used the below code to convert the information in the `SEAD-tables.csv` to a folder of files in markdown format that Obsidian would read as a single file for each table or column, with front matter properties for each file specifying the metadata for the table or column (e.g. `primary_key`, `foreign_keys`, `connected_tables`, etc.), in such a way as to create links between the notes based on that metadata. 

The files were then opened in Obsidian using the "Open folder as vault" option. (I believe that some manual cleaning of the output files may have been necessary before everything worked properly in Obsidian, but no record was made of what steps, if any, that manual cleanup entailed.)

````
import pandas as pd
import os

# Load the CSV file
df = pd.read_csv("SEAD tables.csv")

# Create output directories
os.makedirs("Tables", exist_ok=True)
os.makedirs("Columns", exist_ok=True)

# Clean up column names
df.columns = df.columns.str.strip()

# Get unique table and column names
unique_tables = df['table_name'].unique()
unique_columns = df['column_name'].unique()

# Create a dictionary to track which tables use each column
column_to_tables = {
    col: df[df['column_name'] == col]['table_name'].unique().tolist()
    for col in unique_columns
}

# Generate table notes
for table in unique_tables:
    table_df = df[df['table_name'] == table]
    primary_key = table_df[table_df['is_pk'] == 'YES']['column_name'].tolist()
    foreign_keys = table_df[table_df['is_fk'] == 'YES']['column_name'].tolist()
    columns = table_df[
        (table_df['is_pk'] != 'YES') & (table_df['is_fk'] != 'YES')
    ]['column_name'].tolist()
    connected_tables = table_df['fk_table_name'].dropna().unique().tolist()

    content = f"# {table}\n\n"
    content += f"**Table Name:** {table}\n"

    if primary_key:
        content += f"**Primary Key:** [[{primary_key[0]}]]\n"
    if foreign_keys:
        content += "**Foreign keys:**\n" + "\n".join([f"- [[{fk}]]" for fk in foreign_keys]) + "\n"
    if columns:
        content += "**Columns:**\n" + "\n".join([f"- [[{col}]]" for col in columns]) + "\n"
    if connected_tables:
        content += "**Connected Tables:**\n" + "\n".join([f"- [[{ct}]]" for ct in connected_tables]) + "\n"

    with open(f"Tables/{table}.md", "w", encoding="utf-8") as f:
        f.write(content)

# Generate column notes
for column in unique_columns:
    column_df = df[df['column_name'] == column]
    data_type = column_df['data_type'].iloc[0]
    connected_tables = column_to_tables[column]

    content = f"# {column}\n\n"
    content += f"**Column Name:** {column}\n"
    content += f"**Data type:** {data_type}\n"
    content += "**Connected Tables:**\n" + "\n".join([f"- [[{tbl}]]" for tbl in connected_tables]) + "\n"

    with open(f"Columns/{column}.md", "w", encoding="utf-8") as f:
        f.write(content)

````

# post-export additions

All additional edits, lookup tables, colour-coding, and commentary present in the notes for the various SEAD tables and columns were added by hand after the Obsidian Vault was created as outlined above.

Where present, the lookup tables were generated using a variation of:

`select *
`from tbl_`*<table_name>*`_types`
