ec24d - EC2 for dummies
=======================

A set of simple shell scripts for managing EC2 nodes.

Installation
------------

Install the EC2 tools. 
Add the bin folder to your PATH.

Usage
-----

`ec24d-start appname`
Creates a node, provisiones it and tags it to belong to the named application.

`ec24d-stop appname`
Terminates *all* nodes of the named application.

`ec24d-push appname`
Pushes the current git repo to the named app.

`ec24d-ssh appname [cmd]`
Peformes ssh on (one node of?) the named app. 

 