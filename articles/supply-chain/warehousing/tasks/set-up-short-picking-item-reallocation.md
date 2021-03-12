---
title: Nimikkeen uudelleenkohdistussääntöjen määrittäminen lyhyttä keräilyä varten
description: Tässä aiheessa kuvataan, miten varastotyöntekijöille annetaan mahdollisuus löytää vaihtoehtoinen sijainti nopeasti, jos sijainnissa, johon heidät on ohjattu ei ole riittävää varastoa.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8baf846d65e6fefe9ca575b5af5a2dbceac666
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976885"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="8502f-103">Nimikkeen uudelleenkohdistussääntöjen määrittäminen lyhyttä keräilyä varten</span><span class="sxs-lookup"><span data-stu-id="8502f-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8502f-104">Tässä menettelyssä kuvataan, miten varastotyöntekijöille annetaan mahdollisuus löytää vaihtoehtoinen sijainti nopeasti, jos sijainnissa, johon heidät on ohjattu ei ole riittävää varastoa.</span><span class="sxs-lookup"><span data-stu-id="8502f-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="8502f-105">Uudelleenkohdistamista hallitaan **Työpoikkeuksella**, jota **Varastotyöntekijä** käyttää.</span><span class="sxs-lookup"><span data-stu-id="8502f-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="8502f-106">On mahdollista käyttää automaattista, manuaalista tai molempia uudelleenkohdistamisprosesseja:</span><span class="sxs-lookup"><span data-stu-id="8502f-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="8502f-107">Automaattinen uudelleenjako - Sijaintidirektiivien avulla määritetään, ovatko tavarat käytettävissä toisessa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="8502f-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="8502f-108">Jos mahdollista, työ päivitetään ja varaston käyttäjä ohjataan vaihtoehtoiseen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="8502f-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="8502f-109">Manuaalinen uudelleenkohdistus - Sallii varaston käyttäjän valita yhdestä tai useasta paikasta, joissa on varaukseton määrä tavaroita.</span><span class="sxs-lookup"><span data-stu-id="8502f-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="8502f-110">Automaattinen ja manuaalinen - Jos järjestelmä ei pysty suorittamaan automaattista uudelleenkohdistamista ja sijainnit ovat käytettävissä varauksettoman määrän kanssa, käyttäjää pyydetään valitsemaan sijainti.</span><span class="sxs-lookup"><span data-stu-id="8502f-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="8502f-111">Määritä työn poikkeukset</span><span class="sxs-lookup"><span data-stu-id="8502f-111">Set up work exceptions</span></span>
<span data-ttu-id="8502f-112">On mahdollista määrittää useita työn poikkeuksia, joilla on eri nimikkeen uudelleenkohdistuskäytännöt, joista varaston työntekijä voi valita käsittelyssä olevan lähetyksen tarpeisiin sopivan.</span><span class="sxs-lookup"><span data-stu-id="8502f-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="8502f-113">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="8502f-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="8502f-114">Siirry **siirtymisruudussa** kohtaan **Varastonhallinta > Asetukset > Työ-> Työn poikkeukset**.</span><span class="sxs-lookup"><span data-stu-id="8502f-114">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="8502f-115">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8502f-115">Click **New**</span></span> 
3. <span data-ttu-id="8502f-116">Kirjoita **Työn poikkeuskoodi** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="8502f-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="8502f-117">Tämä on tämän poikkeuksen otsikko.</span><span class="sxs-lookup"><span data-stu-id="8502f-117">This will be the title of this exception .</span></span> <span data-ttu-id="8502f-118">Esimerkiksi, Lyhyt keräily käsin.</span><span class="sxs-lookup"><span data-stu-id="8502f-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="8502f-119">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="8502f-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="8502f-120">Tämä on lyhyt kuvaus tämän poikkeuksen käytöstä.</span><span class="sxs-lookup"><span data-stu-id="8502f-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="8502f-121">Esimerkiksi Lyhyt poiminta -nimike ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="8502f-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="8502f-122">Valitse **Poikkeus**-tyyppi-kenttään **Lyhyt keräily**.</span><span class="sxs-lookup"><span data-stu-id="8502f-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="8502f-123">Valitse **Varaston oikaiseminen** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="8502f-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="8502f-124">Jos se valitaan, varaston arvoksi asetetaan automaattisesti 0 lyhyen keräilyn sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="8502f-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="8502f-125">Syötä tai valitse arvo **Oikaisutyypin oletuskoodi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8502f-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="8502f-126">Esimerkiksi kohteessa USMF voit valita **Poista var. muk. lähtevä**. Kukin oikaisutyyppikoodi sisältää neljä ominaisuutta: nimi, kuvaus, varastokirjauskansion nimi ja **Poista varaukset**.</span><span class="sxs-lookup"><span data-stu-id="8502f-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="8502f-127">Jos **Poista varaus** on käytössä, lyhyen poimitun tilausrivin varaukset poistetaan.</span><span class="sxs-lookup"><span data-stu-id="8502f-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="8502f-128">Valitse **Nimikkeen uudelleenkohdistus** -kentässä arvo, kuten Manuaalinen.</span><span class="sxs-lookup"><span data-stu-id="8502f-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="8502f-129">Jos valitset asetukseksi Manuaalinen tai Automaattinen ja manuaalinen, varastotyöntekijän on voitava käyttää manuaalista uudelleenkohdistusta.</span><span class="sxs-lookup"><span data-stu-id="8502f-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="8502f-130">Määritä manuaalinen nimikkeiden uudelleenkohdistus työntekijän käyttöön</span><span class="sxs-lookup"><span data-stu-id="8502f-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="8502f-131">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="8502f-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="8502f-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8502f-132">Close the page.</span></span>
2. <span data-ttu-id="8502f-133">Siirry **siirtymisruudussa** kohtaan **Varastonhallinta > Asetukset > Työntekijä**.</span><span class="sxs-lookup"><span data-stu-id="8502f-133">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="8502f-134">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="8502f-134">Click **Edit**.</span></span>
4. <span data-ttu-id="8502f-135">Valitse luettelosta työntekijä.</span><span class="sxs-lookup"><span data-stu-id="8502f-135">In the list, select worker.</span></span> <span data-ttu-id="8502f-136">Esimerkiksi Julia Funderburk.</span><span class="sxs-lookup"><span data-stu-id="8502f-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="8502f-137">Laajenna **Käyttäjät**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="8502f-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="8502f-138">Valitse luettelosta **Käyttäjätunnus**.</span><span class="sxs-lookup"><span data-stu-id="8502f-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="8502f-139">Esimerkki: 24.</span><span class="sxs-lookup"><span data-stu-id="8502f-139">For example, 24.</span></span>
7. <span data-ttu-id="8502f-140">Laajenna **Työ**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="8502f-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="8502f-141">Valitse **Salli manuaalinen nimikkeen uudelleenkohdistus** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8502f-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
