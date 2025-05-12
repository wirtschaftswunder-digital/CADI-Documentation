---
layout: default
title: Troubleshooting
has_children: true
has_toc: true
permalink: 
nav_order: 8
---

# Troubleshooting
{: .no_toc }

## Laden der Buchungsmaske wird blockiert


Wenn die Buchungsmaske oder die Termin Tabelle auf einer Website nicht richtig laden oder bestimmte Funktionen wie die automatische Höhenanpassung der Termin-Tabelle nicht funktionieren, liegt das häufig an den Sicherheitseinstellungen der einbettenden Website – genauer gesagt an der **Content Security Policy (CSP)**.

### Ursache

Die Seite, auf der die Buchungsmaske eingebettet ist, erlaubt nur das Laden von Skripten von der eigenen Domain. Skripte von externen Quellen wie `cdn.jsdelivr.net` oder `pf.camps.digital` werden blockiert. Unsere Buchungsmaske nutzt jedoch ein Script von dort, um die Höhe der Termin-Tabelle automatisch an den Inhalt anzupassen.

Im HTML-Quellcode der betroffenen Seite findet sich meist ein Eintrag wie dieser:

```html
<meta http-equiv="Content-Security-Policy" content="script-src 'self';">
```

### Lösung

Die Content Security Policy (CSP) der einbettenden Seite muss so erweitert werden, dass Skripte von `cdn.jsdelivr.net` und unseren anderen Quellen erlaubt sind. Je nach Setup (z. B. WordPress-Plugin oder Theme-Datei) kann dies unterschiedlich umgesetzt werden.

Füge folgenden `meta`-Tag im `<head>` der Seite ein **oder passe ihn entsprechend an**, wenn er bereits vorhanden ist:

```html
<meta http-equiv="Content-Security-Policy" content="script-src 'self' https://cdn.jsdelivr.net https://pf.camps.digital;">
```