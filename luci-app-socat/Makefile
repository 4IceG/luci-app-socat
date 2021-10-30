include $(TOPDIR)/rules.mk
	
LUCI_TITLE:=Web UI for socat
LUCI_DEPENDS:=+socat +luci-compat
PKG_VERSION:=1.1-2021-10-30
PKG_LICENSE:=GPLv3

define Package/luci-app-socat/postinst
#!/bin/sh
rm -rf /tmp/luci-indexcache
rm -rf /tmp/luci-modulecache/
/sbin/set_at_port.sh
exit 0
endef
	
include $(TOPDIR)/feeds/luci/luci.mk
	
# call BuildPackage - OpenWrt buildroot signature
