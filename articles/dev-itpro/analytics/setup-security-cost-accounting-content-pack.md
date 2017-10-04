---
title: "Kustannuslaskennan Power BI -sisällön suojauksen määrittäminen"
description: "Tässä ohjeaiheessa kerrotaan, miten Kustannuslaskennan käyttöoikeustason tietoturva täytetään Microsoft Power BI:n rivitason tietoturvaan. Tämä toiminto takaa, että käyttäjät näkevät vain Power BI -tietoja, joihin heillä on käyttöoikeus."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 04f8cb1a6375be9371bca2af7e4044392ce7322b
ms.openlocfilehash: 12fd8e11211b701304f9f4a68ff31f3b42e3e8ee
ms.contentlocale: fi-fi
ms.lasthandoff: 08/02/2017

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Kustannuslaskennan Power BI -sisällön suojauksen määrittäminen

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, miten Kustannuslaskennan käyttöoikeustason tietoturva täytetään Microsoft Power BI:n rivitason tietoturvaan. Tämä toiminto takaa, että käyttäjät näkevät vain Power BI -tietoja, joihin heillä on käyttöoikeus.

<a name="overview"></a>Yleiskuvaus
--------

Microsoft Power BI:n **Kustannuslaskennan analyysi** -sisältö rajoittaa käyttäjien käyttöoikeuksia Power BI:n rivitason tietoturvan avulla. Suojaus perustuu käyttöoikeustason organisaatiohierarkiaan, joka on määritetty Kustannuslaskennan parametreissa. Lisätietoja Power BI:n **kustannuslaskennan analyysi** -sisällöstä löydät kohdasta [Power BI:n kustannuslaskennan analyysi -sisältö](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Luo perustiedot
Power BI -sisällön omistajan on tehtävä seuraavat toimet täyttääkseen käyttöoikeustason tietoturva Power BI:hin. **Huomautus:** käyttäjä, joka julkaisee Power BI:n **kustannuslaskennan analyysi** -sisällön on automaattisesti omistaja. Vain omistaja voi Power BI:n tietoturvan. Lisäksi, kunnes omistaja lisää käyttäjiä PowerBI.com-sivustossa, vain omistaja voi nähdä Power BI:n **kustannuslaskennan analyysi** -sisällön tiedot.

1.  Julkaise määritystiedoston Power BI:hin.
2.  Kirjaudu PowerBI.com -sivustoon.
3.  Paikanna **Kustannuslaskennan analyysin** Power BI -sisällön tietojoukko.
4.  Avaa Suojaus-välilehti. 

    ![Suojaus-välilehden avaaminen](./media/CA-picture-1.png)

5.  **Kustannusobjektin vastuuhenkilö** -rooli on jo luotu. Lisätä muut kustannuslaskennan käyttöoikeustason organisaatiohierarkian jäsenet. 

    ![Jäsenten lisääminen](./media/CA-picture-2.png)

Käyttäjät, joille lisätään **Kustannusobjektin vastuuhenkilö** -rooli näkevät vain ne tiedot, joihin heillä on käyttöoikeus sen mukaan, miten kustannuslaskennan käyttöoikeustason organisaatiohierarkia on määritetty. **Huomautus:** Rivitason suojaus koskee ruutuja ja raportteja, jotka on upotettu Microsoft Dynamics 365 for Finance and Operationsiin Power BI:stä.

## <a name="updating-security"></a>Suojauksen päivittäminen
Jos kustannuslaskennan käyttöoikeustason suojaukseen tehdään päivityksiä ja haluat, että Power BI käyttää näitä päivityksiä, sinun on päivitettävä **kustannuslaskennan analyysin** Power BI -sisällön yksikkösäilö. Kun Finance and Operationsin yksikkösäilön päivitys on valmis, päivitä PowerBI.com-sivuston tiedot. Lisätietoja yksikkösäilön päivittämisestä on kohdassa [Yksikkösäilön päivittäminen](power-bi-integration-entity-store.md#update-entity-store). **Kkustannuslaskennan analyysin** Power BI -sisällön omistajan on suoritettava yksikkösäilön päivitys myös, jos uusille käyttäjille annetaan käyttöoikeus organisaatiohierarkiaan. Omistajan on lisäksi lisättävä uusille käyttäjille **Kustannusobjektini vastuuhenkilö** -rooli PowerBI.com-sivustossa, jotta rivitason tietoturva koskee heitä.

## <a name="disabling-security"></a>Suojauksen poistaminen käytöstä
Oletetaan, että organisaatiosi haluaa rajoittaa tietojen käyttöä. Jos jostain syystä suojausparametrit on poistettu käytöstä, kun suoritat kustannuslaskennan, omistajan on lisättävä käyttäjille Power BI:ssä **Kustannuslaskija** -rooli. Jos muutat suojauksen Käytössä-tilasta käytöstä poistetuksi, käyttäjien poistaminen **Kustannusobjektin vastuuhenkilö** -roolista voi olla tarpeen. Ja päinvastoin, jos otat suojauksen uudelleen käyttöön. Käyttäjät voivat kuulua molempiin rooleihin. Yhteinen käyttö on molempien roolien liitto. Kun kyseessä on **kustannuslaskennan analyysin** Power BI -sisältö, käyttäjillä, joilla on yhteinen käyttöoikeus, on rajoittamaton käyttöoikeus tietoihin. Jos tavoitteesi on rajoittaa käyttöoikeuksia, käyttäjät on määritettävä ainoastaan **Kustannusobjektin vastuuhenkilö** -rooliin. Nämä rivitason suojauspäivitykset tulevat voimaan heti. Käyttäjien, joita muutokset koskevat, tulisi päivittää selaimen sisältö.

## <a name="additional-resources"></a>Lisäresurssit
Katso lisätietoja Power BI:n rivitason suojauksesta kohdasta [Mallin tietoturvan hallinta Power BI:ssä](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).



