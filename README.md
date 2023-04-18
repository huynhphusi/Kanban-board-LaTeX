# Kanban-board-LaTeX
Thiết kế bảng Kanban trong LaTeX, dùng tổng hợp kiến thức rất tiện

## Demo
![Demo 1](https://raw.githubusercontent.com/huynhphusi/Kanban-board-LaTeX/main/demo1.jpg)
![Demo 2](https://raw.githubusercontent.com/huynhphusi/Kanban-board-LaTeX/main/demo2.jpg)

## Định nghĩa lệnh
Màu sắc và các khung văn bản được định nghĩa trong file config.tex, các khung này được custom từ gói lệnh tcolorbox nên cũng không quá xa lạ với người dùng LaTeX.

'''
\definecolor{trello_bg_green}{HTML}{023020}
\definecolor{trello_bg_blue}{HTML}{191970}
\definecolor{trello_bg_pink}{HTML}{FF10F0}
\definecolor{trello_bg_violet}{HTML}{7F00FF}
\definecolor{trello_bg_orange}{HTML}{FF5733}

\definecolor{trello_bd_green}{HTML}{023020}
\definecolor{trello_bd_blue}{HTML}{191970}
\definecolor{trello_bd_pink}{HTML}{FF10F0}
\definecolor{trello_bd_violet}{HTML}{7F00FF}
\definecolor{trello_bd_orange}{HTML}{FF5733}

\newcounter{khung_trello}
\newtcolorbox[use counter=khung_trello]{khung_trello}[2]{size=title,
	shadow={0.2mm}{-0.3mm}{0mm}{black!40}, breakable, enhanced,
	%colback=red!5!white,
	colback=trello_bg_#2,
	colbacktitle=trello_bg_#2,titlerule=-1mm,
	colframe=trello_bd_#2,
	title={\vspace*{2mm}\hspace*{1mm}\bf\color{white}\large #1}, 
	sharp corners,rounded corners, arc=0.5mm,left=0mm,right=0mm,top=1mm,bottom=1mm
}
\newcounter{khung_trello_box}
\newtcolorbox[use counter=khung_trello_box]{khung_trello_box}[1][]{enhanced,
	%drop fuzzy shadow south,
	shadow={0mm}{-0.2mm}{0mm}{black!40},
	colframe=black,colback=white,boxrule=0pt,enlarge bottom by=-1mm,
	left=1mm,right=1mm,top=1mm,bottom=0mm
}
'''
