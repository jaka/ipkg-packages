include $(TOPDIR)/rules.mk

PKG_NAME:=usbtemp-cli
PKG_VERSION:=2018-03-07
PKG_RELEASE:=$(PKG_SOURCE_VERSION)

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git://github.com/usbtemp/usbtemp-cli.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=bbf04f1ba8dbb3cf4a51fdd8f216fcd34b984393
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	CATEGORY:=Utilities
	TITLE:=Read temperature from USB thermometer
	DEPENDS:=+kmod-usb-serial +kmod-usb-serial-pl2303
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/usbtemp-cli $(1)/usr/bin/usbtemp-cli
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
