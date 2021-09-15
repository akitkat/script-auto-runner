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
