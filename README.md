# DM Dog Training: temporary www redirect

Temporary GitHub Pages site for www.dmdogtraining.co.uk (Oct 2026). Wix kept www attached to its
Cloudflare account after Dec disconnected the domain, so www pointed at Wix's 404. www is a
DNS-only CNAME to GitHub Pages instead, and every page here sends visitors to the same path on
https://dmdogtraining.co.uk (the live site, Big-Bark-Media/dm-dog-training).

Undo once Wix releases www: delete the CNAME in Cloudflare, add www back as a custom domain on the
dm-dog-training Worker (wrangler.jsonc), set REDIRECT_APEX back to "true", then archive this repo.
