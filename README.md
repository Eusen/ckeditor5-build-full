CKEditor 5 Full Editor Build
========================================

[![npm version](https://badge.fury.io/js/%40ckeditor%2Fckeditor5-build-decoupled-document.svg)](https://www.npmjs.com/package/@ckeditor/ckeditor5-build-decoupled-document)
[![Build Status](https://travis-ci.org/ckeditor/ckeditor5-build-decoupled-document.svg?branch=master)](https://travis-ci.org/ckeditor/ckeditor5-build-decoupled-document)
<br>
[![Dependency Status](https://david-dm.org/ckeditor/ckeditor5-build-decoupled-document/status.svg)](https://david-dm.org/ckeditor/ckeditor5-build-decoupled-document)
[![devDependency Status](https://david-dm.org/ckeditor/ckeditor5-build-decoupled-document/dev-status.svg)](https://david-dm.org/ckeditor/ckeditor5-build-decoupled-document?type=dev)


![CKEditor 5 decoupled document editor build screenshot](https://c.cksource.com/a/1/img/npm/ckeditor5-build-decoupled-document.png)
![CKEditor 5 balloon editor build screenshot](https://c.cksource.com/a/1/img/npm/ckeditor5-build-balloon.png)
![CKEditor 5 balloon block editor build screenshot](https://c.cksource.com/a/1/img/npm/ckeditor5-build-balloon-block.png)
![CKEditor 5 classic editor build screenshot](https://c.cksource.com/a/1/img/npm/ckeditor5-build-classic.png)
![CKEditor 5 inline editor build screenshot](https://c.cksource.com/a/1/img/npm/ckeditor5-build-inline.png)

## Quick start

Use it in your JavaScript application:

```js
import CKEditor from './ckeditor';

// Or using the CommonJS version:
// const DecoupledEditor = require( './ckeditor' );

CKEditor
	.create( 'decoupled', document.querySelector( '#editor' ) , /** config {} */)
		.then( editor => {
			// The toolbar needs to be explicitly appended.
			document.querySelector( '#toolbar-container' ).appendChild( editor.ui.view.toolbar.element );

			window.editor = editor;
		} )
	.catch( err => {
		console.error( err.stack );
	} );
```

**Note:** If you are planning to integrate CKEditor 5 deep into your application, it is actually more convenient and recommended to install and import the source modules directly (like it happens in `ckeditor.js`). Read more in the [Advanced setup guide](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/advanced-setup.html).

## License

Licensed under the terms of [GNU General Public License Version 2 or later](http://www.gnu.org/licenses/gpl.html). For full details about the license, please check the `LICENSE.md` file or [https://ckeditor.com/legal/ckeditor-oss-license](https://ckeditor.com/legal/ckeditor-oss-license).
