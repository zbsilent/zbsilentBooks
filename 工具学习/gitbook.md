# GitBook命令

[![](https://img.shields.io/badge/GitBook-zbsilent-brightgreen)](Https://github.com/zbsilent)

---

###### 查看版本

```shell
$ gitbook ls-remote
$ npm install babel-cli babel-preset-es2015
$ cd 4.0.0-alpha.4/node_modules/gitbook-plugin-livereload
$ npm install
```

###### 异常解决方案

```sh
$ gitbook serve --log=debug
Error: ENOENT: no such file or directory, open '/Users/zbsilent/.gitbook/versions/4.0.0-alpha.2/node_modules/gitbook-plugin-livereload/_assets/plugin.js'
```

```shell
$ /Users/zbsilent/.gitbook/versions/4.0.0-alpha.2/lib/output/website/copyPluginAssets.js
```

```js
/**
 * Copy assets from a plugin
 *
 * @param {Plugin}
 * @return {Promise}
 */
function copyAssets(output, plugin) {
    var logger = output.getLogger();
    var pluginRoot = plugin.getPath();
    var options = output.getOptions();

    var outputRoot = options.get('root');
    var prefix = options.get('prefix');

    var assetFolder = path.join(pluginRoot, ASSET_FOLDER, prefix);
    var assetOutputFolder = path.join(outputRoot, 'gitbook', plugin.getName());

    if (!fs.existsSync(assetFolder)) {
        return Promise();
    }

    logger.debug.ln('copy assets from plugin', assetFolder);
    return fs.copyDir(assetFolder, assetOutputFolder, {
        deleteFirst: false,
        overwrite: true,
        confirm: false #这里true改成false
    });
}

```
###### 创建book.json配置文件
```json
{
  "title" : "itcode",
  "description" : "记录自己日常学习总结",
  "author" : "wangmaolin",
  "generator": "site",
  "language" : "zh-hans",
  "gitbook" : "3.2.3",
  "links" : {
    "sidebar" : {
      "Home" : "http://itcode.wiki"
    }
  },
  "structure": {
    "readme": "README.md",
    "summary":"SUMMARY.md",
    "glossary":"GLOSSARY.md"
  },
  "styles": {
   "website": "styles/website.css",
   "ebook": "styles/ebook.css",
   "pdf": "styles/pdf.css",
   "mobi": "styles/mobi.css",
   "epub": "styles/epub.css"
  },
  "plugins": [
    "-lunr",
    "-search",
    "search-pro",
    "toggle-chapters",
    "splitter",
    "donate",
    "github",
    "github-buttons",
    "edit-link",
    "advanced-emoji",
    "tbfed-pagefooter",
    "simple-page-toc",
    "baidu",
    "github-buttons",
    "changyan",
    "anchors",
    "expandable-chapters-small",
    "favicon",
    "anchor-navigation-ex",
    "sharing-plus",
    "edit-link-plus",
    "sitemap-general"
  ],
  "pluginsConfig": {
    "sitemap-general": {
      "prefix": "http://itcode.wiki"
    },
    "edit-link-plus": {

             "base": {
               "snowdreams1006.github.io":"https://github.com/snowdreams1006/gitbook-plugin-edit-link-plus/edit/master/docs",
              "snowdreams1006.gitlab.io":"https://gitlab.com/snowdreams1006/gitbook-plugin-edit-link-plus/edit/master/docs",
              "snowdreams1006.gitee.io":"https://gitee.com/snowdreams1006/gitbook-plugin-edit-link-plus/edit/master/docs",

              "type": [
                    "string",
                    "object"
                  ],
                  "title": "Base for the edit redirection",
                  "required": true
                },
                "defaultBase": {
                  "testxxxx": "https://github.com/snowdreams1006/gitbook-plugin-edit-link-plus/edit/master/docs",
                  "type": "string",
                  "title": "Default base for the edit redirection",
                  "required": false
                },
                "label": {
                  "type": [
                    "string",
                    "object"
                  ],
                  "title": "Label for the edit button",
                  "default": "Edit This Page",
                  "required": false
                }
      },
    "github-buttons": {
        "buttons": [{
            "user": "Blankj",
            "repo": "glory",
            "type": "star",
            "size": "small",
            "count": true
            }
        ]
    },
    "changyan": {
      "appid": "cytowLiqM",
      "conf": "the conf in the code generate by changyan"
    },
    "github": {
      "url": "https://gitee.com/wmlhub/gitbook/tree/master"
    },
    "search-pro": {
      "cutWordLib": "nodejieba",
      "defineWord": ["gitbook-use"]
    },
    "simple-page-toc": {
      "maxDepth": 3,
      "skipFirstH1": false
    },
    "sharing": {
        "douban": true,
        "facebook": true,
        "google": true,
        "hatenaBookmark": true,
        "instapaper": true,
        "line": true,
        "linkedin": true,
        "messenger": true,
        "pocket": true,
        "qq": true,
        "qzone": true,
        "stumbleupon": true,
        "twitter": true,
        "viber": true,
        "vk": true,
        "weibo": true,
        "whatsapp": true,
        "wechat":true,
        "all": [
            "google", "facebook", "weibo", "twitter",
            "qq", "qzone", "linkedin", "pocket","wechat"
        ]
    },

    "tbfed-pagefooter": {
      "copyright":"Copyright &copy wml 2018",
      "modify_label": "该文件修订时间：",
      "modify_format": "YYYY-MM-DD HH:mm:ss"
    },
    "anchor-navigation-ex": {
        "showLevel": false
    },
    "baidu": {
      "token" : "084b900a1e26f6bae60e09d18e3aa455"
    },
    "sitemap": {
      "hostname": "https://wmlhub.gitee.io/gitbook/"
    },
    "favicon":{
        "shortcut": "./source/images/favicon.jpg",
        "bookmark": "./source/images/favicon.jpg",
        "appleTouch": "./source/images/apple-touch-icon.jpg",
        "appleTouchMore": {
            "120x120": "./source/images/apple-touch-icon.jpg",
            "180x180": "./source/images/apple-touch-icon.jpg"
        }
    },
    "donate": {
      "wechat": "",
      "alipay": "",
      "title": "",
      "button": "赏",
      "alipayText": "支付宝打赏",
      "wechatText": "微信打赏"
    },

    "edit-link": {
      "base": "https://gitee.com/wmlhub/gitbook/tree/master",
      "label": "Edit This Page"
    }

  },
  "pdf": {
    "pageNumbers": true,
    "fontFamily": "Arial",
    "fontSize": 12,
    "paperSize": "a4",
    "margin": {
        "right": 62,
        "left": 62,
        "top": 56,
        "bottom": 56
    }
  }
}
```
###### 下载依赖
```shell
gitbook install
```
