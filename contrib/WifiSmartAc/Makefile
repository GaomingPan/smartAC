# Copyright (C) 2006,2008 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk
PKG_NAME:=WifiSmartAc
PKG_VERSION:=0.0.1
PKG_RELEASE:=Beta-1
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:= @SF/$(PKG_NAME)
PKG_MD5SUM:=
PKG_FIXUP:=autoreconf
PKG_INSTALL:=1
include $(INCLUDE_DIR)/package.mk
define Package/WifiSmartAc
	SECTION:=WifiSmartAc
	CATEGORY:=WifiAC
	DEPENDS:=+uci +libpthread
	TITLE:=A client for the remote server interface to setting the ap
	URL:=http://www.exrample.org
endef
define Package/WifiSmartAc/description
This software is a client for the remote server interface to setting the ap.
endef
define Package/WifiSmartAc/conffiles
/etc/smartac.conf
endef
define Package/WifiSmartAc/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/src/WifiSmartAc $(1)/usr/sbin
	$(INSTALL_DIR) $(1)/etc
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/etc/wifismartac.conf $(1)/etc/wifismartac.conf
endef
$(eval $(call BuildPackage,WifiSmartAc))


