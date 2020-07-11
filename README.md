# Redmine Image Clipboard Paste

Plugin for redmine which allows pasting image data from the clipboard directly into the comments input field on a new ticket or comment. The image will be given an arbitrary filename and added as an attachment and also inserted into the comment text using Redmine's markup language.

## Features

* Paste images from the clipboard
* Drag and drop image files directly into the input element
* Added to ticket as an attachment
* Added into the comment text field using Redmine's markup language

## Getting the plugin

A copy of the plugin can be downloaded from GitHub: http://github.com/credativUK/redmine_image_clipboard_paste

## Installation

To install the plugin clone the repro from github and migrate the database:

```
cd /path/to/redmine/
git clone git://github.com/credativUK/redmine_image_clipboard_paste.git plugins/redmine_image_clipboard_paste
rake db:migrate_plugins RAILS_ENV=production 
for 2.x 
or this
rake redmine:plugins:migrate RAILS_ENV=development 
for 4.x
```

To uninstall the plugin migrate the database back and remove the plugin:

```
cd /path/to/redmine/
rake db:migrate:plugin NAME=redmine_image_clipboard_paste VERSION=0 RAILS_ENV=production  
for 2.x 
or this
rake redmine:plugins:migrate NAME=redmine_image_clipboard_paste VERSION=0 RAILS_ENV=production
for 4.x
rm -rf plugins/redmine_image_clipboard_paste
```

Further information about plugin installation can be found at: http://www.redmine.org/wiki/redmine/Plugins

## Compatibility

The latest version of this plugin is modified and tested only with Redmine 4.0.x

Browser compatibility will be an issue since it is making use of the FileAPI which is still a working draft at time of writing and each browser has it's own implementation of this.

Paste is only supported by WebKit based browsers.
## UPDATED
# fixed copy paste function for modern firefox and chrome (thanks [@thorin](https://github.com/thorin))
## /UPDATED
Drag and drop should be supported by all modern browsers, tested with Chrome, Firefox and IE.

## License

This plugin is licensed under the GNU GPLv2 license. See LICENSE-file for details.

## Copyright

Copyright (c) 2013 credativ Ltd.

