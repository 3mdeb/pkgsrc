# $NetBSD: Makefile,v 1.1 2021/02/12 08:15:51 pin Exp $

DISTNAME=	lok-0.1.2
CATEGORIES=	textproc devel
MASTER_SITES=	${MASTER_SITE_GITHUB:=wyhaya/}
GITHUB_TAG=	v${PKGVERSION_NOREV}

MAINTAINER=	pin@NetBSD.org
HOMEPAGE=	https://github.com/wyhaya/lok/
COMMENT=	Count the number of codes
LICENSE=	mit

.include "cargo-depends.mk"

USE_LANGUAGES+=	c

INSTALLATION_DIRS=	bin

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/target/release/lok ${DESTDIR}${PREFIX}/bin

.include "../../lang/rust/cargo.mk"
.include "../../mk/bsd.pkg.mk"
