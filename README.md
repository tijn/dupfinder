# Dupfinder

A tool for finding duplicate files.

# Usage

Give it a directory to search in (called the haystack) and one or more files to search for (called the needles).

    find-dups HAYSTACK NEEDLES

# Why?

I found some old backups and I was wondering which things I actually transferred to the new computer. I needed a program to help me with this. I found some that would start off by calculating a hash of every single file on my hard drive. Undoubtedly to create an index that later can be searched using the contents of the "needles". I decided that I could postpone the heavy calculation until I found two files with the exact same size. (If the size is different, the contents are different.) (The reason is of course that getting a file size is a really cheap operation and calculating a hash of the file contents is not.)

It's keeping a big list in memory of all files you tell it to look for. We have gigabytes of memory these days and it proved not to be a problem at all for me.
