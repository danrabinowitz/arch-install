install/root/install-secrets.tar.gpg: $(shell find secret)
	mkdir -p install/root
	(cd secret; tar cf - . | gpg -c -) > install/root/install-secrets.tar.gpg
