`sudo apt-get install git`

`git config --global user.name "Your name"`
`git config --global user.email ""`

SSH for git
`ssh-keygen -t ed25519 -C "your_email@example.com"`
`eval "$(ssh-agent -s)"` 
`ssh-add ~/.ssh/id_ed25519`
`cat ~/.ssh/id_ed25519.pub | clip.exe`
