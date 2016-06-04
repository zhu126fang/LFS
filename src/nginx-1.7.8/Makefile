
default:	build

clean:
	rm -rf Makefile objs

build:
	$(MAKE) -f objs/Makefile
	$(MAKE) -f objs/Makefile manpage

install:
	$(MAKE) -f objs/Makefile install

upgrade:
	/opt/nginx-1.7.8/sbin/nginx -t

	kill -USR2 `cat /opt/nginx-1.7.8/logs/nginx.pid`
	sleep 1
	test -f /opt/nginx-1.7.8/logs/nginx.pid.oldbin

	kill -QUIT `cat /opt/nginx-1.7.8/logs/nginx.pid.oldbin`
