# Copyright (C) 2019, ATA Engineering, Inc.
# 
# This program is free software; you can redistribute it and/or
# modify it under the terms of the GNU Lesser General Public
# License as published by the Free Software Foundation; either
# version 3 of the License, or (at your option) any later version.
# 
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
# Lesser General Public License for more details.
# 
# You should have received a copy of the GNU Lesser General Public License
# along with this program; if not, write to the Free Software Foundation,
# Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301, USA.

DOC_NAME = wallProbe
TEX_FILES = wallProbe.tex
MAIN_FILE = wallProbe

$(DOC_NAME).pdf: $(TEX_FILES)
	latex $(MAIN_FILE); latex $(MAIN_FILE)
	dvips -t letter -Ppdf -o $(DOC_NAME).ps $(MAIN_FILE)
	ps2pdf $(DOC_NAME).ps
	rm $(DOC_NAME).ps $(MAIN_FILE).dvi


all: $(DOC_NAME).pdf 

FRC: 

clean:
	rm -fr *.dvi *.log *.aux *~ *.bbl *.blg *.toc *.pdf *.ps

distclean: clean

