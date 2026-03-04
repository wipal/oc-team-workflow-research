# 📱 Mobile App Project Template

## Project Type Information

| Field | Value |
|-------|-------|
| **Type** | Mobile Application |
| **Complexity** | Medium / High |
| **Team Size** | 3-10 members typical |

---

## 1. Common Roles

| Role | Platform | Responsibilities |
|------|----------|------------------|
| **Mobile Dev** | Claude Code | App development |
| **BE Developer** | Claude Code | API, Backend |
| **UI/UX Designer** | Human/AI | Design, Prototypes |
| **QA Engineer** | Claude Code | Testing |
| **DevOps** | OpenClaw | CI/CD, Deployment |
| **PM** | Human | Project management |

---

## 2. Tech Stack Options

### Cross-Platform (Recommended)
| Option | Use Case | Skills Required |
|--------|----------|-----------------|
| **React Native** | iOS + Android | React, Native modules |
| **Flutter** | iOS + Android | Dart, Flutter SDK |
| **Expo** | Quick development | React Native, Expo SDK |

### Native
| Option | Use Case | Skills Required |
|--------|----------|-----------------|
| **Swift** | iOS only | Swift, SwiftUI |
| **Kotlin** | Android only | Kotlin, Jetpack Compose |

### Backend
| Option | Use Case |
|--------|----------|
| Firebase | BaaS, Quick setup |
| Supabase | Open source BaaS |
| Custom API | Full control |

---

## 3. Deployment Options

### App Stores
| Store | Requirements | Time |
|-------|--------------|------|
| **Apple App Store** | Apple Dev Account ($99/yr) | 1-7 days review |
| **Google Play** | Google Dev Account ($25 once) | 1-3 days review |

### CI/CD for Mobile
| Option | Purpose |
|--------|---------|
| **Expo EAS** | React Native builds |
| **Codemagic** | Flutter builds |
| **Bitrise** | Multi-platform |
| **GitHub Actions** | Custom pipelines |

---

## 4. Infrastructure Setup

### Development
```yaml
requirements:
  - Node.js 18+
  - Xcode (for iOS)
  - Android Studio (for Android)
  - Expo CLI / React Native CLI
```

### Signing & Certificates
```yaml
ios:
  - Apple Developer Certificate
  - Provisioning Profiles
  - App Store Connect API Key

android:
  - Keystore (signing key)
  - Google Play Console Account
```

---

## 5. Credentials Needed

| Credential | Purpose | Storage |
|------------|---------|---------|
| Apple Dev Account | iOS builds | Secure vault |
| Signing Keystore | Android builds | Secure vault |
| API Keys | Backend services | .env |
| Push Notification Keys | Notifications | Server config |
| App Store Connect API | CI/CD | GitHub Secrets |

---

## 6. Git Branch Strategy

```
main (production)
  └── develop
        ├── feature/xxx
        ├── bugfix/xxx
        └── release/x.x.x
```

### Commit Convention
```
[Agent-Name] type: message

Examples:
[Mobile-Dev] feat: add push notifications
[BE-Dev] feat: add user API
[Designer] design: update onboarding screens
```

---

## 7. Project Structure

```
project/
├── mobile/
│   ├── src/
│   ├── assets/
│   ├── tests/
│   └── app.json
├── backend/ (if custom)
│   ├── src/
│   └── package.json
├── docs/
│   └── meeting-notes/
├── design/
│   └── figma-link.md
└── README.md
```

---

## 8. Meeting Notes

All meetings stored in: `/docs/meeting-notes/`

Format: `YYYY-MM-DD-[topic].md`

---

## 9. Quick Start Checklist

- [ ] Choose tech stack (React Native/Flutter)
- [ ] Create GitHub repo
- [ ] Setup Apple Developer account
- [ ] Setup Google Play Console
- [ ] Configure signing certificates
- [ ] Setup CI/CD pipeline
- [ ] Create .env from template
- [ ] Setup meeting notes folder
- [ ] Add team members

---

*Template by Hina 🍀*