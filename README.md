# MSPS #

`msps` is the *M*ac *S*hell *P*roxy *S*etter. It takes care of all your shell
proxy worries.

# INTERFACE? # 

`<INTERFACE>` is the network interface name as given by `networksetup
-listallnetworkservices` (*not* the ones retrieved through `ifconfig`).

# One-off usage #

`source msps <INTERFACE>` sets your `http_proxy`, `https_proxy` and `no_proxy`
variables in the *current* shell according to the settings in your Mac Network
preferences.

# Permanent "installation" #

Put `source SOMEPATH/msps "YOUR_FAVORITE_INTERFACE"` into the shell startup
configuration file of your choice (e.g. `.bashrc`, `.zshrc`). You can download
it through `curl -O https://raw.githubusercontent.com/noroute/msps/master/msps`.

Remember that after changing the network environment you need to re-source
`msps` for the changes to take effect.

# Compatibility #

`msps` has been tested with Mac OS X 10.8 to 10.11 with `bash` and `zsh`. Many
other setups may work but are untested.
