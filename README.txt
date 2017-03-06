My N00b settings for Vim, Linux (and Windows?)

Installation:

  WIN:
    1.  Download and install official Vim;
    2.  In user home directory (in Vim it is under $HOME and that's how we're
        going to call it; usually C:\Users\<Username>) create a 'dotvim' folder; it will
        be the root for the git repo;

    3.  In this 'dotvim', execute git clone https://github.com/boyanstoyanov/dotvim.git ./
    4.  Go in this folder and if necessary 'git clone' all Vim plugins in their
        corresponding folders under dotvim/bundle. (TODO(boyan): maybe later
        make them git submodules?);
    5.  Create $HOME\vimtmp folder, which is in vimrc as a
        default backup vim folder;
    6.  Prepend/change following line in default _vimrc, which is usually in the Vim
        installation folder(to find out exactly, run :echo $VIM; or for more
        info - :help runtimepath in vim and search for $VIM), to point to our custom vimrc file:
        source $HOME/dotvim/vimrc  
    7.  Create following soft link to 
        vimfiles [$HOME\dotvim\vimfiles] (as described above, replace $HOME
        with its value, usually C:\Users\<Username>)
    
  LINUX:
        Similar as Windows, replace paths as necessary; (TODO(boyan): maybe
        describe it?)  

