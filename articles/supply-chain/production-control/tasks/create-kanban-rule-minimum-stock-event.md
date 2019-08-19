---
title: Luo kanban-sääntö käyttäen vähimmäisvarastotapahtumaa
description: Tämä menettely keskittyy asetuksiin, jotka tarvitaan kanban-säännön luomiseen vähimmäisvarastotapahtuman perusteella sen varmistamiseksi, että tiettyä tuotetta on aina saatavilla tietyssä paikassa.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b578a664e9e3b6496e5665b2eefd9d75f86ecc3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837827"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a>Luo kanban-sääntö käyttäen vähimmäisvarastotapahtumaa

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tämä menettely keskittyy asetuksiin, jotka tarvitaan kanban-säännön luomiseen vähimmäisvarastotapahtuman perusteella sen varmistamiseksi, että tiettyä tuotetta on aina saatavilla tietyssä paikassa. Kanban-sääntö luodaan materiaalin siirtämiselle sijaintiin, kun varaston taso laskee alle 200 kappaleen. Tarvittavat kanbanit luodaan ajamalla tarvekohdistustapahtuman käsittely. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF. Tämä tehtävä on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun tuotteen tuotannon valmisteluun lean-ympäristössä.


## <a name="create-a-new-kanban-rule"></a>Luo uusi kanban-sääntö
1. Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.
2. Valitse Uusi.
3. Valitse Tyyppi-kentän arvoksi "Otto".
    * Tätä tyyppiä käytetään siirtokanbanien luomiseen.  
4. Valitse Täydennysstrategia-kentässä Tapahtuma.
    * Tapahtumastategiaa käytetään, jotta kanbanien siirto voidaan tehdä tapahtuman perusteella. Jäljempänä menettelyssä siirtokanbanit käynnistetään varaston täydennyksen kautta.  
5. Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.
    * Anna tai valitse ReplenishSpeakerComponents. Siirtotehtävällä on vastaanottava (tulos-)varasto ja toimipaikka 12, minkä vuoksi materiaalit siirretään varaston 12 toimipaikkaan 12.  
6. Laajenna Tiedot-osa.
7. Anna tai valitse Tuote-kentässä arvo.
    * Valitse M0007.  
8. Laajenna Tapahtumat-osa.
9. Valitse Varaston täydennystapahtuma -kentässä Erä.
    * Tämä luo kanbanit materiaalitarpeen täyttämisellä liittyvässä sijainnissa tarvekohdistustapahtuman käsittelyn aikana.  

## <a name="set-the-minimum-quantity-for-the-item"></a>Aseta nimikkeen vähimmäismäärä
1. Napsauta Tuote-kentän linkkiä.
2. Käytä Nimiketunnus-kentän linkkiä napsauttamalla.
3. Laajenna tuotekuvan tietoruutu.
4. Valitse toimintoruudussa Suunnitelma.
5. Valitse Nimikekattavuus.
6. Valitse Uusi.
7. Merkitse valittu rivi luettelossa.
8. Anna tai valitse Varasto-kentässä arvo.
    * Määritä Varasto-arvoksi 12.  
9. Määritä vähimmäisarvoksi "200".

## <a name="run-the-batch-event-creation-job"></a>Suorita tapahtumien luonnin erätyö
1. Valitse Laadunvalvonta > Kausittaiset tehtävät > Kanban-työn eräkäsittely > Tarvekohdistustapahtuman käsittely.
2. Valitse OK.
3. Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse aiemmin luomasi kanban-sääntö.  
5. Laajenna Kanbanit-osa.
    * Huomaa, että kanban luotiin siirtämään tarvittava materiaalin varastoon 12.  

