COMMENT =		Compile and install Ruby
V =			20120423
DISTNAME =		ruby-build-${V}
CATEGORIES =		devel
MAINTAINER =		patrik@starkast.net

# Licensing
PERMIT_PACKAGE_CDROM =	Yes 
PERMIT_PACKAGE_FTP =	Yes
PERMIT_DISTFILES_CDROM =Yes
PERMIT_DISTFILES_FTP =	Yes

MASTER_SITES =		http://github.com/sstephenson/ruby-build/tarball/
# Wierd filename, Github ...
DISTFILES =		v${V}

# Just scripts
NO_BUILD =		Yes
NO_REGRESS =		Yes

do-install:
	# Don't know the name of the directory, rename to something we know
	@cd ${WRKDIR} && mv sstephenson-ruby-build-*/* ${DISTNAME}/
	${INSTALL_SCRIPT} ${WRKSRC}/bin/* ${PREFIX}/bin/
	${INSTALL_DATA_DIR} ${PREFIX}/share/ruby-build/
	${INSTALL_DATA} ${WRKSRC}/share/ruby-build/* \
		${PREFIX}/share/ruby-build/


.include <bsd.port.mk>
