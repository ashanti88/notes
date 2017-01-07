**Apache Fullstatus**

[ http://www.linuxspy.info/1886/enable-httpd-fullstatus-to-monitor-apache-status/](http://www.linuxspy.info/1886/enable-httpd-fullstatus-to-monitor-apache-status/ "http://www.linuxspy.info/1886/enable-httpd-fullstatus-to-monitor-apache-status/" )




**﻿watch -n2 '/etc/init.d/httpd fullstatus|egrep -v "^$" | egrep -v "(GET \/server-status|OPTIONS \\*) " '
**

**
**

**See config files for domains**

**
**

**htt****pd -S** - shows all the vhosts/domains, config files and lines they are on




**Restart Apache Service with CPanel**

**
**/scripts/restartsrv_apache




**Check to see what sites are running on 443**




httpd -S 2&gt;&amp;1|grep "port 443 name"|grep -v `hostname`| awk {'print $4'}httpd -S 2&gt;&amp;1|grep "port 443 name"|grep -v `hostname`| awk {'print $4'}




**Apachebuddy**

If this downloads as index.html

wget --trust-server-names apachebuddy.pl 

&lt;&lt;or&gt;&gt;


    wget mysqltuner.pl (This will download as index.html)mv index.html mysqltuner.pl/apachebuddy.plchmod +x mysqltuner.pl/apachebuddy.pl





    **Find all sites that use SSL's**
    /etc/ssl/certs# apache2ctl -S 2>&1|grep "port 443 name"|grep -v `hostname`| awk {'print $4'}



`
`

`**If a site randomy returns 403's and then 200 when curling**`

Add Options +Indexes to the .htaccess file and you will get 200 on curls




[ https://stackoverflow.com/questions/10365520/error-directory-index-forbidden-by-options-directive](https://stackoverflow.com/questions/10365520/error-directory-index-forbidden-by-options-directive "https://stackoverflow.com/questions/10365520/error-directory-index-forbidden-by-options-directive" )




Remove passphrase from SSL site:




cd /etc/ssl/certs

cp bachtrack.com.key bachtrack.com.key.bak

openssl rsa -in bachtrack.com.key -out bachtrack.com.key.new

Put in passphrase when prompted.

cp bachtrack.com.key.new bachtrack.com.key.new

Edit or copy plasmapp.com.conf  back into place.

service httpd start




**For traceenable on Apache (PCI Compliance)**


&lt;?php if (!$VAR-&gt;server-&gt;webserver-&gt;apache-&gt;traceEnableCompliance): ?&gt;
        TraceEnable off

&lt;?php endif; ?&gt;







Apache 2.4









