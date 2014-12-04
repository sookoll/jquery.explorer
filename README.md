jquery.explorer
===============

jquery.explorer is a configurable, AJAX file browser plugin for jQuery.

Basic idea from unmaintained jQuery File Tree (v1.01) (12 April 2008) from ABeautifulSite.net:  
[http://www.abeautifulsite.net/jquery-file-tree/](http://www.abeautifulsite.net/jquery-file-tree/)

## Usage

    $('#explorer').explorer();

or

    $('#explorer').explorer({
      root : '../content/',
      script : 'server/explore.php',
      folderEvent : 'click',
      onafterexplore : function() {
          // do something after tree is rendered
      },
      ondeleteclick : function(path) {
          // do something if delete button is clicked, e.g. delete item
      }
    }, function(file) {
        // do something with this file
    });

## Data source

Data source can be plain json file or script that return formatted data as json string. No hard-coded elements and classnames in server side.

### Example:

    [
      {"id":"5","path":"images\/","type":"directory","name":"images"},
      {"id":"9","path":"uudised\/","type":"directory","name":"uudised"},
      {"id":"11","path":"viud\/","type":"directory","name":"viud"},
      {"id":"15","path":"405.md","type":"file","ext":"ext_md","name":"405.md"},
      {"id":"16","path":"footer1.md","type":"file","ext":"ext_md","name":"footer1.md"},
      {"id":"17","path":"galerii.md","type":"file","ext":"ext_md","name":"galerii.md"}
    ]


## Licensing

This plugin is licensed under the MIT License.

## Special thanks

A special thanks goes out to [FAMFAMFAM](http://www.famfamfam.com/) for their excellent Silk Icon Set.
