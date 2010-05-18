
<a name="markdownpreprocessor"></a>
Markdown Preprocessor
======================

The Markdown Preprocessor is a Python script designed to add extended features
on top of the excellent Markdown syntax defined by John Gruber.  These additions
are mainly focused on creating larger technical documents without needing to use
something as heavy and syntactically complex as Docbook.

1\.  [Features](#features)
2\.  [Support](#support)

<a name="features"></a>
1\. Features
--------

The biggest feature provided by markdown-pp is the generation of a table of
contents for a document, with each item linked to the appropriate section of the
markup.  The table is inserted into the document wherever the preprocessor finds
`!TOC` at the beginning of a line.  Named `<a>` tags are inserted above each
Markdown header, and the headings are numbered hierarchically based on the
heading tag that Markdown would generate.

Example file.mdpp:

	# Document Title

	!TOC

	## Header 1
	### Header 1.a
	## Header 2

The preprocessor would generate the following Markdown-ready document file.md:

	<a name="documenttitle"></a>
	# Document Title

	1\. [Header 1](#header1)
	1.1\. [Header 1.a](#header1a)
	2\. [Header 2](#header2)

	<a name="header1"></a>
	## Header 1
	<a name="header1a"></a>
	### Header 1.a
	<a name="header2"></a>
	## Header 2

<a name="support"></a>
2\. Support
-------

If you find any problems with Markdown-PP, or have any feature requests, please
report them to [my bugtracker][1], and I will respond when possible.  Code
cantributions are *always* welcome.

[1] http://leetcode.net/mantis
