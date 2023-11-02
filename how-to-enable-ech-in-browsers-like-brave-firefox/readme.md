> How to enable (ESNI) ECH in browsers like brave, chrome or firefox

> Why do we need encrypted SNI? https://www.cloudflare.com/learning/ssl/what-is-encrypted-sni/

**How to enable ech in firefox**

```
1. Go to the settings options in the firefox and open the Privacy and Settings tab and scroll down to DNS over HTTPS.
  1.1 Select either from the Default, Increased or Max Protection and select the provider NextDNS(also you can choose Cloudflare).
2. Open New Tab and type "about:config" in the address bar and select the accept the risk and continue option to proceed
  2.1 Search "network.trr.mode" and change it to 3 from 2
  2.2 Seach and Toggle "network.dns.echconfig.enabled" to true from false
  2.3 Similary, change "network.dns.http3_echconfig.enabled" and "security.tls.ech.grease_http3"
3. Restart the browser and visit the site https://tls-ech.dev to check whether the browser is using ech or not
```
Website to check - https://tls-ech.dev and https://www.cloudflare.com/ssl/encrypted-sni/

**How to enable ech in brave or chromium fork browsers**

```
1. Open the Settings panel go to the Privacy and Security section in Brave Browser and select the security sub-section.
2. Select the "use-secure-dns" section and select the NextDNS(or Cloudflare) from the Dropdown.
3. Open New Tab and type "brave://flags" or "chrome://flags" in the respective browsers
  3.1 Change these settings or flags - (Toggle this from Default to Enabled)
    3.1.1 #encrypted-client-hello - Enabled
    3.1.2 #use-dns-https-svcb-alpn - Enabled
4. Restart the browser and visit the site https://tls-ech.dev to check whether the browser is using ech or not
```

**Images of firefox**
![Firefox Ech Setting](https://user-images.githubusercontent.com/74139127/280112000-4107aa44-c372-4890-aac2-ebd88a5dc8ef.png)
![Firefox Ech Setting](https://user-images.githubusercontent.com/74139127/280111997-12f3b6ad-cfb0-4ab1-a8a1-b522adaaf33b.png)
![Firefox Ech Setting](https://user-images.githubusercontent.com/74139127/280112002-bcef4c33-8306-4050-993f-780535e4f00f.png)
![Firefox Ech Setting](https://user-images.githubusercontent.com/74139127/280112005-b0535a56-c2cf-487e-babe-90fac26e185b.png)
![Firefox Ech Setting](https://user-images.githubusercontent.com/74139127/280112010-7cab1a01-f5e8-4fc6-826d-68e7bf7034a4.png)


**Images of Brave Browser - similar for chromium fork browsers**
![Brave ESNI Setting](https://user-images.githubusercontent.com/74139127/280112307-d3508f6c-3dc4-4257-8fed-c6ee9a30b6b0.png)
![Brave ESNI Setting](https://user-images.githubusercontent.com/74139127/280112317-cbfc7958-0752-4e4c-895d-4cca93270bca.png)
![Brave ESNI Setting](https://user-images.githubusercontent.com/74139127/280112319-103c982f-d644-4008-9ed3-e43a31948e87.png)
![Brave ESNI Setting](https://user-images.githubusercontent.com/74139127/280112320-c15613d3-8d3f-4385-a714-180d70978acf.png)

