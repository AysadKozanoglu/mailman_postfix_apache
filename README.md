### Quick install guide
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

copy the apache.conf from /etc/mailman/ to /etc/apach2/sites-enabled

comment the line ScriptAlias from mailman/apache.conf

edit the mm_cfg.py in /etc/mailman  and customize it
MTA ='postfix'

Postfix notices:
if you edit /etc/aliases or virtual_* files than generate ne alias with and restart postfix
<pre>newaliases</pre>   


## info see example configs from prod server



[Aysad Kozanoglu]
