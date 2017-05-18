---
title: "Seuraa provisioita myyntipisteissä myyntiryhmien avulla"
description: "Vähittäismyynnin yleinen käytäntö on myynnin seuranta, jonka tekee asiakkaan kanssa työskennellyt päällikkö – avun tarjoaminen, lisämyynti ja tapahtumien käsittely."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: f92d81512d84b819d411775d67bfa6934642bcb5
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Seuraa provisioita myyntipisteissä myyntiryhmien avulla

[!include[banner](includes/banner.md)]


Vähittäismyynnin yleinen käytäntö on myynnin seuranta, jonka tekee asiakkaan kanssa työskennellyt päällikkö – avun tarjoaminen, lisämyynti ja tapahtumien käsittely.

Myynnin seuraaminen myyntiedustajan mukaan on päällikön myyntitaitojen mitta, kun taas kassamyyjän myynti mitataan nopeuden ja tehokkuuden kautta. Myyntiedustajien myynnin seurantaa käytetään usein myös palkkioiden ja muiden kannustimien laskemiseen.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Työntekijän määrittäminen myyntiedustajaksi myyntipisteessä
Kun työntekijä lisätään myynnin ryhmään, he saavat oikeuden palkkioihin ja hänet voidaan tunnistaa myyntiedustajaksi järjestelmässä. Työntekijä, joka ei ole myyntiryhmässä ei ole oikeutettu palkkioihin ja ei näy myyntiedustajana myyntipistesovelluksessa. Myyntipisteessä myyntiedustajien luettelo johdetaan kaikista myynnin ryhmistä, jotka sisältävät vähintään yhden myymälään määritetyn työntekijän. Luettelo näytetään myyntipisteessä myyntiryhmän tunnuksen ja nimen yhdistelmänä (tunnus: nimi). Oletusmyyntiryhmä voidaan määrittää työntekijöille tukemaan tilanteita, joissa vähittäismyyjä valitsee määrittää myyntiedustajan automaattisesti myyntipisteriveille. Käyttäjät voivat valita kaikista myyntiryhmistä, joihin työntekijä kuuluu.

## <a name="functionality-profile-settings"></a>Toimintoprofiilien asetukset
Myymälälle on useita toimintoprofiilien asetuksia, jotka määrittävät myyntipisteen työnkulun ja prosessin, johon myyntiedustajat kuuluvat.

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Profiili**                           | **Kuvaus**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Oletus kassaan, kun käytettävissä** | Jos tämä asetus on käytössä, myyntipiste täyttää automaattisesti tapahtumarivit nykyisen kassamyyjän oletusmyyntiryhmällä. Jos kassanhoitajalle ei ole määritetty myynnin oletusryhmää, arvoa ei määritetä. Käyttäjä voi silti asettaa myyntiryhmän manuaalisesti käyttämällä myyntipisteen painikeruudukon painiketta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Kysy myyntiedustajaa**   | Tällä vaihtoehdolla on kolme mahdollista arvoa: ** Ei **-Jos tämä vaihtoehto valitaan, käyttäjää ei kehoteta valitsemaan myynnin ryhmää. Arvo voidaan edelleen asettaa käyttämällä kassanhoitajan myyntioletusryhmää tai manuaalisesti käyttämällä myyntipisteen painikeruudukon painiketta. **Tapahtuman alussa** - Jos tämä vaihtoehto on valittuna, ja joko **Oletus kassaan** -asetus ei ole käytössä tai nykyisellä kassalla ei ole myynnin oletusryhmää, käyttäjää pyydetään valitsemaan myyntiryhmä kunkin tapahtuman alussa. Valitsemalla myyntiryhmän tässä kehotteessa kaikki seuraavat rivit lasketaan oletuksena valittuun myynnin ryhmään. Käyttäjä voi silti asettaa myyntiryhmän manuaalisesti käyttämällä myyntipisteen painikeruudukon painiketta. **Kullekin riville** - Jos tämä vaihtoehto on valittuna, ja joko **Oletus kassaan** -asetus ei ole käytössä tai nykyisellä kassalla ei ole myynnin oletusryhmää, käyttäjää pyydetään valitsemaan myyntiryhmä jokaisen rivin lisäämisen jälkeen. Käyttäjä voi silti asettaa myyntiryhmän manuaalisesti käyttämällä myyntipisteen painikeruudukon painiketta. |
| **Vaadi**                           | Tämä vaihtoehto on sovellettava vain, kun myyntipiste on määritetty kysymään myyntiedustajaa. Jos käytössä, käyttäjää vaaditaan valitsemaan myyntiryhmä ennen jatkamista. Muussa tapauksessa käyttäjä saa kehotteen, mutta voi peruuttaa ja jatkaa tekemättä valintaa. Rivin lisäämisen jälkeen käyttäjä, jolla on riittävät oikeudet, voi silti poistaa myyntiryhmän riviltä. "Pyydä myyntiedustajaa" -toimintoa ei pakoteta tässä tilanteessa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Myyntiedustajan tietojen näyttäminen myyntipisteen tapahtumanäytössä
Myyntipisteen tapahtumanäytön asettelu ja sisältö ovat määritettävissä käyttämällä näyttöasettelun suunnittelutoimintoa ja myymälöihin, kassakoneisiin tai työntekijöille määritettyjen näyttöasettelujen avulla. **Myyntiedustaja** -kenttä voidaan lisätä Kuitti-ruudun Rivit-välilehteen.  Tämä näyttää määritetyn myyntiryhmän tunnuksen tapahtumanäytön kullekin riville.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Myyntiedustajatoimintojen lisääminen myyntipisteen painikeruudukoihin
Myyntipisteessä käyttäjät voivat määrittää painikeruudukoita, jotka on sisällytetty näyttöasetteluihin tarjoamaan pääsyn myyntipisteen toimintoihin. Seuraavat myyntiedustajiin liittyvät myyntipisteen toiminnot voidaan määrittää painikeruudukon painikkeisiin.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Toiminto**                             | **Kuvaus**                                                                                                                                                                                                                                                                              |
| Aseta myyntiedustaja riville          | Tämä myyntipistetoiminto näyttää luettelon myymälän kelvollisista myyntiryhmistä (tunnus: nimi). Myyntiryhmän valitseminen tästä listasta asettaa arvon nykyiselle tapahtumariville.                                                                                                            |
| Poista myyntiedustaja riviltä        | Tämä myyntipistetoiminto poistaa nykyisen myyntiryhmän arvon nykyisestä tapahtumarivistä.                                                                                                                                                                                                  |
| Määritä tapahtuman myyntiedustaja   | Tämä myyntipistetoiminto näyttää luettelon myymälän kelvollisista myyntiryhmistä (tunnus: nimi). Myyntiryhmän valitseminen tästä listasta asettaa oletusarvon nykyiselle tapahtumalle. Kaikki olemassa olevat rivit sekä kaikki myöhemmin lisätyt rivit, joihin ei ole määritetty myyntiryhmää, määritetään. |
| Poista tapahtuman myyntiedustaja | Tämä myyntipistetoiminto poistaa nykyisen myyntiryhmän oletusarvon nykyisestä tapahtumasta. Se ei vaikuta tapahtumassa olemassa oleviin riveihin.                                                                                                                             |

## <a name="calculating-commissions"></a>Provisiolaskelmat
Provisio lasketaan työntekijöille määritetyissä myynnin ryhmissä laskelman kirjaamisen tai myyntitilauksen kirjaamisen yhteydessä. Provision määrä määräytyy työntekijän provisio-osuuden mukaan, kuten myyntiryhmässä ja tapahtuman asiakkaan ja/tai tuotteiden liittyvissä provision laskenta-asetuksissa on määritetty.




