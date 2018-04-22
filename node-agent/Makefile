include $(TOPDIR)/rules.mk

PKG_NAME:=node-agent
PKG_VERSION:=2018-04-22
PKG_RELEASE:=$(PKG_SOURCE_VERSION)

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git://github.com/jaka/node-agent.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=cfa29df338fa7a29064b2c1fc7e9bb72f7d5d660
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	SECTION:=net
	CATEGORY:=Network
	DEPENDS:=+libjson-c +liblibre
	TITLE:=A portable fork of nodewatcher-agent
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/node-agent $(1)/usr/bin/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
