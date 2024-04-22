# Automate Let's Encrypt cert generation

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

