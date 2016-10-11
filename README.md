# Dupfinder

A tool for finding duplicate files.

# Usage

Give it a directory to search in (called the haystack) and one or more files to search for (called the needles).

    find-dups [options] haystack needle...

    -h, --help
    -v, --[no-]verbose
    -p, --print         Print 'needle', 'hay' or 'separator'; should be a comma-separated list (no spaces!)

# Why?

I found some old backups and I was wondering which things I allready transferred to the new computer. There were many files so I needed a program to help me with this. I found some existing solutions that would start off by calculating a hash of every single file on my hard drive. Undoubtedly to create an index that later can be searched using the contents of the "needles". I decided that I could postpone the heavy calculation until I found two files with the exact same size. (If the size is different, the file contents must logically be different too.) This resulted in a huge speed increase since fetching the size of a file a really cheap operation compared to calculating the hash of some file's contents.

The program keeps a big list in memory of all the files you tell it to look for. We have gigabytes of memory these days and it proved not to be a problem at all for me.
