= wget =
%% used for retrieving content from web servers
%% supports http, https, ftp
%% supports recursive downloads (from HTML file or web directory)

* wget www.google.com

* wget -r -m www.ingrahaminstitute.com
%% -r = -recursive
%% -m = -mirror

* wget -e robots=off www.url.com
%% by default wget considers robots file

* wget -nc  www.url.com
%% -nc = --no-clobber to skip downloads that would download to existing files

* wget -np www.url.com
%% -np = --no-parent
%% to stop wget from ascending into a parent directory

* wget --accept jpg,gif,bmp www.url.com
%% download only certain file types
%% Similarly you can use the --reject command to ignore specific file-types

* --level=0
%% dictates the depth of the directories you’d like to download, in this case
%% its set to 0, meaning that there is no pre-determined depth to download (aka
%% it will recursively download everything).

* FOR g IN dir1 dir2 dir3
DO wget -e robots=off -r --level=0 -nc -np -accept tx  www.url.com/$g
done
%% script to download txt files from specific directory in a url
