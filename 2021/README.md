# OpenGRC XML version 2021
OpenGRC native XML file format, published in 2021

## Compatibility
The OpenGRC native XML file format is designed to facilitate easy transformation of data into XBRL, ReqIF, JSON or CSV formats.

## Schema index
### Metadata
- <https://xml.opengrc.org/2021/types>
- <https://xml.opengrc.org/2021/topics>
- <https://xml.opengrc.org/2021/relations>
- <https://xml.opengrc.org/2021/categories>
- <https://xml.opengrc.org/2021/suggestions>
- <https://xml.opengrc.org/2021/specification>

### Objects
- <https://xml.opengrc.org/2021/assets>
- <https://xml.opengrc.org/2021/products>
- <https://xml.opengrc.org/2021/threats>
- <https://xml.opengrc.org/2021/treatments>
- <https://xml.opengrc.org/2021/causes>
- <https://xml.opengrc.org/2021/sources>
- <https://xml.opengrc.org/2021/occurrences>
- <https://xml.opengrc.org/2021/audits>
- <https://xml.opengrc.org/2021/controls>
- <https://xml.opengrc.org/2021/requirements>

## Authoring and distribution

### Suggested authoring tools
- For simple purposes the functionality to export a spreadsheet to XML in Microsoft Excel or LibreOffice Calc are sufficient
- For full XML capabilities it is recommended to use a proper editor, like those found in this list: <https://en.wikipedia.org/wiki/Comparison_of_XML_editors>
- For complex authoring needs, the use of a dedicated authoring tool is highly recommended

### Understanding identifiers
- The ''identifier'' element serves the purpose to uniquely identify a particular element across versions and language versions
- The ''identifier'' element does not serve the same purpose as ''xml:id'', <https://www.w3.org/TR/xml-id/>
- The ''identifier'' field should be set to a globally unique string to uniquely identify a particular class or instance
- Identifiers in packages published for public consumption should be URNs, <https://tools.ietf.org/html/rfc8141>
- Identifiers in packages for internal use can be UUIDs, <https://tools.ietf.org/html/rfc4122>
- Identifiers in packages for internal that are UUIDs use also be URNs, <https://tools.ietf.org/html/rfc4122>
- Identifiers are used to link objects and metadata separately from the XML-intrinsic reference functionality

### How to pack content for distribution:
1. Create content in compliance with the appropriate schemas using your favourite tool
3. Create a 'manifest.xml' file at the root folder in accordance with the schema <https://xml.opengrc.org/2021/package>
4. In the 'manifest.xml' document, add relative path to each file which belongs in the package assembly
5. Pack the files as a zip file archive (do not enable password protection)
6. Ensure that the file suffix is ''.opengrc'', rename it from ''.zip'' if required
7. Generate the MD5 checksum for your distribution package, publish the checksum on your webside
