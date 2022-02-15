## Guide to install Node version manager

We are using [fnm](https://github.com/Schniz/fnm) as our preferred node version
manager


In order to install this on your linux system. Use the following guide

1. Download the installer script for linux enviornment

```bash
curl -fsSL https://fnm.vercel.app/install | bash
```

2. Add completions for your shell

```bash
fnm completions --shell bash 
```

3. Add the following line to your `.bashrc` file. You can use your preferred
	editor to open `.bashrc` file. Considering you are using Ubuntu we will use
	gedit

First open the file with gedit

```bash
gedit ~/.bashrc
```
Now paste the following at the bottom of `.bashrc` file

```bash
# FNM cli tool config
eval "$(fnm env --use-on-cd)"
```

press `Ctrl + s` to save the file and close the gedit application

4. Close the terminal and start a new terminal session

5. Now you can install any node version you like with `fnm install`

- List all available node version with

```bash
fnm list-remote
```

- Install the v14 LTS node version of `v14.19.0`

```bash
fnm install v14.19.0
```

Tip:

For particular project just create a `.node-version` in root of folder
containing the node version value.

paste version in this format in `.node-version` file
.node-version file
```
v14.19.0
`
