---
title: EUR-00015 Toimittajan ALV-tunnuksen rekisteröinti
description: Tässä toimintaohjeessa kuvataan, miten ALV-tunnukset ja verovapausnumerot lisätään toimittajan tilille.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5126868038801091c7a9c17eee78e31db322cbb7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407887"
---
# <a name="eur-00015-registration-of-vendor-vat-id"></a><span data-ttu-id="50974-103">EUR-00015 Toimittajan ALV-tunnuksen rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="50974-103">EUR-00015 Registration of vendor VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50974-104">Tässä toimintaohjeessa kuvataan, miten ALV-tunnukset ja verovapausnumerot lisätään toimittajan tilille.</span><span class="sxs-lookup"><span data-stu-id="50974-104">This procedure shows how to add VAT registration IDs and a tax except number to a vendor account.</span></span> <span data-ttu-id="50974-105">Tämä prosessi on samanlainen yrityksille ja asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="50974-105">This process is similar for legal entities and customers.</span></span> 

<span data-ttu-id="50974-106">Ennen kuin tämän menettelyn voi suorittaa, ALV-tunnukset on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="50974-106">Before you can complete this procedure you must set up VAT IDs.</span></span> <span data-ttu-id="50974-107">Tämä menettely koskee kaikkia Euroopan maita/alueita.</span><span class="sxs-lookup"><span data-stu-id="50974-107">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="50974-108">Tämä menettely luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Saksassa.</span><span class="sxs-lookup"><span data-stu-id="50974-108">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="50974-109">Nämä toimet tekee yleensä tietojen hallinnan järjestelmänvalvoja, ostoreskontrapäällikkö tai myyntireskontrapäällikkö.</span><span class="sxs-lookup"><span data-stu-id="50974-109">This procedure is intended for a data management administrator, accounts payable manager, or accounts receivable manager.</span></span> <span data-ttu-id="50974-110">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="50974-110">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="50974-111">Siirry kohtaan Ostoreskontra > Toimittajat > Kaikki toimittajat.</span><span class="sxs-lookup"><span data-stu-id="50974-111">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="50974-112">Etsi luettelosta asiakas DE-01001 ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="50974-112">In the list find and select vendor DE-01001</span></span>
3. <span data-ttu-id="50974-113">Valitse Rekisteröintitunnukset.</span><span class="sxs-lookup"><span data-stu-id="50974-113">Click Registration IDs.</span></span>
4. <span data-ttu-id="50974-114">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="50974-114">Click Add.</span></span>
5. <span data-ttu-id="50974-115">Valitse ALV-tunnus.</span><span class="sxs-lookup"><span data-stu-id="50974-115">Select VAT ID.</span></span>
6. <span data-ttu-id="50974-116">Kirjoita Rekisteröintinumero-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="50974-116">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="50974-117">Määritä valitun toimittajan saksalainen ALV-tunnus.</span><span class="sxs-lookup"><span data-stu-id="50974-117">Specify a VAT ID in Germany for the selected vendor.</span></span> <span data-ttu-id="50974-118">Tunnuksen on vastattava rekisteröintityypille määritettyä muotoa.</span><span class="sxs-lookup"><span data-stu-id="50974-118">The ID must match the specified format of the registration type.</span></span>  
7. <span data-ttu-id="50974-119">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="50974-119">Click the General tab.</span></span>
8. <span data-ttu-id="50974-120">Kirjoita päivämäärä Voimassa-kenttään.</span><span class="sxs-lookup"><span data-stu-id="50974-120">In the Effective field, enter a date.</span></span>
9. <span data-ttu-id="50974-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="50974-121">Click Save.</span></span>
10. <span data-ttu-id="50974-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="50974-122">Click New.</span></span>
11. <span data-ttu-id="50974-123">Kirjoita Nimi tai kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="50974-123">In the Name or description field, type a value.</span></span>
    * <span data-ttu-id="50974-124">Syötä arvoksi esimerkiksi ITA.</span><span class="sxs-lookup"><span data-stu-id="50974-124">For example, enter ITA.</span></span>  
12. <span data-ttu-id="50974-125">Syötä tai valitse arvo Maa/alue-kentässä.</span><span class="sxs-lookup"><span data-stu-id="50974-125">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="50974-126">Voit valita esimerkiksi arvon ITA.</span><span class="sxs-lookup"><span data-stu-id="50974-126">For example, select ITA.</span></span>  
13. <span data-ttu-id="50974-127">Valitse Ensisijainen maalle -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="50974-127">Select Yes in the Primary for country field.</span></span>
14. <span data-ttu-id="50974-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="50974-128">Click Save.</span></span>
15. <span data-ttu-id="50974-129">Valitse Yhteenveto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="50974-129">Click the Overview tab.</span></span>
16. <span data-ttu-id="50974-130">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="50974-130">Click Add.</span></span>
17. <span data-ttu-id="50974-131">Syötä tai valitse arvo Rekisteröintityyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="50974-131">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="50974-132">Valitse esimerkiksi ALV-tunnus.</span><span class="sxs-lookup"><span data-stu-id="50974-132">For example, select VAT ID.</span></span>  
18. <span data-ttu-id="50974-133">Kirjoita Rekisteröintinumero-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="50974-133">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="50974-134">Määritä esimerkiksi italialainen ALV-tunnus.</span><span class="sxs-lookup"><span data-stu-id="50974-134">For example, specify a VAT ID in Italy.</span></span>  <span data-ttu-id="50974-135">Tunnuksen on vastattava rekisteröintityypille määritettyä muotoa.</span><span class="sxs-lookup"><span data-stu-id="50974-135">The ID must have the same format as the registration type.</span></span>  
19. <span data-ttu-id="50974-136">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="50974-136">Click Save.</span></span>
20. <span data-ttu-id="50974-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="50974-137">Close the page.</span></span>
21. <span data-ttu-id="50974-138">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="50974-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="50974-139">Voit valita esimerkiksi arvon DE-01001</span><span class="sxs-lookup"><span data-stu-id="50974-139">For example, select DE-01001.</span></span>  
22. <span data-ttu-id="50974-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="50974-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="50974-141">Laajenna Lasku ja toimitus -osa.</span><span class="sxs-lookup"><span data-stu-id="50974-141">Expand the Invoice and delivery section.</span></span>
24. <span data-ttu-id="50974-142">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="50974-142">Click Edit.</span></span>
25. <span data-ttu-id="50974-143">Anna tai valitse Verovapausnumero-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="50974-143">In the Tax exempt number field, enter or select a value.</span></span>
26. <span data-ttu-id="50974-144">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="50974-144">Click Save.</span></span>

