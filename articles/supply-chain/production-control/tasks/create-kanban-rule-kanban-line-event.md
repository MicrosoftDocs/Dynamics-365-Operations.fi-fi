---
title: Luo kanban-sääntö käyttämällä kanban-rivitapahtumaa
description: Tämä menettely luo kanban-säännön vetämällä prosessitoiminnosta kanban-rivitapahtuman asetuksen avulla.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b8f56877d499efa6bd635b4d8b5f7dc78a7f78ae
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147040"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a>Luo kanban-sääntö käyttämällä kanban-rivitapahtumaa

[!include [banner](../../includes/banner.md)]

Tämä menettely luo kanban-säännön vetämällä prosessitoiminnosta kanban-rivitapahtuman asetuksen avulla. Kanban-sääntö käynnistyy kanban-prosessitehtävästä, jonka kumpikin määrä on vähintään 25. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF. Tämä tehtävä on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun tuotteen tuotannon valmisteluun lean-ympäristössä.


## <a name="create-a-kanban-rule"></a>Luo kanban-sääntö
1. Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.
2. Valitse Uusi.
3. Valitse Täydennysstrategia-kentässä Tapahtuma.
    * Tämä luo kanbanit suoraan tarpeen mukaan. Sitä käytetään asettamaan sääntöjä, joilla määritetään tilaukselle valmistamisen skenaario.  
4. Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.
    * Anna tai valitse SpeakerAssemblyAndPolish. Valmistuksen kanban-säännön ensimmäinen tehtävä on tuotantovirran prosessitehtävä. Kun valitset tehtävän, tehtävän voimassaolopäivämäärät kopioidaan kanban-säännön voimassaolopäivämääriin.  
5. Laajenna Tiedot-osa.
6. Kirjoita Tuote-kentän arvoksi L0001.
7. Laajenna Tapahtumat-osa.
8. Valitse Kanban-rivin tapahtuma -kentässä Automaattinen.
    * Järjestelmä luo tapahtuma-kanbanit tarvittaessa.  Tällä kentällä voit määrittää kanban-säännöt, jotka tarvitaan tuotantovirran alempana olevien prosessitehtävien materiaalin täydentämiseen. Kun valinta on Automaattinen, tapahtuma-kanbanit luodaan tarpeen mukaan. Tätä asetusta suositellaan, jos tuotanto on tarkoitus suorittaa samana päivänä.  
9. Määritä tapahtuman vähimmäismääräksi 25.
    * Tapahtuma-kanbaneja muodostetaan, kun kysynnän määrä on yhtä suuri tai suurempi kuin tämä kenttä. Tästä on hyötyä, jos tuotettavan tilausmäärän on oltava pienempi kuin tämä kenttä yhdellä koneella ja enemmän kuin tämä kenttä toisella koneella.  
10. Valitse Tallenna.

## <a name="create-sales-order-and-trigger-kanban-chain"></a>Luo myyntitilaus ja käynnistä kanban-ketju
1. Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.
2. Valitse Uusi.
3. Syötä tai valitse arvo Asiakastili-kentässä.
    * Valitse asiakastili US-003, Forest Wholesales.  
4. Valitse OK.
5. Kirjoita Nimiketunnus-kenttään L0001.
    * L0001 on nimike, jolle kanban-sääntö on luotu.  
6. Valitse määräksi 27.
    * Koska 27 on suurempi kuin kanban-säännön vähimmäismäärä, 25, tapahtuma-kanban käynnistyy.  
7. Kirjoita Toimipaikka-kenttään 1.
8. Anna tai valitse Varasto-kentässä arvo.
    * Valitse varasto 13.  
9. Valitse Tallenna.

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a>Näytä kanban-säännöllä luotu kanban
1. Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Laajenna Kanbanit-osa.
    * Huomaa, että kanban 27:lle luotiin käsittelemään toiminto, joka perustuu luotuun kanban-sääntöön.  
    * Tämä on viimeinen vaihe.  

