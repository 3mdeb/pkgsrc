# $NetBSD: Makefile,v 1.35 2021/01/23 14:23:07 bsiegert Exp $

DISTNAME=	go-dns-1.1.3
PKGREVISION=	22
CATEGORIES=	net
MASTER_SITES=	${MASTER_SITE_GITHUB:=miekg/}
GITHUB_PROJECT=	dns
GITHUB_TAG=	v${PKGVERSION_NOREV}
GITHUB_TYPE=	tag

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/miekg/dns
COMMENT=	Complete DNS library for Go
LICENSE=	modified-bsd

GO_DIST_BASE=	${GITHUB_PROJECT}-${GITHUB_TAG:S/v//}
GO_SRCPATH=	github.com/miekg/dns

PFX=		vendor/golang.org

USE_TOOLS+=	bash:run # golang.org/x/sys already switched to bash
REPLACE_BASH+=	${PFX}/x/sys/plan9/mkall.sh
REPLACE_BASH+=	${PFX}/x/sys/plan9/mkerrors.sh
REPLACE_BASH+=	${PFX}/x/sys/unix/mkall.sh
REPLACE_BASH+=	${PFX}/x/sys/unix/mkerrors.sh

REPLACE_PERL+=	${PFX}/x/sys/plan9/mksyscall.pl
REPLACE_PERL+=	${PFX}/x/sys/unix/linux/mksysnum.pl
REPLACE_PERL+=	${PFX}/x/sys/unix/mksyscall.pl
REPLACE_PERL+=	${PFX}/x/sys/unix/mksyscall_solaris.pl
REPLACE_PERL+=	${PFX}/x/sys/unix/mksysctl_openbsd.pl
REPLACE_PERL+=	${PFX}/x/sys/unix/mksysnum_darwin.pl
REPLACE_PERL+=	${PFX}/x/sys/unix/mksysnum_dragonfly.pl
REPLACE_PERL+=	${PFX}/x/sys/unix/mksysnum_freebsd.pl
REPLACE_PERL+=	${PFX}/x/sys/unix/mksysnum_netbsd.pl
REPLACE_PERL+=	${PFX}/x/sys/unix/mksysnum_openbsd.pl

.include "../../lang/go/go-package.mk"
.include "../../mk/bsd.pkg.mk"
