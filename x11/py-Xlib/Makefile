# $NetBSD: Makefile,v 1.16 2020/12/19 16:56:34 prlw1 Exp $

DISTNAME=	python-xlib-0.29
PKGNAME=	${PYPKGPREFIX}-${DISTNAME:S/python-x/X/}
CATEGORIES=	x11
MASTER_SITES=	${MASTER_SITE_PYPI:=p/python-xlib/}
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	prlw1@cam.ac.uk
HOMEPAGE=	https://github.com/python-xlib/python-xlib/
COMMENT=	XLib in pure Python
LICENSE=	gnu-lgpl-v2.1

DEPENDS+=	${PYPKGPREFIX}-six>=1.10.0:../../lang/py-six
BUILD_DEPENDS+=	${PYPKGPREFIX}-setuptools_scm-[0-9]*:../../devel/py-setuptools_scm

USE_LANGUAGES=	# none

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
