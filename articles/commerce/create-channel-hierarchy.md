---
title: Vähittäismyyntikanavan siirtymishierarkian luominen
description: Tässä artikkelissa käsitellään kanavan siirtymishierarkian luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: c3b28dd29bf444a75e5aa0a2a105d8a03fcacb0d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270261"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Vähittäismyyntikanavan siirtymishierarkian luominen


[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään kanavan siirtymishierarkian luontia Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus

Kanavan siirtymishierarkiaa käytetään tuotteiden luokkiin ryhmittelemiseen ja järjestämiseen, jotta niitä voidaan selata verkossa tai myyntipisteessä (POS).

## <a name="create-a-channel-navigation-hierarchy"></a>Luo kanavan siirtymishierarkia

Voit luoda kanavan siirtymishierarkian seuraavasti.

1. Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäiskauppa ja kauppa \> Tuotteet ja luokat \> Kanavan siirtymisluokat**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna nimi **Nimi**-ruutuun.
1. Syötä **Kuvaus**-ruutuun kuvaus.
1. Valitse **Luo**.
1. Valitse toimintoruudussa **Uusi luokkasolmu** luodaksesi pääsolmun.
1. Anna nimi **Nimi**-ruutuun.
1. Syötä **Kuvaus**-ruutuun kuvaus.
1. Syötä **Kutsumanimi**-ruutuun kutsumanimi.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa näkyy esimerkki pääsolmusta.

![Pääsolmun esimerkki.](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a>Siirtymisluokkasolmujen luominen

Seuraavien ohjeiden avulla voit luoda lisää siirtymisluokkasolmuja edustamaan tuoteluokkia kanavalla.

1. Valitse siirtymisruudussa se pääsolmu, johon luokka lisätään.
1. Valitse toimintoruudusta **Uusi luokkasolmu**.
1. Anna nimi **Nimi**-ruutuun.
1. Syötä **Kuvaus**-ruutuun kuvaus.
1. Syötä **Kutsumanimi**-ruutuun kutsumanimi.
1. Syötä **Näyttöjärjestys**-ruutuun näyttöjärjestys (valinnainen).
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa näkyy esimerkki valmiista kanavan siirtymishierarkiasta.

![Kanavan hierarkian esimerkki.](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>Lisää tuotteita luokkasolmuihin

Voit lisätä tuotteita luokkasolmuihin noudattamalla seuraavia ohjeita.

1. Valitse luokkasolmu.
1. Valitse **Tuotteet**-kohdassa **Lisää**.
1. Etsi uudet tuotteet, jotka haluat lisätä tuotenumeron tai tuotteen nimen avulla, ja valitse sitten **OK**.
1. Valitse toimintoruudussa **Tallenna**.

> [!NOTE]
> Tuotteiden lisääminen kanavan siirtymishierarkiassa olevaan solmuun ei riitä siihen, että näkyisivät valitussa kanavassa, sillä tuotteet on myös lajiteltava kanavaan. Lisätietoa valikoimista on kohdassa [Valikoiman hallinta](assortments.md).

Seuraavassa kuvassa näkyy esimerkkisolmu, johon on lisätty tuotteita.

![Luokkasolmuun lisätyt tuotteet.](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>Tuotemääriteryhmien lisääminen luokkasolmuihin

> [!NOTE]
> Määriteryhmät on luotava ennen kuin voit lisätä ne solmuun kanavan siirtymishierarkian sisällä.

Voit lisätä tuotteen määriteryhmän luokkasolmuun seuraavien ohjeiden avulla.

1. Valitse luokkasolmu.
1. Valitse **Tuotteen määriteryhmä**-kohdassa **Lisää**.
1. Etsi lisättävät määriteryhmät ja valitse **OK**.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa näkyy esimerkkisolmu, johon on lisätty tuotemääriteryhmiä.

![Tuotemääriteryhmiä solmussa.](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>Lisäresurssit

[Valikoimien määrittäminen](set-up-assortments.md)

[Määritteiden ja määriteryhmien hallinta](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
