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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://azure.microsoft.com/services/websites/)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](app-service-how-works-readme.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-php-web-site-gallery.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-java-get-started.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-create-deploy.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-dotnet-get-started.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](app-service-web-php-get-started.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-python-create-deploy-django-app.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](app-service-web-nodejs-get-started.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](documentdb-nodejs-application.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](link:http://blog.syntaxc4.net/post/2012/07/26/accessing-app-settings-configured-in-windows-azure-web-sites-using-php-and-node-js.aspx)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-hybrid-connection-get-started.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-integrate-with-vnet.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-authentication-authorization.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-dotnet-deploy-aspnet-mvc-app-membership-oauth-sql-database.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-deploy.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-staged-publishing.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](cloud-services-continuous-delivery-use-vso.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](link:http://blogs.msdn.com/b/tomholl/archive/2014/11/10/a-b-testing-with-azure-websites.aspx)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-configure-ssl-certificate.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-custom-domain-name.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-security.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-publish-source-control.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-java-get-started.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](app-service-deployment-readme.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-traffic-manager.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-scale/#scalingstandard.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](cdn-websites-with-cdn.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](app-service-scale-readme.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-scale.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](install-configure-powershell.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](command-line-tools/#Commands_to_manage_your_web_sites.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://msdn.microsoft.com/en-us/library/azure/dn602775)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-backup.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](app-service-web-test-in-production-get-start.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](https://azure.microsoft.com/blog/2014/12/09/azure-hdinsight-introduces-built-in-integration-with-azure-websites-to-do-web-log-analytics/)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-monitor.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-enable-diagnostic-log.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](web-sites-dotnet-troubleshoot-visual-studio.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](websites-webjobs-resources.md)
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
To report bugs or get some help check: http://xmlsoft.org/bugs.html](link:http://microsoftazurewebsitescheatsheet.info/)
