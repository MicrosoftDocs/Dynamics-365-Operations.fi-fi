---
title: Nimikkeen uudelleenkohdistussääntöjen määrittäminen lyhyttä keräilyä varten
description: Tässä menettelyssä kuvataan, miten varastotyöntekijöille annetaan mahdollisuus löytää vaihtoehtoinen sijainti nopeasti, jos sijainnissa, johon heidät on ohjattu ei ole riittävää varastoa.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf56a0811c4793ee2e3eaf78c8696c3c29e984c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "361219"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="5d999-103">Nimikkeen uudelleenkohdistussääntöjen määrittäminen lyhyttä keräilyä varten</span><span class="sxs-lookup"><span data-stu-id="5d999-103">Set up short picking item reallocation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d999-104">Tässä menettelyssä kuvataan, miten varastotyöntekijöille annetaan mahdollisuus löytää vaihtoehtoinen sijainti nopeasti, jos sijainnissa, johon heidät on ohjattu ei ole riittävää varastoa.</span><span class="sxs-lookup"><span data-stu-id="5d999-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="5d999-105">On mahdollista käyttää automaattista uudelleenkohdistusta, jossa tavarat noudetaan toisesta sijainnista, jossa ne ovat saatavilla, sijaintidirektiivien avulla.</span><span class="sxs-lookup"><span data-stu-id="5d999-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="5d999-106">Vaihtoehtona, jos käytössä on manuaalinen uudelleenkohdistus, mobiililaitteella voidaan näyttää luettelo sijainneista, joissa tarvittu määrä on saatavilla, jolloin varastotyöntekijä voi valita käytettävän sijainnin.</span><span class="sxs-lookup"><span data-stu-id="5d999-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="5d999-107">Voit käyttää tätä menettelyä esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="5d999-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="5d999-108">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="5d999-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="5d999-109">Määritä työn poikkeukset</span><span class="sxs-lookup"><span data-stu-id="5d999-109">Set up work exceptions</span></span>
1. <span data-ttu-id="5d999-110">Siirry kohtaan Varastonhallinta > Asetukset > Työ > Työn poikkeukset.</span><span class="sxs-lookup"><span data-stu-id="5d999-110">Go to Warehouse management > Setup > Work > Work exceptions.</span></span>
2. <span data-ttu-id="5d999-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5d999-111">Click New.</span></span>
    * <span data-ttu-id="5d999-112">On mahdollista määrittää useita työn poikkeuksia, joilla on eri nimikkeen uudelleenkohdistuskäytännöt, joista varaston työntekijä voi valita käsittelyssä olevan lähetyksen tarpeisiin sopivan.</span><span class="sxs-lookup"><span data-stu-id="5d999-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="5d999-113">Kirjoita Työn poikkeuskoodi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="5d999-113">In the Work exception code field, type a value.</span></span>
    * <span data-ttu-id="5d999-114">Anna työn poikkeukselle nimi, joka ilmaisee, mitä varten se on.</span><span class="sxs-lookup"><span data-stu-id="5d999-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="5d999-115">Esimerkiksi, Lyhyt keräily käsin.</span><span class="sxs-lookup"><span data-stu-id="5d999-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="5d999-116">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5d999-116">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5d999-117">Valitse Poikkeustyyppi-kenttään "Lyhyt keräily".</span><span class="sxs-lookup"><span data-stu-id="5d999-117">In the Exception type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="5d999-118">Valitse Varaston oikaiseminen -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="5d999-118">Select the Adjust inventory check box.</span></span>
    * <span data-ttu-id="5d999-119">Tämä vaihtoehto tarkoittaa, että varaston arvoksi asetetaan automaattisesti 0 lyhyen keräilyn sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="5d999-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="5d999-120">Syötä tai valitse arvo Oikaisutyypin oletuskoodi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="5d999-120">In the Default adjustment type code field, enter or select a value.</span></span>
    * <span data-ttu-id="5d999-121">Esimerkiksi USMF-yrityksessä voit valita "Poista Res Adj Out".</span><span class="sxs-lookup"><span data-stu-id="5d999-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="5d999-122">Valitse Nimikkeen uudelleenkohdistus -kentässä Manuaalinen.</span><span class="sxs-lookup"><span data-stu-id="5d999-122">In the Item reallocation field, select 'Manual'.</span></span>
    * <span data-ttu-id="5d999-123">Jos valitset asetukseksi Manuaalinen tai Automaattinen ja manuaalinen, varastotyöntekijän on voitava käyttää manuaalista uudelleenkohdistusta.</span><span class="sxs-lookup"><span data-stu-id="5d999-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="5d999-124">Määritä manuaalinen nimikkeiden uudelleenkohdistus työntekijän käyttöön</span><span class="sxs-lookup"><span data-stu-id="5d999-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="5d999-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5d999-125">Close the page.</span></span>
2. <span data-ttu-id="5d999-126">Siirry kohtaan Varastonhallinta > Asetukset > Työntekijä.</span><span class="sxs-lookup"><span data-stu-id="5d999-126">Go to Warehouse management > Setup > Worker.</span></span>
3. <span data-ttu-id="5d999-127">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="5d999-127">Click Edit.</span></span>
4. <span data-ttu-id="5d999-128">Valitse luettelosta työntekijä 24.</span><span class="sxs-lookup"><span data-stu-id="5d999-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="5d999-129">Laajenna Työ-osa.</span><span class="sxs-lookup"><span data-stu-id="5d999-129">Expand the Work section.</span></span>
6. <span data-ttu-id="5d999-130">Valitse Salli manuaalinen nimikkeen uudelleenkohdistus -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="5d999-130">Select Yes in the Allow manual item reallocation field.</span></span>

