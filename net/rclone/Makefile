# $NetBSD: Makefile,v 1.16 2021/02/11 22:02:19 leot Exp $

# When updating changelog is available in
# ${WRKSRC}/docs/content/changelog.md
DISTNAME=	rclone-1.54.0
CATEGORIES=	net
MASTER_SITES=	${MASTER_SITE_GITHUB:=rclone/}
GITHUB_TAG=	v${PKGVERSION_NOREV}

MAINTAINER=	leot@NetBSD.org
HOMEPAGE=	https://rclone.org/
COMMENT=	Rsync for cloud storage
LICENSE=	mit

GO_BUILD_PATTERN=	--ldflags "-X github.com/rclone/rclone/fs.Version=${PKGVERSION_NOREV}"

CHECK_RELRO_SKIP+=	bin/rclone

INSTALLATION_DIRS+=	bin ${PKGMANDIR}/man1

do-install:
	${INSTALL_PROGRAM} ${WRKDIR}/.gopath/bin/rclone ${DESTDIR}${PREFIX}/bin
	${INSTALL_MAN} ${WRKSRC}/rclone.1 ${DESTDIR}${PREFIX}/${PKGMANDIR}/man1

.include "go-modules.mk"

.include "../../lang/go/go-module.mk"
.include "../../mk/bsd.pkg.mk"
