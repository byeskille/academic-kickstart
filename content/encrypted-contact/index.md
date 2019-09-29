---
title: Kryptert kontakt
date: 2019-09-18
math: true
diagram: true
markup: mmark
image:
  placement: 3
  caption: 'PGP-oppsett med fysiske smartkort – både YubiKey og kort'
---

Som journalist er det viktig for meg at jeg kan kontaktes sikkert av de som ønsker det.

Jeg har derfor en rekke muligheter for både kryptert og anonym kontakt (f.eks. Signal, Wire, PGP og SecureDrop).

*Om det ikke er behov for spesielt sikker kommunikasjon kan jeg alltids nås raskt via vanlig telefon eller e-post:<br/>
E-post (privat): [oyvind@byeskille.no](mailto:oyvind@byeskille.no)<br/>
E-post (jobb): [oyvind.bye.skille@nrk.no](mailto:oyvind.bye.skille@nrk.no)<br/>
Mobil: +47 41 47 32 20*


## Kryptert

### Signal

Hvis du ikke ønsker å legge igjen for mange spor i teledata kan du kommunisere med meg via den krypterte appen [Signal](https://signal.org/). Den tilbyr tekstmeldinger, taleanrop og videosamtaler.

Signal er en app som sender all kommunikasjon som krypterte datapakker.

Dermed legges det ikke igjen spor i verken telefonregningen eller som data i telenettene som kan si noe om hva som ble kommunisert eller hvem som kommuniserte med hverandre. Signal er kjent for å være basert på åpen kildekode, blir vurdert som sikre krypteringsløsninger og de som tilbyr appen samler inn [minimalt med metadata](https://signal.org/bigbrother/).

Les mer om appen og sikkerhet i et [tidligere innlegg jeg har skrevet](https://byeskille.no/2015/11/sikrere-kommunikasjon-signal/).

**Hvis du vil kommunisere med meg via Signal bruker du mitt telefonnummer:
+47 41473220**

### Wire

En utfordring dog med appen Signal for noen er at man må bruke et mobilnummer for å sette opp appen. Om man ikke ønsker å knytte kontoen for kryptert kommunikasjon så tett til en virkelig identitet kan det dermed være en idé å bruke en annen tjeneste.

En slik annen tjeneste er appen [Wire](https://wire.com/en/).

Wire er ganske lik Signal både i bruk og teknologi. Samtidig er det mulig å registrere en konto knyttet til en e-postadresse og ikke et telefonnummer. Og du trenger ikke dele verken telefonnummer eller e-postadresse med andre for å kunne kommunisere – det holder å dele et brukernavn.

Her er en beskrivelse av hvordan du [setter opp Wire uten telefonnummer](https://medium.com/@wireapp/staying-anonymous-on-wire-22faa13aba4d).

**Om du vil kontakte meg via Wire finner du meg under brukernavnet:<br/>
byeskille**

### Kryptert e-post PGP

For sikker e-post bruk PGP. Min offentlige nøkkel [finner du her](https://www.byeskille.no/byeskille-BA3721AF33FB6D2A.asc.txt), under er litt info om den:
```
4096R/0xBA3721AF33FB6D2A 2016-05-28 [expires: 2020-06-11]
Key fingerprint = D901 EA75 C112 A105 2AD9 90B3 BA37 21AF 33FB 6D2A
uid Øyvind Bye Skille – oyvind.bye.skille @ nrk.no
uid Øyvind Bye Skille – oyvind @ byeskille.no
uid Øyvind Bye Skille – oyvind @ byeskille.net
```

**OBS:** PGP krypterer innholdet i selve e-posten, men ikke emnefeltet (som standard) eller hvem som kommuniserer med hverandre. Dermed vil kryptert e-post lekke noe mer informasjon om noen overvåker netttrafikk.

For kommunikasjon med PGP trenger du min offentlige nøkkel. Den kan også lastes ned fra [Keybase](https://keybase.io/byeskille) eller nøkkeltjenere som [keys.openpgp.org](https://keys.openpgp.org/search?q=oyvind.bye.skille%40nrk.no).

PGP kan også brukes for å kryptere filer som så sendes over andre kanaler enn e-post.

I juni 2018 [gikk jeg selv over til et oppsett for PGP](https://byeskille.no/2018/06/ny-pgp-nokkel-new-pgp-key/) der mine private/hemmelige nøkler, aldri har vært, eller skal være på datamaskiner tilkoblet internett.

For å få til dette bruker jeg fysiske smartkort og YubiKey.

Da jeg byttet krypteringsnøkler laget jeg en kryptografisk signert bekreftelse på overgangen fra gamle til nye krypteringsnøkler (key transition statement).

Den kan sees under og lastes ned [her](https://byeskille.no/20180612-key-transition-byeskille7B44C24E6BD4E124-to-byeskilleBA3721AF33FB6D2A-signed.txt).

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

## Mulighet for helt anonym kommunikasjon

### SecureDrop

Om du er i en situasjon der noen kan ha ønske om å avsløre at du har kontakt med en journalist kan det være lurt å ta ektra sikkerhetshensyn.

Ved å bruke tor-nettverket i tillegg til kryptering vil du da kunne unngå at noen kan spore at kommunikasjonen har skjedd.

Løsningen SecureDrop gjør det mulig å sikre at all kommunikasjonen med mediehuset og/eller journalisten går over tor-nettverket og er kryptert.

**Likevel: Det er viktig at du ikke bruker utstyr (datamaskin/mobiltelefon) eller nettverk som er knyttet til de som kan være ute etter å avsløre kontakten (arbeidsgiver/organisasjon etc).**

Så ikke bruk jobbdatamaskinen eller mobilen du har fått på jobb. Bruk gjerne også et trådløst nettverk som ikke direkte kan kobles til deg.

Om du vil kontakte meg med ekstra sikkerhet og mulighet for å være anonym kan du sende inn informasjon til NRKs SecureDrop:


- Last da ned Tor-nettleseren fra __www.torproject.org__
- Besøk __www.nrk.no/varsle__
- Send inn info og merk innsendelsen med mitt navn
