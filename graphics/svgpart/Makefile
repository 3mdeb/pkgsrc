# $NetBSD: Makefile,v 1.56 2021/02/07 06:30:28 ryoon Exp $

DISTNAME=	svgpart-${KAPPSVER}
PKGREVISION=	6
CATEGORIES=	graphics

HOMEPAGE=	https://kde.org/applications/graphics/
COMMENT=	KDE svg part
LICENSE=	gnu-gpl-v2 AND gnu-fdl-v1.2 AND gnu-lgpl-v2

.include "../../meta-pkgs/kde/applications.mk"

USE_TOOLS+=	msgmerge

.include "../../devel/kparts/buildlink3.mk"
.include "../../x11/qt5-qtbase/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
