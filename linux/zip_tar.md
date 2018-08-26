== p7zip ==
Command line port of 7zip
* pacman -S p7zip
* 7z e <archive> : extract to current directory without using directory names
* 7z x <archive> : archive with full file path
* 7z x <archive> -o<output_directory>
*



* unzip file.zip -d destination_folder
* unzip -l file.zip (to list files in a zip)

> unrar x file.rar
> unrar l file.rar
> unrar e file.rar
> unrar t file.rar
> rar a file.rar folder
> rar r file.rar
> rar u file.rar newFile.txt
> rar a -p file.rar



Extract Multiple zip files to separate folder
for f in *.zip; do unzip -d "${f%*.zip}" "$f"; done

tar tvf tarball.tar.bz2 (lists contens of a tarball)
tar xf tarball.tar.xz (unpacks in current directory)

(tarballs = archives)



