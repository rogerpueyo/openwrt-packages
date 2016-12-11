#
# Copyright (C) 2016 Roger Pueyo Centelles <roger.pueyo@guifi.net>
#
# This is free software, licensed under the GNU General Public License v3
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=mikrotik_btest
PKG_VERSION:=0.5.1
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/kadosch/mikrotik_btest/archive/$(PKG_VERSION)
PKG_HASH:=ce0d7acc7df5cca2fa0ffcbd9fccd3a6373d06649ad6cc67ca5f0482541fe722

PKG_LICENSE:=GPLv3
PKG_LICENSE_FILES:=COPYING

include $(INCLUDE_DIR)/package.mk

define Package/mikrotik-btest
  SECTION:=net
  CATEGORY:=Network
  TITLE:=Bandwidth test client for Mikrotik BTest server
  DEPENDS:=+libpthread +librt
  URL:=https://github.com/kadosch/mikrotik_btest.git
  MAINTAINER:=Roger Pueyo Centelles <roger.pueyo@guifi.net>
endef

define Package/mikrotik-btest/description
	A bandwidth test client compatible with Mikrotik's RouterOS BTest server.
endef

define Package/mikrotik-btest/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/mikrotik_btest $(1)/usr/bin/mikrotik_btest
endef

$(eval $(call BuildPackage,mikrotik-btest))
