.PHONY: all
all: html doc

.PHONY: html
html: index.jemdoc \
contact.jemdoc \
pubs.jemdoc \
hobbies.jemdoc
	jemdoc *.jemdoc
	mv *.html ..

.PHONY: doc
doc: ~/Documents/cv_abbrev/cv_abbrev.pdf \
~/Documents/papers/renyi_information/allerton15_renyi.pdf \
~/Documents/papers/6111_proj_report/6111_proj_report.pdf \
~/Documents/papers/phd_thesis/thesis/main.pdf \
~/Documents/papers/meng/thesis/main.pdf \
~/Documents/papers/boolean_spectrum/doc/icassp_arxiv/mask.pdf \
~/.keys/mypub.key
	mkdir -p ../doc
	rsync ~/Documents/cv_abbrev/cv_abbrev.pdf ../doc/cv.pdf
	rsync ~/Documents/papers/renyi_information/allerton15_renyi.pdf ../doc/allerton15_renyi.pdf
	rsync ~/Documents/papers/6111_proj_report/6111_proj_report.pdf ../doc/6111_proj_report.pdf
	rsync ~/.keys/mypub.key ../doc/pub.key
	rsync ~/Documents/papers/phd_thesis/thesis/main.pdf ../doc/phd_thesis.pdf
	rsync ~/Documents/papers/meng/thesis/main.pdf ../doc/meng_thesis.pdf
	rsync ~/Documents/papers/boolean_spectrum/doc/icassp_arxiv/mask.pdf ../doc/mask.pdf

.PHONY : clean
clean :
	rm -f ../*.html
	rm -rf ../doc
