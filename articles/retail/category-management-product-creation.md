---
title: "Vähittäismyynnin tuoteluokkien ja tuotteiden hallinta"
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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 19c972164474c972aab642c3cccc67cf396a6cb2
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="manage-retail-product-categories-and-products"></a>Vähittäismyynnin tuoteluokkien ja tuotteiden hallinta

[!include [banner](./includes/banner.md)]

Tässä ohjeaiheessa käsitellään parannettua tapaa hallita vähittäismyynnin tuoteluokkia ja tuotteita Microsoft Dynamics 365 for Retailissa. Myynninedistämispäälliköt näkevät näiden parannusten avulla tuoteominaisuuksien rakenteen, jonka vähittäismyynnin tuotehierarkia ja vapautetut tuotetiedot jakavat.

Saat lisätietoja vähittäismyynnin tuoteluokkien hallinnasta valitsemalla **Luokka- ja tuotehallinta** -työtilassa **Vähittäismyynnin tuotehierarkia** -ruudun.

Kiinnitä huomiota avautuvan **Vähittäismyynnin tuotehierarkia** -sivun parannuksiin. Aiemmissa Retail-versioissa tuotteen ominaisuudet jaettiin *tuotteen perusominaisuuksiin* ja *vähittäismyyntituotteen tuotteenominaisuuksiin* niiden käyttöalueen mukaan. Vähittäismyyntituotteen ominaisuuksien käyttöalue on *yleinen*. Toisin sanoen tietyn vähittäismyyntituotteen ominaisuuden arvot jaetaan kaikissa yrityksissä. Tuotteen perusominaisuudet ovat sen sijaan *yrityskohtaisia*. Toisin sanoen tietyn tuotteen perusominaisuuden arvo voi vaihdella yrityksissä kun yrityksen yksittäisten liiketoimintatarpeiden perusteella.

Parannetussa vähittäismyynnin tuoteluokkarakenteessa tuotteen ominaisuudet erotetaan loogisesti sen perusteella, miten niitä voi käyttää ryhmässä, jotta ne vastaavat vapautettujen tuotetietojen lomakerakennetta.

![Kenttien ryhmittely ominaisuuksien käyttöalueen perusteella](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Yrityskohtaisten ominaisuuksien hallinnan voi vaihtaa yleisestä yrityskohtaiseksi.

Voit hallita ominaisuuksia kaikissa yrityksissä valitsemalla **Näytä kaikissa yrityksissä** (tai **Muokkaa kaikissa yrityksissä**).

![Näyttäminen tai muokkaaminen kaikissa yrityksissä](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Voit hallita tietyn yrityksen ominaisuuksia valitsemalla **Näytä tietyssä yrityksessä** (tai **Muokkaa tietyssä yrityksessä**).

![Näyttäminen tai muokkaaminen tietyssä yrityksessä](media/ToggleToEditForAllLegalEntities.PNG)

Parannetussa vähittäismyynnin tuoteluokkarakenteessa myynninedistämispäällikkö voi nyt myös määrittää oletusarvot lisätuoteominaisuusjoukolle yksittäisellä luokkatasolla. Kun tuotteet sitten luodaan, ne perivät tuoteominaisuuksiensa oletusarvot sen perusteella, mitä on kyseisten ominaisuuksien liitos yksittäiseen vähittäismyynnin tuotehierarkialuokkaan. Näitä perittyjä tuoteominaisuuksia voidaan myös muokata kunkin tuotteen kohdalla siten, että ne vastaavat yksittäisiä liiketoimintatarpeita.

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a>Vähittäismyynnin tuotehierarkiasivulla päivitettävien tuoteominaisuuksien valinta

Voit käyttää uutta tuoteominaisuuksien parannettua rakennetta, kun valitset, mitkä päivitetyt tuoteominaisuudet on siirrettävä liitettyihin tuotteisiin. Valitse **Vähittäismyynnin tuotehierarkia** -sivun toimintoruudussa **Luokka** ja avaa sitten **Päivitä tuotteet** -valintaikkuna valitsemalla **Päivitä tuotteet**.

![Päivitä tuotteet -valintaikkuna.](media/NewUpdateProductsEnhancedView.PNG)

