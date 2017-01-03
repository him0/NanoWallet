# Nano Wallet (Electron Application Branch) #

### How to use Nano Wallet ? ###

After downloading the latest version here https://forum.nem.io/t/nano-wallet-beta-1-1-11-5-000-xem-bug-bounty/2791, extract the NanoWallet folder from the archive, then you can simply click on start.html to open the app in your default browser. No installation or local server needed.

### How to import NCC wallet ? ###

Open NCC and your wallet, clicking on user icon should reveal a drop-down menu with "Export to ligthwallet".
Once your have your wallet (.json format), open Nano and import it from the login page. It'll ask for an upgrade and trigger the download of your updated wallet.
Do not delete your old NCC wallet and keep it safe somewhere.

### Imported accounts that are already harvesting using NCC ###

NCC is using a different way to generate the remote associated with an account. Nano Wallet uses BIP32 to generate it deterministically and make everything easier. In order to manage and monitor harvesting, you'll need to deactivate the old remote account from NCC and activate your new remote account from Nano. Alternatively you can use a custom delegated public key in Nano Wallet importance transaction page.

**/!\ Main network: Please note that if you are part of the Supernodes program you'll need to re-enroll your node using your new delegated public key.**

### How to update Nano Wallet ? ###

Before update make sure that you don't have any wallets stored into the NanoWallet folder (you can place them anywhere you want). Then, just delete old version and unzip new version.

# Developers #

### Build from source ###

1) Install gulp

<pre>npm install -g gulp-cli</pre>

2) Open a console to the path of the NanoWallet folder and install all the needed dependencies

<pre>npm install</pre>

3) Build:

<pre>gulp</pre>

### Build Electron App ###

1)pack the electron applications(mac, win, linux)

<pre>npm run pack</pre>

2)build the electron application installers(mac, win)

<pre>npm run build</pre>

3)zip the electron applications

<pre>npm run archive</pre>

### Known issues ###

- Sometimes, depending the node used, unconfirmed data to sign is not incoming from websocket
