# ISC2-CPEsLIST-Bookmarklet
Bookmarklet to get a list of CPEs sorted by date at the new ISC2 CPE Portal (CISSP)

1. Bookmark this.

```javascript:var a={};var t=document.getElementsByClassName("tile");for(var i=0;i<t.length;i++){var h='<tr><td>'+t[i].innerText.replace("<","&lt;").replace(/[\r\n]+/g,'</td><td>').replace(/<td>.*?: /g,'<td>').replace(/<td>Delete<\/td><td>/g,'')+'</tr>';var d=Date.parse(h.match(/[A-Z][a-z][a-z] [0-9]{1,2}, [0-9]{4,4}/));a[d]=h;}a.sort;document.write('<table border=1><tr><th>Title</th><th>CPE Type</th><th>Activity Dates</th><th>Status</th><th>Credits</th><th>Domains</th></tr>');var s=Object.keys(a);s.sort();for(var k in s.reverse()){document.write(a[s[k]]);}document.write('</table>');```

2. Go to https://www.isc2.org/ and sign in.

3. Click "SUBMIT / EDIT MY CPE CREDITS" link.

4. Click "View" in "Your Certifications".

5. Run Bookmarklet.
