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
ms.openlocfilehash: 40bbb8429355fa18fe12c7cf56f8d58f19766cad
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009419"
---
# <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="9d2c3-104">Yksinkertaistettu työntekijöiden lisääminen ja navigointi</span><span class="sxs-lookup"><span data-stu-id="9d2c3-104">Streamlined employee entry and navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9d2c3-105">Dynamics 365 Talentissa työntekijä- ja työsuhdemerkinnät voidaan tehdä tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-105">Dynamics 365 Talent allows efficient entry of employee and employment data.</span></span> <span data-ttu-id="9d2c3-106">Voit päivittää nopeasti entisten, aktiivisten ja tulevien työntekijöiden ja alihankkijoiden työhistoriatiedot.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-106">You can quickly update work history information for past, active, and future employees and contractors.</span></span>

<span data-ttu-id="9d2c3-107">Voit myös ottaa käyttöön yksinkertaistetun siirtymiskokemuksen, jolla liittyvät tiedot löydetään ja tarvittavat muutokset voidaan tehdä nopeasti.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-107">You can also enable a simplified navigation experience to quickly find related information and make any necessary changes.</span></span> <span data-ttu-id="9d2c3-108">Tämä toiminto on nyt käytettävissä eristysympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-108">This functionality is now available in sandbox environments.</span></span> <span data-ttu-id="9d2c3-109">Ota tämä toiminto käyttöön valitsemalla **Järjestelmän hallinta > Linkit > Asetukset > Järjestelmän parametrit > Esiversio-ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-109">To turn this feature on, navigate to **System administration > Links > Setup > System parameters > Preview features**.</span></span> <span data-ttu-id="9d2c3-110">Valitse **Laajennettu työntekijälomake ja siirtyminen**.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-110">Select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="9d2c3-111">Nämä muutokset otetaan nyt käyttöön kaikille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-111">This will enable these changes for all users.</span></span> <span data-ttu-id="9d2c3-112">Voit poistaa tämän asetuksen käytöstä milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-112">You can turn this option off at any time.</span></span>

## <a name="view-options"></a><span data-ttu-id="9d2c3-113">Näytä asetukset</span><span class="sxs-lookup"><span data-stu-id="9d2c3-113">View options</span></span>

<span data-ttu-id="9d2c3-114">Voit valita työntekijälomakkeen **Näytä asetukset** -asetuksen avulla minkä tahansa samassa luettelossa olevien työntekijöiden ja alihankkijoiden yhdistelmän.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-114">You can use **View options** on the worker form to select any combination of employees and contractors from a single list.</span></span> <span data-ttu-id="9d2c3-115">Voit tarkastella näiden asetusten avulla eri yritysten työntekijöitä tai sen yrityksen työntekijöitä, johon olet kirjautuneena.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-115">These options allow you to view workers across legal entities or for the legal entity you're currently signed into.</span></span> <span data-ttu-id="9d2c3-116">Voit tarkastella myös aktiivisia, odottavia ja lopettaneita työntekijöitä sekä rajoittaa tuloksia työntekijän tyypin (työntekijä tai alihankkija) mukaan.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-116">You can also view active, pending, and exited workers, and you can restrict results based on the type of worker (employee or contractor).</span></span> <span data-ttu-id="9d2c3-117">Jos lisäsuojaus on otettu käyttöön, näet vain niiden yritysten työntekijät ja alihankkijat, joiden käyttöoikeus sinulla on.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-117">If advanced security is enabled, you will only see those employees and contractors in the legal entities you have access to.</span></span>

<span data-ttu-id="9d2c3-118">Luettelonäkymän sarakkeet muuttuvat valintojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-118">Columns in the list view change based on your selections.</span></span> <span data-ttu-id="9d2c3-119">Esimerkiksi lopettaneita työntekijöitä tarkasteltaessa työsuhteen loppumispäivä ja syykoodit näkyvät luettelossa ylimääräisinä sarakkeina.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-119">For example, when viewing exited employees, the termination date and reason codes display as additional columns in the list.</span></span> 

<span data-ttu-id="9d2c3-120">[![Näytä asetukset](./media/Worker-view-option.png)](./media/worker-view-option.png)</span><span class="sxs-lookup"><span data-stu-id="9d2c3-120">[![View options](./media/Worker-view-option.png)](./media/worker-view-option.png)</span></span>

## <a name="navigation-and-banner"></a><span data-ttu-id="9d2c3-121">Siirtyminen ja ilmoituspalkki</span><span class="sxs-lookup"><span data-stu-id="9d2c3-121">Navigation and banner</span></span>

<span data-ttu-id="9d2c3-122">Ilmoituspalkissa näkyy avaintietoja kustakin työntekijästä.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-122">A banner displays key information for each worker.</span></span> <span data-ttu-id="9d2c3-123">Aktiivisten työntekijöiden ilmoituspalkissa on seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="9d2c3-123">The banner for active workers displays the following fields:</span></span>

- <span data-ttu-id="9d2c3-124">**Titteli**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-124">**Title**</span></span>
- <span data-ttu-id="9d2c3-125">**Osasto**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-125">**Department**</span></span>
- <span data-ttu-id="9d2c3-126">**Toimityyppi**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-126">**Position type**</span></span>
- <span data-ttu-id="9d2c3-127">**Työntekijätyyppi**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-127">**Worker type**</span></span>
- <span data-ttu-id="9d2c3-128">**Esimies**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-128">**Manager**</span></span>
- <span data-ttu-id="9d2c3-129">**Oikeushenkilö**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-129">**Legal entity**</span></span>

<span data-ttu-id="9d2c3-130">Lopettaneiden työntekijöiden ilmoituspalkissa on seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="9d2c3-130">The banner for exited workers displays the following fields:</span></span>

- <span data-ttu-id="9d2c3-131">**Lopettamispäivä**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-131">**Exited date**</span></span>
- <span data-ttu-id="9d2c3-132">**Syy**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-132">**Reason**</span></span>

<span data-ttu-id="9d2c3-133">Odottavien työntekijöiden ilmoituspalkissa on seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="9d2c3-133">The banner for pending employees displays the following fields:</span></span>

- <span data-ttu-id="9d2c3-134">**Titteli**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-134">**Title**</span></span>
- <span data-ttu-id="9d2c3-135">**Osasto**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-135">**Department**</span></span>
- <span data-ttu-id="9d2c3-136">**Toimityyppi**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-136">**Position type**</span></span>
- <span data-ttu-id="9d2c3-137">**Esimies**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-137">**Manager**</span></span>
- <span data-ttu-id="9d2c3-138">**Aloituspäivämäärä**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-138">**Starting date**</span></span>
- <span data-ttu-id="9d2c3-139">**Oikeushenkilö**</span><span class="sxs-lookup"><span data-stu-id="9d2c3-139">**Legal entity**</span></span>

<span data-ttu-id="9d2c3-140">Työntekijäsivun toimintoruutu on järjestetty uudelleen ja siinä on vähemmän asetuksia.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-140">The action pane of the worker page has been re-organized to include fewer options.</span></span> <span data-ttu-id="9d2c3-141">Tiedot on nyt järjestetty seuraaviin luokkiin:</span><span class="sxs-lookup"><span data-stu-id="9d2c3-141">Information is now organized in the following categories:</span></span> 

- <span data-ttu-id="9d2c3-142">Työ</span><span class="sxs-lookup"><span data-stu-id="9d2c3-142">Work</span></span>
- <span data-ttu-id="9d2c3-143">Henkilö</span><span class="sxs-lookup"><span data-stu-id="9d2c3-143">Person</span></span>
- <span data-ttu-id="9d2c3-144">Poistu</span><span class="sxs-lookup"><span data-stu-id="9d2c3-144">Leave</span></span>
- <span data-ttu-id="9d2c3-145">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="9d2c3-145">Compensation</span></span>
- <span data-ttu-id="9d2c3-146">Edut</span><span class="sxs-lookup"><span data-stu-id="9d2c3-146">Benefits</span></span>
- <span data-ttu-id="9d2c3-147">Yhteensopivuus</span><span class="sxs-lookup"><span data-stu-id="9d2c3-147">Compliance</span></span>

<span data-ttu-id="9d2c3-148">Lisäksi työntekijän pääsivulla on uusi **Linkit**-välilehti, jossa käyttäjät voivat keskitetysti käyttää kaikkia työntekijään liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-148">In addtion, a new **Links** tab on the main worker page gives users a central location to access all related information for a worker.</span></span>

<span data-ttu-id="9d2c3-149">Näiden muutosten vuoksi tiedot näkyvät nyt eri paikassa kuin aiemmin.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-149">Due to these changes, information may appear in a different location than you're used to.</span></span> <span data-ttu-id="9d2c3-150">Esimerkiksi aiemmin työntekijälomakkeessa näkyneet palkanlaskentatiedot näkyvät nyt toimintoruudussa kohdassa**Kompensaatio > Palkanlaskenta**, ja **Henkilökohtaiset tiedot** -välilehdessä on nyt **Lisätietoja**-painike, jolla voi piilottaa harvoin käytetyt kentät.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-150">For example, payroll information that previously displayed on the worker form now appears in the action pane under **Compensation > Payroll**, and the **Personal information** tab now has a **More information** button to hide fields that aren't accessed often.</span></span>

<span data-ttu-id="9d2c3-151">[![Banneri](./media/Banner.png)](./media/Banner.png)</span><span class="sxs-lookup"><span data-stu-id="9d2c3-151">[![Banner](./media/Banner.png)](./media/Banner.png)</span></span>

## <a name="work-history"></a><span data-ttu-id="9d2c3-152">Työhistoria</span><span class="sxs-lookup"><span data-stu-id="9d2c3-152">Work history</span></span>

<span data-ttu-id="9d2c3-153">**Työhistoria**-välilehdessä näkyy nyt työhistoria kaikissa yrityksissä, ja nämä tiedot ovat käytettävissä lopettaneiden, aktiivisten ja odottavien työntekijöiden ja alihankkijoiden osalta.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-153">The **Work history** tab shows work history accross all legal entities and is available for exited, active, and pending employees and contractors.</span></span> <span data-ttu-id="9d2c3-154">Voit nyt tarkastella kerralla kaikkien niiden yritysten koko työhistoriaa, joiden käyttöoikeus sinulla on.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-154">You can now view all work history at once for the legal entities you have access to.</span></span> <span data-ttu-id="9d2c3-155">Voit lisäksi muokata kunkin työhistoriamerkinnän tietoja tietokontekstia muuttamatta.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-155">In addition, you can edit information for each of the work history entries without changing the data context.</span></span> <span data-ttu-id="9d2c3-156">Voit päivittää kaikki tiedot suoraan sivulla.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-156">You can update all information directly on the page.</span></span> 

<span data-ttu-id="9d2c3-157">[![Työhistoria](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span><span class="sxs-lookup"><span data-stu-id="9d2c3-157">[![Work history](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span></span>

## <a name="position-history"></a><span data-ttu-id="9d2c3-158">Toimen historiatiedot</span><span class="sxs-lookup"><span data-stu-id="9d2c3-158">Position history</span></span>

<span data-ttu-id="9d2c3-159">Työntekijän pääsivun **Toimet**-välilehdessä on täydellinen näkymä kaikissa organisaatiossa olevista toimista mukaan lukien entiset, nykyiset ja tulevat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-159">The **Positions** tab on the main worker page provides a full view of all positions held within the organization, including past, present, and any future assignments.</span></span> <span data-ttu-id="9d2c3-160">Voit edelleen siirtyä suodaan työntekijän toimihistoriaan myös toimintoruudussa.</span><span class="sxs-lookup"><span data-stu-id="9d2c3-160">You can still navigate directly to the worker's position history in the action pane as well.</span></span>

<span data-ttu-id="9d2c3-161">[![Toimet](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span><span class="sxs-lookup"><span data-stu-id="9d2c3-161">[![Positions](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span></span>

