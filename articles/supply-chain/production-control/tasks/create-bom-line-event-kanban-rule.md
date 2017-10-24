--- 
title: "Luo tuoterakennerivitapahtuman kanban-sääntö"
description: "Tehtävässä keskitytään määrityksiin, jotka tarvitaan tapahtuman kanban-säännön luomiseen, jotta voidaan varmistaa toimitukset tuotannon tuoterakenneriveille lean-menetelmiä ja perinteisiä menetelmiä yhdistävässä tuotantoympäristössä."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 452cc5cf6060b71f91ad43e39e756dc23d759448
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-bom-line-event-kanban-rule"></a>Luo tuoterakennerivitapahtuman kanban-sääntö

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tehtävässä keskitytään määrityksiin, jotka tarvitaan tapahtuman kanban-säännön luomiseen, jotta voidaan varmistaa toimitukset tuotannon tuoterakenneriveille lean-menetelmiä ja perinteisiä menetelmiä yhdistävässä tuotantoympäristössä. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF. Tehtävä on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun tuotteen tuotannon valmisteluun.


## <a name="create-a-new-kanban-rule"></a>Luo uusi kanban-sääntö
1. Valitse Tuotannonhallinta > Kausittaiset tehtävät > Kanban-määrän laskeminen > Kanban-säännöt.
2. Valitse Uusi.
3. Valitse Tyyppi-kentän arvoksi "Otto".
    * Otto-tyyppiä käytetään siirtokanbanien luomiseen.  
4. Valitse Täydennysstrategia-kentässä Tapahtuma.
    * Tapahtumastategia valitaan, jotta kanbanien siirto voidaan tehdä tapahtuman perusteella. Strategia käynnistetään myöhemmin tehtäväoppaassa tuotantotilauksen arvioinnilla.  
5. Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.
    * Anna tai valitse ReplenishSpeakerComponents. Siirtotehtävällä on vastaanottava (tulos-)varasto ja toimipaikka 12, minkä vuoksi materiaalin siirretään varaston 12 toimipaikkaan 12.  
6. Laajenna Tiedot-osa.
7. Anna tai valitse Tuote-kenttän arvoksi M0001.
8. Laajenna Tapahtumat-osa.
9. Valitse Tuotantotilausrivin tapahtuma -kentässä Automaattinen.
    * Kun tuoterakennerivin tapahtumakentän arvo on Automaattinen, kanban luodaan täyttämään tuotantotilauksen tuoterakennerivien materiaalitarpeet.  
10. Sulje sivu.

## <a name="create-and-modify-a-new-production-order"></a>Luo ja muokkaa uusi tuotantotilaus
1. Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.
2. Valitse Uusi tuotantotilaus.
3. Syötä tai valitse arvo Nimiketunnus-kentässä.
    * Kirjoita tai valitse L0001. Nimikettä L0001 käytetään, koska nimike M0001 sisältyy nimikkeen L0001 nimikkeen tuoterakenteeseen.  
4. Valitse Luo.
5. Napsauta luettelossa L0001-rivillä olevaa linkkiä
6. Valitse Tuoterakenne.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Valitse Muokkaa.
9. Valitse Rivin tyyppi -kenttään "Tarvekohdistuksen tarjonta".
    * Tarvekohdistuksen tarjonta valitaan käynnistämään kanbanin toimitusten luonti.  
10. Valitse Resurssin kulutus -kentässä Ei.
    * Resurrsin kulutus -valintaruudun merkinnän poistamalla voit vaihtaa varastoa.  
11. Laajenna Varaston dimensiot -osa.
12. Syötä Varasto-kenttään 12.
    * Varastoksi on määritetty 12, koska se on ottotehtävän tulosvarasto.  
13. Syötä Toimipaikka-kenttään arvo 12.
    * Toimipaikaksi on määritetty 12, koska se on ottotehtävän tulostoimipaikka.  
14. Sulje sivu.
15. Sulje sivu.

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a>Arvioi tuotantotilaus ja näytä luotu kanban
1. Valitse Arvio.
    * Tuotantotilauksen arviointi käynnistää liittyvässä kanbanissa nimikkeen M0001 toimituksen luonnin.  
2. Valitse OK.
3. Sulje sivu.
4. Sulje sivu.
5. Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse nimikkeelle M0001 luotu tapahtuman kanban-sääntö.  
7. Laajenna Kanbanit-osa.
8. Merkitse valittu rivi luettelossa.
    * Huomaa kanban, joka on luotu toimittamaan M0001 arvioituun tuotantotilaukseen.  
    * Tämä on viimeinen vaihe!  


