---
title: Rekisteröi nimikkeet erikoisvarastointikäyttöön tarkoitetuksi nimikkeiksi käyttäen nimikkeen saapumisen kirjauskansiota
description: Tässä menettelyssä käsitellään, miten nimikkeet rekisteröidään käyttämällä nimikkeen saapumisen kirjauskansiota, kun käytössä on varastonhallinnan lisäprosessit.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 392884d2a87c10a5f38bf6f51967f879c68c1ca6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558077"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="eb990-103">Rekisteröi nimikkeet erikoisvarastointikäyttöön tarkoitetuksi nimikkeiksi käyttäen nimikkeen saapumisen kirjauskansiota</span><span class="sxs-lookup"><span data-stu-id="eb990-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb990-104">Tässä menettelyssä käsitellään, miten nimikkeet rekisteröidään käyttämällä nimikkeen saapumisen kirjauskansiota, kun käytössä on varastonhallinnan lisäprosessit.</span><span class="sxs-lookup"><span data-stu-id="eb990-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="eb990-105">Vastaanottoassistentti tekee yleensä tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="eb990-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="eb990-106">Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omia tietoja.</span><span class="sxs-lookup"><span data-stu-id="eb990-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="eb990-107">Sinun on vahvistettava ostotilaus, jossa on avoin ostotilausrivi, ennen tämän opastuksen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="eb990-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="eb990-108">Rivin nimikkeen on oltava varastoitu, eikä se saa käyttää tuotevariantteja. Seurantadimensiot eivät myöskään saa olla käytössä.</span><span class="sxs-lookup"><span data-stu-id="eb990-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="eb990-109">Nimike on myös liitettävä varastodimensioryhmään, jossa varastonhallintaprosessi on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="eb990-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="eb990-110">Varastonhallintaprosessit on oltava otettuna käyttöön käytettävässä varastossa ja vastaanottoa on ohjattava käytettävässä toimipaikassa rekisterikilvillä.</span><span class="sxs-lookup"><span data-stu-id="eb990-110">The warehouse that’s used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="eb990-111">Jos käytössä on USMF, voit käyttää ostotilauksen luontiin yritystiliä 1001, varastoa 51 ja nimikettä M9200.</span><span class="sxs-lookup"><span data-stu-id="eb990-111">If you’re using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="eb990-112">Kirjoita muistiin luomasi ostotilauksen numero sekä ostotilausrivillä käytetty nimiketunnus ja toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="eb990-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="eb990-113">Luo nimikkeen saapumisen kirjauskansion otsikko</span><span class="sxs-lookup"><span data-stu-id="eb990-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="eb990-114">Valitse Nimikkeen saapuminen.</span><span class="sxs-lookup"><span data-stu-id="eb990-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="eb990-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="eb990-115">Click New.</span></span>
3. <span data-ttu-id="eb990-116">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="eb990-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="eb990-117">Jos käytössä on USMF, voit syöttää arvoksi WHS.</span><span class="sxs-lookup"><span data-stu-id="eb990-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="eb990-118">Jos käytät muita tietoja, kirjauskansiolla, jonka nimen valitsit, on oltava seuraavat ominaisuudet: Tarkista keräilysijainti -asetukseksi on määritettävä Ei ja Karanteeninhallinta-asetukseksi Ei.</span><span class="sxs-lookup"><span data-stu-id="eb990-118">If you’re using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="eb990-119">Kirjoita arvo Numero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="eb990-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="eb990-120">Kirjoita arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="eb990-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="eb990-121">Valitse ostotilausrivillä käyttämäsi toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="eb990-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="eb990-122">Se toimii oletusarvona, jota kaikki kirjauskansion rivit käyttävät oletuksena.</span><span class="sxs-lookup"><span data-stu-id="eb990-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="eb990-123">Valitse USMF-tiedoissa varastoa 51, valitse toimipaikka 5.</span><span class="sxs-lookup"><span data-stu-id="eb990-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="eb990-124">Kirjoita arvo Varasto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="eb990-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="eb990-125">Valitse varasto, jota voi käyttää yhdessä valitsemasi toimipaikan kanssa.</span><span class="sxs-lookup"><span data-stu-id="eb990-125">Select a valid warehouse for the site that you’ve selected.</span></span> <span data-ttu-id="eb990-126">Se toimii oletusarvona, jota kaikki kirjauskansion rivit käyttävät oletuksena.</span><span class="sxs-lookup"><span data-stu-id="eb990-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="eb990-127">Jos käytät USMF-tietojen esimerkkiarvoja, valitse 51.</span><span class="sxs-lookup"><span data-stu-id="eb990-127">If you’re using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="eb990-128">Kirjoita arvo kenttään Sijainti.</span><span class="sxs-lookup"><span data-stu-id="eb990-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="eb990-129">Valitse sijainti valitsemastasi varastosta.</span><span class="sxs-lookup"><span data-stu-id="eb990-129">Select a valid location in the warehouse that you’ve selected.</span></span> <span data-ttu-id="eb990-130">Sijainnin on liityttävä sijaintiprofiiliin, jota rekisterikilpi hallitsee.</span><span class="sxs-lookup"><span data-stu-id="eb990-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="eb990-131">Se toimii oletusarvona, jota kaikki kirjauskansion rivit käyttävät oletuksena.</span><span class="sxs-lookup"><span data-stu-id="eb990-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="eb990-132">Jos käytät USMF-tietojen esimerkkiarvoja, valitse Bulk-008.</span><span class="sxs-lookup"><span data-stu-id="eb990-132">If you’re using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="eb990-133">Napsauta Rekisterikilpi-kentässä alanuolta kakkospainikkeella ja valitse Näytä tiedot.</span><span class="sxs-lookup"><span data-stu-id="eb990-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="eb990-134">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="eb990-134">Click New.</span></span>
10. <span data-ttu-id="eb990-135">Kirjoita Rekisterikilpi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="eb990-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="eb990-136">Kirjoita arvo muistiin.</span><span class="sxs-lookup"><span data-stu-id="eb990-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="eb990-137">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="eb990-137">Click Save.</span></span>
12. <span data-ttu-id="eb990-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="eb990-138">Close the page.</span></span>
13. <span data-ttu-id="eb990-139">Kirjoita Rekisterikilpi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="eb990-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="eb990-140">Anna juuri luodun rekisterikilven arvo.</span><span class="sxs-lookup"><span data-stu-id="eb990-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="eb990-141">Se toimii oletusarvona, jota kaikki kirjauskansion rivit käyttävät oletuksena.</span><span class="sxs-lookup"><span data-stu-id="eb990-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="eb990-142">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="eb990-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="eb990-143">Lisää rivi</span><span class="sxs-lookup"><span data-stu-id="eb990-143">Add a line</span></span>
1. <span data-ttu-id="eb990-144">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="eb990-144">Click Add line.</span></span>
2. <span data-ttu-id="eb990-145">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="eb990-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="eb990-146">Anna ostotilausrivillä käyttämäsi nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="eb990-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="eb990-147">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="eb990-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="eb990-148">Anna rekisteröitävä määrä.</span><span class="sxs-lookup"><span data-stu-id="eb990-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="eb990-149">Päivämäärä-kenttä määrittää päivämäärän, jolloin tämän nimikkeen käytettävissä oleva määrä rekisteröidään varastoon.</span><span class="sxs-lookup"><span data-stu-id="eb990-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="eb990-150">Järjestelmä lisää erätunnuksen tiedot, jos erä voidaan yksilöivästi tunnistaa annetuista tiedoista.</span><span class="sxs-lookup"><span data-stu-id="eb990-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="eb990-151">Muussa tapauksessa tiedot on lisättävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="eb990-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="eb990-152">Tämä on pakollinen kenttä, joka linkittää tämän rekisteröinnin tietylle lähdeasiakirjariville.</span><span class="sxs-lookup"><span data-stu-id="eb990-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="eb990-153">Suorita rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="eb990-153">Complete the registration</span></span>
1. <span data-ttu-id="eb990-154">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="eb990-154">Click Validate.</span></span>
    * <span data-ttu-id="eb990-155">Tämä tarkistaa, että kirjauskansio on valmis kirjattavaksi.</span><span class="sxs-lookup"><span data-stu-id="eb990-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="eb990-156">Jos vahvistus epäonnistuu, virheet on korjattava ennen kirjausta kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="eb990-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="eb990-157">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="eb990-157">Click OK.</span></span>
    * <span data-ttu-id="eb990-158">Tarkista sanoma, kun olet valinnut OK.</span><span class="sxs-lookup"><span data-stu-id="eb990-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="eb990-159">Kyseisen sanoman pitäisi ilmoittaa, että kirjauskansio on OK.</span><span class="sxs-lookup"><span data-stu-id="eb990-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="eb990-160">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="eb990-160">Click Post.</span></span>
4. <span data-ttu-id="eb990-161">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="eb990-161">Click OK.</span></span>
    * <span data-ttu-id="eb990-162">Tarkista sanomarivi, kun olet valinnut OK.</span><span class="sxs-lookup"><span data-stu-id="eb990-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="eb990-163">Sanoman pitäisi ilmoittaa, että toiminto onnistui.</span><span class="sxs-lookup"><span data-stu-id="eb990-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="eb990-164">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="eb990-164">Close the page.</span></span>

