This is a fork with bugfix made on Mon Dec 17 13:50:34 CET 2018 in window.js:

```
   parseDeclaration: function(elementElement) {
        var template = this.fetchTemplate(elementElement);
        if (template) {
   +      try {
              var root = this.shadowFromTemplate(template);
              this.shadowRoots[elementElement.name] = root;
   +      } catch (e) {
   +          console.dir(e)
   +      }
        }
      },
```

Seems to be a bug in polymer, 
I don't really have the time to properly fix this,  so download the build [here](build.zip) to load the bugfixed extension manually.

---

[![Code Climate](https://codeclimate.com/github/yoichiro/chromeos-filesystem-webdav/badges/gpa.svg)](https://codeclimate.com/github/yoichiro/chromeos-filesystem-webdav)

# WebDAV File System

WebDAV File System provides you an ability to access to your WebDAV storage directly from the Files app.

<a target="_blank" href="https://chrome.google.com/webstore/detail/webdav-file-system/hmckflbfniicjijmdoffagjkpnjgbieh">
  Go to WebDAV File System page on Chrome WebStore
</a>

<img src="https://raw.githubusercontent.com/yoichiro/chromeos-filesystem-webdav/master/docs/screenshot.png">

## How to build

```
$ git clone https://github.com/yoichiro/chromeos-filesystem-webdav.git
$ cd chromeos-filesystem-webdav
$ npm install
$ grunt
```

## Dependent libraries

* [Polymer](https://www.polymer-project.org/)
* [jQuery](http://jquery.com/)

## License

All files are licensed under the BSD license. See the LICENSE file for details.
All original source code is Copyright 2015 Yoichiro Tanaka.
