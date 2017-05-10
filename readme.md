git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim 
## 光标移动
	
	hjkl
	0^$
	{}
	前后追溯：`, c-i, c-o
	:
	%（到最后一行）
	/插件，精确定位
	*#（搜索+移动）
	f F
	t xxx前的第一个字符
	c-d c-u
	窗口间 map

## 快速编辑

	区域选择：() '' "" {} 内部快速选中、删除、复制等
	y c d 
	i a
	移动+编辑组合 y$ de dt(目标字符前一个字符))
	选中 + u U
	全文/选中 替换 %s/xx/yy/g
	J
	=
	> <
	
## tab & buffer
	
	map


## 列操作
	
	c-v ^/$ I/A ESC

## 行操作
	
	V

## 宏
	
	q a @a @@

## 搜索

	当前
	全局
	基于ctag / cscope
	ctrlp
	ack/ag

## 书签

	m M

## 其它

	map保存退出
	与Chrome无缝结合工作流(Vimium插件)
