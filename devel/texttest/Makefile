# $NetBSD: Makefile,v 1.5 2020/12/19 11:03:48 schmonz Exp $

DISTNAME=		TextTest-4.0.5
PKGNAME=		${DISTNAME:tl}
CATEGORIES=		devel python
MASTER_SITES=		${MASTER_SITE_SOURCEFORGE:=texttest/}

MAINTAINER=		schmonz@NetBSD.org
HOMEPAGE=		http://texttest.sourceforge.net/
COMMENT=		Tool for text-based Approval Testing
LICENSE=		gnu-lgpl-v2.1

DEPENDS+=		${PYPKGPREFIX}-gobject3-[0-9]*:../../devel/py-gobject3

USE_LANGUAGES=		# none

REPLACE_PYTHON=		texttestlib/default/batch/__init__.py \
			texttestlib/default/virtualdisplay.py

SUBST_CLASSES+=		prefix
SUBST_STAGE.prefix=	pre-configure
SUBST_FILES.prefix=	texttestlib/default/__init__.py
SUBST_VARS.prefix=	PREFIX

.include "../../lang/python/application.mk"
.include "../../lang/python/distutils.mk"
.include "../../x11/gtk3/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
