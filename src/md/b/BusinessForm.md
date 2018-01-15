---
slug: business-form
title: 帳票
layout: page.jade
---

## articles

- [そろそろ真面目に、HTMLで帳票を描く話をしようか \- Qiita](http://qiita.com/cognitom/items/d39d5f19054c8c8fd592)
- [ゲームミュージックと生存確認をかねた画期的な: svgの印刷結果をクロスブラウザ化する](http://defghi1977-onblog.blogspot.jp/2013/04/svg.html)


## Services

### [帳票開発を、もっと簡単に「Docurain\-ドキュレイン\-」](http://site.docurain.jp/)
- [私「Excel通知表やめたいんですけど…」校長「おう、いいよ。」私「えっ？」 \- パパ教員の戯れ言日記](http://blog.edunote.jp/entry/2018/01/13/155921)


## [fraserxu/electron\-pdf](https://github.com/fraserxu/electron-pdf)
📄 A command line tool to generate PDF from URL, HTML or Markdown files.

- [PDF Generation On The Web · Fraser Xu](https://fraserxu.me/2015/08/20/pdf-generation-on-the-web/)


## [wkhtmltopdf](https://wkhtmltopdf.org/)
open source (LGPLv3) command line tools to render HTML into PDF and various image formats using the Qt WebKit rendering engine.

- [Single page & full size rendering · Issue \#1782 · wkhtmltopdf/wkhtmltopdf](https://github.com/wkhtmltopdf/wkhtmltopdf/issues/1782)
  - `--disable-smart-shrinking`
  - `--zoom 1.33` is a good fit for the 96dpi Windows default setting.
- [wkhtmltopdf: ハガキサイズのPDFを余白なしで作る \- Toolbox](http://d.hatena.ne.jp/m0t0m0t0/20151114/1447488492)
  - `-T 0 -L 0 -B 0 -R 0 --disable-smart-shrinking`


## Headless Chrome

- [ヘッドレス Chrome ことはじめ  \|  Web  \|  Google Developers](https://developers.google.com/web/updates/2017/04/headless-chrome?hl=ja)

[adieuadieu/serverless\-chrome](https://github.com/adieuadieu/serverless-chrome)
: Run headless Chrome/Chromium on AWS Lambda \(maybe Azure, & GCP later\)
- [How to get headless Chrome running on AWS Lambda – Marco Lüthy – Medium](https://medium.com/@marco.luethy/running-headless-chrome-on-aws-lambda-fa82ad33a9eb)

[westy92/html\-pdf\-chrome](https://github.com/westy92/html-pdf-chrome)
: HTML to PDF converter via Chrome/Chromium

[GoogleChrome/puppeteer](https://github.com/GoogleChrome/puppeteer)
: Headless Chrome Node API
- [Puppeteer API Document](https://github.com/GoogleChrome/puppeteer/blob/master/docs/api.md)
- [\-\-headless時代の本命？ Chrome を Node\.jsから操作するライブラリ puppeteer について \- Qiita](http://qiita.com/Quramy/items/26058e83e898ec2ec078)
- [Send POST request to a page and take screenshot · Issue \#669 · GoogleChrome/puppeteer](https://github.com/GoogleChrome/puppeteer/issues/669)  
  POSTリクエストを送るには Request Interception を使う。 overrides.headers で Content-Type も指定しないと Express では受け付けてもらえないので注意。
```bash
$ curl http://www.google.com -d 'a=b&c=d'
```
```js
await page.setRequestInterceptionEnabled(true);
page.on('request', request => {
  const overrides = {};
  if (request.url === 'http://www.google.com') {
    overrides.method = 'POST';
    overrides.headers = {
      'Content-Type': 'application/x-www-form-urlencoded; charset=UTF-8',
    };
    overrides.postData = 'a=b&c=d';
  }
  request.continue(overrides);
});
await page.goto('http://www.google.com');
```


## Apache PDFBox
[Apache PDFBox \| A Java PDF Library](https://pdfbox.apache.org/)


## PDFtk
[PDFtk \- The PDF Toolkit](https://www.pdflabs.com/tools/pdftk-the-pdf-toolkit/)
