# $NetBSD: Makefile,v 1.21 2021/01/16 13:08:39 taca Exp $

DISTNAME=	pygments.rb-2.0.0
CATEGORIES=	textproc

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/tmm1/pygments.rb
COMMENT=	Pygments wrapper for ruby
LICENSE=	mit

DEPENDS+=	${RUBY_PKGPREFIX}-multi_json>=1.0.0:../../textproc/ruby-multi_json

REPLACE_PYTHON=	lib/pygments/mentos.py

.include "../../lang/ruby/gem.mk"
.include "../../lang/python/application.mk"
.include "../../mk/bsd.pkg.mk"
