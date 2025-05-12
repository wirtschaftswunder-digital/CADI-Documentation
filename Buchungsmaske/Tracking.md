---
layout: default
title: Google Ads Tracking
parent: Buchungsmaske
nav_order: 7
---

# Tracking
{: .no_toc }

## 1. Script auf Webseite

Um das neue CADI Setup zu nutzen muss das folgende Script auf Ihrer Webseite **global** eingebunden werden. Es muss also auf allen Unterseiten geladen werden. Das Script sorgt dafür, dass von Google Ads hinzugefügte URL Tracking Parameter bei der Navigation über Ihre Webseite nicht verloren gehen und dass die Parameter von der CADI Buchungsmaske ausgelesen werden können.

```js
<script src="https://cdn.jsdelivr.net/gh/wirtschaftswunder-digital/cadi-conversion-support@latest/index.js"></script>
```

## 2. Einstellungen in CADI

In der CADI Company App müssen Sie Ihr Google Ads Konto vollständig verknüpfen. Befolgen Sie dazu die unter *Tracking* aufgeführten Schritte in der Company App.