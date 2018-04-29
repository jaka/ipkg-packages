include $(TOPDIR)/rules.mk

PKG_NAME:=node-agent
PKG_VERSION:=2018-04-29
PKG_RELEASE:=$(PKG_SOURCE_VERSION)

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git://github.com/jaka/node-agent.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=5028dc3f95c78ceec7c6ed1f0f7718fbd6a6a1c1
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	SECTION:=net
	CATEGORY:=Network
	DEPENDS:=+libjson-c +liblibre
	TITLE:=A portable fork of nodewatcher-agent
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./files/node-agent.init $(1)/etc/init.d/node-agent
	$(INSTALL_DIR) $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/node-agent $(1)/usr/bin/
	$(INSTALL_DIR) $(1)/usr/share/node-agent
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/babel.so $(1)/usr/share/node-agent
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/dhcpleases.so $(1)/usr/share/node-agent
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/fileoutput.so $(1)/usr/share/node-agent
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/resources.so $(1)/usr/share/node-agent
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/system.so $(1)/usr/share/node-agent
	$(INSTALL_DIR) $(1)/www/nodewatcher
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
