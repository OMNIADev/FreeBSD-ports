# Created by: Koop Mast <kwm@rainbow-runner.nl>
# $FreeBSD$

PORTNAME=	gstreamer1-vaapi
PORTVERSION=	1.8.0
PORTREVISION=	3
CATEGORIES=	multimedia
MASTER_SITES=	https://gstreamer.freedesktop.org/src/gstreamer-vaapi/
DISTNAME=	gstreamer-vaapi-${PORTVERSION}

MAINTAINER=	multimedia@FreeBSD.org
COMMENT=	GStreamer hardware video decoding via VA-API plug-in

LICENSE=	LGPL21

LIB_DEPENDS=	libva.so:multimedia/libva

GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--disable-wayland
INSTALL_TARGET=	install-strip
USES=		compiler:c11 gmake libtool pkgconfig tar:xz
USE_LDCONFIG=	yes
USE_GSTREAMER1=	bad gl
USE_GL=		gl
USE_XORG=	x11 xrandr xrender xproto:build

# drm backend needs libudev so disable it for now.
CONFIGURE_ARGS+=--disable-drm

.include <bsd.port.mk>
