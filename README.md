<h1>Setting up a full Bitcoin node, conducting an air-gapped transaction & getting familiar with the Lightning network</h1>

<h2>Introduction</h2>
We will be installing the BTC node on an Raspberry Pi 4 using the Umbrel OS, there are several benefits while running a personal full Bitcoin node:

- Enhanced Security: Running your own full node allows you to verify and validate your own transactions, reducing the risk of relying on third-party services.
- Privacy: By running a full node, you don't have to rely on external servers for transaction information, which enhances your financial privacy.
- Supporting the Network: Running a full node contributes to the decentralization and resilience of the Bitcoin network. The more nodes there are, the more robust the network becomes.
- Trustless Transactions: You can independently verify the validity of transactions without relying on external sources. This aligns with the principle of trustlessness, a core aspect of Bitcoin.
- Learning Experience: Running a full node can be an educational experience, helping you understand the inner workings of the Bitcoin network and blockchain technology.


<h2>Getting the hardware necessary for the project:</h2>

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






<br />
