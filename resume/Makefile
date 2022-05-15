date = $(shell date +%d%m%Y)

pre_build:
	rm -rf build/
	mkdir build/

post_build:
	rm build/*.aux
	rm build/*.log
	rm build/*.out

regular: pre_build
	pdflatex --jobname=build/Resume_Vasyl_Horbachenko_$(date)_Light "\input{latest.tex}"
	@$(MAKE) --no-print-directory post_build

dark: pre_build
	pdflatex --jobname=build/Resume_Vasyl_Horbachenko_$(date)_Dark "\def\darkmode{1} \input{latest.tex}"
	@$(MAKE) --no-print-directory post_build

all: regular dark
