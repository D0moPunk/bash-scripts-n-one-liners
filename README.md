A repository of utility bash scripts and one-liners for security automation and penetration testing. It's in the works.

Extract links from html document
--------------------------------
cat document.html | grep -Eo "(http|https)://[a-zA-Z0-9./?=_%:&-]*" | sort -u

Get browser inactivity (JavaScript)
-----------------------------------
'This page has been inactive for: ' + Math.round((Date.now()-new Date(performance.getEntriesByType("navigation")[0].loadEventEnd+performance.timeOrigin))/60000) + ' minutes.'

openssl for testing weak ciphers and protocols
----------------------------------------------
openssl s_client -connect [host]:443 -tls1 -cipher DES-CBC3-SHA



