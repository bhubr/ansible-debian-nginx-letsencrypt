# Automate Let's Encrypt cert generation

> This is a **quick'n'dirty** repo for testing certbot automation on VMs exposed to the internet.
>
> This is by no means something to be taken as a production-ready example.

## 1. setup Nginx config for `.acme-challenge`

```
ansible-playbook -bK -i inventory.ini playbook-nginx-acme-challenge.yml
```

## 2a. Perform certbot **dry-run**

```
ansible-playbook -bK -i inventory.ini playbook-certbot-dry.yml
```

## 2a. Run **actual** certbot issue

```
ansible-playbook -bK -i inventory.ini playbook-certbot.yml
```

## 3. Setup vhosts for domains

```
ansible-playbook -bK -i inventory.ini playbook-nginx-vhosts.yml
```
