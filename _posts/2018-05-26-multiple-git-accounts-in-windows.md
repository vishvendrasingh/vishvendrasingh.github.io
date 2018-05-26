---
title: Multiple git accounts in windows
layout: page
comments: true
social-share: true
show-avatar: true
---

**Create key**

`$ssh-keygen -t rsa -C "your_email@youremail.com`

**Creates a new ssh key using the provided email**


```
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/you/.ssh/id_rsa): 
```


**check if ssh-agent is running or not**
```
$exec ssh-agent bash
$ssh-add /c/Users/you/.ssh/id_rsa_two
```

**Create a config file But the fun is not over yet! You need to set up the two profiles in a config file. Create /c/Users/you/.ssh/config and make it look like this:**

```
#Account one
Host one.github.com
    HostName github.com
    PreferredAuthentications publickey
		User git
    IdentityFile /c/Projects/.ssh/id_rsa

#Account two
Host two.github.com
    HostName github.com
    PreferredAuthentications publickey
		User git
    IdentityFile /c/Projects/.ssh/id_rsa_two
```
		
**check if it is working fine**
```
$ssh -T git@github.co
$ssh -T git@github.com -i /c/Users/you/.ssh/id_rsa_two
```

**then set git remote like this**
git@one.github.com:one/one..git