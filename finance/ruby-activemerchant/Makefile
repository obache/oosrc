# $NetBSD: Makefile,v 1.11 2021/06/14 15:23:12 taca Exp $

DISTNAME=	activemerchant-1.121.0
CATEGORIES=	finance

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://activemerchant.org/
COMMENT=	Ruby library for credit card processing
LICENSE=	mit

DEPENDS+=	${RUBY_ACTIVESUPPORT_DEPENDS}
DEPENDS+=	${RUBY_PKGPREFIX}-builder>=2.1.2:../../textproc/ruby-builder
#DEPENDS+=	${RUBY_PKGPREFIX}-i18n>=0.6.9:../../devel/ruby-i18n
DEPENDS+=	${RUBY_PKGPREFIX}-nokogiri>=1.4<2:../../textproc/ruby-nokogiri

USE_LANGUAGES=	# empty

RUBY_RAILS_ACCEPTED=	# empty

.include "../../lang/ruby/gem.mk"
.include "../../mk/bsd.pkg.mk"
