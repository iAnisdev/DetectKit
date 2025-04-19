# 🔍 DetectKit

**DetectKit** is a lightweight, open-source mobile toolkit for image-based detection using **any AI model**. Built with **React Native + Expo**, it supports real-time image upload and response rendering from customizable backend APIs. Use it with zero-shot models like **CLIP**, object detectors like **YOLO**, or even your own ML pipelines.

---

## 📱 Features

- 📸 Capture or upload image from mobile
- 🧠 Send to any backend for inference (REST API)
- 🔊 Read out the response via device text-to-speech
- 🧩 Modular and backend-agnostic design
- 🌐 Works in tunnel, LAN, or cloud environments
- 🧪 Built with React Native and Expo SDK

---

## 🔧 Backend API Contract

Your backend must expose the following endpoints:

1. GET `/health` - Health check endpoint
   - Returns: `{ "status": "ok" }`

2. POST `/upload` - Image upload endpoint
   - Accepts: `multipart/form-data` with a single field: `file` (the image)
   - Returns JSON response in this format:

```json
{
  "confidence": number,
  "message": string
}
```

## 📁 Project Structure

```
/app
  ├── components/
  ├── screens/
  ├── utils/
  ├── assets/
  └── App.js
```

## 🌐 Community & Contributions

Have a feature request or model idea? Open a pull request or start a discussion!

## 📄 License

MIT License © 2024 [Anis]

---

## 📋 Prerequisites

Before getting started, make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v18 or later)
- [pnpm](https://pnpm.io/) (v8 or later)
- [Expo CLI](https://docs.expo.dev/get-started/installation/) (v6 or later)

You can verify your installations with:

```bash
node --version
pnpm --version
npx expo --version
```

## 🚀 Quick Start

```bash
# 1. Clone the repo
git clone https://github.com/iAnisDev/detectkit.git
cd detectkit

# 2. Install dependencies using pnpm
pnpm install

# 3. Start the app
pnpm expo start
