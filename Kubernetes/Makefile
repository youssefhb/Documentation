SHELL=/bin/bash

FILE_NAME = Kubernetes
READER = AcroRd32.exe




.PHONY: all pdf xml html clean

all:
	@echo "Welcome to ascii-doctor."
	@echo ${SRC_DIR}


pdf:
	asciidoctor -a  pdf-stylesdir=./resources/themes -a pdf-style=asciidoctor-no-watermark -B '.' -b pdf -r asciidoctor-pdf ${FILE_NAME}.adoc
	${READER} ${FILE_NAME}.pdf &
	
xml:
	asciidoctor -b docbook ${FILE_NAME}.adoc
	yelp  ${FILE_NAME}.xml 


html:
	asciidoctor  ${FILE_NAME}.adoc
	
clean:
	rm -f *.pdf  *.html  *.xml

