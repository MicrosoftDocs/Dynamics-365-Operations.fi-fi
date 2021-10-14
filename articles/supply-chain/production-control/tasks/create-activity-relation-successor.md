---
title: Tehtäväsuhteen luonti – seuraaja
description: Lean-tuotantovirran tehtävien työnkulku dokumentoidaan tehtäväsuhteiden kautta.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cee0c75de1fee24cfb6df018de62ece102c96cc
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579205"
---
# <a name="create-activity-relation---successor"></a>Tehtäväsuhteen luonti – seuraaja

[!include [banner](../../includes/banner.md)]

Lean-tuotantovirran tehtävien työnkulku dokumentoidaan tehtäväsuhteiden kautta. Tässä tallenteessa käsitellään tehtäväsuhteen luontia.

Edellytykset:

- Tuotantovirta ja versio luonnostilassa. 

- Tuotantovirtaan luodaan kaksi toisiaan seuraavaa tehtävää, jotka eivät ole suhteessa toisiinsa.


## <a name="find-the-production-flow-version"></a>Etsi tuotantovirran versio 
1. Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Merkitse valittu rivi luettelossa.
5. Valitse luonnosversio luettelosta.
    * Tehtäväsuhteet voidaan lisätä sekä tuotantovirran luonnosversioihin että aktiivisiin versioihin.  

## <a name="open-the-activity-overview"></a>Avaa tehtävän yhteenveto
1. Valitse Tehtävät.
    * Huomaa, että lomake näyttää kaikki tuotantovirran tehtävät, jotka on kohdistettu siihen tuotantovirtojen versioon, jossa työskentelet.  

## <a name="add-a-successor"></a>Lisää seuraaja
1. Valitse Lisää seuraaja.
2. Avaa haku napsauttamalla Tehtävä-kentässä avattavan valikon painiketta.
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Valitse Rajoitus-valintaruutu.
6. Lisää Rajoitusarvo-kenttään numero.
    * Aikarajoitus on edeltäjän (eräpäivä ja -aika) ajoitetun lopun ja seuraajan ajoitetun alun väliin ajoitettava aika.  
7. Kirjoita Yksiköt-kenttään arvo.
8. Lisää Syklin kestojen suhde -kenttään numero.
    * Jos molemmat tehtävät suoritetaan samassa tahdissa, syklin keston suhteen on oltava 1. Jos edeltäjä suoritetaan seuraajan kaksinkertaisella tahdilla, suhteen on oltava 2.   Syklin kestosuhteita käytetään tuotantovirtatehtävien yksittäisten syklien kestojen laskentaan.  
9. Valitse OK.
10. Sulje sivu.
11. Valitse Ruudukkoruutu-välilehti.
12. Sulje sivu.
13. Päivitä sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]