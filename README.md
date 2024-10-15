## Kali-Nethunter [non-root]:

[Kali NetHunter](https://www.kali.org/get-kali/#kali-mobile)) is a Mobile Penetration Testing Platform, and it allows for maximum flexibility with no commitment.

_For use on **unmodified stock Android phones without voiding the warranty**!_

## Screenshot:

![alt text](https://github.com/popeye0013/kali-nethunter-project/blob/main/NH-Rootless-KeX.png)

## Prerequisite:

- Android Device (Stock unmodified device, no root or custom recovery required)

## Installation:

- Install the **NetHunter-Store app** from: <https://store.nethunter.com/>
- From the Kali NetHunter Store, install **Termux**, **NetHunter-KeX client**, and **Hacker's keyboard**
  _Note: The button "install" may not change to "installed" in the store client after installation - just ignore it. Starting termux for the first time may seem stuck while displaying "installing" on some devices - just hit enter._
- Open **Termux** and type:

<!-- https://offs.ec/2MceZWr -> https://raw.githubusercontent.com/popeye0013/kali-nethunter-project/main/install-nethunter-termux -->

## Setting Up Our Environment:

Next up, we would need some packages which we would need during the installation process.

First, update and upgrade the system with :
```
pkg update && pkg update -y
```

Next up we need to setup our system so that we can access the files created by Termux outside of our Termux session as well. This can be done with :
```
termux-setup-storage
```

Once you have granted the required Permissions, finally install the required packages with :
```
pkg install wget fish
```

Once done, we can proceed to the actual installation step.
Next we need to fetch and execute a script which will install Kali Linux for us. To fetch the script, type:
```
wget https://raw.githubusercontent.com/popeye0013/kali-nethunter-project/main/install-nethunter-termux
```

Now, we need to make the script executable and run it with:
```
chmod +x install-nethunter-termux
```
```
./install-nethunter-termux
```
This will fetch Kali Linux files and install them for us on our Android device. The script would fetch around 1.5GB of files so naturally, it might take a lot of time depending upon your network speed. Once the script is done extracting the rootfs file, you can even delete it.

Once the script has finished, you can run Kali Nethunter from the CLI.

To launch Kali Linux in CLI mode, type:
```
nethunter
```

This would drop into a shell on Kali Linux. You can now use Kali Tools or check your OS with
```
$ cat /etc/os-release | grep "\bNAME="
NAME="Kali GNU/Linux"
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

## Conclusion

Note that on non-rooted you cannot use some tools which require root permissions . However, this still remains utilitarian when performing memory intensive operations like Password cracking and bruteforcing. Most mobile devices nowadays come with a lot of RAM and brilliant processors which can help to crack password hashes or bruteforce our way into systems all the while retaining the functionalities of a normal Android Device.

## Support:

<p align="vertical"><a href="https://paypal.me/popeye0013"><img src="https://github.com/aha999/DonateButtons/blob/1371730702589476cbd31790685ded66857a1f08/Paypal.png" width="175"></a></p>
