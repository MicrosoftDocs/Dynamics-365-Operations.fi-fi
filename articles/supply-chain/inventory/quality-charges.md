---
title: Määrityksistä poikkeamisen toimintojen kulut
description: Tässä aiheessa kuvataan, kuinka luodaan laatukuluja, joita voidaan käyttää määrityksistä poikkeamisen toiminnoissa.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 382890232bff47a885840af1eb7e91d27bb46cae
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022297"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="f9873-103">Määrityksistä poikkeamisen toimintojen kulut</span><span class="sxs-lookup"><span data-stu-id="f9873-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9873-104">Tässä aiheessa kuvataan, kuinka luodaan laatukuluja, joita voidaan käyttää määrityksistä poikkeamisen toiminnoissa.</span><span class="sxs-lookup"><span data-stu-id="f9873-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="f9873-105">Määritä **Laadun kulut** -sivulla kulujen tyypit, jotka voidaan lisätä määrityksistä poikkeamiseen liittyviin toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="f9873-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="f9873-106">Kulujen avulla voit seurata tietoja maksuista tai kuluista, jotka olet velkaa asiakkaalle määrityksistä poikkeavista tuotteista tai jotka toimittaja on velkaa sinulle saamistasi määrityksistä poikkeavista tuotteista.</span><span class="sxs-lookup"><span data-stu-id="f9873-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="f9873-107">Kulujen avulla voit myös seurata kustannuksia, joita edellytetään ulkoisilta toimittajilta tai palveluilta toiminnon suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="f9873-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="f9873-108">Esimerkkejä laadun kuluista</span><span class="sxs-lookup"><span data-stu-id="f9873-108">Examples of quality charges</span></span>

<span data-ttu-id="f9873-109">Työskentelet valmistusyhtiössä.</span><span class="sxs-lookup"><span data-stu-id="f9873-109">You work for a manufacturing company.</span></span> <span data-ttu-id="f9873-110">Yritykselläsi on sopimuksia useiden toimittajien kanssa.</span><span class="sxs-lookup"><span data-stu-id="f9873-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="f9873-111">Näissä sopimuksissa on kuvattu nimikkeiden ajallaan olevaa lähetystä, vahinkoja ja tuotteiden laatua koskevat vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="f9873-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="f9873-112">Samoin useat asiakkaasi ovat tehnyt yrityksesi kanssa sopimuksia palautuksista, vahingoista ja tuotteiden laadusta.</span><span class="sxs-lookup"><span data-stu-id="f9873-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="f9873-113">Maksurakenne määritetään jokaiselle tilanteelle ja määritetään sopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="f9873-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="f9873-114">Voit määrittää laatukuluja erityyppisten kulujen, kuten *Vahingot*, *Myöhässä oleva lähetys* ja *Laatu*, määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="f9873-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="f9873-115">Kun sitten luot määrityksistä poikkeamisen, lisäät yhden tai useita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="f9873-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="f9873-116">Määritä maksuja koskevat tiedot valitsemalla kunkin toiminnon kohdalla **Kulut**.</span><span class="sxs-lookup"><span data-stu-id="f9873-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="f9873-117">Laatukulun luominen</span><span class="sxs-lookup"><span data-stu-id="f9873-117">Create a quality charge</span></span>

1. <span data-ttu-id="f9873-118">Valitse **Varastonhallinta \> Asetukset \> Laadunhallinta \> Laadun kulut**.</span><span class="sxs-lookup"><span data-stu-id="f9873-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="f9873-119">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f9873-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="f9873-120">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="f9873-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="f9873-121">**Kulujen koodi** – Kirjoita laatukulun yksilöivä tunnus tai nimi.</span><span class="sxs-lookup"><span data-stu-id="f9873-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="f9873-122">**Kuvaus** – Anna laatukulun yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f9873-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="f9873-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f9873-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="f9873-124">Laatukulun lisääminen määrityksistä poikkeamisen toimintoon</span><span class="sxs-lookup"><span data-stu-id="f9873-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="f9873-125">Lisätietoja toimintojen lisäämisestä määrityksistä poikkeamiseen ja kulujen kohdistamisesta niihin on kohdassa [Toiminnot määrityksistä poikkeamisille](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="f9873-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9873-126">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f9873-126">Additional resources</span></span>

- [<span data-ttu-id="f9873-127">Laadunhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="f9873-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="f9873-128">Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="f9873-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="f9873-129">Määrityksistä poikkeamisia hyväksyvät työntekijät</span><span class="sxs-lookup"><span data-stu-id="f9873-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="f9873-130">Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="f9873-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="f9873-131">Määrityksistä poikkeamisten diagnostiikkatyypit</span><span class="sxs-lookup"><span data-stu-id="f9873-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="f9873-132">Määrityksistä poikkeamisten laatukulut</span><span class="sxs-lookup"><span data-stu-id="f9873-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="f9873-133">Toiminnot määrityksistä poikkeamisille</span><span class="sxs-lookup"><span data-stu-id="f9873-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="f9873-134">Laadunhallinta varastoprosesseja varten</span><span class="sxs-lookup"><span data-stu-id="f9873-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
