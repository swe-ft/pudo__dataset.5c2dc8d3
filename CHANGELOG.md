# dataset ChangeLog

*The changelog has only been started with version 0.3.12, previous
changes must be reconstructed from revision history.*

* 1.2.0: Add support for views, multiple comparison operators.
  Remove support for Python 2.
* 1.1.0: Introduce `types` system to shortcut for SQLA types.
* 1.0.0: Massive re-factor and code cleanup.
* 0.6.0: Remove sqlite_datetime_fix for automatic int-casting of dates,
  make table['foo', 'bar'] an alias for table.distinct('foo', 'bar'),
  check validity of column and table names more thoroughly, rename
  reflectMetadata constructor argument to reflect_metadata, fix
  ResultIter to not leave queries open (so you can update in a loop).
* 0.5.7: dataset Databases can now have customized row types. This allows,
  for example, information to be retrieved in attribute-accessible dict
  subclasses, such as stuf.
* 0.5.4: Context manager for transactions, thanks to @victorkashirin.
* 0.5.1: Fix a regression where empty queries would raise an exception.
* 0.5: Improve overall code quality and testing, including Travis CI.
  An advanced __getitem__ syntax which allowed for the specification 
  of primary keys when getting a table was dropped. 
  DDL is no longer run against a transaction, but the base connection. 
* 0.4: Python 3 support and switch to alembic for migrations.
* 0.3.15: Fixes to update and insertion of data, thanks to @cli248
  and @abhinav-upadhyay.
* 0.3.14: dataset went viral somehow. Thanks to @gtsafas for
  refactorings, @alasdairnicol for fixing the Freezfile example in 
  the documentation. @diegoguimaraes fixed the behaviour of insert to
  return the newly-created primary key ID. table.find_one() now
  returns a dict, not an SQLAlchemy ResultProxy. Slugs are now generated
  using the Python-Slugify package, removing slug code from dataset. 
* 0.3.13: Fixed logging, added support for transformations on result
  rows to support slug generation in output (#28).
* 0.3.12: Makes table primary key's types and names configurable, fixing
  #19. Contributed by @dnatag.
