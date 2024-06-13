<h1 align="center">
<a href="icon"><img src="static/icon.png" alt="icon" height="400px"></a>
</h1>

<h4 align="center">Open Source Recon Template for VPS on Digital Ocean </h4>

<p align="center">
  <a href=https://github.com/cunhaDev/recon-template>Configure Your VPS with Ubuntu 20.04</a> •
  <a href="#usage">Use Recon Template</a> •

**Recon Template** is a simple and easy-to-use template based on terraform and shell script for create and configure a VPS on Digital Ocean with focus on Pentest.
Hero contain the Commands for install all tools based on template and methodologies of [@ofjaaah](https://twitter.com/ofjaaah).

</p>

## Usage

**`Recon Template`** requires **System Linux Ubuntu 20.04** and **Golang installed on VPS.**.

1. If don't have a System VPS and Go installed, please follow the setup [Here](https://github.com/cunhaDev/recon-template)


2. Copy the command for create and open install file:

```sh
nano recon-template.sh
```

2. Copy the command and past on file `recon-template.sh`:

```sh
#!/bin/bash

packages=(
    "github.com/tomnomnom/assetfinder@latest"
    "github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest"
    "github.com/tomnomnom/httprobe@latest"
    "github.com/projectdiscovery/httpx/cmd/httpx@latest"
    "github.com/projectdiscovery/nuclei/v2/cmd/nuclei@latest"
    "github.com/hakluke/hakrawler@latest"
    "github.com/tomnomnom/waybackurls@latest"
    "github.com/ffuf/ffuf@latest"
    "github.com/hahwul/dalfox/v2@latest"
    "github.com/tomnomnom/hacks/anti-burl@latest"
    "github.com/tomnomnom/anew@latest"
    "github.com/tomnomnom/qsreplace@latest"
    "github.com/tomnomnom/gf@latest"
    "github.com/jaeles-project/gospider@latest"
    "github.com/haccer/subjack@latest"
    "github.com/projectdiscovery/dnsx/cmd/dnsx@latest"
    "github.com/KathanP19/Gxss@latest"
    "github.com/j3ssie/metabigor@latest"
    "github.com/dwisiswant0/cf-check@latest"
    "github.com/projectdiscovery/naabu/v2/cmd/naabu@latest"
    "github.com/tomnomnom/hacks/filter-resolved@latest"
    "github.com/owasp-amass/amass/v4/...@master"
    "github.com/lc/gau/v2/cmd/gau@latest"
    "github.com/deletescape/goop@latest"
    "github.com/hakluke/hakcheckurl@latest"
    "github.com/tomnomnom/meg@latest"
    "github.com/takshal/freq@latest"
    "github.com/j3ssie/sdlookup@latest"
    "github.com/d3mondev/puredns/v2@latest"
    "github.com/hueristiq/xurlfind3r/cmd/xurlfind3r@latest"
    "github.com/ferreiraklet/airixss@latest"
    "github.com/ferreiraklet/nilo"
    "github.com/hueristiq/xurlfind3r/cmd/xurlfind3r@latest"
)

for package in "${packages[@]}"
do
    go install "$package"
done
```

3. execute command Ctrl X, after press Y and press ENTER for save file.

4. execute command for create executable:

```sh
chmod +x recon-template.sh
```
5. execute this command for install Go tools:

```sh
./recon-template.sh
```

6. execute this command for move all tools to /usr/local/bin:

```sh
sudo mv $HOME/go/bin/* /usr/local/bin
```
<table>
<tr>
<td>  

> **Observation**:
> - *Currently, this project have manual dependecy for install tools, soon it will be on unique Tool.*

</table>
</tr>
</td> 
