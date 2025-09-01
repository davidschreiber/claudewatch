# ⌚ ClaudeWatch

> *Never miss a Claude moment on your wrist* 🤖✨

**ClaudeWatch** delivers instant WearOS notifications whenever Claude AI needs your input or completes tasks. Stay connected to your AI assistant, wherever you are! 

---

## ✨ Features

🔔 **Instant Notifications** - Get pinged when Claude needs you  
✅ **Task Alerts** - Know immediately when work is done  
⌚ **Watch Integration** - Full WearOS native experience  
⚡ **Battery Smart** - Optimized for all-day wear  
🎛️ **Customizable** - Your alerts, your way  

## 🚀 Quick Start

```bash
git clone https://github.com/davidschreiber/claudewatch.git
cd claudewatch
./gradlew installDebug
```

## 📋 Requirements

- 📱 WearOS 3.0+ smartwatch
- 🤖 Claude AI account  
- 📶 Internet on phone & watch

## 🏗️ Project Structure

```
📦 claudewatch/
├── 🖥️ server/     # Ktor backend (Railway deployment)
├── 📱 mobile/     # Phone companion app (FCM receiver)
├── ⌚ wear/       # WearOS app (notification mirror)
└── 🔧 .github/    # CI/CD workflows
```

### Architecture Overview

**Companion-Centric Design:**
- 🖥️ **Backend (Ktor)**: Receives webhooks, sends FCM push notifications
- 📱 **Phone App**: Receives FCM, creates local notifications (auto-mirrors to WearOS)
- ⌚ **WearOS App**: Lightweight, receives mirrored notifications from Phone

**Key Benefits:**
- ✅ Single notification source (no duplicates)
- ⚡ Battery efficient on WearOS
- 🔄 Automatic Phone→Watch synchronization
- 🌐 Centralized webhook processing

## 🔒 Privacy First

✅ Encrypted data transmission  
✅ No content stored on watch  
✅ Secure token storage  
✅ Minimal data collection  

## 🤝 Contributing

Love the project? Jump in! 

1. 🍴 Fork it
2. 🌿 Branch it (`git checkout -b feature/cool-thing`)
3. 💾 Commit it (`git commit -m 'Add cool thing'`)
4. 🚀 Push it (`git push origin feature/cool-thing`)
5. 📬 PR it!

## 📄 License

MIT License - see [LICENSE](LICENSE) for details

---

<div align="center">

**Built with ❤️ for Claude AI enthusiasts**

🏗️ *WearOS* • 🎨 *Material3* • ⚡ *Kotlin*

*Not affiliated with Anthropic*

</div>