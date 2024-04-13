
# X11 Tunnel
> [!NOTE]
> Running graphical software on Gravity with [X11 tunneling](https://en.wikipedia.org/wiki/X_Window_System)   
> Actually, sometimes using **[VNC](/Advanced/VNC)** is better 😜   
> X11 allows you to run a **graphical application** on the *login* or *computing node*, and to control it from your local computer. For example, you can **view images** in the *Gravity* using    
> `eog`
> `display`
> Or, you can even run a browser
> `firefox`
> 

## Windows

For Windows users, we recommend you to use **[MobaXTerm](https://mobaxterm.mobatek.net/download.html)**. It comes with built-in X11 support, so you don't need to do any extra steps. Just [login Gravity](/Basic/Login). Once you are connected, you can connect to an interactive compute node using the -X switch, for example 🌰

```bash
qsub -I -X -v DISPLAY -l nodes=1:ppn=72,mem=1gb,walltime=12:00:00 -q normal
```

Then, you can run your graphical application from the computing node 🎉.

## Mac

Mac users would need to install the program called [XQuartz](https://www.xquartz.org). After installation, double-click on the XQuartz icon to start it (it usually installs into `Applications` -> `Utilities`). Then, in a terminal window

```bash
ssh -Y -i <your_ssh_key> <username>@gravity.sjtu.edu.cn
```

Once you are logged in, you can connect to an interactive compute node using the -X switch, for example

```bash
qsub -I -X -v DISPLAY -l nodes=1:ppn=36,mem=100gb,walltime=12:00:00 -q normal
```

Then, you can run your graphical application from the computing node 🎉.

## Linux
Just use `ssh` to log in!

```bash
ssh -X -i <your_ssh_key> <username>@gravity.sjtu.edu.cn
```

Once you are connected, you can connect to an interactive compute node using the -X switch, for example

```bash
qsub -I -X -v DISPLAY -l nodes=1:ppn=36,mem=100gb,walltime=12:00:00 -q normal
```

Then, you can run your graphical application from the computing node 🎉.
