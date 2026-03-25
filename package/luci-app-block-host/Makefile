#
# Copyright (C) 2025 OpenWrt.org
#
# This is free software, licensed under the Apache License, Version 2.0 .
#

include $(TOPDIR)/rules.mk

LUCI_TITLE:=LuCI support for blocking hosts by hostname
LUCI_PKGARCH:=all
LUCI_DEPENDS:=+nftables

PKG_NAME:=luci-app-block-host
PKG_VERSION:=1.0.0
PKG_RELEASE:=1

# 从 src 目录复制源码到 package
define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	cp -r $(CURDIR)/../src/* $(PKG_BUILD_DIR)/
endef

include $(TOPDIR)/feeds/luci/luci.mk

# call BuildPackage - OpenWrt buildroot signature
