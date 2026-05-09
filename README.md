# 📦 UniversalRepository

A community-maintained third-party package repository providing pre-built packages
for multiple Linux distributions from a single source.
---

## 📥 Installation

### Void Linux

```sh
echo "repository=https://universalrepository.pages.dev/void" \
  | sudo tee /etc/xbps.d/universalrepo.conf
```

### Fedora

```sh
[universalrepository]
name=Universal Repository
baseurl=https://universalrepository.pages.dev/fedora
enabled=1
gpgcheck=0
metadata_expire=1h
priority=10
```

### Arch Linux

```sh
# Import and sign the GPG key
sudo pacman-key --recv-key F600BA22F0D90359 --keyserver keyserver.ubuntu.com
sudo pacman-key --lsign-key F600BA22F0D90359

# Add the repository to /etc/pacman.conf
sudo tee -a /etc/pacman.conf <<EOF

[universal-repo]
Server = https://universalrepository.pages.dev/arch
EOF
```

---

## 📄 License

See [LICENSE](LICENSE) for details.
