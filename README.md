# script-auto-runner

## 1. 検索順位表示

```js
(() => {
  document.querySelector("body").insertAdjacentHTML(
    "afterend",
    `
      <style>
        body {
          counter-reset: result !important;
        }
        h3.LC20lb:before {
            content: counter(result) ". " !important;
            counter-increment: result !important;
            display: inline-block;
            background: #fbe4c2;
            margin-right: 1em;
        }
      </style>
    `
  );
})();
```

### domain
- `www.google.com`

## 2. Contentful Auto Login

```js
(() => {
  if (location.href == "https://www.contentful.com/") {
    location.href = "https://be.contentful.com/login";
  }
  if (location.href == "https://be.contentful.com/login") {
    document
      .querySelector(
        "body > div.row > div > div.account__box.box > div > div.row.row--lessgutter > div:nth-child(1) > a"
      )
      .click();
  }
})();
```

### domain
- `be.contentful.com, www.contentful.com`

## 3. ホテル名コピー in GoogleTravel

```js
(() => {
  const textarea = document.createElement("textarea");
  textarea.textContent = [
    ...document.querySelectorAll(
      "#yDmH0d > c-wiz.zQTmif.SSPGKf > div > div.lteUWc > div > c-wiz > div > div.OEKf8b > div.gpcwnc > div > main > div > c-wiz > div.iQJyJ.oJeWuf > div.l5cSPd > c-wiz > div > div > div > div.kCsInf.ZJqrAd.qiy8jf > div > div.idWj5c.Mq5k0e.CiuVaf > div.lPksYb"
    ),
  ]
    .map((e) => e.querySelector("div.gacGFb > h2").innerText)
    .join("\n");

  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  document.body.removeChild(textarea);
})();
```

### domain
- `www.google.com`

## 4. ホテル名コピー in Precious

```js
(() => {
  const textarea = document.createElement("textarea");
  textarea.textContent = [
    ...document.querySelectorAll(
      "#yDmH0d > c-wiz.zQTmif.SSPGKf > div > div.lteUWc > div > c-wiz > div > div.OEKf8b > div.gpcwnc > div > main > div > c-wiz > div.iQJyJ.oJeWuf > div.l5cSPd > c-wiz > div > div > div > div.kCsInf.ZJqrAd.qiy8jf > div > div.idWj5c.Mq5k0e.CiuVaf > div.lPksYb"
    ),
  ]
    .map((e) => e.querySelector("div.gacGFb > h2").innerText)
    .join("\n");

  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  document.body.removeChild(textarea);
})();
```

### domain
- `precious.jp`

## 5. 楽天GORA コースIDコピー in ゴルフラボ

```js
(() => {
  const textarea = document.createElement("textarea");
  textarea.textContent = [
    ...document.querySelectorAll(
      "#main-contents > section > article > div.cps-post-main-box > div > div > a"
    ),
  ]
    .map((e) => e.href.match(/.*c_id%2F(\d+).*/)[1])
    .join("\n");

  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  document.body.removeChild(textarea);
})();
```

### domain
- `www.golflab.jp`

## 6. ホテルNoコピー in 楽天トラベル キーワード検索

```js
(() => {
  const textarea = document.createElement("textarea");
  textarea.textContent = document
    .querySelector("#HotelNos")
    .value.split(",")
    .join("\n");

  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  document.body.removeChild(textarea);
})();
```

### domain
- `kw.travel.rakuten.co.jp`

## 7. ホテル名コピー in TravelBook

```js
(() => {
  const textarea = document.createElement("textarea");
  textarea.textContent = [
    ...document.querySelectorAll(
      "body > div.ptl > div > div > article > div.article.article__container > div.hotel-item-list.mbl.mtm > ul > li > div > a > div.topic-hotel-item__content.mbs > h3"
    ),
  ]
    .map((e) => e.innerText)
    .join("\n");

  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  document.body.removeChild(textarea);
})();
```

### domain
- `www.travelbook.co.jp`

## 8. 楽天GORA コースIDコピー in kiki golfer

```js
(() => {
  const textarea = document.createElement("textarea");
  textarea.textContent = [
    ...document.querySelectorAll(
      "#article > div.post_content.clearfix p a"
    ),
  ]
    .filter((e) => e.innerText.includes("楽天GORA"))
    .map((e) => e.href.match(/.*c_id%2F(\d+).*/)?.[1])
    .join("\n");

  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  document.body.removeChild(textarea);
})();
```

### domain
- `kiki-golfer.com`

## 9. ホテルNoコピー in journal4

```js
(() => {
  const textarea = document.createElement("textarea");
  textarea.textContent = [
    ...document.querySelectorAll("#nocopy > div.entry-content > div > a"),
  ]
    .filter((e) => e.href.match(/^https:\/\/hb.afl.rakuten.co.jp/))
    .map(e=>e.href.match(/HOTEL%2F(\d+)/)[1])
    .join("\n");

  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  document.body.removeChild(textarea);
})();
```

### domain
- `journal4.net`

## 10. ホテルNoコピー in travel gpoint

```js
(() => {
  const textarea = document.createElement("textarea");
  textarea.textContent = [
    ...document.querySelectorAll(
      "#gpointbody_qg > main > article > div.main-content > section.ranking-area > div > div.hotel-info > p.btn-lowest > a"
    ),
  ]
    .filter((e) => e.href.match(/^https:\/\/hb.afl.rakuten.co.jp/))
    .map((e) => e.href.match(/plan%2F(\d+)/)[1])
    .join("\n");

  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  document.body.removeChild(textarea);
})();
```

### domain
- `travel.gpoint.co.jp`

## 11. ホテルNoコピー in IiSENTAKU

```js
(() => {
  const textarea = document.createElement("textarea");
  textarea.textContent = [...document.querySelectorAll("#center01 > div a")]
    .filter((e) => e.href.includes("rakuten"))
    .map((e) => e.href.match(/%2F(\d+)\.html$/)[1])
    .join("\n");

  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  document.body.removeChild(textarea);
})();
```

### domain
- `www.be2to.com`

## 12. ホテル名コピー in ikyu

```js
(() => {
  const textarea = document.createElement("textarea");
  textarea.textContent = [
    ...document.querySelectorAll(
      "#ga-article_plugin div.bottom-of-ikyu-plugin > h3"
    ),
  ]
    .map((e) => e.innerText)
    .join("\n");

  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  document.body.removeChild(textarea);
})();
```

### domain
- `www.ikyu.com`

## 13. ホテルNoコピー in icotto

```js
(() => {
  const textarea = document.createElement("textarea");
  textarea.textContent = [
    ...document.querySelectorAll(
      "#js-presses > div.l-container > article > div > div.l-container--sticky > section > div > div > div > div > div.p-presses-show-spot__container--left > dl > dd > a"
    ),
  ]
    .filter((e) => e.href.includes("rakuten"))
    .map((e) => e.href.match(/252FHOTEL%252F(\d+)/)[1])
    .join("\n");

  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  document.body.removeChild(textarea);
})();
```

### domain
- `icotto.jp`


## 14. 楽天市場itemCodeコピー 

```js
(() => {
  const textarea = document.createElement("textarea");
  textarea.textContent = [
    ...document.querySelectorAll(
      "#root > div.dui-container.main > div.dui-container.content > div.dui-container.searchresults > div > div"
    ),
  ]
    .filter((e) => e.querySelector("div.content.merchant._ellipsis > a"))
    .map(
      (e) =>
        `${
          e
            .querySelector("div.content.merchant._ellipsis > a")
            .href.split("/")[3]
        }:${e.dataset.id}`
    )
    .join("\n");

  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand("copy");
  document.body.removeChild(textarea);
})();
```

### domain
- `search.rakuten.co.jp`
