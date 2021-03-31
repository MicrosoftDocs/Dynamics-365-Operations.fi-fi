---
title: Tytäryhtiön tietojen vieminen tiedostoihin
description: Tässä aiheessa kerrotaan, miten tietoja viedään Microsoft Dynamics 365 Financesta ja tuodaan konsolidoituun yritykseen.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 33c17cc2c1dcaa57244bf0bfaa661b11b221e2f6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205496"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="95165-103">Tytäryhtiön tietojen vieminen tiedostoihin</span><span class="sxs-lookup"><span data-stu-id="95165-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95165-104">**Vienti**-sivulla (**Järjestelmänvalvonta \> Työtilat \> Tuonti/Vienti**) voit valmistella tytäryhtiöiden tietojen viennin tiedostoihin, jotka voidaan sitten tuoda konsilidoituun yritykseen.</span><span class="sxs-lookup"><span data-stu-id="95165-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="95165-105">Lisätietoja tietojen tuonti- ja vientiprosesseista on kohdassa [Tietojen tuonti- ja vientitöiden yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="95165-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="95165-106">Luo yritys konsolidointiprosessia varten.</span><span class="sxs-lookup"><span data-stu-id="95165-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="95165-107">Lisätietoja yritysten luomisesta on kohdassa [yrityksen luominen](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="95165-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="95165-108">Lisätietoja on kohdissa [Valmistele yritys, jota voidaan käyttää konsolidoinnissa](prepare-company-for-consolidation.md) ja [Määritä tytäryhtiö konsolidointia varten](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="95165-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="95165-109">Siirry kohtaan **Konsolidoinnit \> Vie yrityksen saldot**.</span><span class="sxs-lookup"><span data-stu-id="95165-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="95165-110">Määritä **Vie yrityksen saldot** -sivun **Ehdot**-välilehdessä konsolidoinnin tiedot määrittämällä seuraavat kentät.</span><span class="sxs-lookup"><span data-stu-id="95165-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="95165-111">Kenttä</span><span class="sxs-lookup"><span data-stu-id="95165-111">Field</span></span>                             | <span data-ttu-id="95165-112">kuvaus</span><span class="sxs-lookup"><span data-stu-id="95165-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="95165-113">Päätili</span><span class="sxs-lookup"><span data-stu-id="95165-113">Main account</span></span>                      | <span data-ttu-id="95165-114">Määritä konsolidoitavat tilit.</span><span class="sxs-lookup"><span data-stu-id="95165-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="95165-115">Jos haluat sisällyttää kaikki tilit, jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="95165-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="95165-116">Käytä konsolidointitiliä</span><span class="sxs-lookup"><span data-stu-id="95165-116">Use consolidation account</span></span>         | <span data-ttu-id="95165-117">Jos olet määrittänyt konsolidointitilit, määritä tämän asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="95165-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="95165-118">Valitse konsolidointitili seuraavasta</span><span class="sxs-lookup"><span data-stu-id="95165-118">Select consolidation account from</span></span> | <span data-ttu-id="95165-119">Valitse joko **Päätili** tai **Konsolidointitiliryhmä**.</span><span class="sxs-lookup"><span data-stu-id="95165-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="95165-120">Konsolidointitiliryhmä</span><span class="sxs-lookup"><span data-stu-id="95165-120">Consolidation account group</span></span>       | <span data-ttu-id="95165-121">Valitse valiltulle konsolidointitilille konsolidointitiliryhmä.</span><span class="sxs-lookup"><span data-stu-id="95165-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="95165-122">Konsolidointikausi</span><span class="sxs-lookup"><span data-stu-id="95165-122">Consolidation period</span></span>              | <span data-ttu-id="95165-123">Määritä Alkaen- ja Asti-päivämäärät konsolidoinnille.</span><span class="sxs-lookup"><span data-stu-id="95165-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="95165-124">Sisällytä todelliset summat</span><span class="sxs-lookup"><span data-stu-id="95165-124">Include actual amounts</span></span>            | <span data-ttu-id="95165-125">Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat sisällyttää todelliset summat.</span><span class="sxs-lookup"><span data-stu-id="95165-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="95165-126">Sisällytä budjettisummat</span><span class="sxs-lookup"><span data-stu-id="95165-126">Include budget amounts</span></span>            | <span data-ttu-id="95165-127">Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat sisällyttää budjettisummat konsolidoinneissa.</span><span class="sxs-lookup"><span data-stu-id="95165-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="95165-128">Budjettimallit</span><span class="sxs-lookup"><span data-stu-id="95165-128">Budget models</span></span>                     | <span data-ttu-id="95165-129">Määritä sisällytettävä budjettimalli.</span><span class="sxs-lookup"><span data-stu-id="95165-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="95165-130">Määritä **Taloushallinnon dimensiot** -välilehdessä konsolidoinnin tiedot:</span><span class="sxs-lookup"><span data-stu-id="95165-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="95165-131">Määritä taloushallinnon dimensiotiedot, jotka pitäisi siirtää tytäryhtiön tilitapahtumista konsolidointiyrityksen tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="95165-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="95165-132">Valitse taloushallinnon dimensio luettelosta.</span><span class="sxs-lookup"><span data-stu-id="95165-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="95165-133">Määritä jokaisen konsolidoidun taloushallinnon dimension oikea määritys.</span><span class="sxs-lookup"><span data-stu-id="95165-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="95165-134">Käytettävissä ovat vaihtoehdot **Dimensio**, **Ryhmädimensio**, **Yritystilit** ja **Tili**.</span><span class="sxs-lookup"><span data-stu-id="95165-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="95165-135">**Ryhmädimensio**-vaihtoehdolla voit määrittää dimensioarvon, jota konsolidoitavien yritysten ryhmä käyttää.</span><span class="sxs-lookup"><span data-stu-id="95165-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="95165-136">Määritä segmenttien järjestys, jonka mukaan konsolidointi tehdään.</span><span class="sxs-lookup"><span data-stu-id="95165-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="95165-137">Määritä vietävä yritys seuraavien vaiheiden mukaisesti **Yritykset**-välilehdessä:</span><span class="sxs-lookup"><span data-stu-id="95165-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="95165-138">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="95165-138">Select **New**.</span></span>
    2. <span data-ttu-id="95165-139">Kirjoita oikeushenkilö **Lähdeyritys**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="95165-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="95165-140">Jos samat kriteerit koskevat useita samassa tietokannassa olevia tytäryhtiöitä, voit siirtää näiden tytäryhtiöiden tiedot erillisiin vientitiedostoihin yhdellä toiminnolla:</span><span class="sxs-lookup"><span data-stu-id="95165-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="95165-141">Luo rivi kullekin tytäryritykselle, jonka tilit pitää viedä tiedostoihin.</span><span class="sxs-lookup"><span data-stu-id="95165-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="95165-142">Nämä tiedostot tuodaan konsolidointiyritykseen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="95165-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="95165-143">Määritä kunkin tytäryhtiön nimi sekä vientityön aikana luotavan vientitiedoston nimi.</span><span class="sxs-lookup"><span data-stu-id="95165-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="95165-144">Valitse **Muunnoserotusten tililaji** -kentässä **Voitot ja tappiot** tai **Tase**.</span><span class="sxs-lookup"><span data-stu-id="95165-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="95165-145">Kirjoita luotavan vientitiedoston tiedostonimi.</span><span class="sxs-lookup"><span data-stu-id="95165-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="95165-146">Suorita vienti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="95165-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="95165-147">Kun vienti on valmis, saat viestin, joka näyttää kuhunkin tiedostoon tallennettujen tietueiden lukumäärän.</span><span class="sxs-lookup"><span data-stu-id="95165-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="95165-148">Tämän jälkeen voit tuoda tiedostoja konsolidointiyritykseen.</span><span class="sxs-lookup"><span data-stu-id="95165-148">You can then import the files into the consolidated legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]