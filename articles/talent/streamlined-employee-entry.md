---
title: Yksinkertaistettu työntekijöiden lisääminen ja navigointi
description: Työntekijöiden tietomerkinnät Dynamics 365 Talentissa on laajennettu sallimaan kaikkien työntekijöiden (entiset, aktiiviset ja tulevat) merkinnät. Yksinkertaistettu/konsolidoitu siirtymismalli on päivitetty etsimään nopeasti aiheeseen liittyviä tietoja sekä näyttämään ja tekemään tarvittavat päivitykset.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: b73b420c2eb75077814fbfeb6cd17404c7efc11e
ms.sourcegitcommit: 436731d8b3889bebfe6f17922b0a31b1994f6796
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/26/2020
ms.locfileid: "4461104"
---
# <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="7f1ca-104">Yksinkertaistettu työntekijöiden lisääminen ja navigointi</span><span class="sxs-lookup"><span data-stu-id="7f1ca-104">Streamlined employee entry and navigation</span></span>

<span data-ttu-id="7f1ca-105">Dynamics 365 Talentissa työntekijä- ja työsuhdemerkinnät voidaan tehdä tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-105">Dynamics 365 Talent allows efficient entry of employee and employment data.</span></span> <span data-ttu-id="7f1ca-106">Voit päivittää nopeasti entisten, aktiivisten ja tulevien työntekijöiden ja alihankkijoiden työhistoriatiedot.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-106">You can quickly update work history information for past, active, and future employees and contractors.</span></span>

<span data-ttu-id="7f1ca-107">Voit myös ottaa käyttöön yksinkertaistetun siirtymiskokemuksen, jolla liittyvät tiedot löydetään ja tarvittavat muutokset voidaan tehdä nopeasti.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-107">You can also enable a simplified navigation experience to quickly find related information and make any necessary changes.</span></span> <span data-ttu-id="7f1ca-108">Tämä toiminto on nyt käytettävissä kaikissa ympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-108">This functionality is now available in all environments.</span></span> <span data-ttu-id="7f1ca-109">Voit ottaa tämän ominaisuuden käyttöön siirtymällä kohtaan **Järjestelmänhallinta > Ominaisuuksienhallinta > Uusi > Virtaviivaistettu työntekijämerkintä > Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-109">To turn this feature on, navigate to **System administration > Feature Management > New > Streamlined employee entry > Enable**.</span></span> <span data-ttu-id="7f1ca-110">Nämä muutokset otetaan nyt käyttöön kaikille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-110">This will enable these changes for all users.</span></span> <span data-ttu-id="7f1ca-111">Voit poistaa tämän asetuksen käytöstä milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-111">You can turn this option off at any time.</span></span>

## <a name="view-options"></a><span data-ttu-id="7f1ca-112">Näytä asetukset</span><span class="sxs-lookup"><span data-stu-id="7f1ca-112">View options</span></span>

<span data-ttu-id="7f1ca-113">Voit valita työntekijälomakkeen **Näytä asetukset** -asetuksen avulla minkä tahansa samassa luettelossa olevien työntekijöiden ja alihankkijoiden yhdistelmän.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-113">You can use **View options** on the worker form to select any combination of employees and contractors from a single list.</span></span> <span data-ttu-id="7f1ca-114">Voit tarkastella näiden asetusten avulla eri yritysten työntekijöitä tai sen yrityksen työntekijöitä, johon olet kirjautuneena.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-114">These options allow you to view workers across legal entities or for the legal entity you're currently signed into.</span></span> <span data-ttu-id="7f1ca-115">Voit tarkastella myös aktiivisia, odottavia ja lopettaneita työntekijöitä sekä rajoittaa tuloksia työntekijän tyypin (työntekijä tai alihankkija) mukaan.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-115">You can also view active, pending, and exited workers, and you can restrict results based on the type of worker (employee or contractor).</span></span> <span data-ttu-id="7f1ca-116">Jos lisäsuojaus on otettu käyttöön, näet vain niiden yritysten työntekijät ja alihankkijat, joiden käyttöoikeus sinulla on.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-116">If advanced security is enabled, you will only see those employees and contractors in the legal entities you have access to.</span></span>

<span data-ttu-id="7f1ca-117">Luettelonäkymän sarakkeet muuttuvat valintojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-117">Columns in the list view change based on your selections.</span></span> <span data-ttu-id="7f1ca-118">Esimerkiksi lopettaneita työntekijöitä tarkasteltaessa työsuhteen loppumispäivä ja syykoodit näkyvät luettelossa ylimääräisinä sarakkeina.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-118">For example, when viewing exited employees, the termination date and reason codes display as additional columns in the list.</span></span> 

<span data-ttu-id="7f1ca-119">[![Näytä asetukset](./media/Worker-view-option.png)](./media/worker-view-option.png)</span><span class="sxs-lookup"><span data-stu-id="7f1ca-119">[![View options](./media/Worker-view-option.png)](./media/worker-view-option.png)</span></span>

## <a name="navigation-and-banner"></a><span data-ttu-id="7f1ca-120">Siirtyminen ja ilmoituspalkki</span><span class="sxs-lookup"><span data-stu-id="7f1ca-120">Navigation and banner</span></span>

<span data-ttu-id="7f1ca-121">Ilmoituspalkissa näkyy avaintietoja kustakin työntekijästä.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-121">A banner displays key information for each worker.</span></span> <span data-ttu-id="7f1ca-122">Aktiivisten työntekijöiden ilmoituspalkissa on seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="7f1ca-122">The banner for active workers displays the following fields:</span></span>

- <span data-ttu-id="7f1ca-123">**Titteli**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-123">**Title**</span></span>
- <span data-ttu-id="7f1ca-124">**Osasto**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-124">**Department**</span></span>
- <span data-ttu-id="7f1ca-125">**Toimityyppi**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-125">**Position type**</span></span>
- <span data-ttu-id="7f1ca-126">**Työntekijätyyppi**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-126">**Worker type**</span></span>
- <span data-ttu-id="7f1ca-127">**Esimies**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-127">**Manager**</span></span>
- <span data-ttu-id="7f1ca-128">**Oikeushenkilö**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-128">**Legal entity**</span></span>

<span data-ttu-id="7f1ca-129">Lopettaneiden työntekijöiden ilmoituspalkissa on seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="7f1ca-129">The banner for exited workers displays the following fields:</span></span>

- <span data-ttu-id="7f1ca-130">**Lopettamispäivä**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-130">**Exited date**</span></span>
- <span data-ttu-id="7f1ca-131">**Syy**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-131">**Reason**</span></span>

<span data-ttu-id="7f1ca-132">Odottavien työntekijöiden ilmoituspalkissa on seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="7f1ca-132">The banner for pending employees displays the following fields:</span></span>

- <span data-ttu-id="7f1ca-133">**Titteli**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-133">**Title**</span></span>
- <span data-ttu-id="7f1ca-134">**Osasto**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-134">**Department**</span></span>
- <span data-ttu-id="7f1ca-135">**Toimityyppi**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-135">**Position type**</span></span>
- <span data-ttu-id="7f1ca-136">**Esimies**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-136">**Manager**</span></span>
- <span data-ttu-id="7f1ca-137">**Aloituspäivämäärä**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-137">**Starting date**</span></span>
- <span data-ttu-id="7f1ca-138">**Oikeushenkilö**</span><span class="sxs-lookup"><span data-stu-id="7f1ca-138">**Legal entity**</span></span>

<span data-ttu-id="7f1ca-139">Työntekijäsivun toimintoruutu on järjestetty uudelleen ja siinä on vähemmän asetuksia.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-139">The action pane of the worker page has been re-organized to include fewer options.</span></span> <span data-ttu-id="7f1ca-140">Tiedot on nyt järjestetty seuraaviin luokkiin:</span><span class="sxs-lookup"><span data-stu-id="7f1ca-140">Information is now organized in the following categories:</span></span> 

- <span data-ttu-id="7f1ca-141">Työ</span><span class="sxs-lookup"><span data-stu-id="7f1ca-141">Work</span></span>
- <span data-ttu-id="7f1ca-142">Henkilö</span><span class="sxs-lookup"><span data-stu-id="7f1ca-142">Person</span></span>
- <span data-ttu-id="7f1ca-143">Loma</span><span class="sxs-lookup"><span data-stu-id="7f1ca-143">Leave</span></span>
- <span data-ttu-id="7f1ca-144">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="7f1ca-144">Compensation</span></span>
- <span data-ttu-id="7f1ca-145">Edut</span><span class="sxs-lookup"><span data-stu-id="7f1ca-145">Benefits</span></span>
- <span data-ttu-id="7f1ca-146">Yhteensopivuus</span><span class="sxs-lookup"><span data-stu-id="7f1ca-146">Compliance</span></span>

<span data-ttu-id="7f1ca-147">Lisäksi työntekijän pääsivun uuden **Linkit**-välilehden avulla käyttäjät voivat käyttää keskitetysti työntekijän kaikkia liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-147">In addition, a new **Links** tab on the main worker page gives users a central location to access all related information for a worker.</span></span>

<span data-ttu-id="7f1ca-148">Näiden muutosten vuoksi tiedot näkyvät nyt eri paikassa kuin aiemmin.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-148">Due to these changes, information may appear in a different location than you're used to.</span></span> <span data-ttu-id="7f1ca-149">Esimerkiksi aiemmin työntekijälomakkeessa näkyneet palkanlaskentatiedot näkyvät nyt toimintoruudussa kohdassa **Kompensaatio > Palkanlaskenta**, ja **Henkilökohtaiset tiedot** -välilehdessä on nyt **Lisätietoja**-painike, jolla voi piilottaa harvoin käytetyt kentät.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-149">For example, payroll information that previously displayed on the worker form now appears in the action pane under **Compensation > Payroll**, and the **Personal information** tab now has a **More information** button to hide fields that aren't accessed often.</span></span>

<span data-ttu-id="7f1ca-150">[![Banneri](./media/Banner.png)](./media/Banner.png)</span><span class="sxs-lookup"><span data-stu-id="7f1ca-150">[![Banner](./media/Banner.png)](./media/Banner.png)</span></span>

## <a name="work-history"></a><span data-ttu-id="7f1ca-151">Työhistoria</span><span class="sxs-lookup"><span data-stu-id="7f1ca-151">Work history</span></span>

<span data-ttu-id="7f1ca-152">**Työhistoria**-välilehdessä näkyy nyt työhistoria kaikissa yrityksissä, ja nämä tiedot ovat käytettävissä lopettaneiden, aktiivisten ja odottavien työntekijöiden ja alihankkijoiden osalta.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-152">The **Work history** tab shows work history across all legal entities and is available for exited, active, and pending employees and contractors.</span></span> <span data-ttu-id="7f1ca-153">Voit nyt tarkastella kerralla kaikkien niiden yritysten koko työhistoriaa, joiden käyttöoikeus sinulla on.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-153">You can now view all work history at once for the legal entities you have access to.</span></span> <span data-ttu-id="7f1ca-154">Voit lisäksi muokata kunkin työhistoriamerkinnän tietoja tietokontekstia muuttamatta.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-154">In addition, you can edit information for each of the work history entries without changing the data context.</span></span> <span data-ttu-id="7f1ca-155">Voit päivittää kaikki tiedot suoraan sivulla.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-155">You can update all information directly on the page.</span></span> 

<span data-ttu-id="7f1ca-156">[![Työhistoria](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span><span class="sxs-lookup"><span data-stu-id="7f1ca-156">[![Work history](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span></span>

## <a name="position-history"></a><span data-ttu-id="7f1ca-157">Toimen historiatiedot</span><span class="sxs-lookup"><span data-stu-id="7f1ca-157">Position history</span></span>

<span data-ttu-id="7f1ca-158">Työntekijän pääsivun **Toimet**-välilehdessä on täydellinen näkymä kaikissa organisaatiossa olevista toimista mukaan lukien entiset, nykyiset ja tulevat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-158">The **Positions** tab on the main worker page provides a full view of all positions held within the organization, including past, present, and any future assignments.</span></span> <span data-ttu-id="7f1ca-159">Voit edelleen siirtyä suodaan työntekijän toimihistoriaan myös toimintoruudussa.</span><span class="sxs-lookup"><span data-stu-id="7f1ca-159">You can still navigate directly to the worker's position history in the action pane as well.</span></span>

<span data-ttu-id="7f1ca-160">[![Toimet](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span><span class="sxs-lookup"><span data-stu-id="7f1ca-160">[![Positions](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span></span>

