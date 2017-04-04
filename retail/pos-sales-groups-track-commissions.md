---
title: "Seurata avulla myyntiryhmät POS palkkiot"
description: "Vähittäismyynnin yleinen käytäntö osakkuusyrityksen joka asiakkaan kanssa myynnin seurantaa on – tarjoaa apua ylös-myydä ja cross-myy tapahtuman käsittely."
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
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dfefdede8f3bc884b230109d6c915127a1361ecd
ms.lasthandoff: 03/31/2017


---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Seurata avulla myyntiryhmät POS palkkiot

Vähittäismyynnin yleinen käytäntö osakkuusyrityksen joka asiakkaan kanssa myynnin seurantaa on – tarjoaa apua ylös-myydä ja cross-myy tapahtuman käsittely.

Mittaa kykyjä myy associates, seuranta myynti myyntiedustajan mukaan on, kun kassa myynti on toimenpide, nopeuden ja tehokkuuden. Myynti myyntiedustajan seurannut käytetään usein myös laskea palkkiot tai muita kannustimia.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Työntekijän on POS Myyntiedustaja määrittäminen
Kun työntekijä lisätään myynnin ryhmään, pääset osalliseksi komission ja tunnistaa myyntiedustajaksi järjestelmään. Työntekijä, joka ei ole Myynti-ryhmässä ei ole oikeutettu komission ja ei näy myynti (POS) kohdistuspisteen myyntiedustajaksi. POS-myyntiedustajien luettelon johdetaan myynnin ryhmiä, jotka sisältävät vähintään yhden työntekijän myymälään. Luettelossa näkyy POS yhdistelmänä myynti Ryhmätunnus ja nimi (ID: nimi). Oletus myyntiryhmälle voidaan määrittää työntekijöille tukea tilanteissa, joissa vähittäismyyjän valitsee automaattisesti asettaa Myyntiedustaja POS riveille. Käyttäjät voivat valita kaikki, jotka työntekijä on jäsenenä myyntiryhmän.

## <a name="functionality-profile-settings"></a>Toimintojen asetukset
Useilla myymälän, jotka määrittävät työnkulku ja prosessin, joihin liittyy myyntiedustajien POS-toimintoja profiiliasetukset.

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Profile**                           | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Default to cashier when available** | Jos tämä asetus on käytössä, POS täyttäminen automaattisesti tapahtumarivit nykyisen kassa oletusryhmä myynnin kanssa. Kassanhoitaja ei ole määritetty myynnin oletusryhmä, jos arvoa ei voi määrittää. Käyttäjä voi asettaa myyntiryhmä manuaalisesti käyttämällä POS-painiketta ruudukko-painike.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Prompt for sales representative**   | Tämä vaihtoehto on kolme mahdollista arvoa: ** ei **-Jos tämä vaihtoehto valitaan, käyttäjää ei kehoteta myynnin ryhmä. Arvo saattaa edelleen myynti kassa oletusryhmä avulla tai manuaalisesti käyttämällä POS painike ruudukossa. **Käynnistä tapahtuman** - Jos tämä vaihtoehto on valittuna, ja joko **oletus kassa** -asetus ei ole käytössä tai nykyisen kassa ei ole myynti oletusryhmä, käyttäjää pyydetään valitsemaan myyntiryhmä alussa kunkin tapahtuman. Valitsemalla Myynti ryhmän kehotteen oletusarvoisesti kaikki seuraavat rivit valitun myynnin ryhmään. Käyttäjä voi asettaa myyntiryhmä manuaalisesti käyttämällä POS-painiketta ruudukko-painike. **Kullekin riville** - Jos tämä vaihtoehto on valittuna, ja joko **oletusarvo on kassa** -asetus ei ole käytössä tai nykyisen kassa ei ole myynti oletusryhmä, käyttäjää pyydetään valitsemaan Myynti ryhmän kunkin rivin lisäämisen jälkeen. Käyttäjä voi manuaalisesti määrittää myyntiryhmän POS-painiketta ruudukko-painike. |
| **Edellyttävät**                           | Tämä vaihtoehto on vain sovellettavan POS on määritetty kysymään myyntiedustajalle. Jos käytössä, käyttäjä edellyttää Myynti ryhmän valitseminen ennen jatkamista. Muussa tapauksessa käyttäjää pyydetään, mutta voit peruuttaa ja jatkaa tekemättä valintaa. Rivin lisäämisen jälkeen käyttäjä, jolla on riittävät oikeudet voi silti poistaa myyntiryhmä riviltä. Tämä tilanne ei säilytetä "Vaadi Myyntiedustaja".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>POS-näytön tapahtumat myynti myyntiedustajan tietojen näyttäminen
Myyntipisteen tapahtuman näytön asettelu ja sisältö ovat määritettävissä näytön asettelun suunnittelun ja määritetty näytön asettelut kaupat, kassakoneet tai työntekijöiden avulla. **Myynti edustaja** Kuitti-ruudusta rivit-välilehdessä voi lisätä kenttään.  Määritettyä myyntiryhmän kunkin rivin tunnus näkyy näytössä tapahtumaa.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Lisäämällä myyntiä edustava Myyntipisteen toimintoja painiketta ristikot
POS käyttäjät painikeruudukot, jotka sisältyvät pääsy Myyntipisteen toimintoja näytön asettelun määrittämiseen. Painikeruudukon painikkeet, jotka koskevat Myyntiedustajat voidaan määrittää Myyntipisteen seuraavat toiminnot.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Toiminto**                             | **Description**                                                                                                                                                                                                                                                                              |
| Aseta myyntiedustaja riville          | POS-toiminto näyttää luettelon tukikelpoisista Myynti-ryhmiä (ID: nimi) myymälän. Myyntiryhmän valitsemalla tästä luettelosta asettaa nykyisen tapahtumarivin.                                                                                                            |
| Poista myyntiedustaja riviltä        | POS-toiminto poistaa nykyisen myynti ryhmän arvo nykyisen tapahtumarivin.                                                                                                                                                                                                  |
| Määritä Myyntiedustaja-tapahtuman   | POS-toiminto näyttää luettelon tukikelpoisista Myynti-ryhmiä (ID: nimi) myymälän. Myyntiryhmän valitsemalla tästä luettelosta määrittää oletusarvon valitun tapahtuman. Set samoin kuin myöhemmin lisätyt rivit on määritetty myyntiryhmä ilman kaikki olemassa olevat rivit. |
| Poista tapahtuman Myyntiedustaja | POS-toiminto poistaa nykyisen tapahtuman nykyisen myynti ryhmän oletusarvo. Se ei vaikuta aiemmin tapahtumassa kaikki rivit.                                                                                                                             |

## <a name="calculating-commissions"></a>Provisioiden laskemiseen
Provisio lasketaan työntekijöiden määritetty myynnin ryhmissä laskelman kirjaamisen tai myyntitilauksen kirjaamisen yhteydessä. Provision määrä määräytyy työntekijän Provisio-osuus perustuu myyntiryhmä ja asiakkaan ja/tai tuotteiden tapahtumaan liittyvän komission laskenta-asetukset.


