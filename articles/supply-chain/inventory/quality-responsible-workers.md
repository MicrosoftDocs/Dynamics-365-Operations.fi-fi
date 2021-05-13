---
title: Määrityksistä poikkeamisia hyväksyvät työntekijät
description: Tässä aiheessa kuvataan, kuinka määritetään määrityksistä poikkeamisia hyväksyvät työntekijät.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5979cb33146a00c3ea49ada9577140b24c07928f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956642"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="ad8a9-103">Määrityksistä poikkeamisia hyväksyvät työntekijät</span><span class="sxs-lookup"><span data-stu-id="ad8a9-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad8a9-104">Tässä aiheessa kuvataan, kuinka määritetään määrityksistä poikkeamisia hyväksyvät työntekijät.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="ad8a9-105">Määrityksistä poikkeamiset on hyväksyttävä, ennen kuin käyttäjät voivat alkaa syöttää tietoja, kuten korjauksia tai työvaiheita.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="ad8a9-106">Ennen kuin käyttäjät voivat hyväksyä tai hylätä määrityksistä poikkeamisia, käyttäjätunnus (käyttäjätietue) on linkitettävä työntekijätietueeseen.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="ad8a9-107">Voit vaihtoehtoisesti määrittää laadusta vastaavat työntekijät ja sallia sitten yhden työntekijän hyväksyä työt toisen työntekijän puolesta.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="ad8a9-108">Salli käyttäjälle määrityksistä poikkeamisen käsittely</span><span class="sxs-lookup"><span data-stu-id="ad8a9-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="ad8a9-109">Ennen kuin käyttäjä voi hyväksyä tai hylätä määrityksistä poikkeamisia, käyttäjätietue on linkitettävä työntekijätietueeseen.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="ad8a9-110">Tämän jälkeen hyväksyntäkentät voidaan määrittää automaattisesti, ja nykyinen käyttäjä voidaan täyttää aikaraportille automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="ad8a9-111">Ennen kuin käyttäjä voi käyttää asiakirjojen huomautuksia, tiedoston käsittely on aktivoitava käyttäjäasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="ad8a9-112">Valitse **Järjestelmänvalvojat \> Käyttäjät \> Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="ad8a9-113">Etsi ja avaa käyttäjä, jonka tulisi pystyä hyväksymään tai hylkäämään määrityksistä poikkeamisia.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="ad8a9-114">Määritä **Henkilö**-kenttään nykyiseen käyttäjätietueeseen liittyvän työntekijän nimi.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="ad8a9-115">Valitse toimintoruudussa **Käyttäjän asetukset**.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="ad8a9-116">**Asetukset**-sivulla nykyiselle käyttäjätietueelle **Asetukset**-välilehdessä määritä **Ota tiedoston käsittely käyttöön** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="ad8a9-117">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="ad8a9-118">Määritä laadusta vastaavat työntekijät</span><span class="sxs-lookup"><span data-stu-id="ad8a9-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="ad8a9-119">Siirry kohtaan **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Laadusta vastaavat työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="ad8a9-120">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="ad8a9-121">Valitse **Työntekijä**-kentästä työntekijä, joka lisää laatutiedot.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="ad8a9-122">Valitse **Vastuussa oleva työntekijä** -kentässä työntekijä, jonka puolesta valittu työntekijä syöttää työt.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="ad8a9-123">Kun määrityksistä poikkeamisia luodaan ja päivitetään, työntekijä syötetään oletusarvon mukaan **Työntekijä**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="ad8a9-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad8a9-124">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ad8a9-124">Additional resources</span></span>

- [<span data-ttu-id="ad8a9-125">Laadunhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="ad8a9-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="ad8a9-126">Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="ad8a9-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="ad8a9-127">Laadun kulut</span><span class="sxs-lookup"><span data-stu-id="ad8a9-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="ad8a9-128">Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="ad8a9-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="ad8a9-129">Määrityksistä poikkeamisten diagnostiikkatyypit</span><span class="sxs-lookup"><span data-stu-id="ad8a9-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="ad8a9-130">Määrityksistä poikkeamisten laatukulut</span><span class="sxs-lookup"><span data-stu-id="ad8a9-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="ad8a9-131">Toiminnot määrityksistä poikkeamisille</span><span class="sxs-lookup"><span data-stu-id="ad8a9-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="ad8a9-132">Laadunhallinta varastoprosesseja varten</span><span class="sxs-lookup"><span data-stu-id="ad8a9-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]