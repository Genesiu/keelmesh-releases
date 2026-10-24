# Keelark Access 0.2.3-preview.2 for Linux

Ubuntu 22.04 x64 desktop: install the matching client and desktop DEB packages together with sudo dpkg -i. GTK3, WebKitGTK 4.0 and iproute2 are required. Ubuntu 24.04 desktop is not supported by this build.

CLI / background service: amd64 and cross-built arm64 DEB or tar kits. ARM64 native acceptance remains pending. The route page is available in the desktop GUI, not a new headless CLI command.

All resources → Routes reads IPv4/IPv6 OS routes, names known tunnel interfaces and can query actual IP egress. Subnet overlaps are red, but do not necessarily imply failure. Unknown interfaces are not guessed; configuration entries do not claim installed routes. Window unlock is required and locking clears route data. Diagnostics never changes routes or starts a tunnel.

Packages retain the accepted Preview 3 network core. Existing profiles, identities, signed grants and running per-profile services are retained. CLI tar installations support shared-file rollback. No program rollback restores revoked grants. Gateways remain 0.2.2-preview.3 and require no update for route diagnostics.

Native acceptance: Ubuntu 22.04 x64 non-root GTK startup, matching DEB upgrade, authenticated live tunnel/route attribution, resources, signed authorization, restart retention and revocation denial. Full interactive polkit/browser-open and all distribution versions are not claimed.
