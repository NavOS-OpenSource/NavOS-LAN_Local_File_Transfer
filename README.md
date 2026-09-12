# NavOS - LAN Local File Transfer

Smart, lightweight file transfer between devices over your local network. NavOS is a self-hosted file transfer and device-sharing application designed to make moving files between your PC, phone, tablet, and other devices on the same network simple. No cloud storage is required. No account is required. Your files stay on your own network.

<img width="335" height="335" alt="Picture1" src="https://github.com/user-attachments/assets/c4f820d3-bdae-45f3-ac2d-6054b3fc98cd" /><img width="335" height="335" alt="Picture1_rev" src="https://github.com/user-attachments/assets/ea80239e-1986-4093-ae8c-338fe4f53bd0" />

---

# Windows Quick Start

If you are using Windows, starting NavOS is simple.

## 1. Download NavOS

Clone this repository to your computer.

    git clone https://github.com/Xx7Navin7xX/NavOS-LAN_Local_File_Transfer.git

Or download the repository as a ZIP file from GitHub and extract it.

---

## 2. Install Python

NavOS requires Python.

Download Python from:

https://www.python.org/downloads/

During installation, make sure Python is added to your PATH.

You can check the installation by opening Command Prompt and running:

    python --version

You should see a Python version number.

---

## 3. Start NavOS

Open the NavOS folder.

You can start the server from Command Prompt:

    python server.py

If the project includes the Windows launcher, you can also start it using:

    Start_windows.bat

---

## 4. Open NavOS

After starting the server, the console will display the address that can be opened in a browser. To connect your phone, make sure your phone and computer are connected to the same local network. If QR sharing is available on the dashboard, Scan it using your phone camera. NavOS opens in your phone browser. No manual IP address entry is required. you can also use this methon to open NavOS in other systems also.

<img width="1263" height="162" alt="image" src="https://github.com/user-attachments/assets/8cfc8de7-1aa3-4e97-a1e3-3bafed3fab5d" />

---


## What is NavOS?

NavOS turns your computer into a private file-sharing server that other devices can access through a web browser.

Once NavOS is running, open the displayed network address on another device and you can:

- Upload files from your phone or PC
- Download files from the server
- Upload and download entire folders
- Transfer large files with resumable uploads
- Share files using QR codes
- Search your shared files
- Preview supported files directly in the browser
- Stream supported media
- Share clipboard content between devices
- Discover other NavOS servers on your local network
- Monitor transfers and server activity
- Protect the server with PIN authentication
- Use HTTP or HTTPS/TLS networking
- Manage files and folders from the web interface

NavOS is designed primarily for trusted local networks such as your home, office, laboratory, workshop, or personal device network.

---

# Features

## File Transfer

### Upload files

Upload one or multiple files directly from the web interface.

Supported upload features include:

- Multiple-file selection
- Drag and drop
- Browser paste support
- Upload progress
- Upload speed information
- Transfer status
- Concurrent uploads
- Pause and resume
- Cancel uploads
- Resumable uploads
- SHA-256 integrity verification

# Media Streaming

Supported audio and video files can be streamed directly from NavOS. 

HTTP Range requests are supported so compatible media players and browsers can request portions of a file instead of downloading the entire file at once. This makes browser-based playback more practical for large media files.

# Clipboard Sharing

NavOS includes a cross-device clipboard system.

You can use it to move text and other useful information between devices without sending yourself messages or using cloud services.

Clipboard entries can be used for things such as:

- Text
- Links
- Commands
- Notes
- OTP codes
- JSON
- Other short pieces of information

The clipboard system includes:

- Clipboard history
- Copying entries
- Editing entries
- Deleting entries
- Expiration
- System clipboard integration

For example, you can copy a command on your PC and quickly access it from your phone through NavOS.

---

# LAN Server Discovery

NavOS can automatically discover compatible NavOS servers on the local network.

This can make it easier to find another computer running NavOS without manually entering its IP address.

The discovery system can provide information such as:

- Device/server name
- IP address
- Port
- Protocol
- Authentication state
- Server availability

Discovery uses the local network and does not require a cloud service.

<img width="1737" height="927" alt="image" src="https://github.com/user-attachments/assets/35b73460-233e-4229-909b-461c90dfbcf8" />

---

# HTTPS with a Custom Certificate

If you already have a certificate and private key, NavOS can be configured to use them.

Example:

    python server.py --https --cert path/to/certificate.pem --key path/to/private-key.pem

Keep private keys protected and never commit them to GitHub.

---

# Important Security Notes

## Do not expose NavOS directly to the internet without understanding the risks.

NavOS is designed around local network sharing. If you only need to transfer files between devices at home, keep the server accessible only from your LAN. Use your firewall to control which devices can reach the server when necessary.

NavOS is designed primarily for use on trusted local networks.

Security features include:

- PIN authentication
- Protected dashboard access
- Authentication tokens
- Login protection
- Failed-login protection
- Protected file operations
- Path traversal protection
- ZIP path validation
- Symlink protection
- Upload path validation
- Resumable-upload validation
- Security configuration protection

---

# Privacy

NavOS is designed around local, self-hosted file transfer.

Your files are served directly from your own computer.

NavOS does not require cloud storage for normal file transfer.

The normal workflow is:

    Your Device
          |
          | Local Network
          v
    NavOS Server
          |
          v
    Shared Files

Your files remain on the computer running NavOS unless you explicitly transfer them to another device.

---

# Common Problems

## NavOS works on the PC but not on my phone

This is commonly caused by firewall or network isolation.

Some routers create separate networks for wireless clients or enable client isolation.

Make sure the phone is allowed to communicate with the computer on the local network.

---

## The browser says the connection is not secure

If HTTPS is enabled and NavOS is using a locally generated or self-signed certificate, your browser may display a certificate warning.

This is expected for certificates that are not issued by a public certificate authority.

Do not ignore certificate warnings on networks or devices you do not trust.

---

## Upload stopped

If a resumable upload is supported for the particular transfer, NavOS can continue the upload instead of starting over.

Check the upload status in the dashboard.

---

## A ZIP does not contain a symbolic link

This is intentional.

NavOS does not follow symbolic links when creating downloadable ZIP archives.

This prevents links from pointing outside the shared directory and exposing unintended files.

---

# Requirements

Typical requirements include:

- Windows, Linux, or another supported Python environment
- Python 3
- A modern web browser
- Local network connectivity for device-to-device access

No cloud account is required for normal operation.

---

# Support the Project

If NavOS is useful to you and you would like to support its development, you can use the support options provided in the application.

Available support methods may include:

- Razorpay
- PayPal
- UPI
- GitHub Sponsors
- Ko-fi

Support is completely optional, but it helps with continued development, testing, maintenance, and future improvements.

---

# Disclaimer

NavOS is provided as a self-hosted local-network application.

You are responsible for configuring your network, firewall, authentication, TLS certificates, shared files, and access permissions appropriately.

Do not expose the application to untrusted networks unless you understand and have appropriately addressed the additional security requirements.

---

## NavOS - LAN Local File Transfer

Smart, lightweight file transfer between devices over your local network.
