COMMENT =		Utilities for Starkast
V =			0.1.3
DISTNAME =		Starkast-Utilities-${V}
CATEGORIES =		utilities
MAINTAINER =		jage@starkast.net

# Licensing
PERMIT_PACKAGE_CDROM =	Yes 
PERMIT_PACKAGE_FTP =	Yes
PERMIT_DISTFILES_CDROM =Yes
PERMIT_DISTFILES_FTP =	Yes

MASTER_SITES =		http://github.com/Starkast/Utilities/tarball/
# Wierd filename, Github ...
DISTFILES =		0.1.3

# Just scripts
NO_BUILD =		Yes
NO_REGRESS =		Yes

do-install:
	# Don't know the name of the directory, rename to something we know
	@cd ${WRKDIR} && mv Starkast-Utilities-*/* ${DISTNAME}/
	${INSTALL_SCRIPT} ${WRKSRC}/bin/* ${PREFIX}/bin/
	${INSTALL_SCRIPT} ${WRKSRC}/sbin/* ${PREFIX}/sbin/
	${INSTALL_SCRIPT} ${WRKSRC}/libexec/* ${PREFIX}/libexec/
	${INSTALL_DATA} ${WRKSRC}/lib/* ${PREFIX}/lib/
	${INSTALL_DATA_DIR} ${WRKSRC}/libdata/* ${PREFIX}/libdata/


.include <bsd.port.mk>
