---
title: Dynamics 365 Human Resources -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 13, 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja.
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 711cc4491024e647429b108438ce1d88483ea63c
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259814"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="edab4-103">Dynamics 365 Human Resources -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 13, 2020)</span><span class="sxs-lookup"><span data-stu-id="edab4-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

<span data-ttu-id="edab4-104">Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="edab4-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="edab4-105">Muutokset koskevat koontiversion numeroa 8.1.3136.</span><span class="sxs-lookup"><span data-stu-id="edab4-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="edab4-106">Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.</span><span class="sxs-lookup"><span data-stu-id="edab4-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="edab4-107">Uusi tuotantojulkaisunopeus</span><span class="sxs-lookup"><span data-stu-id="edab4-107">New production release cadence</span></span>

<span data-ttu-id="edab4-108">Tämän viikon julkaisun myötä henkilöresurssien julkaisurytmi siirtyy viikoittaisesta päivityksestä kahden viikon välein tapahtuvaan päivitykseen.</span><span class="sxs-lookup"><span data-stu-id="edab4-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="edab4-109">Kaikkien alueiden palvelupäivitysten käyttöönottoprosessi kestää nyt kaksi viikkoa, jotta varmistetaan yhdenmukaisuus turvallisten käyttöönottokäytäntöjen kanssa ja ylläpidetään palvelun korkeaa vakautta ja luotettavuutta.</span><span class="sxs-lookup"><span data-stu-id="edab4-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="edab4-110">Lisätestit ja -näytöt ovat käytössä, jotta varmistetaan onnistunut käyttöönotto prosessin kaikissa vaiheissa.</span><span class="sxs-lookup"><span data-stu-id="edab4-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="edab4-111">Lisätietoja julkaisurytmin prosessista on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="edab4-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="edab4-112">Pyöristystarkkuus-kenttää ei voi muokata pyöristystyypin määrittämisen jälkeen (435616)</span><span class="sxs-lookup"><span data-stu-id="edab4-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="edab4-113">Tämän muutoksen yhteydessä **Pyöristystarkkuus**-kenttä on nyt käytettävissä **Pyöristystyyppi**-kentän päivittämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="edab4-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="edab4-114">Loman rekisteröinti päättymispäivämäärää ei voi muokata, jos lomasuunnitelmassa ei ole jaksotuskausia (413628)</span><span class="sxs-lookup"><span data-stu-id="edab4-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="edab4-115">Voit nyt muokata rekisteröinnin päättymispäivämäärää saamatta virhettä Kentän jaksotuspäivämäärän peruste on täytettävä.</span><span class="sxs-lookup"><span data-stu-id="edab4-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a><span data-ttu-id="edab4-116">Työyksikkö ei synkronoi kohteeseen Common Data Service (430834)</span><span class="sxs-lookup"><span data-stu-id="edab4-116">Employment entity doesn't sync to Common Data Service (430834)</span></span>

<span data-ttu-id="edab4-117">Tämä muutos korjaa ongelman, jossa työsuhteen tiedot eivät synkronoidu Common Data Serviceen taloushallinnon dimensioiden lisäämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="edab4-117">This change corrects an issue where the employment data wasn't syncing to Common Data Service after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="edab4-118">Työkalenterin aikavälin yksikön usean ylätason poistaminen (431775)</span><span class="sxs-lookup"><span data-stu-id="edab4-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="edab4-119">Tämä muutos poistaa **Työkalenterin aikavälin** -yksikön useat ylätasot.</span><span class="sxs-lookup"><span data-stu-id="edab4-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="edab4-120">Suodatus CAST-toiminnolla ei toimi OData-puhelun toimityöntekijän määritysyksikössä (431699)</span><span class="sxs-lookup"><span data-stu-id="edab4-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="edab4-121">Tämä päivitys sisältää muutoksen, jonka mukaan **Toimen työntekijän tehtävä** -kohteen OData-suodattimelle sallitaan CAST-toiminto.</span><span class="sxs-lookup"><span data-stu-id="edab4-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="edab4-122">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="edab4-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="edab4-123">Loman keskeytys</span><span class="sxs-lookup"><span data-stu-id="edab4-123">Leave suspension</span></span>

<span data-ttu-id="edab4-124">Voit keskeyttää työntekijän loman ja poissaolon henkilöstöhallinnossa.</span><span class="sxs-lookup"><span data-stu-id="edab4-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="edab4-125">Loman keskeyttäminen pysäyttää valittujen lomatyyppien lomajaksotukset.</span><span class="sxs-lookup"><span data-stu-id="edab4-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="edab4-126">Jos keskeytys tapahtuu jaksotuksen käsittelyn jälkeen, loman keskeyttäminen luo suhteutetun oikaisun työntekijän lomasaldoon.</span><span class="sxs-lookup"><span data-stu-id="edab4-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="edab4-127">Lisätietoja on kohdassa [Loman keskeytys](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="edab4-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="edab4-128">Siirtokirjauksen suorituksen säännöt</span><span class="sxs-lookup"><span data-stu-id="edab4-128">Carry forward rules</span></span>

<span data-ttu-id="edab4-129">Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään.</span><span class="sxs-lookup"><span data-stu-id="edab4-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="edab4-130">Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi.</span><span class="sxs-lookup"><span data-stu-id="edab4-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="edab4-131">Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="edab4-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="edab4-132">Tunnetut ongelmat</span><span class="sxs-lookup"><span data-stu-id="edab4-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="edab4-133">Työsuhteen tiedot -yksikkö</span><span class="sxs-lookup"><span data-stu-id="edab4-133">Employment Details entity</span></span>

<span data-ttu-id="edab4-134">**Työsuhteen tiedot** -yksikköön on päivitetty seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="edab4-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="edab4-135">**Maksutiheys**</span><span class="sxs-lookup"><span data-stu-id="edab4-135">**PayFrequency**</span></span>
- <span data-ttu-id="edab4-136">**Työsuhdeluokan tunnus**</span><span class="sxs-lookup"><span data-stu-id="edab4-136">**Employment Category ID**</span></span>
- <span data-ttu-id="edab4-137">**Työsuhteen tyyppi**</span><span class="sxs-lookup"><span data-stu-id="edab4-137">**Employment Type**</span></span>
- <span data-ttu-id="edab4-138">**Työsuhteen tyypin tunnus**</span><span class="sxs-lookup"><span data-stu-id="edab4-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="edab4-139">**Etujen työllisyystila**</span><span class="sxs-lookup"><span data-stu-id="edab4-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="edab4-140">Näiden kenttien asetustiedot perustuvat siihen, että **Ominaisuuksien hallinta**-työtilassa otetaan käyttöön toimintojen hallinta.</span><span class="sxs-lookup"><span data-stu-id="edab4-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="edab4-141">Älä täytä tai päivitä näitä kenttiä **Työsuhteen tiedot** -yksiköstä, koska ne aiheuttavat virheitä tuonnin aikana.</span><span class="sxs-lookup"><span data-stu-id="edab4-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="edab4-142">SharePoint-esikatselu ei toimi joissakin ympäristöissä</span><span class="sxs-lookup"><span data-stu-id="edab4-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="edab4-143">Jos SharePoint-ohjelmassa tallennettujen asiakirjojen esikatselu ei toimi, kokeile seuraavia toimia:</span><span class="sxs-lookup"><span data-stu-id="edab4-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="edab4-144">Tarkista, että järjestelmänvalvojakäyttäjätilillä on käyttäjätietueeseen liittyvä sähköpostiviesti.</span><span class="sxs-lookup"><span data-stu-id="edab4-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="edab4-145">Voit tarkastella näitä tietoja **Käyttäjä**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="edab4-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="edab4-146">Jos sähköpostia ei ole määritetty, sähköposti ja palveluntarjoaja on lisättävä OData Excel-lisäosaasi.</span><span class="sxs-lookup"><span data-stu-id="edab4-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="edab4-147">Oletusarvon mukaan sähköpostiosoitetta ei ole Excelin suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="edab4-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="edab4-148">Sinun on muokattava Excelin rakennetta, lisättävä kaikki kentät, otettava käyttöön ja päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="edab4-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="edab4-149">Kun olet tehnyt nämä vaiheet, voit päivittää järjestelmänvalvojatilin.</span><span class="sxs-lookup"><span data-stu-id="edab4-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="edab4-150">Kun järjestelmänvalvojatiliin on liitetty sähköpostitili, kirjaudu henkilöstöresursseihin järjestelmänvalvojan tunnistetiedoilla.</span><span class="sxs-lookup"><span data-stu-id="edab4-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="edab4-151">Avaa tiedoston esikatselu SharePoint-sovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="edab4-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="edab4-152">Kirjaudu sisään toisella käyttäjätilillä, jolla on liitteiden käyttöoikeus, ja varmista, että esikatselu toimii odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="edab4-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>