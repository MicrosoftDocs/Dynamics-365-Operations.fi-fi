---
title: Määritä erillisen valmistuksen resurssiryhmä
description: Resurssiryhmä on operatiivisten resurssien joukko, joka vastaa yleensä tuotannon työnohjauksen keltaisten viivojen määrittämää työsolujen fyysistä organisaatiota.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24097cbb6f0ffae7b1b52bd3c70b7e054b3ce86c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257312"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="93942-103">Määritä erillisen valmistuksen resurssiryhmä</span><span class="sxs-lookup"><span data-stu-id="93942-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="93942-104">Resurssiryhmä on operatiivisten resurssien joukko, joka vastaa yleensä tuotannon työnohjauksen keltaisten viivojen määrittämää työsolujen fyysistä organisaatiota.</span><span class="sxs-lookup"><span data-stu-id="93942-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="93942-105">Tässä kuvataan, miten erillisessä tuotannossa käytettävä resurssiryhmä määritetään.</span><span class="sxs-lookup"><span data-stu-id="93942-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="93942-106">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="93942-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="93942-107">Siirry Resurssiryhmät-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="93942-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="93942-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="93942-108">Click New.</span></span>
3. <span data-ttu-id="93942-109">Kirjoita arvo Resurssiryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93942-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="93942-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93942-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="93942-111">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93942-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="93942-112">Syötä tai valitse arvo Tuotantoyksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93942-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="93942-113">Oletustoimintaparametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="93942-113">Define default operational parameters</span></span>
1. <span data-ttu-id="93942-114">Laajenna Työvaihe-osa.</span><span class="sxs-lookup"><span data-stu-id="93942-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="93942-115">Syötä numero Hävikkiprosentti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93942-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="93942-116">Syötä tai valitse arvo Asetusluokka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93942-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="93942-117">Syötä tai valitse arvo Ajoaikaluokka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93942-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="93942-118">Syötä numero Työvaiheen karkeasuunnittelun prosenttiosuus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="93942-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="93942-119">Työtuntien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="93942-119">Define operating hours</span></span>
1. <span data-ttu-id="93942-120">Laajenna Kalenterit-osa.</span><span class="sxs-lookup"><span data-stu-id="93942-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="93942-121">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="93942-121">Click Add.</span></span>
3. <span data-ttu-id="93942-122">Syötä tai valitse arvo Kalenteri-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93942-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="93942-123">Operatiivisten resurssien lisääminen</span><span class="sxs-lookup"><span data-stu-id="93942-123">Add operations resources</span></span>
1. <span data-ttu-id="93942-124">Laajenna Resurssit-osa.</span><span class="sxs-lookup"><span data-stu-id="93942-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="93942-125">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="93942-125">Click Add.</span></span>
3. <span data-ttu-id="93942-126">Syötä tai valitse arvo Resurssi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93942-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="93942-127">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="93942-127">Click Add.</span></span>
5. <span data-ttu-id="93942-128">Syötä tai valitse arvo Resurssi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93942-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="93942-129">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="93942-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="93942-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="93942-130">In the list, click the link in the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]