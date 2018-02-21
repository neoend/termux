"http://vlee.kr/1142
set nocompatible  "doesn't compatible with original vi
set autoindent
set cindent
set smartindent
set wrap
set nowrapscan       "doesn't go back to the first when searching
set nobackup
set noswapfile
set visualbell      "screen refresh when wrong key press
set ruler
set shiftwidth=4
set number           "set nu
set fencs=ucs-bom,utf-8,euc-kr.latin1 "korean file -> euc-kr, unicode -> unicode
set fileencoding=utf-8
set tenc=utf-8       " terminal encoding
set expandtab       " spaces inspite of tab
set hlsearch         "set hls "highlight search keyword
set ignorecase       "set ic " when searching
set tabstop=4
set lbr
set incsearch        " search gradual when inputing keyword
set cursorline
set laststatus=2
syntax on
filetype indent on
set background=dark
"colorscheme jellybeans
set backspace=eol,start,indent "when input backspace go to before line
set history=1000
highlight Comment term=bold cterm=bold ctermfg=4 "highlight comment
set mouse=a          " using mouse
set t_Co=256         " adjust color

"----------------- vundle ----------------
" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
" alternatively, pass a path where Vundle should install plugins
"call vundle#begin('~/some/path/here')
 
" let Vundle manage Vundle, required
Plugin 'VundleVim/Vundle.vim'

"extra bundles
Plugin 'cscope.vim'

call vundle#end()
"----------------- vundle ----------------

