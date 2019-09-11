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
ms.openlocfilehash: 5e71729dafd2ad85a01b055363d1c7056b5558b2
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873102"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="6f97f-103">Tietojen integroinnin vianmääritysopas</span><span class="sxs-lookup"><span data-stu-id="6f97f-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="6f97f-104">Ota laajennusten seurantalokit käyttöön Common Data Servicessa ja tarkista kaksoiskirjoituksen laajennusvirheiden tiedot.</span><span class="sxs-lookup"><span data-stu-id="6f97f-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="6f97f-105">Jos kaksoiskirjoituksen synkronoinnin aikana ilmenee ongelma tai virhe, tarkista jäljityslokin virheet noudattamalla näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="6f97f-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="6f97f-106">Ennen kuin voit tarkastaa virheet, sinun on otettava käyttöön laajennuksen jäljityslokit.</span><span class="sxs-lookup"><span data-stu-id="6f97f-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="6f97f-107">Lisätietoja on seuravan oppaan Näytä seurantaloki -osassa: [Laajennuksen kirjoittaminen ja rekisteröinti](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span><span class="sxs-lookup"><span data-stu-id="6f97f-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="6f97f-108">Nyt voit tarkastaa virheet.</span><span class="sxs-lookup"><span data-stu-id="6f97f-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="6f97f-109">Kirjaudu sisään Microsoft Dynamics 365 for Sales -järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="6f97f-109">Sign in to Microsoft Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="6f97f-110">Valitse ensin **Asetukset**-painike (rataskuvake) ja sitten **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="6f97f-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="6f97f-111">Valitse **Asetukset**-valikosta **Mukautus \> Laajennuksen jäljitysloki**.</span><span class="sxs-lookup"><span data-stu-id="6f97f-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="6f97f-112">Näet virheen tiedot napsauttamalla tyypin nimeä **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span><span class="sxs-lookup"><span data-stu-id="6f97f-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="6f97f-113">Tarkista kaksoiskirjoituksen synkronointivirheet Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="6f97f-113">Inspect dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="6f97f-114">Tarkista testauksen aikana tapahtuvat virheet noudattamalla näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="6f97f-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="6f97f-115">Kirjaudu Microsoft Dynamics Lifecycle Servicesiin (LCS).</span><span class="sxs-lookup"><span data-stu-id="6f97f-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="6f97f-116">Avaa LCS-projekti, jotta voit tehdä kaksoiskirjoitustestauksen.</span><span class="sxs-lookup"><span data-stu-id="6f97f-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="6f97f-117">Valitse **Pilvipalveluympäristöt**.</span><span class="sxs-lookup"><span data-stu-id="6f97f-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="6f97f-118">Luo etätyöpöytäyhteys Dynamics 365 for Finance and Operations -virtuaalikoneeseen (VM) käyttämällä LCS:ssä näkyvää paikallista tiliä.</span><span class="sxs-lookup"><span data-stu-id="6f97f-118">Make a Remote desktop connection to the Dynamics 365 for Finance and Operations virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="6f97f-119">Avaa tapahtumien katseluohjelma.</span><span class="sxs-lookup"><span data-stu-id="6f97f-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="6f97f-120">Siirry kohtaan **Sovellusten ja palveluiden lokit \> Microsoft \> Dynamics \> AX -DualWriteSync \> Toiminnassa**.</span><span class="sxs-lookup"><span data-stu-id="6f97f-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="6f97f-121">Virheet ja tiedot näytetään.</span><span class="sxs-lookup"><span data-stu-id="6f97f-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-finance-and-operations-and-link-another-environment"></a><span data-ttu-id="6f97f-122">Common Data Service -ympäristön linkityksen poistaminen ja toisen ympäristön linkittäminen Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="6f97f-122">Unlink one Common Data Service environment from Finance and Operations and link another environment</span></span>

<span data-ttu-id="6f97f-123">Voit päivittää linkit seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="6f97f-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="6f97f-124">Siirry Finance and Operations -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="6f97f-124">Go to the Finance and Operations environment.</span></span>
2. <span data-ttu-id="6f97f-125">Avaa Tietojen hallinta.</span><span class="sxs-lookup"><span data-stu-id="6f97f-125">Open Data Management.</span></span>
3. <span data-ttu-id="6f97f-126">Valitse **Linkki CDS for Appsiin**.</span><span class="sxs-lookup"><span data-stu-id="6f97f-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="6f97f-127">Valitse kaikki suoritettavat yhdistämismääritykset ja valitse sitten **Pysäytä**.</span><span class="sxs-lookup"><span data-stu-id="6f97f-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="6f97f-128">Valitse kaikki yhdistämismääritykset ja valitse sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="6f97f-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f97f-129">**Poista**-vaihtoehto ei tule näkyviin, jos **CustomerV3-Account** -malli on valittuna.</span><span class="sxs-lookup"><span data-stu-id="6f97f-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="6f97f-130">Tyhjennä tämän mallin valinta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="6f97f-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="6f97f-131">**CustomerV3-Account** on vanhempi valmisteltu malli, joka toimii Prospektista käteiseksi -ratkaisun kanssa.</span><span class="sxs-lookup"><span data-stu-id="6f97f-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="6f97f-132">Koska se julkaistaan maailmanlaajuisesti, se näkyy kaikkien mallien näkymässä.</span><span class="sxs-lookup"><span data-stu-id="6f97f-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="6f97f-133">Valitse **Poista ympäristön linkitys**.</span><span class="sxs-lookup"><span data-stu-id="6f97f-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="6f97f-134">Vahvista toiminto valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6f97f-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="6f97f-135">Voit linkittää uuden ympäristön noudattamalla [asennusoppaan](https://aka.ms/dualwrite-docs) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="6f97f-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
