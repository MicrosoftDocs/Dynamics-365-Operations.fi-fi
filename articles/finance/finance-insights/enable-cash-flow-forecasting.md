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
ms.openlocfilehash: 1977dac4a3ab66cca2248dc0124d3a06d6963f40
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978761"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="030bd-103">Kassavirtaennusteiden käyttöönotto (esiversio)</span><span class="sxs-lookup"><span data-stu-id="030bd-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="030bd-104">Tässä ohjeaiheessa kerrotaan, miten kassavirtaennusteiden toiminto otetaan käyttöön Finance Insightsissa.</span><span class="sxs-lookup"><span data-stu-id="030bd-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="030bd-105">Jos haluat käyttää kassavirran maksuennusteita, sinun on määritettävä asiakkaan maksuennusteiden toiminto kohdan [Asiakkaan maksuennusteiden käyttöönotto](enable-cust-paymnt-prediction.md) ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="030bd-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="030bd-106">Muodosta yhteys ympäristön Azure SQL:n ensisijaiseen esiintymään Microsoft Dynamics Lifecycle Services (LCS) -ratkaisun ympäristösivun tietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="030bd-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="030bd-107">Suorita seuraava Transact-SQL (T-SQL) -komento, jos haluat ottaa käyttöön eristysympäristön väliversiotestaukset.</span><span class="sxs-lookup"><span data-stu-id="030bd-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="030bd-108">(Sinun on ehkä otettava käyttöön IP-osoitteen käyttö LCS:ssä ennen etäyhteyden muodostamista Application Object Serveriin \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="030bd-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="030bd-109">Jos Microsoft Dynamics 365 Finance -käyttöönotto on Service Fabric -käyttöönotto, voit ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="030bd-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="030bd-110">Finance Insightsin ryhmä on todennäköisesti jo ottanyt sen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="030bd-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="030bd-111">Jos et näe toimintoja **Toimintojen hallinta** -työtilassa tai jos niiden käyttöönotossa on ongelmia, ota yhteyttä käyttämällä osoitetta <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="030bd-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="030bd-112">Avaa **Toimintojen hallinta** -työtila ja toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="030bd-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="030bd-113">Valitse **Tarkista päivitysten saatavuus**.</span><span class="sxs-lookup"><span data-stu-id="030bd-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="030bd-114">Ota seuraavat toiminnot käyttöön:</span><span class="sxs-lookup"><span data-stu-id="030bd-114">Turn on the following features:</span></span>

        - <span data-ttu-id="030bd-115">Uusi ruudukko-ohjausobjekti</span><span class="sxs-lookup"><span data-stu-id="030bd-115">New grid control</span></span>
        - <span data-ttu-id="030bd-116">Ryhmitteleminen ruudukoissa (esiversio)</span><span class="sxs-lookup"><span data-stu-id="030bd-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="030bd-117">Asiakkaan maksuennusteet (esiversio)</span><span class="sxs-lookup"><span data-stu-id="030bd-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="030bd-118">Kassavirtaennusteet (esiversio)</span><span class="sxs-lookup"><span data-stu-id="030bd-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="030bd-119">Siirry kohtaan **Maksuliikenteen hallinta \> Kassavirtaennusteen määritys** ja lisää rahatilit, jotka ennusteisiin lisätään.</span><span class="sxs-lookup"><span data-stu-id="030bd-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="030bd-120">Jos rahatilejä ei ole määritetty, kassavirtaa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="030bd-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="030bd-121">Siirry kohtaan **Maksuliikenteen hallinta \> Asetukset \> Finance Insights (esiversio) \> Kassavirtaennusteet (esiversio)** ja tee seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="030bd-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="030bd-122">Valitse **Kassavirtaennuste**-välilehdessä **Ota toiminto käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="030bd-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="030bd-123">Valitse **Luo ennustemalli**.</span><span class="sxs-lookup"><span data-stu-id="030bd-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="030bd-124">Lisätietoja kassavirtaennusteominaisuudesta on kohdassa [Kassavirtaennusteet](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="030bd-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="030bd-125">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="030bd-125">Privacy notice</span></span>

<span data-ttu-id="030bd-126">Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.</span><span class="sxs-lookup"><span data-stu-id="030bd-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
