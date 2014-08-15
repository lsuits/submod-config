submod-config
=============

Utility script to build a fresh parent project using git submodules.

### Usage

From the commandline, run this script, giving it a target directory and a data file
containing a list of your submodules having the following form:

	local path 	 	(relative to the moodle root, aka $CFG->dirroot)
	remote path		(git clone path)
	[branch] 		(optional- if omitted, the default branch for the repository)

with record separated by one or more blank lines.

### Parent repo

If you specify a repository in your datafile having the local path '.', 
it will be the first repository to be cloned, and all others will be added 
as its submodules. Specifying more than one parent repo will cause an error.

Typcial usage might be as follows: 

	php install /var/www/html/moodle/ mymods.submod