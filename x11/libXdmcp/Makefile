# $NetBSD: Makefile,v 1.11 2020/01/18 23:35:51 rillig Exp $

DISTNAME=		libXdmcp-1.1.3
CATEGORIES=		x11
MASTER_SITES=		${MASTER_SITE_XORG:=lib/}
EXTRACT_SUFX=		.tar.bz2

MAINTAINER=		joerg@NetBSD.org
HOMEPAGE=		https://xorg.freedesktop.org/
COMMENT=		X Display Manager Control Protocol library from X.org

USE_LIBTOOL=		yes
USE_TOOLS+=		pkg-config
PKGCONFIG_OVERRIDE+=	xdmcp.pc.in
GNU_CONFIGURE=		yes

.include "../../meta-pkgs/modular-xorg/hacks.mk"

.include "../../x11/xorgproto/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
