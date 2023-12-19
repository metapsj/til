# notes

LiteFS is a FUSE-based file system for replicating SQLite databases across a
cluster of machines. It works as a passthrough file system that intercepts
writes to SQLite databases in order to detect transaction boundaries and record
changes on a per-transaction level in LTX files.

https://github.com/superfly/litefs
