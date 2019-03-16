# Patchup [![Build Status](https://travis-ci.com/Dezyh/Patchup.svg?branch=master)](https://travis-ci.com/Dezyh/Patchup)

A library to create patches between two binary files, aimed at reducing file sizes when updating large but similar files.

To create a patch between two binary files, [Myers algorithm](http://www.xmailserver.org/diff2.pdf) is implemented to compute the differences in O(nd) time and O(n) space where n is the shorter of the two files and d is the number of differences between the two files. 

The next part of this project is to improve the runtime complexity at the expense of space required. This is through implementing Ukkonens algorithm to construct suffix trees in O(n) time to efficiently find maximal unique matches between the two files and then compute the diff between these regions. This is useful for binary files where the same data has been moved to another location. 
