How to create a windows-1252 CSV
================================

Microsoft Excel will open all CSV files with the windows-1252 encoding (also
called 'ansi'). Under certain circomstances (Microsoft Excel >= 2007 on
Windows), an UTF-8 encoded CSV with BOM might be correctly opened.

You can find in this repository an example of how to generate a CSV encoded in
windows-1252 directly in the browser. This example depends on two external
projects:

  * [stringencoding](https://github.com/inexorabletash/text-encoding) - a JS shim to implement http://encoding.spec.whatwg.org/#api
  * [FileSaver.js](https://github.com/eligrey/FileSaver.js) - a JS library to save Blob as file


stringencoding
--------------

The version in this repo is modified, a bug has been fixed (see
f859ae64c9244ba424151448b6133553d8f33e83), and most of the encoding have been
removed (except windows-1252 of course).
