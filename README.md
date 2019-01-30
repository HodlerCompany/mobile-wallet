# Qredit Mobile


> A Wallet for Everyone

Qredit mobile wallet is a hybrid application (using the same codebase for Android and iOS which helps with coordinated development). Created using Ionic framework and ARK’s [TypeScript API](https://github.com/ArkEcosystem/ark-ts) to interact with the Qredit network via your mobile phone, anytime, anywhere (as long as you have an internet connection).

## Download

- [Google Play](https://play.google.com/store/apps/details?id=io.qredit.wallet.mobile)
- [APK Release](https://github.com/HodlerCompany/mobile-wallet/releases)


## Features

- Import your existing passphrase (import by QR Scanner or write/paste your passphrase).
- Generate a new passphrase.
- Encrypt access to your profile with a custom 6 digit PIN (AES256+PBKDF2).
- Most transaction types are available: send, receive, vote, unvote, register a delegate.
- Option for additional profiles (separate profiles for different Qredit addresses or networks).
- Option to add contacts and easily transact with them.
- Total balance of your combined Qredit addresses.
- Wallet backup - input your selected PIN to decrypt your wallet and gain view of your private data.
- Change PIN - if you want to change your encryption/decryption PIN you can easily do so..
- Clear Data — you can clear all your data from the phone.
- Overview of network status with an option to change peer.
- Current market value, along with weekly movements.

## Build

Install the dependencies and build the APK:

```bash
$ npm install -g ionic cordova@7.1.0
$ npm install
$ ionic cordova prepare android
$ ionic cordova plugin rm cordova-plugin-console
$ ionic cordova build --release android
```

Sign (android) APK:

```bash
$ jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore /platforms/android/app/build/outputs/apk/release/my-release-key.keystore /platforms/android/app/build/outputs/apk/release/app-release-unsigned.apk HodlerCompany
$ zipalign -v 4 /platforms/android/app/build/outputs/apk/release/app-release-unsigned.apk Qredit.apk
```

Run on device:

```bash
$ ionic cordova run ios
$ ionic cordova run android
```

Debug in browser:

```bash
$ npm run ionic:serve
```

## Testing

To run the unit tests:
```bash
$ npm test
```

To run the unit tests and watch them:
```bash
$ npm run test:unit
```

To run the unit tests and generate a coverage report:
```bash
$ npm run test:coverage
```

To run the E2E (end to end) tests:
```bash
$ npm run test:e2e
```

## Security

If you discover a security vulnerability within this application, please send an e-mail to nayiem@qredit.io. All security vulnerabilities will be promptly addressed.

## Qredits to the ARK Team!

- [Lúcio Rubens](https://github.com/luciorubeens)
- [Alex Barnsley](https://github.com/alexbarnsley)
- [All Contributors](../../contributors)

## License

[MIT](LICENSE) © [QreditPlatform](https://qredit.io)
[MIT](LICENSE) © [ArkEcosystem](https://ark.io)
