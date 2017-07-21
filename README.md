### Quick install guide


for the FQDN and correty identifing from postfix 
--> /etc/hosts & /etc/mailname
<pre>x.x.x.x  your.domain.com</pre>

--> /etc/hostname
<pre>your</pre>

hostname -f
<pre>your.domain.com</pre>

uname -n
<pre>your</pre>

<pre>
apt-get update && apt-get install build-essential
apt-get install mailman
</pre>

this will install apache2 by default

<pre>apt-get install postfix</pre>

mode: internet site   
FQDN must show to server ip

create initial list for mailman
<pre>newlist mailman</pre>

create your first mailinlist
<pre>newlist <list_name>@<my.domain1.com></pre>

Type <pre>/usr/lib/mailman/bin/genaliases</pre>, which will update /var/lib/mailman/data/aliases and var/lib/mailman/data/virtual-mailman accordingly. Now restart mailman to take our new settings

(re)start mailman <pre>/etc/init.d/mailman</pre>

copy the apache.conf from /etc/mailman/ to /etc/apach2/sites-enabled

comment the line ScriptAlias from mailman/apache.conf

edit the mm_cfg.py in /etc/mailman  and customize it
MTA ='postfix'

Postfix notices:
if you edit /etc/aliases or virtual_* files than generate ne alias with and restart postfix
<pre>newaliases</pre>   


#info -> see example configs from prod server



[Aysad Kozanoglu]
