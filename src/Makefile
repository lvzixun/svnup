# to build svnup, comment out either below
# for systems which have libmd for md5, choose former
# for other systems which have openssl, choose latter
# MDFLAGS= -lmd -lssl
MDFLAGS= -lssl -lcrypto -DOPENSSL

svnup: svnup.c
	$(CC) -g -Wall -o $@ $(CFLAGS) $? $(MDFLAGS)   -L/usr/local/opt/openssl/lib -I/usr/local/opt/openssl/include
	cp svnup.conf /usr/local/etc/svnup.conf

clean:
	rm -f svnup
