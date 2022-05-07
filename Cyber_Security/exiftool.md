# Exiftool
[Back to cyber security page](./index.md)

---

## What is 
exiftool - Read and write meta information in files

---

## Options
exiftool [OPTIONS] -tagsFromFile SRCFILE [-[DSTTAG<]SRCTAG...] FILE...

```bash
  -TAG or --TAG                    Extract or exclude specified tag
  -TAG[+-^]=[VALUE]                Write new value for tag
  -TAG[+-]<=DATFILE                Write tag value from contents of file
  -TAG[+-]<SRCTAG                  Copy tag value (see -tagsFromFile)

  -tagsFromFile SRCFILE            Copy tag values from file
  -x TAG      (-exclude)           Exclude specified tag
```

- Input-output text formatting

```bash
  -args       (-argFormat)         Format metadata as exiftool arguments
  -b          (-binary)            Output metadata in binary format
  -c FMT      (-coordFormat)       Set format for GPS coordinates
  -charset [[TYPE=]CHARSET]        Specify encoding for special characters
  -csv[[+]=CSVFILE]                Export/import tags in CSV format
  -csvDelim STR                    Set delimiter for CSV file
  -d FMT      (-dateFormat)        Set format for date/time values
  -D          (-decimal)           Show tag ID numbers in decimal
  -E,-ex,-ec  (-escape(HTML|XML|C))Escape tag values for HTML, XML or C
  -f          (-forcePrint)        Force printing of all specified tags
  -g[NUM...]  (-groupHeadings)     Organize output by tag group
  -G[NUM...]  (-groupNames)        Print group name for each tag
  -h          (-htmlFormat)        Use HTML formatting for output
  -H          (-hex)               Show tag ID numbers in hexadecimal
  -htmlDump[OFFSET]                Generate HTML-format binary dump
  -j[[+]=JSONFILE] (-json)         Export/import tags in JSON format
  -l          (-long)              Use long 2-line output format
  -L          (-latin)             Use Windows Latin1 encoding
  -lang [LANG]                     Set current language
  -listItem INDEX                  Extract specific item from a list
  -n          (--printConv)        No print conversion
  -p FMTFILE  (-printFormat)       Print output in specified format
  -php                             Export tags as a PHP Array
  -s[NUM]     (-short)             Short output format
  -S          (-veryShort)         Very short output format
  -sep STR    (-separator)         Set separator string for list items
  -sort                            Sort output alphabetically
  -struct                          Enable output of structured information
  -t          (-tab)               Output in tab-delimited list format
  -T          (-table)             Output in tabular format
  -v[NUM]     (-verbose)           Print verbose messages
  -w[+|!] EXT (-textOut)           Write (or overwrite!) output text files
  -W[+|!] FMT (-tagOut)            Write output text file for each tag
  -Wext EXT   (-tagOutExt)         Write only specified file types with -W
  -X          (-xmlFormat)         Use RDF/XML output format
```

- Processing control
- 
```bash
  -a          (-duplicates)        Allow duplicate tags to be extracted
  -e          (--composite)        Do not generate composite tags
  -ee[NUM]    (-extractEmbedded)   Extract information from embedded files
  -ext[+] EXT (-extension)         Process files with specified extension
  -F[OFFSET]  (-fixBase)           Fix the base for maker notes offsets
  -fast[NUM]                       Increase speed when extracting metadata
  -fileOrder[NUM] [-]TAG           Set file processing order
  -i DIR      (-ignore)            Ignore specified directory name
  -if[NUM] EXPR                    Conditionally process files
  -m          (-ignoreMinorErrors) Ignore minor errors and warnings
  -o OUTFILE  (-out)               Set output file or directory name
  -overwrite_original              Overwrite original by renaming tmp file
  -overwrite_original_in_place     Overwrite original by copying tmp file
  -P          (-preserve)          Preserve file modification date/time
  -password PASSWD                 Password for processing protected files
  -progress[:[TITLE]]              Show file progress count
  -q          (-quiet)             Quiet processing
  -r[.]       (-recurse)           Recursively process subdirectories
  -scanForXMP                      Brute force XMP scan
  -u          (-unknown)           Extract unknown tags
  -U          (-unknown2)          Extract unknown binary tags too
  -wm MODE    (-writeMode)         Set mode for writing/creating tags
  -z          (-zip)               Read/write compressed information
```

- Other options

```bash
  -@ ARGFILE                       Read command-line arguments from file
  -k          (-pause)             Pause before terminating
  -list[w|f|wf|g[NUM]|d|x]         List various exiftool capabilities
  -ver                             Print exiftool version number
  --                               End of options
```

- Special features

```bash
  -geotag TRKFILE                  Geotag images from specified GPS log
  -globalTimeShift SHIFT           Shift all formatted date/time values
  -use MODULE                      Add features from plug-in module
```

- Utilities

```bash
  -delete_original[!]              Delete "_original" backups
  -restore_original                Restore from "_original" backups
```

- Advanced options

```bash
  -api OPT[[^]=[VAL]]              Set ExifTool API option
  -common_args                     Define common arguments
  -config CFGFILE                  Specify configuration file name
  -echo[NUM] TEXT                  Echo text to stdout or stderr
  -efile[NUM][!] ERRFILE           Save names of files with errors
  -execute[NUM]                    Execute multiple commands on one line
  -list_dir                        List directories, not their contents
  -srcfile FMT                     Process a different source file
  -stay_open FLAG                  Keep reading -@ argfile even after EOF
  -userParam PARAM[[^]=[VAL]]      Set user parameter (API UserParam opt)
  
 ``` 
  
---

### Sources :
- [Exiftools man page](https://exiftool.org/exiftool_pod.html)