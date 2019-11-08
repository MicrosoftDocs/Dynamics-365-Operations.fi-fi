---
title: Mobiililaskujen hyväksynnät
description: Tämä aihe on tarkoitettu antamaan käytännön lähestymistavan mobiiliskenaarioiden suunnitteluun ottamalla toimittajan laskujen mobiilihyväksynnän esimerkkitapaukseksi.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dd72c8a54498cc6ffae7125c5c2f44bfac5a5995
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658641"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="873d8-103">Mobiililaskujen hyväksynnät</span><span class="sxs-lookup"><span data-stu-id="873d8-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="873d8-104">Mobiiliominaisuuksien avulla liiketoimintakäyttäjät voivat suunnitella mobiilin käyttökokemuksen.</span><span class="sxs-lookup"><span data-stu-id="873d8-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="873d8-105">Vaativimmissa skenaarioissa ympäristö sallii myös, että kehittäjät laajentavat ominaisuuksia kuin haluavat.</span><span class="sxs-lookup"><span data-stu-id="873d8-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="873d8-106">Tehokkain keino oppia joitakin uusia käsitteitä mobiiliympäristössä on käydä läpi joitakin suunnittelutilanteita.</span><span class="sxs-lookup"><span data-stu-id="873d8-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="873d8-107">Tämä aihe on tarkoitettu antamaan käytännön lähestymistavan mobiiliskenaarioiden suunnitteluun ottamalla toimittajan laskujen mobiilihyväksynnän esimerkkitapaukseksi.</span><span class="sxs-lookup"><span data-stu-id="873d8-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="873d8-108">Tämä ohjeaihe auttaa sinua suunnittelemaan tilanteen muita variaatioita ja sitä voidaan soveltaa myös muihin tilanteisiin, jotka eivät liity toimittajan laskuihin.</span><span class="sxs-lookup"><span data-stu-id="873d8-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="873d8-109">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="873d8-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="873d8-110">Edellytys</span><span class="sxs-lookup"><span data-stu-id="873d8-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="873d8-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="873d8-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="873d8-112">Mobiilikäsikirja esitiedoiksi</span><span class="sxs-lookup"><span data-stu-id="873d8-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="873d8-113">Mobiiliympäristö</span><span class="sxs-lookup"><span data-stu-id="873d8-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="873d8-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="873d8-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="873d8-115">Ympäristö, johon on asennettu in versio 1611 ja Platform update 3 (marraskuu 2016)</span><span class="sxs-lookup"><span data-stu-id="873d8-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="873d8-116">Asenna hotfix-korjaus KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="873d8-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="873d8-117">Tehtävän tallennus voit virheellisesti tallentaa kaksi avattavan luettelon Sulje-komentoa. Tämä sisältyy Platform update 3:een (marraskuun 2016 päivitys).</span><span class="sxs-lookup"><span data-stu-id="873d8-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="873d8-118">Asenna hotfix-korjaus KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="873d8-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="873d8-119">Tämän päivityksen avulla liitteitä voi tarkastella mobiiliasiakkaassa. Tämä sisältyy Platform update 3:een (marraskuun 2016 päivitys).</span><span class="sxs-lookup"><span data-stu-id="873d8-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="873d8-120">Asenna hotfix-korjaus KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="873d8-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="873d8-121">Sovelluskoodi toimittajan laskujen hyväksynnän mobiilisovellukselle. Tämä sisältyy versioon 7.0.1 (toukokuu 2016).</span><span class="sxs-lookup"><span data-stu-id="873d8-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="873d8-122">Android-, iOS- tai Windows-laite, jossa on asennettuna mobiilisovellus.</span><span class="sxs-lookup"><span data-stu-id="873d8-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="873d8-123">Etsi sovellus omasta sovelluskaupastasi.</span><span class="sxs-lookup"><span data-stu-id="873d8-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="873d8-124">Johdanto</span><span class="sxs-lookup"><span data-stu-id="873d8-124">Introduction</span></span>
<span data-ttu-id="873d8-125">Toimittajalaskujen mobiilihyväksyntä vaatii nämä kolme hotfix-korjausta, jotka on mainittu "Edellytykset"-osassa.</span><span class="sxs-lookup"><span data-stu-id="873d8-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="873d8-126">Nämä hotfix-korjaukset eivät tarjoa työtilaa laskujen hyväksyntään.</span><span class="sxs-lookup"><span data-stu-id="873d8-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="873d8-127">Perustiedot työtiloista mobiiliympäristössä on mobiilikäsikirjassa, joka mainitaan "Edellytykset"-osassa.</span><span class="sxs-lookup"><span data-stu-id="873d8-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="873d8-128">Laskun hyväksynnän työtila on suunniteltava.</span><span class="sxs-lookup"><span data-stu-id="873d8-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="873d8-129">Jokainen organisaatio määrittää oman toimittajan laskujen liiketoimintaprosessinsa eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="873d8-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="873d8-130">Ennen kuin suunnittelet toimittajan laskujen hyväksynnän mobiilikäyttöliittymän, sinun kannattaa harkita seuraavia näkökohtia liiketoimintaprosesseista.</span><span class="sxs-lookup"><span data-stu-id="873d8-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="873d8-131">Ajatuksena on käyttää näitä tietopisteitä mahdollisimman paljon laitteen käyttäjäkokemuksen parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="873d8-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="873d8-132">Mitkä laskun otsikon kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</span><span class="sxs-lookup"><span data-stu-id="873d8-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="873d8-133">Mitkä laskurivien kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</span><span class="sxs-lookup"><span data-stu-id="873d8-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="873d8-134">Kuinka monta laskuriviä yhdessä laskussa on?</span><span class="sxs-lookup"><span data-stu-id="873d8-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="873d8-135">Käytä tässä 80-20-sääntö ja optimoi tärkeimmät 80 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="873d8-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="873d8-136">Haluavatko käyttäjät tarkastella mobiililaitteessa kirjanpidollisia jakoja (laskujen koodausta) tarkistusten aikana?</span><span class="sxs-lookup"><span data-stu-id="873d8-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="873d8-137">Jos vastaus tähän kysymykseen on kyllä, harkitse seuraavia kysymyksiä:</span><span class="sxs-lookup"><span data-stu-id="873d8-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="873d8-138">Kuinka monta kirjanpidollista jakoa (laajennettua hintaa, arvonlisäveroa, kulua, jakoa jne.) on yhdellä laskurivillä?</span><span class="sxs-lookup"><span data-stu-id="873d8-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="873d8-139">Käytä uudelleen 80-20-sääntöä.</span><span class="sxs-lookup"><span data-stu-id="873d8-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="873d8-140">Onko laskuissa myös kirjanpidolliset jaot laskuotsikossa?</span><span class="sxs-lookup"><span data-stu-id="873d8-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="873d8-141">Jos näin on, ovatko nämä kirjanpidolliset jaot on käytettävissä laitteessa?</span><span class="sxs-lookup"><span data-stu-id="873d8-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="873d8-142">Tässä ohjeaiheessa ei kerrota, kuinka muokkaa kirjanpidon jakoja, koska tätä toimintoa ei tueta tällä hetkellä mobiiliskenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="873d8-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="873d8-143">Haluavatko käyttäjät nähdä laskun liitteet laitteella?</span><span class="sxs-lookup"><span data-stu-id="873d8-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="873d8-144">Laskun hyväksyntöjen mobiilikokemuksen rakenne vaihtelee riippuen vastauksista näihin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="873d8-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="873d8-145">Tavoitteena on optimoida organisaation liiketoimintaprosessin mobiilikäyttökokemus.</span><span class="sxs-lookup"><span data-stu-id="873d8-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="873d8-146">Aiheen loppuosassa tarkastelemme kahta skenaarion versiota, jotka perustuvat eri vastauksiin edellisiin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="873d8-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="873d8-147">Yleisenä ohjeena voi sanoa, että kun työskentelet mobiilisuunnittelijan kanssa, muista julkaista muutokset, jotta päivityksiä ei menetettäisi.</span><span class="sxs-lookup"><span data-stu-id="873d8-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="873d8-148">Yksinkertaisen laskun hyväksynnän skenaarion suunnitteleminen Contosolle</span><span class="sxs-lookup"><span data-stu-id="873d8-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="873d8-149">Skenaarion määrite</span><span class="sxs-lookup"><span data-stu-id="873d8-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="873d8-150">Vastaus</span><span class="sxs-lookup"><span data-stu-id="873d8-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="873d8-151">Mitkä laskun otsikon kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</span><span class="sxs-lookup"><span data-stu-id="873d8-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="873d8-152">Toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="873d8-152">Vendor name</span></span></li>
<li><span data-ttu-id="873d8-153">Laskun kokonaissumma</span><span class="sxs-lookup"><span data-stu-id="873d8-153">Invoice total</span></span></li>
<li><span data-ttu-id="873d8-154">Laskutusasiakasnumero</span><span class="sxs-lookup"><span data-stu-id="873d8-154">Invoice account</span></span></li>
<li><span data-ttu-id="873d8-155">Laskun numero</span><span class="sxs-lookup"><span data-stu-id="873d8-155">Invoice number</span></span></li>
<li><span data-ttu-id="873d8-156">Laskun päivämäärä</span><span class="sxs-lookup"><span data-stu-id="873d8-156">Invoice date</span></span></li>
<li><span data-ttu-id="873d8-157">Laskun kuvaus</span><span class="sxs-lookup"><span data-stu-id="873d8-157">Invoice description</span></span></li>
<li><span data-ttu-id="873d8-158">Eräpäivä</span><span class="sxs-lookup"><span data-stu-id="873d8-158">Due date</span></span></li>
<li><span data-ttu-id="873d8-159">Laskutusvaluutta</span><span class="sxs-lookup"><span data-stu-id="873d8-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="873d8-160">Mitkä laskurivien kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</span><span class="sxs-lookup"><span data-stu-id="873d8-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="873d8-161">Hankintaluokka</span><span class="sxs-lookup"><span data-stu-id="873d8-161">Procurement category</span></span></li>
<li><span data-ttu-id="873d8-162">Määrä</span><span class="sxs-lookup"><span data-stu-id="873d8-162">Quantity</span></span></li>
<li><span data-ttu-id="873d8-163">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="873d8-163">Unit price</span></span></li>
<li><span data-ttu-id="873d8-164">Rivin nettosumma</span><span class="sxs-lookup"><span data-stu-id="873d8-164">Line net amount</span></span></li>
<li><span data-ttu-id="873d8-165">Valmisteveron määrä</span><span class="sxs-lookup"><span data-stu-id="873d8-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="873d8-166">Kuinka monta laskuriviä yhdessä laskussa on?</span><span class="sxs-lookup"><span data-stu-id="873d8-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="873d8-167">Käytä tässä 80-20-sääntö ja optimoi tärkeimmät 80 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="873d8-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="873d8-168">1</span><span class="sxs-lookup"><span data-stu-id="873d8-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="873d8-169">Haluavatko käyttäjät tarkastella mobiililaitteessa kirjanpidollisia jakoja (laskujen koodausta) tarkistusten aikana?</span><span class="sxs-lookup"><span data-stu-id="873d8-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="873d8-170">Kyllä</span><span class="sxs-lookup"><span data-stu-id="873d8-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="873d8-171">Kuinka monta kirjanpidollista jakoa (laajennettua hintaa, arvonlisäveroa, kulua jne.) on yhdellä laskurivillä?</span><span class="sxs-lookup"><span data-stu-id="873d8-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="873d8-172">Käytä uudelleen 80-20-sääntöä.</span><span class="sxs-lookup"><span data-stu-id="873d8-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="873d8-173">Laajennettu hinta: 2 ALV: 0 Kulut: 0</span><span class="sxs-lookup"><span data-stu-id="873d8-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="873d8-174">Onko laskuissa myös kirjanpidolliset jaot laskuotsikossa?</span><span class="sxs-lookup"><span data-stu-id="873d8-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="873d8-175">Jos näin on, ovatko nämä kirjanpidolliset jaot on käytettävissä laitteessa?</span><span class="sxs-lookup"><span data-stu-id="873d8-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="873d8-176">Ei käytössä</span><span class="sxs-lookup"><span data-stu-id="873d8-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="873d8-177">Haluavatko käyttäjät nähdä laskun liitteet laitteella?</span><span class="sxs-lookup"><span data-stu-id="873d8-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="873d8-178">Kyllä</span><span class="sxs-lookup"><span data-stu-id="873d8-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="873d8-179">Luo työtila</span><span class="sxs-lookup"><span data-stu-id="873d8-179">Create the workspace</span></span>

1.  <span data-ttu-id="873d8-180">Selaimessa ja kirjaudu sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="873d8-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="873d8-181">Kun olet kirjautunut sisään, lisää **&mode=mobile** URL-osoitteeseen (kuten seuraavassa esimerkissä) ja päivitä sivu: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="873d8-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="873d8-182">Valitse **Asetukset** (ratas) -painike oikeassa yläkulmassa ja valitse sitten **Mobiilisovellus**.</span><span class="sxs-lookup"><span data-stu-id="873d8-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="873d8-183">Mobiilisovelluksen suunnitteluohjelma pitäisi tulla näkyviin samoin kuin tehtävän tallennustoiminto.</span><span class="sxs-lookup"><span data-stu-id="873d8-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="873d8-184">Luo uusi työtila napsauttamalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="873d8-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="873d8-185">Kirjoita tässä esimerkissä työtilan nimeksi **Omat hyväksynnät**.</span><span class="sxs-lookup"><span data-stu-id="873d8-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="873d8-186">Anna kuvaus.</span><span class="sxs-lookup"><span data-stu-id="873d8-186">Enter a description.</span></span>
6.  <span data-ttu-id="873d8-187">Valitse työtilan väri.</span><span class="sxs-lookup"><span data-stu-id="873d8-187">Select a workspace color.</span></span> <span data-ttu-id="873d8-188">Työtilan väriä käytetään tämän työtilan yleisenä tyylinä mobiilikokemuksessa.</span><span class="sxs-lookup"><span data-stu-id="873d8-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="873d8-189">Valitse työtilan kuvake.</span><span class="sxs-lookup"><span data-stu-id="873d8-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="873d8-190">Valitse **Valmis**</span><span class="sxs-lookup"><span data-stu-id="873d8-190">Click **Done**</span></span>
9.  <span data-ttu-id="873d8-191">Tallenna muutokset valitsemalla **Julkaise työtila**</span><span class="sxs-lookup"><span data-stu-id="873d8-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="873d8-192">Minulle määritetyt toimittajien laskut</span><span class="sxs-lookup"><span data-stu-id="873d8-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="873d8-193">Ensimmäinen mobiilisivu, joka tulee suunnitella, on luettelo laskuista, jotka on määritetty käyttäjälle tarkistettavaksi.</span><span class="sxs-lookup"><span data-stu-id="873d8-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="873d8-194">Voit suunnitella tämän mobiilisivun **VendMobileInvoiceAssignedToMeListPage**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="873d8-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="873d8-195">Ennen kuin suoritat nämä toimet, varmista, että vähintään yksi toimittajalasku on määritetty itsellesi tarkistettavaksi, ja että laskurivillä on kaksi jakoa.</span><span class="sxs-lookup"><span data-stu-id="873d8-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="873d8-196">Tämä määritys täyttää tämän skenaarion vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="873d8-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="873d8-197">Korvaa URL-osoitteessa valikkovaihtoehdon nimi merkkijonolla **VendMobileInvoiceAssignedToMeListPage**, jos haluat avata **Minulle määritetyt odottavat toimittajan laskut** -luettelosivun mobiiliversion **Ostoreskontra**-moduulissa.</span><span class="sxs-lookup"><span data-stu-id="873d8-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="873d8-198">Tässä sivussa näkyvät ne laskut, jotka on järjestelmässä liitetty sinulle.</span><span class="sxs-lookup"><span data-stu-id="873d8-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="873d8-199">Voit etsiä tietyn laskun käyttämällä suodatinta vasemmalla puolella.</span><span class="sxs-lookup"><span data-stu-id="873d8-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="873d8-200">Kuitenkaan tässä esimerkissä ei edellytetä tiettyä laskua.</span><span class="sxs-lookup"><span data-stu-id="873d8-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="873d8-201">Tarvitset vain jonkin sinulle määritetyn laskun, jonka avulla voit suunnitella mobiilisivun.</span><span class="sxs-lookup"><span data-stu-id="873d8-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="873d8-202">Käytettävissä olevat uudet sivut on suunniteltu erityisesti kehittämään mobiiliskenaarioita toimittajalaskuille.</span><span class="sxs-lookup"><span data-stu-id="873d8-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="873d8-203">Siksi sinun on käytettävä näitä sivuja.</span><span class="sxs-lookup"><span data-stu-id="873d8-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="873d8-204">URL-osoitteen pitäisi olla samantyyppinen seuraavan osoitteen kanssa, ja siihen siirryttyäsi sinun pitäisi nähdä oheisen kuvan mukainen sivu: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="873d8-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="873d8-205">[![Minulle määritettyjen odottavien toimittajalaskujen luettelosivu](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="873d8-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="873d8-206">Valitse **Asetukset** (ratas) -painike oikeassa yläkulmassa ja valitse sitten **Mobiilisovellus**.</span><span class="sxs-lookup"><span data-stu-id="873d8-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="873d8-207">Valitse työtila ja sitten **Muokkaa**</span><span class="sxs-lookup"><span data-stu-id="873d8-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="873d8-208">Valitse **Lisää sivu** luodaksesi ensimmäisen mobiilisivun.</span><span class="sxs-lookup"><span data-stu-id="873d8-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="873d8-209">Kirjoita nimi, kuten **Omat toimittajalaskut** sekä kuvaus, kuten **Minulle tarkistettavaksi määritetyt toimittajalaskut**.</span><span class="sxs-lookup"><span data-stu-id="873d8-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="873d8-210">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="873d8-210">Click **Done**.</span></span>
7.  <span data-ttu-id="873d8-211">Valitse mobiilisivujen suunnitteluohjelmassa **Kentät**-välilehdessä **Valitse kentät**.</span><span class="sxs-lookup"><span data-stu-id="873d8-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="873d8-212">Luettelosivun sarakkeiden tulisi olla likipitäen kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="873d8-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="873d8-213">[![Sarakkeet Minulle määritetyt odottavat toimittajan laskut -sivulla](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="873d8-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="873d8-214">Lisää tarvittavat sarakkeet luettelosivulta, joka on näytettävä käyttäjille mobiilisivulla.</span><span class="sxs-lookup"><span data-stu-id="873d8-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="873d8-215">Kentät näytetään loppukäyttäjille lisäämisjärjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="873d8-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="873d8-216">Ainoa tapa muuttaa kenttien järjestystä on valita kaikki kentät uudelleen.</span><span class="sxs-lookup"><span data-stu-id="873d8-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="873d8-217">Tämän skenaarion vaatimusten mukaan seuraavat kahdeksan kenttää ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="873d8-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="873d8-218">Joidenkin käyttäjien mielestä kahdeksan kenttää mobiililaitteessa saattaa kuitenkin olla liikaa.</span><span class="sxs-lookup"><span data-stu-id="873d8-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="873d8-219">Siksi näytämme vain tärkeimmät kentät mobiilissa luettelonäkymässä.</span><span class="sxs-lookup"><span data-stu-id="873d8-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="873d8-220">Muut kentät näkyvät tietonäkymässä, jonka suunnittelemme myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="873d8-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="873d8-221">Nyt lisäämme seuraavat kentät.</span><span class="sxs-lookup"><span data-stu-id="873d8-221">For now, we will add the following fields.</span></span> <span data-ttu-id="873d8-222">Napsauta plus-merkkiä (**+**) sarakkeissa lisätäksesi ne mobiilisivulle.</span><span class="sxs-lookup"><span data-stu-id="873d8-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="873d8-223">Toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="873d8-223">Vendor name</span></span>
    - <span data-ttu-id="873d8-224">Laskun kokonaissumma</span><span class="sxs-lookup"><span data-stu-id="873d8-224">Invoice total</span></span>
    - <span data-ttu-id="873d8-225">Laskutusasiakasnumero</span><span class="sxs-lookup"><span data-stu-id="873d8-225">Invoice account</span></span>
    - <span data-ttu-id="873d8-226">Laskun numero</span><span class="sxs-lookup"><span data-stu-id="873d8-226">Invoice number</span></span>
    - <span data-ttu-id="873d8-227">Laskun päivämäärä</span><span class="sxs-lookup"><span data-stu-id="873d8-227">Invoice date</span></span>

  <span data-ttu-id="873d8-228">Kun kentät on lisätty, mobiilisivun pitäisi muistuttaa seuraavaa kuvaa.</span><span class="sxs-lookup"><span data-stu-id="873d8-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
   <span data-ttu-id="873d8-229">[![Sivu kenttien lisäämisen jälkeen](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="873d8-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="873d8-230">On myös lisättävä seuraavat sarakkeet nyt, että voimme ottaa työnkulkutoimintoja myöhemmin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="873d8-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="873d8-231">Näytä Suorita-tehtävä</span><span class="sxs-lookup"><span data-stu-id="873d8-231">Show complete task</span></span>
    - <span data-ttu-id="873d8-232">Näytä Delegoi-tehtävä</span><span class="sxs-lookup"><span data-stu-id="873d8-232">Show delegate task</span></span>
    - <span data-ttu-id="873d8-233">Näytä Peruuta-tehtävä</span><span class="sxs-lookup"><span data-stu-id="873d8-233">Show recall task</span></span>
    - <span data-ttu-id="873d8-234">Näytä Hylkää-tehtävä</span><span class="sxs-lookup"><span data-stu-id="873d8-234">Show reject task</span></span>
    - <span data-ttu-id="873d8-235">Näytä Pyydä suoritusta -tehtävä</span><span class="sxs-lookup"><span data-stu-id="873d8-235">Show request completion task</span></span>
    - <span data-ttu-id="873d8-236">Näytä Lähetä uudelleen -tehtävä</span><span class="sxs-lookup"><span data-stu-id="873d8-236">Show resubmit task</span></span>

10. <span data-ttu-id="873d8-237">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="873d8-238">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="873d8-239">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="873d8-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="873d8-240">Ota käyttöön **Näytä laskun loppusumma odottavien toimittajalaskujen luettelossa** Ostoreskontran parametrit -lomakkeessa kohdassa **Lasku**.</span><span class="sxs-lookup"><span data-stu-id="873d8-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="873d8-241">Huomaa, että ainoastaan ottamalla käyttöön tämän parametrin laskun kokonaissumma lasketaan näytettäväksi odottavien toimittajan laskujen luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="873d8-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="873d8-242">Tämä on uusi ominaisuus, joka kuuluu vaadittuun hotfix-korjaukseen 3208224.</span><span class="sxs-lookup"><span data-stu-id="873d8-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="873d8-243">Toimittajan laskun tiedot</span><span class="sxs-lookup"><span data-stu-id="873d8-243">Vendor invoice details</span></span>

<span data-ttu-id="873d8-244">Voit suunnitella laskun tietojen sivun käyttämällä **VendMobileInvoiceHeaderDetails**-sivua.</span><span class="sxs-lookup"><span data-stu-id="873d8-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="873d8-245">Huomaa, että riippuen järjestelmässäsi olevien laskujen määrästä tällä sivulla näytetään vanhin lasku (lasku, joka on luotu ensin).</span><span class="sxs-lookup"><span data-stu-id="873d8-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="873d8-246">Voit etsiä tietyn laskun käyttämällä suodatinta vasemmalla puolella.</span><span class="sxs-lookup"><span data-stu-id="873d8-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="873d8-247">Kuitenkaan tässä esimerkissä ei edellytetä tiettyä laskua.</span><span class="sxs-lookup"><span data-stu-id="873d8-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="873d8-248">Tässä tarvitaan vain jotkin laskutiedot, että voimme suunnitella mobiilisivun.</span><span class="sxs-lookup"><span data-stu-id="873d8-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="873d8-249">[![Työnkulku-sivu](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="873d8-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="873d8-250">Korvaa URL-osoitteessa valikkovaihtoehto nimi merkkijonolla **VendMobileInvoiceHeaderDetails**, jos haluat avata lomakkeen</span><span class="sxs-lookup"><span data-stu-id="873d8-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="873d8-251">Avaa mobiilisivujen suunnitteluohjelma **Asetukset** (ratas) -painikkeesta.</span><span class="sxs-lookup"><span data-stu-id="873d8-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="873d8-252">Valitse **Muokkaa**-painike käynnistääksesi muokkaustilan työtilassa.</span><span class="sxs-lookup"><span data-stu-id="873d8-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="873d8-253">Valitse **Omat toimittajalaskut** -sivu, jonka loit aiemmin ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="873d8-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="873d8-254">Valitse **Kentät** -välilehdessä sarakkeen otsikko **Ruudukko**.</span><span class="sxs-lookup"><span data-stu-id="873d8-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="873d8-255">Valitse **Ominaisuudet &gt; Lisää sivu**.</span><span class="sxs-lookup"><span data-stu-id="873d8-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="873d8-256">**Huomautus:** Kun valitset **Ruudukko**-otsikon ja lisäät sivun, yhteys tietosivuun muodostetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="873d8-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="873d8-257">Kirjoita sivun otsikko, esimerkiksi **Laskun tiedot** ja kuvaus, kuten **Näytä laskun otsikko ja rivitiedot**.</span><span class="sxs-lookup"><span data-stu-id="873d8-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="873d8-258">Klikkaa **Valitse kentät**.</span><span class="sxs-lookup"><span data-stu-id="873d8-258">Click **Select fields**.</span></span> <span data-ttu-id="873d8-259">Huomaa, että kentät näytetään loppukäyttäjille lisäämisjärjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="873d8-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="873d8-260">Ainoa tapa muuttaa kenttien järjestystä on valita kaikki kentät uudelleen.</span><span class="sxs-lookup"><span data-stu-id="873d8-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="873d8-261">Lisää seuraavat kentät otsikosta tämän skenaarion vaatimusten mukaan:</span><span class="sxs-lookup"><span data-stu-id="873d8-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="873d8-262">Toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="873d8-262">Vendor name</span></span>
   - <span data-ttu-id="873d8-263">Laskun kokonaissumma</span><span class="sxs-lookup"><span data-stu-id="873d8-263">Invoice total</span></span>
   - <span data-ttu-id="873d8-264">Laskutusasiakasnumero</span><span class="sxs-lookup"><span data-stu-id="873d8-264">Invoice account</span></span>
   - <span data-ttu-id="873d8-265">Laskun numero</span><span class="sxs-lookup"><span data-stu-id="873d8-265">Invoice number</span></span>
   - <span data-ttu-id="873d8-266">Laskun päivämäärä</span><span class="sxs-lookup"><span data-stu-id="873d8-266">Invoice date</span></span>
   - <span data-ttu-id="873d8-267">Laskun kuvaus</span><span class="sxs-lookup"><span data-stu-id="873d8-267">Invoice description</span></span>
   - <span data-ttu-id="873d8-268">Eräpäivä</span><span class="sxs-lookup"><span data-stu-id="873d8-268">Due date</span></span>
   - <span data-ttu-id="873d8-269">Laskutusvaluutta</span><span class="sxs-lookup"><span data-stu-id="873d8-269">Invoice currency</span></span>

10. <span data-ttu-id="873d8-270">Lisää seuraavat kentät sivun riviruudukosta:</span><span class="sxs-lookup"><span data-stu-id="873d8-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="873d8-271">Hankintaluokka</span><span class="sxs-lookup"><span data-stu-id="873d8-271">Procurement category</span></span>
    - <span data-ttu-id="873d8-272">Määrä</span><span class="sxs-lookup"><span data-stu-id="873d8-272">Quantity</span></span>
    - <span data-ttu-id="873d8-273">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="873d8-273">Unit price</span></span>
    - <span data-ttu-id="873d8-274">Rivin nettosumma</span><span class="sxs-lookup"><span data-stu-id="873d8-274">Line net amount</span></span>
    - <span data-ttu-id="873d8-275">Valmisteveron määrä</span><span class="sxs-lookup"><span data-stu-id="873d8-275">1099 amount</span></span>

11. <span data-ttu-id="873d8-276">Kun kaikki edellisten kahden vaiheen kentät on lisätty, valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="873d8-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="873d8-277">Sivun tulisi olla likipitäen kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="873d8-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="873d8-278">[![Sivu kenttien lisäämisen jälkeen](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="873d8-278">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="873d8-279">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="873d8-280">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="873d8-281">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="873d8-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="873d8-282">Työnkulkutehtävät</span><span class="sxs-lookup"><span data-stu-id="873d8-282">Workflow actions</span></span>

<span data-ttu-id="873d8-283">Käytä **VendMobileInvoiceHeaderDetails**-sivua lisätäksesi työnkulkutoimintoja.</span><span class="sxs-lookup"><span data-stu-id="873d8-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="873d8-284">Jos haluat avata tämän sivun, korvaa valikkovaihtoehdon nimi URL-osoitteessa, kuten teit aikaisemmin.</span><span class="sxs-lookup"><span data-stu-id="873d8-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="873d8-285">Avaa sitten mobiilisivujen suunnitteluohjelma **Asetukset** (ratas) -painikkeesta.</span><span class="sxs-lookup"><span data-stu-id="873d8-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="873d8-286">Toimi seuraavien vaiheiden mukaisesti lisätäksesi työnkulkutoimintoja tietosivulle.</span><span class="sxs-lookup"><span data-stu-id="873d8-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="873d8-287">Sinulle on oltava määritettynä sopivassa tilassa olevia laskuja, joiden avulla pääset työnkulkutoimintoihin.</span><span class="sxs-lookup"><span data-stu-id="873d8-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="873d8-288">Työnkulkutoimintojen tallentaminen</span><span class="sxs-lookup"><span data-stu-id="873d8-288">Record workflow actions</span></span>
1.  <span data-ttu-id="873d8-289">Valitse **Muokkaa**-painike käynnistääksesi muokkaustilan työtilassa.</span><span class="sxs-lookup"><span data-stu-id="873d8-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="873d8-290">Valitse **Laskun tiedot** -sivu, jonka loit aiemmin ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="873d8-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="873d8-291">Valitse **Toiminnot**-välilehdessä **Lisää toiminto**.</span><span class="sxs-lookup"><span data-stu-id="873d8-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="873d8-292">Kirjoita toiminnon otsikko, esimerkiksi **Hyväksy** ja kuvaus, kuten **Hyväksy lasku**.</span><span class="sxs-lookup"><span data-stu-id="873d8-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="873d8-293">Huomaa, että tässä antamasi otsikko näkyy loppukäyttäjille toiminnon nimenä mobiilisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="873d8-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="873d8-294">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="873d8-294">Click **Done**.</span></span>
6.  <span data-ttu-id="873d8-295">Klikkaa **Valitse kentät**.</span><span class="sxs-lookup"><span data-stu-id="873d8-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="873d8-296">Siirry työnkulkuprosessin kautta **VendMobileInvoiceHeaderDetails**-sivulle ja suorita toiminto, jonka haluat tallentaa.</span><span class="sxs-lookup"><span data-stu-id="873d8-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="873d8-297">Varmista, että kirjoitat työnkulun kommentit tämän prosessin aikana, jotta kommenttikenttä sisältyy myös mobiilikokemukseen.</span><span class="sxs-lookup"><span data-stu-id="873d8-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="873d8-298">Kun työnkulkutoiminto on suoritettu, valitse **Valmis** viimeistelläksesi Valitse kentät -tehtävän.</span><span class="sxs-lookup"><span data-stu-id="873d8-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="873d8-299">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="873d8-300">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="873d8-301">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="873d8-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="873d8-302">Tallenna kaikki tarvittavat työnkulkutoiminnot toistamalla edelliset vaiheet.</span><span class="sxs-lookup"><span data-stu-id="873d8-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="873d8-303">.js-tiedoston luominen</span><span class="sxs-lookup"><span data-stu-id="873d8-303">Create a .js file</span></span>
1. <span data-ttu-id="873d8-304">Avaa Muistio tai Microsoft Visual Studio ja liitä seuraava koodi.</span><span class="sxs-lookup"><span data-stu-id="873d8-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="873d8-305">Tallenna tiedosto .js-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="873d8-305">Save the file as a .js file.</span></span> <span data-ttu-id="873d8-306">Koodilla voidaan suorittaa seuraavia toimintoja:</span><span class="sxs-lookup"><span data-stu-id="873d8-306">This code does the following:</span></span>
    - <span data-ttu-id="873d8-307">Se piilottaa ylimääräiset työnkulkuun liittyvät sarakkeet, jotka on lisätty aiemmin mobiililuettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="873d8-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="873d8-308">Lisäsimme nämä sarakkeet, jotta sovelluksella on nämä tiedot oikeassa asiayhteydessä, jotta se voi suorittaa seuraavan vaiheen.</span><span class="sxs-lookup"><span data-stu-id="873d8-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="873d8-309">Aktiiviseen työnkulun vaiheen perusteella se käyttää logiikkaa, joka näyttää vain kyseiset toiminnot.</span><span class="sxs-lookup"><span data-stu-id="873d8-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="873d8-310">Sivujen ja muiden ohjausobjektien nimet on oltava koodissa samat kuin työtilan nimet.</span><span class="sxs-lookup"><span data-stu-id="873d8-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  <span data-ttu-id="873d8-311">Lataa kooditiedoston työtilaan valitsemalla **Logiikka**-välilehti</span><span class="sxs-lookup"><span data-stu-id="873d8-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="873d8-312">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="873d8-313">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="873d8-314">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="873d8-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="873d8-315">Toimittajalaskujen liitteet</span><span class="sxs-lookup"><span data-stu-id="873d8-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="873d8-316">Valitse **Asetukset** (ratas) -painike oikeassa yläkulmassa ja valitse sitten **Mobiilisovellus**.</span><span class="sxs-lookup"><span data-stu-id="873d8-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="873d8-317">Valitse **Muokkaa**-painike käynnistääksesi muokkaustilan työtilassa.</span><span class="sxs-lookup"><span data-stu-id="873d8-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="873d8-318">Valitse <strong>Laskun tiedot \*\*-sivu, jonka loit aiemmin ja valitse sitten \*\*Muokkaa</strong>.</span><span class="sxs-lookup"><span data-stu-id="873d8-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="873d8-319">Määritä **Tiedostojen hallinta** -asetukseksi **Kyllä** alla olevan esimerkin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="873d8-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="873d8-320">**Huomautus:** Jos ei ole liitteitä ei ole tarpeen näyttää mobiililaitteessa, voit jättää tämän vaihtoehdon arvoksi **Ei**, joka on oletusasetus.</span><span class="sxs-lookup"><span data-stu-id="873d8-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![Tiedoston hallinta](./media/docmanagement-216x300.png)

5. <span data-ttu-id="873d8-322">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="873d8-323">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="873d8-324">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="873d8-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="873d8-325">Toimittajan laskujen rivijaot</span><span class="sxs-lookup"><span data-stu-id="873d8-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="873d8-326">Tämän skenaarion vaatimukset vahvistavat, että seillä on vain rivitason jaot ja että laskulla on aina vain yksi rivi.</span><span class="sxs-lookup"><span data-stu-id="873d8-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="873d8-327">Koska tämä skenaario on yksinkertainen, mobiililaitteen käyttökokemuksenkin täytyy olla yksinkertainen, jotta käyttäjän ei tarvitse porautua alaspäin useita tasoja nähdäkseen jaot.</span><span class="sxs-lookup"><span data-stu-id="873d8-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="873d8-328">Toimittajan laskuihin sisältyy mahdollisuus näyttää kaikki jaot laskun otsikosta.</span><span class="sxs-lookup"><span data-stu-id="873d8-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="873d8-329">Tämän kokemuksen tarvitsemme mobiiliskenaariossa.</span><span class="sxs-lookup"><span data-stu-id="873d8-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="873d8-330">Tämän vuoksi käytämme **VendMobileInvoiceAllDistributionTree**-sivua suunnittellaksemme mobiiliskenaarion tämän osan.</span><span class="sxs-lookup"><span data-stu-id="873d8-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="873d8-331">Kun tiedämme vaatimukset, se auttaa päättämään, mitä tiettyä sivua käyttää ja miten tarkalleen optimoida käyttäjän mobiilikokemus, kun suunnittelemme tätä skenaariota.</span><span class="sxs-lookup"><span data-stu-id="873d8-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="873d8-332">Toisessa tilanteessa käytämme toista sivua näyttämään jaot, koska skenaarioiden vaatimukset eroavat.</span><span class="sxs-lookup"><span data-stu-id="873d8-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="873d8-333">Korvaa valikkovaihtoehdon nimi URL-osoitteessa, kuten teit aikaisemmin.</span><span class="sxs-lookup"><span data-stu-id="873d8-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="873d8-334">Sivun, joka näkyy, on muistutettava seuraavaa kuvaa.</span><span class="sxs-lookup"><span data-stu-id="873d8-334">The page that appears should resemble the following illustration.</span></span>

<span data-ttu-id="873d8-335">[![Kaikki jaot -sivu](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="873d8-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="873d8-336">Avaa mobiilisivujen suunnitteluohjelma **Asetukset** (ratas) -painikkeesta.</span><span class="sxs-lookup"><span data-stu-id="873d8-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="873d8-337">Valitse **Muokkaa**-painike käynnistääksesi muokkaustilan työtilassa.</span><span class="sxs-lookup"><span data-stu-id="873d8-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="873d8-338">**Huomautus:** Näet, että kaksi uutta sivua on luotu automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="873d8-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="873d8-339">Järjestelmä luo nämä sivut, koska otit käyttöön tiedostojen hallinnan edellisessä osassa.</span><span class="sxs-lookup"><span data-stu-id="873d8-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="873d8-340">Voit ohittaa nämä uudet sivut.</span><span class="sxs-lookup"><span data-stu-id="873d8-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="873d8-341">Valitse **Lisää sivu**.</span><span class="sxs-lookup"><span data-stu-id="873d8-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="873d8-342">Kirjoita sivun otsikko, esimerkiksi **Näytä kirjanpito**  ja kuvaus, kuten **Näytä laskun kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="873d8-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="873d8-343">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="873d8-343">Click **Done**.</span></span>

7.  <span data-ttu-id="873d8-344">Klikkaa **Kentät**-välilehdessä **Valitse kentät**, valitse seuraavat kentät Jaot-sivulta ja valitse sitten **Valmis**:</span><span class="sxs-lookup"><span data-stu-id="873d8-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="873d8-345">Summa</span><span class="sxs-lookup"><span data-stu-id="873d8-345">Amount</span></span>
    2.  <span data-ttu-id="873d8-346">Valuutta</span><span class="sxs-lookup"><span data-stu-id="873d8-346">Currency</span></span>
    3.  <span data-ttu-id="873d8-347">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="873d8-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="873d8-348">Emme valinneet **Kuvaus**-saraketta jakoruudukosta, koska tämän skenaarion vaatimukset vahvistivat, että vain laajennetulle hinnalle on olemassa jako.</span><span class="sxs-lookup"><span data-stu-id="873d8-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="873d8-349">Tämän vuoksi käyttäjä ei edellytä toista kenttää sen summan tyypin määrittämiseksi, jolle jako on.</span><span class="sxs-lookup"><span data-stu-id="873d8-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="873d8-350">Kuitenkin seuraavassa skenaariossa me **tulemme** käyttämään tätä tietoa, koska tämän skenaarion vaatimukset määrittävät, että muuntyyppisilläkin summilla on jakoja (kuten arvonlisävero).</span><span class="sxs-lookup"><span data-stu-id="873d8-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="873d8-351">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="873d8-352">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="873d8-353">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="873d8-353">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="873d8-354">**Näytä kirjanpito** -mobiilisivua ei ole tällä hetkellä linkitetty yhteenkään tähän mennessä suunniteltuun mobiilisivuun.</span><span class="sxs-lookup"><span data-stu-id="873d8-354">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="873d8-355">Koska käyttäjän pitää voida siirtyä **Näytä kirjanpito** -sivulle mobiililaitteen **Laskun tiedot** -sivulta, meidän on luotava siirtyminen **Laskun tiedot** -sivulta **Näytä kirjanpito** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="873d8-355">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="873d8-356">Luomme tämän siirtymisen JavaScript-lisälogiikan avulla.</span><span class="sxs-lookup"><span data-stu-id="873d8-356">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="873d8-357">Avaa .js-tiedosto, jonka loit aiemmin ja lisää rivit, jotka näkyvät korostettuina seuraavassa koodissa.</span><span class="sxs-lookup"><span data-stu-id="873d8-357">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="873d8-358">Tämä koodi tekee kaksi asiaa:</span><span class="sxs-lookup"><span data-stu-id="873d8-358">This code does two things:</span></span>
    1.  <span data-ttu-id="873d8-359">Sen avulla varmistetaan, että käyttäjät eivät voi siirtyä suoraan työtilasta **Näytä kirjanpito** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="873d8-359">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="873d8-360">Se luo siirtymisen ohjausobjektin **Laskun tiedot** -sivulta **Näytä kirjanpito** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="873d8-360">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="873d8-361">Sivujen ja muiden ohjausobjektien nimet on oltava koodissa samat kuin työtilan nimet.</span><span class="sxs-lookup"><span data-stu-id="873d8-361">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  <span data-ttu-id="873d8-362">Lataa kooditiedosto työtilaan ja korvaa edellinen koodi valitsemalla **Logiikka**-välilehti</span><span class="sxs-lookup"><span data-stu-id="873d8-362">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="873d8-363">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-363">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="873d8-364">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="873d8-364">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="873d8-365">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="873d8-365">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="873d8-366">Valintasäännöt</span><span class="sxs-lookup"><span data-stu-id="873d8-366">Validation</span></span>

<span data-ttu-id="873d8-367">Avaa sovellus mobiililaitteessa ja muodosta yhteys esiintymään.</span><span class="sxs-lookup"><span data-stu-id="873d8-367">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="873d8-368">Varmista, että kirjaudut yritykseen jossa toimittajalaskuja on määritetty sinulle tarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="873d8-368">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="873d8-369">Sinun pitäisi voida suorittaa seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="873d8-369">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="873d8-370">Nähdä **Omat hyväksynnät** -työtila.</span><span class="sxs-lookup"><span data-stu-id="873d8-370">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="873d8-371">Porautua **Omat hyväksynnät** -työtilaan ja nähdä **Omat toimittajalaskut** -sivun.</span><span class="sxs-lookup"><span data-stu-id="873d8-371">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="873d8-372">Porautua **Omat toimittajalaskut** -sivulle ja nähdä sinulle määritetyt laskut.</span><span class="sxs-lookup"><span data-stu-id="873d8-372">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="873d8-373">Poraudu yhteen laskuista ja tarkastele laskun otsikon ja rivien tietoja.</span><span class="sxs-lookup"><span data-stu-id="873d8-373">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="873d8-374">Tiedot-sivulla näet linkin liitteisiin ja tämän linkin avulla voit siirtyä liiteluetteloon ja tarkastella liitteitä.</span><span class="sxs-lookup"><span data-stu-id="873d8-374">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="873d8-375">Tiedot-sivulla näet linkin **Näytä kirjanpito** -sivulle ja tämän linkin avulla voit siirtyä jakosivulle ja tarkastella jakoja.</span><span class="sxs-lookup"><span data-stu-id="873d8-375">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="873d8-376">Valitse Tiedot-sivulla **Toiminnot**-valikko sivun alaosasta ja suorita työnkulkutoimintoja, joita sovelletaan työnkulun vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="873d8-376">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="873d8-377">Monimutkaisen laskun hyväksynnän skenaarion suunnitteleminen Fabrikamille</span><span class="sxs-lookup"><span data-stu-id="873d8-377">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="873d8-378">Skenaarion määrite</span><span class="sxs-lookup"><span data-stu-id="873d8-378">Scenario attribute</span></span></th>
<th><span data-ttu-id="873d8-379">Vastaus</span><span class="sxs-lookup"><span data-stu-id="873d8-379">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="873d8-380">Mitkä laskun otsikon kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</span><span class="sxs-lookup"><span data-stu-id="873d8-380">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="873d8-381">Toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="873d8-381">Vendor name</span></span></li>
<li><span data-ttu-id="873d8-382">Laskun summa</span><span class="sxs-lookup"><span data-stu-id="873d8-382">Invoice amount</span></span></li>
<li><span data-ttu-id="873d8-383">Laskutusasiakasnumero</span><span class="sxs-lookup"><span data-stu-id="873d8-383">Invoice account</span></span></li>
<li><span data-ttu-id="873d8-384">Laskun numero</span><span class="sxs-lookup"><span data-stu-id="873d8-384">Invoice number</span></span></li>
<li><span data-ttu-id="873d8-385">Laskun päivämäärä</span><span class="sxs-lookup"><span data-stu-id="873d8-385">Invoice date</span></span></li>
<li><span data-ttu-id="873d8-386">Laskun kuvaus</span><span class="sxs-lookup"><span data-stu-id="873d8-386">Invoice description</span></span></li>
<li><span data-ttu-id="873d8-387">Eräpäivä</span><span class="sxs-lookup"><span data-stu-id="873d8-387">Due date</span></span></li>
<li><span data-ttu-id="873d8-388">Laskutusvaluutta</span><span class="sxs-lookup"><span data-stu-id="873d8-388">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="873d8-389">Mitkä laskurivien kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</span><span class="sxs-lookup"><span data-stu-id="873d8-389">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="873d8-390">Hankintaluokka</span><span class="sxs-lookup"><span data-stu-id="873d8-390">Procurement category</span></span></li>
<li><span data-ttu-id="873d8-391">Määrä</span><span class="sxs-lookup"><span data-stu-id="873d8-391">Quantity</span></span></li>
<li><span data-ttu-id="873d8-392">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="873d8-392">Unit price</span></span></li>
<li><span data-ttu-id="873d8-393">Rivin nettosumma</span><span class="sxs-lookup"><span data-stu-id="873d8-393">Line net amount</span></span></li>
<li><span data-ttu-id="873d8-394">Valmisteveron määrä</span><span class="sxs-lookup"><span data-stu-id="873d8-394">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="873d8-395">Kuinka monta laskuriviä yhdessä laskussa on?</span><span class="sxs-lookup"><span data-stu-id="873d8-395">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="873d8-396">Käytä tässä 80-20-sääntö ja optimoi tärkeimmät 80 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="873d8-396">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="873d8-397">5</span><span class="sxs-lookup"><span data-stu-id="873d8-397">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="873d8-398">Haluavatko käyttäjät tarkastella mobiililaitteessa kirjanpidollisia jakoja (laskujen koodausta) tarkistusten aikana?</span><span class="sxs-lookup"><span data-stu-id="873d8-398">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="873d8-399">Kyllä</span><span class="sxs-lookup"><span data-stu-id="873d8-399">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="873d8-400">Kuinka monta kirjanpidollista jakoa (laajennettua hintaa, arvonlisäveroa, kulua jne.) on yhdellä laskurivillä?</span><span class="sxs-lookup"><span data-stu-id="873d8-400">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="873d8-401">Käytä uudelleen 80-20-sääntöä.</span><span class="sxs-lookup"><span data-stu-id="873d8-401">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="873d8-402">Laajennettu hinta: 2 ALV: 2 Kulut: 2</span><span class="sxs-lookup"><span data-stu-id="873d8-402">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="873d8-403">Onko laskuissa myös kirjanpidolliset jaot laskuotsikossa?</span><span class="sxs-lookup"><span data-stu-id="873d8-403">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="873d8-404">Jos näin on, ovatko nämä kirjanpidolliset jaot on käytettävissä laitteessa?</span><span class="sxs-lookup"><span data-stu-id="873d8-404">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="873d8-405">Ei käytössä</span><span class="sxs-lookup"><span data-stu-id="873d8-405">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="873d8-406">Haluavatko käyttäjät nähdä laskun liitteet laitteella?</span><span class="sxs-lookup"><span data-stu-id="873d8-406">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="873d8-407">Kyllä</span><span class="sxs-lookup"><span data-stu-id="873d8-407">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="873d8-408">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="873d8-408">Next steps</span></span>

<span data-ttu-id="873d8-409">Skenaariolle 1 voidaan tehdä seuraavat muunnelmat perustuen skenaarion 2 vaatimuksiin.</span><span class="sxs-lookup"><span data-stu-id="873d8-409">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="873d8-410">Voit parantaa mobiilisovelluskokemusta tämän osan avulla.</span><span class="sxs-lookup"><span data-stu-id="873d8-410">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="873d8-411">Koska skenaariossa 2 odotetaan enemmän laskurivejä, seuraavat muutokset rakenteeseen auttavat optimoimaan mobiililaitteen käyttökokemusta:</span><span class="sxs-lookup"><span data-stu-id="873d8-411">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="873d8-412">Sen sijaan että tarkastelisit laskurivejä tietosivulla (kuten skenaariossa 1), käyttäjät voivat tarkastella rivejä erillisellä mobiilisivulla.</span><span class="sxs-lookup"><span data-stu-id="873d8-412">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="873d8-413">Koska tässä tilanteessa on odotettavissa useita laskun rivejä ja jos **VendMobileInvoiceAllDistributionTree** -sivua käytetään mobiilin jakosivun suunnittelussa (kuten skenaariossa 1), se voi olla hämmentävää käyttäjälle yhdistää rivit jakoihin.</span><span class="sxs-lookup"><span data-stu-id="873d8-413">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="873d8-414">Tämän vuoksi käytä **VendMobileInvoiceLineDistributionTree**-sivua jakosivun suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="873d8-414">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="873d8-415">Parhaassa tapauksessa tässä skenaariossa jaot pitäisi näyttää laskurivin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="873d8-415">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="873d8-416">Varmista siksi, että käyttäjä voi porautua riviin nähdäkseen jakosivun.</span><span class="sxs-lookup"><span data-stu-id="873d8-416">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="873d8-417">Sivulinkkiominaisuuden avulla voit määrittää porautumisen samalla tavalla kuin otsikko- ja tietosivuille skenaariossa 1.</span><span class="sxs-lookup"><span data-stu-id="873d8-417">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="873d8-418">Koska skenaariossa 2 on odotettavissa useita summatyyppejä (arvonlisävero, kulut jne.), on hyödyllistä näyttää summatyypin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="873d8-418">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="873d8-419">(Nämä tiedot jätettiin pois skenaariossa 1).</span><span class="sxs-lookup"><span data-stu-id="873d8-419">(We omitted this information in scenario 1.)</span></span>




