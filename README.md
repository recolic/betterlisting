# BetterListing

## What is BetterListing?

BetterListing enhances and themes the default NGINX directory listings __WITHOUT__ the need for the Fancy Index module. As BetterListing uses Javascript and jQuery, no compiling or reinstalling is required. Who can be bothered with that, anyway?  

__Try it out:__ [devcoster.com/betterlisting/demo](https://www.devcoster.com/betterlisting/demo)  

BetterListing was tested on NGINX 1.10.0

## Features:

- A modern theme that styles the default directory listing.
- Folder and file icons for every item in the directory.
- Search functionality that searches as you type. 
- Easily add support for new MIME types when needed.
- Released under GNU General Public License v3 (GPL-3).
- Supports the following file types
```
.7z, .avi, .bin, .c++, .c, .css, .deb, .doc, .docx, .gif, .gzip, .html, .ico, .iso, .java, .jpeg, .jpg, .js, .mp3, .mp4, .msg, .ogg, .pdf, .php, .png, .ppt, .pptx, .psd, .py, .rar, .sql, .swf, .tiff, .torrent, .txt, .wav, .wmv, .xls, .xlsx, .zip
```

## Requirements:

- NGINX (Fancy Index module not required)
- Write access to `/etc/nginx/sites-enabled/default`
 
## Installation:


## Acknowledgements:

- [Apaxy](https://github.com/AdamWhitcroft/Apaxy) created by [AdamWhitcroft](http://adamwhitcroft.com) for the idea. If it was available for NGINX, I would have used that.
- BetterListing makes use of [Faenza icons](http://tiheum.deviantart.com/art/Faenza-Icons-173323228) by [tiheum](http://tiheum.deviantart.com/).