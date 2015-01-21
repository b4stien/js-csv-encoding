How to create a windows-1252 CSV
================================

Microsoft Excel will open all CSV files with the `windows-1252` encoding (also
called `ansi`). Under certain circomstances (Microsoft Excel >= 2007 on
Windows), an `UTF-8` encoded CSV with BOM might be correctly opened.

You can find in this repository an example of how to generate a CSV encoded in
`windows-1252` directly in the browser. This example depends on two external
projects:

  * [text-encoding](https://github.com/inexorabletash/text-encoding) - a JS shim to implement the [Encoding Living Standard](http://encoding.spec.whatwg.org/)
  * [FileSaver.js](https://github.com/eligrey/FileSaver.js) - a JS library to save Blob as file


text-encoding
-------------

The version in this repo is slightly modified one. The
[Encoding Living Standard](http://encoding.spec.whatwg.org/) does not specify
how to encode to `windows-1252`, hence the modifications at the end of
`encoding.js` and the call to `CustomTextEncoder` (with a special flag) instead
of `TextEncoder`.

For more rational about this, see https://github.com/inexorabletash/text-encoding#non-standard-behavior.
