My N00b settings for Vim, Linux (and Windows?)

Installation:

  WIN:
    1.  Install official Vim;
    2.  In user home directory (in Vim it is under $HOME and that's how we're
        going to call it; usually C:\Users\<Username>) create a 'dotvim' folder; it will
        be the root for the git repo;

    3.  In this 'dotvim', execute git clone https://github.com/boyanstoyanov/dotvim.git .\
    4.  Go in this folder and if necessary 'git clone' all Vim plugins in their
        corresponding folders under dotvim/vimfiles/bundle. (TODO(boyan): maybe later make them git submodules?);
    5.  Create $HOME\vimtmp folder, which is set in vimrc as a
        default backup vim folder;
    6.  Prepend/change following line in default _vimrc which is usually in the Vim
        installation folder (to find out exactly, run :echo $VIM; or for more
        info - :help runtimepath in vim and search for $VIM) 
        to point to our custom vimrc file:
        > source $HOME\dotvim\vimrc  
    7.  Create soft link to 
        vimfiles [$HOME\dotvim\vimfiles] (as explained above, replace $HOME
        with its value, usually C:\Users\<Username> for Win )
        > mklink /d
D:\Programs\VimWindows\Vim\vimfiles C:\Users\<Username>\dotvim\vimfiles
    
  LINUX:
        Similar as Windows, replace paths as necessary; (TODO(boyan): maybe
        describe it?) 

    1.  Install official Vim;
    2.  In user home directory (in Vim it is under $HOME variable and that's how we're
        going to call it; usually ~/) create a 'dotvim' folder; it will
        be the root for the git repo;
    3.  In this 'dotvim', execute git clone https://github.com/boyanstoyanov/dotvim.git ./
    4.  Go in this folder and if necessary 'git clone' all Vim plugins in their
        corresponding folders under dotvim/vimfiles/bundle. (TODO(boyan): maybe later make them git submodules?);
    5.  Create ~/vimtmp folder, which is set in vimrc as a
        default backup vim folder;
    6.  Prepend/change following line in default .vimrc, which is usually in ~/.vimrc 
        (to find out exactly, run :echo $VIM; or for more info - :help runtimepath in vim and search for $VIM), to point to our custom vimrc file:
        > source $HOME/dotvim/vimrc  
    7.  Create soft link to vimfiles [~/dotvim/vimfiles] 
        > ln -s ~/dotvim/vimfiles ~/.vim
        
WIN cygwin:
        Like in Linux but in the cygwin folder? (TODO: check this and describe it better)
