# Internal Self-Signed Certificate

This repository contains a self-signed TLS/SSL certificate for internal or local use.

## macOS Installation

To trust the certificate on macOS, run the following command:

```bash
sudo security add-trusted-cert -d -r trustRoot \
  -k /Library/Keychains/System.keychain \
  gotchax.crt
```

## Linux

### Ubuntu / Debian
```bash
sudo cp gotchax.crt /usr/local/share/ca-certificates/
sudo update-ca-certificates
```

### RHEL / CentOS / Rocky / Alma

```bash
sudo cp gotchax.crt /etc/pki/ca-trust/source/anchors/
sudo update-ca-trust
```

## Windows

Open **Command Prompt as Administrator**:

```bash
certutil -addstore -f "Root" selfsigned_gotchax.crt
```

## Mobile Devices
### Android

- Copy selfsigned_gotchax.crt to your device.
- Go to Settings → Security → Install from storage.
- Select the certificate to install.

### iOS

-  Email the certificate to yourself or use AirDrop.
-  Open the certificate file.
-  Tap Install and follow prompts in Settings → General → VPN & Device Management.