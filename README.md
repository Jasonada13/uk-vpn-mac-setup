# UK VPN setup for Mac

Download and install your prepared London VPN connection. No GitHub account is needed to download it.

**[Download the Mac setup kit](https://github.com/Jasonada13/uk-vpn-mac-setup/releases/latest/download/UK-VPN-for-Mac.dmg)** · [All downloads](https://github.com/Jasonada13/uk-vpn-mac-setup/releases/latest)

The download is about 112 MB. It is a password-protected disk image containing the official AmneziaVPN installer, your private connection file and offline instructions. Get the download password directly from Jason.

## 1. Open the download

1. On your Mac, click **Download the Mac setup kit** above. Do not use GitHub's green **Code → Download ZIP** button: that only downloads this guide.
2. Open `UK-VPN-for-Mac.dmg` from Downloads.
3. Enter the **download password Jason sends you privately**. This is different from your Mac login password.
4. In Finder, open the mounted **UK VPN Setup** disk. Copy `UK-London-Partner.vpn` somewhere you can find it, such as Downloads.

## 2. Install AmneziaVPN

You need **macOS 14 Sonoma or newer**. The included installer supports Apple Silicon (including M4) and Intel Macs.

1. Open `AmneziaVPN-macOS.pkg` from the mounted disk and follow the installer.
2. If macOS asks, use **your own Mac password or Touch ID** to approve installation.
3. Open AmneziaVPN from Applications. Fully quit it with **Command-Q**, then reopen it once. The official guide also recommends restarting your Mac after installation.

The `.dmg` is just the password-protected delivery container. The app itself uses a normal `.pkg` Mac installer.

If AmneziaVPN 5.0.3.0 or a newer stable release is already installed, skip this section.

## 3. Import and connect

1. In AmneziaVPN, choose **Get Started** or **+**.
2. Choose **Connection settings file**, select `UK-London-Partner.vpn`, and continue.
3. Select **UK London** and click **Connect**. Approve normal macOS VPN permission prompts if they appear.
4. Open [this connection check](https://www.cloudflare.com/cdn-cgi/trace). It should show `loc=GB`; the expected IP address is in `START-HERE.txt` inside your download.
5. Try your application website, including login and a document upload. Also check reconnecting after the Mac wakes from sleep.

You do not need an Oracle account, a server password, a paid Amnezia subscription or Jason's Mac to stay online. When finished, click **Disconnect** in AmneziaVPN. After importing the profile, you can eject the setup disk in Finder.

## If something goes wrong

- **GitHub shows a page instead of downloading:** open [All downloads](https://github.com/Jasonada13/uk-vpn-mac-setup/releases/latest), expand **Assets**, and select `UK-VPN-for-Mac.dmg`. The automatically generated Source code downloads do not contain the kit.
- **The disk image rejects the password:** copy it exactly, including hyphens, without surrounding spaces. Ask Jason privately if needed.
- **Error 1200 or the app freezes:** fully quit with Command-Q and reopen. If it is unresponsive, press Command-Option-Escape and force-quit **AmneziaVPN only**, then reopen it. Your connection file stays available in the disk image.
- **The VPN will not connect:** first check ordinary internet access and automatic date/time. Tell Jason the error code and whether you are on Wi-Fi or a mobile hotspot.
- **A download is interrupted:** retry the release download. Being able to open GitHub pages does not always mean its download servers are reachable on the same network.

Keep the download password and `.vpn` file private; they grant use of this VPN. Do not post them in GitHub issues or comments. The encrypted kit contains a guest connection only, with no server administration keys. Connectivity and speed must be tested on your own network.

## Optional speed check

Once connected, open [Cloudflare Speed Test](https://speed.cloudflare.com/) and privately send Jason the download speed, upload speed and latency. A UK-side connection test cannot predict performance from your network.

## Software and verification

The package is the unmodified official **AmneziaVPN 5.0.3.0** macOS installer. Its signature and Apple notarization were checked, and its SHA256 matched the upstream GitHub release asset. The upstream filename contains `x64`, but its app binaries support both Apple Silicon and Intel.

[Official release](https://github.com/amnezia-vpn/amnezia-client/releases/tag/5.0.3.0) · [macOS installation guide](https://docs.amnezia.org/documentation/instructions/installing-app-on-macos/) · [File import guide](https://docs.amnezia.org/documentation/instructions/connect-via-config/) · [Source and licence information](THIRD-PARTY-NOTICES.md)

`SHA256SUMS.txt` contains the checksums for the encrypted download and the installer inside it.
