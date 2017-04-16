"  必须配置
set nocompatible
filetype off
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
" 在这里添加你想安装的Vim插件
" Plugins.
Plugin 'VundleVim/Vundle.vim'
" 垂直线对齐
Plugin 'nathanaelkane/vim-indent-guides'
" 缩进帮助
Plugin 'Yggdroot/indentLine'
"  集成git
Plugin 'tpope/vim-fugitive'
"  powerline
Plugin 'Lokaltog/powerline', {'rtp': 'powerline/bindings/vim/'}
" nerdTree
Plugin 'scrooloose/nerdtree'
" 代码检查
Plugin 'vim-syntastic/syntastic'
" buffer
Plugin 'fholgado/minibufexpl.vim'
" tagBar
Plugin 'majutsushi/tagbar'
" 搜索 https://github.com/dyng/ctrlsf.vim  
Plugin 'dyng/ctrlsf.vim'
"  代码折叠插件    折叠也能看见文档字符串
Plugin 'tmhedberg/SimpylFold'
" buffer
Plugin 'vim-airline/vim-airline'
Plugin 'vim-airline/vim-airline-themes'
" nerdtree书签
Plugin 'MattesGroeger/vim-bookmarks'

Plugin 'ctrlpvim/ctrlp.vim'
" Plugin 'Valloric/YouCompleteMe'

call vundle#end()            " required
filetype plugin indent on    " required


" 主题
let g:molokai_original = 1
let g:rehash256 = 1
set background=dark
colorscheme molokai

" Plugin indentLine settings.
let g:indentLine_char = "┆"
let g:indentLine_enabled = 1
let g:autopep8_disable_show_diff=1

" Plugin syntastic settings.
set statusline+=%#warningmsg#
set statusline+=%{SyntasticStatuslineFlag()}
set statusline+=%*
let g:syntastic_always_populate_loc_list = 1
let g:syntastic_auto_loc_list = 1
let g:syntastic_check_on_open = 0
let g:syntastic_check_on_wq = 0
let g:syntastic_mode_map = {'mode': 'passive', 'active_filetypes': [], 'passive_filetypes': []}
" Use pylint to check python files.
let g:syntastic_python_checkers = ['pylint']
map <F5> :SyntasticToggleMode<CR> :SyntasticCheck<CR>
" Ignore warnings about newlines trailing.
let g:syntastic_quiet_messages = { 'regex': ['trailing-newlines', 'invalid-name',
    \'too-many-lines', 'too-many-instance-attributes', 'too-many-public-methods',
    \'too-many-locals', 'too-many-branches'] }

" Plugin nerdtree settings.
map <F2> :NERDTreeToggle<CR>
" 显示行号
let NERDTreeShowLineNumbers=1
let NERDTreeAutoCenter=1
let NERDTreeChDirMode=1
let NERDTreeShowBookmarks=1
" 设置宽度
let NERDTreeWinSize=25
" 是否显示隐藏文件
let NERDTreeShowHidden=0
let NERDTreeIgnore=['\~$', '\.pyc$', '\.swp$', '\.git$', '\']
let g:NERDTreeIndicatorMapCustom = {
    \ "Modified"  : "✹",
    \ "Staged"    : "✚",
    \ "Untracked" : "✭",
    \ "Renamed"   : "➜",
    \ "Unmerged"  : "═",
    \ "Deleted"   : "✖",
    \ "Dirty"     : "✗",
    \ "Clean"     : "✔︎",
    \ "Unknown"   : "?"
    \ }

" tagbar
"文件侦查启动,用以检测文件的后缀  
filetyp on  
"设置tagbar使用的ctags的插件,必须要设置对  
let g:tagbar_ctags_bin='/usr/bin/ctags'  
"设置tagbar的窗口宽度  
let g:tagbar_width=30  
"设置tagbar的窗口显示的位置,为左边  
let g:tagbar_left=1  
"打开文件自动 打开tagbar  
"autocmd BufReadPost *.css,*.py,*.php,*.js call tagbar#autoopen() 

map <F8> :TagbarToggle<CR>
let g:tagbar_type_css = {
\ 'ctagstype' : 'Css',
    \ 'kinds'     : [
        \ 'c:classes',
        \ 's:selectors',
        \ 'i:identities'
    \ ]
\ }
let g:tagbar_type_go = {
    \ 'ctagstype': 'go',
    \ 'kinds' : [
        \'p:package',
        \'f:function',
        \'v:variables',
        \'t:type',
        \'c:const'
    \]
\}


"  设置重新载入.vimrc快捷键
map ss :source ~/.vimrc
"  设置快速编辑.vimrc快捷键
" map ee :e ~/.vimrc
"  括号匹配
set showmatch

"  sv上下分屏  vs左右分屏,鼠标拖动分屏
set splitbelow
set splitright
"if has('mouse')
"    set mouse=a
"endif

"  hjkl屏幕移动
nnoremap <C-J> <C-W><C-J>
nnoremap <C-K> <C-W><C-K>
nnoremap <C-L> <C-W><C-L>
nnoremap <C-H> <C-W><C-H>

"  代码折叠za或者space
set foldmethod=indent
set foldlevel=59
nnoremap <space> za
" 折叠也能看见文档字符串
let g:SimpylFold_docstring_preview=1

"  开启行号,高亮行和列光标
set nu
set cursorcolumn
set cursorline
highlight CursorLine   cterm=NONE ctermbg=black ctermfg=green guibg=NONE guifg=NONE
highlight CursorColumn cterm=NONE ctermbg=black ctermfg=green guibg=NONE guifg=NONE


"  tablestop,且table变空格
set ts=4
set expandtab

"  python php代码缩进
au BufNewFile,BufRead *.py *.php
\ set tabstop=4
\ set softtabstop=4
\ set shiftwidth=4
\ set textwidth=79
\ set expandtab
\ set autoindent
\ set fileformat=unix

"  网页代码缩进
au BufNewFile,BufRead *.js, *.html, *.css
\ set tabstop=2
\ set softtabstop=2
\ set shiftwidth=2


"  utf-8中文帮助
set encoding=utf-8
set helplang=cn

" 第一行确保了在你完成操作之后，自动补全窗口不会消失
" 第二行则定义了“转到定义”的快捷方式。
" let g:ycm_autoclose_preview_window_after_completion=1
" map <leader>g  :YcmCompleter GoToDefinitionElseDeclaration<CR>

" 语法高亮,pep8检查
let python_highlight_all=1
syntax on

"  查找不区分大小写
set ignorecase

" Auto add head info
" .py file into add header
function HeaderPython()
    call setline(1, "#!/usr/bin/env python")
    call append(1, "# -*- coding: utf-8 -*-")
    normal G
    normal o
endf
autocmd bufnewfile *.py call HeaderPython()
