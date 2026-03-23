# Destiny - Least Authority
[Destiny - Least Authority](https://leastauthority.com/community-matters/destiny/#GetDestiny) 

 Destiny is an open source secure file transfer application that does not reveal identities – neither between participants nor towards the service provider.

Destiny was developed for and with Human Rights Organizations (HROs) as a free Privacy Enhancing Technology (PET) alternative which does not collect personal identifying information for file transfer. Funding for Destiny was made possible by a grant. Destiny is free to download and use.

![](https://leastauthority.com/wp-content/uploads/2022/09/Destiny-Icon-Only-1000x1000-1.svg)

Destiny uses the “[Magic Wormhole](https://github.com/magic-wormhole/magic-wormhole)” protocol. Magic Wormhole is designed to be an easy and private way to get a file safely from one device to another. Users can select a file on their device and share the one-time code with the intended recipient for safe delivery. No sign-up or log-in is needed. Files are sent in real-time. We don’t store your file and we minimize the data collection. Both users need to have the application installed and be online at the same time.

What Makes Destiny Secure?
--------------------------

![](https://leastauthority.com/wp-content/uploads/2022/09/identityless.png)

**Identity-less**

No need to disclose identity information (such as name, email address or phone number) to be able to transfer files.

![](https://leastauthority.com/wp-content/uploads/2022/09/endtoendencryption.png)

**End-to-End Encryption**

Files are end-to-end encrypted and only the sender and recipient can read them.

![](https://leastauthority.com/wp-content/uploads/2022/09/fullstrengthkeys.png)

**Full-strength Keys**

Although our codes are short and human-memorable, they are part of an online “Password Authenticated Key Exchange” (PAKE) which only allows a single guess – and yields a 256-bit full-strength symmetric key.

![](https://leastauthority.com/wp-content/uploads/2022/09/peertopeerfilesharing.png)

**Peer-to-Peer File Sharing**

Destiny attempts to make a direct network connection to the other party. If both parties are on the same local network they should connect without any traffic leaving that network. When this isn’t possible (e.g. if neither party has a public IP address) then our relay server is used.

If you would like to learn more about Destiny, including an overview of the application and its features, see our blog post marking the release of Destiny below.

Security Audit of Destiny
-------------------------

Following security best-practices, Least Authority hired an independent, third-party organization to conduct a security audit of Destiny. Radically Open Security was selected via a competitive bidding process and the audit and remediation were completed prior to the release of Destiny. The full audit report is available below.

How to Download and Use Destiny
-------------------------------

Walk through the onboarding process (this will only appear once, when you first download the application).

Click on the + sign or drag and drop a file into the dotted zone to select a file to send.

The application will automatically generate a one-time code. Pass on the code to the intended recipient verbally, digitally, or by any other means that you deem safe. For ease of use you can copy the code using the Copy button. Note that anyone with access to the code can receive your file.

The recipient can navigate to the Receive tab and enter the code in the “Enter Code Here” field and click the Next button.

Press Download to begin downloading the file to your device. If there are no interruptions or cancellations the file will be delivered successfully and you will see a screen that says “File download successful”. The page will also include information about where your file has been downloaded to.

The code is now no longer usable. No one else can receive the file with this code.

Magic Wormhole and Open Source
------------------------------

Magic Wormhole was originally presented at PyCon 2016 along with a Python implementation by Brian Warner. It is an implementation of a “PAKE” (Password Authenticated Key Exchange) that uses the resulting secure keys and a custom peer-to-peer protocol to transfer files.

Since then, implementations in several languages have emerged. We run our own “mailbox / rendezvous” and “transit relay” servers (different from the default ones). The Destiny app can interoperate with other implementations over these servers. Although we do not provide professional support for this, experts can direct their clients to use the mailbox / rendezvous server at wss://wormhole.app:4001/v1 and the transit relay at wss://wormhole.app:4003

We are also making further protocol improvements including “Dilation” to facilitate multiple transfers in both directions (as well as robust retries). Although the main use-case of magic wormhole is file-transfer, the core protocols can be used for any kind of streaming data over TCP. We are helping improve [the protocol specifications](https://github.com/magic-wormhole/magic-wormhole-protocols) and the reference Python implementations at:

*   [https://github.com/magic-wormhole/magic-wormhole](https://github.com/magic-wormhole/magic-wormhole)
*   [https://github.com/magic-wormhole/magic-wormhole-mailbox-server](https://github.com/magic-wormhole/magic-wormhole-mailbox-server)
*   [https://github.com/magic-wormhole/magic-wormhole-transit-relay](https://github.com/magic-wormhole/magic-wormhole-transit-relay)

All of our improvements to the code we’ve used as well as the new Destiny application are open-source. If you are interested in improving or auditing our implementation, please join us at [https://github.com/LeastAuthority/destiny](https://github.com/LeastAuthority/destiny)