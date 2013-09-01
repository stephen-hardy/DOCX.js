DOCX.js
=======

DOCX.js is a JavaScript library for converting the data in base64 DOCX files into HTML - and back! Please note that this library is licensed under the Microsoft Office Extensible File License - a license NOT approved by the OSI. While this license is based off of the MS-PL, which is OSI-approved, there are significant differences.

mceDocx.js
==========

Docx.js for tinyMCE

This is a modified version of docx.js from [https://github.com/stephen-hardy/docx.js](https://github.com/stephen-hardy/docx.js).

## Dependencies
  
  * JsZip.js

## How to

    <html>
	<head>
		<script type="text/javascript" src="jszip/test/jquery-1.8.3.min.js"></script>
		<script src="jszip/jszip.js"></script>
		<script src="jszip/jszip-deflate.js"></script>
		<script src="jszip/jszip-inflate.js"></script>
		<script src="jszip/jszip-load.js"></script>
		<script src="docx.js"></script>
		<script type="text/javascript" src="tinymce/js/tinymce/tinymce.min.js"></script>
		<script type="text/javascript">
		tinymce.init({
			element_format : "xhtml",
		 selector: "textarea#elm1",
		 plugins: ['save'],
		 toolbar: "save",
		 save_enablewhendirty: true,
    		 save_onsavecallback: function() {
    			var tempit = docx(tinymce.activeEditor.getBody());
    			window.location.href = tempit.href();
    		}
 		});
		</script>
	</head>
	<body>
		<textarea id="elm1" name="area"></textarea>
	</body>
	</html>

