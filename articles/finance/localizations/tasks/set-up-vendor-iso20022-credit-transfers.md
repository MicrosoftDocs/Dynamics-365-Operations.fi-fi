---
title: Määritä toimittajat ja toimittajien pankkitilit ISO20022-tilisiirtoja varten
description: Tässä menettelyssä kerrotaan, miten ISO20022-pankkisiirron tai minkä tahansa muun toimittajan maksutiedoston luomisessa vaadittava toimittaja ja toimittajakohtaisen pankkitilin tiedot määritetään.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b3a16d614efed0aafbf13fc59c17ab568811d82
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222036"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="2e215-103">Määritä toimittajat ja toimittajien pankkitilit ISO20022-tilisiirtoja varten</span><span class="sxs-lookup"><span data-stu-id="2e215-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2e215-104">Tässä menettelyssä kerrotaan, miten ISO20022-pankkisiirron tai minkä tahansa muun toimittajan maksutiedoston luomisessa vaadittava toimittaja ja toimittajakohtaisen pankkitilin tiedot määritetään.</span><span class="sxs-lookup"><span data-stu-id="2e215-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="2e215-105">Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.</span><span class="sxs-lookup"><span data-stu-id="2e215-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="2e215-106">Tämä on neljäs viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="2e215-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="2e215-107">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="2e215-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="2e215-108">Pankin tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2e215-108">Set up bank details</span></span>
1. <span data-ttu-id="2e215-109">Siirry kohtaan Ostoreskontra > Toimittajat > Kaikki toimittajat.</span><span class="sxs-lookup"><span data-stu-id="2e215-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="2e215-110">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="2e215-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2e215-111">Voit esimerkiksi suodattaa Toimittajan tili -kenttää arvolla DE-001.</span><span class="sxs-lookup"><span data-stu-id="2e215-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="2e215-112">Avaa toimittajan tiedot valitsemalla DE-001.</span><span class="sxs-lookup"><span data-stu-id="2e215-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="2e215-113">Valitse toimintoruudussa Toimittaja.</span><span class="sxs-lookup"><span data-stu-id="2e215-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="2e215-114">Valitse Pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="2e215-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="2e215-115">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="2e215-115">Click Edit.</span></span>
    * <span data-ttu-id="2e215-116">Jos pankkitiliä ei ole käytettävissä, tili on luotava.</span><span class="sxs-lookup"><span data-stu-id="2e215-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="2e215-117">Syötä SWIFT-koodi-kenttään COBADEFFXXX.</span><span class="sxs-lookup"><span data-stu-id="2e215-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="2e215-118">Kirjoita IBAN-kenttään DE36200400000628808808.</span><span class="sxs-lookup"><span data-stu-id="2e215-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="2e215-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2e215-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="2e215-120">Toimittajan maksutavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2e215-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="2e215-121">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="2e215-121">Click Edit.</span></span>
2. <span data-ttu-id="2e215-122">Laajenna tai tiivistä Maksu-osa.</span><span class="sxs-lookup"><span data-stu-id="2e215-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="2e215-123">Avaa haku valitsemalla Maksutapa-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2e215-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2e215-124">Valitse luettelosta SEPA CT -rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="2e215-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="2e215-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2e215-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]