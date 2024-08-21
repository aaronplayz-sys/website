---
layout: post
title: My Adguard Home DNS Setup
date: 2024-08-19
description: For a while I have been expeirmenting my configurations, now I feel like sharing my journey and my configurations.
tags: Linux, DNS
categories: posts
toc:
  sidebar: left
---

## My start with DNS servers

Starting out early in my IT journey and taking privacy, and security in mind. After reading articles and watching videos online. Using a diffrent DNS server can sometimes a small improvment to your online experience. For this reason I had always pointed my devices to quad9 servers because of were they are based and their logging policies.

## Using Pihole

Now, I do not have any hate for pihole, I could never seem to find my way around the menu. For many this software dose wonders. For me it felt too technical to use and stuck with DNS servers that filters ads and more with providers like Adguard DNS. For a while this suited my needs, then I wanted to include more extensive lists to expand the coverage.

Sure using providers like Adguard DNS or NextDNS are awsome. The only factor that keeps me from using them are having to pay monthly to keep the filtering service active.

## The release of Adguard Home

When this software came out, I decided to try it out and deployed it on my network. To me this software has a modern take on handling DNS request and the ability to use DNS-Over-Https and DNS-Over-TLS protocold