---
title: Määrityksistä poikkeamisten ongelmatyypit
description: Tässä aiheessa kuvataan, kuinka voit luoda ja käyttää ongelmatyyppejä määrityksistä poikkeamisille.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df509365f5c900898921acfbda380b5e20c7a251
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956644"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="ff5f6-103">Määrityksistä poikkeamisten ongelmatyypit</span><span class="sxs-lookup"><span data-stu-id="ff5f6-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff5f6-104">Tässä aiheessa kuvataan, kuinka voit luoda ja käyttää ongelmatyyppejä määrityksistä poikkeamisille.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="ff5f6-105">Määritä **Ongelmatyypit**-sivulla luokitus laatuongelmille, joita kohdataan erityyppisissä määrityksistä poikkeamisen tyypeissä.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="ff5f6-106">Määritä jokaiselle luotavalle ongelmatyypille määrityksistä poikkeamisten tyypit, joiden kanssa ongelmatyyppiä voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="ff5f6-107">Voit määrittää seuraavat määrityksistä poikkeamisten tyypit:</span><span class="sxs-lookup"><span data-stu-id="ff5f6-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="ff5f6-108">**Sisäinen** – Tämän tyyppiset määrityksistä poikkeamiset koskevat käytettävissä olevaa varastoa (esimerkiksi laatutilaukset tai karanteenitilaukset).</span><span class="sxs-lookup"><span data-stu-id="ff5f6-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="ff5f6-109">**Asiakas:** Tämän tyyppiset määrityksistä poikkeamiset liittyvät myyntitilauksiin.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="ff5f6-110">**Toimittaja:** Tämän tyyppiset määrityksistä poikkeamiset liittyvät ostotilauksiin.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="ff5f6-111">**Huoltopyyntö:** Tämän tyyppiset määrityksistä poikkeamiset liittyvät huoltotilauksiin.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="ff5f6-112">**Tuotanto** –Tämän tyyppiset määrityksistä poikkeamiset liittyvät erätilauksiin tai tuotantotilauksiin.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="ff5f6-113">**Oheistuotteen tuotanto** –Tämän tyyppiset määrityksistä poikkeamiset liittyvät erätilauksiin tai oheistuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="ff5f6-114">Kun luot uuden ongelman tyypin, valitse toimintoruudusta **Määrityksistä poikkeamisen tyypit** ja luo luettelo määrityksistä poikkeamisen tyypeistä, jotka on hyväksytty ongelmatyypille.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="ff5f6-115">Vikakoodiin liittyvä ongelmatyyppi voi esimerkiksi koskea kaikkia määrityksistä poikkeamisen tyyppejä.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="ff5f6-116">Asiakasvalituksiin liittyvä ongelmatyyppi saattaa kuitenkin koskea vain **Asiakas**- ja **Huoltopyyntö**-tyyppejä määrityksistä poikkeamisille.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="ff5f6-117">Esimerkkejä ongelmatyypeistä</span><span class="sxs-lookup"><span data-stu-id="ff5f6-117">Examples of problem types</span></span>

<span data-ttu-id="ff5f6-118">Seuraavassa on esimerkkejä ongelmatyyppien skenaarioista, joita voidaan käyttää eri määrityksistä poikkeamisten tyyppien kanssa:</span><span class="sxs-lookup"><span data-stu-id="ff5f6-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="ff5f6-119">**Asiakas**: Asiakas teki valituksen, asiakas teki palautuksen tai laatumääritykset eivät täyttyneet.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="ff5f6-120">**Toimittaja:** Tuote oli vioittunut, laatumääritykset eivät täyty tai väärä tuote vastaanotettiin.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="ff5f6-121">**Huoltopyyntö:** Laatumääritykset eivät täyty, asiakas teki valituksen tai kone on huollettava.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="ff5f6-122">**Tuotanto:** Laatumääritykset eivät täyty, kone on huollettava tai tuote on vioittunut.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="ff5f6-123">**Oheistuotteen tuotanto:** Laatumääritykset eivät täyty, kone on huollettava tai tuote on vioittunut.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="ff5f6-124">Ongelmatyypin luominen ja sen määrittäminen määrityksistä poikkeamisten tyyppeihin</span><span class="sxs-lookup"><span data-stu-id="ff5f6-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="ff5f6-125">Valitse **Varastonhallinta \> Asetukset \> Laadunhallinta \> Ongelmatyypit**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="ff5f6-126">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ff5f6-127">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="ff5f6-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ff5f6-128">**Ongelmatyyppi** – Anna ongelmatyypin yksilöivä tunniste tai nimi.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="ff5f6-129">**Kuvaus** – Anna ongelmatyypin yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="ff5f6-130">Kun uusi rivi on vielä valittuna, valitse **Määrityksistä poikkeamisen tyypit** toimintoruudusta.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="ff5f6-131">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ff5f6-132">Määritä sitten uudelle riville **Määrityksistä poikkeamisen tyyppi** -kentän arvoksi määrityksistä poikkeamisen tyyppi, jonka haluat sallia ongelmatyypille.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="ff5f6-133">Toista edellinen vaihe jokaiselle määrityksistä poikkeamisen tyypille, jonka haluat valtuuttaa ongelmatyypille.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="ff5f6-134">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff5f6-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ff5f6-135">Additional resources</span></span>

- [<span data-ttu-id="ff5f6-136">Laadunhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="ff5f6-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="ff5f6-137">Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="ff5f6-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="ff5f6-138">Määrityksistä poikkeamisia hyväksyvät työntekijät</span><span class="sxs-lookup"><span data-stu-id="ff5f6-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="ff5f6-139">Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="ff5f6-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="ff5f6-140">Määrityksistä poikkeamisten diagnostiikkatyypit</span><span class="sxs-lookup"><span data-stu-id="ff5f6-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="ff5f6-141">Määrityksistä poikkeamisten laatukulut</span><span class="sxs-lookup"><span data-stu-id="ff5f6-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="ff5f6-142">Toiminnot määrityksistä poikkeamisille</span><span class="sxs-lookup"><span data-stu-id="ff5f6-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="ff5f6-143">Laadunhallinta varastoprosesseja varten</span><span class="sxs-lookup"><span data-stu-id="ff5f6-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]