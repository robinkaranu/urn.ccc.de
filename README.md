# urn.ccc.de

... is a URN resolver enabling persistent URIs & QR codes, e.g. for inventory & asset mgmt  purposes. The resolver is initially implemented as a simple Nginx configuration, which can be viewed and modified at [https://github.com/voc/urn.ccc.de/](https://github.com/voc/urn.ccc.de/).

This first draft is implemented as a Vhost on [data.c3voc.de](https://c3voc.de/wiki/intern:server:data.c3voc.de), a VM on the [VOC Proxmox Cluster](https://c3voc.de/wiki/intern:server:proxmox).


The schema for the URIs is:

    //urn.ccc.de/<namespace>:<id>

Each local/decentralized entity can request a redirect of namespace to a URL of their choice. IATA & ICAO codes are reserved for the respective Erfa/Chaostreffs. For example, [//urn.ccc.de/muc:b1234](//urn.ccc.de/muc:b1234) redirects to the public representation of the [muCCC](https://c3voc.de/wiki/muCCC) inventory box with the corresponding ID, [//urn.ccc.de/voc:wink:123](//urn.ccc.de/voc:wink:123) to [VOC item 123](https://c3voc.de/wink/items/123)
