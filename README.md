# Internal Self-Signed TLS/SSL Certificates

This repository contains **self-signed TLS/SSL certificates for internal use only**.

These certificates are intended for development, testing, and internal services.
**Do not use these certificates in public or production environments.**

---

## ⚠️ Security Notice

- This repository contains **trust material**.
- Only authorized team members should have access.
- Self-signed certificates bypass public CA validation and **should never be used externally**.
- Treat certificates and private keys as sensitive assets.

---

## Installing the Certificate

### macOS

To trust the self-signed certificate on macOS, run the following command:

> ⚠️ Requires administrator privileges.  
> This installs the certificate into the **System keychain**, making it trusted system-wide.

```bash
sudo security add-trusted-cert -d -r trustRoot \
  -k /Library/Keychains/System.keychain \
  selfsigned_gotchax.crt
