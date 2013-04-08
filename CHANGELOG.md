Change log
==========

Version 0.3.2 - 8 Apr 2013
------------------------

matonb:
* 0.3.1 Patched - Serious Problem:  SanitizeTextFiles If logic removed all lines containing "Begin".
* 0.3.2 Replaced if block for skipping code sections in SanitizeTextFiles with regular expression.

Version 0.3 - 6 Apr 2013
------------------------

bkidwell:
* Sanitize query exports.
* Fixed SERIOUS TYPO in UCS2-to-UTF-8 conversion (wrong threshold for 2 byte versus 3 byte symbol in output stream).
* AggressiveSanitize default True.

matonb:
* Added AggressiveSanitize constant, it's a number to allow for different levels in the future. ~~Default False.~~
* Added Skipping for GUID & Namemap in aggressive sanitize mode.
* ~~If AggressiveSanitize is on, also sanitize query exports.~~
* Append Number of objects imported/exported to information lines in immediate window.
* Updated readme (removed references to terminal window).
* Close all open forms and reports when importing and exporting because you can't import an open form or report.

Version 0.2 - 4 Apr 2013
------------------------

matonb:
* Added dbLongBinary "DOL" to SkipList in SanitizeTextFiles.
* Added Source directory check to ImportAllSource, pops up a message box if missing.
* Only create source directories if there is something to export.

bkidwell:
* Removed external executable for converting UCS-2-little-endian to and from UTF-8; replaced with VB6 methods.
* Added demo database to the repository.
* Removed the need for a special "export_[name]" query to export and import a lookup table.
* Added check to determine if Queries, Forms, etc. are exported from THIS database (depending on which version of Access created it) uses UCS-2-little-endian, or a legacy 8-bit Windows character set. Skip converting to/from UTF-8 if not using UCS-2, because the point of the conversion was to avoid writing 0x00 bytes in the text files and confuse diff/merge tools.

Version 0.1 - 22 Oct 2012
-------------------------

Initial release
