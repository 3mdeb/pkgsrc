# $NetBSD: Makefile,v 1.44 2020/08/31 18:11:35 wiz Exp $
#

DISTNAME=		roller-1.21
PKGREVISION=		#
PKGREVISION=		1
CATEGORIES=		sysutils
MASTER_SITES=		http://software.kimmo.suominen.com/

MAINTAINER=		pkgsrc-users@NetBSD.org
COMMENT=		Roll log files

DEPENDS+=		cpogm-[0-9]*:../../sysutils/cpogm
DEPENDS+=		logtime-[0-9]*:../../time/logtime
DEPENDS+=		pflogsumm>=1.1.5:../../sysutils/pflogsumm

.include "../../mk/bsd.prefs.mk"

NO_CONFIGURE=		yes
USE_TOOLS+=		perl:run

BUILD_MAKE_FLAGS+=	PREFIX=${PREFIX}
INSTALL_MAKE_FLAGS+=	PREFIX=${DESTDIR}${PREFIX}

MAKE_FLAGS+=		GAWK=${AWK}
MAKE_FLAGS+=		PERL=${PERL5}
MAKE_FLAGS+=		SH=${SH}

.include "../../mk/bsd.pkg.mk"
