ServiceNowBookmarklets
======================

Javascript bookmarklets to auto-apply templates/kb articles to Service Now Tickets


Generic intake:

old
javascript: (function() % 7Bvar L = "https://yale.service-now.com/incident.do?sys_id=-1";
    if (location != L) location = L;
    else %7BreflistPick('incident.u_kb_article', 'e6c37a6d2b4c38c0fcb01abf59da1564', 'KB0000636'); % 7D % 7D)();
new
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

In Person
old
javascript: (function() % 7Bvar L = "https://yale.service-now.com/incident.do?sys_id=-1";
    if (location != L) location = L;
    else %7BreflistPick('incident.u_kb_article', 'fbebf3339004fc40fde6c4b91cbd300a', 'KB0000701'); % 7D % 7D)();
new
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

Over Phone
In Person
old
javascript: (function() % 7Bvar L = "https://yale.service-now.com/incident.do?sys_id=-1";
    if (location != L) location = L;
    else %7BreflistPick('incident.u_kb_article', '8c972ff390c0fc40fde6c4b91cbd300a', 'KB0000695'); % 7D % 7D)();
new
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

