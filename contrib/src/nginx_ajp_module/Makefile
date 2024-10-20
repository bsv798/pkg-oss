# nginx_ajp_module

include $(dir $(abspath $(lastword $(MAKEFILE_LIST))))/version
NGINX_AJP_MODULE_GITURL := $(GITHUB)/msva/nginx_ajp_module.git

PKGS += nginx_ajp_module

$(TARBALLS)/nginx_ajp_module-$(NGINX_AJP_MODULE_GITHASH).tar.xz:
	$(call download_git,$(NGINX_AJP_MODULE_GITURL),,$(NGINX_AJP_MODULE_GITHASH))

.sum-nginx_ajp_module: nginx_ajp_module-$(NGINX_AJP_MODULE_GITHASH).tar.xz
	$(call check_githash,$(NGINX_AJP_MODULE_GITHASH))
	touch $@

nginx_ajp_module: nginx_ajp_module-$(NGINX_AJP_MODULE_GITHASH).tar.xz .sum-nginx_ajp_module
	$(UNPACK)
	$(MOVE)

.nginx_ajp_module: nginx_ajp_module
	touch $@
