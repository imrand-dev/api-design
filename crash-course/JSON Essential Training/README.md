## JSON Essential Training — Sasha Vodnik

<a href="https://www.linkedin.com/learning/json-essential-training">
<img src="https://i.ibb.co/2dWWfkk/image.png" alt="json-training">
</a>

### JSON Variants

* web page — https://www.json.org/json-en.html
* Wiki Page — https://en.wikipedia.org/wiki/JSON
* Python — https://docs.python.org/3/library/json.html
* JavaScript — https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON
* JSON with comments — https://github.com/komkom/jsonc
* JSON-P — https://en.wikipedia.org/wiki/JSONP
* JSON-LD [semantic markup] — https://json-ld.org/
* JSON5 – JSON for Humans - https://json5.org/

### JSON Rules

* `""` for keys and values.
* JSON objects starts with `{}`.
* JSON arrays starts with `[]`.
* No leading zeros `0` in number.
* No trailing decimals in number.
* No trailing comma.
* No comments.
* No circular reference.

### JSON vs JavaScript

if zero is significant in front of number in JSON then make them as string `"01"`

```js
// JSON
{
    "filename": "contacts.pdf",
    "version": 2,
    "sequence": 1,
    "approved": true
}
```

```js
// JavaScript Object
{
    filename: 'contacts.pdf',
    approved: true,
    sequence: 01, // valid
    version: 2., // valid
}
```

### Conversion

* JSON to JavaScript Object `JSON.parse(string [,reviver]);`
* JavaScript Object to JSON `JSON.stringify(value [,replacer, space]);` 
* JSON to Python Dictionary `json.loads(strings)`
* Python Dictionary to JSON `json.dumps(dicts)`    

Other available formats are `YAML, XML, CSV`.

### Convert XML to JSON

* xml2json — http://goessner.net/ 
* XML String to DOM Node
    * `let peopleDataNode = (new DomParser()).parseFromString(rawData, "text/xml");`
* DOM Node to JSON
    * `let ConvertedData = xml2json(peopleDataNode, "");`
* JSON to Object
    * `let parseData = JSON.parse(convertedData);`

### JSON Schema

* Web Page — https://json-schema.org/
* Create Schema from JSON — https://jsonschema.net/app/schemas/0
* Validate Schema — https://www.jsonschemavalidator.net/
* JSON Formatter — https://jsonformatter.org/

```js
{
    "$schema": "http://json-schema.org/draft-07/schema#",
    "$id": "http://example.com/schemas/products.json",
    "title": "h+ Sport Products",
    "description": "Schema for h+ Sport product data",
    "type": "array",
    "items": {
        "type": "object",
        "properties": {
            "id": {
                "type": "string"
            },
            "name": {
                "type": "string"
            },
            "description": {
                "type": "string"
            },
            "image_title": {
                "type": "string"
            },
            "image": {
                "type": "string"
            }
        }
    }
}
```
