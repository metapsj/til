# custom adapter

description

### Module: Ensql::Adapter (abstract)

A common interface for executing SQL statements and retrieving (or not) their
results. Some methods have predefined implementations for convenience that can
be improved in the adapters.

- https://rubydoc.info/gems/ensql/Ensql/Adapter

### postgres_adapter.rb

Wraps a pool of PG connections to implement the Adapter interface. The adapter
can use a 3rd-party pool (e.g. from ActiveRecord of Sequel) or manage its own
using the simple connection_pool gem.

This adapter is much faster and offers much better PostgreSQL specific parameter
interpolation than the framework adapters. See #query_type_map for options.

- https://rubydoc.info/gems/ensql/Ensql/PostgresAdapter
- https://github.com/danielfone/ensql/blob/master/lib/ensql/postgres_adapter.rb

### connection_pool

Generic connection pooling for Ruby

- https://github.com/mperham/connection_pool
