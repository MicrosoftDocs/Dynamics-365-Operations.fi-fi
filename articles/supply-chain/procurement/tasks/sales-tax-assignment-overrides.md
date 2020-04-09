---
title: Arvonlisäveron määrittäminen ja ohitukset
description: Tässä menettelyssä kerrotaan miten arvonlisäveroryhmät määritetään kaupan kanaville.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8d7025db9dae57d04ee8b0f827cc13d659ad699
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3161774"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="8cd20-103">Arvonlisäveron määrittäminen ja ohitukset</span><span class="sxs-lookup"><span data-stu-id="8cd20-103">Sales tax assignment and overrides</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8cd20-104">Tässä menettelyssä kerrotaan miten arvonlisäveroryhmät määritetään kaupan kanaville.</span><span class="sxs-lookup"><span data-stu-id="8cd20-104">This procedure demonstrates how to assign sales tax groups to commerce channels.</span></span> <span data-ttu-id="8cd20-105">Siinä käydään läpi myös uusien arvonlisävero-ohitusten luontiprosessi sekä niiden määrittäminen olemassa oleviin arvonlisäveron ohitusryhmiin.</span><span class="sxs-lookup"><span data-stu-id="8cd20-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="8cd20-106">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="8cd20-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="8cd20-107">Valitse Retail ja Commerce > Kanavat > Myymälät > Kaikki myymälät.</span><span class="sxs-lookup"><span data-stu-id="8cd20-107">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="8cd20-108">Napsauta luettelossa Houstonin kanavan linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8cd20-108">In the list, click the Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="8cd20-109">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="8cd20-109">Click Edit.</span></span>
    * <span data-ttu-id="8cd20-110">Arvonlisäveroryhmä-kenttä sisältää nykyisen yrityksen arvonlisäveroryhmien luettelon.</span><span class="sxs-lookup"><span data-stu-id="8cd20-110">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="8cd20-111">Tällä hetkellä määritetty ryhmä on yleinen "Teksas"-arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="8cd20-111">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="8cd20-112">Myös seuraavat arvonlisäveroryhmät ovat järjestelmässä: Washington ja Washington, King County.</span><span class="sxs-lookup"><span data-stu-id="8cd20-112">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="8cd20-113">Arvonlisäveroryhmät voivat sisältää useita kuntia koskevia veroja.</span><span class="sxs-lookup"><span data-stu-id="8cd20-113">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="8cd20-114">"Arvonlisäveron ohitus" -kentässä määritetään kanavan arvonlisäveron ohitusryhmät.</span><span class="sxs-lookup"><span data-stu-id="8cd20-114">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="8cd20-115">Arvonlisäveron ohitusryhmiä voi käyttää useiden arvonlisäveropoikkeuksien ryhmittämiseen, jotka toimivat useille myymälöille.</span><span class="sxs-lookup"><span data-stu-id="8cd20-115">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="8cd20-116">Sen sijaan, että arvonlisäveron ohitukset määritettäisiin yksitellen, voit säästää aikaa luomalla ryhmän ja määrittää sen suoraan kanaviin.</span><span class="sxs-lookup"><span data-stu-id="8cd20-116">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="8cd20-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8cd20-117">Click Save.</span></span>
5. <span data-ttu-id="8cd20-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8cd20-118">Close the page.</span></span>
6. <span data-ttu-id="8cd20-119">Valitse Retail ja Commerce > Kanavan asetukset > Arvonlisäverot > Arvonlisäveron ohitukset.</span><span class="sxs-lookup"><span data-stu-id="8cd20-119">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="8cd20-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8cd20-120">Click New.</span></span>
8. <span data-ttu-id="8cd20-121">Anna Arvonlisäveron ohitus -kentässä uudelle ohitukselle nimi.</span><span class="sxs-lookup"><span data-stu-id="8cd20-121">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="8cd20-122">Anna ohituksen kuvaus Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8cd20-122">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="8cd20-123">Ota tilaksi "Käytössä".</span><span class="sxs-lookup"><span data-stu-id="8cd20-123">Set the status to "Enable."</span></span>
11. <span data-ttu-id="8cd20-124">Laajenna tai tiivistä Ohitus-osa.</span><span class="sxs-lookup"><span data-stu-id="8cd20-124">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="8cd20-125">Valitse vaihtoehto Tyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="8cd20-125">In the Type field, select an option.</span></span>
    * <span data-ttu-id="8cd20-126">Nimikkeen arvonlisäveroryhmiä voi käyttää verojen ohittamiseen tietyille nimikkeille, jotka kuuluvat ryhmään.</span><span class="sxs-lookup"><span data-stu-id="8cd20-126">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="8cd20-127">Esimerkiksi ruokanimikkeiden verotus on yleensä eri tasolla kuin fyysisillä tuotteilla, ja niillä on yleensä oma arvonlisäveroryhmänsä.</span><span class="sxs-lookup"><span data-stu-id="8cd20-127">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span> <span data-ttu-id="8cd20-128">Arvonlisäveroryhmät ovat tietyn kanavan käytettävissä olevia veroryhmiä.</span><span class="sxs-lookup"><span data-stu-id="8cd20-128">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="8cd20-129">Jos esimerkiksi kanava myy sekä vähittäiskauppana sekä yrityksille, nimikkeille voi käyttää eri arvonlisäveroryhmiä.</span><span class="sxs-lookup"><span data-stu-id="8cd20-129">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="8cd20-130">Kaikki sovellettavat verot liitetään arvonlisäveroryhmään.</span><span class="sxs-lookup"><span data-stu-id="8cd20-130">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="8cd20-131">Nyt voit valita Lähde- ja Kohde-verot tai "Veroryhmästä" ja "Veroryhmään" luodaksesi arvonlisäveron ohituksen.</span><span class="sxs-lookup"><span data-stu-id="8cd20-131">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span> <span data-ttu-id="8cd20-132">Lähde-kenttä ilmaisee ohitettavan veron tai veroryhmän.</span><span class="sxs-lookup"><span data-stu-id="8cd20-132">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="8cd20-133">Nimikkeen arvonlisäveroryhmän ohittamisella on eri vaihtoehdot kuin arvonlisäveroryhmän perusteella ohittamisella.</span><span class="sxs-lookup"><span data-stu-id="8cd20-133">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span> <span data-ttu-id="8cd20-134">Arvonlisäveron ohitukset voi määrittää ohittamaan verot kokonaisilla tapahtumilla tai vain tietyillä tapahtuman riveillä.</span><span class="sxs-lookup"><span data-stu-id="8cd20-134">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="8cd20-135">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8cd20-135">Click Save.</span></span>
14. <span data-ttu-id="8cd20-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8cd20-136">Close the page.</span></span>
15. <span data-ttu-id="8cd20-137">Valitse Retail ja Commerce > Kanavan asetukset > Arvonlisäverot > Arvonlisäveron ohitusryhmät.</span><span class="sxs-lookup"><span data-stu-id="8cd20-137">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="8cd20-138">Tässä vaiheessa määritetään uusi ohitus arvonlisäveron ohitusryhmään, joka on liitetty Houstonin kanavaan.</span><span class="sxs-lookup"><span data-stu-id="8cd20-138">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="8cd20-139">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="8cd20-139">Click Edit.</span></span>
17. <span data-ttu-id="8cd20-140">Laajenna tai tiivistä Asetukset-osa.</span><span class="sxs-lookup"><span data-stu-id="8cd20-140">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="8cd20-141">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="8cd20-141">Click Add.</span></span>
19. <span data-ttu-id="8cd20-142">Avaa haku valitsemalla Arvonlisäveron ohitusryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8cd20-142">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="8cd20-143">Valitse luettelosta aiemmin luotu arvonlisäveron ohitus.</span><span class="sxs-lookup"><span data-stu-id="8cd20-143">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="8cd20-144">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8cd20-144">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="8cd20-145">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8cd20-145">Click Save.</span></span>

