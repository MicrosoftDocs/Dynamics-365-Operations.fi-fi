---
title: Tuoteluokan hallinta
description: "Tässä ohjeaiheessa kerrotaan, miten myynninedistämispäälliköt voivat hallita vähittäismyynnin tuotehierarkian ja vapautetun tuotteen tietojen välisiä suhteita vähittäismyynnin tuoteluokkien avulla."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a>Parannettu tuotteiden ja luokkien hallinta

[!include[banner](./includes/banner.md)]

Tässä ohjeaiheessa kerrotaan parannetusta tavasta hallita vähittäismyynnin tuoteluokkia ja tuotteita Dynamics 365 for Retailissa. Myynninedistämispäälliköt näkevät näiden parannusten avulla tuoteominaisuuksien yhteisen rakenteen vähittäismyynnin tuotehierarkian ja vapautettujen tuotetietojen välillä.

Saat lisätietoja vähittäismyynnin tuoteluokkien valitsemalla **Vähittäismyynnin tuotehierarkia** **Luokka- ja tuotehallinta** -työtilassa ja tarkastelemalla **Vähittäismyynnin tuoteluokka** -sivun parannettua rakennetta.

![Luokka- ja tuotehallinta -työtila](media/LaunchRetailProductHierarchy.png)

Aiemmissa versioissa tuotteen ominaisuudet jaettiin **tuotteen perusominaisuuksiin** ja **vähittäismyyntituotteen tuotteenominaisuuksiin** niiden käyttöalueen mukaan. **Vähittäismyyntituotteen ominaisuudet** oli käyttöalueeltaan *yleinen*, mikä tarkoitti, että tietyllä **vähittäismyyntituotteen ominaisuudella** sama arvo jaetaan kaikissa yrityksissä. **Tuotteen perusominaisuudet** ovat *yrityskohtaisia*. Toisin sanoen tietyn **tuotteen perusominaisuuden** arvo voi vaihdella yrityksissä yksittäisten liiketoimintatarpeiden perusteella.

Parannetussa vähittäismyynnin tuoteluokkarakenteessa tuotteen ominaisuudet erotetaan loogisesti sen perusteella, miten käytettäviä ne ovat ryhmässä, vastaamaan vapautettujen tuotetietojen lomakerakennetta.

![Kenttien ryhmittely käyttöalueen perusteella](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Ominaisuuksien hallinnan yrityskohtaisille ominaisuuksille voi vaihtaa yleisestä yrityskohtaiseksi. Voit tehdä valitsemalla joko **Näytä tai muokkaa kaikissa yrityksissä** tai **Näytä tai muokkaa tietyssä yrityksessä**.

![Näkymän vaihtelu yksittäisen yrityksen ja kaikkien yritysten välillä](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Näkymän vaihtelu yksittäisen yrityksen ja kaikkien yritysten välillä](media/ToggleToEditForAllLegalEntities.PNG)  

Edellisiin versioihin verrattuna uudessa vähittäismyynnin tuoteluokkarakenteessa myynninedistämispäällikkö voi myös määrittää oletusarvot lisätuoteominaisuusjoukolle yksittäisellä luokkatasolla. Tuotetta luotaessa tuote perii nämä tuoteominaisuuden oletusarvot perustuen liitokseen vähittäismyynnin tuotehierarkian yksittäiseen luokkaan. Näitä perittyjä tuoteominaisuuksia voidaan myös muokata kunkin tuotteen kohdalla siten, että vastaavat yksittäisiä liiketoimintatarpeita.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Valitse ominaisuudet, jotka päivitetään tuotteille vähittäismyynnin tuoteluokkalomakkeessa 
 
Voit käyttää tätä uutta tuoteominaisuuksien parannettua rakennetta, kun valitset mitkä päivitetyt tuoteominaisuudet on siirrettävä liitettyihin tuotteisiin. 

![Uusi päivitettyjen tuotteiden parannettu näkymä](media/NewUpdateProductsEnhancedView.PNG) 

Myynninedistämispäälliköt voivat muokata näitä perittyjä tuoteominaisuuksia tuotekohtaisesti täyttääkseen yksittäisiä liiketoiminnan vaatimuksia.


