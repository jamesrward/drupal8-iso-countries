# Drupal 8 country list import with iso alpha 2 and 3 codes

Requirements: migrate_plus, migrate_tools, migrate_source_csv

1. Create content type via config sync using node.type.country.yml
2. Upload csv to private files.  I created a content type called private files to do this but there are other ways.
3. Import migration via config sync using country_migration.yml
4. Run `drush migrate-import country_csv`
5. You should receive the following response
```
Processed 245 items (245 created, 0 updated, 0 failed, 0 ignored) -     [status]
done with 'country_csv'
```

You should not have 245 country items with all the included fields.

Note:  I also created a migration group called csv_imports but this import does not appear under that list.  Perhaps as the modules stabilize this will work as expected.
