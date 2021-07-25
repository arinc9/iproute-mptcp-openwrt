#
# Copyright (C) 2021 Arınç ÜNAL <arinc.unal@arinc9.com>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=iproute-mptcp
PKG_VERSION:=5.4.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/multipath-tcp/iproute-mptcp
PKG_SOURCE_VERSION:=825d9e1245d90171bc787280560e9749402aa90a
PKG_MIRROR_HASH:=17bcb541afceb1a4073508a6bdef81196e66e88ab8b9987a7bf28066d0e839a7

PKG_BUILD_PARALLEL:=1
PKG_LICENSE:=GPL-2.0

include $(INCLUDE_DIR)/package.mk

define Package/iproute-mptcp
  TITLE:=Routing control utility (multipath)
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Routing and Redirection
  DEPENDS:=+libselinux +libmnl +libelf
  ALTERNATIVES:=:/sbin/ip:/usr/libexec/iproute-mptcp
endef

define Package/iproute-mptcp/install
	$(INSTALL_DIR) $(1)/usr/libexec
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/ip/ip $(1)/usr/libexec/iproute-mptcp
endef

$(eval $(call BuildPackage,iproute-mptcp))
