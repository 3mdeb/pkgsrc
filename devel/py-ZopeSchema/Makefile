# $NetBSD: Makefile,v 1.6 2021/02/09 07:26:29 adam Exp $

DISTNAME=	zope.schema-6.0.1
PKGNAME=	${PYPKGPREFIX}-${DISTNAME:S/zope.s/ZopeS/}
CATEGORIES=	devel python
MASTER_SITES=	${MASTER_SITE_PYPI:=z/zope.schema/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/zopefoundation/zope.schema
COMMENT=	Zope Interface extension for defining data schemas
LICENSE=	zpl-2.1

DEPENDS+=	${PYPKGPREFIX}-ZopeEvent-[0-9]*:../../devel/py-ZopeEvent
DEPENDS+=	${PYPKGPREFIX}-ZopeInterface>=5.0.0:../../devel/py-ZopeInterface
TEST_DEPENDS+=	${PYPKGPREFIX}-ZopeI18NMessageid-[0-9]*:../../devel/py-ZopeI18NMessageid
TEST_DEPENDS+=	${PYPKGPREFIX}-ZopeTestrunner-[0-9]*:../../devel/py-ZopeTestrunner
TEST_DEPENDS+=	${PYPKGPREFIX}-zope.testing-[0-9]*:../../devel/py-zope.testing

PYTHON_VERSIONED_DEPENDENCIES+=	setuptools

.include "../../lang/python/egg.mk"
.include "../../lang/python/versioned_dependencies.mk"
.include "../../mk/bsd.pkg.mk"
