---
title: Toimitusaikataulut
description: "Toimitusaikataulujen avulla voit seurata tilausrivin määrää, kun käytät useita toimituksia yksittäistä myyntitilausta, myyntitarjousta tai ostotilausta varten."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 701a8b2b94fecedcddada46ad6438448254c8e77
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017

---

# <a name="delivery-schedules"></a>Toimitusaikataulut

[!include[banner](../includes/banner.md)]


Toimitusaikataulujen avulla voit seurata tilausrivin määrää, kun käytät useita toimituksia yksittäistä myyntitilausta, myyntitarjousta tai ostotilausta varten.

Toimitusaikataulua käytetään, kun tilauksen kokonaismäärä tai tarjousrivi pitää toimittaa useissa lähetyksissä. Toimitusrivit edustavat yksittäisiä lähetyksiä. Jos toimitusrivejä on kaksi tai useampi, ne muodostavat yhden toimitusaikataulun. Toimitusriveillä voi olla eri toimituspäiviä, määriä, toimitustapoja ja varastodimensioita, kuten toimipaikka ja varasto.  

**Esimerkki toimitusaikataulusta**

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| Kokonaistilaus (alkuperäinen tilausrivi) | 600 tuolia                               |
| Pyydetty toimitusaikataulu       | 100 tuolia kuukaudessa                     |
| Pyydetty toimituksen aikajakso | 6 kuukautta, kunkin kuukauden ensimmäisenä päivänä |

Tässä skenaariossa asiakas pyytää toimittamaan 600 tuolia 100 tuolin erissä kuuden kuukauden ajan. Voit seurata toimitusvaatimuksia luomalla toimitusaikataulun. Luo Toimitusaikataulu-sivulla kuusi erillistä toimitusriviä. Kullakin toimitusrivillä on 100 tuolia sekä niiden toimituspäivämäärät. Tässä tapauksessa kullekin riville luodaan vastakirjaus kuukauden ensimmäisenä päivänä kuutena peräkkäisenä kuukautena.  

Kun luot toimitusaikataulun, alkuperäisen tilausrivin tyypiksi vaihtuu automaattisesti **Tilausrivi ja monta toimitusta**. Tämäntyyppistä riviä kutsutaan kaupalliseksi riviksi, ja se on merkitty kuvakkeella. Toimitusrivi on merkitty eri kuvakkeella. Jos muutat toimitusrivillä olevaa määrää, kaupalliselle riville päivittyy toimitusaikataulun kokonaismäärä. Jos kauppasopimuksessa tilaukselle on määritetty kokonaisalennus, toimitusaikataulu varmistaa, että tilaus on oikeutettu kokonaisalennukseen, vaikka se jaettaisiinkin erillisiin toimituksiin.  

Tilaukset, joilla on toimitusaikataulu, käsitellään toimitusrivien perusteella. Käsittely sisältää pakkausluetteloiden, tuotteen vastaanottojen ja laskutuksen kirjaamisen.  

Asiakirjatulosteissa tilauksista ja tarjouksista, joilla on toimitusaikataulu, näkyvät vain toimitusrivit. Niillä ei näy alkuperäisiä rivejä (kaupallisia rivejä). **Huomautus:** Lisäksi näkyvät vain toimitusrivit, kun suoritat seuraavat toiminnot:

-   Julkaise
-   kopioit sivuja
-   selaat luettelosivuja ja raportteja.

Kun vahvistat myyntitarjouksia, tuloksena muodostuvissa myyntitilauksissa näkyy koko toimitusaikataulu, myös tilausrivit, joihin sisältyy useita toimituksia. Lisäksi koko toimitusaikataulu näkyy kaikilla tärkeimmillä sivuilla, kuten myyntitilauksissa, myyntitarjouksissa ja ostotilauksissa.



