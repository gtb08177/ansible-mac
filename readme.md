# ansible-mac
A one-stop shop repository for configuring Mac OS X to my liking.

## Usage
### Install ansible requirements
    ansible-galaxy install -r requirements.yml

### Execute the ansible playbook    
    ansible-playbook -i inventory --ask-become-pass playbook.yml

---

## Improvements to make
On the previous execution, I took the following notes to help future proof it (perhaps script it):
- Ensure xcode command line tools is installed (to allow this playbook to work)
- Securely automate the installation of private ssh keys (previously had to use AirDrop)
- Start the ansible playbook process
- Include the install of oh-my-zsh

---

## Contingencies
In the event Ansible is proving to be difficult, the homebrew specific aspects can be installed using the Brewfile.
    
    `Brew bundle`

---

## Helpful Commands
### Encrypt a file
    `ansible-vault encrypt myfile.zip`


### Encrypt a string
    `ansible-vault encrypt_string 'my_string_value' --name 'var_name'`
