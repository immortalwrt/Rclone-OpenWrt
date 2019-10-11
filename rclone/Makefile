####
 #  File: /Makefile
 #  Project: rclone
 #  File Created: Friday, 11th October 2019 4:50:49 pm
 #  Author: ElonH[EH](elonhhuang@gmail.com)
 #  License: GNU General Public License v3.0 or later(http://www.gnu.org/licenses/gpl-3.0-standalone.html)
 #  Copyright (C) 2019 [ElonH]
####

include $(TOPDIR)/rules.mk

PKG_NAME:=rclone
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/rclone/rclone.git
PKG_SOURCE_VERSION:=5d3323605080509cf53de5980443c6d02fd50a48
PKG_SOURCE_DATE:=20191011
# PKG_MIRROR_HASH:=d3e4524e9ccaa3fd9dcdd6e00cd8d07a301858f0c8ac42d2984484ebb1cabe03

PKG_LICENSE:=GPLv3
PKG_MAINTAINER:=ElonH <elonhhuang@gmail.com>

PKG_BUILD_DEPENDS:=golang/host
PKG_BUILD_PARALLEL:=1

GO_PKG:=github.com/rclone/rclone
# GO_PKG_SOURCE_ONLY:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/golang/golang-package.mk


define Package/$(PKG_NAME)
	SECTION:=net
	CATEGORY:=Network
	SUBMENU:=File Transfer
	TITLE:=rsync for cloud storage.
	URL:=https://rclone.org
  	DEPENDS:=$(GO_ARCH_DEPENDS) 
endef

define Package/$(PKG_NAME)/description
Rclone ("rsync for cloud storage") is a command line program to sync root/usr/bin and directories to and from different cloud storage providers.
Cloud storage providers:
	1Fichier, Alibaba Cloud (Aliyun) Object Storage System (OSS), Amazon Drive, Amazon S3, 
	Backblaze B2, Box, Ceph, C14, DigitalOcean Spaces, Dreamhost, Dropbox, FTP, 
	Google Cloud Storage, Google Drive, Google Photos, HTTP, Hubic, Jottacloud, 
	IBM COS S3, Koofr, Memset Memstore, Mega, Microsoft Azure Blob Storage, 
	Microsoft OneDrive, Minio, Nextcloud, OVH, OpenDrive, Openstack Swift, 
	Oracle Cloud Storage, ownCloud, pCloud, premiumize.me, put.io, QingStor, 
	Rackspace Cloud root/usr/bin, rsync.net, Scaleway, SFTP, Wasabi, WebDAV, 
	Yandex Disk, The local root/usr/binystem.
endef

$(eval $(call GoSrcPackage,$(PKG_NAME)))
$(eval $(call BuildPackage,$(PKG_NAME)))
