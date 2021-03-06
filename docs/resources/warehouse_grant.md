
# snowflake_warehouse_grant

<!-- These docs are auto-generated by code in ./docgen, run by with make docs. Manual edits will be overwritten. -->

**Note**: The snowflake_warehouse_grant resource creates exclusive attachments of grants.
		Across the entire Snowflake account, all of the warehouses to which a single grant is attached must be declared
		by a single snowflake_warehouse_grant resource. This means that even any snowflake_warehouse that have the attached
		grant via any other mechanism (including other Terraform resources) will have that attached grant revoked by this resource.
		These resources do not enforce exclusive attachment of a grant, it is the user's responsibility to enforce this.
		
## properties

|       NAME        |  TYPE  |                                         DESCRIPTION                                         | OPTIONAL | REQUIRED  | COMPUTED | DEFAULT |
|-------------------|--------|---------------------------------------------------------------------------------------------|----------|-----------|----------|---------|
| privilege         | string | The privilege to grant on the warehouse.                                                    | true     | false     | false    | "USAGE" |
| roles             | set    | Grants privilege to these roles.                                                            | true     | false     | false    |         |
| warehouse_name    | string | The name of the warehouse on which to grant privileges.                                     | false    | true      | false    |         |
| with_grant_option | bool   | When this is set to true, allows the recipient role to grant the privileges to other roles. | true     | false     | false    | false   |
