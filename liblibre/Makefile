PKG_NAME:=liblibre
PKG_VERSION:=2018-04-21
PKG_RELEASE:=$(PKG_SOURCE_VERSION)

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git://github.com/jaka/liblibre.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=a03571d2f072157aa32437e4a57ecf84a79da9ae
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	SECTION:=libs
	CATEGORY:=Libraries
	TITLE:=C library for event driven main loop, circular stream buffer and parsing arguments
endef

define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/include/libre
	$(CP) $(PKG_BUILD_DIR)/include $(1)/usr/include/libre/
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/lib/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/liblibre.so $(1)/usr/lib/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
