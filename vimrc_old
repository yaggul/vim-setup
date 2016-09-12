execute pathogen#infect()
let g:jedi#setup_py_version = 3

colorscheme evening_2
set ruler
set showcmd
set wildmenu
syntax on
set t_Co=256

set tabstop=4
set softtabstop=4
set shiftwidth=4
set textwidth=79
set expandtab
set autoindent
set fileformat=unix



"au BufNewFile,BufRead *.py
"   \ set tabstop=4
"   \ set softtabstop=4
"   \ set shiftwidth=4
"   \ set textwidth=79
"   \ set expandtab
"   \ set autoindent
"   \ set fileformat=unix

"au BufNewFile,BufRead *.js, *.html, *.css
"   \ set tabstop=2
"   \ set softtabstop=2
"   \ set shiftwidth=2


set nohlsearch
set incsearch

set ignorecase
set smartcase

set backspace=indent,eol,start

set autoindent

set laststatus=2

set confirm

set cmdheight=2

set number
set nocompatible
"filetype off
"au BufRead,BufNewFile *.py,*.pyw,*.c,*.h match BadWhitespace /\s\+$/
set encoding=utf-8


set rtp+=~/.vim/bundle/Vundle.vim

call vundle#begin()

Plugin 'gmarik/Vundle.vim'
Plugin 'scrooloose/nerdtree'
Plugin 'flazz/vim-colorschemes'
Plugin 'kien/ctrlp.vim'
Plugin 'tpope/vim-commentary'
Plugin 'leshill/vim-json'
Plugin 'pangloss/vim-javascript'
Plugin 'indenthtml.vim'
Plugin 'tpope/vim-markdown'
Plugin 'mattn/emmet-vim'
Plugin 'tpope/vim-endwise'
Plugin 'scrooloose/syntastic'
Plugin 'vim-ruby/vim-ruby'
Plugin 'tmhedberg/SimpylFold'
Plugin 'Lokaltog/powerline', {'rtp': 'powerline/bindings/vim/'}
Plugin 'derekwyatt/vim-scala'
Plugin 'leafgarland/typescript-vim'
Plugin 'terryma/vim-expand-region'
Plugin 'tpope/vim-repeat'
Plugin 'tpope/vim-fugitive'
Plugin 'tpope/vim-surround'
Plugin 'kana/vim-textobj-user'
Plugin 'bps/vim-textobj-python'
Plugin 'davidhalter/jedi-vim'

call vundle#end()

filetype plugin indent on

let g:ycm_autoclose_preview_window_after_completion=1
map <leader>g  :YcmCompleter GoToDefinitionElseDeclaration<CR>

let python_highlight_all=1
set clipboard=unnamed

"python with virtualenv support
python3 << EOF
import os
import sys
if 'VIRTUAL_ENV' in os.environ:
    project_base_dir = os.environ['VIRTUAL_ENV']
    activate_this = os.path.join(project_base_dir, 'bin/activate_this.py')
    execfile(activate_this, dict(__file__=activate_this))
EOF


noremap <A-j> :m .+1<CR>==
noremap <A-K> :m .-2<CR>==
inoremap <A-j> <Esc>:m .+1<CR>==gi
inoremap <A-k> <Esc>:m .-2<CR>==gi
vnoremap <A-j> :m '>+1<CR>gv=gv
vnoremap <A-k> :m '<-2<CR>gv=gv


"Syntastic setup

let g:syntastic_enable_signs=1

" Try to optimize syntastic in terminal Vim as its already 0 on MacVim.
let syntastic_full_redraws=0
let g:syntastic_enable_highlighting=0

" Add some fancy symbols for the error and warning messages.
let g:syntastic_error_symbol='✗'
let g:syntastic_style_error_symbol='✠'
let g:syntastic_warning_symbol='⚠'
let g:syntastic_style_warning_symbol='≈'

let g:syntastic_always_populate_loc_list = 0
let g:syntastic_auto_loc_list = 0
let g:syntastic_check_on_open = 0
let g:syntastic_check_on_wq = 1

let g:syntastic_python_checkers = ['pep8']
