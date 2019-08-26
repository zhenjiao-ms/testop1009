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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://azure.microsoft.com/documentation/learning-paths/virtual-machines/)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](resource-manager-template-walkthrough.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-connect-logon.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-creation-choices.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-faq.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-hero-tutorial.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://azure.microsoft.com/pricing/free/)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](powershell-install-configure.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-guidance-compute-single-vm.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](choose-web-site-cloud-service-vm.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](resource-group-overview.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-about.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-containers.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-compare-deployment-models.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-endpoints-in-resource-manager.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-load-balance.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](resource-group-rbac.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-a8-a9-a10-a11-specs.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-hybrid-use-benefit-licensing.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-infrastructure-service-guidelines.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-manage-availability.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-multiple-vms.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-planned-maintenance.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-sizes.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-app-frameworks.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-capture-image.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-chef-automation.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-cli-ps-findimage.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-create-availability-set.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-csharp-template.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-extensions-diagnostics-template.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-prepare-for-upload-vhd-image.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-ps-create.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-ps-template.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-specialized-image.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-upload-image.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-vmss-powershell-creating.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-migration-classic-resource-manager.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-migration-classic-resource-manager-deep-dive.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-ps-migration-classic-resource-manager.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](backup-azure-vms-first-look-arm.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](backup-azure-vms-automation.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](resource-group-using-tags.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-csharp-manage.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-cli-deploy-templates.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-extensions-dsc-credentials.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-key-vault-setup.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-ps-manage.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-winrm.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-networks-arm-asm-s2s-howto.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-cli-manage.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-move-vm.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-nsg-quickstart-portal.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-nsg-quickstart-powershell.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-portal-create-fqdn.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-ps-common-ref.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-reset-rdp.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-tag.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-extensions-authoring-templates.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-extensions-configuration-samples.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-extensions-customscript.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-extensions-dsc-overview.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-extensions-features.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-extensions-troubleshoot.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-sql-server-iaas-overview.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-hpcpack-cluster-options.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-lob.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-matlab-mdcs-cluster.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-sharepoint-farm.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-about-disks-vhds.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-attach-disk-portal.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-classic-change-drive-letter.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-detach-disk.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-expand-os-disk.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-networks-create-nsg-arm-pportal.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-ps-common-network-ref.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-allocation-failure.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-redeploy-to-new-node.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-restart-resize-error-troubleshooting.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-troubleshoot-app-connection.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-troubleshoot-deployment-new-vm.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-troubleshoot-rdp-connection.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](resource-group-authoring-templates.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-csharp.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](vs-azure-tools-resource-groups-deployment-projects-create-deploy.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://msdn.microsoft.com/en-us/library/azure/mt131911)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://msdn.microsoft.com/en-us/library/azure/dn973320)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://msdn.microsoft.com/en-us/library/azure/mt125979)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://msdn.microsoft.com/en-us/library/azure/mt131037)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://msdn.microsoft.com/en-us/library/azure/mt705635)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://azure.microsoft.com/documentation/articles/?product=virtual-machines-windows&tag=azure-service-management)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](virtual-machines-windows-index/#windows-vms-in-the-classic-deployment-model.md)
