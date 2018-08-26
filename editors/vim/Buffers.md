= Vim Buffers =
* vim file1.ext file2.ext
* :e file3.ext , :edit file.ext
* vim file* 
%% open multiple files using shell expansion
* :buffers, :ls, :files
%% to see buffers
* :h :buffers
* :buffer 2, :b3
%% (to open file 3 as per buffers command) (can also pass file name)
* :bnext, :bn
%% go to next buffer
* :bprevious, :bp
%% go to previous buffer
* :b 1 
%% to move to 1st buffer, 1<C-^>
* :b fileName 
%% to switch to buffer having file name. File name can be partial.
%% Press tab to complete file name. You can also press C-D to list the
%% file names
* :bfirst, :bf 
%% go to first buffer
* :blast, :bl
%% go to last buffer
* <C-^>
%% (got to previously open buffer)
* :hidden 
%% allows you switch between buffers without writing
* set hidden?
* :badd file.ext 
%% open a file in buffer without switching to it
* :bdelete, :bd
%% unlists current buffer from list)
* :bd3
%% unlists 3rd buffer
* :1,3bd
%% unlists 1 to 3
* :%bd
%% unlists all buffers
* :bufdo set nu
%% execute command in all bufers
* :bufdo %s/#/@/g | w 
%% first substibute, then save for each buffer
* :wall (write in all buffers)
* :explore (or :E) 
%% to view explorer. (use :bd to get out --- deletes explorer buffer)
* :qall
%% quit all
* :sbuffer 3
%% open buffer 3 in split
* :sb1
%% open buffer in split window
* :vert sb1
