files_dir := $(dir $(realpath $(firstword $(MAKEFILE_LIST))))

install/root/install-secrets.tar.gpg: secret/home/djr/.ssh/id_ed25519 $(shell find secret)
	mkdir -p "${files_dir}install/root"
	(cd secret; tar cf - . | gpg -c -) > install/root/install-secrets.tar.gpg


secret/home/djr/.ssh/id_ed25519:
	$(shell [ -f "${files_dir}secret/home/djr/.ssh/id_ed25519" ] && (echo "secret/home/djr/.ssh/id_ed25519 exists. Refusing to overwrite"; exit 99) )
	ssh-keygen -o -a 100 -t ed25519 -f "${files_dir}secret/home/djr/.ssh/id_ed25519"
