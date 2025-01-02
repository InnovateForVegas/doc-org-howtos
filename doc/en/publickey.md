<!--
 Copyright (C) 2022 Innovate for Vegas Foundation
 
 This file is part of doc-org-howtos.
 
 doc-org-howtos is free software: you can redistribute it and/or modify
 it under the terms of the GNU General Public License as published by
 the Free Software Foundation, either version 3 of the License, or
 (at your option) any later version.
 
 doc-org-howtos is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 GNU General Public License for more details.
 
 You should have received a copy of the GNU General Public License
 along with doc-org-howtos.  If not, see <http://www.gnu.org/licenses/>.
-->

# Public Key Encryption and Innovate for Vegas Foundation

There was a time, not so long ago, when encryption technology was treated as a munition (a physical weapon) by the US Government, and so using it to protect privacy and ensure authenticity (signing documents, attestation of key ownership by others) carried some concern, some controversy, and some international interoperability issues. Today, in modern times, we often use tools which offer *end-to-end encryption* and we barely give it a second thought. Believe it or not, Public Key Infrastructure, and one of the earliest public technologies within this realm, PGP, are still in use and still work great.

As part of a general focus by our organization on individual privacy and security, we will emphasize and encourage the use of the tried-and-true technologies, in addition to other, newer technologies as they become provably effective and safe to use. There is a learning curve, to be sure, but the alternative appears to lead individuals to blindly trust incoming messages and documents, to suffer phishing and spear phishing attacks, account compromises, identity and property theft, and possibly worse.

We would like to remember and employ tools and methods that are already available, for decades, to offer some protections against these direct attacks, and so we will make use of these to become familiar.

## What is PGP?

PGP, or [Pretty Good Privacy](https://en.wikipedia.org/wiki/Pretty_Good_Privacy), was written by Phil Zimmerman and launched in 1991. It was the cause of great concern at government levels as it placed powerful encryption and signing tools into the hands of the public. PGP is still in use today, and has grown in adoption and development, easily found today at [OpenPGP](https://www.openpgp.org/) making strong, tested encryption available to anyone who wants to make use of it. That includes us!

While PGP is still in use, there is an open source, actively developed set of tools called GPG, or GnuPG, which stands for [Gnu Privacy Guard](https://gnupg.org/). You may see PGP, OpenPGP, GPG, GnuPG, and other names of tools and platforms and websites used under the Public Key Infrastructure umbrella, and all of these enable interoperable public key cryptography and related interactions, making them extremely powerful and accessible to anyone across many platforms and implementations.

## What is Public Key Cryptography?

The mathematics that enable public key cryptography are quite interesting and worth diving into if you are interested. The Wikipedia link above for Pretty Good Privacy will get you started down that path. If you are unfamiliar with public key cryptography, here is a very rudimentary overview (again, dive into how it all works if you are interested, it is worth knowing and understanding).

### Terminology

- **Key Pair** is often how the public+private keys are referred to. They go together explicitly; you generate a key pair and the result is a public key and a private key.
- **Private Key** is the private part that you never, ever, ever share with anyone. Just as the name implies, it is private, and must remain that way. Usually the private key is protected by a passphrase, which you must use to decrypt and enable the private key for a particular length of time, you should never share that passphrase, either.
- **Public Key** is the part of a key pair that can be shared openly, and in fact it should be shared far and wide so that other people can use your public key.
- **Keyserver** is an open source and distributed way of sharing your public key(s) with the world. Share your public key in one or more keyservers without concern, they are public keys! Do note, though, that anyone can post a public key to a keyserver, it is important to know that the key really does belong to who you believe it belongs to.
- **Key Verification** can be performed using a Key Fingerprint, which is a short string of characters that you can read to the owner of a key in a voice or video call so they may verify it, you may have the owner read those values to you, or you can verify them by inspection in person. You can also begin with a known block of text, encrypt and/or sign it, and send it to the other and verify that the decrypted message matches the original, which proves the key is controlled by the individual whom you believed controls it. This sounds complicated, but it is not, and it is a core component of the Web of Trust.
- **Web of Trust** is a model whereby public keys are verified by one or more people, who themselves are verified by one or more other people, using a common Key Verification method, so that a public key obtained from a public keyserver, verified by multiple individuals, will have the trust of those individuals applied to that public key in a provable way using digital signatures applied to the key.
- **Revocation** is something you can do if your private key becomes compromised, or if you want to indicate that a public key should no longer be used. For example, if you no longer work for a particular employer, you could revoke your keys you may have created and associated with your work email address.
- **Signed Key** is, as we will summarize below, the signing of your public key by one or more other private keys, which provides a way for others to attest to the validity of your public key, and thus the authenticity of you. This has limited validity in some cases, and this so-called *Web of Trust* is as valuable as the individuals participating within it.
- **Sub-Keys** are additional parts of your key pair that can be used for specific use cases. Once you encounter this level of detail you will be making serious use of PKI, which is great! There is some documentation about the subkey mechanism in the [GPG Key Management Documentation](https://www.gnupg.org/gph/en/manual/c235.html) but for now, a *subkey* is a part of your key pair. You can create a signing-only or encrypting-only subkey which will be bound to your key pair, but which may be revoked separately from your key pair. This seems complicated, but it is not once you put your keys to use.
- **Secure Hash** is something you may see frequently in the exciting world of Blockchain. A secure hash is a mathematical operation performed on some data so that the result is other data that is provably based on the source data, but which cannot regenerate the source data. A very simple example follows below.
- **Clear Text** is the unencrypted (or not-encrypted, or pre-encrypted) message you typically send via email or write on a postcard before mailing it.
- **Cypher Text** is the encrypted message you should send via email and any other way if you would prefer others not read (and possibly edit) your Clear Text.
- **Message Digest** is the output of a securely hashed input message (the Clear Text) and explicitly indicates that a source Clear Text must, when passed through the selected Secure Hash algorithm, result in the matching hash value found in the Message Digest.
- **Symmetric Cypher** is an encryption scheme whereby an encryption key can be used to both encrypt Clear Text and decrypt Cypher Text using the same key. There is no key pair in a symmetric encryption scheme, as in the typical use case that same key is used for both transformations of your message data.
- **Asymmetric Cypher** is the general term used to describe encryption schemes that use one key to encrypt Clear Text and another key to decrypt Cypher Text. The specifics of how the keys are used in the particular scheme can vary, we will focus on PGP and the so-called PGP Envelope here.
- **Session Key** is a Symmetric Cypher key generated by a message sender and included in the PGP Envelope. It is used only once, for a given message, and is encrypted using the public key of the recipient, so that only the recipient can decrypt the session key with their private key.

This is enough to get use started!

### Email Workflow Example

Suppose you would like to send an encrypted email message to your friend. The most common names used for these sorts of examples are Alice and Bob, which we will assign She/Her/Hers and He/Him/His pronouns for our examples:

1. Alice would like to send an encrypted message to Bob. First, Bob and Alice generate their key pairs and they can either publish their public keys to public keyservers, or they can send their public keys directly to each other.
2. Alice can verify Bob by, in this example, calling Bob and asking Bob to read the fingerprint value of his key to her, which she can confirm. Alice can do the same so Bob can verify her public key, confirming the fingerprint value.
3. Once the keys are verified, Alice can sign Bob´s key and Bob can sign Alice´s key (the publication of signed keys to public keyservers and the use of public key certificate authorities is something we will cover in the vLocal Initiative!)
4. Now, Alice can use Bob´s public key to encrypt the message she would like to send to him. Her OpenPGP software will create a session key, encrypt the clear text with the session key, encrypt the session key with the public key, and package the resulting cypher text and encrypted session key into a pgp envelope (for the reader, investigate how MIME, or Multipurpose Internet Mail Extensions, are used for this sort of thing).
5. When Bob receives the email from Alice, it will be obviously marked as an encrypted message. If Bob is using an email client that can encrypt and decrypt emails (there are many, Alice is using one already), he may be asked for his keypair passphrase to decrypt the message using his private key. At that point, the session key is decrypted and that session key is used to decrypt the cypher text back into the original clear text.
6. Usually, email clients will leave the encrypted message in the inbox or folder or file it uses to store mail. This is called *at rest* encryption, so that Bob must decrypt the message each time he wants to view it, or reply to it. In the case of replying, he can decrypt the message, create a reply, and encrypt it with Alice´s public key, and the circle of encrypted messaging continues.

What if Alice wants to verify that she is sending content, but wants to enable Bob and perhaps others to be able to read the Clear Text. In this case, Alice wants to send a Signed message.

1. Alice is going to send a message to Bob, and maybe she will add some other recipients and she has not obtained or verified their public keys. Rather than using Bob´s public key to encrypt her session key for the cypher text in her message, she is going to do something else.
2. To sign her message, Alice will enter the passphrase for her private key, and use that private key to encrypt a message digest created from her clear text. The secure hash algorithm used to generate the message digest is indicated in the envelope, which will contain the clear text of the message and the hashed clear text in the form of the message digest, which is encrypted with Alice´s private key.
3. When Bob receives the message from Alice, he can see that it is a signed message, and since he has Alice´s verified public key, he can verify that the message Alice sent is from Alice, and has not been altered, by re-creating a message digest from the clear text in the message, decrypting the message digest from Alice using Alice´s public key, and comparing the results. If they are a perfect match, we know that only Alice could have created and signed the message digest with her private key, and since the hash values match, we know that the message content was unaltered since any change to the clear text would have changed the has result in the message digest.
4. Anyone who has received the signed message from Alice, but who does not have her public key in their possession, can still read the message clear text. They can verify Alice as the sender, and the integrity of the clear text if they obtain Alice´s public key from a public keyserver. The new user(s) can contact Alice to verify her public key, or if Alice´s key is published with attesting in the form of Bob´s signature, a person who knows Bob might trust Alice implicitly and verify the message accordingly.

As with most things, it sounds more complicated to describe that it is in practice, and this is mostly true in the case of Public Key Cryptography. There are other uses cases, such as signing messages published to public forums and social media sites, encrypting files on a thumb drive or in the cloud, and signing your committed changes to an Entity repository (see the [Github](github.md) document here for some details about that).

## Motivation

Why do we want to use this tried-and-true technology that is freely available to all to help protect privacy, increase personal security, and enable individuals to verify and validate message senders and their message content?

The answer is in the question of course, but let us examine some simply cases where mindful use of encryption and signing tools and methods would help (though not completely solve) some common troubles we read about all too often:

- You might receive an email from a sender that looks like Amazon or Google or Microsoft or your bank or your insurance company, or anyone you might trust based on that **From** line. You click on a link in the message that looks like it might be important, but the sender had forged that From line and its actually a phishing attack! It only get worse from here.
- You receive a forwarded message from someone you do not know very well, but the original sender seems legitimate. The message has a link within it and you click on it. Uh oh, that was not a good idea.
- You receive another forwarded message, this time there is some important reference information and a phone number to call. You might even have been expecting this forwarded message, and if you are not careful you may call the phone number in the forwarded message… which was changed somewhere along the line, so that you call the number trusting it, and your troubles begin!
- You send a message to someone with important information in it, but the message is damaged or altered along the way. Without any check on the message content, the recipient assumes your message is correct and proceeds on that assumption. The damage or alteration could have occurred maliciously in what we call a Person-in-the-Middle attack.
- You may be required to verify your login (or initial sign up) to an online service by receiving an email with a click-through verification link within it. In a really sophisticated attack scenario (though they are happening more often, especially where a workplace email address is concerned), the sign-up process may be compromised, or the login process may have been attacked and intercepted, so that the verification email is from an adversary, forged and fraudulent. You click on the verification, which the adversary can use steal your credentials! (Not exactly this simple, but not much more difficult)
- Surely there are more, especially variations where one´s entire online presence is literally stolen once a main email account can be compromised with a password reset, and that only gets worse with each passing minute. In other cases, a click on a link from a forged sender results in theft of cryptocurrency assets or entire wallets.

The ability to verify the contents of a message, and to establish some confidence baseline in the sender (the **From** line) of an incoming email message, the ability to verify the contents of a forwarded message, and the ability to exchange important information with far-reaching implications in a secure, encrypted way are all protections available today, and they have been available for decades.

As we all use technology more, and rely on the information flow using these technologies, the ability to trust sources and content of messages, files, attachments, social media posts, and so on, is only becoming more important, and in some cases critical, with far reaching consequences as we continue to believe that the extra effort to secure our communications is not ultimately worthwhile.

If you wear a seatbelt in an automobile, if you wear a helmet on a motorcycle, if you lock your doors, if you have smoke detectors, you already know that prevention is better than recovery, we can make similar arguments supporting expansive use of public key encryption technology, which has been available to all in open source form the whole time.

## A word on Crypto

Cryptography is a complicated science with substantial expertise in group theory, number fields, computational complexity, and so on all applied to old and new ways. This document is not arguing for or against the use of cryptocurrencies (other than using cryptography to protect communications about wallets and assets, we have already seen those thefts happen), but to be clear:

Cryptography, Encryption, and Signing are terms we use to describe securing and authenticating messages, senders, and recipients.

Cryptocurrencies make use of the so-called Blockchain, which itself relies (in the proof of work scheme) on the difficulty calculating a message digest of a block with some known bits in the hash. This is a novel use of hash collision detection, and it is worth understanding in general, and specifically if you are using Blockchain at all.
