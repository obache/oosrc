# $NetBSD: Makefile,v 1.27 2020/12/04 20:45:17 nia Exp $

DISTNAME=	wikipediafs-0.4
PKGNAME=	fuse-${DISTNAME}
PKGREVISION=	2
CATEGORIES=	filesystems
MASTER_SITES=	${MASTER_SITE_SOURCEFORGE:=wikipediafs/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://wikipediafs.sourceforge.net/
COMMENT=	FUSE filesystem for accessing the wikipedia
LICENSE=	gnu-gpl-v2

DEPENDS+=	${PYPKGPREFIX}-fuse-bindings-[0-9]*:../../filesystems/py-fuse-bindings

PYTHON_VERSIONS_ACCEPTED= 27 # py-fuse-bindings
EGG_NAME=	wikipediafs-0.0.0

SUBST_CLASSES+=		config
SUBST_STAGE.config=	pre-configure
SUBST_FILES.config=	setup.py
SUBST_SED.config+=	-e "s|/usr/share/man/man1/|${PKGMANDIR}/man1/|g"
SUBST_MESSAGE.config=	Fixing paths.

.include "../../lang/python/distutils.mk"
.include "../../mk/fuse.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
