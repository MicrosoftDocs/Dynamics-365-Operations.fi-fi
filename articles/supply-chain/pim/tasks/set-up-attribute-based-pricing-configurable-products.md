---
title: Määritä määrittäville tuotteille määritepohjainen hinnoittelu
description: Tässä aiheessa kerrotaan, miten määritepohjainen hinnoittelu määritetään.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a75f3afcf4761ac6a9575eae9a620a1e9f01c8e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426922"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Määritä määrittäville tuotteille määritepohjainen hinnoittelu

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kerrotaan, miten määritepohjainen hinnoittelu määritetään. Edellytyksenä on oltava tuotemääritysmalli, jolla on yksi tai useampi osa ja määrite. Tämä esimerkki käyttää USMF-yrityksen demotietojen korkealaatuista kaiutinmallia. Tämän tehtävän suorittaa yleensä tuotepäällikkö.


## <a name="create-a-new-price-model"></a>Luo uusi hintamalli
1. Valitse **Tuotevarianttimallin määritys** aloitussivulla.
2. Valitse **Tuotekonfiguraation mallit** **Linkit**-osiossa.
3. Valitse luettelosta **High End Speaker** -rivi, mutta älä napsauta nimen linkkiä.
4. Valitse toimintoruudussa **Malli**.
5. Valitse **Hintamallit**.
6. Valitse **Uusi**.
7. Kirjoita arvo **Hintamallin nimi** -kenttään. Käytä nimeä, jonka avulla malli on helppo tunnistaa.  
8. Kirjoita **Kuvaus**-kenttään arvo.
9. Valitse **Tallenna**.

## <a name="add-price-elements"></a>Lisää hintaelementit
1. Valitse **Muokkaa**. Kullakin tuotemallin osalla voi olla perushintaelementti ja rajaton määrä hintalausekesääntöjä. Voit myös lisätä hinnat eri valuutoissa.  
2. Syötä arvo **Perushintalauseke**-kenttään. Kirjoita esimerkiksi 100. Lähtöhinta-lauseke voi olla numeerinen arvo tai aritmeettinen laskutoimitus, johon liittyy vähintään yksi määrite.  
3. Valitse **Lisää**.
4. Syötä **Nimi**-kenttään `Rosewood`. Hintalausekkeen nimi auttaa tunnistamaan, mitä hintaelementti edustaa. Tässä esimerkissä luodaan hintaelementti kaapin viimeistelyvaihtoehdolle Ruusupuu.  
5. Valitse **Muokkaa ehtoa**. Hintaehto takaa, että hintalausekkeen elementti sisältyy myyntihintaan vain, jos tietty määritteiden yhdistelmä on läsnä.  
6. Kirjoita **ConstraintBody**-kenttään `CabinetFinish=="Rosewood"`.
7. Valitse **OK**.
8. Kirjoita arvo **Lauseke**-kenttään. Kirjoita esimerkiksi `50`. 
9. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]