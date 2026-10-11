# A319 / A350 Advanced — public website starter

Freeware, individually registered, donation-supported Aerofly FS 4 aircraft enhancement project.

## Publish the site

1. Create a **new public GitHub repository** (suggested name: `advanced-aerofly`). Keep your aircraft source, private support registry, and third-party sound assets in separate **private** storage.
2. Upload `index.html`, `terms.html`, `privacy.html`, and the `assets/` directory to the repository root. **Do not upload `admin/` or private user data.**
3. In repository **Settings → Pages**, select **Deploy from a branch**, choose `main` / `(root)`, and save. Your pages URL will use the repository owner's GitHub Pages domain.
4. Add approved screenshots, tested aircraft downloads and release notes only after validating redistribution permission for **every bundled third-party asset**.
5. Replace the 'coming soon' download copy with official GitHub Release links once releases actually exist.
6. Create a donation account (e.g., Ko-fi) and add its real official URL to the donation section. No payment link is included in this starter.
7. Finish the privacy notice before requesting or storing user registrations. Set up a private registration contact channel or secure form. Do **not** collect emails through public GitHub issues.
8. Have licensing/permissions reviewed before distributing community sound packages. A prohibition on re-sharing cannot grant permission to distribute someone else's assets.

## Support-key prototype

`admin/support_keys.py` is an **offline command-line issuer**, not a website registration backend. It produces random unique per-aircraft keys and records customer ID, name, email, aircraft and timestamp in a SQLite database stored by default outside the repository at `~/.advanced_support/registrations.sqlite3`.

For example:

```bash
python admin/support_keys.py issue --name "Test User" --email "test@example.invalid" --aircraft a350
python admin/support_keys.py lookup --id 1
```

These keys are **support identifiers**, not secure proof of entitlement or DRM. Automatic request submission, email delivery, online verification, account management and donation processing are **not connected** in this prototype.

## Publish-ready checklist

- [ ] Verify permissions for all sounds and other third-party assets
- [ ] Review licence, README and installer acceptance wording
- [ ] Confirm screenshots and product descriptions against shipping builds
- [ ] Add contact details, GDPR lawful basis, retention and erasure procedure to privacy notice
- [ ] Choose a secure way to receive requests and deliver keys privately
- [ ] Add live donation URL
- [ ] Prepare release ZIPs and checksum files
- [ ] Publish links and carry out Windows/laptop installation tests
