##

The main purpose of the Terraform language is declaring resources, which represent

%

infrastructure objects

##

The main purpose of the Terraform language is declaring resources, all other language features exist only to make the definition of resources more flexible and

%

convenient

##

A Terraform configuration is a complete document in the Terraform language that tells Terraform how to manage a given collection of

%

infrastructure

##

A Terraform configuration can consist of multiple files and

%

directories

##

The syntax of the Terraform language consists of only a few basic elements:

- `_____`
- `_____`
- `_____`

%

- Blocks
- Arguments
- Expressions

##

Blocks are containers for other content and usually represent the configuration of some kind of object, like a 

%

resource

##

Blocks have a block type, can have zero or more labels, and have a body that contains any number of arguments and nested

%

blocks

##

Most of Terraform's features are controlled by top-level `_____` in a configuration file.

%

Most of Terraform's features are controlled by top-level **blocks** in a configuration file.

##

Arguments assign a value to a name. They appear within

%

blocks

##

Expressions represent a value, either literally or by referencing and combining other

%

values

##

Expressions appear as values for arguments, or within other

%

expressions

##

The Terraform language is declarative, describing an intended goal rather than

%

the steps to reach that goal

##

The ordering of blocks and the files they are organized into are generally `_____`; Terraform only considers implicit and explicit relationships between resources when determining an order of operations.

%

The ordering of blocks and the files they are organized into are generally **not significant**; Terraform only considers implicit and explicit relationships between resources when determining an order of operations.

##

```
resource "aws_vpc" "main" {
  cidr_block = var.base_cidr_block
}

[BLOCK `_____`] "[BLOCK `_____`]" "[BLOCK `_____`]" {
  # Block `_____`
  [IDENTIFIER] = [`_____`] # Argument
}
```

%

```
resource "aws_vpc" "main" {
  cidr_block = var.base_cidr_block
}

[BLOCK **TYPE**] "[BLOCK **LABEL**]" "[BLOCK **LABEL**]" {
  # Block **body**
  [IDENTIFIER] = [**EXPRESSION**] # Argument
}
```
