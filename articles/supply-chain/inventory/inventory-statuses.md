---
title: Varaston tilat
description: "Tässä artikkelissa kuvataan, miten varaston tiloja voidaan käyttää varaston luokittelussa ja seuraamisessa."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5caa5620db428f18d451fdfe2aeae9e2a76a24f8
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="inventory-statuses"></a>Varaston tilat

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan, miten varaston tiloja voidaan käyttää varaston luokittelussa ja seuraamisessa.

Voit käyttää varaston tilaa luokitellaksesi varaston. Sitten voit aloittaa asianmukaiset toiminnot, kuten täydennys tai poislaitettava työ.

Seuraavassa on esimerkkejä tavoista, joilla voit käyttää varaston tiloja:

-   Luo varaston tiloja käytettävissä olevalle varastolle, saapuville tapahtumille ja lähteville tapahtumille.
-   Määritä varaston oletustila varastotapahtumille.
-   Muuta nimikkeiden varastotilaa ennen saapumista, saapumisen yhteydessä tai kun nimikkeet sijoitetaan pois varastosiirrossa.
-   Käytä varaston tilaa niiden nimikkeiden hinnoitteluun, jotka palautetaan ja suunnitellaksesi nimikkeiden kattavuuden pääsuunnittelun aikana.

Varaston tila on yksi varastodimensioryhmän dimensioista. Varaston tiloja voidaan luokitella käytettävissä oleviin ja ei-käytettävissä oleviin ja voit käyttää **Varaston esto** -parametria estämään nimikkeet, joilla on ei-käytettävissä oleva varaston tila. Toimituskiellossa olevien nimikkeiden katsotaan olevan osa fyysistä varastoa, eikä niitä vodai käyttää tuotantotilauksessa, myyntitilauksessa, siirtotilauksessa tai lähtevässä tapahtumassa.

Voit käyttää saapuville töille varastonimikkeitä, joiden varastotila on joko käytettävissä tai ei käytettävissä. Voit luoda esimerkiksi käytettävissä oleville tilan, jonka nimi on **Valmis**, ei-käytettävissä oleville tilan, jonka nimi on **Vioittuneet** ja toimituskiellossa oleville tilan, jonka nimi on **Suljettu**. Luodessasi ostotilauksen vastaanotetuille tai palautetuille nimikkeille, jos mitkään nimikkeet ovat vahingoittuneita tai rikkoutuneita, voit muuttaa niiden varaston tilan **Vioittuneet**-ostotilauksen rivillä. Sen jälkeen, kun nimikkeet on otettu vastaan, tilaksi määritetään automaattisesti **Suljettu**. Jos skannaat vioittuneet nimikkeet mobiililaitteella, Microsoft Dynamics 365 for Finance and Operations voi käyttää sijainnin direktiivejä ja työn malleja näyttämään tietoja sopivasta sijainnista tai ne sijainnit, jossa voit poispanna kyseiset nimikkeet. Palautetuille nimikkeille luodaan jakelutyyppi **Varaus** **Varastotapahtumat** -lomakkeessa.

Ulosmeneville töille käytetään nimikkeitä, joilla on saatavilla oleva varaston tila. Jos on nimikkeitä, joiden tila on **Rikkoutunut** ja pääsuunnittelu suoritetaan näillä nimikkeillä, niitä pidetään puuttuvina ja varasto täydennetään automaattisesti.

Kun olet määrittänyt varaston tilat, voit määrittää varaston oletustilan toimipaikalle, nimikkeelle ja varastolle. Voit myös määrittää oletustilan myyntiin, siirtoon ja ostotilauksiin. Myyntitilausten ja lähtevien siirtotilausten oletustilassa **Varastonesto**-asetus ei voi olla asennossa **Kyllä**. Varaston tila, joka periytyy toimipaikan, varaston, nimikkeen, ostotilauksen, siirtotilauksen tai myyntitilauksen oletusarvoasetuksista, voidaan muuttaa käyttämällä mobiililaitetta tai ostotilauksessa, myyntitilauksessa tai siirtotilausrivillä.

Suunnitellaksesi kattavuusryhmän nimikkeille, joiden varastotila on käytettävissä oleva, valitse **Kattavuussuunnitelma dimension mukaan** -vaihtoehto varastodimensiolle **Varastodimensioryhmät** -sivulla. Avatessasi **Nimikkeen kattavuus**-ohjatun toiminnon, nimikkeet, joilla on käytettävissä oleva tila, näkyvät **Tila**-sivulla. Luo näille nimikkeille kattavuusasetukset valitsemalla saatavilla oleville varastotiloille varastotilatunnus. Kattavuusasetusten perusteella voit laskea nimikevaatimukset sekä käytettävissä olevien nimikkeiden tarjonnan ja kysynnän ennusteen pääsuunnittelun aikana. Et voi luoda nimikkeen kattavuusasetusta, jolla on toimituskiellossa oleva varastotila. Vaihtoehtoisesti, voit käyttää **Nimikekattavuus** -sivua nimikkeen kattavuusparametrien luomiseen tai muokkaamiseen.

