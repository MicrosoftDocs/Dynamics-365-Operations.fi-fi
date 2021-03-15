---
title: Toimitusaikataulun luominen
description: Tässä osoitetaan, miten myyntitilaukselle luodaan toimitusaikataulu.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa9539ce92297a3b4f22ac18af79fdea98759e49
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991837"
---
# <a name="create-delivery-schedule"></a>Toimitusaikataulun luominen

[!include [banner](../../includes/banner.md)]

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]