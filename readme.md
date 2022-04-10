## mac-ansible
A one-stop shop repository for collecting all artefacts related to my Macbook configurations for easy redeployment

### Install requirements
`ansible-galaxy install -r requirements.yml`

#
### Run the playbook
`ansible-playbook -i inventory --vault-id @prompt --ask-become-pass playbook.yml`
<br/>
`ansible-playbook -i inventory --ask-become-pass playbook.yml`

#
### Encrypt a file
`ansible-vault encrypt myfile.zip`

#
### Encrypt a string
`ansible-vault encrypt_string 'my_string_value' --name 'var_name'`
