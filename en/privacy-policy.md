---
title: Privacy Policy
description: Privacy policy for Parallel-Bridge
lang: en
---

[日本語]({{ '/privacy-policy' | relative_url }}) · [User Guide]({{ '/en/' | relative_url }})

Applies to: the Windows app "Parallel-Bridge" and the Edge extension "Parallel-Bridge for Edge"

Last updated: 2026-09-12

## Summary

Parallel-Bridge opens file-share paths (UNC paths of the form `\server\share\...`) written on
pages on your local network in File Explorer with a single click.

**Parallel-Bridge does not send your information to the developer or to any third party.**
There are no ads, no analytics, and no usage tracking (telemetry).
Everything happens on your own PC.

## What the Windows app handles

### The contents of a link

When you click a link, the app receives:

- the share path to open
- the website the link claims to come from (its origin)
- an optional title for display

These are used only to check that the path is in a safe form and to open File Explorer.

### What is stored on your PC

The app stores the following in its private per-user app folder.
Other users and other apps cannot read it.

| Information | Purpose |
|---|---|
| Settings (shares that open without asking, allowed servers, click behavior) | So you are not asked the same question again |

**No history or log of the folders you open is kept.**

Uninstalling the app deletes all settings.

### Network access

The app accesses the network only **to check that the linked share exists**.
This uses Windows' built-in file sharing (SMB) and goes to the file server named in the link.
Displaying the folder afterwards is done by File Explorer.

For safety, the app contacts only servers on your local network by default.
Links pointing to servers on the internet are not opened.

### The Windows registry

To communicate with the browser extension, the app creates one registry key:

```
HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.parallelbridge.host
```

The key contains only the location of a configuration file inside the app's own folder.
Because of how Windows packaging works, the key remains after you uninstall the app,
but the file it points to is removed, so it has no effect.
You can delete it with Registry Editor if you wish.

## What the browser extension handles

### Page content

The extension reads page content **only on sites you have enabled**, to find share links and
text that looks like a share path.
On sites you have not enabled, it does not access page content at all.

Paths it finds are handed **only to the Parallel-Bridge app on your own PC** when you click them.
They are never sent to an external server.

### What is stored

| Information | Where |
|---|---|
| The list of sites you enabled | The browser's extension storage |
| The list of sites where plain text paths are also linked | Same |
| Click behavior, marking of converted links | Same |

**If browser sync is turned on**, these settings sync to the other browsers you are signed in to.
That sync is a feature of Microsoft Edge and follows the browser vendor's policy.

### Permissions used

| Permission | Why |
|---|---|
| Storage | To save the settings above |
| Scripting, active tab | To run the link conversion, only on sites you enabled |
| Site access (optional) | Requested per site, only when you press "Enable on this site" |
| Native messaging | To communicate with the Parallel-Bridge app on your PC |

## Third parties

Parallel-Bridge does not sell, provide, or share your information with third parties.

## Children's privacy

Parallel-Bridge does not collect personal information from anyone, regardless of age.

## Changes to this policy

If this policy changes, this page is updated and the "last updated" date is revised.

## Contact

Please use [GitHub Issues](https://github.com/msmsrep/Parallel-Bridge/issues)
for bug reports and questions about this policy.
