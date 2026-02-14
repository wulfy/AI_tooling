<template name="tables">
# {TABLE NAME}

{Table Description}

## Fields

| Field Name | Field Type | Field Description | Nullable | FK |
|------------|------------|-------------------|----------|------|
| ... | ... | ... | TRUE|FALSE | [{Table}.{Field}](./{table-name}.md) |

## Primary Key

- {Field Name}

## Indexes

- {Index Name}: {Field Name}, {Field Name},...

## Relevant files
<!-- Relevant files from the legacy codebase -->
- [FileName.ext](relative/path/to/file/from/this/markdown/file)
- ...

</template>

<instructions>
tables = CobolProject.tables

for(each model in tables)
  file("./teardown/tables/{model.name}.md").write(<template name="model" />, model)

file("./teardown/tables.md").write(mermaid-diagram, tables)
</instructions>.execute()