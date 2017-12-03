# Terminal

## Obtain full path in terminal
```
$ pwd
```

## Directory with space
When you use directory with space, you have to add `\` before the space.
(e.g. `/Users/tomoyasasaki/Google\ ドライブ/TMY/`)

## Set Global PATH

1. open and edit `.bash_profile` 
e.g. `sudo emacs .bash_profile` or `sudo vi .bash_profile`
2. add the PATH
e.g. `export PATH=$PATH:[PATH you want to add]`
3. when you use emacs, use `command + x` and `command + c` to finish editing and save
4. then don't forget to put `source ~/.bash_profile` 
5. check PATH with `printenv PATH`

#### Reference
* http://qiita.com/nbkn/items/01a11392921119fa0153
* http://qiita.com/soarflat/items/d5015bec37f8a8254380
* http://cns-guide.sfc.keio.ac.jp/2000/4/1/2.html

## Set PATH for Tex packages
1. put style file here with new directory:
`/usr/local/texlive/2014/texmf-dist/tex/latex/misc/`
The new directory will be like this: `/usr/local/texlive/2014/texmf-dist/tex/latex/misc/NEWSTY/`
2. don't forget to set after finishing the operation below: `$ sudo mktexlsr`

* `kpsewhich --expand-path='$TEXMFLOCAL'`

	> `/usr/local/texlive/texmf-local`
* `kpsewhich --progname=platex jarticle.cls`

	> `/usr/local/texlive/2014/texmf-dist/tex/platex/base/jarticle.cls`

### maybe ok
create directory and set sty file (e.g. STYLE.sty)

1. move to the directory where the style file is placed

2. `$ sudo mkdir -p -v /usr/local/texlive/2014/texmf-dist/tex/latex/misc/STYLE`

3. `$ sudo mv STYLE.sty /usr/local/texlive/2014/texmf-dist/tex/latex/misc/STYLE`

#### Reference
* http://emath.a.la9.jp/ydir/Wiki/index.php?emath.sty%A4%CE%C3%D6%A4%AD%BE%EC%BD%EA
* https://texwiki.texjp.org/?TeX%20%E3%81%AE%E3%83%87%E3%82%A3%E3%83%AC%E3%82%AF%E3%83%88%E3%83%AA%E6%A7%8B%E6%88%90
* https://texwiki.texjp.org/?LaTeX%E5%85%A5%E9%96%80%2F%E5%90%84%E7%A8%AE%E3%83%91%E3%83%83%E3%82%B1%E3%83%BC%E3%82%B8%E3%81%AE%E5%88%A9%E7%94%A8
* http://demmys.hatenablog.com/entry/2012/06/06/234808

## Create and remove file through terminal
* create files: `touch [filename]`
* remove files: `rm -Rf [filename]` or `rm -R [filename]`
* move files: at the directory where the file exists`mv [filename] [destination]`

## Read text files in terminal with less
### Options
* `-F`: 行数が短くて位置画面に収まる場合は less がすぐに終了する。
* `--help`: ヘルプ表示
* `-i`: 検索モードでキーワードをすべて小文字で入力した場合に、大文字小文字の区別をしない。 検索キーワードに大文字が混ざっていた場合にはこのオプションをつけていても大文字小文字を区別する。
* `-N`: 行番号を表示する。(`cat` でこれに相当するのは `-n`)
* `-r`: エスケープシーケンスなどのバイナリをエスケープシーケンスとして解釈せずに、 そのまま出力される。
* `-R`: 色のエスケープシーケンスをそのとおりに解釈して 色付きで表示する。 色以外のエスケープシーケンスは解釈せず、 そのまま出力される。 `ls` は `--color`、 `grep` は `--color=always` を付けると 色付きで出力される。
* `-S`: 長い行を折り返さずに横方向にもページングできるようにする。 各行の左の方だけ見えれば十分な場合にもこのオプションは便利。
* `--version`: バージョン表示
* `-X`: `less` 終了時に画面をクリアしない。

-- というパラメータを渡すとそれ以降のパラメータをオプションではなくファイル名とみなしてくれるので、 - で始まるファイル名を扱いたい場合に使うとよい。


### command while reading a file
* `q`: `less`コマンドを終了
* `SPACE`: 1画面分下にスクロール
* `f`: 1画面分下にスクロール
* `b`: 1画面分上にスクロール
* `g`: ファイルの先頭に移動
* `Shift + <`: ファイルの先頭に移動
* `Shift + G`: ファイルの最後に移動
* `Shift + >`: ファイルの最後に移動

### Reference
https://hydrocul.github.io/wiki/commands/less.html

# Dealing with pics
## Jpegoptim
https://github.com/tjko/jpegoptim

Optimize the size of png and jpeg.

e.g. `jpegoptim --strip-all --max=90 test.jpg`
* `--strip-all`: erase all meta data
* `--max=90`: 90% of the quality
* `*.jpg`: set wild card to optimize multiple files

# Use Gmail in China
http://kinto-un.hatenablog.com/entry/2015/02/15/152313

# Markdown
## Markdown Cheatsheet
Please check [here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

## To use keyboard-like character
Check [here](https://meta.askubuntu.com/questions/707/how-to-use-keyboard-icon-in-markdown).

# Shortcuts
* Change windows within an application: <kbd>command</kbd> + <kbd>F1</kbd>