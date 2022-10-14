## mac-ansible
A one-stop shop repository for collecting all artefacts related to my Macbook configurations for easy redeployment

### Install requirements
`ansible-galaxy install -r requirements.yml`

#
### Run the playbook
`ansible-playbook -i inventory --vault-id @prompt --ask-become-pass playbook.yml`
<br/>
`ansible-playbook -i inventory --ask-become-pass playbook.yml`

---
#
### Improvements to make
On the previous execution, I took the following notes to help future proof it:
Had to manually install home-brew
Had to manually share over ssh keys via airdrop
Had to use home-brew to install Ansible so I could then run Ansible
(This could have perhaps been a separate shell script to get this going before jumping into the main swing of things) 


Do I use the brew bundle file to maintain what’s installed ? Or do I use the jeffgeerling stuff???
 

New automation idea
Script that will:
- Obtain / push SSH keys to the machine
- Git clone (Via ssh now) to get Mac-ansible side of it
- Install home-brew via the curl command on the site
- Install ansible via home-brew
- Start the ansible playbook process
- Move the .zshrc file after ohmyzsh has been installed

What about the home-brew file ??
`Brew bundle` is all you need


Oh my Zsh is a manual curl command 
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"


#
### Encrypt a file
`ansible-vault encrypt myfile.zip`

#
### Encrypt a string
`ansible-vault encrypt_string 'my_string_value' --name 'var_name'`
