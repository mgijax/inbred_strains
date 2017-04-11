# inbred_strains
Pages for inbred strains of mice and rats, formatted for the web using data from Festing.

## quick overview
This directory contains scripts for administering the inbred strains listing
by M.F. Festing.  These were moved out of the wi_pg product that we are
workign to retire.  The scripts are:

findStrains : attempts to locate strain headings in .rtf file
doit : script that runs the following other scripts
    preprocess	: turns "full" rtf into "pidgin" rtf
    parse	: turns pidgin rtf into html (plus a diagnostics file)
    postprocess	: summarizes diagnostics

Since there is now both a mouse and a rat strain listing, the 'doit' script
takes a single argument, either 'mouse' or 'rat'.

The product subdirectories are structured as follows:

inbred_strains/admin/		# -- scripts for doing the work
	    doit
	    findStrains
	    fixLength
	    indexStrains
	    parse
	    postprocess
	    preprocess

inbred_strains/data/		# -- source data are stored here
	mouse/
		source.rtf
	rat/
		source.rtf

inbred_strains/www/		# -- www files stored here
	include/
	    (has links to html include files)
	mouse/
	    INTRO.shtml
	    REFS.shtml
	    STRAINS.shtml
	    docs/
		*.shtml
	        include (has links to html include files)
	rat/
	    INTRO.shtml
	    REFS.shtml
	    STRAINS.shtml
	    include (has links to html include files)
	    docs/
		*.shtml
	        include (has links to html include files)
	
The inbred_strains/admin/ directory includes scripts for building the strain
docs from the original rtf files. 
