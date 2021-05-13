---
title: Määrityksistä poikkeamisten diagnostiikkatyypit
description: Tässä aiheessa kuvataan, kuinka käytetään ja luodaan määrityksistä poikkeamisten kanssa käytettäviä diagnostiikkatyyppejä.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19fcd57e28efabd6ca32c444ab961b876bde424d
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956633"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="4bac7-103">Määrityksistä poikkeamisten diagnostiikkatyypit</span><span class="sxs-lookup"><span data-stu-id="4bac7-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bac7-104">Tässä aiheessa kuvataan, kuinka käytetään ja luodaan määrityksistä poikkeamisten kanssa käytettäviä diagnostiikkatyyppejä.</span><span class="sxs-lookup"><span data-stu-id="4bac7-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="4bac7-105">Määritä diagnostiikkatoimenpiteiden luokitus **Diagnostiikan tyypit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4bac7-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="4bac7-106">Kun luot korjauksen määrityksestä poikkeamiselle, valitset diagnostiikan.</span><span class="sxs-lookup"><span data-stu-id="4bac7-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="4bac7-107">Korjaus ilmaisee hyväksytyn poikkeaman vianmääritystoimenpiteen ja sen tekijän.</span><span class="sxs-lookup"><span data-stu-id="4bac7-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="4bac7-108">Se määrittää myös halutun ja suunnittelun valmistumispäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="4bac7-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="4bac7-109">Esimerkkejä diagnostiikkatyypeistä</span><span class="sxs-lookup"><span data-stu-id="4bac7-109">Examples of diagnostic types</span></span>

<span data-ttu-id="4bac7-110">Työskentelet valmistusyrityksessä, ja useat nimikkeet ovat epäonnistuneet laatutestissä.</span><span class="sxs-lookup"><span data-stu-id="4bac7-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="4bac7-111">Nämä nimikkeet siirretään karanteenialueelle ja merkitään määrityksistä poikkeaviksi tuotteiksi.</span><span class="sxs-lookup"><span data-stu-id="4bac7-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="4bac7-112">Määrityksistä poikkeamisen tietue luodaan Microsoft Dynamics 365 Supply Chain Managementissa tietojen seuraamiseksi ongelman ratkaisun kautta.</span><span class="sxs-lookup"><span data-stu-id="4bac7-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="4bac7-113">Tässä tapauksessa laatuongelmat tapahtuvat, koska nimikkeitä pakkaavan koneen laakerit ovat vioittuneet ja ylikuumenneet.</span><span class="sxs-lookup"><span data-stu-id="4bac7-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="4bac7-114">Tämän ongelman korjaus on laitteen osien korvaaminen.</span><span class="sxs-lookup"><span data-stu-id="4bac7-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="4bac7-115">Kun määrität diagnostiikkatyypit, voit luoda useita tietueita, joista jokainen edustaa erityyppistä ongelmaa, joka koneella saattaa olla.</span><span class="sxs-lookup"><span data-stu-id="4bac7-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="4bac7-116">Vaihtoehtoisesti voit luoda yhden yleisen diagnostiikkatyypin, joka kuvaa koneiden korjausta.</span><span class="sxs-lookup"><span data-stu-id="4bac7-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="4bac7-117">Diagnostiikkatyypin luominen</span><span class="sxs-lookup"><span data-stu-id="4bac7-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="4bac7-118">Valitse **Varastonhallinta \> Asetukset \> Laadunhallinta \> Diagnostiikan tyypit**.</span><span class="sxs-lookup"><span data-stu-id="4bac7-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="4bac7-119">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4bac7-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="4bac7-120">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="4bac7-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="4bac7-121">**Diagnostiikka** – Anna diagnostiikkatyypin yksilöivä tunniste tai nimi.</span><span class="sxs-lookup"><span data-stu-id="4bac7-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="4bac7-122">**Kuvaus** – Anna diagnostiikkatyypin yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="4bac7-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="4bac7-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4bac7-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4bac7-124">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4bac7-124">Additional resources</span></span>

- [<span data-ttu-id="4bac7-125">Laadunhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="4bac7-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="4bac7-126">Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="4bac7-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="4bac7-127">Määrityksistä poikkeamisia hyväksyvät työntekijät</span><span class="sxs-lookup"><span data-stu-id="4bac7-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="4bac7-128">Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="4bac7-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="4bac7-129">Määrityksistä poikkeamisten ongelmatyypit</span><span class="sxs-lookup"><span data-stu-id="4bac7-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="4bac7-130">Määrityksistä poikkeamisten laatukulut</span><span class="sxs-lookup"><span data-stu-id="4bac7-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="4bac7-131">Toiminnot määrityksistä poikkeamisille</span><span class="sxs-lookup"><span data-stu-id="4bac7-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="4bac7-132">Laadunhallinta varastoprosesseja varten</span><span class="sxs-lookup"><span data-stu-id="4bac7-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
