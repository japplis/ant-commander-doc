# Multiple files rename

Multiple file rename is only available in [Ant Commander Pro file manager](https://www.antcommander.com/)

Note that the extension is not included when renaming multiple files. Use rename extension action for that.

## How to rename files?

- In a table with file, choose _File -> Rename multiple files_
- Select the files you want to rename
- If not files are selected, all listed files will be used
- Just perform a find / replace for what you want to change in the files names
- Note that file extension is not including in the rename, use _File -> Rename extension_ for it

## Advanced rename files
You can use regular expression with the _Reg Exp_ button to perform for advanced rename.

| Rename | Find | Replace | Examples |
| ------ | ---- | ------- | -------- |
| Prefix files | ^ | prefix- | image001.jpg -> prefix-image001.jpg |
| Suffix files | $ | -suffix | image001.jpg -> image001-suffix.jpg |
| Groups | (\[a-zA-Z\]+)(\d+) | $1-$2 | image001.jpg -> image-001.jpg |
| Use file name | .+ | $0-test | image001.jpg -> image001-test.jpg |

More about regular expression pattern [here](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/regex/Pattern.html)</a>

> Note: Do NOT use _.*_ but _.+_ to match the file name in the regular expression

> If no groups are created in the regular expression with parenthesis, only $0 can be used to represent the text matching the regular expression

### Special replacement

- _%DIRNAME%_ Use the parent directory name
- _%DIRNAME:-x%_ Use the xth parent of the file directory (e.g. %DIRNAME:-2% this/is/a/test/file.txt would output 'is')
- _%DIRNAME:x%_ Use the xth child to the file from the base directory (e.g. %DIRNAME:3% this/is/a/test/file.txt would output 'a')
- _%DATE:yyyy-MM-dd-HH-mm.ss%_ Use the file last modified date/time in the name. See [Date Time Patterns](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/time/format/DateTimeFormatter.html)

Special replacement will work with regular expression on and off.

### Rename with directory changes

By default multiple rename will use the file name without the extension.

If in the _Find_ the '/' character is used, the relative path is used instead.<br>
e.g. if _test/file.txt_ is selected, Find _test/_ Replace with _test-_ will move the file to test-file.txt in the base directory.

If in the _Replace with_ field the '/' character is used, the output will consired it as a folder specification.<br>
e.g. if _Invoice-Company-12345.pdf_ is selected, Find _Invoice-([A-Za-z]+)-_ (Reg Exp) Replace with _$1/$0_ will move the file to Company/Invoice-Company-12345.pdf.

### Special changes

Use _Special rename multiple files_ action to replace based on:
- Truncate file name to a maximum number of character
- Change the case of the file name (e.g. to lowercase)
- Add a counter at the end of the file
- Remove accents and diacritics in file names

  Note that if you want to remove all specific non-ascii characters, you can do a find \p{M} replace with nothing in the regular multi-rename tool with regular expression enabled.
- File mapping

  The mapping should be in the form of _Filename1->NewName1;Filename2->NewName2;..._

  You can click on the edit button next to the field to make it easier to enter the mapping.

  In the edit text field you can use **tabs** as separator between old filename and new filename to it makes it easier to import the mapping from Excel or another table tool.
