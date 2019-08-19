---
title: Arvonlisäveron määrittäminen ja ohitukset
description: Tässä menettelyssä kerrotaan miten arvonlisäveroryhmät määritetään vähittäismyynnin kanaville.
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
ms.openlocfilehash: f08829bccbaea6fb70563e553f9042300b4d5ea9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837995"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="d808b-103">Arvonlisäveron määrittäminen ja ohitukset</span><span class="sxs-lookup"><span data-stu-id="d808b-103">Sales tax assignment and overrides</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d808b-104">Tässä menettelyssä kerrotaan miten arvonlisäveroryhmät määritetään vähittäismyynnin kanaville.</span><span class="sxs-lookup"><span data-stu-id="d808b-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="d808b-105">Siinä käydään läpi myös uusien arvonlisävero-ohitusten luontiprosessi sekä niiden määrittäminen olemassa oleviin arvonlisäveron ohitusryhmiin.</span><span class="sxs-lookup"><span data-stu-id="d808b-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="d808b-106">Tässä menettelyssä</span><span class="sxs-lookup"><span data-stu-id="d808b-106">This procedure</span></span>

<span data-ttu-id="d808b-107">käytetään esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="d808b-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="d808b-108">Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälät > Kaikki vähittäismyymälät.</span><span class="sxs-lookup"><span data-stu-id="d808b-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="d808b-109">Napsauta luettelossa Houstonin vähittäismyyntikanavan linkkiä.</span><span class="sxs-lookup"><span data-stu-id="d808b-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="d808b-110">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="d808b-110">Click Edit.</span></span>
    * <span data-ttu-id="d808b-111">Arvonlisäveroryhmä-kenttä sisältää nykyisen yrityksen arvonlisäveroryhmien luettelon.</span><span class="sxs-lookup"><span data-stu-id="d808b-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="d808b-112">Tällä hetkellä määritetty ryhmä on yleinen "Teksas"-arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="d808b-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="d808b-113">Myös seuraavat arvonlisäveroryhmät ovat järjestelmässä: Washington ja Washington, King County.</span><span class="sxs-lookup"><span data-stu-id="d808b-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="d808b-114">Arvonlisäveroryhmät voivat sisältää useita kuntia koskevia veroja.</span><span class="sxs-lookup"><span data-stu-id="d808b-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="d808b-115">"Arvonlisäveron ohitus" -kentässä määritetään kanavan arvonlisäveron ohitusryhmät.</span><span class="sxs-lookup"><span data-stu-id="d808b-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="d808b-116">Arvonlisäveron ohitusryhmiä voi käyttää useiden arvonlisäveropoikkeuksien ryhmittämiseen, jotka toimivat useille myymälöille.</span><span class="sxs-lookup"><span data-stu-id="d808b-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="d808b-117">Sen sijaan, että arvonlisäveron ohitukset määritettäisiin yksitellen, voit säästää aikaa luomalla ryhmän ja määrittää sen suoraan kanaviin.</span><span class="sxs-lookup"><span data-stu-id="d808b-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="d808b-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d808b-118">Click Save.</span></span>
5. <span data-ttu-id="d808b-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d808b-119">Close the page.</span></span>
6. <span data-ttu-id="d808b-120">Valitse Vähittäismyynti ja kauppa > Kanavan asetukset > Arvonlisäverot > Arvonlisäveron ohitukset.</span><span class="sxs-lookup"><span data-stu-id="d808b-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="d808b-121">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d808b-121">Click New.</span></span>
8. <span data-ttu-id="d808b-122">Anna Arvonlisäveron ohitus -kentässä uudelle ohitukselle nimi.</span><span class="sxs-lookup"><span data-stu-id="d808b-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="d808b-123">Anna ohituksen kuvaus Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d808b-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="d808b-124">Ota tilaksi "Käytössä".</span><span class="sxs-lookup"><span data-stu-id="d808b-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="d808b-125">Laajenna tai tiivistä Ohitus-osa.</span><span class="sxs-lookup"><span data-stu-id="d808b-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="d808b-126">Valitse vaihtoehto Tyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d808b-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="d808b-127">Nimikkeen arvonlisäveroryhmiä voi käyttää verojen ohittamiseen tietyille nimikkeille, jotka kuuluvat ryhmään.</span><span class="sxs-lookup"><span data-stu-id="d808b-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="d808b-128">Esimerkiksi ruokanimikkeiden verotus on yleensä eri tasolla kuin fyysisillä tuotteilla, ja niillä on yleensä oma arvonlisäveroryhmänsä.</span><span class="sxs-lookup"><span data-stu-id="d808b-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="d808b-129">Arvonlisäveroryhmät ovat tietyn kanavan käytettävissä olevia veroryhmiä.</span><span class="sxs-lookup"><span data-stu-id="d808b-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="d808b-130">Jos esimerkiksi kanava myy sekä vähittäiskauppana sekä yrityksille, nimikkeille voi käyttää eri arvonlisäveroryhmiä.</span><span class="sxs-lookup"><span data-stu-id="d808b-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="d808b-131">Kaikki sovellettavat verot liitetään arvonlisäveroryhmään.</span><span class="sxs-lookup"><span data-stu-id="d808b-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="d808b-132">Nyt voit valita Lähde- ja Kohde-verot tai "Veroryhmästä" ja "Veroryhmään" luodaksesi arvonlisäveron ohituksen.</span><span class="sxs-lookup"><span data-stu-id="d808b-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="d808b-133">Lähde-kenttä ilmaisee ohitettavan veron tai veroryhmän.</span><span class="sxs-lookup"><span data-stu-id="d808b-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="d808b-134">Nimikkeen arvonlisäveroryhmän ohittamisella on eri vaihtoehdot kuin arvonlisäveroryhmän perusteella ohittamisella.</span><span class="sxs-lookup"><span data-stu-id="d808b-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="d808b-135">Arvonlisäveron ohitukset voi määrittää ohittamaan verot kokonaisilla tapahtumilla tai vain tietyillä tapahtuman riveillä.</span><span class="sxs-lookup"><span data-stu-id="d808b-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="d808b-136">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d808b-136">Click Save.</span></span>
14. <span data-ttu-id="d808b-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d808b-137">Close the page.</span></span>
15. <span data-ttu-id="d808b-138">Valitse Vähittäismyynti ja kauppa > Kanavan asetukset > Arvonlisäverot > Arvonlisäveron ohitusryhmät.</span><span class="sxs-lookup"><span data-stu-id="d808b-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="d808b-139">Tässä vaiheessa määritetään uusi ohitus arvonlisäveron ohitusryhmään, joka on liitetty Houstonin kanavaan.</span><span class="sxs-lookup"><span data-stu-id="d808b-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="d808b-140">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="d808b-140">Click Edit.</span></span>
17. <span data-ttu-id="d808b-141">Laajenna tai tiivistä Asetukset-osa.</span><span class="sxs-lookup"><span data-stu-id="d808b-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="d808b-142">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="d808b-142">Click Add.</span></span>
19. <span data-ttu-id="d808b-143">Avaa haku valitsemalla Arvonlisäveron ohitusryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="d808b-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="d808b-144">Valitse luettelosta aiemmin luotu arvonlisäveron ohitus.</span><span class="sxs-lookup"><span data-stu-id="d808b-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="d808b-145">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="d808b-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="d808b-146">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d808b-146">Click Save.</span></span>

