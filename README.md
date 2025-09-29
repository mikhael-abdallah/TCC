# TCC IME/USP — BikeSP: Painel Administrativo

Este repositório utiliza o modelo LaTeX do IME/USP já configurado para o seu
TCC sobre o Bike~SP (painel administrativo). Use os comandos abaixo para
compilar e veja a estrutura de arquivos para editar conteúdo.

Referências úteis:
- **Normas IME/DCC**: https://www.ime.usp.br/dcc/pos/normas/tesesedissertacoes
- **BikeSP — piloto**: https://interscity.org/bikesp/piloto/
- **Resumo do projeto (CRBAM23)**: https://interscity.org/assets/CRBAM23_BookOfAbstracts_pgs_71_to_74-Ana-Yoon-Faria-de-Lima.pdf
- **Wiki do app BikeSP**: https://gitlab.com/interscity/bikesp/bikespapp/-/wikis/home

Besides that, there are lots of comments in the .tex and .sty files
about the packages used and things you might want to customize or
learn more about. These comments are in Brazilian Portuguese. Even
if you have some LaTeX experience, you may benefit from skimming the
comments, tutorial, and examples, as they include some useful tips.

## Como compilar

Pré-requisitos (Ubuntu/Debian):
```
sudo apt install biber latexmk texlive-plain-generic texlive-latex-base texlive-luatex lmodern fonts-lmodern texlive-latex-recommended texlive-fonts-recommended texlive-latex-extra texlive-fonts-extra texlive-bibtex-extra texlive-science texlive-lang-english texlive-lang-portuguese
```

Compilação:
```
make        # gera tese.pdf
make clean  # limpa temporários
make distclean # limpa também PDFs gerados
```

## Estrutura do TCC

- `tese.tex`: arquivo principal. Já configurado como TCC e apontando para os capítulos do Bike~SP.
- `conteudo/resumoabstract.tex`: resumo/abstract com palavras-chave; personalize conforme necessário.
- `conteudo/00-introducao-bikesp.tex`: introdução ao Bike~SP e objetivo do TCC.
- `conteudo/01-contexto-painel.tex`: cronograma (pré-teste, inscrições LimeSurvey ~3000 candidatos, julho e 4 semanas de agosto), atores/processos e objetivos do painel.
- `conteudo/02-implementacao.tex`: arquitetura, módulos, pagamentos/contestações e diretrizes de screenshots.
- `conteudo/03-resultados.tex`: resultados operacionais e estado da análise de dados.
- `conteudo/04-conclusao.tex`: conclusão e trabalhos futuros.
- `bibliografia.bib`: referências (inclui CRBAM23, piloto InterSCity, wiki BikeSP e MAC0499).

## Diretrizes para figuras (screenshots)

- **Legibilidade**: capture em resolução suficiente para impressão; evite compressão excessiva.
- **Anonimização**: oculte dados pessoais (nome, email, IDs).
- **Explicação no texto**: além da legenda, descreva no corpo do texto o contexto, a tarefa sendo exibida e o que observar.
- **Consistência**: use o mesmo tema de cores e zoom entre figuras relacionadas.

The template probably includes all packages you'd expect, such as the
AMS packages (amsthm, amsmath etc.), babel, geometry, hyperref, graphicx,
array etc. It also includes many others; in no particular order, these
are directly used in the template:
etoolbox, expl3, xparse, letltxmacro, regexpatch, fontenc, inputenc,
fontspec, fontaxes, unicode-math, calc, ragged2e, microtype, filehook,
indentfirst, footmisc, emptypage, caption, biblatex, setspace, parskip,
xcolor, textcase, fancyhdr, float, flafter, pdflscape, tikz, floatrow,
rotating, subcaption, pdfpages, tablefootnote, longtable, l3keys2e,
multirow, makecell, booktabs, tocbibind, imakeidx, verbatim, mathtools,
csquotes, hypcap, hyperxmp, listings, textcomp, multicol, stfloats, fnpct,
epigraph, todonotes, soul, soulutf8, translator, pgfgantt, tcolorbox,
titlesec, framed, adjustbox, threeparttable, colortbl, fewerfloatpages,
datetime2, iflang, lstautogobble, froufrou, enumitem, contour, siunitx,
pgfplots, appendix, iftex, cancel, and hologo. Several others are
loaded indirectly by these.

The default fonts depend on these packages: lmodern, fix-cm, libertinus,
libertinust1math, fourier-orns, and sourcecodepro.

The example presentation uses beamer, appendixnumberbeamer, qrcode,
and beamertheme-metropolis.

As of 2023, in debian/ubuntu systems, you need to install (with
their dependencies) at least: biber, latexmk, texlive-plain-generic,
texlive-latex-base, texlive-luatex, lmodern, fonts-lmodern,
texlive-latex-recommended, texlive-fonts-recommended, texlive-latex-extra,
texlive-fonts-extra, texlive-bibtex-extra, texlive-science,
texlive-lang-english, and texlive-lang-portuguese. Just run

`sudo apt install biber latexmk texlive-plain-generic texlive-latex-base texlive-luatex lmodern fonts-lmodern texlive-latex-recommended texlive-fonts-recommended texlive-latex-extra texlive-fonts-extra texlive-bibtex-extra texlive-science texlive-lang-english texlive-lang-portuguese`

## Dicas rápidas

- Ajuste metadados em `tese.tex` (`\title`, `\author`, `\orientador`, `\defesa`).
- Use `\cite{...}` para referenciar CRBAM23, piloto InterSCity e wiki BikeSP conforme necessário.
- Siga o cronograma descrito no capítulo de contexto ao relatar atividades.

## Licenças

Este repo mantém as licenças originais do modelo IME/USP. O texto deste TCC
pode usar CC-BY ou outra Creative Commons conforme `\direitos{...}` em `tese.tex`.
