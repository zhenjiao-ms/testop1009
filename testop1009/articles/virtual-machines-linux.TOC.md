# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-quick-create-portal.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-quick-create-cli.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://azure.microsoft.com/pricing/free-trial/)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](xplat-cli-install.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-mac-create-ssh-keys.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-add-disk.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-attach-disk-portal.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-cli-ps-findimage.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-cli-vmss-create.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-create-cli-complete.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-create-ssh-secured-vm-from-template.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-docker-machine.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-nsg-quickstart.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-using-cloud-init.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-using-vmaccess-extension.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](guidance-compute-single-vm-linux.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-containers.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-azure-overview.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-create-upload-generic.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-creation-choices.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-endorsed-distros.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-manage-availability.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machine-scale-sets-overview.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-sizes.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-use-root-privileges.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-a8-a9-a10-a11-specs.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-compare-deployment-models.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-infrastructure-availability-sets-guidelines.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-infrastructure-example.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-infrastructure-naming-guidelines.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-infrastructure-networking-guidelines.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-infrastructure-resource-groups-guidelines.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-infrastructure-storage-solutions-guidelines.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-infrastructure-subscription-accounts-guidelines.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-infrastructure-virtual-machine-guidelines.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-planned-maintenance.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-planned-maintenance-schedule.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-agent-user-guide.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-app-frameworks.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-capture-image.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-cli-deploy-templates.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-copy-vm.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-create-upload-centos.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-create-upload-ubuntu.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-debian-create-upload-vhd.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-prepare-oracle.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-redhat-create-upload-vhd.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-update-infrastructure-redhat.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](azure-security-disk-encryption.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-cli-migration-classic-resource-manager.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-migration-classic-resource-manager-deep-dive.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-unique-vm-id.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-vm-monitoring.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-dockerextension.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-extensions-authoring-templates.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-extensions-configuration-samples.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-extensions-customscript.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-extensions-features.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-extensions-troubleshoot.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-tag.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-sap-dbms-guide.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-sap-deployment-guide.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-sap-get-started.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-sap-planning-guide.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-sap-on-suse-quickstart.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](storage-azure-cli.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](storage-how-to-use-files-linux.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-about-disks-vhds.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-configure-lvm.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-configure-raid.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](load-balancer-get-started-internet-arm-ps.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-networks-overview.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-portal-create-fqdn.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-network-create-udr-arm-cli.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-networks-create-nsg-arm-cli.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-networks-create-vnet-arm-cli.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-allocation-failure.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-extensions-troubleshoot.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-troubleshoot-app-connection.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-troubleshoot-ssh-connection.md)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](azure-cli-arm-commands.md)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://msdn.microsoft.com/en-us/library/azure/mt163647)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://msdn.microsoft.com/en-us/library/azure/mt163658)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://msdn.microsoft.com/en-us/library/azure/dd179355)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://azure.microsoft.com/documentation/templates/)
# Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://azure.microsoft.com/documentation/articles/?product=virtual-machines-linux&tag=azure-service-management)
## [Usage : xmllint [options] XMLfiles ...
	Parse the XML files and output the result of the parsing
	--version : display the version of the XML library used
	--debug : dump a debug tree of the in-memory document
	--shell : run a navigating shell
	--debugent : debug the entities defined in the document
	--copy : used to test the internal copy implementation
	--recover : output what was parsable on broken XML documents
	--huge : remove any internal arbitrary parser limits
	--noent : substitute entity references by their value
	--noenc : ignore any encoding specified inside the document
	--noout : don't output the result tree
	--path 'paths': provide a set of paths for resources
	--load-trace : print trace of all external entities loaded
	--nonet : refuse to fetch DTDs or entities over network
	--nocompact : do not generate compact text nodes
	--htmlout : output results as HTML
	--nowrap : do not put HTML doc wrapper
	--valid : validate the document in addition to std well-formed check
	--postvalid : do a posteriori validation, i.e after parsing
	--dtdvalid URL : do a posteriori validation against a given DTD
	--dtdvalidfpi FPI : same but name the DTD with a Public Identifier
	--timing : print some timings
	--output file or -o file: save to a given file
	--repeat : repeat 100 times, for timing or profiling
	--insert : ad-hoc test for valid insertions
	--compress : turn on gzip compression of output
	--html : use the HTML parser
	--xmlout : force to use the XML serializer when using --html
	--nodefdtd : do not default HTML doctype
	--push : use the push mode of the parser
	--pushsmall : use the push mode of the parser using tiny increments
	--memory : parse from memory
	--maxmem nbbytes : limits memory allocation to nbbytes bytes
	--nowarning : do not emit warnings from parser/validator
	--noblanks : drop (ignorable?) blanks spaces
	--nocdata : replace cdata section with text nodes
	--format : reformat/reindent the input
	--encode encoding : output in the given encoding
	--dropdtd : remove the DOCTYPE of the input docs
	--pretty STYLE : pretty-print in a particular style
	                 0 Do not pretty print
	                 1 Format the XML content, as --format
	                 2 Add whitespace inside tags, preserving content
	--c14n : save in W3C canonical format v1.0 (with comments)
	--c14n11 : save in W3C canonical format v1.1 (with comments)
	--exc-c14n : save in W3C exclusive canonical format (with comments)
	--nsclean : remove redundant namespace declarations
	--testIO : test user I/O support
	--catalogs : use SGML catalogs from $SGML_CATALOG_FILES
	             otherwise XML Catalogs starting from 
	         file:///etc/xml/catalog are activated by default
	--nocatalogs: deactivate all catalogs
	--auto : generate a small doc on the fly
	--xinclude : do XInclude processing
	--noxincludenode : same but do not generate XInclude nodes
	--nofixup-base-uris : do not fixup xml:base uris
	--loaddtd : fetch external DTD
	--dtdattr : loaddtd + populate the tree with inherited attributes 
	--stream : use the streaming interface to process very large files
	--walker : create a reader and walk though the resulting doc
	--pattern pattern_value : test the pattern support
	--chkregister : verify the node registration code
	--relaxng schema : do RelaxNG validation against the schema
	--schema schema : do validation against the WXS schema
	--schematron schema : do validation against a schematron
	--sax1: use the old SAX1 interfaces for processing
	--sax: do not build a tree but work just at the SAX level
	--oldxml10: use XML-1.0 parsing rules before the 5th edition
	--xpath expr: evaluate the XPath expression, imply --noout

Libxml project home page: http://xmlsoft.org/
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-linux-opensource-links.md)
