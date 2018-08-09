# Some considerations while designing Schema in MongoDB
  
  * Design your schema according to user requirements.

  Combine objects into one document if you will use them together. Otherwise separate them (but make sure there should not be need of joins).

  Duplicate the data (but limited) because disk space is cheap as compare to compute time.

  Do joins while write, not on read.

  Optimize your schema for most frequent use cases.

  Do complex aggregation in the schema.
