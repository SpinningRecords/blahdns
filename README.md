* [![HitCount](http://hits.dwyl.io/ookangzheng/blahdns.svg)](http://hits.dwyl.io/ookangzheng/blahdns) 
* Need some coffee to keep servers operate 🥰 <a href='https://ko-fi.com/P5P4GPQ8' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://az743702.vo.msecnd.net/cdn/kofi4.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>


## Announcements

* All DoT, DoH SSL cert is up to date, will be expire at July 20, 2020
* For more old announcements, go [here](https://github.com/ookangzheng/blahdns/issues/36)
* Blahdns blacklist [Hosts](https://oooo.b-cdn.net/blahdns/adsblock.txt) or [RPZ](https://oooo.b-cdn.net/blahdns/rpz.txt) 

## Our features
* Block Trackers, Ads, Malwares
* No ECS, DNSSEC ready, No logs, OpenNIC, Eth TLD, Yggdrasil 
* Both trackers are blocked by default. 
`data.mob.com, google-analytics, googleadservices, amazon-adsystem, crashlytics.com analytics.yahoo, doubleclick.net, hm.baidu.com, etc.. `
* support http://matoken.eth/ | http://mesh.ygg/ | http://i2pd.ygg/ | http://blahdns.oss/ | https://i❤.ws/

## Beta DoH CDN (Japan & Finland only)
```
https://doh1.blahdns.com/uncensor 
https://doh2.blahdns.com/uncensor 
https://doh1.blahdns.com/dns-query (censored)
https://doh2.blahdns.com/dns-query (censored)
```

## Curl with DoH for testing purpose
```
// Censored 
curl --doh-url https://doh-jp.blahdns.com/dns-query https://ssl.google-analytics.com
// Return 
curl: (7) Failed to connect to ssl.google-analytics.com port 443: Connection refused

// Uncensor
curl --doh-url https://doh-jp.blahdns.com/uncensor https://ssl.google-analytics.com
// Return
<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="https://www.google.com/analytics/">here</A>.
</BODY></HTML>
```

## How to setup / config DoH DoT Dnscrypt 👇
Config: [HERE for more details](https://github.com/ookangzheng/blahdns/tree/master/server-conf)

## Server status
* Server status [UpTimeRobot](https://stats.blahdns.com) | [Dnsprivacy.org](https://dnsprivacy.org/jenkins/job/dnsprivacy-monitoring/)

## Server architecture

```bash
Server (August 25, 2019 -- Germany, Japan, Finland)
|-- Let's Encrypt SSL
|-- Knot-resolver (OpenNIC, ICANN)
|   |-- DNSCryptv2 (dnsdist, port 8443)
|   |-- doh-server (DoH, GET, POST -- m13253)
|   |-- |-- DoH (HAProxy, port 443, TLS 1.3, require SNI)
|-- DoT (HAProxy, port 853, 443, TLS 1.3, require SNI)
```

## Config file / Client
* Yggdrasil IPv6 Network: [Setup guide](https://github.com/ookangzheng/blahdns/blob/master/client-conf/yggdrasil.md)
* Android DoH/DoT: [Nebulo App](https://play.google.com/store/apps/details?id=com.frostnerd.smokescreen) | [personalDNSfilter App](https://zenz-solutions.de/personaldnsfilter/) | [Intra](https://play.google.com/store/apps/details?id=app.intra)
* iOS Dnscryptv2/DoH: [Dnscloak](https://itunes.apple.com/app/dnscloak-secure-dns-client/id1452162351)
* Dnscryptv2: [dnscrypt-proxy](https://github.com/jedisct1/dnscrypt-proxy/)
* Config files: [ Client config example ](https://github.com/ookangzheng/blahdns/tree/master/client-conf)

## Default blocked wildcard domain
* `+.glassbox.+ `# https://techcrunch.com/2019/02/06/iphone-session-replay-screenshots

## Awesome dns-resolver
https://gist.github.com/ookangzheng/c8fba46fe1dbcc8152e3231f53f91e86

## Huge thanks to those OSS and ORG
1. [Knot-resolver](https://github.com/CZ-NIC/knot-resolver)
2. [m13253](https://github.com/m13253/dns-over-https)
3. [DNSPrivacy.org](https://dnsprivacy.org)

## Disclaimer
* This is an experimental service, I'm not responsible for any down-time.
* Be sure you have agree with our [POLICY](https://github.com/ookangzheng/blahdns/#policy) before start to use. 
* This service is for PERSONAL use, huge traffic are not welcome, will drop PTR, ANY by default.
* We can't block some ads with Apps inside your phone (Youtube official app Ads, Facebook app Ads, Twitter app Ads... )

## Policy
* Use at your own risk. Under no circumstances will the operator be held responsible or liable in any way for any claims, damages, losses, expenses, costs or liabilities whatsoever (including, without limitation, any direct or indirect damages for loss of profits, business interruption or loss of information) resulting or arising directly or indirectly from accessing or otherwise using this service (Blahdns server).
* The operator does not guarantee in any way the access, availability and continuity of the functioning of this service. 
* By using this website and service you consent to the disclaimer and agree to its terms and conditions.

## Donate

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=KC33GK5CT2Q9Y&source=url)
|
<a href='https://ko-fi.com/P5P4GPQ8' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://az743702.vo.msecnd.net/cdn/kofi4.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>
