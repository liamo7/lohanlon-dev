---
title: 'How this blog is setup with Cloudflare Pages'
description: 'A reference to remember how this site was initially setup.'
pubDate: 'Dec 19 2025'
heroImage: '../../assets/cloudflare-pages-title.jpg'
---

This post is a reference for how this site is set up using Cloudflare Pages, and to serve as a reminder if I need to do this again for another site in the future.

## Overview

This site is hosted on **Cloudflare Pages**, which provides static site hosting with automatic builds and deployments from GitHub.

The site is intentionally static and does not require any server-side runtime or custom infrastructure. 

Deployments happen automatically on every push to the `main` branch.

## Initial setup

The initial setup is done via the Cloudflare dashboard.

Although Cloudflare groups Pages under **“Workers & Pages”**, it is easy to accidentally create a Worker instead. When creating a new application, make sure to explicitly select **Pages**.

The Pages project is configured with the following settings:

- **Framework preset:** Astro  
- **Build command:** `npm run build`  
- **Build output directory:** `dist`

Once configured, Cloudflare automatically builds and deploys the site whenever changes are pushed to the repository.

## Custom domain

A custom domain is attached via the Pages project settings.

Cloudflare automatically:
- Configures DNS records
- Issues and renews HTTPS certificates
- Serves the site via its global edge network

It can take a few minutes for DNS and TLS changes to propagate before the domain becomes accessible.

