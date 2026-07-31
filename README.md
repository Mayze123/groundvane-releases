# Groundvane Releases

Distribution for [Groundvane](https://github.com/Mayze123), a native macOS ground station for ArduPilot aircraft. This repository carries the update feed and the signed archives, and nothing else — the source lives elsewhere and is private.

## Downloads

Each version is a [GitHub Release](../../releases) tagged `v<marketing>-<build>`, with the notarized `.zip` attached as an asset.

## Update feed

`appcast.xml` is served by GitHub Pages at
`https://mayze123.github.io/groundvane-releases/appcast.xml`

Installed copies read that URL directly and validate every download against an ed25519 public key compiled into the application. Replacing the feed is not sufficient to ship an update, and is not sufficient to compromise one.

## Publishing

Archives are uploaded to a Release **before** `appcast.xml` is pushed. A feed that names a file which is not yet uploaded advertises a download that 404s to everyone who checks in the interval.
