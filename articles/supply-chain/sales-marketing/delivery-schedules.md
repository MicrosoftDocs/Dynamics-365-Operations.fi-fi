---
title: Toimitusaikataulut
description: Toimitusaikataulujen avulla voit seurata tilausrivin määrää, kun käytät useita toimituksia yksittäistä myyntitilausta, myyntitarjousta tai ostotilausta varten.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfc9467e6c7df70ce749f531bab447513ea3349e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998575"
---
# <a name="delivery-schedules"></a>Toimitusaikataulut

[!include [banner](../includes/banner.md)]

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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]