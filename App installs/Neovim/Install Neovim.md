Step 1:
	Install the build prerequisites
		https://github.com/neovim/neovim/wiki/Building-Neovim#build-prerequisites
		Ubuntu/Debian 
			sudo apt-get install ninja-build gettext cmake unzip curl

Step 2:
	Clone Neovim
		 `git clone https://github.com/neovim/neovim`
	Run this command
		`cd neovim && make CMAKE_BUILD_TYPE=RelWithDebInfo`
	If on Ubuntu/Debian:
		`cd build && cpack -G DEB && sudo dpkg -i nvim-linux64.deb`
		

Step 3:
	Uninstall:
		Possible `dpkg -l | grep nvim`
		Else `sudo cmake --build build/ --target uninstall`
		OR `sudo rm /usr/local/bin/nvim` and `sudo rm -r /usr/local/share/nvim/`
	Confirm:
		`sudo find / -path /mnt -prune -o -name 'nvim' -print -o -name 'neovim' -print
`