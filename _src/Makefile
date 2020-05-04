.PHONY: all
all: html doc

.PHONY: html
html: index.jemdoc \
contact.jemdoc \
pubs.jemdoc \
talks.jemdoc \
hobbies.jemdoc
	./jemdoc *.jemdoc
	mv *.html ..

.PHONY: doc
doc: ~/Dropbox/cv_abbrev/cv_abbrev.pdf \
~/doc/papers/renyi_information/allerton_paper.pdf \
~/doc/papers/renyi_information/talk/allerton15.pdf \
~/doc/6111_proj_report/proj_report.pdf \
~/Dropbox/phd_thesis/thesis/main.pdf \
~/doc/meng/thesis/main.pdf \
~/Dropbox/boolean_spectrum/doc/icassp_arxiv/mask.pdf \
~/.keys/mypub.key
	mkdir -p ../doc
	rsync ~/Dropbox/cv_abbrev/cv_abbrev.pdf ../doc/cv.pdf
	rsync ~/doc/papers/renyi_information/allerton_paper.pdf ../doc/allerton15_renyi.pdf
	rsync ~/doc/papers/renyi_information/talk/allerton15.pdf ../doc/allerton15_renyi_slides.pdf
	rsync ~/doc/6111_proj_report/proj_report.pdf ../doc/6111_proj_report.pdf
	rsync ~/.keys/mypub.key ../doc/pub.key
	rsync ~/Dropbox/phd_thesis/thesis/main.pdf ../doc/phd_thesis.pdf
	rsync ~/doc/meng/thesis/main.pdf ../doc/meng_thesis.pdf
	rsync ~/Dropbox/boolean_spectrum/doc/icassp_arxiv/mask.pdf ../doc/mask.pdf

.PHONY : clean
clean :
	rm -f ../*.html
	rm -rf ../doc
