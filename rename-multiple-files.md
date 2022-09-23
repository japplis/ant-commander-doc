# Multiple file rename

Multiple file rename is only available in [Ant Commander Pro file manager](https://www.antcommander.com/)

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

More about regular expression pattern [here](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/regex/Pattern.html)</a>

### Special replacement

- _%DIRNAME%_ Use the parent directory name
- _%DATE:yyyy-MM-dd-HH-mm.ss%_ Use the file last modified date/time in the name. See [Date Time Patterns](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/time/format/DateTimeFormatter.html)

### Special changes

Use _Special rename multiple files_ action to replace based on:
- Truncate file name to a maximum number of character
- Change the case of the file name (e.g. to lowercase)
- Add a counter at the end of the file
- Remove accents and diacritics in file names
