# Blockstack update server

This repository hosts two files:
* the `macappcast.xml` file that our macOS app auto update framework uses
* the `appcast.xml` file that our old macOS app auto update framework used to use before the app was signed by Blockstack PBC.

## Adding a new version
To add a new version, you need to add an `<item>` tag filling in the appropriate info as below:

```
<item>
  <title>Blockstack v0.21.4</title>
  <description>
    <![CDATA[
    <p>This public alpha features:</p>
    <ul>
    <li>Fixes a Blockstack core bug</li>
    </ul>

    <p><strong>Known issues</strong></p>
    <p>These will be fixed in an upcoming release:</p>
    <ul>
    <li>Dropbox support is temporarily disabled in this release. It will be re-enabled in a future release.</li>
    </ul>
    <p><em>Names purchased in a pre-release version prior to v0.10.0 will need to be transferred to the production keychain location with a future tool.</p></em>
    ]]>
  </description>
  <pubDate>Tue, 5 December 2017 23:00:00 +0000</pubDate>
  <enclosure url="https://github.com/blockstack/blockstack-browser/releases/download/v0.21.4/Blockstack-for-macOS-v0.21.4.dmg" sparkle:shortVersionString="0.21.4" sparkle:version="78" length="64227382" type="application/octet-stream"/>
</item>
```


## Deploy

`firebase deploy`
