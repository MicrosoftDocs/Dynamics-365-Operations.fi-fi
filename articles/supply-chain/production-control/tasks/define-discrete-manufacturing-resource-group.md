--- 
title: "Määritä erillisen valmistuksen resurssiryhmä"
description: "Resurssiryhmä on operatiivisten resurssien joukko, joka vastaa yleensä tuotannon työnohjauksen keltaisten viivojen määrittämää työsolujen fyysistä organisaatiota."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2423fe91d1531a326080e3a584195ea864f2e3e
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="40451-103">Määritä erillisen valmistuksen resurssiryhmä</span><span class="sxs-lookup"><span data-stu-id="40451-103">Define discrete manufacturing resource group</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40451-104">Resurssiryhmä on operatiivisten resurssien joukko, joka vastaa yleensä tuotannon työnohjauksen keltaisten viivojen määrittämää työsolujen fyysistä organisaatiota.</span><span class="sxs-lookup"><span data-stu-id="40451-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="40451-105">Tässä kuvataan, miten erillisessä tuotannossa käytettävä resurssiryhmä määritetään.</span><span class="sxs-lookup"><span data-stu-id="40451-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="40451-106">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="40451-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="40451-107">Siirry Resurssiryhmät-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="40451-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="40451-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="40451-108">Click New.</span></span>
3. <span data-ttu-id="40451-109">Kirjoita arvo Resurssiryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="40451-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="40451-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="40451-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="40451-111">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="40451-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="40451-112">Syötä tai valitse arvo Tuotantoyksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="40451-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="40451-113">Oletustoimintaparametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="40451-113">Define default operational parameters</span></span>
1. <span data-ttu-id="40451-114">Laajenna Työvaihe-osa.</span><span class="sxs-lookup"><span data-stu-id="40451-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="40451-115">Syötä numero Hävikkiprosentti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="40451-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="40451-116">Syötä tai valitse arvo Asetusluokka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="40451-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="40451-117">Syötä tai valitse arvo Ajoaikaluokka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="40451-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="40451-118">Syötä numero Työvaiheen karkeasuunnittelun prosenttiosuus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="40451-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="40451-119">Työtuntien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="40451-119">Define operating hours</span></span>
1. <span data-ttu-id="40451-120">Laajenna Kalenterit-osa.</span><span class="sxs-lookup"><span data-stu-id="40451-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="40451-121">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="40451-121">Click Add.</span></span>
3. <span data-ttu-id="40451-122">Syötä tai valitse arvo Kalenteri-kenttään.</span><span class="sxs-lookup"><span data-stu-id="40451-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="40451-123">Operatiivisten resurssien lisääminen</span><span class="sxs-lookup"><span data-stu-id="40451-123">Add operations resources</span></span>
1. <span data-ttu-id="40451-124">Laajenna Resurssit-osa.</span><span class="sxs-lookup"><span data-stu-id="40451-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="40451-125">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="40451-125">Click Add.</span></span>
3. <span data-ttu-id="40451-126">Syötä tai valitse arvo Resurssi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="40451-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="40451-127">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="40451-127">Click Add.</span></span>
5. <span data-ttu-id="40451-128">Syötä tai valitse arvo Resurssi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="40451-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="40451-129">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="40451-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="40451-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="40451-130">In the list, click the link in the selected row.</span></span>


