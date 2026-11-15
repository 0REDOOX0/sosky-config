# SOSKY Tunnel — config

Encrypted configuration for the **SOSKY Tunnel** app.

- Every `*.enc.json` file is an **AES-256-GCM** envelope: `{"v":1, "alg":"AES-256-GCM", "iv":..., "data":...}`
- `manifest.json` lists the SHA-256 of every envelope and is **signed with Ed25519**.
  The app verifies the signature (public key embedded in the app) and every hash
  before decrypting — a tampered or fake config is rejected.
- No keys live in this repository. Plaintext configs never leave the owner's machine.

Files: ssh, ssl, openvpn, xray, hy2, dnstt, sslovpn, ovpn_files, version.
