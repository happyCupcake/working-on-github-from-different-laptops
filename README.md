# Working on Github from different laptops

It's a pain to do this every time and I cannot remember the commands. And Github documentation has it scattered around in the most generic way [here.](https://docs.github.com/en/authentication/connecting-to-github-with-ssh). As you all know, I am lazy, so I have decided to consolidate all of those commands in one place for my sanity and productiveness.

## Verify what keys you have
ls -al ~/.ssh


## Generate a new private and public key pair for ssh access
```ssh-keygen -t ed25519 -C "your_email@example.com" ```

-C flag is for adding a comment

## Start the ssh-agent
eval "$(ssh-agent -s)"

## Add your SSH private key to the ssh-agent
ssh-add ~/.ssh/id_ed25519

## Add the SSH public key to your account on GitHub

### Copy the full SSH public key to your clipboard

### Add to github settings
- click your profile photo, then click Settings.
- In the "Access" section of the sidebar, click SSH and GPG keys.
- Click New SSH key or Add SSH key.
- In the "Key" field, paste your public key.
- Click Add SSH key.
