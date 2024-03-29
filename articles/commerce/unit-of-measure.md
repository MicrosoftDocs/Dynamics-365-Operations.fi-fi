---
title: Mittayksikön asetusten käyttäminen
description: Tässä artikkelissa käsitellään mittayksikön asetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 7a7be6395a8bfce38e84f850bd792f358941c18a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275567"
---
# <a name="apply-unit-of-measure-settings"></a>Mittayksikön asetusten käyttäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään mittayksikön asetuksia ja kuvataan, miten niitä käytetään Microsoft Dynamics 365 Commerce -ohjelmassa.

Tuote voidaan myydä eri yksikköinä, esimerkiksi "kappale", "pari" ja "tusina". Commerce-pääkonttorisovelluksessa tuotteen myyntimittayksikkö voidaan määrittää ja se voidaan näyttää sähköisenä kauppapaikkana. Jos esimerkiksi jälleenmyyjä myy tuotteen sekä yksittäin että tusinana, käytettävissä olevat mittayksiköt voidaan näyttää yhdessä muiden tuotetietojen kanssa.

Seuraavassa esimerkissä on esitetty, että Commerce-pääkonttorisovelluksen tuotteelle on määritetty myyntimittayksikkö **kpl**.

![Esimerkki tuotteesta, joka on konfiguroitu mittayksiköllä Commerce headquarters -sovelluksessa.](./media/Productunit-headquarters.PNG)

> [!NOTE]
> Mittayksikön kohdistamisen ja näyttämisen tuki on käytettävissä Commerce-versiosta 10.0.19 alkaen.

## <a name="unit-of-measure-settings"></a>Mittayksikön asetukset

Mittayksikön näyttöasetukset määritetään Commercen sivustonmuodostimessa kohdassa **Sivuston asetukset \> Laajennukset \> Näytä tuotteiden mittayksikkö**. Tuettuja asetuksia on kolme:

- **Älä näytä** – Kun tämä asetus on valittuna, sähköisen kaupankäynnin toimipaikka ei näytä tuotteen mittayksikköä. Tämä on oletusasetus.
- **Näytä tuotteen ostokokemuksessa** – Kun tämä asetus valitaan, mittayksikkö näkyy tuotetietosivuilla, ostoskorissa, kassalla, tilaushistoriassa ja tilausten erittelysivuilla.
- **Näytä tuotteen selaus- ja ostokokemuksessa** – Kun tämä asetus valitaan, mittayksikkö näkyy tuotteen ostokokemussivuilla sekä tuotteen selauskokemuksen aikana. Osana tätä toimintatapaa mittayksiköt näkyvät hakutuloksissa ja tuotekokoelman moduuleissa.

> [!IMPORTANT]
> Mittayksikön näyttöasetukset ovat käytettävissä Commerce-versiosta 10.0.19 alkaen. Jos päivität vanhemmasta Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti. Ohjeita on kohdassa [SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-unit-of-measure-settings"></a>Mittayksikköasetuksia käyttävät moduulit

Mittayksikköasetuksia käyttävät moduulit sisältävät ostoruudun, toiveluettelon, ostoskorin, ostoskorikuvakkeen, hakutulossäilön, tuotekokoelman, kassan ja tilaustietojen moduulit.

Seuraavassa kuvan esimerkissä tuotetietosivu (PDP) näyttää tuotteen mittayksikön (**kpl**).

![Esimerkki tuotetietosivusta, jossa on näkyvissä mittayksikkö.](./media/Productunit-PDP.png)

Seuraavassa kuvan esimerkissä tuotekokoelmamoduuli näyttää tuotteen mittayksikön (**kpl**).

![Esimerkki tuotekokoelmamoduulista, jossa on näkyvissä mittayksikkö.](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ostoskorimoduuli](add-cart-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Tilin hallintasivut ja -moduulit](account-management.md)

[SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
