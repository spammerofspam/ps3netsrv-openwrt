include $(TOPDIR)/rules.mk

PKG_NAME:=udpbd-server
PKG_RELEASE:=1
PKG_LICENSE:=GPLv3

PKG_MAINTAINER:=Me

include $(INCLUDE_DIR)/package.mk

define Package/udpbd-server
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=File Transfer
  TITLE:=PS2 UDPBD server
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Compile
	$(TARGET_CXX) $(TARGET_CPPFLAGS) $(TARGET_CFLAGS) -o $(PKG_BUILD_DIR)/udpbd-server main.cpp $(TARGET_LDFLAGS)
endef

define Package/udpbd-server/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/udpbd-server $(1)/usr/bin/udpbd-server
endef

$(eval $(call BuildPackage,udpbd-server))