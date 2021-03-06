% Indirection Reference
% 
% 

**This page is autogenerated; any changes will get overwritten**
*(last generated on Sat May 08 22:14:07 +1000 2010)*

This is the list of all indirections, their associated terminus
classes, and how you select between them.

In general, the appropriate terminus class is selected by the
application for you (e.g., `puppetd` would always use the `rest`
terminus for most of its indirected classes), but some classes are
tunable via normal settings. These will have `terminus setting`
documentation listed with them.

# catalog

## compiler

Puppet's catalog compilation interface, and its back-end is
Puppet's compiler

## yaml

Store catalogs as flat files, serialized using YAML.

# checksum

## file

Store files in a directory set based on their checksums.

# facts

## facter

Retrieve facts from Facter. This provides a somewhat abstract
interface between Puppet and Facter. It's only \`somewhat\`
abstract because it always returns the local host's facts,
regardless of what you attempt to find.

## memory

Keep track of facts in memory but nowhere else. This is used for
one-time compiles, such as what the stand-alone `puppet` does. To
use this terminus, you must load it with the data you want it to
contain.

## yaml

Store client facts as flat files, serialized using YAML, or return
deserialized facts from disk.

# file\_content

## file

Retrieve file contents from disk.

## file\_server

Retrieve file contents using Puppet's fileserver.

## modules

Retrieve file contents from modules.

## rest

Retrieve file contents via a REST HTTP interface.

# file\_metadata

## file

Retrieve file metadata directly from the local filesystem.

## file\_server

Retrieve file metadata using Puppet's fileserver.

## modules

Retrieve file metadata from modules.

## rest

Retrieve file metadata via a REST HTTP interface.

# node

Where to find node information. A node is composed of its name, its
facts, and its environment.

-   **Terminus Setting**: node\_terminus

## exec

Call an external program to get node information. See the
\`ExternalNodes\`:trac: page for more information.

## ldap

Search in LDAP for node configuration information. See the
\`LdapNodes\`:trac: page for more information. This will first
search for whatever the certificate name is, then (if that name
contains a '.') for the short name, then 'default'.

## memory

Keep track of nodes in memory but nowhere else. This is used for
one-time compiles, such as what the stand-alone `puppet` does. To
use this terminus, you must load it with the data you want it to
contain; it is only useful for developers and should generally not
be chosen by a normal user.

## plain

Always return an empty node object. Assumes you keep track of nodes
in flat file manifests. You should use it when you don't have some
other, functional source you want to use, as the compiler will not
work without a valid node terminus.

Note that class is responsible for merging the node's facts into
the node instance before it is returned.

## rest

This will eventually be a REST-based mechanism for finding nodes.
It is currently non-functional.

## yaml

Store node information as flat files, serialized using YAML, or
deserialize stored YAML nodes.

# report

## processor

Puppet's report processor. Processes the report with each of the
report types listed in the 'reports' setting.


* * * * *

*This page autogenerated on Sat May 08 22:14:07 +1000 2010*



