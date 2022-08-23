---
title: Myynninedistämiskohteiden lajittelujärjestyksen muuttaminen
description: Tässä artikkelissa selitetään käsitteitä, jotka liittyvät useiden kaupankäyntiin liittyvien entiteettien näyttöjärjestyksen valvontaan Dynamics 365 Commercessa.
author: josaw1
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 80586597f4f60476b341e4cf1cfd90f3681e15c0
ms.sourcegitcommit: 52e31b1ef2b3ed8675de931d06090cd57e057fc2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9265833"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Kaupankäynnin entiteettien lajittelujärjestyksen muuttaminen


[!Include [banner](includes/banner.md)]

Vähittäiskauppiaat pitävät tuotteen etsintätyökalua ensisijaisena työkaluna asiakkaan vuorovaikutuksessa kaikkien kanavien kautta. Useiden ominaisuuksien avulla asiakkaat voivat helposti löytää tuotteita. Asiakkaat voivat esimerkiksi selata luokkia, hakua ja suodatusta.

Tässä artikkelissa selitetään käsitteitä, jotka liittyvät useiden kaupankäyntiin liittyvien entiteettien näyttöjärjestyksen valvontaan. Siinä selitetään myös lajittelujärjestyksen muuttaminen.

## <a name="overview"></a>Yleiskuvaus

Commercessa eri myynninedistämiseen liittyvien yksiköiden lajittelu on kohdistettu aiemmin luotujen asiakasskenaarioiden kanssa, eikä käyttöönottokumppanien laajennuksia enää tarvita.

Commerce-versioissa 10.0.5 ja aikaisemmista versiossa siirtymishierarkian luokkien lajittelujärjestys oli aakkosjärjestyksessä. Nykyinen mukautetun lajittelujärjestystoiminnon avulla myyntipäälliköt voivat määrittää eri myyntikohteisiin liittyvien entiteettien lajittelujärjestyksen kaikissa peruskäyttäjäohjelmissa. Näitä asiakasohjelmia ovat esimerkiksi pääkonttori (HQ) ja puhelinkeskus.

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

![Tuotehierarkian mukautettu lajittelu negatiivisin arvoin.](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Vapautetut tuotteet luokittain tuotehierarkian mukaan mukautetusti lajiteltuna.](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Kanavan siirtymishierarkian luokkien näyttöjärjestyksen määrittäminen

Ennen kuin voit tehdä nämä toimet, demotiedot on asennettava ympäristöösi.

1. Siirry kohtaan **Retail ja Commerce \> Tuotteet ja luokat \> Kanavan siirtymisluokat**.
2. Valitse luettelosta **Fashion**-siirtymishierarkia.
3. Valitse **Muokkaa luokkahierarkiaa**.
4. Valitse **Muokkaa**.
5. Valitse puussa **Fashion \> Womenswear \> Women's Shoes**.
6. Syötä **Näyttöjärjestys**-kenttään numero.
7. Valitse puussa **Fashion \> Womenswear \> Tops**.

Voit myös määrittää alaluokkien lajittelujärjestyksen.

8. Valitse puussa **Fashion \> Menswear \> Casual Shirts**.
9. Syötä **Näyttöjärjestys**-kenttään numero.
10. Valitse puussa **Fashion \> Menswear \> Coats & Jackets**.
11. Syötä **Näyttöjärjestys**-kenttään numero.
12. Toista kaikille muille luokille, joiden järjestystä haluat muuttaa.

Kanavan siirtymishierarkian näyttöjärjestys näkyy pääkonttorissa, tuoteluettelossa ja kanavissa.

![Kanavan siirtymishierarkia mukautetusti lajiteltuna.](./media/ChannelNavCustomSorted.png)

![Luettelon siirtymishierarkia mukautetusti lajiteltuna kanavan siirtymishierarkian mukaan.](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Myyntipisteet, jossa on mukautettuja lajiteltuja luokkia.](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Oletusarvon mukaan **Ota käyttöön myynninedistämisyksiköiden näyttöjärjestys** -toiminto on poissa käytöstä. Ota toiminto käyttöön käyttämällä [toimintojen hallintaa](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Kun otat toiminnon käyttöön, suorita **Yleinen konfiguraatio -1110** -CDX-työ jakeluaikataulusta.
> Jos myyntipisteen luokkien järjestystä ei päivitetä, aktivoi laite uudelleen. Luokkatiedot haetaan laitteen aktivoinnin yhteydessä, joten laitteen täytyy ehkä hakea luokkatiedot uudelleen päivitetyin näyttötilauksin. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
