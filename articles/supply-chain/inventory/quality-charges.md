---
title: Määrityksistä poikkeamisen toimintojen kulut
description: Tässä aiheessa kuvataan, kuinka luodaan laatukuluja, joita voidaan käyttää määrityksistä poikkeamisen toiminnoissa.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfa424e94048aa9eb1ce4da9aa69e8d4df71cefb
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956637"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="440da-103">Määrityksistä poikkeamisen toimintojen kulut</span><span class="sxs-lookup"><span data-stu-id="440da-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="440da-104">Tässä aiheessa kuvataan, kuinka luodaan laatukuluja, joita voidaan käyttää määrityksistä poikkeamisen toiminnoissa.</span><span class="sxs-lookup"><span data-stu-id="440da-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="440da-105">Määritä **Laadun kulut** -sivulla kulujen tyypit, jotka voidaan lisätä määrityksistä poikkeamiseen liittyviin toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="440da-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="440da-106">Kulujen avulla voit seurata tietoja maksuista tai kuluista, jotka olet velkaa asiakkaalle määrityksistä poikkeavista tuotteista tai jotka toimittaja on velkaa sinulle saamistasi määrityksistä poikkeavista tuotteista.</span><span class="sxs-lookup"><span data-stu-id="440da-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="440da-107">Kulujen avulla voit myös seurata kustannuksia, joita edellytetään ulkoisilta toimittajilta tai palveluilta toiminnon suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="440da-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="440da-108">Esimerkkejä laadun kuluista</span><span class="sxs-lookup"><span data-stu-id="440da-108">Examples of quality charges</span></span>

<span data-ttu-id="440da-109">Työskentelet valmistusyhtiössä.</span><span class="sxs-lookup"><span data-stu-id="440da-109">You work for a manufacturing company.</span></span> <span data-ttu-id="440da-110">Yritykselläsi on sopimuksia useiden toimittajien kanssa.</span><span class="sxs-lookup"><span data-stu-id="440da-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="440da-111">Näissä sopimuksissa on kuvattu nimikkeiden ajallaan olevaa lähetystä, vahinkoja ja tuotteiden laatua koskevat vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="440da-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="440da-112">Samoin useat asiakkaasi ovat tehnyt yrityksesi kanssa sopimuksia palautuksista, vahingoista ja tuotteiden laadusta.</span><span class="sxs-lookup"><span data-stu-id="440da-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="440da-113">Maksurakenne määritetään jokaiselle tilanteelle ja määritetään sopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="440da-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="440da-114">Voit määrittää laatukuluja erityyppisten kulujen, kuten *Vahingot*, *Myöhässä oleva lähetys* ja *Laatu*, määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="440da-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="440da-115">Kun sitten luot määrityksistä poikkeamisen, lisäät yhden tai useita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="440da-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="440da-116">Määritä maksuja koskevat tiedot valitsemalla kunkin toiminnon kohdalla **Kulut**.</span><span class="sxs-lookup"><span data-stu-id="440da-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="440da-117">Laatukulun luominen</span><span class="sxs-lookup"><span data-stu-id="440da-117">Create a quality charge</span></span>

1. <span data-ttu-id="440da-118">Valitse **Varastonhallinta \> Asetukset \> Laadunhallinta \> Laadun kulut**.</span><span class="sxs-lookup"><span data-stu-id="440da-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="440da-119">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="440da-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="440da-120">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="440da-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="440da-121">**Kulujen koodi** – Kirjoita laatukulun yksilöivä tunnus tai nimi.</span><span class="sxs-lookup"><span data-stu-id="440da-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="440da-122">**Kuvaus** – Anna laatukulun yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="440da-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="440da-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="440da-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="440da-124">Laatukulun lisääminen määrityksistä poikkeamisen toimintoon</span><span class="sxs-lookup"><span data-stu-id="440da-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="440da-125">Lisätietoja toimintojen lisäämisestä määrityksistä poikkeamiseen ja kulujen kohdistamisesta niihin on kohdassa [Toiminnot määrityksistä poikkeamisille](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="440da-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="440da-126">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="440da-126">Additional resources</span></span>

- [<span data-ttu-id="440da-127">Laadunhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="440da-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="440da-128">Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="440da-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="440da-129">Määrityksistä poikkeamisia hyväksyvät työntekijät</span><span class="sxs-lookup"><span data-stu-id="440da-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="440da-130">Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="440da-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="440da-131">Määrityksistä poikkeamisten diagnostiikkatyypit</span><span class="sxs-lookup"><span data-stu-id="440da-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="440da-132">Määrityksistä poikkeamisten laatukulut</span><span class="sxs-lookup"><span data-stu-id="440da-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="440da-133">Toiminnot määrityksistä poikkeamisille</span><span class="sxs-lookup"><span data-stu-id="440da-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="440da-134">Laadunhallinta varastoprosesseja varten</span><span class="sxs-lookup"><span data-stu-id="440da-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
