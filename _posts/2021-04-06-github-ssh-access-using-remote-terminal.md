# Github SSH access using a remote terminal

To make my life easier, I recently setup ssh access to github on my `desktop` machine by following [Github's instructions](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent). To test ssh access on this machine, I launched a terminal using my GNOME3 desktop environment and ran `ssh -T git@github.com` which returned
```
Hi <github_username>! You've successfully authenticated, but GitHub does not provide shell access.
```

However, when logging into `desktop` using ssh, i.e `ssh user@desktop`, the ssh access test above failed. [Stackoverflow](https://stackoverflow.com/questions/45137676/ssh-key-issue-connecting-to-github-via-remote-machine) to the rescue! Turns out, the ssh-keys for accessing the host `github.com` are stored in [GNOME Keyring](https://wiki.gnome.org/Projects/GnomeKeyring) hence when logging into the machine via ssh without GNOME3, the keys could not be found.

The solution is to create (if it doesn't exist) a ssh config file at `~/.ssh/config` and populate it using
```
Host github.com
  IdentityFile ~/.ssh/path_to_private_key
  IdentitiesOnly yes
```
