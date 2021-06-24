---
title: Kassavirtaennusteiden käyttöönotto (esiversio)
description: Tässä ohjeaiheessa kerrotaan, miten kassavirtaennusteiden toiminto otetaan käyttöön Finance Insightsissa.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222555"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="96b65-103">Kassavirtaennusteiden käyttöönotto (esiversio)</span><span class="sxs-lookup"><span data-stu-id="96b65-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="96b65-104">Tässä ohjeaiheessa kerrotaan, miten kassavirtaennusteiden toiminto otetaan käyttöön Finance Insightsissa.</span><span class="sxs-lookup"><span data-stu-id="96b65-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="96b65-105">Jos haluat käyttää kassavirran maksuennusteita, sinun on määritettävä asiakkaan maksuennusteiden toiminto kohdan [Asiakkaan maksuennusteiden käyttöönotto](enable-cust-paymnt-prediction.md) ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="96b65-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="96b65-106">Muodosta yhteys ympäristön Azure SQL:n ensisijaiseen esiintymään Microsoft Dynamics Lifecycle Services (LCS) -ratkaisun ympäristösivun tietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="96b65-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="96b65-107">Suorita seuraava Transact-SQL (T-SQL) -komento, jos haluat ottaa käyttöön eristysympäristön väliversiotestaukset.</span><span class="sxs-lookup"><span data-stu-id="96b65-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="96b65-108">(Sinun on ehkä otettava käyttöön IP-osoitteen käyttö LCS:ssä ennen etäyhteyden muodostamista Application Object Serveriin \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="96b65-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="96b65-109">Ohita tämä vaihe, jos käytössä on versio 10.0.20 tai myöhempi versio tai jos käytössä on Service Fabric -toteutus.</span><span class="sxs-lookup"><span data-stu-id="96b65-109">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="96b65-110">Finance Insightsin ryhmä on todennäköisesti jo ottanyt sen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="96b65-110">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="96b65-111">Jos et näe ominaisuutta **Toimintojen hallinta** -työtilassa tai jos sen käyttöönotossa on ongelmia, ota yhteyttä käyttämällä osoitetta <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="96b65-111">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="96b65-112">Avaa **Toimintojen hallinta** -työtila ja toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="96b65-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="96b65-113">Valitse **Tarkista päivitysten saatavuus**.</span><span class="sxs-lookup"><span data-stu-id="96b65-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="96b65-114">Ota seuraavat toiminnot käyttöön:</span><span class="sxs-lookup"><span data-stu-id="96b65-114">Turn on the following features:</span></span>

        - <span data-ttu-id="96b65-115">Uusi ruudukko-ohjausobjekti</span><span class="sxs-lookup"><span data-stu-id="96b65-115">New grid control</span></span>
        - <span data-ttu-id="96b65-116">Ryhmitteleminen ruudukoissa (esiversio)</span><span class="sxs-lookup"><span data-stu-id="96b65-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="96b65-117">Asiakkaan maksuennusteet (esiversio)</span><span class="sxs-lookup"><span data-stu-id="96b65-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="96b65-118">Kassavirtaennusteet (esiversio)</span><span class="sxs-lookup"><span data-stu-id="96b65-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="96b65-119">Siirry kohtaan **Maksuliikenteen hallinta \> Kassavirtaennusteen määritys** ja lisää rahatilit, jotka ennusteisiin lisätään.</span><span class="sxs-lookup"><span data-stu-id="96b65-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="96b65-120">Jos rahatilejä ei ole määritetty, kassavirtaa ei voi luoda.</span><span class="sxs-lookup"><span data-stu-id="96b65-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="96b65-121">Siirry kohtaan **Maksuliikenteen hallinta \> Asetukset \> Finance Insights (esiversio) \> Kassavirtaennusteet (esiversio)** ja tee seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="96b65-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="96b65-122">Valitse **Kassavirtaennuste**-välilehdessä **Ota toiminto käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="96b65-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="96b65-123">Valitse **Luo ennustemalli**.</span><span class="sxs-lookup"><span data-stu-id="96b65-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="96b65-124">Lisätietoja kassavirtaennusteominaisuudesta on kohdassa [Kassavirtaennusteet](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="96b65-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
