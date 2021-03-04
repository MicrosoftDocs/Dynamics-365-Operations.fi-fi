---
title: Budjettiehdotusten käyttöönotto (esiversio)
description: Tässä ohjeaiheessa kerrotaan, miten budjettiehdotustoiminto otetaan käyttöön Finance Insightsissa.
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
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: d8443c4e3e6f3d3a90acedc7c05b2846d6b68369
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646202"
---
# <a name="enable-budget-proposals-preview"></a>Budjettiehdotusten käyttöönotto (esiversio)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten budjettiehdotustoiminto otetaan käyttöön Finance Insightsissa.

1. Muodosta yhteys ympäristön Azure SQL:n ensisijaiseen esiintymään Microsoft Dynamics Lifecycle Services (LCS) -ratkaisun ympäristösivun tietojen avulla. Suorita seuraava Transact-SQL (T-SQL) -komento, jos haluat ottaa käyttöön eristysympäristön väliversiotestaukset. (Sinun on ehkä otettava käyttöön IP-osoitteen käyttö LCS:ssä ennen etäyhteyden muodostamista Application Object Serveriin \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Jos Microsoft Dynamics 365 Finance -käyttöönotto on Service Fabric -käyttöönotto, voit ohittaa tämän vaiheen. Finance Insightsin ryhmä on todennäköisesti jo ottanyt sen käyttöön. Jos ominaisuus ei ole **Toimintojen hallinta** -työtilassa tai jos sen käyttöönotossa on ongelmia, lähetä viesti [Finance Insights -sovelluksen esiversioryhmälle](mailto:fiap@microsoft.com).

2. Avaa **Toimintojen hallinta** -työtila ja toimi seuraavasti:

    1. Valitse **Tarkista päivitysten saatavuus**.
    2. Hae **budjettiehdotus** ja ota toiminto käyttöön.

3. Siirry kohtaan **Budjetointi \> Asetukset \> Perusbudjetointi \> Budjettiehdotus (esiversio)** ja valitse **Ota toiminto käyttöön**.

#### <a name="privacy-notice"></a>Tietosuojatiedot
Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.