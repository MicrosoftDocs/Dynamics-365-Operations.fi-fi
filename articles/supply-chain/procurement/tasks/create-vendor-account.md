--- 
title: Toimittajatilin luominen
description: "Tässä menetelmässä selvitetään toimittajatili luominen sekä lisätään osoite- ja yhteystiedot."
author: mkirknel
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6ff2357d5266c45be2f403e463c72089d73db21b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-vendor-account"></a><span data-ttu-id="1b2bb-103">Toimittajatilin luominen</span><span class="sxs-lookup"><span data-stu-id="1b2bb-103">Create a vendor account</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1b2bb-104">Tässä menetelmässä selvitetään toimittajatili luominen sekä lisätään osoite- ja yhteystiedot.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="1b2bb-105">Menettelyssä ei näytetä miten kaikki osto- ja rahoitustarkoitusten kentät täytetään.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="1b2bb-106">Kenttien kuvauksissa on lisätietoja kyseistä kentistä.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="1b2bb-107">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="1b2bb-108">Yleensä hankinta-asiantuntija tai myyntireskontran henkilökunta luo toimittajatilit.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="1b2bb-109">Toimittajatilin luominen</span><span class="sxs-lookup"><span data-stu-id="1b2bb-109">Create a vendor account</span></span>
1. <span data-ttu-id="1b2bb-110">Valitse Hankinta > Toimittajat > Kaikki toimittajat.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-110">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="1b2bb-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-111">Click New.</span></span>
3. <span data-ttu-id="1b2bb-112">Kirjoita arvo Toimittajan tili -kenttään.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-112">In the Vendor account field, type a value.</span></span>
    * <span data-ttu-id="1b2bb-113">Arvo voidaan lisätä automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-113">The value may be populated automatically.</span></span> <span data-ttu-id="1b2bb-114">Siinä tapauksessa voit ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-114">If so, you can skip this step.</span></span>  
    * <span data-ttu-id="1b2bb-115">Toimittajatilin voi luoda henkilölle tai organisaatiolle.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="1b2bb-116">Käytettävissä olevat kentät määräytyvät tämän mukaan.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-116">This will affect which fields are available.</span></span> <span data-ttu-id="1b2bb-117">Tässä esimerkissä luodaan organisaation toimittajatili.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-117">In this example, we’ll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="1b2bb-118">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-118">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="1b2bb-119">Jos toimittaja jo rekisteröity osapuoleksi järjestelmään, voit valita toimittajan tässä kentässä vetämällä ja pudottamalla, jolloin uusi toimittajatili perii jo rekisteröidyn osoitteen ja yhteystiedot.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that’s already registered.</span></span>  
5. <span data-ttu-id="1b2bb-120">Syötä tai valitse Ryhmä-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-120">In the Group field, enter or select a value.</span></span>
    * <span data-ttu-id="1b2bb-121">Toimittajaryhmän avulla ryhmitetään toimittajat, joille jokin seuraavista parametreista on yhteinen: maksuehdot, selvityskausi, varastokirjauksen kirjanpitotilit – mukaan lukien arvonlisäveroryhmä, oletuskirjanpitotilit, tuotteen suodatinkoodit ja tarjontaennustemääritys.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment , settle period,  inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>  
6. <span data-ttu-id="1b2bb-122">Täytä Työntekijämäärä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-122">In the Number of employees field, enter a number.</span></span>
7. <span data-ttu-id="1b2bb-123">Kirjoita Organisaatiotunnus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-123">In the Organization number field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="1b2bb-124">Lisää osoite</span><span class="sxs-lookup"><span data-stu-id="1b2bb-124">Add an address</span></span>
1. <span data-ttu-id="1b2bb-125">Laajenna osa Osoitteet.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-125">Expand the Addresses section.</span></span>
2. <span data-ttu-id="1b2bb-126">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-126">Click Add.</span></span>
3. <span data-ttu-id="1b2bb-127">Syötä tai valitse Tarkoitus-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-127">In the Purpose field, enter or select a value.</span></span>
    * <span data-ttu-id="1b2bb-128">Voit valita useita tarkoituksia.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-128">You can select one or more purposes.</span></span> <span data-ttu-id="1b2bb-129">Näiden avulla voit valita tietylle tarkoitukselle oikean osoitteen.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="1b2bb-130">Esimerkiksi jos tarkoitus on "lasku", tätä osoitetta käytetään lähetettävissä laskuissa.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-130">For example, if the purpose is “Invoice” that address will be used when you send invoices.</span></span>  
4. <span data-ttu-id="1b2bb-131">Kirjoita Nimi tai kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-131">In the Name or description field, type a value.</span></span>
5. <span data-ttu-id="1b2bb-132">Syötä tai valitse arvo Maa/alue-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-132">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="1b2bb-133">Anna osoitetiedot.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-133">Enter the address details.</span></span> <span data-ttu-id="1b2bb-134">Valitsemasi maa tai alue määrittää näkyviin tulevat kentät, sillä ne vastaavat kyseisen maan tai alueen osoitemuotoa.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span>   
6. <span data-ttu-id="1b2bb-135">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-135">Click OK.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="1b2bb-136">Lisää yhteystiedot</span><span class="sxs-lookup"><span data-stu-id="1b2bb-136">Add contact information</span></span>
1. <span data-ttu-id="1b2bb-137">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-137">Click Add.</span></span>
2. <span data-ttu-id="1b2bb-138">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-138">In the Description field, type a value.</span></span>
3. <span data-ttu-id="1b2bb-139">Valitse vaihtoehto Tyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-139">In the Type field, select an option.</span></span>
4. <span data-ttu-id="1b2bb-140">Kirjoita arvo Yhteyshenkilön puhelinnumero/osoite -kenttään.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-140">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="1b2bb-141">Valitse Ensisijainen-valintaruutu, jos tämä on yhteyshenkilön ensisijainen osoite.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-141">You can select the Primary check box if this is the primary contact.</span></span>  
5. <span data-ttu-id="1b2bb-142">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-142">Click Save.</span></span>
6. <span data-ttu-id="1b2bb-143">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-143">Close the page.</span></span>
7. <span data-ttu-id="1b2bb-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1b2bb-144">Close the page.</span></span>


