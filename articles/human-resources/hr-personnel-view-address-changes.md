---
title: Osoitemuutosten tarkasteleminen ja hallinta
description: Tässä ohjeaiheessa kerrotaan, kuinka voit tarkastella ja hallita Dynamics 365 Human Resources -järjestelmän osoitemuutoksia.
author: andreabichsel
manager: AnnBe
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a69d723b45e834b022491c8eaf2a7fb580e54f1d
ms.sourcegitcommit: 288df4fe766536e51ca9b5306c5bb948b7772ac5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2020
ms.locfileid: "3688318"
---
# <a name="view-and-manage-address-changes"></a><span data-ttu-id="b1b0a-103">Osoitemuutosten tarkasteleminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="b1b0a-103">View and manage address changes</span></span>

<span data-ttu-id="b1b0a-104">Tässä ohjeaiheessa kerrotaan, kuinka voit tarkastella ja hallita osoitemuutoksia työntekijän itsepalvelun **Muokkaa henkilökohtaisia tietoja** -sivulla tai **työntekijän** tiedot -sivulla Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-104">This topic explains how you can view and manage address changes in the Employee self-service **Edit personal details** page or the **Worker** details page in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="b1b0a-105">Monet organisaatiot haluavat, että työntekijät voivat hallita omia henkilötietojaan itsepalvelukokemuksen kautta.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-105">Many organizations want employees to manage their own personal details through a self-service experience.</span></span> <span data-ttu-id="b1b0a-106">Voit sallia käyttäjien päivittää osoitteensa **työntekijän itsepalvelu** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-106">You can allow users to update their address in the **Employee self service** workspace.</span></span> <span data-ttu-id="b1b0a-107">Tämän jälkeen voit seurata muutoksia **henkilöstöhallinnan** työtilassa.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-107">You can then monitor these changes in the **Personnel management** workspace.</span></span> <span data-ttu-id="b1b0a-108">Jotta voisit käyttää tätä toimintoa, sinun on määritettävä, kuinka monta päivää haluat tarkastella muutoksia **henkilöstöhallinnon parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-108">To use this feature, you must specify the number of days that you want to view changes in the **Human resources parameters** page.</span></span>

## <a name="configure-address-change-parameters"></a><span data-ttu-id="b1b0a-109">Osoitteenmuutosparametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b1b0a-109">Configure address change parameters</span></span>

<span data-ttu-id="b1b0a-110">Voit määrittää, montako päivää haluat osoitteiden muutosten näkyvän **henkilöstöhallinnan** työtilassa, toimimalla seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b1b0a-110">To configure the number of days that you want address changes to appear in the **Personnel management** workspace, follow these steps:</span></span>

1. <span data-ttu-id="b1b0a-111">Valitse siirtymisruudussa **henkilöstöhallinto**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-111">On the navigation pane, select **Personnel management**.</span></span>

2. <span data-ttu-id="b1b0a-112">Valitse **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-112">Select **Links**.</span></span>

3. <span data-ttu-id="b1b0a-113">Määritä **henkilöstöhallinnon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-113">Select **Human resources parameters**.</span></span>

4. <span data-ttu-id="b1b0a-114">Kirjoita osoitteenmuutoskohdan **päivien määrä** -kenttään päivien määrä, jonka haluat **osoitteen muutosten** näkyvän **henkilöstöhallinnon** työtilassa.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-114">In the **Number of days** field under **Address change**, enter the number of days that you want address changes to appear in the **Personnel management** workspace.</span></span>

5. <span data-ttu-id="b1b0a-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-115">Close the page.</span></span>

## <a name="create-or-change-an-employee-address"></a><span data-ttu-id="b1b0a-116">Työntekijän osoitteen luominen tai muuttaminen</span><span class="sxs-lookup"><span data-stu-id="b1b0a-116">Create or change an employee address</span></span>

<span data-ttu-id="b1b0a-117">Työntekijät voivat päivittää osoitteensa **työntekijän itsepalvelu** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-117">Employees can update their own address in the **Employee self service** workspace.</span></span> <span data-ttu-id="b1b0a-118">Noudata seuraavia ohjeita luodaksesi tai muuttaaksesi osoitetta:</span><span class="sxs-lookup"><span data-stu-id="b1b0a-118">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="b1b0a-119">Valitse **Työntekijän itsepalvelu** -ruutu aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-119">Select the **Employee self-service** tile on your home page.</span></span>

2. <span data-ttu-id="b1b0a-120">Valitse **Muokkaa henkilökohtaisia tietoja**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-120">Select **Edit personal details**.</span></span>

3. <span data-ttu-id="b1b0a-121">Valitse **Lisää** lisätäksesi osoitteen.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-121">To add an address, select **Add**.</span></span> <span data-ttu-id="b1b0a-122">Jos haluat päivittää aiemmin luotua osoitetta, valitse osoite listasta ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-122">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="b1b0a-123">Kirjoita **Nimi tai kuvaus**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-123">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="b1b0a-124">Valitse **Tarkoitus** avattavasta luetteloruudusta ja valitse sitten osoitetyyppi.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-124">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="b1b0a-125">Syötä **Maa/alue**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-125">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="b1b0a-126">Kirjoita **postinumero**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-126">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="b1b0a-127">Kirjoita **katuosoite**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-127">Enter the **Street**.</span></span>

9. <span data-ttu-id="b1b0a-128">Kirjoita **paikkakunta**, **osavaltio**ja **alue**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-128">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="b1b0a-129">Yleensä nämä kentät määritetään automaattisesti **Postinumero**-kentän perusteella.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-129">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="b1b0a-130">Vaihtoehtoisesti voit valita ensisijaisen osoitteen **ensisijaiselle** kentälle.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-130">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="b1b0a-131">Vain yksi osoite voidaan merkitä ensisijaiseksi.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-131">Only one address can be marked as the primary.</span></span> <span data-ttu-id="b1b0a-132">Jos toinen osoite on jo merkitty ensisijaiseksi osoitteeksi, sinun on vahvistettava, että haluat käyttää tätä osoitetta ensisijaisena.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-132">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="b1b0a-133">Vaihtoehtoisesti voit valita yksityisen osoitteen **yksityiselle** kentälle.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-133">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="b1b0a-134">Vain käyttäjät, joilla on nimenomainen oikeus tarkastella yksityisiä osoitetietoja, voivat tarkastella tätä osoitetta.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-134">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="b1b0a-135">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-135">Select **OK**.</span></span>

## <a name="create-or-change-a-worker-address"></a><span data-ttu-id="b1b0a-136">Työntekijän osoitteen luominen tai muuttaminen</span><span class="sxs-lookup"><span data-stu-id="b1b0a-136">Create or change a worker address</span></span>

<span data-ttu-id="b1b0a-137">Voit päivittää osoitteen **henkilöstöhallinnan** työtilassa.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-137">You can update an address in the **Personnel management** workspace.</span></span> <span data-ttu-id="b1b0a-138">Noudata seuraavia ohjeita luodaksesi tai muuttaaksesi osoitetta:</span><span class="sxs-lookup"><span data-stu-id="b1b0a-138">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="b1b0a-139">Valitse **henkilöstöhallinnan** työtilassa **linkit** ja valitse sitten **työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-139">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>

3. <span data-ttu-id="b1b0a-140">Valitse työntekijä ja valitse sitten **Osoitteet**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-140">Select the worker, and then select **Addresses**.</span></span>

3. <span data-ttu-id="b1b0a-141">Valitse **Lisää** lisätäksesi osoitteen.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-141">To add an address, select **Add**.</span></span> <span data-ttu-id="b1b0a-142">Jos haluat päivittää aiemmin luotua osoitetta, valitse osoite listasta ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-142">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="b1b0a-143">Kirjoita **Nimi tai kuvaus**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-143">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="b1b0a-144">Valitse **Tarkoitus** avattavasta luetteloruudusta ja valitse sitten osoitetyyppi.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-144">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="b1b0a-145">Syötä **Maa/alue**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-145">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="b1b0a-146">Kirjoita **postinumero**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-146">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="b1b0a-147">Kirjoita **katuosoite**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-147">Enter the **Street**.</span></span>

9. <span data-ttu-id="b1b0a-148">Kirjoita **paikkakunta**, **osavaltio**ja **alue**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-148">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="b1b0a-149">Yleensä nämä kentät määritetään automaattisesti **Postinumero**-kentän perusteella.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-149">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="b1b0a-150">Vaihtoehtoisesti voit valita ensisijaisen osoitteen **ensisijaiselle** kentälle.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-150">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="b1b0a-151">Vain yksi osoite voidaan merkitä ensisijaiseksi.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-151">Only one address can be marked as the primary.</span></span> <span data-ttu-id="b1b0a-152">Jos toinen osoite on jo merkitty ensisijaiseksi osoitteeksi, sinun on vahvistettava, että haluat käyttää tätä osoitetta ensisijaisena.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-152">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="b1b0a-153">Vaihtoehtoisesti voit valita yksityisen osoitteen **yksityiselle** kentälle.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-153">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="b1b0a-154">Vain käyttäjät, joilla on nimenomainen oikeus tarkastella yksityisiä osoitetietoja, voivat tarkastella tätä osoitetta.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-154">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="b1b0a-155">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-155">Select **OK**.</span></span>
 
## <a name="create-a-future-change-for-an-address"></a><span data-ttu-id="b1b0a-156">Osoitteen tulevan muutoksen luominen</span><span class="sxs-lookup"><span data-stu-id="b1b0a-156">Create a future change for an address</span></span>

<span data-ttu-id="b1b0a-157">Joissakin tapauksissa saatat haluta päivittää osoitteen muuttumaan tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-157">In some cases, you might want to update an address to change in the future.</span></span> <span data-ttu-id="b1b0a-158">Tämä on hyödyllistä esimerkiksi silloin, kun työntekijä muuttaa seuraavan kuukauden 15. päivänä.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-158">For example, this would be useful if an employee is moving on the 15th of the following month.</span></span>

1. <span data-ttu-id="b1b0a-159">Avaa **Hallitse osoitteita** -sivu valitsemalla **Lisää asetuksia > Lisäasetukset** mistä tahansa osoiteruudukosta.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-159">Open the **Manage addresses** page by selecting **More options > Advanced** from any address grid.</span></span>

2. <span data-ttu-id="b1b0a-160">Luo uusi osoite valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-160">Select **New** to create a new address.</span></span>

3. <span data-ttu-id="b1b0a-161">Voit kirjoittaa osoitteen tiedot.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-161">Enter the details of the address.</span></span>

4. <span data-ttu-id="b1b0a-162">Valitse **Yleinen**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-162">Select the **General** FastTab.</span></span>

5. <span data-ttu-id="b1b0a-163">Valitse **voimaantulopäivämäärä**-kentässä uuden osoitteen voimaantulopäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-163">In the **Effective date** field, select the date the new address will be effective.</span></span>

6. <span data-ttu-id="b1b0a-164">Valitse **vanhentumispäivämäärä** -kentästä, milloin osoite ei enää ole voimassa.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-164">In the **Expiration date** field, optionally select when the address will no longer be effective.</span></span>

7. <span data-ttu-id="b1b0a-165">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-165">Close the pages.</span></span>

## <a name="view-and-monitor-address-changes"></a><span data-ttu-id="b1b0a-166">Osoitemuutosten tarkasteleminen ja seuranta</span><span class="sxs-lookup"><span data-stu-id="b1b0a-166">View and monitor address changes</span></span>

<span data-ttu-id="b1b0a-167">Henkilöstöhallinnon henkilöstö voi tarkastella ja seurata osoitemuutoksia **henkilöstönhallinta**-työtilassa.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-167">HR personnel can view and monitor address changes from the **Personnel management** workspace.</span></span> <span data-ttu-id="b1b0a-168">Jos haluat tarkastella osoitteenmuutoksia, avaa **henkilöstöhallinto**-ruutu **Aloitussivulta**.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-168">To view the address changes, open the **Personnel management** tile from the **Home** page.</span></span> <span data-ttu-id="b1b0a-169">Osoitteenmuutokset näkyvät ruudun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-169">The address changes display on a tile in the upper-right corner.</span></span> <span data-ttu-id="b1b0a-170">Osoitteen yläpuolella oleva numero ilmaisee, kuinka monta **osoitemuutosta** on tapahtunut **henkilöstö hallinnon parametrit** -sivulla määritettyjen päivien määrän aikana.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-170">The number above **Address changes** shows how many address changes occurred in the number of days specified in the **Human resources parameters** page.</span></span> 

<span data-ttu-id="b1b0a-171">Kun valitset **osoitteenmuutokset**-ruudun, uusi sivu näyttää osoitteenmuutosten tiedot.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-171">When you select the **Address changes** tile, a new page displays the details of any address changes.</span></span> <span data-ttu-id="b1b0a-172">Voit halutessasi valita **Sisällytä tulevia osoitemuutoksia** oikeassa yläkulmassa, jolloin osoitteenmuutokset tulevat näkyviin myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-172">You can optionally select **Include future address changes** in the upper-right corner to display address changes with a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="b1b0a-173">Jos haluat saada hälytyksen tai sähköpostiviestin näistä osoitemuutoksista, voit luoda uuden hälytyssäännön toimintoruudun **asetukset**-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-173">If you want to receive an alert or email about these address changes, you can create a new alert rule on the **Options** tab in the Action Pane.</span></span> <span data-ttu-id="b1b0a-174">Lisätietoja hälytyssäännöistä on kohdassa [Hälytyssääntöjen luominen](/fin-ops-core/fin-ops/get-started/create-alert-rules.md).</span><span class="sxs-lookup"><span data-stu-id="b1b0a-174">For more information about alert rules, see [Create alert rules](/fin-ops-core/fin-ops/get-started/create-alert-rules.md).</span></span><br><br>

> <span data-ttu-id="b1b0a-175">Jos haluat määrittää työnkulun osoitemuutoksille, voit valita hälytyssäännössä **Lähetä ulkoisesti** -vaihtoehdon ja Power Automate käynnistää sitten liiketoimintatapahtuman ja määrittää työnkulun.</span><span class="sxs-lookup"><span data-stu-id="b1b0a-175">If you want to configure a workflow for the address changes, you can select the **Send externally** option on your alert rule, and then use Power Automate to trigger the business event and configure a workflow.</span></span> <span data-ttu-id="b1b0a-176">Lisätietoja on kohdassa [hälytykset liiketoimintatapahtumina](/fin-ops-core/dev-itpro/business-events/alerts-business-events.md).</span><span class="sxs-lookup"><span data-stu-id="b1b0a-176">For more information, see [Alerts as business events](/fin-ops-core/dev-itpro/business-events/alerts-business-events.md).</span></span>
