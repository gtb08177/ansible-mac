### To install requirements:
ansible-galaxy install -r requirements.yml

#
### To run:
ansible-playbook -i inventory --vault-id @prompt --ask-become-pass playbook.yml
ansible-playbook -i inventory --ask-become-pass playbook.yml

#
### To encrypt a file:
ansible-vault encrypt myfile.zip

#
### To encrypt a string:
ansible-vault encrypt_string 'my_string_value' --name 'var_name'