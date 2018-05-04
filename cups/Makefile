#
# Copyright (C) 2006-2016 OpenWrt.org
# Copyright (C) 2016 lede-project.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=cups
PKG_VERSION:=2.2.6
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-source.tar.gz
PKG_SOURCE_URL:=https://github.com/apple/cups/releases/download/v$(PKG_VERSION)/
PKG_MD5SUM:=e91c26d8d97b5a1630a962f530f02192

TARGET_LDFLAGS+=-Wl,-rpath-link=$(STAGING_DIR)/usr/lib

include $(INCLUDE_DIR)/package.mk

define Package/cups/Default
  URL:=http://www.cups.org/
  SUBMENU:=Printing
endef

define Package/cups
$(call Package/cups/Default)
  SECTION:=net
  CATEGORY:=Network
  DEPENDS:=+libcups +libcupsmime +libcupscgi +libcupsppdc +libusb-1.0
  TITLE:=Common UNIX Printing System (daemon)
endef

define Package/cups/description
	Common UNIX Printing System (daemon)
endef

define Package/cups/conffiles
/etc/cups/classes.conf
/etc/cups/cupsd.conf
/etc/cups/printers.conf
endef

define Package/cups-bsd
$(call Package/cups/Default)
  SECTION:=net
  CATEGORY:=Network
  DEPENDS:=+libcups
  TITLE:=Common UNIX Printing System - BSD commands (old)
endef

define Package/cups-bsd/description
	Common UNIX Printing System - BSD commands (old)
endef

define Package/cups-client
$(call Package/cups/Default)
  SECTION:=net
  CATEGORY:=Network
  DEPENDS:=+libcups +libcupsimage +libcupsmime
  TITLE:=Common UNIX Printing System - Client commands
endef

define Package/cups-client/conffiles
/etc/cups/client.conf
endef

define Package/cups-client/description
	Common UNIX Printing System - Client commands
endef

define Package/cups-filters
$(call Package/cups/Default)
  SECTION:=net
  CATEGORY:=Network
  DEPENDS:=+libcupsimage
  TITLE:=Common UNIX Printing System - Filter
endef

define Package/cups-filters/description
	Common UNIX Printing System - Filter
endef

define Package/cups-ppdc
$(call Package/cups/Default)
  SECTION:=net
  CATEGORY:=Network
  DEPENDS:=+libcupsppdc
  TITLE:=Common UNIX Printing System - PPDC utils
endef

define Package/cups-ppdc/description
	Common UNIX Printing System - PPDC utils
endef

define Package/libcups
$(call Package/cups/Default)
  SECTION:=libs
  CATEGORY:=Libraries
  DEPENDS:=+zlib +libpthread +libpng +libjpeg
  TITLE:=Common UNIX Printing System - Core library
endef

define Package/libcups/description
	Common UNIX Printing System - Core library
endef

define Package/libcupscgi
$(call Package/cups/Default)
  SECTION:=libs
  CATEGORY:=Libraries
  DEPENDS:=+libcups
  TITLE:=Common UNIX Printing System - CGI library
endef

define Package/libcupscgi/description
	Common UNIX Printing System - CGI library
endef

define Package/libcupsimage
$(call Package/cups/Default)
  SECTION:=libs
  CATEGORY:=Libraries
  DEPENDS:=+libcups
  TITLE:=Common UNIX Printing System - Image library
endef

define Package/libcupsimage/description
	Common UNIX Printing System - Image library
endef

define Package/libcupsmime
$(call Package/cups/Default)
  SECTION:=libs
  CATEGORY:=Libraries
  DEPENDS:=+libcups
  TITLE:=Common UNIX Printing System - MIME library
endef

define Package/libcupsmime/description
	Common UNIX Printing System - MIME library
endef

define Package/libcupsppdc
$(call Package/cups/Default)
  SECTION:=libs
  CATEGORY:=Libraries
  DEPENDS:=+libcups +libstdcpp
  TITLE:=Common UNIX Printing System - PPDC library
endef

define Package/libcupsppdc/description
	Common UNIX Printing System - PPDC library
endef



define Package/cups-locale-zhcn
  SECTION:=net
  CATEGORY:=Network
  TITLE:=Chinese locale for CUPS
    DEPENDS:=cups
  SUBMENU:=Printing
endef

define Package/cups-locale-zhcn/description
	CUPS Chinese locale resouces.
endef



define Package/cups-locale-ca
  SECTION:=net
  CATEGORY:=Network
  TITLE:=Catalan locale for CUPS
    DEPENDS:=cups
  SUBMENU:=Printing
endef

define Package/cups-locale-ca/description
	CUPS Catalan locale resouces.
endef


define Package/cups-locale-cs
  SECTION:=net
  CATEGORY:=Network
  TITLE:=Czech locale for CUPS
    DEPENDS:=cups
  SUBMENU:=Printing
endef

define Package/cups-locale-cs/description
	CUPS Czech locale resouces.
endef


define Package/cups-locale-de
  SECTION:=net
  CATEGORY:=Network
  TITLE:=German locale for CUPS
    DEPENDS:=cups
  SUBMENU:=Printing
endef

define Package/cups-locale-de/description
	CUPS German locale resouces.
endef


define Package/cups-locale-es
  SECTION:=net
  CATEGORY:=Network
  TITLE:=Spanish locale for CUPS
    DEPENDS:=cups
  SUBMENU:=Printing
endef

define Package/cups-locale-es/description
	CUPS Spanish locale resouces.
endef


define Package/cups-locale-fr
  SECTION:=net
  CATEGORY:=Network
  TITLE:=French locale for CUPS
    DEPENDS:=cups
  SUBMENU:=Printing
endef

define Package/cups-locale-fr/description
	CUPS French locale resouces.
endef


define Package/cups-locale-it
  SECTION:=net
  CATEGORY:=Network
  TITLE:=Italian locale for CUPS
    DEPENDS:=cups
  SUBMENU:=Printing
endef

define Package/cups-locale-it/description
	CUPS Italian locale resouces.
endef


define Package/cups-locale-ja
  SECTION:=net
  CATEGORY:=Network
  TITLE:=Japanese locale for CUPS
    DEPENDS:=cups
  SUBMENU:=Printing
endef

define Package/cups-locale-ja/description
	CUPS Japanese locale resouces.
endef


define Package/cups-locale-ptBR
  SECTION:=net
  CATEGORY:=Network
  TITLE:=Brazilian Portuguese locale for CUPS
    DEPENDS:=cups
  SUBMENU:=Printing
endef

define Package/cups-locale-ptBR/description
	CUPS Brazilian Portuguese locale resouces.
endef


define Package/cups-locale-ru
  SECTION:=net
  CATEGORY:=Network
  TITLE:=Russian locale for CUPS
    DEPENDS:=cups
  SUBMENU:=Printing
endef

define Package/cups-locale-ru/description
	CUPS Russian locale resouces.
endef



define Build/Configure
	$(call Build/Configure/Default, \
		--with-cups-user="nobody" \
		--with-cups-group="nogroup" \
		--with-system-groups="root" \
		--with-pdftops="none" \
		--without-perl \
		--without-python \
		--without-php \
		--enable-default-shared \
		--enable-shared \
		--enable-image \
		--enable-libusb \
		--disable-acl \
		--disable-dnssd \
		--disable-dbus \
		--disable-avahi \
		--disable-launchd \
		--disable-ldap \
		--disable-pam \
		--disable-slp \
		--disable-gnutls \
		--disable-openssl \
		--disable-cdsassl \
		--disable-ssl \
		--disable-gssapi \
		--disable-tiff, \
		UNAME="Linux" \
		LIBS="$(TARGET_LDFLAGS) -lz -lpng -ljpeg" \
	)
endef

define Build/Compile
	$(MAKE) -C $(PKG_BUILD_DIR) \
		$(TARGET_CONFIGURE_OPTS) \
		DSTROOT="$(PKG_INSTALL_DIR)" \
		STRIP="/bin/true" \
		all install
endef

define Package/cups/install
	rm -rf $(1)/etc/cups
	$(INSTALL_DIR) $(1)/etc/cups
	$(CP) $(PKG_INSTALL_DIR)/etc/cups/* $(1)/etc/cups/
	rm -rf $(1)/etc/cups/certs
	ln -sf /tmp $(1)/etc/cups/certs
	rm -f $(1)/usr/bin/cups-config
	$(INSTALL_DIR) $(1)/usr/lib/cups
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/cups/backend $(1)/usr/lib/cups
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/cups/cgi-bin $(1)/usr/lib/cups
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/cups/daemon $(1)/usr/lib/cups
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/cups/driver $(1)/usr/lib/cups
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/cups/monitor $(1)/usr/lib/cups
	$(INSTALL_DIR) $(1)/usr/share/cups/templates
	$(CP) $(PKG_INSTALL_DIR)/usr/share/cups/templates/*.tmpl \
		$(1)/usr/share/cups/templates/
	$(INSTALL_DIR) $(1)/usr/share/cups/mime
	$(CP) $(PKG_INSTALL_DIR)/usr/share/cups/mime/* $(1)/usr/share/cups/mime/
	$(INSTALL_DIR) $(1)/usr/share/icons/hicolor/16x16/apps
	$(CP) $(PKG_INSTALL_DIR)/usr/share/icons/hicolor/16x16/apps/cups.png $(1)/usr/share/icons/hicolor/16x16/apps/
	$(INSTALL_DIR) $(1)/usr/share/icons/hicolor/32x32/apps
	$(CP) $(PKG_INSTALL_DIR)/usr/share/icons/hicolor/32x32/apps/cups.png $(1)/usr/share/icons/hicolor/32x32/apps/
	### Do install docs: cups web interface relies on them
	$(INSTALL_DIR) $(1)/usr/share/doc/cups
	$(CP) $(PKG_INSTALL_DIR)/usr/share/doc/cups/*.*html \
		$(1)/usr/share/doc/cups/
	$(CP) $(PKG_INSTALL_DIR)/usr/share/doc/cups/*.css \
		$(1)/usr/share/doc/cups/
	$(CP) $(PKG_INSTALL_DIR)/usr/share/doc/cups/*.txt \
		$(1)/usr/share/doc/cups/
	$(CP) $(PKG_INSTALL_DIR)/usr/share/doc/cups/*.txt \
		$(1)/usr/share/doc/cups/
	$(CP) $(PKG_INSTALL_DIR)/usr/share/doc/cups/images \
		$(1)/usr/share/doc/cups/
	$(CP) $(PKG_INSTALL_DIR)/usr/share/doc/cups/help \
		$(1)/usr/share/doc/cups/
	$(INSTALL_DIR) $(1)/usr/sbin
	# overwrite default config with our own
	$(CP) ./files/etc/cups/* $(1)/etc/cups/
	# install initscript with priority 60
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./files/cupsd.init $(1)/etc/init.d/cupsd
	$(INSTALL_BIN) \
		$(PKG_INSTALL_DIR)/usr/sbin/{cupsctl,cupsd} \
		$(1)/usr/sbin/
	# needed for cups to find usb printers per http://wiki.openwrt.org/doc/howto/cups.server
	chmod 700 $(1)/usr/lib/cups/backend/usb
endef

define Package/cups-bsd/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/{lprm,lpq,lpr} $(1)/usr/bin/
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/sbin/lpc $(1)/usr/sbin/
endef

define Package/cups-client/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) \
		$(PKG_INSTALL_DIR)/usr/bin/{lp,cancel,cupstestppd,cupstestdsc,cups-config} \
		$(PKG_INSTALL_DIR)/usr/bin/{ipptool,lpoptions,lpstat} \
		$(1)/usr/bin/
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) \
		$(PKG_INSTALL_DIR)/usr/sbin/{cupsaccept,cupsaddsmb,cupsfilter} \
		$(PKG_INSTALL_DIR)/usr/sbin/{lpadmin,lpinfo,lpmove} \
		$(1)/usr/sbin/
	(cd $(1)/usr/sbin; ln -sf cupsaccept accept; ln -sf cupsaccept cupsenable; ln -sf cupsaccept cupsdisable; ln -sf cupsaccept reject; ln -sf cupsaccept cupsreject;)
	$(INSTALL_DIR) $(1)/usr/share/cups/ipptool
	$(CP) $(PKG_INSTALL_DIR)/usr/share/cups/ipptool/* \
		$(1)/usr/share/cups/ipptool/
endef

define Package/cups-filters/install
	$(INSTALL_DIR) $(1)/usr/lib/cups/filter
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/cups/filter/{commandtops,gziptoany,pstops,rastertoepson,rastertohp,rastertolabel,rastertopwg} \
		$(1)/usr/lib/cups/filter
	(cd $(1)/usr/lib/cups/filter; ln -sf rastertolabel rastertodymo;)
endef

define Package/cups-ppdc/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) \
		$(PKG_INSTALL_DIR)/usr/bin/{ppdc,ppdhtml,ppdi,ppdmerge,ppdpo} \
		$(1)/usr/bin/
endef

define Package/libcups/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libcups.so* $(1)/usr/lib/
endef

define Package/libcupscgi/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libcupscgi.so* $(1)/usr/lib/
endef

define Package/libcupsimage/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libcupsimage.so* $(1)/usr/lib/
endef

define Package/libcupsmime/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libcupsmime.so* $(1)/usr/lib/
endef

define Package/libcupsppdc/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libcupsppdc.so* $(1)/usr/lib/
endef



define Package/cups-locale-ca/install
	$(INSTALL_DIR) $(1)/usr/share/locale/ca
	$(CP) $(PKG_INSTALL_DIR)/usr/share/locale/ca/* $(1)/usr/share/locale/ca/
endef

define Package/cups-locale-cs/install
	$(INSTALL_DIR) $(1)/usr/share/locale/cs
	$(CP) $(PKG_INSTALL_DIR)/usr/share/locale/cs/* $(1)/usr/share/locale/cs/
endef

define Package/cups-locale-de/install
	$(INSTALL_DIR) $(1)/usr/share/locale/de
	$(CP) $(PKG_INSTALL_DIR)/usr/share/locale/de/* $(1)/usr/share/locale/de/
	$(INSTALL_DIR) $(1)/usr/share/cups/templates/de
	$(CP) $(PKG_INSTALL_DIR)/usr/share/cups/templates/de/*.tmpl \
		$(1)/usr/share/cups/templates/de/
endef

define Package/cups-locale-es/install
	$(INSTALL_DIR) $(1)/usr/share/locale/es
	$(CP) $(PKG_INSTALL_DIR)/usr/share/locale/es/* $(1)/usr/share/locale/es/
	$(INSTALL_DIR) $(1)/usr/share/cups/templates/es
	$(CP) $(PKG_INSTALL_DIR)/usr/share/cups/templates/es/*.tmpl \
		$(1)/usr/share/cups/templates/es/
endef

define Package/cups-locale-fr/install
	$(INSTALL_DIR) $(1)/usr/share/locale/fr
	$(CP) $(PKG_INSTALL_DIR)/usr/share/locale/fr/* $(1)/usr/share/locale/fr/
	$(INSTALL_DIR) $(1)/usr/share/cups/templates/fr
	$(CP) $(PKG_INSTALL_DIR)/usr/share/cups/templates/fr/*.tmpl \
		$(1)/usr/share/cups/templates/fr/
endef

define Package/cups-locale-it/install
	$(INSTALL_DIR) $(1)/usr/share/locale/it
	$(CP) $(PKG_INSTALL_DIR)/usr/share/locale/it/* $(1)/usr/share/locale/it/
endef

define Package/cups-locale-ja/install
	$(INSTALL_DIR) $(1)/usr/share/locale/ja
	$(CP) $(PKG_INSTALL_DIR)/usr/share/locale/ja/* $(1)/usr/share/locale/ja/
	$(INSTALL_DIR) $(1)/usr/share/cups/templates/ja
	$(CP) $(PKG_INSTALL_DIR)/usr/share/cups/templates/ja/*.tmpl \
		$(1)/usr/share/cups/templates/ja/
endef

define Package/cups-locale-ptBR/install
	$(INSTALL_DIR) $(1)/usr/share/locale/pt_BR
	$(CP) $(PKG_INSTALL_DIR)/usr/share/locale/pt_BR/* $(1)/usr/share/locale/pt_BR/
	$(INSTALL_DIR) $(1)/usr/share/cups/templates/pt_BR
	$(CP) $(PKG_INSTALL_DIR)/usr/share/cups/templates/pt_BR/*.tmpl \
		$(1)/usr/share/cups/templates/pt_BR/
endef

define Package/cups-locale-ru/install
	$(INSTALL_DIR) $(1)/usr/share/locale/ru
	$(CP) $(PKG_INSTALL_DIR)/usr/share/locale/ru/* $(1)/usr/share/locale/ru/
	$(INSTALL_DIR) $(1)/usr/share/cups/templates/ru
	$(CP) $(PKG_INSTALL_DIR)/usr/share/cups/templates/ru/*.tmpl \
		$(1)/usr/share/cups/templates/ru/
endef

define Package/cups-locale-zhcn/install
	$(INSTALL_DIR) $(1)/usr/share/locale/zh_CN
	$(CP) $(PKG_INSTALL_DIR)/usr/share/locale/zh_CN/* $(1)/usr/share/locale/zh_CN/
endef



define Build/InstallDev
	$(INSTALL_DIR) $(2)/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/cups-config $(2)/bin/
	$(INSTALL_DIR) $(1)/usr/include
	$(CP) $(PKG_INSTALL_DIR)/usr/include/cups $(1)/usr/include/
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libcups*.so* $(1)/usr/lib/
endef

$(eval $(call BuildPackage,cups))
$(eval $(call BuildPackage,libcups))
$(eval $(call BuildPackage,libcupscgi))
$(eval $(call BuildPackage,libcupsimage))
$(eval $(call BuildPackage,libcupsmime))
$(eval $(call BuildPackage,libcupsppdc))
$(eval $(call BuildPackage,cups-bsd))
$(eval $(call BuildPackage,cups-client))
$(eval $(call BuildPackage,cups-filters))
$(eval $(call BuildPackage,cups-ppdc))
$(eval $(call BuildPackage,cups-locale-ca))
$(eval $(call BuildPackage,cups-locale-cs))
$(eval $(call BuildPackage,cups-locale-de))
$(eval $(call BuildPackage,cups-locale-es))
$(eval $(call BuildPackage,cups-locale-fr))
$(eval $(call BuildPackage,cups-locale-it))
$(eval $(call BuildPackage,cups-locale-ja))
$(eval $(call BuildPackage,cups-locale-ptBR))
$(eval $(call BuildPackage,cups-locale-ru))
$(eval $(call BuildPackage,cups-locale-zhcn))

