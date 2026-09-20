---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

![Likha Control Room - Queue Management](../../images/control-room-queues.png)

## File Actions activities

File Actions activities work with files on disk. Some actions save a Boolean result variable, while text actions read or write file contents.

### File Actions > Move File

Moves a file into a destination folder.

Properties:

```txt
File path             file to move
Destination Folder    folder where the file will be moved
fileMoved             Boolean output variable
```

### File Actions > Rename File

Renames a file in its current folder.

Properties:

```txt
File path to rename   file to rename
new File name         new file name, including extension
RenamedFile           Boolean output variable
```

### File Actions > Delete File

Deletes a file.

Properties:

```txt
File path to delete   file to delete
DeletedFile           Boolean output variable
```

### File Actions > If file exists

Checks whether a file or path exists.

Properties:

```txt
Filepath      path to check
FileExist     Boolean output variable
```

### File Actions > Read Text from File

Reads text from a file and saves it to a Text variable.

Properties:

```txt
File path        file to read
Output Text      Text output variable
Encoding         System Default, ASCII, Unicode, or UTF-8
```

### File Actions > Write text to file

Writes text to a file. Parent folders are created automatically when needed.

Properties:

```txt
File Path        file to write
Text to write    text content
Encoding         System Default, ASCII, Unicode, or UTF-8
```

Notes:

- Output variables are set to `true` when the action succeeds.
- Output variables are set to `false` when the action cannot be completed.
- Error handling supports Retry on error, Stop with error, Resume next, and Go To label.
- `Read Text from File` saves the file contents into the selected output variable.
- `Write text to file` overwrites the target file contents.
- File paths can use variables such as `{{input_file}}`.
