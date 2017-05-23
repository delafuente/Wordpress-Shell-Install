Wordpress-Shell-Install
=======================

Copyright 2013 Oliver M. Grech and other contributors
Fork by Lucas de la Fuente
http://www.olivermgrech.com/wordpress-command-line-installer/

Usage
=====

1) First, you may change some variables inside the script, that is intended to be used within the same server installation for many Wordpress sites.

1.1 Change the value of mysqlhost if you want something different than localhost
1.2 Change the value of dbAdMinUser if you want something different than root
1.3 Change the dbAdminPass
1.4 Change the value of wpemail. I left this fixed for all the installations, but you can easily require another parameter and set it as the current install e-mail
1.5 Change the wp db prefix ( here set as ws_ ) under the line that reads sed -e "s/'wp_'/'ws_'/" $installPath/wp-config.php

2. If you want to automatically download some plugins, you can use the block under the Auto-download plugins comment, one per plugin

3. You can call the script with some parameters ( after making wpinstall.sh executable by chmod u+x wpinstall.sh ) this way:

./wpinstall.sh db_name db_user dbpass shell_user "My Site Title" "www.mysite.com" "/home/user/public_html"

3.1 Parameters explanation:

 [1] db_name: new database name
 [2] db_user: DB user, and wordpress admin
 [3] dbpass: new database user password
 [4] shell_user: shell user to chown files ( username or www-data, will chown all files as shell_user:shell_user )
 [5] site title: Site title, between quotes
 [6] site url: without http://, like www.example.com
 [7] install path: like "/home/user/public_html", quoted if some space in between

4. You can also call this file within other script, so you can automate the installation of wordpress sites.


5. This Project is under the MIT License

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
