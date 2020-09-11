---
title: cloudflareHelper.ps1
description: Details about the cloudflareHelper.ps1 script
---

# cloudflareHelper.ps1

## Overview

The `cloudflareHelper.ps1` script has functionality to assist interacting with the cloudflare API in order to create DNS entries

## Functions

* CallCloudflare([string]$token, [string]$urlPart, [Microsoft.PowerShell.Commands.WebRequestMethod]$method, [string]$body = $null)
* GetCloudflareDnsZone([string]$token, [string]$domain)
* GetCloudflareDnsRecord([string]$token, [string]$zoneid, [string]$domain, [string]$record)
* CheckCloudflareDnsRecord([string]$token, [string]$zoneid, [string]$domain, [string]$record)
* GetCloudflareDnsIp([string]$token, [string]$domain, [string]$record)
* CreateCloudflareARecord([string]$token, [string]$domain, [string]$record, [string]$ipaddr)
* UpdateCloudflareARecord([string]$token, [string]$domain, [string]$record, [string]$ipaddr, [bool]$warnOnUpdate = $false)
* CreateOrUpdateCloudflareARecord([string]$token, [string]$domain, [string]$record, [string]$ipaddr, [bool]$warnOnUpdate = $false)