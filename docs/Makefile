DOCS = yum-changelog yum-list-data yum-filter-data yum-verify yum-utils yum-aliases \
       yum-versionlock yum-fs-snapshot yum-ovl
DOCS_DEPRECATED = debuginfo-install find-repos-of-install needs-restarting package-cleanup \
                  repoclosure repodiff repomanage repoquery repotrack reposync repo-graph \
                  repo-rss verifytree yumdownloader yum-builddep yum-config-manager yum-debug-dump \
                  yum-debug-restore yum-groups-manager show-installed show-changed-rco
DOCS5 = yum-changelog.conf yum-versionlock.conf yum-fs-snapshot.conf
DOCS8 = yum-copr
DOCS8_DEPRECATED = yum-complete-transaction yumdb

all:
	echo "Nothing to do"

clean:
	rm -f *.pyc *.pyo *~

install:
	mkdir -p $(DESTDIR)/usr/share/man/man1
	mkdir -p $(DESTDIR)/usr/share/man/man5
	mkdir -p $(DESTDIR)/usr/share/man/man8
	for doc in $(DOCS); do \
		install -m 644 $$doc.1 $(DESTDIR)/usr/share/man/man1/; \
	done
	for doc in $(DOCS_DEPRECATED); do \
		install -m 644 $$doc.1 $(DESTDIR)/usr/share/man/man1/$$doc-deprecated.1; \
	done
	for doc in $(DOCS5); do \
		install -m 644 $$doc.5 $(DESTDIR)/usr/share/man/man5/; \
	done
	for doc in $(DOCS8); do \
		install -m 644 $$doc.8 $(DESTDIR)/usr/share/man/man8/; \
	done
	for doc in $(DOCS8_DEPRECATED); do \
		install -m 644 $$doc.8 $(DESTDIR)/usr/share/man/man8/$$doc-deprecated.8; \
	done
