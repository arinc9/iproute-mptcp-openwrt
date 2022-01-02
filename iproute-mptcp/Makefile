#
# Copyright (C) 2021 Arınç ÜNAL <arinc.unal@arinc9.com>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=iproute-mptcp
PKG_VERSION:=5.15.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/multipath-tcp/iproute-mptcp
PKG_SOURCE_VERSION:=791723bdb4efd3bb2b67e5c21d367eadd35b54c0
PKG_MIRROR_HASH:=79fd73546e7e55422132f1dad4489c91a5326a78cf894e1d415c6b3138956afd

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
