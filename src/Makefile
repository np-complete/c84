.SUFFIXES: .tex .dvi .aux .bbl .pdf .md
PARTS = ニコ書を支える快楽天.tex \
	ニコ書を支えるAC5.tex \
	ニコ書を支える覚悟.tex \
	ニコ書を支えるイカ.tex \
	ニコ書を支えるパーカー.tex \
	ニコ書を支える命名.tex \
	ニコ書を支える本とさや.tex \
	ニコ書を支える東京洋菓子倶楽部.tex \
	ニコ書を支える飯.tex
all: c84.dvi c84.pdf

.dvi.pdf:
	dvipdfmx -p a4 -f dlbase14.map -o $@ $<
c84.dvi:$(PARTS) c84.tex
	pslatex c84.tex
	pslatex c84.tex
.md.tex:
	pandoc -S -o $@ -f markdown $<

clean:
	rm *.aux *.log $(PARTS)
