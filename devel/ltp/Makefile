#
# Copyright (C) 2006-2012 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=ltp-full
PKG_VERSION:=20160510
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.xz
PKG_SOURCE_URL:=https://github.com/linux-test-project/ltp/releases/download/$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk


define Package/ltp
  SECTION:=devel
  CATEGORY:=Development
  TITLE:=Linux test Project
  DEPENDS:=+librpc
  URL:=http://linux-test-project.github.io
endef




define Package/ltp/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/strace $(1)/usr/bin/
endef

$(eval $(call BuildPackage,ltp))
