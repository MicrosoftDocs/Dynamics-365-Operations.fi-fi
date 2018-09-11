--- 
title: "Tavaralähetysvaraston omistajuuden muuttaminen tuotannon kysynnän perusteella"
description: "Tässä menettelyssä, miten muutat tavaralähetysvaraston omistajuuden toimittajalta yrityksellesi, kun varastolle on kysyntää tuotannossa."
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 5dd00e6f53d13305949d225e73223ab54947c804
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="dc114-103">Tavaralähetysvaraston omistajuuden muuttaminen tuotannon kysynnän perusteella</span><span class="sxs-lookup"><span data-stu-id="dc114-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc114-104">Tässä menettelyssä, miten muutat tavaralähetysvaraston omistajuuden toimittajalta yrityksellesi, kun varastolle on kysyntää tuotannossa.</span><span class="sxs-lookup"><span data-stu-id="dc114-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="dc114-105">Tämä omistajuuden muutos tehdään luomalla ja kirjaamalla varaston omistajuuden muutoksen kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="dc114-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="dc114-106">Omistajuuden muutoksen kirjauskansiorivit voidaan luoda manuaalisesti, tai kuten tässä tallenteessa on näytetty, tuotannon kysynnän perusteella.</span><span class="sxs-lookup"><span data-stu-id="dc114-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="dc114-107">Yleensä työnohjauksen esimies suorittaa tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="dc114-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="dc114-108">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="dc114-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="dc114-109">Jos käytät omia tietojasi, varmista, että sinulla on seuraavat edellytykset: varaston kirjauskansionimi, joka on määritetty varaston omistajuuden muutokselle, fyysisesti kirjattuja käytettäviä nimikkeitä, joiden omistaja on toimittaja; ja yksi tai useampi tuotantotilauksen rivi materiaalille.</span><span class="sxs-lookup"><span data-stu-id="dc114-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="dc114-110">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="dc114-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="dc114-111">Luo varaston omistajuuden kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="dc114-111">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="dc114-112">Siiry kohtaan Varastonhallinta > Kirjauskansioviennit > Nimikkeet > Varaston omistajuuden muutos.</span><span class="sxs-lookup"><span data-stu-id="dc114-112">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="dc114-113">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="dc114-113">Click New.</span></span>
    * <span data-ttu-id="dc114-114">Varaston omistajuuden muutoksen kirjauskansiota käytetään muuttamaan tavaralähetysvaraston omistajuus toimittajalta nykyiselle yritykselle.</span><span class="sxs-lookup"><span data-stu-id="dc114-114">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="dc114-115">Omistuksen muutos tehdään vapauttamalla käytettävä varasto, jonka omistaja on toimittaja, ja sitten vastaanottamalla ko. varasto nykyiselle yritykselle.</span><span class="sxs-lookup"><span data-stu-id="dc114-115">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="dc114-116">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dc114-116">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="dc114-117">Voit valita ainoastaan varastokirjauskansion nimet, joiden kirjauskansiotyyppi on Omistajuuden muutos.</span><span class="sxs-lookup"><span data-stu-id="dc114-117">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="dc114-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="dc114-118">Click OK.</span></span>
5. <span data-ttu-id="dc114-119">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="dc114-119">Click Functions.</span></span>
6. <span data-ttu-id="dc114-120">Valitse Luo kirjauskansion rivit tuotantotilauksista.</span><span class="sxs-lookup"><span data-stu-id="dc114-120">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="dc114-121">Voit käynnistää omistajan muutosprosessin luomalla kyselyn kaikille tuotannon riveille, joilla on raaka-aineiden kulutuskysyntää.</span><span class="sxs-lookup"><span data-stu-id="dc114-121">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="dc114-122">Valitse vaihtoehto Sisällytettävät varasto-ottotilat -kentässä.</span><span class="sxs-lookup"><span data-stu-id="dc114-122">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="dc114-123">Tämän vaihtoehdon avulla voit suodattaa varastotapahtumien ottotilan perusteella.</span><span class="sxs-lookup"><span data-stu-id="dc114-123">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="dc114-124">Voit esimerkiksi luoda kirjauskansiorivit varastolle, jolla on fyysiset tilat Kerätty ja Varattu.</span><span class="sxs-lookup"><span data-stu-id="dc114-124">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="dc114-125">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="dc114-125">Expand the Records to include section.</span></span>
    * <span data-ttu-id="dc114-126">Tämä osan ohjeiden avulla voi lisätä ylimääräisiä suodattimia.</span><span class="sxs-lookup"><span data-stu-id="dc114-126">This section lets you apply additional filtering.</span></span> <span data-ttu-id="dc114-127">Voit esimerkiksi valita tietyn raaka-ainepäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="dc114-127">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="dc114-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="dc114-128">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="dc114-129">Kirjaa varaston omistajuuden muutoksen kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="dc114-129">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="dc114-130">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="dc114-130">Click Post.</span></span>
    * <span data-ttu-id="dc114-131">Kun kirjauskansio kirjataan, toimittajan omistama varasto vapautetaan "Omistuksen muutos"-viittauksen avulla.</span><span class="sxs-lookup"><span data-stu-id="dc114-131">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="dc114-132">Varasto vastaanotetaan sitten käytettäväksi varastotapahtumalla, johon päivitetään ostotilauksen tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="dc114-132">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="dc114-133">Huomaa, että vain ne tapahtumat luodaan, jotka liittyvät kirjattuun kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="dc114-133">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="dc114-134">Odotettuja varastotapahtumia ei luoda.</span><span class="sxs-lookup"><span data-stu-id="dc114-134">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="dc114-135">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="dc114-135">Click OK.</span></span>
3. <span data-ttu-id="dc114-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dc114-136">Close the page.</span></span>


