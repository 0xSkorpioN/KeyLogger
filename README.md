# KeyLogger
This program runs invisibly, collects the victim's keystrokes and sends them back via a network to an address of choice.

## Usage:
First, you need to download a tool to listen for TCP traffic on the machine from inside the victim's machine. The best choice is Netcat.

### On Windows:

https://eternallybored.org/misc/netcat/

Unpack the archive (be careful as windows defender might complain that this is a virus, so it's recommended to at least make this file an exception for AV).

Depending on your system architecture, use nc.exe (for 32 bit) or nc64.exe (for 64 bit).

### On Linux:

You might want to use the kali linux built-in netcat as well; it's up to you.

Navigate to the directory where netcat resides. Then, run:

`nc.exe -lvp 5555 (or the port you specified in the source code) <- For Windows`

`nc -lvp 5555 (or the port you specified in the source code) <- For Linux`

**TIP: If your program is not connecting and you are using Windows, check the Firewall settings. It is possible that the firewall is blocking you, so you might want to turn it off for this exercise.**

Go to the target/victim machine, execute the program and type something.

Going back to your "attacking" machine, you should see everything have been wrote in the target/victim machine are shown to you.

**Note: You have to put the DirStealer.exe somehow in the victim's machine secretly 😉**
