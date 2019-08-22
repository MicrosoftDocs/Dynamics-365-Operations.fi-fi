---
title: Määritä määrittäville tuotteille määritepohjainen hinnoittelu
description: Tässä menettelyssä kerrotaan, miten määritepohjainen hinnoittelu määritetään.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba84fa4de660d16b266763fff5b0b794ed327c81
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844198"
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

