# $NetBSD: Makefile,v 1.9 2021/02/27 19:17:56 ryoon Exp $

GITHUB_PROJECT=	libkkc
GITHUB_RELEASE=	v${PKGVERSION_NOREV}
DISTNAME=	libkkc-0.3.5
PKGREVISION=	2
CATEGORIES=	converters textproc japanese inputmethod
MASTER_SITES=	${MASTER_SITE_GITHUB:=ueno/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/ueno/libkkc/
COMMENT=	Japanese Kana Kanji conversion library
LICENSE=	gnu-gpl-v3

PYTHON_VERSIONS_ACCEPTED=	27 # py-marisa
BUILD_DEPENDS+=	${PYPKGPREFIX}-marisa-[0-9]*:../../textproc/py-marisa

GNU_CONFIGURE=		yes
USE_LIBTOOL=		yes
USE_TOOLS+=		gmake intltool msgfmt pkg-config
USE_LANGUAGES=		c c++
USE_PKGLOCALEDIR=	yes

PKGCONFIG_OVERRIDE+=	libkkc/kkc-1.0.pc.in

TEST_TARGET=	check

PYTHON_FOR_BUILD_ONLY=	yes
.include "../../lang/python/application.mk"
.include "../../devel/glib2/buildlink3.mk"
BUILDLINK_DEPMETHOD.gobject-introspection+=	build
.include "../../devel/gobject-introspection/buildlink3.mk"
.include "../../devel/libgee/buildlink3.mk"
.include "../../textproc/json-glib/buildlink3.mk"
.include "../../textproc/marisa/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
