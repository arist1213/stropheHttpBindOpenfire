This is a simple demo to connect xmpp using strophe and bosh.

Include simple three steps.

1. First make sure you setup your xmpp server correct.
	#1 enable xmpp "HTTP BIND" option
	#2 open the 7070 port in your server, iptables for linux and restart.
2. Set the apache or nginx to proxy or rewrite to your xmppserver.com:7070 
	#1 add this to your apache httpd.conf
	# this will let xmlhttprequest to have cros ability.
	<VirturalHost *>
		AddDefaultCharset UTF-8
		RewriteEngine On
		RewriteRule ^/http-bind/ http://localhost:7070 [P]
	</VituralHost>
	#2 Restart your apache
3. open index.html and enjoy.
