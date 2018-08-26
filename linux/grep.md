= GREP (Global Regular Expression Print) =

* grep "text_to_search" file_to_search
* grep -n "text_to_search" file_to_search
%% show line numbers also
* grep -vn "text_to_search" file_to_search
%% shows negative results, i.e., lines that do not match
* grep -c "text_to_search" file_to_search
%% show only line numbers and no matching line
* grep -l "text_to_search" *
%% lists the files which have matching line
* grep -i "text_to_search" file_to_search
%% ignores case
* grep -f file_with_search_content file_to_search
* grep "e$" file_to_search
%% searches for lines ending with e
* grep "boots?" file
%% ? matches 0 or 1 occurrences of previous character
* grep -H 'test' : print file name for each match (or use --with-filename)
* grep -n 'test' : prefix each line with line number (or use --line-number)

== Extended Grep (egrep) ==
%% (or use grep -E) (but egrep also provide more functionality like pipe below)
* egrep "boot|boots" (matches boot or boots)

== Fast Grep (fgrep) ==
%% (searches for strings of literal characters) (or use grep -F)
* fgrep "book$" file (will search for book$, $ is not treated as special character)

Witty Examples
* find | grep "hello" (search for file in current directory with "hello" in name)
* tail -n8 file | grep "boo" (search boo in last 8 lines of file)
* find . -exec grep "boo" {} \; (search for text in every directory below the current directory)
* grep "\([a-z]\)\1" file (using backreferences, searches for lines that contain two instances of a letter in succession )

Source: http://www.uccs.edu/~ahitchco/grep/

* grep -c name /prod/cpuinfo
(count number of cores within the cpu)
