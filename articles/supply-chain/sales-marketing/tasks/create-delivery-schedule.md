---
title: Toimitusaikataulun luominen
description: Tässä osoitetaan, miten myyntitilaukselle luodaan toimitusaikataulu.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dccc90321977382c7625ca1785427a6d26a14f27
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835626"
---
# <a name="create-delivery-schedule"></a>Toimitusaikataulun luominen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä osoitetaan, miten myyntitilaukselle luodaan toimitusaikataulu. Toimitusaikataulua käytetään, kun tilauksen määrä tai tarjous pyydetään toimittamaan useissa lähetyksissä. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.


## <a name="create-delivery-schedule"></a>Toimitusaikataulun luominen
1. Siirry Kaikki myyntitilaukset -kohtaan.
2. Valitse Uusi.
3. Syötä tai valitse arvo Asiakastili-kentässä.
4. Valitse OK.
5. Syötä tai valitse arvo Nimiketunnus-kentässä.
6. Syötä Määrä-kenttään lukua 1 suurempi arvo.
7. Valitse myyntitilausrivi.
8. Valitse Toimitusaikataulu.
    * Toimitusaikataulu-sivulla voi määrittää asiakkaalle toimitettavan tilausrivin kokonaismäärän lähetysten määrän.    
    * Oletusarvoisesti järjestelmä kopioi alkuperäisen myyntirivin kokonaismäärän ja muut toimitustiedot ensimmäiselle toimitusaikatauluriville. Tässä esimerkissä luodaan kaksi lähetystä sisältävä aikataulu. Toisen lähetyksen päivämäärä on viikon kuluttua ensimmäisen lähetyksen päivämäärästä.  
9. Syötä Määrä-kenttään luku, joka on osa kokonaismäärää.
10. Valitse Uusi.
11. Syötä jäljellä oleva määrä Määrä-kenttään.
12. Syötä Pyydetty lähetyspäivämäärä -kenttään päivämäärä, joka on viikon kuluttua ensimmäisen toimitusrivin päivämäärästä.
    * Kulujen muunto -pikavälilehden kaksi vaihtoehtoa ohjaavat sitä, miten kulut jaetaan toimitusaikatauluriveille sen jälkeen, kun ne on liitetty alkuperäiseen tilausriviin. Jos valitset Kopioi bruttosummat, jokaiselle riville kopioidaan sama kulusumma. Kohdista toimitusriveille -vaihtoehto jakaa kulun tasaisesti kaikille toimitusriveille.  
    * Vain kiinteät kulut voidaan jakaa. Muuttuvat kulut kopioidaan yhä riveille.  
13. Siirrä kohdistin pois toiselta toimitusriviltä, jolloin sivu päivittyy.
    * Voit seurata toimitusaikatauluriveille kohdistettua kokonaismäärää Summa- ja Jäljellä-kentän avulla. Kun jäljellä oleva summa on nolla, alkuperäisen rivin kokonaismäärä on kohdistettu aikatauluun.   
14. Valitse OK.
    * Toimitusaikataulu on nyt kopioitu tilausriveille.   
    * Alkuperäinen tilausrivi, jota sanotaan kaupalliseksi riviksi, on muunnettu tilausriviksi, jolla on useita toimituksia. Se merkitään erillisellä kuvakkeella ja toimii toimitusrivien otsikkona.  
    * Kaksi uutta riviä, joita sanotaan toimitusriveiksi, muodostavat toimitusaikataulun. Tilaus käsitellään alkuperäisen rivin sijaan näiden rivien avulla. Jos tulostettuna on asiakirjoja, kuten vahvistus-, keräys- tai pakkausluettelot, vain toimitusrivit näytetään.   
    * Toimitusriveillä on eri toimituspäiviä, määriä, toimitustapoja ja varastodimensioita, kuten toimipaikka ja varasto. Tuotedimensioiden on kuitenkin aina vastattava kaupallisen rivin arvoja. Niitä ei voi muuttaa.  
15. Syötä Määrä-kenttään nykyistä lukua suurempi arvo.
16. Valitse kaupallinen rivi, kun haluat nähdä tilanteen määrän uudelleenlaskemisen jälkeen.
17. Valitse toimintoruudussa Kerää ja pakkaa.
18. Valitse Kirjaa pakkausluettelo.
19. Laajenna Parametrit-osa.
20. Valitse Määrä-kentässä Kaikki.
    * Huomaa, että pakkausluettelo luodaan kahdelle toimitusaikatauluriville, ei alkuperäiselle tilausriville.  
21. Valitse Tulosta pakkausluettelo -kentässä Kyllä.
22. Valitse OK.
23. Valitse Kyllä.
24. Sulje sivu.

