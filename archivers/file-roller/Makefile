# $NetBSD: Makefile,v 1.151 2021/05/02 10:24:47 nia Exp $

DISTNAME=	file-roller-3.38.0
MASTER_SITES=	${MASTER_SITE_GNOME:=/sources/${PKGBASE}/${PKGVERSION_NOREV:R}/}
CATEGORIES=	archivers gnome
EXTRACT_SUFX=	.tar.xz

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://wiki.gnome.org/Apps/FileRoller
COMMENT=	Archive manager for the GNOME desktop environment
LICENSE=	gnu-gpl-v2

USE_TOOLS+=	msgfmt pkg-config itstool

MESON_ARGS+=	-Dpackagekit=false
MESON_ARGS+=	-Dnautilus-actions=false

.include "../../mk/bsd.prefs.mk"

# msgfmt: unknown option -- xml
GETTEXT_TOOLS_REQD=	0.19.7

PYTHON_FOR_BUILD_ONLY=	tool

.include "../../devel/meson/build.mk"
.include "../../archivers/libarchive/buildlink3.mk"
.include "../../devel/glib2/schemas.mk"
.include "../../graphics/hicolor-icon-theme/buildlink3.mk"
.include "../../lang/python/tool.mk"
.include "../../sysutils/desktop-file-utils/desktopdb.mk"
.include "../../sysutils/libnotify/buildlink3.mk"
.include "../../textproc/json-glib/buildlink3.mk"
.include "../../x11/gtk3/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
