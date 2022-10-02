<!--
 Copyright (C) 2022 Code for Vegas Foundation
 
 This file is part of doc-cfv-howtos.
 
 doc-cfv-howtos is free software: you can redistribute it and/or modify
 it under the terms of the GNU General Public License as published by
 the Free Software Foundation, either version 3 of the License, or
 (at your option) any later version.
 
 doc-cfv-howtos is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 GNU General Public License for more details.
 
 You should have received a copy of the GNU General Public License
 along with doc-cfv-howtos.  If not, see <http://www.gnu.org/licenses/>.
-->

# Secrets

A secret is something that should not be shared with others, whether those others are people, companies, computers, or anything else. The only way to ensure a secret remains a secret is to never divulge it in any way to anyone, never write it down, never utter it out loud in your sleep, never tap it out in Morse Code on your desk with your pencil. Never.

Let us address all of the secrets that cannot be kept so secret.

## Passwords

You have a GitHub password, perhaps, or maybe a password that you use to log in to your email account, or maybe you have a PIN code that you use to unlock your mobile phone. You should never write that password down anywhere, ever. This does not guarantee it cannot be compromised, but it is all you can do on your side of the authentication process to protect it. Your mobile device, your email provider, or GitHub all know your password also (well, they can verify it), and any time a password is stored somewhere else there is a chance that it could be stolen, but we can hope that the other side of your password-protected account is not storing your password as what is called Clear Text, but is instead storing a salted hash, at least.

If you are not storing your passwords in your personal memory (if you have more than 10 secure passwords, *and they are all different,* you have probably reached an upper limit on convenience), you should be storing them in an encrypted password store, like Bitwarden or password-manager or 1Password or similar. Keep your passwords safe, and keep the place where you store them safe, and make sure you can trust that if you are not keeping your passwords safe when they are stored, that you can trust the service that claims to be doing that for you (we like Bitwarden, but there are many fine services out there). It is essential that these services store your information encrypted and *without* recovery. This means only you know your main password to unlock what they usually call a Vault that holds your encrypted passwords.

This may seem obvious, but how you manage your personal passwords and the tools you use to store them is important!

## Non-personal Accounts

As you participate in more projects and activities in an organization such as Code for Vegas Foundation, or maybe in your own collaborative projects, or in a job at any company, you may find yourself with accounts that are not really yours. Your company email address, a cloud service account, an alternate GitHub account for paid work projects using Enterprise Authentication, or any number of similar possibilities. In these cases, the account may have associated with it a lot more intellectual property, collaborative work, financial implications, and so on. Imagine that as painful and expensive as it may be if you were to lose or otherwise compromise your own password(s), allowing a non-personal account compromise can be even worse, and may involve more people than yourself. If you have established your own best practices for managing and protecting your own secrets, apply those best practices to the secrets attached to your non-personal accounts and services.

It is important to connect non-personal accounts and associated secrets with the responsibility that goes with possessing those secrets and using those accounts.

## Non-personal Credentials

With the explosion of cloud services and the ability to make use of these services across various accounts and regions and teams, there has been a substantial increase in the use of IAM, or Identity and Access Management, commonly found with that acronym using Amazon Web Services and more and more services every day. In fact, as we will cover in the next section, IAM as a general concept applies to everything in this document.

It is possible, even likely that a cloud service will be associated with an account, which you will not have access to. This is sometimes called the Root Account, which is often created by a system administrator at your company, or maybe your colleagues and collaborators have one individual keeping track of accounts and account creation, or maybe you are doing it yourself. The root account will have a username (typically an email address but not always) and a password, and ideally a second factor authentication scheme in place as well. This root account and its login credentials should only be used very rarely, to create some initial IAM roles and configure initial account billing information, but that is really everything.

All other access will typically be through an IAM Access Key and an IAM Secret. Treat these as you would any other username and password, with the extra attention you would give to those for a non-personal account.

There are several useful properties of IAM credentials, but the most important in the context of this document is the fact that these credentials can be changed any time. In fact, *credential rotation* is common, and helps to mitigate exposure if there is a leak of credentials, so that credentials that have been compromised will not be valid for long. If there is a built-in rotation process that changes the credentials frequently, and if all workflows are compatible with this rotation policy, then changing credentials in an emergency should be almost as convenient. Part of this workflow is to always assume that the credentials may change, and so they should not be copied and pasted into any code or configuration files or anywhere else, they should always be retrieved from a secure credential store, and that secure credential store should always contain the most current credentials whenever there is a rotation, whether scheduled or in the event of an emergency.

It is important to make a note of this for your entire career and life, because there have been far too many cases of credentials of any kind (whether personal or non-personal, for accounts or for service, or anything else) being copied and pasted into files or other places that are visible to the general public, or perhaps visible to someone who takes the time to view the data obscured *insecurely* inside applications or other places one might not think to look. Always treat IAM credentials as you would any others.

## IAM

There are two important concepts behind the notion of IAM, just as the name, *Identity* and *Access* Management implies. Sometimes you may see the short word *auth* used in reference to *Authentication* but there is slightly more to it than that.

### Authentication

This is where your username and password, and ideally a second factor, are checked and verified. Just as the name, *Two Factor Authentication* implies, the second factor is an attempt to make more valid that verification that you are who or what you are claiming to be. This might also be the Access Key and Secret used to access cloud services, and other similar applications, or it could be a fingerprint, a retina scan, a facial scan, or any combination of the big three:

* Something you have (a physical key, chip card, usb or nfc token, etc)
* Something you are (your fingerprint, face, retina, blood, gait, etc)
* Something you know (username, password, where you were born, the name of your pet, etc)

When we say *two factor authentication* we are adding another factor from these three, so that while you may use your username and password (things you know), that second factor could be a 6-digit numeric value that changes every 20-60 seconds provided by a secure token (a thing you have, even if it is a Authenticator application on your mobile device). This makes it more difficult to compromise the proof of your identity that is authentication.

### Authorization

An authenticated user (or accessor) is typically authorized to perform certain functions, take certain actions, access particular information, based on their authenticated credentials. You may have multiple sets of credentials, each with different authorization policies, it is important to understand which credentials enable which access so you can keep only the least-privileged credentials at risk when necessary. For example, if you need to keep credentials for updating a website in a place to use via some automation tools, it is better to store those credentials for that use than to store credentials that allow you to delete content.

In other words, be aware of how your authenticated access is authorized, what is allowed and what is not, and keep that in mind if you need to use your credentials in deployment pipelines or other types of automation where your credentials are out of your control. The weakest credentials with the least authorization possible to enable your automated workflow is the way to go!

## End Notes

A few final thoughts on secrets and managing them:

* Treat all secrets as if they were your own and controlled access to the most important things.
* Never re-use passwords. Ever.
* Become familiar with encryption of your credentials when you store them, whether locally on your phone or computer, or elsewhere.
* Consider using a physical second factor authentication device for any accounts and services which support them
* If your credentials have been compromised, change them as soon as is possible if you can, and alert the people who manage the associated services **immediately**.
* Never paste your credentials into software source code, configuration files, graphic images, audio files, video files, on a wall, post-it note, or on your body via temporary or permanent tattoo. Ever.
* Never share credentials. Shared secrets should be kept secret as though they are not shared.
* Use secret access methods to retrieve secret credentials from vaults or similar mechanisms and do not store them in new places. Always get the secret from the vault, never the notepad.

If there is ever a question about whether to store a secret credential some place that leads you ask at all, the answer is No.
