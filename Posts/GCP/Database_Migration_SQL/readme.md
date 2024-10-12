# Database Migration from Local Server SQL to Cloud SQL in GCP: Step-by-Step Guide

Before proceeding with the migration, it's crucial to ensure proper network access:

- Check firewall access for the required port on your local server
- Ensure port forwarding is enabled on your router
- If port forwarding isn't possible due to double NAT, consider using tunneling services like Telebit

These steps are essential for establishing a successful connection between your local server and GCP during the migration process.

## 1. Enable Database Migration API

First, enable the Database Migration API in your GCP project.

![Data_migration_API_enable](https://github.com/user-attachments/assets/2b891ef8-66fb-44d8-80bf-0c29e5bb190a)

## 2. Create Connection Profiles

Navigate to the Database Migration service and create connection profiles for both source and destination databases.

![connection_profiles](https://github.com/user-attachments/assets/a4e9d016-186d-4241-9d88-f0500704e37c)

![Create_connection_profile_1](https://github.com/user-attachments/assets/ada9c26d-f144-4425-92cc-707eaf592979)

## 3. Create Migration Job

Set up a new migration job to define the migration process.

![Migration_jobs](https://github.com/user-attachments/assets/ab434cb6-c9cd-4105-bb8e-2090e8df8507)

![Create_migration_job](https://github.com/user-attachments/assets/5bcb85bb-f015-44b3-97a9-7df053cb86f1)

## 4. Configure Source and Destination

Select the source (your local SQL database) and define the destination (Cloud SQL instance).

![select_source_migration_creation](https://github.com/user-attachments/assets/17a446ba-2e5b-402f-94e4-9a4278117902)

![Define_destination_1](https://github.com/user-attachments/assets/aba9e370-9de3-4d3a-9aa8-a7229b2aaa3a)

![Define_destination_2](https://github.com/user-attachments/assets/4e711b20-b089-4810-baed-06b2a45dfe45)

## 5. Set Up Connectivity

Choose the appropriate connectivity method for your migration.

![Connectivity_method](https://github.com/user-attachments/assets/5093768b-13e4-4242-8668-a0fbc368b493)

## 6. Test and Verify

Run a test to ensure the connection is successful.

![test_complete_success](https://github.com/user-attachments/assets/fb2025de-edd5-4f8d-ba0a-8a084da95b32)

## 7. Check the Created Cloud SQL Instance

Navigate to the Cloud SQL and check the migrated database

![sql_instances](https://github.com/user-attachments/assets/042068d8-c5f4-4f18-9bf0-0a694e1a361c)

![sql_database_menu](https://github.com/user-attachments/assets/4256e888-a030-4131-b006-24659e372a6c)

![cloud_sql_databases](https://github.com/user-attachments/assets/39c33550-f3da-40de-b080-c21c3b407895)

## 8. Enable Cloud SQL Admin API

Make sure the Cloud SQL Admin API is enabled for your project.

![cloud_sql_admin_api_enable](https://github.com/user-attachments/assets/e014caca-70c6-4f8d-baf3-f36e01525842)

## 9. Verify Migration

Check both the Cloud Shell and your local server to ensure databases and tables have been migrated correctly.

![Cloud_shell_databases](https://github.com/user-attachments/assets/435a9fef-0827-4f68-821c-017e48049250)

![cloud_shell_tables](https://github.com/user-attachments/assets/847bc04b-c760-4844-9f6f-fcf78a150767)

![Vm_databases](https://github.com/user-attachments/assets/fc554c84-ec98-413b-b36f-55cf21b6a5ea)

![vm_tables](https://github.com/user-attachments/assets/e239e1ad-2641-427c-a1bf-703251527f37)

## 10. Test Data Modifications

Create a new table or modify existing data in your local server to test continuous migration.

![creating_table_vm](https://github.com/user-attachments/assets/47dbcce5-aaee-4cad-8e35-0637ef21549a)

![updated_tables_cloud_shell](https://github.com/user-attachments/assets/f22d1ca6-0e4e-4bb4-8f30-64ff131dee9a)

## 11. Promote Migration

Once satisfied with the migration, promote the migration task to make Cloud SQL the primary database.

![promote_migration_task](https://github.com/user-attachments/assets/12c8d25c-630e-4fa2-b393-ec7314e43d5f)

## 12. Finalize Migration

After promotion, your Cloud SQL instance becomes a standalone instance, completing the migration process.

![standalone_sql](https://github.com/user-attachments/assets/cd05635b-81dd-469c-a19f-521fa26cacb8)
