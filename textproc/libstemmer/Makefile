# $NetBSD: Makefile,v 1.3 2021/02/18 10:26:56 wiz Exp $

DISTNAME=	snowball-2.1.0
PKGNAME=	${DISTNAME:S/snowball/libstemmer/}
CATEGORIES=	textproc
MASTER_SITES=	${MASTER_SITE_GITHUB:=snowballstem/}
GITHUB_PROJECT=	snowball
GITHUB_TAG=	v${PKGVERSION_NOREV}

MAINTAINER=	ryoon@NetBSD.org
HOMEPAGE=	https://snowballstem.org/
COMMENT=	Snowball compiler and the stemming algorithms
LICENSE=	modified-bsd

USE_TOOLS+=	gmake perl
MAKE_FILE=	GNUmakefile

INSTALLATION_DIRS+=	bin include lib

do-install:
	${INSTALL_DATA} ${WRKSRC}/include/libstemmer.h \
		${DESTDIR}${PREFIX}/include
	${INSTALL_LIB} ${WRKSRC}/libstemmer.so.0.0.0 \
		${DESTDIR}${PREFIX}/lib
	${LN} -sf libstemmer.so.0.0.0 \
		${DESTDIR}${PREFIX}/lib/libstemmer.so.0
	${LN} -sf libstemmer.so.0.0.0 \
		${DESTDIR}${PREFIX}/lib/libstemmer.so

.include "../../mk/bsd.pkg.mk"
