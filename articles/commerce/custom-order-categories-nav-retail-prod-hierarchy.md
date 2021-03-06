---
title: Kaupankäynnin entiteettien lajittelujärjestyksen muuttaminen
description: Tässä ohjeaiheessa selitetään käsitteitä, jotka liittyvät useiden kaupankäyntiin liittyvien entiteettien näyttöjärjestyksen valvontaan Dynamics 365 Commercessa.
author: josaw1
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 31798508e4cc71e31a30dc91acebfdde8226b16c
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937059"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Kaupankäynnin entiteettien lajittelujärjestyksen muuttaminen


[!include [banner](includes/banner.md)]

Vähittäiskauppiaat pitävät tuotteen etsintätyökalua ensisijaisena työkaluna asiakkaan vuorovaikutuksessa kaikkien kanavien kautta. Eri toiminnot voivat auttaa asiakkaita löytämään tuotteita helposti. He voivat esimerkiksi selata luokkia, hakua ja suodatusta.

Tässä ohjeaiheessa selitetään käsitteitä, jotka liittyvät useiden kaupankäyntiin liittyvien entiteettien näyttöjärjestyksen valvontaan. Siinä selitetään myös lajittelujärjestyksen muuttaminen.

## <a name="overview"></a>Yleiskuvaus

Useiden kaupankäyntiin liittyvien entiteettien lajittelun tukea on parannettu. Tämä tuki on nyt paremmin linjassa nykyisten asiakasskenaarioiden kanssa, jotka ovat aiemmin edellyttäneet käyttöönottokumppaneiden laajennuksia.

Retailin versiota 10.0.5 vanhemmissa versioissa siirtymishierarkian luokkien lajittelujärjestys oli aakkosjärjestyksessä. Uuden mukautetun lajittelujärjestystoiminnon avulla myyntipäälliköt voivat määrittää eri myyntikohteisiin liittyvien entiteettien lajittelujärjestyksen kaikissa peruskäyttäjäohjelmissa. Näitä asiakasohjelmia ovat esimerkiksi pääkonttori (HQ) ja puhelinkeskus.

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>Tuotehierarkian luokkien näyttöjärjestyksen määrittäminen

Ennen kuin voit tehdä nämä toimet, demotiedot on asennettava ympäristöösi.

1. Valitse **Retail ja Commerce \> Luokka- ja tuotehallinta \> Commerce-tuotehierarkia**.
2. Valitse **Muokkaa luokkahierarkiaa**.
3. Valitse **Muokkaa**.
4. Laajenna puussa **ALL \> Action Sports**.
5. Laajenna puussa **ALL \> Team Sports**.
6. Syötä **Näyttöjärjestys**-kenttään numero. (Luku voi olla negatiivinen.)
7. Toista vaiheet 4-6 kaikille muille luokille, joiden järjestystä haluat muuttaa.

Kanavan siirtymishierarkian näyttöjärjestys näkyy kaupankäynnin tuotehierarkian ja vapautettujen tuotteiden luokan pääkonttorissa.

![Tuotehierarkian mukautettu lajittelu negatiivisin arvoin](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Vapautetut tuotteet luokittain tuotehierarkian mukaan mukautetusti lajiteltuna](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Kanavan siirtymishierarkian luokkien näyttöjärjestyksen määrittäminen

Ennen kuin voit tehdä nämä toimet, demotiedot on asennettava ympäristöösi.

1. Siirry kohtaan **Retail ja Commerce \> Tuotteet ja luokat \> Kanavan siirtymisluokat**.
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

Kanavan siirtymishierarkian näyttöjärjestys näkyy pääkonttorissa, tuoteluettelossa ja kanavissa.

![Kanavan siirtymishierarkia mukautetusti lajiteltuna](./media/ChannelNavCustomSorted.png)

![Luettelon siirtymishierarkia mukautetusti lajiteltuna kanavan siirtymishierarkian mukaan](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Myyntipisteet, jossa on mukautettuja lajiteltuja luokkia](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Mukautettu lajittelujärjestys on oletusarvoisesti poissa käytöstä. Lisätietoja tämän toiminnon ja muiden toimintojen ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]