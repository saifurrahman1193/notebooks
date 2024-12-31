# Combine & Export to PDF
```
sudo apt install python-pip
sudo apt install pandoc texlive-xetex texlive-fonts-recommended

cat *.md > NLP.md
pandoc NLP.md -o NLP.pdf
pandoc NLP.md -o NLP.docx
```