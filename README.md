<Directory /usr/share/phpMyAdmin/>
  AddDefaultCharset UTF-8

  <IfModule mod_authz_core.c>
    # Apache 2.4
    <RequireAny>
#       Require ip 127.0.0.1
#       Require ip ::1
       Require all granted
    </RequireAny>
  </IfModule>
  <IfModule !mod_authz_core.c>
    # Apache 2.2
    Order Deny,Allow
    Deny from All
    Allow from 127.0.0.1
    Allow from ::1
  </IfModule>
</Directory>
