---
title: Budjettiehdotusten käyttöönotto (esiversio)
description: Tässä ohjeaiheessa kerrotaan, miten budjettiehdotustoiminto otetaan käyttöön Finance Insightsissa.
author: ShivamPandey-msft
ms.date: 07/24/2020
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
ms.openlocfilehash: 7e90a1a2f2a8e7808f03ce9a6ee58c027bd48d8d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818701"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="d2e62-103">Budjettiehdotusten käyttöönotto (esiversio)</span><span class="sxs-lookup"><span data-stu-id="d2e62-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d2e62-104">Tässä ohjeaiheessa kerrotaan, miten budjettiehdotustoiminto otetaan käyttöön Finance Insightsissa.</span><span class="sxs-lookup"><span data-stu-id="d2e62-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="d2e62-105">Muodosta yhteys ympäristön Azure SQL:n ensisijaiseen esiintymään Microsoft Dynamics Lifecycle Services (LCS) -ratkaisun ympäristösivun tietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="d2e62-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="d2e62-106">Suorita seuraava Transact-SQL (T-SQL) -komento, jos haluat ottaa käyttöön eristysympäristön väliversiotestaukset.</span><span class="sxs-lookup"><span data-stu-id="d2e62-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="d2e62-107">(Sinun on ehkä otettava käyttöön IP-osoitteen käyttö LCS:ssä ennen etäyhteyden muodostamista Application Object Serveriin \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="d2e62-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="d2e62-108">Jos Microsoft Dynamics 365 Finance -käyttöönotto on Service Fabric -käyttöönotto, voit ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="d2e62-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="d2e62-109">Finance Insightsin ryhmä on todennäköisesti jo ottanyt sen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="d2e62-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="d2e62-110">Jos ominaisuus ei ole **Toimintojen hallinta** -työtilassa tai jos sen käyttöönotossa on ongelmia, lähetä viesti [Finance Insights -sovelluksen esiversioryhmälle](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="d2e62-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="d2e62-111">Avaa **Toimintojen hallinta** -työtila ja toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d2e62-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="d2e62-112">Valitse **Tarkista päivitysten saatavuus**.</span><span class="sxs-lookup"><span data-stu-id="d2e62-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="d2e62-113">Hae **budjettiehdotus** ja ota toiminto käyttöön.</span><span class="sxs-lookup"><span data-stu-id="d2e62-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="d2e62-114">Siirry kohtaan **Budjetointi \> Asetukset \> Perusbudjetointi \> Budjettiehdotus (esiversio)** ja valitse **Ota toiminto käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="d2e62-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="d2e62-115">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="d2e62-115">Privacy notice</span></span>
<span data-ttu-id="d2e62-116">Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.</span><span class="sxs-lookup"><span data-stu-id="d2e62-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]