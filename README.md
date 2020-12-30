# docsToText
A JavaScript library that extract text from documents without server upload in browser

You can extract text from doc, docx, xls, xlsx, ppt, pptx, pdf, hwp files. Take a look at the following example. It can be extracted very simply.

Parse on remote url download 

[example](https://www.docs-extractor.com)

```javascript
const docToText = new DocToText();
const url = 'https://docs-extractor.com/sample/sample.docx';

// single file extract to text
docToText.extractToText(url, 'docx')
    .then(function (text) {
        // text
    }).catch(function (error) {
        // error
    });
```

Parse on local upload file

```javascript
const file = files[0];
const {name} = file;
const ext = name.toLowerCase().substring(name.lastIndexOf('.') + 1);

const docToText = new DocToText();

// single file extract to text
docToText.extractToText(file, ext)
    .then(function (text) {
        // text
    }).catch(function (error) {
        // error
    });
```

Parse on remote zip url download

```javascript
const docToText = new DocToText();
const url = 'https://docs-extractor.com/sample/sample.zip';

// single zip file extract to text
docToText.extractZipToText(url)
    .then(function (text) {
        // text
    }).catch(function (error) {
        // error
    });
```

Parse on local upload zip file

```javascript
const docToText = new DocToText();
const url = 'https://docs-extractor.com/sample/sample.zip';

const file = files[0];
const docToText = new DocToText();

// single zip file extract to text
docToText.extractZipToText(file)
    .then(function (text) {
        // text
    }).catch(function (error) {
        // error
    });
```

Support Browser

Internet Explorer 11+ / Edge / Chrome / Safari / Firefox
