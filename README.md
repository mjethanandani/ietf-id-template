This repository is a template for writing a new IETF individual submission. It has all the Makefiles, Dockerfiles, and other tools needed to build the draft. It has support for validating YANG modules that you may want to include in the draft.

# What do you need
To build the draft from this template, you need to have Docker installed and running on the machine where this repository will be cloned.

# Structure of the repository

The repository consists of the following

- Makefile
- Dockerfile
- start.sh
- src
- src/addstyle
- src/replace.sh
- src/download-dependent-modules.py
- src/validate-and-gen-trees.sh
- src/insert-figures.sh
- src/yang folder: consists of any YANG modules and instance examples for the YANG module
- draft
- draft/Makefile
- draft/draft-rfcxml-general-template-annotated.xml

# How to use this repository
## Create a clone

To use this repository, first clone it using the command

	`git clone https://github.com/mjethanandani/ietf-id-template.git`

## Create a tag

Next, create a git tag for the draft-xxx-yyy-zzz.xml as follows:

	`git tag draft-xxx-yyy-zzz-00`

This will tell 'make' what version of the draft to build

Remember to push the tag along with any other changes to the remote.

	`git push tag -a`
	
## Building the draft

To build the draft, type make in the root of the repository

	`make`	

	





