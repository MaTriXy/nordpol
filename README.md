![Nordpol icon](/nordpol_super_secret_nfc_project.png?raw=true)
# Fidesmo Nordpol - The Android Support Library for NFC

## Goal of the project
To make it as easy as possible to communicate with a NFC device using ISO 14443-4 commands. Specifically we are targeting devices that communicates using ISO 7816-4 APDUs.

## Rationale
Communicating with NFC devices using Android can sometimes be a bit challenging. There is both the new reader mode and the old intent based method. When doing real processing on the card, timeouts starts being an issue and several of the default values require some tweaking. On top of this, on some devices the NFC implementation require some quirks to work properly. We have gathered up our experience from several years of working with NFC on the Android platform into this library.

## Usage

To include the project into your gradle android build:
```
repositories {
    ...
    maven {
        url 'http://releases.marmeladburk.fidesmo.com'
    }
}
dependencies {
    ...
    compile group: 'com.fidesmo', name: 'nordpol-android', version: '0.1.5', ext: 'aar', transitive: true
}
```
## API

TBD

## Building

We use SBT for building. Get it
[here](http://www.scala-sbt.org/download.html)

The android subproject expects a local.properties file that points to
the Android SDK. So to build you need to create the file
`android/local.properties` (relative to the root directory of the
repository) containing the following:

On UNIX
```
sdk.dir = /path/to/android/sdk
```

On Windows
```
sdk.dir = Z:\\path\to\android\sdk
```

## Contributions

Additions, bugfixes and issues are very welcome. Added code should be
formatted and structured according to [Googles
styleguide](http://google.github.io/styleguide/javaguide.html). A pull
request should pass the Travis CI before it is merged. If possible
a pull request should be rebased to the most recent master
commit. Don't forget to add yourself to the list of contributors below.

Thanks for your contributions:

- [adriaan-telcred](https://github.com/adriaan-telcred)

## Used by

![Fidesmo logo](/fidesmo-logo.webp?raw=true)
[Fidesmo](https://play.google.com/store/apps/details?id=com.fidesmo.sec.android)
![Ledger Wallet logo](/ledger-wallet-logo.webp?raw=true)
[Ledger Wallet](https://github.com/LedgerHQ/ledger-wallet-android)
