# Furcha MR2 — downloads

Installers, firmware images and manuals for the **Furcha MR2 desktop RFID reader**
(13.56 MHz Mifare, USB HID keyboard).

Everything is published under [**Releases**](../../releases) — the latest build is
always at the top.

## What to download

| File | What it is |
|---|---|
| `ConfiguratorMR2-Setup-X.Y.exe` | Windows installer for the configurator. Self-contained: no .NET or drivers needed. |
| `ConfiguratorMR2-Setup-X.Y.zip` | The same installer inside a password-protected archive (password: `1234`), for mail systems that strip `.exe` attachments. |
| `mr2_00.00.0X.0Y.img` | Signed reader firmware image, flashed from the configurator. |
| `MR2_Reader_Manual_EN/RU/ET.pdf` | User manual — modes, Edit Reader, firmware update. |

## Firmware and configurator go together

A firmware release that changes the configuration protocol needs the matching
configurator, so **install the `.exe` and flash the `.img` from the same release**.
A mismatch usually shows up as empty or garbled data in the Edit Reader section.

## Updating the firmware, in short

1. Connect: **USB reader (MR2)** → select the reader → **Connect**.
2. Section **Boot Mode** → press **Boot Mode**. The reader reboots into its
   bootloader and re-appears in the list as *Furcha DownLoad Firmware Update*.
3. Select that entry → **Connect** → **FW update** → choose the `.img`.
   The configurator verifies the image (device model, integrity, Furcha
   signature) and shows its version before flashing.
4. Wait for 100 % — do not unplug. The reader restarts into the new firmware.

The full procedure, including what to do if the reader stays in boot mode, is in
the manual.

---

Source code lives in private repositories; this one carries the published builds
only.
