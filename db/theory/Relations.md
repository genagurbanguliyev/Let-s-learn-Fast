

##### relation actions:
There are several actions you can define for a foreign key constraint when the referenced primary key is updated or deleted:

1. **NO ACTION**: This is the default action. If an attempt is made to update or delete a primary key that is referenced by a foreign key, the operation is disallowed, and an error is returned.

2. **RESTRICT**: Similar to NO ACTION, this prevents the update or deletion of the primary key if there are any dependent rows in the foreign key table.

3. **CASCADE**: If the primary key is updated, the corresponding foreign key values in the related table(s) are automatically updated to reflect the change. Similarly, if a row with a primary key is deleted, all related rows in the foreign key table(s) are also deleted.

4. **SET NULL**: If the primary key is updated or deleted, the corresponding foreign key values in the related table(s) are set to NULL. This requires that the foreign key column(s) allow NULL values.

5. **SET DEFAULT**: If the primary key is updated or deleted, the corresponding foreign key values in the related table(s) are set to their default values. This requires that the foreign key column(s) have a default value defined.