# BetterListing

## What is BetterListing?

BetterListing enhances and themes the default NGINX directory listings __WITHOUT__ the need for the Fancy Index module. As BetterListing uses Javascript and jQuery, no compiling or reinstalling is required. Who can be bothered with that, anyway?  
  
__Try it out:__ [devcoster.com/betterlisting/demo](https://www.devcoster.com/betterlisting/demo)

## Features:

- A modern theme that styles the default directory listing.
- Folder and file icons for every item in the directory.
- Search functionality that searches as you type. 
- Easily add support for new MIME types when needed.
- Released under GNU General Public License v3 (GPL-3).
- Supports the following file types:
`
.7z, .avi, .bin, .c++, .c, .css, .deb, .doc, .docx, .gif, .gzip, .html, .ico, .iso, .java, .jpeg, .jpg, .js, .mp3, .mp4, .msg, .ogg, .pdf, .php, .png, .ppt, .pptx, .psd, .py, .rar, .sql, .swf, .tiff, .torrent, .txt, .wav, .wmv, .xls, .xlsx, .zip
`

## Requirements:

- NGINX (Tested on 1.10.0)
- Write access to `/etc/nginx/sites-enabled/default`

## Installation:

1.  Unzip BetterListing to your NGINX webroot so you end up with the following structure:
``` 
wwwroot/
	|- betterlisting/
	|- index.html
    |- robots.txt
    |- downloads/
    |- etc.
```
2.  Open `top.html` found in `/betterlisting/` and input your sites name, URL and Google Analytics code if required. The comments near the top of the file will tell you where to do this. 
3.  Open your NGINX site configuration file found at `/etc/nginx/sites-enabled/default`.
4.  For every existing root directory you want to add BetterListing to, add these lines in the correct location block:
```
add_before_body /betterlisting/top.html;
add_after_body /betterlisting/bot.html;
audoindex_exact_size off;
autoindex_localtime on;
```
The following example shows what your configuration might look like if you wanted to use BetterListing on `yourdomain.com/downloads`.
```
server {
		server_name: yourdomain.com;
		root /var/www/html;
    
    	location /downloads {
	    	add_before_body /betterlisting/top.html;
	    	add_after_body /betterlisting/bot.html;
	    	autoindex on;
	    	autoindex_localtime on;
	    	autoindex_exact_size off;
		    try files $uri $uri/ =404;
		}
}
```
## Acknowledgements:

- [Apaxy](https://github.com/AdamWhitcroft/Apaxy) created by [AdamWhitcroft](http://adamwhitcroft.com) for the idea. If it was available for NGINX, I would have used that.
- BetterListing makes use of [Faenza icons](http://tiheum.deviantart.com/art/Faenza-Icons-173323228) by [tiheum](http://tiheum.deviantart.com/).