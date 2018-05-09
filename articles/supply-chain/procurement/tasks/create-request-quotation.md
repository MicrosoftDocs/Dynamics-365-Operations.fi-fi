--- 
title: "Luo tarjouspyyntö"
description: "Tässä menettelyssä näytetään, miten tarjouspyyntö luodaan."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9e7deb10cc0e5669d209ad7340108911a37bbc89
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="15818-103">Luo tarjouspyyntö</span><span class="sxs-lookup"><span data-stu-id="15818-103">Create a request for quotation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15818-104">Tässä menettelyssä näytetään, miten tarjouspyyntö luodaan.</span><span class="sxs-lookup"><span data-stu-id="15818-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="15818-105">Se on yleensä ostoedustajan tehtävä.</span><span class="sxs-lookup"><span data-stu-id="15818-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="15818-106">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="15818-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="15818-107">Ennen aloittamista on määritettävä pyyntötyypit.</span><span class="sxs-lookup"><span data-stu-id="15818-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="15818-108">Kun olet suorittanut tämän tehtävän ja luonut sekä lähettänyt tarjouspyynnön, voit sitten määrittää toimittajakohtaiset vastaukset, tehdä niistä vertailun ja myöntää sopimuksen.</span><span class="sxs-lookup"><span data-stu-id="15818-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="15818-109">Valmistele uusi tarjouspyyntö</span><span class="sxs-lookup"><span data-stu-id="15818-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="15818-110">Valitse Hankinta > Tarjouspyynnöt > Kaikki tarjouspyynnöt.</span><span class="sxs-lookup"><span data-stu-id="15818-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="15818-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="15818-111">Click New.</span></span>
    * <span data-ttu-id="15818-112">Käytettävissä ovat seuraavat ostotyypit: ostotilaus (oletusarvo): asiakirja, jolla vahvistetaan tarjous ostaa tuotteita, tai hyväksyntä tarjouksesta myydä tuotteita maksua vastaan.</span><span class="sxs-lookup"><span data-stu-id="15818-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="15818-113">Ostoehdotus: tämä tyyppi valitaan automaattisesti, jos luot tarjouspyynnön suoraan ostoehdotuksesta.</span><span class="sxs-lookup"><span data-stu-id="15818-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="15818-114">Jos valitset tämän tyypin manuaalisesti, saat virhesanoman.</span><span class="sxs-lookup"><span data-stu-id="15818-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="15818-115">Ostosopimus: sopimus tietyn tuotemäärän tai tietyn arvoisen tuotemäärän ostamiseksi toimittajalta tiettynä ajanjaksona.</span><span class="sxs-lookup"><span data-stu-id="15818-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="15818-116">Jos valitset tämän asetuksen, ostosopimusta koskeva päivämääräväli on syötettävä.</span><span class="sxs-lookup"><span data-stu-id="15818-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="15818-117">Syötä Asiakirjan otsikko -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="15818-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="15818-118">Syötä tai valitse arvo Pyyntötyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="15818-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="15818-119">Jos tulosmalli on liitetty pyyntötyyppiin, tämä on luotavan tarjouspyynnön oletusarvoinen pisteytystapa.</span><span class="sxs-lookup"><span data-stu-id="15818-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="15818-120">Pisteytystavan voi muuttaa jälkikäteen.</span><span class="sxs-lookup"><span data-stu-id="15818-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="15818-121">Kirjoita päivämäärä Toimituspäivämäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15818-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="15818-122">Valitse päivämäärä, johon mennessä haluat saada pyydetyt nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="15818-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="15818-123">Anna päivämäärä ja kellonaika Vanhentumispäivä ja -aika -kenttään.</span><span class="sxs-lookup"><span data-stu-id="15818-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="15818-124">Määritä päivämäärä ja kellonaika, johon mennessä toimittajien on vastattava tarjouspyyntöön.</span><span class="sxs-lookup"><span data-stu-id="15818-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="15818-125">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="15818-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="15818-126">Oletusarvoinen toimitusosoite on varaston osoite.</span><span class="sxs-lookup"><span data-stu-id="15818-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="15818-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="15818-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="15818-128">Lisää rivejä</span><span class="sxs-lookup"><span data-stu-id="15818-128">Add lines</span></span>
    * <span data-ttu-id="15818-129">Kun olet määrittänyt tarjouspyynnön perustiedot, määritä tavarat tai palvelut, joihin haluat saada tarjouksen toimittajilta.</span><span class="sxs-lookup"><span data-stu-id="15818-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="15818-130">Rivin oletustyyppi on nimike.</span><span class="sxs-lookup"><span data-stu-id="15818-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="15818-131">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="15818-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="15818-132">Jos käytössä on USMF, voit valita T0020.</span><span class="sxs-lookup"><span data-stu-id="15818-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="15818-133">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15818-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="15818-134">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="15818-134">Click Add line.</span></span>
4. <span data-ttu-id="15818-135">Valitse Rivin tyyppi -kenttään "Luokka".</span><span class="sxs-lookup"><span data-stu-id="15818-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="15818-136">Luokkarivin tyypin avulla voi luoda tarjouspyyntöjä muille kuin varastotuotteille tai palveluille.</span><span class="sxs-lookup"><span data-stu-id="15818-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="15818-137">Tavaran tai palvelun tyyppi on sitten valittava hankintaluokkien hierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="15818-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="15818-138">Kirjoita tai valitse arvo Hankintaluokka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15818-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="15818-139">Kirjoita arvo Tuotteen nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15818-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="15818-140">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15818-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="15818-141">Syötä tai valitse arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15818-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="15818-142">Lisää toimittajia</span><span class="sxs-lookup"><span data-stu-id="15818-142">Add vendors</span></span>
1. <span data-ttu-id="15818-143">Napsauta otsikko vaihtaaksesi rivinäkymästä otsikkonäkymään.</span><span class="sxs-lookup"><span data-stu-id="15818-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="15818-144">Laajenna Toimittaja-osa.</span><span class="sxs-lookup"><span data-stu-id="15818-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="15818-145">Napsauta kohtaa Toimittajien lisääminen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="15818-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="15818-146">Voit lisätä toimittajia tarjouspyyntöön automaattisesti hankintaluokan pyydettyjen nimikkeiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="15818-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="15818-147">Jos riveillä oleville luokille ei ole hyväksytty toimittajia, voit lisätä toimittajat manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="15818-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="15818-148">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="15818-148">Click Add.</span></span>
5. <span data-ttu-id="15818-149">Anna tai valitse arvo Toimittajatili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="15818-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="15818-150">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="15818-150">Click Add.</span></span>
7. <span data-ttu-id="15818-151">Anna tai valitse arvo Toimittajatili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="15818-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="15818-152">Kun olet valinnut toimittajan, tila on Luotu.</span><span class="sxs-lookup"><span data-stu-id="15818-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="15818-153">Tämä tarkoittaa sitä, että toimittajatiedot on tallennettu tarjouspyyntöön, mutta et ole vielä lähettänyt tarjouspyyntöä toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="15818-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="15818-154">Voit lisätä toimittajan tarjouspyyntöön toimittajan tilasta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="15818-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="15818-155">Lähetä tarjouspyyntö toimittajille</span><span class="sxs-lookup"><span data-stu-id="15818-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="15818-156">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="15818-156">Click Send.</span></span>
    * <span data-ttu-id="15818-157">Tarkista Lähetetään tarjouspyyntöä -sivulta, että luettelo sisältää ne toimittajat, jolle haluat lähettää tarjouspyynnön.</span><span class="sxs-lookup"><span data-stu-id="15818-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="15818-158">Valitse Tulosta.</span><span class="sxs-lookup"><span data-stu-id="15818-158">Click Print.</span></span>
    * <span data-ttu-id="15818-159">Tämän valintaikkunan avulla voit tulostaa tarjouspyynnön.</span><span class="sxs-lookup"><span data-stu-id="15818-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="15818-160">Voit tulostaa halutessasi vastauslomakkeen, jonka sisältö määritellään hankintaparametreissa</span><span class="sxs-lookup"><span data-stu-id="15818-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="15818-161">Voit valita vastauslomakkeiden tulostustavan, napsauttamalla Tulostuksen lisäasetuksia, kun olet avannut Tulosta-valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="15818-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="15818-162">Yksi tarjouspyyntö tulostetaan kullekin toimittajalle, joka sisältää rivit, joiden tila on Luotu tai Lähetetty.</span><span class="sxs-lookup"><span data-stu-id="15818-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="15818-163">Järjestelmä ei tulosta peruutettuja rivejä eikä rivejä, joilla on rekisteröityjä vastauksia.</span><span class="sxs-lookup"><span data-stu-id="15818-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="15818-164">Valitse Peruuta.</span><span class="sxs-lookup"><span data-stu-id="15818-164">Click Cancel.</span></span>
4. <span data-ttu-id="15818-165">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="15818-165">Click OK.</span></span>
5. <span data-ttu-id="15818-166">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15818-166">Close the page.</span></span>
6. <span data-ttu-id="15818-167">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15818-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="15818-168">Näytä tarjouspyyntöjen kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="15818-168">View the RFQ journal</span></span>
1. <span data-ttu-id="15818-169">Valitse Hankinnat > Tarjouspyynnöt > Tarjouspyynnön seuranta > Tarjouspyynnön kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="15818-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="15818-170">Napsauta Esikatselu/tulostus.</span><span class="sxs-lookup"><span data-stu-id="15818-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="15818-171">Valitse Alkuperäisen esikatselu.</span><span class="sxs-lookup"><span data-stu-id="15818-171">Click Original preview.</span></span>
4. <span data-ttu-id="15818-172">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15818-172">Close the page.</span></span>
5. <span data-ttu-id="15818-173">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15818-173">Close the page.</span></span>


