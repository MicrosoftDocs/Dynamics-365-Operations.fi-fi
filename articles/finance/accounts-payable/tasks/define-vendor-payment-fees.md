---
title: Määritä toimittajan maksulisät
description: Määritä toimittajan toimitusmaksut.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e9e723ec54b6f34082c422ce4c8e48bf52d2e3e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189450"
---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="d3118-103">Määritä toimittajan maksulisät</span><span class="sxs-lookup"><span data-stu-id="d3118-103">Define vendor payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3118-104">Määritä toimittajan toimitusmaksut.</span><span class="sxs-lookup"><span data-stu-id="d3118-104">Set up vendor payment fees.</span></span> <span data-ttu-id="d3118-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="d3118-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="d3118-106">Siirry kohtaan Ostoreskontra > Maksun asetukset > Toimitusmaksu.</span><span class="sxs-lookup"><span data-stu-id="d3118-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="d3118-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d3118-107">Click New.</span></span>
3. <span data-ttu-id="d3118-108">Kirjoita arvo Lisämaksun tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="d3118-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="d3118-109">Lisämaksun tunnukseksi kannattaa valita lisämaksun käyttötarkoitusta kuvaava tunnus, kuten Sähköisen rahansiirron lisämaksu.</span><span class="sxs-lookup"><span data-stu-id="d3118-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="d3118-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d3118-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d3118-111">Kirjoita arvo Lisämaksun kuvaus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="d3118-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="d3118-112">Määritä lisätietoja lisämaksun käyttämisestä lisäämällä kuvaus.</span><span class="sxs-lookup"><span data-stu-id="d3118-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="d3118-113">Valitse Veloitus-kentässä Toimittaja tai Kirjanpito.</span><span class="sxs-lookup"><span data-stu-id="d3118-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="d3118-114">Kirjanpitoa käytetään, kun lisämaksu veloitetaan organisaatiolta.</span><span class="sxs-lookup"><span data-stu-id="d3118-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="d3118-115">Toimittajaa käytetään, kun lisämaksu määritetään toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="d3118-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="d3118-116">Syötä päätili, jolta lisämaksu veloitetaan.</span><span class="sxs-lookup"><span data-stu-id="d3118-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="d3118-117">Tämä vaihtoehto on käytettävissä vain, kun Veloitus-asetukseksi valitaan Kirjanpito.</span><span class="sxs-lookup"><span data-stu-id="d3118-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="d3118-118">Valitse kirjauskansio, jossa tätä lisämaksua voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="d3118-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="d3118-119">Valitse toimittajan toimitusmaksuksi Toimittajan suoritus -kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="d3118-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="d3118-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d3118-120">Click Save.</span></span>
10. <span data-ttu-id="d3118-121">Valitse Toimittajan toimitusmaksun asetukset.</span><span class="sxs-lookup"><span data-stu-id="d3118-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="d3118-122">Jatka toimitusmaksun asetuksiin ja määritä, milloin lisämaksu on valitsemasi kirjauskansion oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="d3118-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="d3118-123">Valitse Taulu, Ryhmä tai Kaikki.</span><span class="sxs-lookup"><span data-stu-id="d3118-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="d3118-124">Määritä arvoksi Taulu, kun valitset yksittäisen pankkitilin. Valitse Ryhmä, kun valitset pankkiryhmän ja Kaikki, kun näitä lisämaksun asetuksia käytetään kaikissa pankkitileissä.</span><span class="sxs-lookup"><span data-stu-id="d3118-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="d3118-125">Valitse pankkiryhmä tai pankkitili.</span><span class="sxs-lookup"><span data-stu-id="d3118-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="d3118-126">Haussa näkyy pankkiryhmä, jos valittuna on Ryhmä, ja pankkitilit, jos valittuna on Taulu.</span><span class="sxs-lookup"><span data-stu-id="d3118-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="d3118-127">Valitse maksutapa, jossa tätä lisämaksua käytetään.</span><span class="sxs-lookup"><span data-stu-id="d3118-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="d3118-128">Valitse valitun maksutavan maksumääritys.</span><span class="sxs-lookup"><span data-stu-id="d3118-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="d3118-129">Maksumäärittelyä käytetään sähköisen rahansiirron maksutavoissa.</span><span class="sxs-lookup"><span data-stu-id="d3118-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="d3118-130">Määritä, onko lisämaksu prosentti, summa vai väli.</span><span class="sxs-lookup"><span data-stu-id="d3118-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="d3118-131">Syötä lisämaksun prosentti tai summa.</span><span class="sxs-lookup"><span data-stu-id="d3118-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="d3118-132">Jos Lisämaksu-kohtaan on valittu Prosentti, syötä prosenttiluku.</span><span class="sxs-lookup"><span data-stu-id="d3118-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="d3118-133">Jos Lisämaksu-kohtaan on valittu Summa, syötä lisämaksun summa.</span><span class="sxs-lookup"><span data-stu-id="d3118-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="d3118-134">Jos Lisämaksu-kohtaan on valittu Väli, syötä lisämaksujen tasot Väli-välilehden avulla.</span><span class="sxs-lookup"><span data-stu-id="d3118-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="d3118-135">Valitse Lisämaksun valuutta -kentässä valuutta, jossa lisämaksu käsitellään.</span><span class="sxs-lookup"><span data-stu-id="d3118-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="d3118-136">Tämä valuutta koskee lisämaksua.</span><span class="sxs-lookup"><span data-stu-id="d3118-136">This currency is for the fee.</span></span> <span data-ttu-id="d3118-137">Maksun valuutan avulla määritetään, milloin lisämaksun sääntöä käytetään maksun valuutan perusteella.</span><span class="sxs-lookup"><span data-stu-id="d3118-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="d3118-138">Pankki saattaa veloittaa lisämaksun esimerkiksi silloin, kun maksu suoritetaan euroina. Muista maksuista ei tässä tapauksessa veloiteta lisämaksua.</span><span class="sxs-lookup"><span data-stu-id="d3118-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="d3118-139">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d3118-139">Click Save.</span></span>
