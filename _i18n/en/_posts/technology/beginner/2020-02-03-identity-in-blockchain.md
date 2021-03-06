---
layout: post
type: article
title: "Identity in Blockchain"
description: "The Horizen Academy is a free educational platform on blockchain technology, cryptocurrency, and privacy. In this article, we explain cryptography's part in blockchain as it relates to identity, ownership, and your key pairs at a beginner level."
permalink: /technology/beginner/identity-in-blockchain/
topic: technology
level: beginner
chapter: "How Does a Blockchain Work?"
further_reads: [the_impact_of_digital_identity, how_blockchain_can_solve_identity_management_problems]
---

In our last article, we talked about the main entities of a blockchain. We concluded that nodes make up the infrastructure of a blockchain and that miners are the bookkeepers of a cryptocurrency. They keep track of how much funds there are and who owns them. We must have a concept of identity to have ownership. You want to be the sole owner of your funds, and there must be a way to associate the funds with you. This is where cryptography enters the scene.

### Public-Key Cryptography

One of the core concepts that make blockchains work is the concept of _asymmetric cryptography_, also known as _public-key cryptography_.
With symmetric cryptography, you encrypt and decrypt a message using the same key (like a padlock).

![Symmetric](/assets/post_files/technology/beginner/identity-in-blockchain/symmetric_D.jpg)
![Symmetric](/assets/post_files/technology/beginner/identity-in-blockchain/symmetric_M.jpg)

With asymmetric cryptography, you encrypt and decrypt a message using two different keys, the public key, and the private key. The keys always come in pairs. If you encrypt a message with a public key, it must be decrypted with the corresponding private key and vice versa. This boils down to a simple concept: Your key pair is your identity on the blockchain.

![Asymmetric](/assets/post_files/technology/beginner/identity-in-blockchain/asymmetric_D.jpg)
![Asymmetric](/assets/post_files/technology/beginner/identity-in-blockchain/asymmetric_M.jpg)

### Your Key Pair is Your Identity

The idea in cryptocurrencies is that you are receiving funds with your public key and spending them with your private key. A private key on the Horizen blockchain could look like this.

<center>
Kz6994Ek9L3uzjQo2wANaHguBbEShoHZo6q1Y3r6rXrHfWka1fnx
</center>

and the corresponding public key or address like this.

<center>
znSrHR9ssjKMsrYfk5fTmKH4LbgDxXJ3s6j.
</center>

The keys were intentionally named public and private key. You can share your public key with anybody that wants to send you money. Your private key, as the name suggests, should remain private under all circumstances, because it allows you to spend your money. If somebody gets their hands on your private key, they can access and steal your funds.

The real-life comparison you will hear most often is your public key being like your address. You can give it to anybody that wants to send you a letter. Your private key is like the key to your postbox. Only this key lets you access your mail, and you wouldn't hand it to a stranger. If you want to learn about this concept in more detail, you will find a more in-depth explanation [in the Advanced Level]({{ site.baseurl }}{% post_url /technology/advanced/2021-02-04-public-key-cryptography %}) and an exact description in the Expert Level.

Your keys are important for sending and receiving transactions. Technically, a transaction is a message to all nodes on the network. This message includes how much of your money you want to send, and to whom. This information is then encrypted with your private key, a step we call _signing a transaction_.

![Signing](/assets/post_files/technology/beginner/identity-in-blockchain/signing_D.jpg)
![Signing](/assets/post_files/technology/beginner/identity-in-blockchain/signing_M.jpg)

A digital signature works similarly to how you authorize real-life transactions using your "analog" signature. Even with modern supercomputers, it is infeasible to forge such a digital signature. The type of public-key cryptography used in blockchains is one of the safest means of encryption available today.

All of this would be cumbersome to do manually and require quite some skill. Luckily there are [wallets]({{ site.baseurl }}{% post_url /technology/beginner/2020-03-01-wallets %}) that help you do all the above. Wallets generate and manage your keys and take care of all the necessary encryption and decryption. What is important is to understand that your private key authorizes the spending of your funds. Keeping it safe is the first and most important lesson. Nobody can help you recover your keys in case you lose them. If somebody were able to recover it for you, they would also be able to take your money at will.

### Summary

Your key pair is your identity on the blockchain. Your public key serves as your address and is used to receive funds. Your private key is like a password -  it lets you (or anybody that gets their hands on it) spend your money. Always protect your private keys and never hand them out to other parties! If anybody asks you for your private key, it is most certainly a scam!
