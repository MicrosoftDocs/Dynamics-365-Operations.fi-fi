---
title: Luo ostosopimus
description: Tämä ohjeaihe opastaa luomaan ostosopimuksen.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1edfd4e56910376d0596eec5eff2af888f7dc98d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207735"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="10214-103">Luo ostosopimus</span><span class="sxs-lookup"><span data-stu-id="10214-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="10214-104">Tämä ohjeaihe opastaa luomaan ostosopimuksen.</span><span class="sxs-lookup"><span data-stu-id="10214-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="10214-105">Se on yleensä ostopäällikön tehtävä.</span><span class="sxs-lookup"><span data-stu-id="10214-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="10214-106">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="10214-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="10214-107">Ennen aloittamista on määritettävä ostosopimusluokitukset.</span><span class="sxs-lookup"><span data-stu-id="10214-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="10214-108">Kun olet luonut sopimuksen, voit luoda sen avulla ostotilauksen, jolloin ostotilauksen ehdot kopioituvat otsikkoon ja niille tilauksen riveille, joihin sopimus vaikuttaa.</span><span class="sxs-lookup"><span data-stu-id="10214-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="10214-109">Luo uusi ostosopimus</span><span class="sxs-lookup"><span data-stu-id="10214-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="10214-110">Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Ostosopimukset > Ostosopimukset**.</span><span class="sxs-lookup"><span data-stu-id="10214-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="10214-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="10214-111">Click **New**.</span></span>
3. <span data-ttu-id="10214-112">Valitse uuden rivin **Toimittajan tili**-kentästä haluamasi tietue avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="10214-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="10214-113">Valitse uuden rivin **Ostosopimuksen luokitus**-kentästä haluamasi tietue avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="10214-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="10214-114">Laajenna **Yleinen**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="10214-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="10214-115">Kirjoita päivämäärä **Vanhentumispäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="10214-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="10214-116">Tämä vanhentumispäivä on kaikkien sitoutumisrivien oletusarvo ja määrittää, miten kauan kukin sitoutuminen on voimassa.</span><span class="sxs-lookup"><span data-stu-id="10214-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="10214-117">Kirjoita **Asiakirjan nimi** -kenttään ostosopimuksen nimi.</span><span class="sxs-lookup"><span data-stu-id="10214-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="10214-118">Jätä **Oletussitoumus** -kentän arvoksi **Tuotteen määrän vahvistus** (tai vaihda tarvittaessa tähän arvoon).</span><span class="sxs-lookup"><span data-stu-id="10214-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="10214-119">Sitoutumisen oletusavo määrittää sopimusrivien vaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="10214-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="10214-120">Jos tarvitset sopimuksen rivejä luodessasi uuden sitoutumistyypin, sinun on muutettava otsikon oletussitoutumista.</span><span class="sxs-lookup"><span data-stu-id="10214-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="10214-121">Sitoutumistyyppejä on 4: **Tuotteen määrän vahvistus** – koskee tiettyä tuotemäärää. **Tuotteen arvon vahvistus** – koskee tuotteen tiettyä valuuttasumma. **Tuoteluokan arvon sitoutuminen** – koskee tiettyä hankintaluokan valuuttasummaa, jossa summa voi olla luettelonimike tai ei-luettelonimike. **Arvon sitoutuminen** – koskee tiettyä valuuttasumma, jonka voi täyttää mikä tahansa tuote tai hankintaluokka.</span><span class="sxs-lookup"><span data-stu-id="10214-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="10214-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="10214-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="10214-123">Lisää sitoutuminen</span><span class="sxs-lookup"><span data-stu-id="10214-123">Add a commitment</span></span>
1. <span data-ttu-id="10214-124">Valitse **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="10214-124">Select **Add line**.</span></span>
2. <span data-ttu-id="10214-125">Valitse **Nimiketunnus**-kentässä avattavasta valikosta haluttu tietue.</span><span class="sxs-lookup"><span data-stu-id="10214-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="10214-126">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="10214-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="10214-127">Kokonaismäärä, jonka olet sopinut ostavasi toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="10214-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="10214-128">Syötä **Yksikköhinta**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="10214-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="10214-129">Laajenna **Rivin erittely** -osa.</span><span class="sxs-lookup"><span data-stu-id="10214-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="10214-130">Valitse **Maksimi pakotetaan** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="10214-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="10214-131">**Maksimi pakotetaan** -vaihtoehto rajoittaa sitoutumisen käyttöä.</span><span class="sxs-lookup"><span data-stu-id="10214-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="10214-132">Voit ostaa enintään rivin **Määrä**-kentässä määritetyn määrän.</span><span class="sxs-lookup"><span data-stu-id="10214-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="10214-133">Lisää otsikkoehdot</span><span class="sxs-lookup"><span data-stu-id="10214-133">Add header conditions</span></span>
1. <span data-ttu-id="10214-134">Valitse toimintoruudussa **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="10214-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="10214-135">Valitse **Vaihda näyttö**.</span><span class="sxs-lookup"><span data-stu-id="10214-135">Select **Change view**.</span></span>
3. <span data-ttu-id="10214-136">Valitse **Otsikkonäkymä**.</span><span class="sxs-lookup"><span data-stu-id="10214-136">Select **Header view**.</span></span>
4. <span data-ttu-id="10214-137">Laajenna **Ehdot**-osa.</span><span class="sxs-lookup"><span data-stu-id="10214-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="10214-138">Valitse **Maksutapa**-kentässä avattavasta valikosta haluamasi tietue.</span><span class="sxs-lookup"><span data-stu-id="10214-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="10214-139">Toimittajatilin maksuehdot näkyvät tässä oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="10214-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="10214-140">Valitse **Toimitustapa**-kentässä avattavasta valikosta haluamasi tietue.</span><span class="sxs-lookup"><span data-stu-id="10214-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="10214-141">Avaa haku napsauttamalla **Toimitusehdot**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="10214-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="10214-142">Vahvista ja aktivoi sopimus</span><span class="sxs-lookup"><span data-stu-id="10214-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="10214-143">Valitse toimintoruudussa **Ostosopimus**.</span><span class="sxs-lookup"><span data-stu-id="10214-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="10214-144">Valitse **Vahvistus**.</span><span class="sxs-lookup"><span data-stu-id="10214-144">Select **Confirmation**.</span></span> <span data-ttu-id="10214-145">Valitse **Merkitse sopimus voimassa olevaksi** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="10214-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="10214-146">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="10214-146">Select **OK**.</span></span>
4. <span data-ttu-id="10214-147">Valitse toimintoruudussa **Ostosopimus**.</span><span class="sxs-lookup"><span data-stu-id="10214-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="10214-148">Valitse **Ostosopimuksen vahvistukset**.</span><span class="sxs-lookup"><span data-stu-id="10214-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="10214-149">**Esikatselu/tulostus**-vaihtoehdolla voi luoda ostosopimusasiakirjan, jonka voi tulostaa tai lähettää asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="10214-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="10214-150">Jos päivität sopimusta myöhemmin ja vahvistat sen uudelleen, molemmat versiot näkyvät tässä.</span><span class="sxs-lookup"><span data-stu-id="10214-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="10214-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="10214-151">Close the page.</span></span>

