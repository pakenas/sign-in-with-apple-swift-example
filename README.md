#  [Sign in with Apple](https://developer.apple.com/sign-in-with-apple/) Example App [![](https://img.shields.io/twitter/url?url=https%3A%2F%2Fgithub.com%2FGetStream%2Fsign-in-with-apple-swift-example)](https://twitter.com/intent/tweet?text=Want%20to%20implement%20Sign%20in%20with%20Apple%20in%20your%20iOS%20app%3F%20Learn%20how%3A&url=https%3A%2F%2Fgithub.com%2FGetStream%2Fsign-in-with-apple-swift-example)

<img align="right" src="meta/anim.gif" width="40%" />

## 📚 Tutorial

This repository contains the completed iOS and Node.js projects following the [Adding Sign in with Apple to your iOS App](https://getstream.io/blog/adding-sign-in-with-apple-to-your-ios-app/) tutorial. You should read it before trying to run this project as it contains it may contain useful information not present in this README.

## ℹ️ About this repository

This repository is built on top of this [iMessage Clone repository](https://github.com/getstream/stream-imessage-clone). By cloning that repository and following the tutorial, you will arrive at a similar state to this one.

## ⚙️ Setup

### Configuration

You should place your [Stream Chat](https://getstream.io/chat) and [Apple Developer](https://developer.apple.com) credentials in [`backend/index.js`](backend/index.js#L7-L16). Make sure to also change the IP address in [`iMessageClone/Authentication.swift`](iMessageClone/Authentication.swift#L39) with the IP and port where the backend is running.

For more information on the Apple Developer credentials you need and how to get them, see the [SETUP.md](https://github.com/ananay/apple-auth/blob/master/SETUP.md) for `apple-auth`.

### Dependencies

Dependencies are included, but if you need to make any changes, use CocoaPods in the root folder:

```bash
$ pod install --repo-update
```

And for the backend, use Yarn or NPM in the `backend` folder:

```bash
$ yarn install
```
or

```bash
$ npm install
```

### Running

#### Backend
To run the backend, you need Node.js 10+, and execute the command `node index.js` in the `backend` folder.

#### iOS
To run the iOS project, you need Xcode 11+ and a real iOS 13 device signed in with an Apple ID and Two-Factor Authentication enabled. Sign in with Apple does not work on simulators!

## 🔗 Helpful Links

- [Build an iMessage Clone with The Stream Chat iOS SDK](https://getstream.io/blog/build-imessage-clone/)
- [Stream Chat iOS Tutorial](https://getstream.io/tutorials/ios-chat/)
- [Stream Chat iOS Repo](https://github.com/GetStream/stream-chat-swift)
- [Stream Chat iOS Docs](http://getstream.io/chat/docs?language=swift)

## 🔎 Troubleshooting

### AKAuthenticationError 7026
You forgot to add the Sign in with Apple capability.

### ASAuthorizationAppleIDProvider.getCredentialState fails with .notFound.
Sign in with Apple won't work on a simulator. You must use a real device.

