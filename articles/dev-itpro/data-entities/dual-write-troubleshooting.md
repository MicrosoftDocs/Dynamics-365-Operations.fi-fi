---
title: Tietojen integroinnin vianmääritysopas
description: Tässä ohjeaiheessa on vianetsintätietoja tietojen integroinnista Microsoft Dynamics 365 for Finance and Operationsin ja Common Data Servicen välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797272"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="f95e9-103">Tietojen integroinnin vianmääritysopas</span><span class="sxs-lookup"><span data-stu-id="f95e9-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="f95e9-104">Ota laajennusten seuranta käyttöön Common Data Servicessa ja tarkista kaksoiskirjoituksen laajennusvirheiden tiedot.</span><span class="sxs-lookup"><span data-stu-id="f95e9-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="f95e9-105">Jos kaksoiskirjoitussynkronoinnilla on ongelma tai virhe, voit tarkastaa jäljityslokin virheet:</span><span class="sxs-lookup"><span data-stu-id="f95e9-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="f95e9-106">Ennen kuin voit tarkastaa virheet, sinun on otettava laajennusten seuranta käyttöön [Laajennuksen rekisteröiminen](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) -ohjeiden avulla laajennuksen jäljityksen mahdollistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="f95e9-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="f95e9-107">Nyt voit tarkastaa virheet.</span><span class="sxs-lookup"><span data-stu-id="f95e9-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="f95e9-108">Kirjaudu Dynamics 365 for Salesiin.</span><span class="sxs-lookup"><span data-stu-id="f95e9-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="f95e9-109">Napsauta Asetukset-kuvaketta (ratas) ja valitse **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="f95e9-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="f95e9-110">Valitse **Asetukset**-valikosta **Mukautus > Laajennuksen jäljitysloki**.</span><span class="sxs-lookup"><span data-stu-id="f95e9-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="f95e9-111">Näet virheen tiedot napsauttamalla tyypin nimeä **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span><span class="sxs-lookup"><span data-stu-id="f95e9-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="f95e9-112">Tarkista kaksoiskirjoituksen synkronointivirheet Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="f95e9-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="f95e9-113">Voit tarkistaa virheet testauksen aikana noudattamalla seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="f95e9-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="f95e9-114">Kirjaudu Lifecycle Servicesiin (LCS).</span><span class="sxs-lookup"><span data-stu-id="f95e9-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="f95e9-115">Avaa LCS-projekti, jonka valitsit kaksoiskirjoitustestauksen suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="f95e9-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="f95e9-116">Siirry pilvipalveluympäristöihin.</span><span class="sxs-lookup"><span data-stu-id="f95e9-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="f95e9-117">Etätyöpöytäyhteys Finance and Operationsin virtuaalikoneeseen käyttämällä paikallista tiliä, joka näkyy LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="f95e9-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="f95e9-118">Avaa tapahtumien katseluohjelma.</span><span class="sxs-lookup"><span data-stu-id="f95e9-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="f95e9-119">Siirry kohtaan **Sovellusten ja palveluiden lokit > Microsoft > Dynamics > AX-DualWriteSync > Toiminnassa**.</span><span class="sxs-lookup"><span data-stu-id="f95e9-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="f95e9-120">Virheet ja tiedot näytetään.</span><span class="sxs-lookup"><span data-stu-id="f95e9-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="f95e9-121">Toisen Common Data Service -ympäristön linkityksen poistaminen ja linkittäminen Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="f95e9-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="f95e9-122">Voit päivittää linkkejä noudattamalla seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="f95e9-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="f95e9-123">Siirry Finance and Operations -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="f95e9-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="f95e9-124">Avaa Tietojen hallinta.</span><span class="sxs-lookup"><span data-stu-id="f95e9-124">Open Data Management.</span></span>
+ <span data-ttu-id="f95e9-125">Valitse **Linkki CDS for Appsiin**.</span><span class="sxs-lookup"><span data-stu-id="f95e9-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="f95e9-126">Valitse kaikki käynnissä olevat yhdistämismääritykset ja valitse **Pysäytä**.</span><span class="sxs-lookup"><span data-stu-id="f95e9-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="f95e9-127">Valitse kaikki yhdistämismääritykset ja valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="f95e9-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f95e9-128">**Poista**-vaihtoehto ei tule näkyviin, jos **CustomerV3-Account** -malli on valittuna.</span><span class="sxs-lookup"><span data-stu-id="f95e9-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="f95e9-129">Poista sen valinta tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="f95e9-129">Unselect it if needed.</span></span> <span data-ttu-id="f95e9-130">**CustomerV3-Account** on vanhempi valmisteltu malli, joka toimii Prospektista käteiseksi -ratkaisun kanssa.</span><span class="sxs-lookup"><span data-stu-id="f95e9-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="f95e9-131">Koska se julkaistaan maailmanlaajuisesti, se näkyy kaikkien mallien näkymässä.</span><span class="sxs-lookup"><span data-stu-id="f95e9-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="f95e9-132">Valitse **Poista ympäristön linkitys**.</span><span class="sxs-lookup"><span data-stu-id="f95e9-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="f95e9-133">Valitse **Kyllä** vahvistusta varten.</span><span class="sxs-lookup"><span data-stu-id="f95e9-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="f95e9-134">Voit linkittää uuden ympäristön noudattamalla [asennusoppaan](https://aka.ms/dualwrite-docs) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="f95e9-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

