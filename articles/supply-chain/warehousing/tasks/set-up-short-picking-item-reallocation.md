---
title: Nimikkeen uudelleenkohdistussääntöjen määrittäminen lyhyttä keräilyä varten
description: Tässä artikkelissa kuvataan, miten varastotyöntekijöille annetaan mahdollisuus löytää vaihtoehtoinen sijainti nopeasti, jos sijainnissa, johon heidät on ohjattu ei ole riittävää varastoa.
author: Mirzaab
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4e6d7f9b09434346cb0f3670d10437ef8197822
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875011"
---
# <a name="set-up-short-picking-item-reallocation"></a>Nimikkeen uudelleenkohdistussääntöjen määrittäminen lyhyttä keräilyä varten

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kuvataan, miten varastotyöntekijöille annetaan mahdollisuus löytää vaihtoehtoinen sijainti nopeasti, jos sijainnissa, johon heidät on ohjattu ei ole riittävää varastoa. 

Uudelleenkohdistamista hallitaan **Työpoikkeuksella**, jota **Varastotyöntekijä** käyttää.

On mahdollista käyttää automaattista, manuaalista tai molempia uudelleenkohdistamisprosesseja:

- Automaattinen uudelleenjako - Sijaintidirektiivien avulla määritetään, ovatko tavarat käytettävissä toisessa sijainnissa. Jos mahdollista, työ päivitetään ja varaston käyttäjä ohjataan vaihtoehtoiseen sijaintiin.
- Manuaalinen uudelleenkohdistus - Sallii varaston käyttäjän valita yhdestä tai useasta paikasta, joissa on varaukseton määrä tavaroita. 
- Automaattinen ja manuaalinen - Jos järjestelmä ei pysty suorittamaan automaattista uudelleenkohdistamista ja sijainnit ovat käytettävissä varauksettoman määrän kanssa, käyttäjää pyydetään valitsemaan sijainti.

## <a name="set-up-work-exceptions"></a>Määritä työn poikkeukset
On mahdollista määrittää useita työn poikkeuksia, joilla on eri nimikkeen uudelleenkohdistuskäytännöt, joista varaston työntekijä voi valita käsittelyssä olevan lähetyksen tarpeisiin sopivan.

Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.

1. Siirry **siirtymisruudussa** kohtaan **Varastonhallinta > Asetukset > Työ-> Työn poikkeukset**.
2. Valitse **Uusi**. 
3. Kirjoita **Työn poikkeuskoodi** -kenttään arvo. Tämä on tämän poikkeuksen otsikko. Esimerkiksi, Lyhyt keräily käsin.
4. Kirjoita **Kuvaus**-kenttään arvo. Tämä on lyhyt kuvaus tämän poikkeuksen käytöstä. Esimerkiksi Lyhyt poiminta -nimike ei ole käytettävissä.
5. Valitse **Poikkeus**-tyyppi-kenttään **Lyhyt keräily**.
6. Valitse **Varaston oikaiseminen** -valintaruutu. Jos se valitaan, varaston arvoksi asetetaan automaattisesti 0 lyhyen keräilyn sijainnissa.
7. Syötä tai valitse arvo **Oikaisutyypin oletuskoodi** -kentässä. Esimerkiksi kohteessa USMF voit valita **Poista var. muk. lähtevä**. Kukin oikaisutyyppikoodi sisältää neljä ominaisuutta: nimi, kuvaus, varastokirjauskansion nimi ja **Poista varaukset**. Jos **Poista varaus** on käytössä, lyhyen poimitun tilausrivin varaukset poistetaan.  
8. Valitse **Nimikkeen uudelleenkohdistus** -kentässä arvo, kuten Manuaalinen. Jos valitset asetukseksi Manuaalinen tai Automaattinen ja manuaalinen, varastotyöntekijän on voitava käyttää manuaalista uudelleenkohdistusta.

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Määritä manuaalinen nimikkeiden uudelleenkohdistus työntekijän käyttöön

Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.

1. Sulje sivu.
2. Siirry **siirtymisruudussa** kohtaan **Varastonhallinta > Asetukset > Työntekijä**.
3. Valitse **Muokkaa**.
4. Valitse luettelosta työntekijä. Esimerkiksi Julia Funderburk.
5. Laajenna **Käyttäjät**-pikavälilehti.
6. Valitse luettelosta **Käyttäjätunnus**. Esimerkki: 24.
7. Laajenna **Työ**-pikavälilehti.
8. Valitse **Salli manuaalinen nimikkeen uudelleenkohdistus** -kentässä **Kyllä**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]