---
title: Tuoteluokkien ja tuotteiden hallinta
description: Tässä artikkelissa kerrotaan, miten myynninedistämispäälliköt voivat hallita tuotehierarkian ja vapautetun tuotteen tietojen välisiä suhteita Commercen tuoteluokkien avulla.
author: ashishmsft
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0871475e0910e0a46544c56083b505ff647fd6a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878567"
---
# <a name="manage-product-categories-and-products"></a>Tuoteluokkien ja tuotteiden hallinta

[!include [banner](./includes/banner.md)]

Tässä artikkelissa kerrotaan parannetusta tavasta hallita Dynamics 365 Commercen tuoteluokkia ja tuotteita. Myynninedistämispäälliköt näkevät näiden parannusten avulla tuoteominaisuuksien rakenteen, jonka tuotehierarkia ja vapautetut tuotetiedot jakavat.

Saat lisätietoja tuoteluokkien hallinnasta valitsemalla **Luokka- ja tuotehallinta** -työtilassa **Commercen tuotehierarkia** -ruudun.

Kiinnitä huomiota avautuvan **Commercen tuotehierarkia** -sivun parannuksiin. Aiemmissa sovelluksen versioissa tuotteen ominaisuudet jaettiin *tuotteen perusominaisuuksiin* ja *vähittäismyyntituotteen tuotteenominaisuuksiin* niiden käyttöalueen mukaan. Vähittäismyyntituotteen ominaisuuksien käyttöalue on *yleinen*. Toisin sanoen tietyn tuoteominaisuuden arvot jaettiin kaikkiin yrityksiin. Tuotteen perusominaisuudet ovat sen sijaan *yrityskohtaisia*. Toisin sanoen tietyn tuotteen perusominaisuuden arvo voi vaihdella yrityksissä kun yrityksen yksittäisten liiketoimintatarpeiden perusteella.

Parannetussa tuoteluokkarakenteessa tuotteen ominaisuudet erotetaan loogisesti sen perusteella, miten niitä voi käyttää ryhmässä, jotta ne vastaavat vapautettujen tuotetietojen lomakerakennetta.

![Kenttien ryhmittely ominaisuuksien käyttöalueen perusteella.](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Yrityskohtaisten ominaisuuksien hallinnan voi vaihtaa yleisestä yrityskohtaiseksi.

Voit hallita ominaisuuksia kaikissa yrityksissä valitsemalla **Näytä kaikissa yrityksissä** (tai **Muokkaa kaikissa yrityksissä**).

![Näyttäminen tai muokkaaminen kaikissa yrityksissä.](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Voit hallita tietyn yrityksen ominaisuuksia valitsemalla **Näytä tietyssä yrityksessä** (tai **Muokkaa tietyssä yrityksessä**).

![Näyttäminen tai muokkaaminen tietyssä yrityksessä.](media/ToggleToEditForAllLegalEntities.PNG)

Parannetussa tuoteluokkarakenteessa myynninedistämispäällikkö voi nyt myös määrittää oletusarvot lisätuoteominaisuusjoukolle yksittäisellä luokkatasolla. Kun tuotteet sitten luodaan, ne perivät tuoteominaisuuksiensa oletusarvot sen perusteella, mikä on kyseisten ominaisuuksien liitos yksittäiseen tuotehierarkialuokkaan. Näitä perittyjä tuoteominaisuuksia voidaan myös muokata kunkin tuotteen kohdalla siten, että ne vastaavat yksittäisiä liiketoimintatarpeita.

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a>Commercen tuotehierarkiasivulla päivitettävien tuoteominaisuuksien valinta

Voit käyttää uutta tuoteominaisuuksien parannettua rakennetta, kun valitset, mitkä päivitetyt tuoteominaisuudet on siirrettävä liitettyihin tuotteisiin. Valitse **Commercen tuotehierarkia** -sivun toimintoruudussa **Luokka** ja avaa sitten **Päivitä tuotteet** -valintaikkuna valitsemalla **Päivitä tuotteet**.

![Päivitä tuotteet -valintaikkuna.](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]