--- 
title: "Arvonlisäveron määrittäminen ja ohitukset"
description: "Tässä menettelyssä kerrotaan miten arvonlisäveroryhmät määritetään vähittäismyynnin kanaville."
author: mkirknel
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
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b3f13738044c81d32098072f26f204a4acb2d08d
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="75bf9-103">Arvonlisäveron määrittäminen ja ohitukset</span><span class="sxs-lookup"><span data-stu-id="75bf9-103">Sales tax assignment and overrides</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="75bf9-104">Tässä menettelyssä kerrotaan miten arvonlisäveroryhmät määritetään vähittäismyynnin kanaville.</span><span class="sxs-lookup"><span data-stu-id="75bf9-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="75bf9-105">Siinä käydään läpi myös uusien arvonlisävero-ohitusten luontiprosessi sekä niiden määrittäminen olemassa oleviin arvonlisäveron ohitusryhmiin.</span><span class="sxs-lookup"><span data-stu-id="75bf9-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="75bf9-106">Tässä menettelyssä</span><span class="sxs-lookup"><span data-stu-id="75bf9-106">This procedure</span></span>

<span data-ttu-id="75bf9-107">käytetään esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="75bf9-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="75bf9-108">Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälät > Kaikki vähittäismyymälät.</span><span class="sxs-lookup"><span data-stu-id="75bf9-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="75bf9-109">Napsauta luettelossa Houstonin vähittäismyyntikanavan linkkiä.</span><span class="sxs-lookup"><span data-stu-id="75bf9-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="75bf9-110">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="75bf9-110">Click Edit.</span></span>
    * <span data-ttu-id="75bf9-111">Arvonlisäveroryhmä-kenttä sisältää nykyisen yrityksen arvonlisäveroryhmien luettelon.</span><span class="sxs-lookup"><span data-stu-id="75bf9-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="75bf9-112">Tällä hetkellä määritetty ryhmä on yleinen "Teksas"-arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="75bf9-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="75bf9-113">Myös seuraavat arvonlisäveroryhmät ovat järjestelmässä: Washington ja Washington, King County.</span><span class="sxs-lookup"><span data-stu-id="75bf9-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="75bf9-114">Arvonlisäveroryhmät voivat sisältää useita kuntia koskevia veroja.</span><span class="sxs-lookup"><span data-stu-id="75bf9-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="75bf9-115">"Arvonlisäveron ohitus" -kentässä määritetään kanavan arvonlisäveron ohitusryhmät.</span><span class="sxs-lookup"><span data-stu-id="75bf9-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="75bf9-116">Arvonlisäveron ohitusryhmiä voi käyttää useiden arvonlisäveropoikkeuksien ryhmittämiseen, jotka toimivat useille myymälöille.</span><span class="sxs-lookup"><span data-stu-id="75bf9-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="75bf9-117">Sen sijaan, että arvonlisäveron ohitukset määritettäisiin yksitellen, voit säästää aikaa luomalla ryhmän ja määrittää sen suoraan kanaviin.</span><span class="sxs-lookup"><span data-stu-id="75bf9-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="75bf9-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="75bf9-118">Click Save.</span></span>
5. <span data-ttu-id="75bf9-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="75bf9-119">Close the page.</span></span>
6. <span data-ttu-id="75bf9-120">Valitse Vähittäismyynti ja kauppa > Kanavan asetukset > Arvonlisäverot > Arvonlisäveron ohitukset.</span><span class="sxs-lookup"><span data-stu-id="75bf9-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="75bf9-121">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="75bf9-121">Click New.</span></span>
8. <span data-ttu-id="75bf9-122">Anna Arvonlisäveron ohitus -kentässä uudelle ohitukselle nimi.</span><span class="sxs-lookup"><span data-stu-id="75bf9-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="75bf9-123">Anna ohituksen kuvaus Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="75bf9-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="75bf9-124">Ota tilaksi "Käytössä".</span><span class="sxs-lookup"><span data-stu-id="75bf9-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="75bf9-125">Laajenna tai tiivistä Ohitus-osa.</span><span class="sxs-lookup"><span data-stu-id="75bf9-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="75bf9-126">Valitse vaihtoehto Tyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="75bf9-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="75bf9-127">Nimikkeen arvonlisäveroryhmiä voi käyttää verojen ohittamiseen tietyille nimikkeille, jotka kuuluvat ryhmään.</span><span class="sxs-lookup"><span data-stu-id="75bf9-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="75bf9-128">Esimerkiksi ruokanimikkeiden verotus on yleensä eri tasolla kuin fyysisillä tuotteilla, ja niillä on yleensä oma arvonlisäveroryhmänsä.</span><span class="sxs-lookup"><span data-stu-id="75bf9-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="75bf9-129">Arvonlisäveroryhmät ovat tietyn kanavan käytettävissä olevia veroryhmiä.</span><span class="sxs-lookup"><span data-stu-id="75bf9-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="75bf9-130">Jos esimerkiksi kanava myy sekä vähittäiskauppana sekä yrityksille, nimikkeille voi käyttää eri arvonlisäveroryhmiä.</span><span class="sxs-lookup"><span data-stu-id="75bf9-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="75bf9-131">Kaikki sovellettavat verot liitetään arvonlisäveroryhmään.</span><span class="sxs-lookup"><span data-stu-id="75bf9-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="75bf9-132">Nyt voit valita Lähde- ja Kohde-verot tai "Veroryhmästä" ja "Veroryhmään" luodaksesi arvonlisäveron ohituksen.</span><span class="sxs-lookup"><span data-stu-id="75bf9-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="75bf9-133">Lähde-kenttä ilmaisee ohitettavan veron tai veroryhmän.</span><span class="sxs-lookup"><span data-stu-id="75bf9-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="75bf9-134">Nimikkeen arvonlisäveroryhmän ohittamisella on eri vaihtoehdot kuin arvonlisäveroryhmän perusteella ohittamisella.</span><span class="sxs-lookup"><span data-stu-id="75bf9-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="75bf9-135">Arvonlisäveron ohitukset voi määrittää ohittamaan verot kokonaisilla tapahtumilla tai vain tietyillä tapahtuman riveillä.</span><span class="sxs-lookup"><span data-stu-id="75bf9-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="75bf9-136">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="75bf9-136">Click Save.</span></span>
14. <span data-ttu-id="75bf9-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="75bf9-137">Close the page.</span></span>
15. <span data-ttu-id="75bf9-138">Valitse Vähittäismyynti ja kauppa > Kanavan asetukset > Arvonlisäverot > Arvonlisäveron ohitusryhmät.</span><span class="sxs-lookup"><span data-stu-id="75bf9-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="75bf9-139">Tässä vaiheessa määritetään uusi ohitus arvonlisäveron ohitusryhmään, joka on liitetty Houstonin kanavaan.</span><span class="sxs-lookup"><span data-stu-id="75bf9-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="75bf9-140">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="75bf9-140">Click Edit.</span></span>
17. <span data-ttu-id="75bf9-141">Laajenna tai tiivistä Asetukset-osa.</span><span class="sxs-lookup"><span data-stu-id="75bf9-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="75bf9-142">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="75bf9-142">Click Add.</span></span>
19. <span data-ttu-id="75bf9-143">Avaa haku valitsemalla Arvonlisäveron ohitusryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="75bf9-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="75bf9-144">Valitse luettelosta aiemmin luotu arvonlisäveron ohitus.</span><span class="sxs-lookup"><span data-stu-id="75bf9-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="75bf9-145">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="75bf9-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="75bf9-146">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="75bf9-146">Click Save.</span></span>


