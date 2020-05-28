= Functions =

function!GetMyName()
  echo 'Brij'
endfunction

command! MyName call GetMyName()

nnoremap M :MyName<CR>


function! AddHelloToTop()
  normal HOhello thereA vim user0
  s/hello there/hi/
  return "we added a message"
endfunction

%% function name must start with capital letter
%% function! replaces function with same name
%% :call AddHelloToTop()


command! Hello call AddHelloToTop()
%% create command Hello to call function
%% command! replaces command with same name
%% :Hello (to run the command)

nnoremap <leader>h :call AddHelloToTop()<cr>
%% creates a mapping for function

:echom AddHelloToTop()
%% prints the return value of function
%% echom addes the value to messages, visible using :messages

:echo


:echo join(split(&runtimepath,','),"\n")
