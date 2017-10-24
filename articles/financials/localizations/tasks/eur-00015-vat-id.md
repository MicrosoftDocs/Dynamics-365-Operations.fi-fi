--- 
title: "Määritä ALV-tunnus"
description: "Tämä toimintosarja opastaa ALV-tunnuksen rekisteröinnin edellytykset, kuten rekisteröintityypin määrittämisen ja sen liittämisen rekisteröintiluokkaan."
author: v-oloski
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 20f64385b988ff48d865d2d521a9e580dc04c4a2
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-vat-id"></a><span data-ttu-id="d179d-103">Määritä ALV-tunnus</span><span class="sxs-lookup"><span data-stu-id="d179d-103">Set up VAT ID</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d179d-104">Tämä toimintosarja opastaa ALV-tunnuksen rekisteröinnin edellytykset, kuten rekisteröintityypin määrittämisen ja sen liittämisen rekisteröintiluokkaan.</span><span class="sxs-lookup"><span data-stu-id="d179d-104">This procedure walks you through VAT ID registration prerequisites, such as setting up a registration type and assigning it to a registration category.</span></span> <span data-ttu-id="d179d-105">Löydät lisätietoja rekisteröintitunnuksista niiden käsittelystä, mukaan lukien niiden edellytykset, Rekisteröintitunnukset-ohjeaiheesta.</span><span class="sxs-lookup"><span data-stu-id="d179d-105">You can find additional information about registration IDs and registration ID processing, including required prerequisites, in the Registration IDs help topic.</span></span> 

<span data-ttu-id="d179d-106">Nämä tiedot koskevat kaikkia Euroopan maita/alueita.</span><span class="sxs-lookup"><span data-stu-id="d179d-106">The information here applies to all European countries/regions.</span></span> <span data-ttu-id="d179d-107">Tämä tehtävä luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Saksassa.</span><span class="sxs-lookup"><span data-stu-id="d179d-107">The task was created using the demo data company DEMF with Germany as the legal entity primary address.</span></span> <span data-ttu-id="d179d-108">Tämä tehtävä on tarkoitettu järjestelmänvalvojille.</span><span class="sxs-lookup"><span data-stu-id="d179d-108">This task is intended for system administrators.</span></span> <span data-ttu-id="d179d-109">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="d179d-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="d179d-110">Valitse Organisaation hallinto > Yleinen osoitekirja > Rekisteröintityypit > Rekisteröintityypit.</span><span class="sxs-lookup"><span data-stu-id="d179d-110">Go to Organization administration > Global address book > Registration types > Registration types.</span></span>
2. <span data-ttu-id="d179d-111">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="d179d-111">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="d179d-112">Syötä Nimi-kenttään arvoksi "ALV-tunnus".</span><span class="sxs-lookup"><span data-stu-id="d179d-112">In the Name field, type 'VAT ID'.</span></span>
4. <span data-ttu-id="d179d-113">Kirjoita Kuvaus-kenttään ALV-numero.</span><span class="sxs-lookup"><span data-stu-id="d179d-113">In the Description field, VAT number.</span></span>
5. <span data-ttu-id="d179d-114">Syötä tai valitse arvoksi DEU Maa/alue-kentässä</span><span class="sxs-lookup"><span data-stu-id="d179d-114">In the Country/region field, enter or select a value DEU</span></span>
6. <span data-ttu-id="d179d-115">Valitse Yksilöllinen-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d179d-115">Select Yes in the Unique field.</span></span>
    * <span data-ttu-id="d179d-116">Valitse tämä valintaruutu varmistaaksesi, että ALV-tunnus on yksilöllinen.</span><span class="sxs-lookup"><span data-stu-id="d179d-116">Select this check box to verify if the VAT ID is unique.</span></span>  
7. <span data-ttu-id="d179d-117">Valitse Ensisijainen maalle -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="d179d-117">Select Yes in the Primary for country field.</span></span>
    * <span data-ttu-id="d179d-118">Valitse tämä valintaruutu, jos ALV-tunnus on voimassa kaikille osoitteille, jotka kuuluvat määritettyyn maahan/alueeseen.</span><span class="sxs-lookup"><span data-stu-id="d179d-118">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
8. <span data-ttu-id="d179d-119">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="d179d-119">Click Create.</span></span>
9. <span data-ttu-id="d179d-120">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="d179d-120">Click Add.</span></span>
10. <span data-ttu-id="d179d-121">Syötä tai valitse arvoksi ITA Maa/alue-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d179d-121">In the Country/region field, enter or select a value ITA</span></span>
11. <span data-ttu-id="d179d-122">Kirjoita Muoto-kenttään "###########".</span><span class="sxs-lookup"><span data-stu-id="d179d-122">In the Format field, type '###########'.</span></span>
    * <span data-ttu-id="d179d-123">Kun annat tämäntyyppisen rekisteröintitunnuksen valitulle maalle/alueelle, rekisteröintitunnusta verrataan tähän muotoon.</span><span class="sxs-lookup"><span data-stu-id="d179d-123">When you enter a registration ID of this type for the selected country/region, the registration ID will be verified against this format.</span></span>  
12. <span data-ttu-id="d179d-124">Valitse Yksilöllinen-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="d179d-124">Select the Unique check box.</span></span>
    * <span data-ttu-id="d179d-125">Valitse tämä valintaruutu varmistaaksesi, että ALV-tunnus on yksilöllinen.</span><span class="sxs-lookup"><span data-stu-id="d179d-125">Select this check box to verify if the VAT ID is unique.</span></span>  
13. <span data-ttu-id="d179d-126">Valitse Ensisijainen maalle -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="d179d-126">Select the Primary for country check box.</span></span>
    * <span data-ttu-id="d179d-127">Valitse tämä valintaruutu, jos ALV-tunnus on voimassa kaikille osoitteille, jotka kuuluvat määritettyyn maahan/alueeseen.</span><span class="sxs-lookup"><span data-stu-id="d179d-127">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
14. <span data-ttu-id="d179d-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d179d-128">Click Save.</span></span>
15. <span data-ttu-id="d179d-129">Valitse Organisaation hallinto > Yleinen osoitekirja > Rekisteröintityypit > Rekisteröintiluokat.</span><span class="sxs-lookup"><span data-stu-id="d179d-129">Go to Organization administration > Global address book > Registration types > Registration categories.</span></span>
16. <span data-ttu-id="d179d-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d179d-130">Click New.</span></span>
17. <span data-ttu-id="d179d-131">Syötä tai valitse arvoksi "ALV-tunnus, DEU" Maa/alue-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d179d-131">In the Country/region field, enter or select a value VAT ID, DEU</span></span>
18. <span data-ttu-id="d179d-132">Valitse Rekisteröintiluokka-kentän arvoksi "ALV-tunnus".</span><span class="sxs-lookup"><span data-stu-id="d179d-132">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="d179d-133">Määritä aiemmin luomasi rekisteröintityyppi esimääritettyyn rekisteröintiluokkaan.</span><span class="sxs-lookup"><span data-stu-id="d179d-133">Assign the registration type that you created earlier to a predefined Registration category.</span></span>  
19. <span data-ttu-id="d179d-134">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d179d-134">Click New.</span></span>
20. <span data-ttu-id="d179d-135">Syötä tai valitse arvoksi "ALV-tunnus, ITA" Maa/alue-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d179d-135">In the Country/region field, enter or select a value VAT ID, ITA</span></span>
21. <span data-ttu-id="d179d-136">Valitse Rekisteröintiluokka-kentän arvoksi "ALV-tunnus".</span><span class="sxs-lookup"><span data-stu-id="d179d-136">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="d179d-137">Määritä luomasi rekisteröintityyppi esimääritettyyn rekisteröintiluokkaan.</span><span class="sxs-lookup"><span data-stu-id="d179d-137">Assign the registration type that you created to a predefined registration category.</span></span>  
22. <span data-ttu-id="d179d-138">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d179d-138">Click Save.</span></span>


