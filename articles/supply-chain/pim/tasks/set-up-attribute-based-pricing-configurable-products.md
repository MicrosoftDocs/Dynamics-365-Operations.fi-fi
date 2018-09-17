--- 
title: "Määritä määrittäville tuotteille määritepohjainen hinnoittelu"
description: "Tässä menettelyssä kerrotaan, miten määritepohjainen hinnoittelu määritetään."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 88402bef6fd5dad38a74795cd31a4046085d6db7
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Määritä määrittäville tuotteille määritepohjainen hinnoittelu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten määritepohjainen hinnoittelu määritetään. Edellytyksenä on oltava tuotemääritysmalli, jolla on yksi tai useampi osa ja määrite. Tämä esimerkki käyttää USMF-yrityksen demotietojen korkealaatuista kaiutinmallia. Tämän tehtävän suorittaa yleensä tuotepäällikkö.


## <a name="create-a-new-price-model"></a>Luo uusi hintamalli
1. Valitse Tuotevarianttimallin määritys.
2. Valitse Tuotekonfiguraation mallit.
3. Valitse luettelosta korkealaatuisen kaiuttimen rivi, mutta älä napsauta nimen linkkiä.
4. Valitse toimintoruudussa Malli.
5. Valitse Hintamallit.
6. Valitse Uusi.
7. Kirjoita arvo Hintamalli-kenttään.
    * Käytä nimeä, jonka avulla malli on helppo tunnistaa.  
8. Kirjoita arvo Kuvaus-kenttään.
9. Valitse Tallenna.

## <a name="add-price-elements"></a>Lisää hintaelementit
1. Valitse Muokkaa.
    * Kullakin tuotemallin osalla voi olla perushintaelementti ja rajaton määrä hintalausekesääntöjä. Voit myös lisätä hinnat eri valuutoissa.  
2. Syötä arvo Perushintalauseke-kenttään.
    * Kirjoita esimerkiksi 100.   Lähtöhinta-lauseke voi olla numeerinen arvo tai aritmeettinen laskutoimitus, johon liittyy vähintään yksi määrite.  
3. ValitseLisää.
4. Kirjoita Nimi-kenttään Ruusupuu.
    * Hintalausekkeen nimi auttaa tunnistamaan, mitä hintaelementti edustaa. Tässä esimerkissä luodaan hintaelementti kaapin viimeistelyvaihtoehdolle Ruusupuu.  
5. Valitse Muokkaa ehtoa.
    * Hintaehto takaa, että hintalausekkeen elementti sisältyy myyntihintaan vain, jos tietty määritteiden yhdistelmä on läsnä.  
6. Lisää ConstraintBody-kenttään CabinetFinish=="Rosewood".
7. Valitse OK.
8. Kirjoita arvo Lauseke-kenttään.
    * Kirjoita esimerkiksi 50.  
9. Sulje sivu.
10. Sulje sivu.


