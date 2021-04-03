---
title: Kassavirtaennusteiden käyttöönotto (esiversio)
description: Tässä ohjeaiheessa kerrotaan, miten kassavirtaennusteiden toiminto otetaan käyttöön Finance Insightsissa.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 2de75962f5b8a71c8f7138289078b5c669ae1daa
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250575"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Kassavirtaennusteiden käyttöönotto (esiversio)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten kassavirtaennusteiden toiminto otetaan käyttöön Finance Insightsissa.

> [!NOTE]
> Jos haluat käyttää kassavirran maksuennusteita, sinun on määritettävä asiakkaan maksuennusteiden toiminto kohdan [Asiakkaan maksuennusteiden käyttöönotto](enable-cust-paymnt-prediction.md) ohjeiden mukaan.

1. Muodosta yhteys ympäristön Azure SQL:n ensisijaiseen esiintymään Microsoft Dynamics Lifecycle Services (LCS) -ratkaisun ympäristösivun tietojen avulla. Suorita seuraava Transact-SQL (T-SQL) -komento, jos haluat ottaa käyttöön eristysympäristön väliversiotestaukset. (Sinun on ehkä otettava käyttöön IP-osoitteen käyttö LCS:ssä ennen etäyhteyden muodostamista Application Object Serveriin \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Jos Microsoft Dynamics 365 Finance -käyttöönotto on Service Fabric -käyttöönotto, voit ohittaa tämän vaiheen. Finance Insightsin ryhmä on todennäköisesti jo ottanyt sen käyttöön. Jos et näe toimintoja **Toimintojen hallinta** -työtilassa tai jos niiden käyttöönotossa on ongelmia, ota yhteyttä käyttämällä osoitetta <fiap@microsoft.com>.
  
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

## <a name="privacy-notice"></a>Tietosuojatiedot

Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]