FancyStat
=========

FancyStat is a stat add on for your working allocator.c implementation,
and displays hopefully a useful 2d diagram of the managed memory from
allocator.c

FancyStat is distributed using the GNU General Public License. 


Installation:
-------------

1. Add #include "fancystat.c" at the very bottom of your working allocator.c
2. Edit line 105 of run_sal.c from:
       else if (line[0] == '!') {
         sal_stats();
   To:
       else if (line[0] == '!') {
         sal_stats2(ptr);

   Edit line 53 of allocator.h from
	void sal_stats(void);
   To:
	void sal_stats(void);
	void sal_stats2(void * alpha[26]);
4. Run make
5. Enjoy!



Requirements
============
fancystat has the following dependencies:

A working allocator.c following the following spec
http://cgi.cse.unsw.edu.au/~cs1927/14s2/assigns/01/index.php

A terminal emulator that supported ascii escape codes for extended colors.
