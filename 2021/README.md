# OpenGRC XML version 2021
OpenGRC native XML file format, published in 2021

## Compatibility
The OpenGRC native XML file format is designed to facilitate easy transformation of data into XBRL, ReqIF, JSON or CSV formats.

## Schema index
### Metadata
- <https://xml.opengrc.org/2021/types.xsd>
- <https://xml.opengrc.org/2021/topics.xsd>
- <https://xml.opengrc.org/2021/relations.xsd>
- <https://xml.opengrc.org/2021/categories.xsd>
- <https://xml.opengrc.org/2021/suggestions.xsd>
- <https://xml.opengrc.org/2021/specification.xsd>

### Objects
- <https://xml.opengrc.org/2021/assets.xsd>
- <https://xml.opengrc.org/2021/products.xsd>
- <https://xml.opengrc.org/2021/threats.xsd>
- <https://xml.opengrc.org/2021/treatments.xsd>
- <https://xml.opengrc.org/2021/causes.xsd>
- <https://xml.opengrc.org/2021/sources.xsd>
- <https://xml.opengrc.org/2021/occurrences.xsd>
- <https://xml.opengrc.org/2021/audit.xsd>
- <https://xml.opengrc.org/2021/criteria.xsd>
- <https://xml.opengrc.org/2021/controls.xsd>
- <https://xml.opengrc.org/2021/requirements.xsd>

## Authoring and distribution

### Suggested authoring tools
- For simple purposes the functionality to export a spreadsheet to XML in Microsoft Excel or LibreOffice Calc are sufficient
- For full XML capabilities it is recommended to use a proper editor, like those found in this list: <https://en.wikipedia.org/wiki/Comparison_of_XML_editors>
- For complex authoring needs, the use of a dedicated authoring tool is highly recommended

### Understanding identifiers
- The ''identifier'' element serves the purpose to uniquely identify a particular element across versions and language versions
- The ''identifier'' element does not serve the same purpose as ''xml:id'', <https://www.w3.org/TR/xml-id/>
- Identifiers are used to link objects and metadata separately from the XML-intrinsic reference functionality
- The ''identifier'' field shall be set to a unique string to identify a particular item
- Identifiers in packages published for public consumption shall be IRIs, <https://tools.ietf.org/html/rfc3987>
  - Web addresses are valid, example: https://organization.tld/accounting/requirements/europe#article-52
  - Tip: Made-up web addresses are equally valid, use any scheme you want with your own domain names
- Identifiers should be URNs if they belong to an assigned namespace
  - IANA maintains an official list here: https://www.iana.org/assignments/urn-namespaces/urn-namespaces.xhtml
  - Examples: National legislation, ISO standards, books; structured schemes like OID or ucode
- Identifiers which are UUIDs can be formatted according to the URN scheme, <https://tools.ietf.org/html/rfc4122>
  - Example: urn:uuid:f81d4fae-7dec-11d0-a765-00a0c91e6bf6
  - Here is an online UUID generator: https://www.uuidgenerator.net/

### How to pack content for distribution:
1. Create content in compliance with the appropriate schemas using your favourite tool
3. Create a 'manifest.xml' file at the root folder in accordance with the schema <https://xml.opengrc.org/2021/package>
4. In the 'manifest.xml' document, add relative path to each file which belongs in the package assembly
5. Pack the files as a zip file archive (do not enable password protection)
6. Ensure that the file suffix is ''.opengrc'', rename it from ''.zip'' if required
7. Generate the MD5 checksum for your distribution package, publish the checksum on your webside
