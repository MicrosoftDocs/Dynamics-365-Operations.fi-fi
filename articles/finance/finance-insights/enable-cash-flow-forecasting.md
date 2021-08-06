---
title: Kassavirtaennusteiden käyttöönotto (esiversio)
description: Tässä ohjeaiheessa kerrotaan, miten kassavirtaennusteiden toiminto otetaan käyttöön Finance Insightsissa.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 29118557a1de4d3521f8125395b26471f7f48f3e
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638618"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Kassavirtaennusteiden käyttöönotto (esiversio)

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten kassavirtaennusteiden toiminto otetaan käyttöön Finance Insightsissa.

> [!NOTE]
> Jos haluat käyttää kassavirran maksuennusteita, sinun on määritettävä asiakkaan maksuennusteiden toiminto kohdan [Asiakkaan maksuennusteiden käyttöönotto](enable-cust-paymnt-prediction.md) ohjeiden mukaan.

1. Muodosta yhteys ympäristön Azure SQL:n ensisijaiseen esiintymään Microsoft Dynamics Lifecycle Services (LCS) -ratkaisun ympäristösivun tietojen avulla. Suorita seuraava Transact-SQL (T-SQL) -komento, jos haluat ottaa käyttöön eristysympäristön väliversiotestaukset. (Sinun on ehkä otettava käyttöön IP-osoitteen käyttö LCS:ssä ennen etäyhteyden muodostamista Application Object Serveriin \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Ohita tämä vaihe, jos käytössä on versio 10.0.20 tai myöhempi versio tai jos käytössä on Service Fabric -toteutus. Finance Insightsin ryhmä on todennäköisesti jo ottanyt sen käyttöön. Jos et näe ominaisuutta **Toimintojen hallinta** -työtilassa tai jos sen käyttöönotossa on ongelmia, ota yhteyttä käyttämällä osoitetta <fiap@microsoft.com>.
  
2. Avaa **Toimintojen hallinta** -työtila ja toimi seuraavasti:

    1. Valitse **Tarkista päivitysten saatavuus**.
    2. Ota seuraavat toiminnot käyttöön:

        - Uusi ruudukko-ohjausobjekti
        - Ryhmitteleminen ruudukoissa (esiversio) 
        - Asiakkaan maksuennusteet (esiversio)
        - Kassavirtaennusteet (esiversio)

3. Siirry kohtaan **Maksuliikenteen hallinta \> Kassavirtaennusteen määritys** ja lisää rahatilit, jotka ennusteisiin lisätään.

    > [!NOTE]
    > Jos rahatilejä ei ole määritetty, kassavirtaa ei voi luoda.

4. Siirry kohtaan **Maksuliikenteen hallinta \> Asetukset \> Finance Insights (esiversio) \> Kassavirtaennusteet (esiversio)** ja tee seuraavat toiminnot:

    1. Valitse **Kassavirtaennuste**-välilehdessä **Ota toiminto käyttöön**.
    2. Valitse **Luo ennustemalli**.

Lisätietoja kassavirtaennusteominaisuudesta on kohdassa [Kassavirtaennusteet](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
