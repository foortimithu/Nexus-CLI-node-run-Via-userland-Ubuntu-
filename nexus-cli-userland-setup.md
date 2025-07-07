# 🚀 Nexus CLI Node Setup via UserLAnd (Ubuntu)

This guide helps you run a Nexus CLI Node using **UserLAnd** on Android with Ubuntu.  
Perfect for mobile node runners without needing a laptop or PC.

---

## ✅ Requirements

- 📱 Android device with **UserLAnd** installed  
- 📦 Ubuntu installed inside UserLAnd  
- 💡 Stable internet connection  
- 💰 Wallet address (e.g., Metamask or any EVM-compatible wallet)  
- ⚙️ Minimum 6GB free storage  
- 📄 Terminal access inside Ubuntu

---

## 🛠️ Step-by-Step Setup (A-Z)

### 🔄 1. Update System
```bash
sudo apt update && sudo apt upgrade -y
```

---

### 📦 2. Install Required Dependencies
```bash
sudo apt install curl wget git unzip build-essential pkg-config libssl-dev -y
```

---

### 🦀 3. Install Rust
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

👉 When prompted, press `1` to proceed with the default installation.

Then:
```bash
source $HOME/.cargo/env
```

---

### ⚙️ 4. Install Nexus CLI
```bash
curl https://cli.nexus.xyz/ | sh
```

Add to path:
```bash
echo 'export PATH="$HOME/.nexus/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

---

### 🧾 5. Register Your User (Wallet)
Replace `<YOUR_WALLET_ADDRESS>` with your real wallet address:
```bash
nexus-network register-user --wallet-address <YOUR_WALLET_ADDRESS>
```

---

### 🧠 6. Register Your Node
```bash
nexus-network register-node
```

✅ Save the returned **Node ID** (e.g., `12563135`)

---

### 🚀 7. Start Your Node
Replace `<NODE_ID>` with your actual node ID:
```bash
nexus-network start --node-id <NODE_ID>
```

---

## 🆘 Help and Community

For more information join Telegram:
https://t.me/cryptoincomefree

Join the Telegram for support:
```
https://t.me/cryptoincomefree
```

---

## 🧽 Troubleshooting

| Issue | Fix |
|-------|-----|
| `nexus-network: command not found` | Run `source ~/.bashrc` again |
| CLI install fails | Check if Rust is correctly installed and sourced |
| Node doesn’t sync | Ensure ports are not blocked by mobile/WiFi |

---

## 📌 Notes

- This guide is for **testnet** only.
- Keep UserLAnd app running in foreground or use **Keep Alive** tools.
- Node may stop when Android kills background apps; avoid heavy multitasking.

---

## 🙌 Credits

Made with ❤️ for mobile node runners.  
Join and earn early testnet rewards!
