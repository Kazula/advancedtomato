include ../common.mak

all:

install:
	install -d $(INSTALLDIR)/sbin
	install -d $(INSTALLDIR)/usr/sbin
	install -d $(INSTALLDIR)/lib

ifeq ($(TCONFIG_USB),y)
# Optware perl symlink
	install -d $(INSTALLDIR)/usr/bin
	ln -sf /opt/bin/perl $(INSTALLDIR)/usr/bin/perl

ifeq ($(CONFIG_LINUX26),y)
#3G modem switch script
	install -m 0700 switch3g $(INSTALLDIR)/usr/sbin
#4G modem switch script
	install -m 0700 switch4g $(INSTALLDIR)/usr/sbin
endif
endif

#MultiWAN watchdog script
	install -m 0700 watchdog $(INSTALLDIR)/usr/sbin

ifeq ($(TCONFIG_DNSCRYPT),y)
	install -m 0700 ntp2ip $(INSTALLDIR)/usr/sbin
endif

#TomatoAnon project
	install -m 0700 tomatoanon $(INSTALLDIR)/usr/sbin

#Adblock
	install -m 0700 adblock $(INSTALLDIR)/usr/sbin

#TTB project
	install -m 0700 ttb $(INSTALLDIR)/usr/sbin

#Ethernet state report
	install -m 0700 ethstate $(INSTALLDIR)/usr/sbin

#stealthMode
	install -m 0700 stealthMode $(INSTALLDIR)/usr/sbin

#MOTD
	install -m 0700 mymotd $(INSTALLDIR)/usr/sbin

#Web Monitor Backup Script
	install -m 0700 webmon_bkp $(INSTALLDIR)/usr/sbin

#optware/entware install script
ifeq ($(TCONFIG_USB),y)
	install -m 0700 optware-install.sh $(INSTALLDIR)/usr/sbin
	install -m 0700 entware-install.sh $(INSTALLDIR)/usr/sbin
endif

ifeq ($(TCONFIG_OPENVPN),y)
#openvpn selectable routing
	install -m 0700 vpnrouting $(INSTALLDIR)/usr/sbin
endif

# cron helper
	install -m 0700 cru $(INSTALLDIR)/usr/sbin

# system info
	install -m 0700 sysinfo $(INSTALLDIR)/usr/sbin

# nas starter # AB multiSSID
	install -m 0700 nas.sh $(INSTALLDIR)/usr/sbin

clean:
