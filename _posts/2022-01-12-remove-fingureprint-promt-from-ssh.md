---
layout: post
title: "How to Remove the password/fingerprint prompt while ssh"
author: igour
categories: [automation, ssh]
tags: [red, yellow]
image: assets/images/11.jpg
description: "Help you to automate your ssh into new server with no extra key stock required."
---

Always I wanted to use my ssh into predefine servers in an automated way, what I do is I create the alias for each server which is generic in my scene.

#### So, how I do this?

It's really simple! I have created the function to do the ssh which I reside in my config script( this will be another blog post), current we just wanted to get rid of the password or fingerprint prompt, so that just one key stock will be in the desired server.

### So what I did

I created one file if already not present in your case, do that.

`vi ~/.ssh/config`

just paste the following into it

```
# Ignore the HostKeyChecking
Host *
 StrictHostKeyChecking no
```

This makes sure the ssh will not ask/check each time the host key before you try to login into the new host/server.

And then use whatever way you wanted to do the ssh, this will not gonna ask for fingerprint, like this

```
ECDSA key fingerprint is SHA256:h8OCcT7dX+z8CmGFjSixDAyfgrvysfxaVczgfA8HFvA.
Are you sure you want to continue connecting (yes/no/[fingerprint])?
```

I will write another blog where I will have a details blog about my way of doing the ssh(its easy), I will see you there.

thank for the short read. Hope it will help.
