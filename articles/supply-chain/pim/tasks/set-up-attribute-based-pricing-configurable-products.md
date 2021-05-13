---
title: Määritä määrittäville tuotteille määritepohjainen hinnoittelu
description: Tässä aiheessa kerrotaan, miten määritepohjainen hinnoittelu määritetään.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921238"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Määritä määrittäville tuotteille määritepohjainen hinnoittelu

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kerrotaan, miten määritepohjainen hinnoittelu määritetään. Edellytyksenä on oltava tuotemääritysmalli, jolla on yksi tai useampi osa ja määrite. Tämä esimerkki käyttää USMF-yrityksen demotietojen korkealaatuista kaiutinmallia. Tämän tehtävän suorittaa yleensä tuotepäällikkö.


## <a name="create-a-new-price-model"></a>Luo uusi hintamalli

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.
1. Valitse luettelosta **High End Speaker** -rivi, mutta älä napsauta nimen linkkiä.
1. Valitse toimintoruudussa **Malli**.
1. Valitse **Hintamallit**.
1. Valitse **Uusi**.
1. Kirjoita arvo **Hintamallin nimi** -kenttään. Käytä nimeä, jonka avulla malli on helppo tunnistaa.  
1. Kirjoita **Kuvaus**-kenttään arvo.
1. Valitse **Tallenna**.

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