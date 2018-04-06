# Portable Executable Inspection

## Toolkit
[PE Insider](http://cerbero.io/peinsider/)
* PE Insider is a free Portable Executable viewer for the community.

[NTCore Explorer Suite](http://www.ntcore.com/exsuite.php)
* Created by Daniel Pistelli, a freeware suite of tools including a PE editor called CFF Explorer and a process viewer. The PE editor has full support for PE32/64. Special fields description and modification (.NET supported), utilities, rebuilder, hex editor, import adder, signature scanner, signature manager, extension support, scripting, disassembler, dependency walker etc

[pestudio](https://www.winitor.com/index.html)
* a powerful parser and a flexible set of configuration files that are used to detect various types of indicators and determine thresholds.

[PEiD](https://www.aldeid.com/wiki/PEiD)
* detect packers, cryptors and compilers found in PE executable files – its detection rate is higher than that of other similar tools since the app packs more than 600 different signatures in PE files.

[Frhed](http://frhed.sourceforge.net/en/)
* Frhed is an binary file editor for Windows. It is small but has many advanced features like ability to load big files partially.

[GNU File](http://gnuwin32.sourceforge.net/packages/file.htm)
* GNU file can be used to determine the filetype. Built-in to Linux or Mac OS X.

[Exeinfo PE](http://exeinfo.pe.hu/)
* Analyzes Windows PE header information, packer detection, provides hints on how to unpack.

[UPX](https://upx.github.io/)
* UPX is a free, portable, extendable, high-performance executable packer for several executable formats.

[TrID](http://mark0.net/soft-trid-e.html)
* Uses pattern database to determine filetype, gives likelihood of detected type.

## File Analysis

Portable Executable files begin or end with specific sequences known as `Magic Bytes`. Most Windows PE's will have `MZ` for the first two bytes. This will sometimes be followed by a statement such as `This program cannot be run in DOS mode.`, but this is not _always_ the case.

### File Signatures to Know

| File | Signature |
|---|---|
|PE (portable executable)|`MZ` in bytes 0-1|
|PDF (portable document format)|`%PDF-` followed by number within first 1024 bytes|
|Old office document (Microsoft Compound Binary Format)|`0xD0CF11E0` (DOCFILE)|
|Zip archive| "PK" in bytes 0-1|

