gcat

Description: 
  This program is used to cat multiple files with smart headers enabled.
  Meaning it will cat files together based on their column header names case 
  insensitive.  If you have multiple files with columns out of order in each file
  this program will reorder their columns based on the column order of the first file.   
             

Default behavior writes out all columns across all files in the order they are seen

Flags:
  -s     = prints out status of file headers
  -v     = prints out status of file headers in `less`
  -d     = specify single file delimiter (default is \t)
  -r     = replace single file delimiter (default is whatever is set for -d)
  -h     = specify headers (ex: -h"header1,header2")
  -^h    = removes specified headers
  -f     = specify index (ex: -f"1,2,3-4")
  -^f    = removes specified index
  -i     = Interactive Mode
  -b     = force progress bar
  -p     = used with -m to put "string" instead of blanks
  -m1    = only writes columns based on the first file; new columns will not be added
  -m2    = only writes columns in common accross all files, no order.
  --help = displays help

  -t = tabmerge (normal ex: gcat -t"key" file1 file2)
       Used in conjunction with tabmerge (ex: gcat -t"key" --filter file1 file2):
       If no key given, assumes first column header as the key
       --filter (--f) = prints rows from file1 which are NOT in file2
       --dedupe (--d) = prints rows from file1 which ARE in file2
                      = if only one file given; prints unique rows from file1
       --t = tabmerge assuming first column header as key
       -x  = specify values (instead of file2) to filter/dedupe by (ex: -x"asdf,whatever")
