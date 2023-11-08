<h1>Setting up a full Bitcoin node, conducting an air-gapped transaction & getting familiar with the Lightning network</h1>

<h2>Introduction</h2>
We will be installing the BTC node on an Raspberry Pi 4 using the Umbrel OS, there are several benefits while running a personal full Bitcoin node:

- Enhanced Security: Running your own full node allows you to verify and validate your own transactions, reducing the risk of relying on third-party services.
- Privacy: By running a full node, you don't have to rely on external servers for transaction information, which enhances your financial privacy.
- Supporting the Network: Running a full node contributes to the decentralization and resilience of the Bitcoin network. The more nodes there are, the more robust the network becomes.
- Trustless Transactions: You can independently verify the validity of transactions without relying on external sources. This aligns with the principle of trustlessness, a core aspect of Bitcoin.
- Learning Experience: Running a full node can be an educational experience, helping you understand the inner workings of the Bitcoin network and blockchain technology.


<h2>Getting the hardware necessary for the Node:</h2>

Raspberry Pi
  
- All variants work but we took the 8 GB RAM for maximum performance
<img src="https://i.imgur.com/4fM28X8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Storage drive
  
- We need a large enough SSD, for running a full node it is recommended to pick a 2 TB SSD drive.
<img src="https://i.imgur.com/xdp9fXN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Storage drive enclosure
  
- To link the storage drive to the Raspberry Pi using a USB connection
<img src="https://i.imgur.com/XGcuoQI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

16GB+ microSD
  
- The microSD card exclusively serves for operating Umbrel OS, while your apps and data reside on the storage drive.
  
Power supply
  
- Ensure to utilize the official Raspberry Pi power supply to mitigate any unforeseen issues.

Ethernet cable
  
- To link the Raspberry Pi to your internet router.
  
Case
  
- Encase and shield your new personal server with a durable case.
<img src="https://i.imgur.com/RaTAmjg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h2>Setup process</h2>

Once all the hardware is assembled we can setup the OS on the Raspberry Pi.

Get umbrelOS

- Retrieve Umbrel OS for Raspberry Pi on your computer. https://umbrel.com/#umbrelos

Download Balena Etcher

- Download and set up Balena Etcher on your computer. This is essential for flashing the Umbrel OS file, downloaded in the previous step, onto the microSD card. https://etcher.balena.io/ 

Plug the microSD card into your computer

- If your computer lacks a card reader, you may require one.
<img src="https://i.imgur.com/zz98OAN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Flash umbrelOS

- Launch Balena Etcher and use it to flash the downloaded Umbrel OS zip file onto the microSD card.
<img src="https://i.imgur.com/JqNDl8U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Insert the microSD card in the Pi

- Once the flashing process is complete, take out the microSD card from your computer and insert it into the Raspberry Pi.
<img src="https://i.imgur.com/Q5rLkxF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Connect the SSD

- Place the SSD into its enclosure and connect it to one of the two USB 3.0 ports (indicated by a blue color) on the Raspberry Pi. Note that unless the SSD was previously employed for running Umbrel, any existing data on it will be automatically erased upon powering up the Raspberry Pi.
<img src="https://i.imgur.com/7iLSsTw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Connect to your router and power up

- Link the Raspberry Pi to your internet router by connecting one end of the Ethernet cable to the Pi and the other end to any available port on your router. Then proceed to power up the Raspberry Pi by connecting the power supply.
<img src="https://i.imgur.com/jpEBVKq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

After a few minutes you will be able to access your Umbrel at http://umbrel.local from any device connected to the same network as the Raspberry Pi. Turning a VPN off will help if you have difficulty connecting. Another way to connect if http://umbrel.local does not work is discovering your Umbrel's IP address with Angry IP https://angryip.org/ and input it into the browser instead of 'umbrel.local'.

Once logged in I suggest setting up Two-factor auth (2FA) in settings.

You can them proceed and install the necessary apps: bitcoin core node, electrum server and lightning node. This can take some time to sync.
<img src="https://i.imgur.com/cKDzMK8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<h2>Hardware wallet(Coldcard MK4) setup:</h2>

There could be multiple choices for a hardware wallet but in this case I believe the MK4 from Coinkite is the best and most advanced one made for true sovereign individuals.
<img src="https://i.imgur.com/Kzv0PYZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Other than the USB-C connector, optional NFC and massive RAM for multisig, there are several benefits for using the MK4:

- Security Features: The Coldcard Mk4 is designed with a focus on security, incorporating features like PIN protection, passphrase support, and a secure element.
- Air-Gapped Operation: It operates in an air-gapped mode, enhancing security by keeping the device physically disconnected from the internet.
- PSBT Support: The Coldcard Mk4 supports Partially Signed Bitcoin Transactions (PSBT), allowing for enhanced flexibility in transaction signing.
- Open Source Firmware: The device's firmware is open source, providing transparency and allowing the community to review and contribute to the code.
- MicroSD Card Slot: It includes a microSD card slot for secure backup and recovery options, adding an extra layer of protection for your wallet.
- Compatibility: The Coldcard Mk4 is compatible with popular wallet software like Electrum and integrates well with the broader Bitcoin ecosystem.
- Tamper-Evident Packaging: The device comes with tamper-evident packaging, providing assurance that the hardware has not been compromised during shipping.
- Offline Key Generation: Private keys can be generated offline on the Coldcard Mk4, reducing the risk of exposure to online threats.
- Large Screen and Keypad: The device features a large screen and keypad, making it user-friendly for confirming transactions and entering PINs securely.
- U2F Authentication: It supports Universal 2nd Factor (U2F) authentication, adding an extra layer of security when accessing certain services.

COLDPOWER Adapter

- Supply power to your Coldcard and other low-power USB devices using a standard 9-volt battery, all without worrying about USB data issues.
<img src="https://i.imgur.com/BIFET4A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

9-volt battery

- To energize the adapter
<img src="https://i.imgur.com/4r4Tbm4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Power-Only USB-C Cable

- A magnetic power-only cable, ensures the secure powering of your COLDCARD Mk4, guaranteeing the absence of connected data lines.
<img src="https://i.imgur.com/ZgTTLIz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Industrial MicroSD

- Adequately sized solely for supporting small backups and transaction signing—illustrated here with a 4GB example.
<img src="https://i.imgur.com/EiYxIcx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Once assembled

<img src="https://i.imgur.com/AXwHDI6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Follow instruction to verify the sealed number and if it matches 
<img src="https://i.imgur.com/HyDQ5eI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Initial setup you will be prompted with pins and anti-phishing code words so you know each time you enter the device it was not tempered with. 

The next step is to generate a new BIP39 seed phrase.
<img src="https://i.imgur.com/hFhNk5i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

I personally suggest using the dice roll option. Once generated you need to backup your newly generated seed phrase, Coinkite offers an paper version. 

<img src="https://i.imgur.com/NMPWPoP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

You can also explore additional options such as metal plates that are fire resistant but the absolute favorite has to be the steel washers as it is compact and can be kept in multiple places. Below is an example of how it looks once completed.

<img src="https://i.imgur.com/UEGrKUa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Even if found by someone you have to have a passphrase over your seed phrase, meaning a 13th(if 12 words) or 25th(if 24 words) password over your seed phrase. This passphrase can be like a real password that you have to remember and by adding that it will generate a completely new set of addresses and a new master key fingerprint.

<img src="https://i.imgur.com/ArbyBMO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Make sure you write down both master key fingerprints for the initial seed phrase and for the passphrase generated wallet. You can use the seed phrase as a decoy if needed or create as many decoys as you need with different passphrases using the same initial seed phrase.


<h2>Connecting on chain Bitcoin wallet</h2>

We will be using Sparrow desktop wallet software to interact with the hardware and play with transactions

First we will be going into the Advanced options → Export wallet 

<img src="https://i.imgur.com/QEWvbi0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Select Generic JSON

<img src="https://i.imgur.com/1FA5fJg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Once you press agree on all the demands, it will write a JSON file on the micro SD card

<img src="https://i.imgur.com/7OEzfr3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

You can unplug the chip and attach it to your desktop. Once sparrow wallet open you click on new wallet

<img src="https://i.imgur.com/ak7ET8R.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Select the Airgapped Hardware wallet option

<img src="https://i.imgur.com/b7zKAIR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Coldcard option

<img src="https://i.imgur.com/kCYnyia.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Since we have our own node we can link it and use it directly for broadcasting transactions.

We are linking it thru Electrum server that we set previously and apply our TOR .onion address and test the connect to see if everything is synced

<img src="https://i.imgur.com/2lOaylR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

To find this information, you can go inside of your Umbrel node in option find the following page where you could get your .onion address by selecting TOR.

<img src="https://i.imgur.com/qKJGLwf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Interact via air gapping in order to receive or send transactions

Here lies all the magic behind the coldcard wallet, as you know we have not plugged this device into anything connected to the internet, all it has been connect to is a 9v battery. 

I will show how we can send funds from it to some other bitcoin wallet. 

We can press on send and select an address to send to, the amount and fees. Then we press Create Transaction

<img src="https://i.imgur.com/kR7sUC5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The next step would be to press Finalize Transaction for Signing

<img src="https://i.imgur.com/OKhhJke.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

At this point, we can not just sign since the keys are not on this computer, therefore we need to save the transaction on the SD card so we can get it approved inside the MK4 Coldcard

<img src="https://i.imgur.com/uw15KJi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

This wills save as .psbt file type standing for Partially Signed Bitcoin Transaction

<img src="https://i.imgur.com/2tZ0OEw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Once back inside the coldcard, we can select Ready to Sign

<img src="https://i.imgur.com/88XWXUx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

It will automatically detect that there is a transaction or multiple ones that needs signing, we select the one we need and accept

<img src="https://i.imgur.com/3Tvg8zE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

This will update the .psbt file as signed. It can then we loaded inside the sparrow wallet

<img src="https://i.imgur.com/IZvbSHr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

We can then see that the signature was accepted and we can proceed to Broadcast the transaction on the blockchain

<img src="https://i.imgur.com/WLHvoWw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>










<br />
