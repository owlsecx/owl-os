# Trust & Verification — Owl OS

Owl OS ships closed-source security tools. That is a deliberate choice, and it
places the burden of proof on us, not on you. This document is how we carry
that burden: what is open, what is closed, what is inside every binary, and how
you can verify all of it yourself.

Last updated: 2026-11-25

---

## 1. Who publishes Owl OS

| | |
|---|---|
| Publisher | Owlsec LLC, New Mexico, United States |
| Website | <https://owlsec.org> |
| Code & inventories | <https://github.com/owlsecx> |
| Contact | info@owlsec.org |
| Security reports | team@owlsec.org |
| Signing key | `22A8 E563 B2E6 4BF8 E121 A2FF 00F5 645A CE5D 0436` |

---

## 2. What is open, what is closed, and why

**Open / unmodified and fully traceable**

- The operating system base is Debian GNU/Linux 12 ("bookworm").
- The Cinnamon desktop and every other Debian package is redistributed
  **unmodified**, at the exact version published by Debian. We have **not**
  rebuilt or patched a single GPL-licensed package.
- Branding is configuration only: theme names, dconf/gsettings values,
  wallpapers, boot splash artwork, icon sets. No GPL source code is altered.
- Third-party tools bundled from the ecosystem (Metasploit, nmap, sqlmap,
  Ghidra, aircrack-ng, bettercap and others) keep their own licenses, which
  ship inside the ISO at `/usr/share/doc/<package>/copyright`.

**Published under the GNU GPL, with full source**

- 39 OwlSec tools written in Go are released under **GPL-3.0**, and 11 written
  in Python under **GPL-2.0**. Their complete source is published at
  <https://github.com/owlsecx> and mirrored at <https://gitlab.com/owlsecx>.
  Each repository states its own licence.

**Closed**

- The remaining OwlSec tools written by Owlsec LLC are proprietary. They are
  distributed as pre-built executables; their source code is not published.
- Reason: they represent three years of original development and are the
  commercial basis of the project.

Closed source is an established model in this field — Burp Suite, Nessus,
Cobalt Strike and Acunetix are all closed. What those products owe their users
is verifiability by other means. So do we. Sections 3 to 6 are that.

---

## 3. Verify the release you downloaded

Every release ships `SHA256SUMS` and a detached signature `SHA256SUMS.asc`.

```bash
# 1. Import the Owl OS signing key
curl -fsSL https://owlsec.org/downloads/owl-os-signing-key.asc | gpg --import

# 2. Confirm the fingerprint matches the one published above
gpg --fingerprint 00F5645ACE5D0436

# 3. Verify the signature on the checksum file
gpg --verify SHA256SUMS.asc SHA256SUMS

# 4. Verify the ISO itself
sha256sum -c SHA256SUMS
```

If step 3 or 4 fails, **do not use the image.** Report it to
team@owlsec.org.

The APT repository at `https://owlsec.org/repo/` is signed with the same key
and configured with `signed-by=`, so unsigned or tampered packages are
rejected by APT itself.

---

## 4. Know exactly what is inside every tool — without the source

Each tool repository contains two files, generated directly from the shipped
binary:

| File | What it gives you |
|---|---|
| `SBOM.cdx.json` | A CycloneDX Software Bill of Materials: the SHA-256 of the binary, the bundled CPython version, and **every** bundled library with its exact version and license. |
| `THIRD-PARTY-NOTICES.md` | The full license text of every third-party component, extracted from the binary itself. |

You can feed the SBOM to any standard scanner (Grype, Trivy, Dependency-Track,
OWASP dependency tooling) and audit our dependencies for known CVEs without
ever seeing our code.

Current state of the toolkit:

- 199 tools bundle **no third-party packages at all** — only the Python
  standard library.
- 51 tools bundle third-party libraries, each listed with version and license.

---

## 5. What the tools do on the network

- The OwlSec tools contain **no telemetry, no analytics, no licence check-in,
  and no automatic update calls.** They do not phone home.
- Any network traffic a tool generates is traffic **you asked it to generate**
  against **the target you specified**.

Do not take our word for it — closed binaries can be observed:

```bash
# Watch every network connection a tool makes
sudo strace -f -e trace=network ./OToolName <args>

# Or capture everything it sends
sudo tcpdump -i any -w tool.pcap &
./OToolName <args>

# Or deny it the network entirely and confirm it still behaves
firejail --net=none ./OToolName --help
```

Behavioural verification works on closed software. We encourage it.

---

## 6. GPL and licence compliance

- [`GPL-WRITTEN-OFFER.txt`](GPL-WRITTEN-OFFER.txt) — our formal three-year offer to supply the
  corresponding source of any GPL/LGPL package in a release.
- [`PACKAGE-MANIFEST.txt`](PACKAGE-MANIFEST.txt) — every Debian package in the release with its exact
  version, so any source can be fetched directly from Debian.
- Because all packages are unmodified, the corresponding source is also
  permanently available from Debian:
  `apt-get source <pkg>=<version>` or <https://snapshot.debian.org/>.
- Our proprietary tools are separate, independent programs distributed on the
  same medium (mere aggregation under GPLv2 §2). They do not link against,
  embed or incorporate GPL-licensed code. The SBOM for each tool is the
  evidence.

If you believe we have a compliance problem, write to info@owlsec.org with the
package and version. We will fix it or publish the source.

---

## 7. Reporting a vulnerability

Email **team@owlsec.org**. Please include affected tool and version, steps
to reproduce, and impact.

- We acknowledge within **72 hours**.
- We aim to ship a fix or a mitigation within **30 days**.
- We will credit you unless you ask us not to.
- Please do not disclose publicly until a fix is available.

---

## 8. Warnings — read these before deploying anything

> **Do not add the Owl OS APT repository to a production system.** It is built
> for Owl OS live and installed desktops. Mixing it into other Debian systems
> can pull unexpected package versions. This warning applies to any
> third-party APT repository, ours included.

> **Try Owl OS in a virtual machine first.** Verify the signature, boot it
> live, and satisfy yourself before installing it on hardware or trusting it
> with engagement data.

> **Owl OS contains offensive security tools.** Using them against systems you
> do not own or lack written authorisation to test is illegal in most
> jurisdictions. You are responsible for your use.

> **Hidden Mode is a convenience, not an anonymity guarantee.** It routes
> traffic through Tor and adds privacy utilities. It cannot protect you against
> a determined adversary, misconfiguration, or your own mistakes.

---

## 9. How Owl OS differs from Kali or BlackArch

Honestly: the base system does not. It is Debian 12 with a Cinnamon desktop
and the same well-known tools Kali also packages.

The difference is the **275+ original OwlSec tools** — auditors, hardening
checkers and intelligence utilities written for this distribution, organised
into categories, with consistent CLI conventions and machine-readable output
(JSON, CSV, SARIF) suitable for pipelines.

If the OwlSec tools are not useful to you, Kali or BlackArch will serve you
better, and we would rather say so than oversell. Check the SBOMs, read the
tool list, and judge for yourself.
