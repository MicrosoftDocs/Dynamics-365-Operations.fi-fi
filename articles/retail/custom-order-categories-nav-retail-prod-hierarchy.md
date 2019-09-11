---
title: Kaupankäynnin entiteettien lajittelujärjestyksen muuttaminen
description: Tässä ohjeaiheessa selitetään käsitteitä, jotka liittyvät useiden kaupankäyntiin liittyvien entiteettien näyttöjärjestyksen valvontaan Microsoft Dynamics 365 for Retailissa.
author: ashishharchwani
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2be3c1198ac6fff851be1bead2f0995202f1f0e7
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2019
ms.locfileid: "1866158"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Kaupankäynnin entiteettien lajittelujärjestyksen muuttaminen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Vähittäiskauppiaat pitävät tuotteen etsintätyökalua ensisijaisena työkaluna asiakkaan vuorovaikutuksessa kaikkien vähittäismyyntikanavien kautta. Eri toiminnot voivat auttaa asiakkaita löytämään tuotteita helposti. He voivat esimerkiksi selata luokkia, hakua ja suodatusta.

Tässä ohjeaiheessa selitetään käsitteitä, jotka liittyvät useiden kaupankäyntiin liittyvien entiteettien näyttöjärjestyksen valvontaan. Siinä selitetään myös lajittelujärjestyksen muuttaminen.

## <a name="overview"></a>Yleiskuvaus

Useiden kaupankäyntiin liittyvien entiteettien lajittelun tukea on parannettu. Tämä tuki on nyt paremmin linjassa nykyisten asiakasskenaarioiden kanssa, jotka ovat aiemmin edellyttäneet käyttöönottokumppaneiden laajennuksia.

Microsoft Dynamics 365 for Retail -versioissa, joiden versiot ovat vanhempia kuin versio 10.0.5, siirtymishierarkian luokkien lajittelujärjestys oli aakkosjärjestyksessä. Uuden mukautetun lajittelujärjestystoiminnon avulla myyntipäälliköt voivat määrittää eri myyntikohteisiin liittyvien entiteettien lajittelujärjestyksen kaikissa peruskäyttäjäohjelmissa. Näitä asiakasohjelmia ovat esimerkiksi pääkonttori (HQ) ja puhelinkeskus.

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a>Vähittäismyynnin tuotehierarkian luokkien näyttöjärjestyksen määrittäminen

Ennen kuin voit tehdä nämä toimet, demotiedot on asennettava ympäristöösi.

1. Valitse **Vähittäismyynti \> Tuotteet ja luokat \> Vähittäismyynnin tuotehierarkia**.
2. Valitse **Muokkaa luokkahierarkiaa**.
3. Valitse **Muokkaa**.
4. Laajenna puussa **ALL \> Action Sports**.
5. Laajenna puussa **ALL \> Team Sports**.
6. Syötä **Näyttöjärjestys**-kenttään numero. (Luku voi olla negatiivinen.)
7. Toista vaiheet 4-6 kaikille muille luokille, joiden järjestystä haluat muuttaa.

Kanavan siirtymishierarkian näyttöjärjestys näkyy vähittäismyynnin tuotehierarkian ja vapautettujen tuotteiden luokan pääkonttorissa.

![Vähittäismyynnin tuotehierarkian mukautettu lajittelu negatiivisin arvoin](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Vapautetut tuotteet luokittain vähittäismyyntituotehierarkian mukaan mukautetusti lajiteltuna](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Kanavan siirtymishierarkian luokkien näyttöjärjestyksen määrittäminen

Ennen kuin voit tehdä nämä toimet, demotiedot on asennettava ympäristöösi.

1. Siirry kohtaan **Vähittäismyynti \> Tuotteet ja luokat \> Kanavan siirtymisluokat**.
2. Valitse luettelosta **Fashion**-siirtymishierarkia.
3. Valitse **Muokkaa luokkahierarkiaa**.
4. Valitse **Muokkaa**.
5. Valitse puussa **Fashion \> Womenswear \> Womens Shoes**.
6. Syötä **Näyttöjärjestys**-kenttään numero.
7. Valitse puussa **Fashion \> Womenswear \> Tops**.

    Voit myös määrittää alaluokkien lajittelujärjestyksen.

8. Valitse puussa **Fashion \> Menswear \> Casual Shirts**.
9. Syötä **Näyttöjärjestys**-kenttään numero.
10. Valitse puussa **Fashion \> Menswear \> Coats & Jackets**.
11. Syötä **Näyttöjärjestys**-kenttään numero.
12. Toista kaikille muille luokille, joiden järjestystä haluat muuttaa.

Kanavan siirtymishierarkian näyttöjärjestys näkyy pääkonttorissa, tuoteluettelossa ja vähittäismyyntikanavissa.

![Kanavan siirtymishierarkia mukautetusti lajiteltuna](./media/ChannelNavCustomSorted.png)

![Luettelon siirtymishierarkia mukautetusti lajiteltuna kanavan siirtymishierarkian mukaan](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Myyntipisteet, jossa on mukautettuja lajiteltuja luokkia](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Mukautettu lajittelujärjestys on oletusarvoisesti poissa käytöstä. Lisätietoja tämän toiminnon ja muiden toimintojen ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).
