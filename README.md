# 📦 UniversalRepository

A community-maintained third-party package repository providing pre-built packages
for multiple Linux distributions from a single source.

> **Browse packages:** https://universalrepo.r1xelelo.workers.dev/
> **Source:** https://codeberg.org/UniversalRepository/Packages

---

## 📥 Installation

### Void Linux

```sh
echo "repository=https://universalrepo.r1xelelo.workers.dev/void" \
  | sudo tee /etc/xbps.d/universalrepo.conf
```

### Fedora

```sh
sudo curl -o /etc/yum.repos.d/universal.repo \
  https://universalrepo.r1xelelo.workers.dev/universal.repo
```

### Arch Linux

```sh
# Import and sign the GPG key
sudo pacman-key --recv-key F600BA22F0D90359 --keyserver keyserver.ubuntu.com
sudo pacman-key --lsign-key F600BA22F0D90359

# Add the repository to /etc/pacman.conf
sudo tee -a /etc/pacman.conf <<EOF

[universal-repo]
Server = https://universalrepo.r1xelelo.workers.dev/arch
EOF
```

---

## 📄 License

See [LICENSE](LICENSE) for details.