################################################################################
#  THIS FILE IS 100% GENERATED BY ZPROJECT; DO NOT EDIT EXCEPT EXPERIMENTALLY  #
#  Read the zproject/README.md for information about making permanent changes. #
################################################################################
# NOTE: stub doc/joex.txt is generated by GSL from project.xml and
#       then comitted to SCM and maintained manually to describe the project.
MAN1 = joexd.1 joexc.1
MAN3 = joex_server.3 joex_proto.3
MAN7 = joex.7
MAN_DOC = $(MAN1) $(MAN3) $(MAN7)

MAN_TXT = $(MAN1:%.1=%.txt)
MAN_TXT += $(MAN3:%.3=%.txt)
MAN_TXT += $(MAN7:%.7=%.txt)

EXTRA_DIST = asciidoc.conf $(MAN_TXT)

if INSTALL_MAN
dist_man_MANS = $(MAN_DOC)
endif

if BUILD_DOC
DISTCLEANFILES = $(MAN_DOC)

dist-hook : $(MAN_DOC)

SUFFIXES=.txt .xml .1 .3 .7

.txt.xml:
	asciidoc -d manpage -b docbook -f $(srcdir)/asciidoc.conf \
        -ajoex_version=@PACKAGE_VERSION@ -o$@ $<
.xml.1:
	xmlto man $<
.xml.3:
	xmlto man $<
.xml.7:
	xmlto man $<

GENERATED_DOCS =
GENERATED_DOCS += joex_server.txt joex_server.doc
joex_server.txt joex_server.doc: ../src/joex_server.c
	./mkman joex_server
GENERATED_DOCS += joex_proto.txt joex_proto.doc
joex_proto.txt joex_proto.doc: ../src/joex_proto.c
	./mkman joex_proto
GENERATED_DOCS += joexd.txt joexd.doc
joexd.txt joexd.doc: ../src/joexd.c
	./mkman joexd joexd
GENERATED_DOCS += joexc.txt joexc.doc
joexc.txt joexc.doc: ../src/joexc.c
	./mkman joexc joexc
clean:
	rm -f *.1 *.3 *.7 $(GENERATED_DOCS)
doc: $(GENERATED_DOCS)

endif
################################################################################
#  THIS FILE IS 100% GENERATED BY ZPROJECT; DO NOT EDIT EXCEPT EXPERIMENTALLY  #
#  Read the zproject/README.md for information about making permanent changes. #
################################################################################
