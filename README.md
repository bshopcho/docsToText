# docsToText
A JavaScript library that extract text from documents without server upload in browser

You can extract text from doc, docx, xls, xlsx, ppt, pptx, pdf, hwp files. Take a look at the following example. It can be extracted very simply.

Parse on remote url download 

[example](https://www.docs-extractor.com)

```javascript
    const url = 'https://docs-extractor.com/sample/sample.docx';
    docToText(url, 'docx')
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

    docToText(file, ext).then(function (text) {
        // text
    }).catch(function (error) {
        // error
    });
```

Support Browser

Internet Explorer 11+ / Edge / Chrome / Safari / Firefox
