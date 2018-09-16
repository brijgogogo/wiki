= curl =

The curl tool lets us fetch a given URL from the command-lin.

* curl http://some.url --output some.file
--output (or -o) flag denotes the filename of the downloaded URL
* curl http://some.url --output some.file --silent
--silent (or -s) doesn't show download progress
* curl http://some.url
If you curl without any options except for the URL, the content of the URL (whether it's a webpage, or a binary file, such as an image or a zip file) will be printed out to screen.
* curl -s http://example.com | wc -l
count number of lines


= sources =
http://www.compciv.org/recipes/cli/downloading-with-curl/
