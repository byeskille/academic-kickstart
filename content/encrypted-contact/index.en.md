---
title: Encrypted contact
date: 2019-09-18
math: false
diagram: false
markup: mmark
image:
  placement: 3
  caption: 'PGP set up with physical smart cards – both YubiKey and OpenPGP card'
---
As a journalist it is important to me anyone can contact me in a secure way.

With that in mind I have set up a range of different options for both encrypted and anonymous communications (i.e. Signal, Wire, PGP and SecureDrop).

*If there is not a need for extra secure communications I can be reached through regular phone or email:<br/>
Email (personal): [oyvind@byeskille.no](mailto:oyvind@byeskille.no)<br/>
Email (work): [oyvind.bye.skille@nrk.no](mailto:oyvind.bye.skille@nrk.no)<br/>
Cell: +47 41 47 32 20*


## Encrypted

### Signal

If you want to reduce the amount of metadata traces via texts or calls on the cell networks, you can communicate with me using the encrypted app [Signal](https://signal.org/). It offers both text messages, voice and video calls.

The Signal app sends all communications as encrypted data packages.

As a result it does not leave a trace on the phone bill, or as open metadata from the cell networks about the contents of communications or who talks to each other. Signal is known for using open source code, is valued by many for solid encryption solutions and the developers running the system is known to collect [little metadata](https://signal.org/bigbrother/).

**If you want to get in touch with me via Signal, use my cell number:<br/>
+47 41473220**

### Wire

A drawback for the Signal app is the requirement to register your account with the service using your personal phone number. If you do not want to tie your actual phone number to the encrypted communication, or share your phone number in order to communicate securely, another service might be an option.

One alternative is the app [Wire](https://wire.com/en/).

Wire is very similar to Signal, both in use and technology. Though when using Wire it is possible to set up an account using an email address and not a phone number. You are also not required to share the email address or a phone number with anyone in order to establish contact through the Wire app – you can share a username instead.

Here is a guide on [how to set up Wire without a phone number](https://medium.com/@wireapp/staying-anonymous-on-wire-22faa13aba4d).

**If you want to reach me through Wire, you find me under the username:<br/>
byeskille**

### Encrypted email PGP

For secure email use PGP. My public key [can be downloaded here](https://www.byeskille.no/byeskille-BA3721AF33FB6D2A.asc.txt).

Here is some info about it:
```
4096R/0xBA3721AF33FB6D2A 2016-05-28 [expires: 2020-06-11]
Key fingerprint = D901 EA75 C112 A105 2AD9 90B3 BA37 21AF 33FB 6D2A
uid Øyvind Bye Skille – oyvind.bye.skille @ nrk.no
uid Øyvind Bye Skille – oyvind @ byeskille.no
uid Øyvind Bye Skille – oyvind @ byeskille.net
```

**NOTICE:** PGP only encrypts the contents of the email, not the subject or any metadata about who communicate. AS a result encrypted email with PGP will leak more info through metadata about the communication to anyone monitoring network traffic.

To communicate with me using PGP you will need my public PGP key. It can be downloaded [here](https://www.byeskille.no/byeskille-BA3721AF33FB6D2A.asc.txt), through [Keybase](https://keybase.io/byeskille) or via key servers as [keys.openpgp.org](https://keys.openpgp.org/search?q=oyvind.bye.skille%40nrk.no).

PGP can also be used to encrypt files, that later on can be transferred through other channeles than email.

In June 2018 [I changed my PGP setup](https://byeskille.no/2018/06/ny-pgp-nokkel-new-pgp-key/) where private/secret keys, never have, or will be directly exposed on computers connected to the internet.

To achieve this I use physical smart cards and YubiKey.

When changing the setup I also changed my encryption keys, and made a cryptographically signed key transition statement.

The key transition statement can be viewed below and downloaded [here](https://byeskille.no/20180612-key-transition-byeskille7B44C24E6BD4E124-to-byeskilleBA3721AF33FB6D2A-signed.txt).

**Key transition statement:**
```
-----BEGIN PGP SIGNED MESSAGE-----
Hash: SHA512

Date: 2018-06-12

To increase the overall security of my setup, I have started using a new OpenPGP key regularly,
and will be transitioning away from my old one.

I'm transitioning from a more simple setup to a system with master key generated offline,
and where all regular usage is done with subkeys on smartcard.

The old key has not been compromised and will therefore not be revoked.
The old key will expire soon, and I prefer all
future correspondence to come to the new one.

This message is signed by both keys to certify the transition.
I will also introduce the new key to Keybase and other natural places.

The old key was:

pub   4096R0x7B44C24E6BD4E124 2011-06-27
      Key fingerprint = E12F B0A6 293C FEA9 DD83  4A48 7B44 C24E 6BD4 E124

And the new key is:

pub   4096R/0xBA3721AF33FB6D2A 2016-05-28
      Key fingerprint = D901 EA75 C112 A105 2AD9  90B3 BA37 21AF 33FB 6D2A

To fetch the full key from a public key server, you can simply do:

  gpg --keyserver keys.riseup.net --recv-key 'D901EA75C112A1052AD990B3BA3721AF33FB6D2A'

If you already know my old key, you can now verify that the new key is
signed by the old one:

  gpg --check-sigs 'D901EA75C112A1052AD990B3BA3721AF33FB6D2A'

If you don't already know my old key, or you just want to be double
extra paranoid, you can check the fingerprint against the one above:

  gpg --fingerprint 'D901EA75C112A1052AD990B3BA3721AF33FB6D2A'

To verify the integrity of this statement:

  wget -q -O- https://byeskille.no/20180612-key-transition-byeskille7B44C24E6BD4E124-to-byeskilleBA3721AF33FB6D2A-signed.txt | gpg --verify

Please let me know if you have any questions, or problems, and sorry
for the inconvenience.

Øyvind Bye Skille, Oslo 12th of June 2018
-----BEGIN PGP SIGNATURE-----

iQIzBAEBCgAdFiEE+JAV+kkeNkHWAO+AqObKY8Zj3MwFAlsgJVMACgkQqObKY8Zj
3Mzl0g/+O2TzS7EsSobH20uCg7Vtjq0jz362cxUCDWfKwF94YHPY5m214JwY/zGC
etBkTfXnbReE6V0FyiTEMx8fcMmjqWwLl8lm1K8fXPc+VcyuCa8037PuTaB94+At
h8J8P6/zPm7g8U5yi4iX149xZ1oxxMAIL5NlA/Uy6fGc+EzsM/YlVCwg6xgXklIe
KcrAx6dLw6lOVtk77K6IKJIkzwOthbja9KSdTqufi84YKGIJWPqdPKproV5V5WkX
31lTRxtgxFJ1/X1rSfq0oqtF8MGBR77fcIgWakmWRhHKsw942tRzC+ISeN1FhRSd
6dQd/uUgpw341HC+/RfPVm4xWKlRpvR6sVk5OUz33o8uGjdirKS2nlDZ+BZQJ22m
V0qGR3cuTvQCo7137DWlhX3lL4edNifNNBKmoi3Ggi9SQDad5rsnV9Zuw8sZan+M
zpji7ZO7iXshlTOYfu7IS+SbyOFW2xkSw8o7BNqYfKtEx7fmNOJkyJk9WbisDHFV
izieeet2n3F00vBk649se7XeITczsmPr3vWYUaElMFl7txUvY9T99p7JX0EJ53ei
IYwxvMchkgwqbMsl81G4KO5Q9iIlmgN+3AOPKxQ5erVq+hRol2vkM98wWCWvSWY+
WrV2F6yOUiT2+7BL8KayAqruTWnpEGzVvMoJK6ohOlBI00Fe6PSJAjMEAQEKAB0W
IQRh5LnAYkxORlwAByBs2IF8cn46pwUCWyAlUwAKCRBs2IF8cn46pwhtD/wOwJHl
A830pkYZ/n9P304UR92epSM8mhQHOhslfT95cfW6kv7JfvcV6W1/hseBvUzm4wpX
vi8j0gFogVyFODWcNEFLe/qU3cSjrw/t9Pny6huUTkX9Kg9n/xuY4EFTqhLB1nNJ
/WwadhDM7VbK+XS3Y3tlp9u6uKkugQOELwjpZV2D/jOlvyAbwaaQU5aI7kXSSTBi
YtuhYKHwIqFMccL3i3UE/aRTgCevGUSa0Yf3kfh15wLPgdN6PsGg4mtQvg6A3U54
B+anJYrJjgMLmdhPiZK5cRRSgESMvA38HUvKnEYaEO+o+AN1oRJP8+2q0z9g8UGP
8F9mmqrlpfbCA5xNxPWN2Vo4+QV8tzC0e9GOabPbSdeTkD4jCoMAfY/Rpj8gDYBb
+bUJh5SLhDfwzSAnXQeiSPZ3y3zbx8yqYa+Gw5gpDT07KMHxKU1u57AbNH6OJIW7
nQLm+9Pt6k+EXfL0NvLGrcdq/xIqO2a9UbbkcmNXDqd4T6PloGUkBonONQRctJE/
LvfkmfInaMXXwl22m8tJkWcUEHUGHo2yffnHwk3m17nWttZiET8DkEEZwlmzDYk8
CvgTWIHHlkY3JnPmhDlPYG4Ke1QG1Z1XT1iaPL8tQ0aADiyQAKl+EvWuzkWYbVbC
6Y4fmSYV6jK0i37kQcdOXwjy357LbxD2A/8Lig==
=TYR1
-----END PGP SIGNATURE-----
```

## Anonymous communications

### SecureDrop

If you are in a situation where someone might want to reveal you have communications with a journalist, it might be wise to take some extra precautions.

By routing the communications via the tor network, in addition to encryption, you can avoid anyone tracking down any trace the contact took place.

The SecureDrop system make it possible to secure all communications to/from the media organization and/or journalist by routing the traffic via the tor network and using strong encryption.

**Advice: In such a situation I would still advice not to use equipment (computers/mobile phones) or networks connected to the ones who might have an incentive to track down the source (employer/organization etc).**

Do not use your work computer or the mobile phone give to you by your employer. You could also use a network not directly connected to yourself.

If you want to get in touch with me as a journalist with the extra security and possibility to be anonymous, you can submit info via the SecureDrop instance of the NRK:


- Download the Tor browser from __www.torproject.org__
- Visit __www.nrk.no/varsle__
- Send in any info, and label it with my name
