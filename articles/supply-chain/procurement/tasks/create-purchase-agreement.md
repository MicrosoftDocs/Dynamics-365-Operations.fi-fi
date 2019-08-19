---
title: Luo ostosopimus
description: Tämä menettely opastaa luomaan ostosopimuksen.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df74eaad51fc4ef28caf96e4bcdc7b03f7e6ec3b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836355"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="2832a-103">Luo ostosopimus</span><span class="sxs-lookup"><span data-stu-id="2832a-103">Create a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2832a-104">Tämä menettely opastaa luomaan ostosopimuksen.</span><span class="sxs-lookup"><span data-stu-id="2832a-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="2832a-105">Se on yleensä ostopäällikön tehtävä.</span><span class="sxs-lookup"><span data-stu-id="2832a-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="2832a-106">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="2832a-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="2832a-107">Ennen aloittamista on määritettävä ostosopimusluokitukset.</span><span class="sxs-lookup"><span data-stu-id="2832a-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="2832a-108">Kun olet luonut sopimuksen, voit luoda sen avulla ostotilauksen, jolloin ostotilauksen ehdot kopioituvat otsikkoon ja niille tilauksen riveille, joihin sopimus vaikuttaa.</span><span class="sxs-lookup"><span data-stu-id="2832a-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="2832a-109">Luo uusi ostosopimus</span><span class="sxs-lookup"><span data-stu-id="2832a-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="2832a-110">Valitse Hankinta > Ostosopimukset > Ostosopimukset.</span><span class="sxs-lookup"><span data-stu-id="2832a-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="2832a-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2832a-111">Click New.</span></span>
3. <span data-ttu-id="2832a-112">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2832a-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2832a-113">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2832a-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2832a-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2832a-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2832a-115">Avaa haku napsauttamalla Ostosopimuksen luokitus -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="2832a-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2832a-116">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2832a-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="2832a-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2832a-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2832a-118">Laajenna Yleiset-osa.</span><span class="sxs-lookup"><span data-stu-id="2832a-118">Expand the General section.</span></span>
10. <span data-ttu-id="2832a-119">Kirjoita päivämäärä Vanhentumispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2832a-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="2832a-120">Tämä vanhentumispäivä on kaikkien sitoutumisrivien oletusarvo ja määrittää, miten kauan kukin sitoutuminen on voimassa.</span><span class="sxs-lookup"><span data-stu-id="2832a-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="2832a-121">Kirjoita Asiakirjan nimi -kenttään ostosopimuksen nimi.</span><span class="sxs-lookup"><span data-stu-id="2832a-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="2832a-122">Jätä Oletussitoumus -kentän arvoksi Tuotteen määrän vahvistus (tai vaihda tarvittaessa tähän arvoon).</span><span class="sxs-lookup"><span data-stu-id="2832a-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="2832a-123">Sitoutumisen oletusavo määrittää sopimusrivien vaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="2832a-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="2832a-124">Jos tarvitset sopimuksen rivejä luodessasi uuden sitoutumistyypin, sinun on muutettava otsikon oletussitoutumista.</span><span class="sxs-lookup"><span data-stu-id="2832a-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="2832a-125">Sitoutumistyyppejä on 4: Tuotteen määrän vahvistus – koskee tiettyä tuotemäärää. Tuotteen arvon vahvistus – koskee tuotteen tiettyä valuuttasumma. Tuoteluokan arvon sitoutuminen – koskee tiettyä hankintaluokan valuuttasummaa, jossa summa voi olla luettelonimike tai ei-luettelonimike. Arvon sitoutuminen – koskee tiettyä valuuttasumma, jonka voi täyttää mikä tahansa tuote tai hankintaluokka.</span><span class="sxs-lookup"><span data-stu-id="2832a-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="2832a-126">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2832a-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="2832a-127">Lisää sitoutuminen</span><span class="sxs-lookup"><span data-stu-id="2832a-127">Add a commitment</span></span>
1. <span data-ttu-id="2832a-128">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="2832a-128">Click Add line.</span></span>
2. <span data-ttu-id="2832a-129">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2832a-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="2832a-130">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2832a-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2832a-131">Valitse tuote,johon haluat lisätä sitoutumisen.</span><span class="sxs-lookup"><span data-stu-id="2832a-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="2832a-132">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2832a-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2832a-133">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2832a-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2832a-134">Kokonaismäärä, jonka olet sopinut ostavasi toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="2832a-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="2832a-135">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="2832a-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="2832a-136">Laajenna Rivin erittely -osa.</span><span class="sxs-lookup"><span data-stu-id="2832a-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="2832a-137">Valitse Maksimi pakotetaan -asetukseksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2832a-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="2832a-138">Maksimi pakotetaan -vaihtoehto rajoittaa sitoutumisen käyttöä.</span><span class="sxs-lookup"><span data-stu-id="2832a-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="2832a-139">Voit ostaa enintään rivin Määrä-kentässä määritetyn määrän.</span><span class="sxs-lookup"><span data-stu-id="2832a-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="2832a-140">Tiivistä Rivitiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="2832a-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="2832a-141">Lisää otsikkoehdot</span><span class="sxs-lookup"><span data-stu-id="2832a-141">Add header conditions</span></span>
1. <span data-ttu-id="2832a-142">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="2832a-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="2832a-143">Valitse Vaihda näkymä.</span><span class="sxs-lookup"><span data-stu-id="2832a-143">Click Change view.</span></span>
3. <span data-ttu-id="2832a-144">Valitse Otsikkonäkymä.</span><span class="sxs-lookup"><span data-stu-id="2832a-144">Click Header view.</span></span>
4. <span data-ttu-id="2832a-145">Laajenna Ehdot-osa.</span><span class="sxs-lookup"><span data-stu-id="2832a-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="2832a-146">Avaa haku valitsemalla Maksutapa-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2832a-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2832a-147">Toimittajatilin maksuehdot näkyvät tässä oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="2832a-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="2832a-148">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2832a-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2832a-149">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2832a-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2832a-150">Avaa haku napsauttamalla Toimitustapa-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="2832a-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="2832a-151">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2832a-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="2832a-152">Avaa haku napsauttamalla Toimitusehdot-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="2832a-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2832a-153">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2832a-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="2832a-154">Vahvista ja aktivoi sopimus</span><span class="sxs-lookup"><span data-stu-id="2832a-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="2832a-155">Valitse toimintoruudussa Ostosopimus.</span><span class="sxs-lookup"><span data-stu-id="2832a-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="2832a-156">Valitse Vahvistus.</span><span class="sxs-lookup"><span data-stu-id="2832a-156">Click Confirmation.</span></span>
    * <span data-ttu-id="2832a-157">Valitse Merkitse sopimus voimassa olevaksi -asetukseksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2832a-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="2832a-158">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2832a-158">Click OK.</span></span>
4. <span data-ttu-id="2832a-159">Valitse toimintoruudussa Ostosopimus.</span><span class="sxs-lookup"><span data-stu-id="2832a-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="2832a-160">Valitse Ostosopimuksen vahvistukset.</span><span class="sxs-lookup"><span data-stu-id="2832a-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="2832a-161">Esikatselu/tulostus-vaihtoehdolla voi luoda ostosopimusasiakirjan, jonka voi tulostaa tai lähettää asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="2832a-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="2832a-162">Jos päivität sopimusta myöhemmin ja vahvistat sen uudelleen, molemmat versiot näkyvät tässä.</span><span class="sxs-lookup"><span data-stu-id="2832a-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="2832a-163">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2832a-163">Close the page.</span></span>

