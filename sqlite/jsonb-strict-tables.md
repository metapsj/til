# jsonb strict tables

source: https://sqlite.org/forum/forumpost/fa6f64e3dc1a5d97

### JSONB has landed

I'm curious, would it be possible (or a good idea) to add JSON and JSONB datatypes
to STRICT tables? Only int/real/text/blob/any column types are currently supported,
but I could see a big benefit to supporting JSON/JSONB column types as well.

```sql
CREATE TABLE t1(
  id TEXT PRIMARY KEY,
  name TEXT,
  settings JSONB
) STRICT;
```

Would essentially be the same as:

```sql
CREATE TABLE t1(
  id TEXT PRIMARY KEY,
  name TEXT,
  settings BLOB CHECK (jsonb_valid(settings))
) STRICT;
```

JSON columns could check if values are json_valid(), and JSONB could use jsonb_valid().
It would be cool if this could be something extensions could use (like an XML extension
adding a xml_valid() constraint to strict "XML" column types).
