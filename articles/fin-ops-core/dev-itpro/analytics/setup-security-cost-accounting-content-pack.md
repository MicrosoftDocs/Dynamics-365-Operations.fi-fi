---
title: Kustannuslaskenta-analyysin Power BI -sisällön suojauksen määrittäminen
description: Tässä artikkelissa kerrotaan, miten Kustannuslaskennan käyttöoikeustason tietoturva täytetään Microsoft Power BI:n rivitason tietoturvaan.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.openlocfilehash: 9f019bec9c28602e31b43a8b3ab820f4a3a31ee8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267929"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Kustannuslaskenta-analyysin Power BI -sisällön suojauksen määrittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten Kustannuslaskennan käyttöoikeustason tietoturva täytetään Microsoft Power BI:n rivitason tietoturvaan. Tämä toiminto takaa, että käyttäjät näkevät vain Power BI -tietoja, joihin heillä on käyttöoikeus.

## <a name="overview"></a>Yleiskuvaus

**Kustannuslaskennan analyysin** Microsoft Power BI -sisältö rajoittaa käyttäjien käyttöoikeuksia Power BI:n rivitason tietoturvan avulla. Suojaus perustuu käyttöoikeustason organisaatiohierarkiaan, joka on määritetty Kustannuslaskennan parametreissa. Lisätietoja **kustannuslaskennan analyysin** Power BI -sisällöstä on kohdassa [Kustannuslaskennan analyysin Power BI -sisältö](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Luo perustiedot
Power BI -sisällön omistajan on tehtävä seuraavat toimet täyttääkseen käyttöoikeustason tietoturvan Power BI:hin.

> [!NOTE]
> Käyttäjä, joka julkaisee **kustannuslaskennan analyysin** Power BI -sisällön on automaattisesti omistaja. Vain omistaja voi määrittää Power BI:n tietoturvan. Ennen kuin omistaja lisää käyttäjiä PowerBI.com-sivustossa, vain omistaja voi nähdä **kustannuslaskennan analyysin** Power BI -sisällön tiedot.

1. Julkaise määritystiedosto Power BI:hin.
2. Kirjaudu PowerBI.com -sivustoon.
3. Paikanna **kustannuslaskennan analyysin** Power BI -sisällön tietojoukko.
4. Avaa Suojaus-välilehti.

    ![Suojaus-välilehden avaaminen.](./media/CA-picture-1.png)

5. **Kustannusobjektin vastuuhenkilö** -rooli on jo luotu. Lisätä muut kustannuslaskennan käyttöoikeustason organisaatiohierarkian jäsenet.

    ![Jäsenten lisääminen.](./media/CA-picture-2.png)

Käyttäjät, joille lisätään **Kustannusobjektin vastuuhenkilö** -rooli näkevät vain ne tiedot, joihin heillä on käyttöoikeus sen mukaan, miten kustannuslaskennan käyttöoikeustason organisaatiohierarkia on määritetty.

> [!NOTE]
> Rivitason suojaus koskee ruutuja ja raportteja, jotka on upotettu Power BI:stä.

## <a name="updating-security"></a>Suojauksen päivittäminen
Jos kustannuslaskennan käyttöoikeustason suojaukseen tehdään päivityksiä ja haluat, että Power BI käyttää näitä päivityksiä, sinun on päivitettävä **kustannuslaskennan analyysin** Power BI -sisällön yksikkösäilö. Kun yksikkösäilön päivitys on valmis, sinun täytyy päivittää PowerBI.com-sivuston tiedot. Lisätietoja yksikkösäilön päivittämisestä on kohdassa [Power BI:n ja yksikkösäilön integrointi](power-bi-integration-entity-store.md#update-entity-store). **Kustannuslaskennan analyysin** Power BI -sisällön omistajan on suoritettava yksikkösäilön päivitys myös, jos uusille käyttäjille annetaan käyttöoikeus organisaatiohierarkiaan. Omistajan on lisäksi lisättävä uusille käyttäjille **Kustannusobjektini vastuuhenkilö** -rooli PowerBI.com-sivustossa, jotta rivitason tietoturva koskee heitä.

## <a name="disabling-security"></a>Suojauksen poistaminen käytöstä
Oletetaan, että organisaatiosi haluaa rajoittaa tietojen käyttöä. Jos jostain syystä suojausparametrit on poistettu käytöstä, kun suoritat kustannuslaskennan, omistajan on lisättävä käyttäjille Power BI:ssä **Kustannuslaskija**-rooli. Jos muutat suojauksen Käytössä-tilasta käytöstä poistetuksi, käyttäjien poistaminen **Kustannusobjektin vastuuhenkilö** -roolista voi olla tarpeen. Ja päinvastoin, jos otat suojauksen uudelleen käyttöön. Käyttäjät voivat kuulua molempiin rooleihin. Yhteinen käyttö on molempien roolien liitto. Kun kyseessä on **kustannuslaskennan analyysin** Power BI -sisältö, käyttäjillä, joilla on yhteinen käyttöoikeus, on rajoittamaton käyttöoikeus tietoihin. Jos tavoitteesi on rajoittaa käyttöoikeuksia, käyttäjät on määritettävä ainoastaan **Kustannusobjektin vastuuhenkilö** -rooliin. Nämä rivitason suojauspäivitykset tulevat voimaan heti. Käyttäjien, joita muutokset koskevat, tulisi päivittää selaimen sisältö.

## <a name="additional-resources"></a>Lisäresurssit
Lisätietoja Power BI:n rivitason suojauksesta on kohdassa [Mallin tietoturvan hallinta Power BI:ssä](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
