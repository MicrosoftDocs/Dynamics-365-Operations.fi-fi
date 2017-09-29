--- 
title: "Rekisteröi nimikkeet perusvarastointikäyttöön tarkoitetuksi nimikkeiksi käyttäen nimikkeen saapumisen kirjauskansiota"
description: "Tässä menettelyssä kerrotaan, miten nimikkeet rekisteröidään käyttämällä nimikkeen saapumisen kirjauskansiota, kun käytössä on varastonhallintamoduulin perusvarastointi."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a5fa86bace459d694ab0a2ec289e11b0e4420932
ms.openlocfilehash: 184f38347e2525f3efef9b0d55003a94a75380d4
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="00162-103">Rekisteröi nimikkeet perusvarastointikäyttöön tarkoitetuksi nimikkeiksi käyttäen nimikkeen saapumisen kirjauskansiota</span><span class="sxs-lookup"><span data-stu-id="00162-103">Register items for a basic warehousing enabled item using an item arrival journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00162-104">Tässä menettelyssä kerrotaan, miten nimikkeet rekisteröidään käyttämällä nimikkeen saapumisen kirjauskansiota, kun käytössä on varastonhallintamoduulin perusvarastointi.</span><span class="sxs-lookup"><span data-stu-id="00162-104">This procedure shows you how to register items using the item arrival journal when you are using “basic warehousing” in the Inventory management module.</span></span> <span data-ttu-id="00162-105">Vastaanottoassistentti tekee yleensä tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="00162-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="00162-106">Voit suorittaa tämän menettelyn esittelytietojen USMF-yrityksen avulla näkyvillä olevilla esimerkkiarvoilla.</span><span class="sxs-lookup"><span data-stu-id="00162-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="00162-107">Jos et käytä USMF-yritystä, sinun on vahvistettava ostotilaus ja avoimen ostotilauksen rivi, ennen kuin aloitat tämän ohjauksen suorittamisen.</span><span class="sxs-lookup"><span data-stu-id="00162-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="00162-108">Rivin nimikkeen on oltava varastoitu, eikä se saa käyttää tuotevariantteja. Seurantadimensiot eivät myöskään saa olla käytössä.</span><span class="sxs-lookup"><span data-stu-id="00162-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="00162-109">Nimike on myös liitettävä varastodimensioryhmään, jonka toimipaikka ja varasto ovat aktiivisia.</span><span class="sxs-lookup"><span data-stu-id="00162-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="00162-110">Nimikkeen saapumisen kirjauskansion otsikon luominen</span><span class="sxs-lookup"><span data-stu-id="00162-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="00162-111">Valitse Inventoinnin- ja varastonhallinta > Kirjauskansioviennit > Nimikkeen saapuminen > Nimikkeen saapuminen.</span><span class="sxs-lookup"><span data-stu-id="00162-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="00162-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="00162-112">Click New.</span></span>
3. <span data-ttu-id="00162-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="00162-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="00162-114">Jos käytössä on USMF, voit syöttää arvoksi WHS.</span><span class="sxs-lookup"><span data-stu-id="00162-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="00162-115">Jos käytät muita tietoja, kirjauskansiolla, jonka nimen valitsit, on oltava seuraavat ominaisuudet: Tarkista keräilysijainti -asetukseksi on määritettävä Ei ja Karanteeninhallinta-asetukseksi Ei.</span><span class="sxs-lookup"><span data-stu-id="00162-115">If you’re using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="00162-116">Kirjoita arvo Pakkausluettelo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="00162-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="00162-117">Tämä on toimittajan luoman pakkausluettelon tunnus.</span><span class="sxs-lookup"><span data-stu-id="00162-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="00162-118">Lisää yksilöivä numero.</span><span class="sxs-lookup"><span data-stu-id="00162-118">Add a unique number.</span></span>  
5. <span data-ttu-id="00162-119">Valitse Numero-kenttään ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="00162-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="00162-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="00162-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="00162-121">Rivien lisääminen nimikkeen saapumisen kirjauskansioon</span><span class="sxs-lookup"><span data-stu-id="00162-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="00162-122">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="00162-122">Click Functions.</span></span>
2. <span data-ttu-id="00162-123">Valitse Luo rivit.</span><span class="sxs-lookup"><span data-stu-id="00162-123">Click Create lines.</span></span>
    * <span data-ttu-id="00162-124">Tämän kirjauskansion rivit voidaan syöttää manuaalisesti tai luoda automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="00162-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="00162-125">Tässä osassa kerrotaan, miten rivit luodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="00162-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="00162-126">Valitse Alusta määrä -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="00162-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="00162-127">Tämä alustaa niiden kirjauskansiorivien määrän, joiden määrää ei ole rekisteröity ostotilausriviltä.</span><span class="sxs-lookup"><span data-stu-id="00162-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="00162-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="00162-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="00162-129">Kirjaa kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="00162-129">Post the journal</span></span>
1. <span data-ttu-id="00162-130">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="00162-130">Click Post.</span></span>
2. <span data-ttu-id="00162-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="00162-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="00162-132">Tuotteen vastaanoton luominen</span><span class="sxs-lookup"><span data-stu-id="00162-132">Generate the product receipt</span></span>
1. <span data-ttu-id="00162-133">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="00162-133">Click Functions.</span></span>
2. <span data-ttu-id="00162-134">Valitse Tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="00162-134">Click Product receipt.</span></span>
3. <span data-ttu-id="00162-135">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="00162-135">Click OK.</span></span>


