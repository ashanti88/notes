**nginx configtest**

nginx -t




**check rewrites in nginx.conf**

grep -i rewrite /etc/nginx/conf.d/tinygreenpc.com.conf | wc -l




**Too Many Open Files Error And Solution**

[ http://www.cyberciti.biz/faq/linux-unix-nginx-too-many-open-files/](http://www.cyberciti.biz/faq/linux-unix-nginx-too-many-open-files/ "http://www.cyberciti.biz/faq/linux-unix-nginx-too-many-open-files/" )




**Check to see what sites are running on 443**




grep 443 /etc/nginx/conf.d/*

_**User Level Authentication in nginx**_


[](http://www.howtoforge.com/basic-http-authentication-with-nginx "http://www.howtoforge.com/basic-http-authentication-with-nginx" )<http://www.howtoforge.com/basic-http-authentication-with-nginx>







&gt;&gt;&gt;&gt;NEEDS SORTING&lt;&lt;&lt;&lt;




To set the real IP showing in the nginx access logs when behind a webcel add the following to /etc/nginx/nginx.conf




 set_real_ip_from 81.201.130.10;

    real_ip_header X-Forwarded-For;
