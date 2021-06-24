---
title: Budjettiehdotusten käyttöönotto (esiversio)
description: Tässä ohjeaiheessa kerrotaan, miten budjettiehdotustoiminto otetaan käyttöön Finance Insightsissa.
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
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222531"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="8a17e-103">Budjettiehdotusten käyttöönotto (esiversio)</span><span class="sxs-lookup"><span data-stu-id="8a17e-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8a17e-104">Tässä ohjeaiheessa kerrotaan, miten budjettiehdotustoiminto otetaan käyttöön Finance Insightsissa.</span><span class="sxs-lookup"><span data-stu-id="8a17e-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="8a17e-105">Muodosta yhteys ympäristön Azure SQL:n ensisijaiseen esiintymään Microsoft Dynamics Lifecycle Services (LCS) -ratkaisun ympäristösivun tietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="8a17e-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="8a17e-106">Suorita seuraava Transact-SQL (T-SQL) -komento, jos haluat ottaa käyttöön eristysympäristön väliversiotestaukset.</span><span class="sxs-lookup"><span data-stu-id="8a17e-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="8a17e-107">(Sinun on ehkä otettava käyttöön IP-osoitteen käyttö LCS:ssä ennen etäyhteyden muodostamista Application Object Serveriin \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="8a17e-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="8a17e-108">Ohita tämä vaihe, jos käytössä on versio 10.0.20 tai myöhempi versio tai jos käytössä on Service Fabric -toteutus.</span><span class="sxs-lookup"><span data-stu-id="8a17e-108">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="8a17e-109">Finance Insightsin ryhmä on todennäköisesti jo ottanyt sen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8a17e-109">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="8a17e-110">Jos et näe ominaisuutta **Toimintojen hallinta** -työtilassa tai jos sen käyttöönotossa on ongelmia, ota yhteyttä käyttämällä osoitetta <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="8a17e-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="8a17e-111">Avaa **Toimintojen hallinta** -työtila ja toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="8a17e-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="8a17e-112">Valitse **Tarkista päivitysten saatavuus**.</span><span class="sxs-lookup"><span data-stu-id="8a17e-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="8a17e-113">Hae **budjettiehdotus** ja ota toiminto käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8a17e-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="8a17e-114">Siirry kohtaan **Budjetointi \> Asetukset \> Perusbudjetointi \> Budjettiehdotus (esiversio)** ja valitse **Ota toiminto käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="8a17e-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
