# Terraform AWS VPC Module Customized

This module is going to create the following resources. For high availability we are going to get first 2 AZ.

* VPC
* Internet gateway associated with VPC
* 2 Public subnets
* 2 Private subnets
* 2 database subnets
* Database subnet group
* EIP
* NAT Gateway
* Public route table
* Private route table
* Database route table
* Routes
* Route table assocations with subnets
* Peering with default VPC (if required)
* Peering routes in acceptor and requestor route tables

# Inputs
* project_name (Mandatory): User must supply their project name
* environment (Mandatory): user must supply their environment
* vpc_cidr (Mandatory): user must supply their VPC CIDR
* enable_dns_hostnames (Optional): Defaults to true
* common_tags (Optional): Default is empty, user can supply tags in list of string format.
* vpc_tags (Optional): Default is empty, user can supply tags in list of string format.
* igw_tags (Optional): Default is empty, user can supply tags in list of string format.
* public_subnet_cidrs (Mandatory): user must supply only two valid public subnet CIDR
* public_subnet_tags (Optional): Default is empty, user can supply tags in list of string format.
* private_subnet_cidrs (Mandatory): user must supply only two valid private subnet CIDR
* private_subnet_tags (Optional): Default is empty, user can supply tags in list of string format.
* database_subnet_cidrs (Mandatory): user must supply only two valid database subnet CIDR
* database_subnet_tags (Optional): Default is empty, user can supply tags in list of string format.
* db_subnet_group_tags (Optional): Default is empty, user can supply tags in list of string format.
* nat_gateway_tags (Optional): Default is empty, user can supply tags in list of string format.
* public_route_table_tags (Optional): Default is empty, user can supply tags in list of string format.
* private_route_table_tags (Optional): Default is empty, user can supply tags in list of string format.
* database_route_table_tags (Optional): Default is empty, user can supply tags in list of string format.
* is_peering_required (Optional) : defaults to false
* vpc_peering_tags (Optional): Default is empty, user can supply tags in list of string format.

# Outputs
* vpc_id: VPC ID created
* public_subnet_ids: list of 2 public subnet IDs created
* private_subnet_ids: list of 2 private subnet IDs created
* database_subnet_ids: list of 2 database subnet IDs created

