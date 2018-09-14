--- 
title: "Määritä konttiinpakkaus"
description: "Tässä menettelyssä kuvataan, kuinka voit automatisoida kuormien konttiinpakkauksen Varastonhallinnassa."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: aeb7d956560c513c08d5e20dcf20989b49137a52
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-containerization"></a>Määritä konttiinpakkaus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kuvataan, kuinka voit automatisoida kuormien konttiinpakkauksen Varastonhallinnassa. Automaattinen konttiinpakkaus luo lähetyksille kontit ja keräilytyöt kun aalto käsitellään, ja työrivit voidaan jakaa määriin, jotka sopivat kontteihin. Tämän avulla varastotyöntekijän voivat keräillä nimikkeet suoraan valittuun konttiin. Manuaaliseen pakkauskäsittelyyn verrattuna järjestelmä automatisoi tehtäviä, kuten konttien luonnin, nimikkeiden liittämisen ja konttien sulkemisen. Tässä menettelyssä käytetään esittely-yritystä USMF, ja sen suorittaa varastopäällikkö.


## <a name="set-up-a-wave-template"></a>Aaltomallin asetuksien määrittäminen
1. Valitse Varastonhallinta > Asetukset > Aallot > Aaltomallit.
2. Valitse Uusi.
3. Syötä Aaltomallin nimi -kenttään arvo.
4. Kirjoita Aaltomallin kuvaus -kenttään arvo.
5. Syötä tai valitse arvo Toimipaikka-kenttään.
6. Anna tai valitse Varasto-kentässä arvo.
7. Laajenna Menetelmät-osa.
    * Valitut menetelmät -ruudussa näkyvät valitun aaltomallin tyypin menetelmät. Aaltomallin on sisällettävä pakkaa konttiin -menetelmä.  
8. Etsi haluamasi tietue luettelosta ja valitse se.
9. Kirjoita arvo Aallon vaihekoodi -kenttään.
    * Kirjoita aaltovaiheen koodi lisätylle menetelmälle, joka voi olla mikä tahansa koodi. Voit lisätä menetelmän useammin kuin kerran ja määrittää sille eri aaltovaiheen koodit. Valitse tällöin Toistettava-asetus tälle menetelmälle Aallon käsittelymenetelmät -sivulla  
10. Valitse Tallenna.
11. Sulje sivu.

## <a name="set-up-a-container-type"></a>Määritä konttityyppi
1. Valitse Varastonhallinta > Asetukset > Kontit > Konttityypit.
    * Voit määrittää haluamasi kontit Konttityypit-sivulla. Voit määrittää konttien fyysiset dimensiot, kuten taarapainon, enimmäispainon, enimmäistilavuuden, pituuden, leveyden ja korkeuden. Tässä esimerkissä on kolmea eri kokoista laatikkoa.  
2. Valitse Uusi.
3. Kirjoita arvo Konttityyppi-kenttään.
4. Syötä Taarapaino-kenttään numero.
5. Lisää Enimmäispaino-kenttään numero.
6. Syötä Tilavuus-kenttään numero.
7. Lisää Pituus-kenttään numero.
8. Kirjoita Leveys-kenttään numero.
9. Kirjoita Korkeus-kenttään numero.
10. Kirjoita arvo Kuvaus-kenttään.
11. Valitse Tallenna.
12. Valitse Uusi.
13. Kirjoita arvo Konttityyppi-kenttään.
14. Kirjoita arvo Kuvaus-kenttään.
15. Syötä Taarapaino-kenttään numero.
16. Lisää Enimmäispaino-kenttään numero.
17. Syötä Tilavuus-kenttään numero.
18. Lisää Pituus-kenttään numero.
19. Kirjoita Leveys-kenttään numero.
20. Kirjoita Korkeus-kenttään numero.
21. Valitse Tallenna.
22. Valitse Uusi.
23. Kirjoita arvo Konttityyppi-kenttään.
24. Kirjoita arvo Kuvaus-kenttään.
25. Syötä Taarapaino-kenttään numero.
26. Lisää Enimmäispaino-kenttään numero.
27. Syötä Tilavuus-kenttään numero.
28. Lisää Pituus-kenttään numero.
29. Kirjoita Leveys-kenttään numero.
30. Kirjoita Korkeus-kenttään numero.
31. Valitse Tallenna.
32. Sulje sivu.

## <a name="set-up-a-container-group"></a>Määritä konttiryhmä
1. Valitse Varastonhallinta > Asetukset > Kontit > Konttiryhmät.
2. Valitse Uusi.
    * Voit määrittää konttityyppien loogiset ryhmät. Voit määrittää kullekin ryhmälle konttien pakkausjärjestyksen ja prosenttiosuuden, jonka perusteella kontit täytetään. Nimikkeen kokodimensiota käytetään määrittämään, onko kontissa tilaa. Järjestelmä valitsee kontin, jonka kokodimensiot ovat lähimpänä nimikettä. Jos ryhmässä on useita konttityyppejä, suosittelemme, että järjestät järjestyksen koon mukaan niin, että suurin kontti on ensimmäinen, numero 1 sarjassa, ja pienin kontti on viimeinen.    
3. Kirjoita Konttiryhmän tunnus -kenttään arvo.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Uusi.
6. Merkitse valittu rivi luettelossa.
7. Anna tai valitse arvo Konttityyppi -kentässä.
8. Valitse Uusi.
9. Merkitse valittu rivi luettelossa.
10. Anna tai valitse arvo Konttityyppi -kentässä.
11. Valitse Uusi.
12. Merkitse valittu rivi luettelossa.
13. Anna tai valitse arvo Konttityyppi -kentässä.
14. Valitse Tallenna.
15. Sulje sivu.

## <a name="set-up-a-container-build-template"></a>Aseta kontin muodostusmalli
1. Valitse Varastonhallinta > Asetukset > Kontit > Kontin rakennusmallit.
2. Valitse Uusi.
    * Kontin rakennusmalli perustuu suoritettavaan konttiinpakkauksen prosessiin. Kukin kontin rakennusmalli määrittää yhden konttiinpakkauksen prosessin, jota käytetään aaltomallissa. Muokkaa kyselyä -komennon avulla voit määrittää ehdot, jonka perusteella valittu malli käsitellään. Voit esimerkiksi haluta suorittaa konttiinpakkauksen vain tietyille asiakkaille, tuotteille tai varastoille, tai voit lisätä vastaavan kyselyalueen malliin. Kontin rakennusmalli linkitetään aaltomallin vaiheisiin Aallon vaihekoodi -kentän avulla. Kun aalto suoritetaan, se määrittää, mitä kontin rakennusmalleja käytetään konttiinpakkauksen aloittamiseen. Peruskyselytyyppi-kenttä määrittää pakattavat kohteet ja suodattimen perusteen.  
3. Merkitse valittu rivi luettelossa.
4. Kirjoita Konttimallin tunnus -kenttään arvo.
5. Anna tai valitse Konttiryhmän tunnus -kentässä arvo.
6. Kirjoita arvo Aallon vaihekoodi -kenttään.
7. Merkitse Salli jaetut keräilyt -valintaruutu.
8. Valitse Tallenna.
9. Napsauta Säilön yhdistämisrajoitukset -kohtaa.
    * Yhdistämislogiikan keskeytysten avulla voit määrittää sääntöjä pakkauksen kohdistusriveille konteissa. Jos esimerkiksi lisäät Nimiketunnus-kentän, kun nimikkeet on liitetty kontteihin, luodaan uusi kontti aina silloin, kun kohdataan uusi nimiketunnus. Tämä estää työntekijöitä pakkaamasta kahden eri asiakkaan kohdistusrivejä samaan konttiin.  
10. Valitse Uusi.
11. Valitse vaihtoehto Taulukko-kentässä.
12. Syötä tai valitse arvo Kentän valinta -kentässä.
13. Valitse OK.


