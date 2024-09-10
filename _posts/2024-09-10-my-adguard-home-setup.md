---
layout: post
title: My Adguard Home DNS Setup
date: 2024-09-10
description: For a while I have been expeirmenting my configurations, now I feel like sharing my journey and my configurations.
tags: Linux, DNS
categories: posts
toc:
  sidebar: left
---

## My start with DNS servers

Starting out early in my IT journey and taking privacy, and security in mind. After reading articles and watching videos online. Using a different DNS server can sometimes be a small improvement to your online experience. For this reason I had always pointed my devices to quad9 or Cloudflare servers because of were they are based and their logging policies.

## Using Pihole

Now, I do not have any hate for pihole, I could never seem to find my way around the menu. To many this software does wonders. For me, it felt too technical to use and stuck with DNS servers that filter ads and more with providers like AdGuard DNS. For a while this suited my needs, then I wanted to include more extensive lists to expand the coverage.

Sure using providers like AdGuard DNS or NextDNS are awesome. The only factor that keeps me from using them are having to pay monthly to keep the filtering service active as most limit the free tier to around 300k requests a month. I did use NextDNS on my phone exclusively for a while to see if I could hit that monthly limit. I have to say, it's not, so bad live off on the free tier if only one device is pointed to the server with your identifier.

## The release of AdGuard Home

When this software came out, I decided to try it out and deployed it on my network. To me this software has a more modern take on handling DNS request and the ability to use DNS-Over-HTTPS and DNS-Over-TLS protocol. Something that pihole can not do out of the box without you having to set up additional software to use DNS-Over-HTTPS. 

AdGuard Home can handle different types rules when it comes to blocking IP's and domains. It understands traditional rules used in ad blocking extensions, host-style (IP addresses), or just a list of domain names.

Since AdGuard Home is a self-host solution, you have more control over what it can do compared to a cloud solution like AdGuard DNS in terms of fine-tuning to your liking.

## My configuration

There are many ways to set up AdGuard Home as there a few ways to block and whitelist domains. I have closely followed yokoffing's guide on [NextDNS-Config](https://github.com/yokoffing/NextDNS-Config) as a based for filters. The rest of my config was inspired from Reddit posts I saw and experimenting with settings.

### General settings

Filter update interval: 24 hours

> ##### TIP
>
> Most lists, including the ones I'm using update once a day.
{: .block-tip }

Optional: Enable AdGuard browsing security web service

Optional: Enable AdGuard parental control web service

> ##### WARNING
>
> These web services preforms API lookups on the domains you browse.
> Do not enable if this is a concern.
{: .block-warning }

Enable log(on by default):

Optional: Anonymize client IP

Query logs rotation: 30 days

> ##### TIP
>
> Logs can be handy when needing to whitelist domains.
> Set the rotation lower if you wish.
{: .block-tip }

Enable statistics(on by default):

Statistics retention: 30 days

> ##### TIP
>
> This keeps track of request made, how many are blocked, etc.
> It is what is shown on the dashboard page.
{: .block-tip }

<div class="row mt-3"> 
  <div class="col-sm mt-3 mt-md-0"> 
    {% include figure.liquid loading="eager" path="assets/img/adguard-home-setup/General-1.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/adguard-home-setup/General-2.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/adguard-home-setup/General-3.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
</div>
<div class="caption"> 
  Screenshot's for reference
</div>

### DNS settings