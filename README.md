**New Purge Mechanism:**

**Please find below update sets:**

sys_remote_update_set_61150f861bf74a90a32e433c8b4bcb14.xml
sys_remote_update_set_e6c747061b7b4a90a32e433c8b4bcb72.xml

How it works:
---------------------------------------------------------------
1. Commit these update sets.
2. Create an application menu and tag all modules to the Menu.
3. Create a new record.
4. List of tables will be populated based on the property.
4.1. If you would like to delete the record from any particuler table, you need to add the table name into sys property.
4.2. Attribute of that table should contain "No audit delete" to "true".
4.3. Enter Start & End Dates (Please note, the deletion should occur to older than 30 days records)
5. Click on "Calculate Records" button. It will fetch the record count and update in "Num of records to delete" field.
6. Status changes to "Estimated/Counted"
7. Now Change the status to "Reviewed".
8. After 4 mins, this record will be picked by a Scheduled Job and proceed for record deletion.
9. Number of jobs will be depends on the sys property.
