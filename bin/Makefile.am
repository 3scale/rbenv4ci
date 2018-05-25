rbenv4ci_templateddir = $(bindir)
rbenv4ci_templated_SCRIPTS = bundle_install_gemfiles bundle_install_rubies ruby_versions

install-exec-am: install-rbenv4ci_templatedSCRIPTS
	(FILES='$(dockerfile_utils_templated_SCRIPTS)'; \
	for file in $${FILES}; do \
	sed -e "s%@SCRIPT_PREFIX_PATH@%$(prefix)%g" \
	    -e "s%@SCRIPT_BIN_PATH@%$(bindir)%g" \
	    -e "s%@SCRIPT_LIB_PATH@%$(libdir)/rbenv4ci%g" \
	    -i "$(DESTDIR)$(rbenv4ci_templateddir)"/$${file}; \
	done)
