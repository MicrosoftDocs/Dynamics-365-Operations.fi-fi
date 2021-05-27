---
title: Toiminnot määrityksistä poikkeamisille
description: Tässä aiheessa kuvataan, kuinka voit luoda ja käyttää toimintoja määrityksistä poikkeamisille.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a6cc88b80f82d77edac0341cb6a3c0db4b42ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022201"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="28af2-103">Toiminnot määrityksistä poikkeamisille</span><span class="sxs-lookup"><span data-stu-id="28af2-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28af2-104">Tässä aiheessa kuvataan, kuinka voit luoda ja käyttää toimintoja määrityksistä poikkeamisille.</span><span class="sxs-lookup"><span data-stu-id="28af2-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="28af2-105">Määritä **Toiminnot**-sivulla luokitukset hyväksytyn määrityksistä poikkeamisen käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="28af2-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="28af2-106">Kun liität määrityksistä poikkeamiseen toiminnon, voit myös määrittää yksityiskohtia tietoja, kuten tietoja liittyvästä materiaalista, työtunneista ja erilaisista toiminnon tekemiseen tarvittavista kuluista.</span><span class="sxs-lookup"><span data-stu-id="28af2-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="28af2-107">Näiden tietojen avulla järjestelmä laskee toiminnon arvioidun kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="28af2-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="28af2-108">Tarkat tiedot ja arvioidut kustannukset on tarkoitettu viitetiedoiksi.</span><span class="sxs-lookup"><span data-stu-id="28af2-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="28af2-109">Laatuun liittyvät toiminnot poikkeavat tuotantoreititystä varten määritettävistä toiminnoista.</span><span class="sxs-lookup"><span data-stu-id="28af2-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="28af2-110">Vaikka voitkin seurata kustannuksia, aikaa ja nimikkeitä, joita käytetään määrityksistä poikkeamiseen liittyvässä toiminnossa, syötetyt tiedot ovat vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="28af2-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="28af2-111">Sitä ei integroida automaattisesti kirjanpitoon, varaston alareskontraan tai **Työajan seuranta** -moduuliin.</span><span class="sxs-lookup"><span data-stu-id="28af2-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="28af2-112">Esimerkkejä toiminnoista</span><span class="sxs-lookup"><span data-stu-id="28af2-112">Examples of operations</span></span>

<span data-ttu-id="28af2-113">Työskentelet valmistusyhtiössä.</span><span class="sxs-lookup"><span data-stu-id="28af2-113">You work for a manufacturing company.</span></span> <span data-ttu-id="28af2-114">Määrityksistä poikkeaminen luotiin ja hyväksyttiin nimikkeille, jotka epäonnistuivat laatutestissä.</span><span class="sxs-lookup"><span data-stu-id="28af2-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="28af2-115">Korjaus on luotu sen merkiksi, että ongelma liittyy koneen huonoon laakeriin.</span><span class="sxs-lookup"><span data-stu-id="28af2-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="28af2-116">Laakerin vaihto edellyttää useita vaiheita, ja kunkin työvaiheen vastuualuetta seurataan.</span><span class="sxs-lookup"><span data-stu-id="28af2-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="28af2-117">Esimerkiksi seuraavat vaiheet voivat olla pakollisia:</span><span class="sxs-lookup"><span data-stu-id="28af2-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="28af2-118">Tuotantorivi pysäytetään ja puhdistusrutiini suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="28af2-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="28af2-119">Huoltohenkilöt vaihtavat laakerin.</span><span class="sxs-lookup"><span data-stu-id="28af2-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="28af2-120">Laadunvalvontahenkilöstö tarkistaa laitteen, ennen kuin se kytketään takaisin päälle.</span><span class="sxs-lookup"><span data-stu-id="28af2-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="28af2-121">Tässä esimerkissä voidaan luoda seuraavat toiminnot, jotka edustavat työtä, joka on tehtävä:</span><span class="sxs-lookup"><span data-stu-id="28af2-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="28af2-122">Pysäytä tuotantorivi.</span><span class="sxs-lookup"><span data-stu-id="28af2-122">Stop the production line.</span></span>
- <span data-ttu-id="28af2-123">Puhdista tuotantorivi.</span><span class="sxs-lookup"><span data-stu-id="28af2-123">Clean out the production line.</span></span>
- <span data-ttu-id="28af2-124">Huolla kone.</span><span class="sxs-lookup"><span data-stu-id="28af2-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="28af2-125">Tarkista kone.</span><span class="sxs-lookup"><span data-stu-id="28af2-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="28af2-126">Luo toiminto</span><span class="sxs-lookup"><span data-stu-id="28af2-126">Create an operation</span></span>

1. <span data-ttu-id="28af2-127">Valitse **Varastonhallinta \> Asetukset \> Laadunhallinta \> Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="28af2-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="28af2-128">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="28af2-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="28af2-129">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="28af2-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="28af2-130">**Toiminto** – Syötä toiminnon yksilöivä tunnus tai nimi.</span><span class="sxs-lookup"><span data-stu-id="28af2-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="28af2-131">**Kuvaus** – Anna toiminnon yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="28af2-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="28af2-132">**Tyyppi** – Jos toimintoa voidaan käyttää vain määrityksistä poikkeamisiin, jotka liittyvät tiettyyn tilaustyyppiin, valitse tilaustyyppi (*Ostotilaus* tai *Myyntitilaus*).</span><span class="sxs-lookup"><span data-stu-id="28af2-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="28af2-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="28af2-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28af2-134">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="28af2-134">Additional resources</span></span>

- [<span data-ttu-id="28af2-135">Laadunhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="28af2-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="28af2-136">Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="28af2-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="28af2-137">Määrityksistä poikkeamisten luonti ja käsittely</span><span class="sxs-lookup"><span data-stu-id="28af2-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="28af2-138">Määrityksistä poikkeamisia hyväksyvät työntekijät</span><span class="sxs-lookup"><span data-stu-id="28af2-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="28af2-139">Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="28af2-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="28af2-140">Määrityksistä poikkeamisten diagnostiikkatyypit</span><span class="sxs-lookup"><span data-stu-id="28af2-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="28af2-141">Määrityksistä poikkeamisten laatukulut</span><span class="sxs-lookup"><span data-stu-id="28af2-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="28af2-142">Määrityksistä poikkeamisten ongelmatyypit</span><span class="sxs-lookup"><span data-stu-id="28af2-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="28af2-143">Laadunhallinta varastoprosesseja varten</span><span class="sxs-lookup"><span data-stu-id="28af2-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
