# ansible


---
- name: Install Ngnix and Start
  hosts: all
  become: true

  tasks:
    - name: Install Ngnix
      apt:
       name: nginx
       state: present

    - name: Start Ngnix
      service:
       name: nginx
       state: started
