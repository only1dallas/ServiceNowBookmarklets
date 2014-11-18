# ServiceNowBookmarklets

## Meta Bookmarklet Generator
Use this to create your own bookmarklets like the ones below!
To use this:
1. Copy this code, paste this into the "Location" of a new bookmark. You might name this "MetaBookmarkletCreator".
2. Navigate to the KB article (open in a new tab, without Service Now frames around it. You might cmd+click on the link of the KB article)
3. Click on the bookmark you made in step 1
4. Follow the instructions in the popup.

```
javascript: (function() {      var L = 'https://yale.service-now.com/incident.do?sys_id=-1';      var LOCATIONSTRING = location.href;      var onANewTicketPage = (LOCATIONSTRING.indexOf('sys_id=-1') > -1);      if (onANewTicketPage) {          reflistPick('incident.u_kb_article', '1de812cc4ddcbd80a6c49b2b9ba4a296', 'KB0005128');      } else {          location = L;      }      })();
```

## Bookmarklet Examples
Javascript bookmarklets to auto-apply templates/kb articles to Service Now Tickets

To use this:
1. Copy this code, paste this into the "Location" of a new bookmark. You might name this "+GenericIntake" if your KB article name is "Generic Intake".
2. Click on the bookmark you made in step 1, follow the instructions in the popup.

If you'd like one that applies a different template than the ones below, try the `Meta Bookmarklet Creator` above.

### STC Generic Intake

```
javascript: (function() {
    var L = "https://yale.service-now.com/incident.do?sys_id=-1";
    var LOCATIONSTRING = location.href;
    var onANewTicketPage = (LOCATIONSTRING.indexOf("sys_id=-1") > -1);
    if (onANewTicketPage) {
        reflistPick('incident.u_kb_article', 'e6c37a6d2b4c38c0fcb01abf59da1564', 'KB0000636');
    } else {
        location = L;
    }
})();
```

### In Person

```
javascript: (function() {
    var L = "https://yale.service-now.com/incident.do?sys_id=-1";
    var LOCATIONSTRING = location.href;
    var onANewTicketPage = (LOCATIONSTRING.indexOf("sys_id=-1") > -1);
    if (onANewTicketPage) {
        reflistPick('incident.u_kb_article', 'fbebf3339004fc40fde6c4b91cbd300a', 'KB0000701');
    } else {
        location = L;
    }
})();
```
### Over Phone

```
javascript: (function() {
    var L = "https://yale.service-now.com/incident.do?sys_id=-1";
    var LOCATIONSTRING = location.href;
    var onANewTicketPage = (LOCATIONSTRING.indexOf("sys_id=-1") > -1);
    if (onANewTicketPage) {
        reflistPick('incident.u_kb_article', '8c972ff390c0fc40fde6c4b91cbd300a', 'KB0000695');
    } else {
        location = L;
    }
})();
```
