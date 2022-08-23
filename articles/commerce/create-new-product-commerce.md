---
title: Uuden tuotteen luominen Commercessa
description: Tässä artikkelissa käsitellään uuden tuotteen luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 01/27/2020
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
ms.openlocfilehash: 654ba19b0bc96ab40c8c27106fd819faa85a4ce8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270178"
---
# <a name="create-a-new-product-in-commerce"></a>Uuden tuotteen luominen Commercessa


[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään uuden tuotteen luontia Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus

Tuote määritetään ensisijaisesti tuotenumeron, nimen ja kuvauksen perusteella. Tuotteen tai palvelun kuvaamiseen tarvitaan myös muita tietoja:

## <a name="create-a-new-product"></a>Luo uusi tuote

1. Siirry selausruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Tuotteet ja luokat \> Tuotteet luokittain**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse avattavassa **Tuotetyyppi**-valikossa joko **Nimike** tai **Palvelu**.
1. Valitse avattavasta **Tuotteen alatyyppi** -luettelosta joko **Tuote** (jos tuotteella ei ole variantteja) tai **Päätuote** (jos tuotteella on variantteja).
1. Syötä **Tuotenumero**-ruutuun tuotenumero, jos sellaista ei ole täytetty valmiiksi.
1. Syötä **Tuotenimi** -ruutuun tuotteen nimi.
1. Syötä **Hakunimi**-ruutuun hakunimi.
1. Valitse avattavassa **Vähittäismyyntiluokka**-luettelosta asianmukainen luokka.
1. Jos tuote on pakkaus, valitse parametrin **Tuotepaketti** arvoksi **Kyllä**.
1. Jos tuotteen alatyyppi on päätuote, määritä **Tuotedimensioryhmä** sisältämään tuetut variantit. Vaihtoehtoja ovat **Väri**, **Koko**, **Tyyli** ja **Määritys**. Tarvittaessa sinun on luotava lisää tuotedimensioryhmiä.
1. Valitse avattavassa **Määritysteknologia**-luettelosta asianmukainen vaihtoehto.
1. Valitse **OK**.

Seuraavassa kuvassa näkyy esimerkkituotteen lisääminen.

![Tuotteen luominen.](media/create-new-product.png)

Kun tuote on lisätty, sille voidaan määrittää lisää tietoja. Näitä ovat esimerkiksi **Tuotekuvaus**, **Varianttiryhmät**, **Dimensioryhmät**, **Tuotemääritteet** ja **Liittyvät tuotteet**.

Seuraavassa kuvassa esitetään tuotteen lisätiedot.

![Tuotteen tiedot.](media/create-new-product-2.png)

### <a name="create-product-variants"></a>Luo tuotevariantit

Jos tuotteen alatyyppi on **Päätuote**, on luotava tiettyjä variantteja. 

Luo tuotevariantteja noudattamalla seuraavia vaiheita.

1. Valitse toimintoruudussa **Tuotevariantit**.
1. Jos toimintoruudussa on valittu varianttiryhmiä, valitse **varianttiehdotukset*.
1. Valitse variantit, joita haluaisit tukea tuotteen osalta.
1. Valitse **Luo**.

## <a name="release-a-product"></a>Tuotteen vapautus

Tuote on ensin vapautettava yritykselle, jotta se voidaan myydä.

1. Valitse tuotesivulla **Vapauta tuotteita**.

    ![Tuotteen vapauttaminen.](media/create-new-product-3.png)

1. Valitse vapautettava tuote ja sitten **Seuraava**.

    ![Vapautettavan tuotteen valitseminen.](media/create-new-product-4.png)

1. Valitse vapautettavien tuotevarianttien joukko ja valitse sitten **Seuraava**.

    ![Vapautettavien varianttien valitseminen.](media/create-new-product-5.png)

1. Valitse yritys ja sitten **Seuraava**.

    ![Yrityksen valitseminen.](media/create-new-product-6.png)

1. Valitse **Valmis**.

    ![Tuotteen vapautuksen viimeistely.](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a>Määritä vapautettu tuote

Kun tuote on vapautettu, se edellyttää lisämääritystä, johon kuuluu hinnan lisääminen tuotteelle.

1. Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäiskauppa ja kauppa \> Tuotteet ja luokat \> Vapautetut tuotteet luokan mukaan**.
1. Valitse vapautetulle tuotteelle tuoteluokkasolmu ja valitse sitten tuote tuoteluettelosta.
1. Valitse toimintoruudussa **Muokkaa**.
1. Määritä **Hankinta**-osassa tarvittavat ominaisuudet, kuten **Yksikkö**, **Hinta** ja **Määrä**.
1. Valitse toimintoruudussa **Vahvista** sen varmistamiseksi, ettei puuttuvien kenttien osalta anneta virheilmoituksia.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa on esimerkki vapautetun tuotteen asetusten määrityksistä.

![Vapautetun tuotteen määritys.](media/create-new-product-8.png)

## <a name="additional-resources"></a>Lisäresurssit

[Luo oikeushenkilöt](channels-legal-entities.md)

[Varianttiryhmän luominen](create-variant-group.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
