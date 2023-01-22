# Kali NetHunter (Rootless Edition) - Kali Linux CLI and KeX using Termux

[Kali NetHunter](https://www.kali.org/get-kali/#kali-mobile)) is a Mobile Penetration Testing Platform, and the [rootless edition](https://www.kali.org/docs/nethunter/nethunter-rootless/) allows for maximum flexibility with no commitment.

_For use on **unmodified stock Android phones without voiding the warranty**!_

[![Termux Menu](../images/010-NH-Rootless-Installation_Start_s.jpg)](../images/010-NH-Rootless-Installation_Start.jpg)

[![KeX](../images/020-NH-Rootless-KeX_s.jpg)](../images/020-NH-Rootless-KeX.jpg)

## Prerequisite:

- Android Device (Stock unmodified device, no root or custom recovery required)

## Installation:

- Install the **NetHunter-Store app** from: <https://store.nethunter.com/>
- From the Kali NetHunter Store, install **Termux**, **NetHunter-KeX client**, and **Hacker's keyboard**
  _Note: The button "install" may not change to "installed" in the store client after installation - just ignore it. Starting termux for the first time may seem stuck while displaying "installing" on some devices - just hit enter._
- Open **Termux** and type:

<!-- https://offs.ec/2MceZWr -> https://gitlab.com/kalilinux/nethunter/build-scripts/kali-nethunter-project/raw/master/nethunter-rootless/install-nethunter-termux -->

```bash
termux-setup-storage
pkg install wget
wget -O install-nethunter-termux https://offs.ec/2MceZWr
chmod +x install-nethunter-termux
./install-nethunter-termux
```

## Usage:

Open Termux and type one of the following:

<!-- Make sure `./install-nethunter-termux` is in sync -->

| Command                   | To                                                      |
| ------------------------- | ------------------------------------------------------- |
| `nethunter`               | Start Kali NetHunter command line interface             |
| `nethunter kex passwd`    | Configure the KeX password (only needed before 1st use) |
| `nethunter kex &`         | Start Kali NetHunter Desktop Experience user sessions   |
| `nethunter kex stop`      | Stop Kali NetHunter Desktop Experience                  |
| `nethunter <command>`     | Run `<command>` in Kali NetHunter environment           |
| `nethunter -r`            | Start Kali NetHunter cli as root                        |
| `nethunter -r kex passwd` | Configure the KeX password for root                     |
| `nethunter -r kex &`      | Start Kali NetHunter Desktop Experience as root         |
| `nethunter -r kex stop`   | Stop Kali NetHunter Desktop Experience root sessions    |
| `nethunter -r kex kill`   | Kill all KeX sessions                                   |
| `nethunter -r <command>`  | Run `<command>` in Kali NetHunter environment as root   |

_Note: The command `nethunter` can be abbreviated to **`nh`**._

_Note: If you ran KeX in the background (`&`) **without having set a password**, you will need to bring it back to the foreground (i.e. via `fg <job id>`) then prompted to enter the password, finally you can then send it to the background again (via `Ctrl + z` and `bg <job id>`)_

To use KeX, start the KeX client, enter your password and click connect.

_Note: For a better viewing experience, enter a custom resolution under "Advanced Settings" in the KeX Client_


Sun May 29 22:51:35 UTC 2022
