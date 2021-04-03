---
title: Tehtäväsuhteen luonti – seuraaja
description: Lean-tuotantovirran tehtävien työnkulku dokumentoidaan tehtäväsuhteiden kautta.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f10ecb8e579975327440ede6ea383226645c8cf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255298"
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