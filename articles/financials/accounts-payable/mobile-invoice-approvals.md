---
title: "Mobiililaskujen hyväksynnät"
description: "Tämä ohjeaihe on tarkoitettu antamaan käytännön lähestymistavan Dynamics 365 for Finance and Operationsin mobiiliskenaarioiden suunnitteluun ottamalla toimittajan laskujen mobiilihyväksynnän esimerkkitapaukseksi."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e39d81b0d600012f936865b53f8556eb3ef0a3d9
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---

# <a name="mobile-invoice-approvals"></a><span data-ttu-id="74269-103">Mobiililaskujen hyväksynnät</span><span class="sxs-lookup"><span data-stu-id="74269-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74269-104">Microsoft Dynamics 365 for Finance and Operations -sovelluksen mobiiliominaisuuksien avulla liiketoimintakäyttäjät voivat suunnitella mobiilin käyttökokemuksen.</span><span class="sxs-lookup"><span data-stu-id="74269-104">Mobile capabilities in Microsoft Dynamics 365 for Finance and Operations let a business user design mobile experiences.</span></span> <span data-ttu-id="74269-105">Vaativimmissa skenaarioissa ympäristö sallii myös, että kehittäjät laajentavat ominaisuuksia kuin haluavat.</span><span class="sxs-lookup"><span data-stu-id="74269-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="74269-106">Tehokkain keino oppia joitakin uusia käsitteitä mobiiliympäristössä on käydä läpi joitakin suunnittelutilanteita.</span><span class="sxs-lookup"><span data-stu-id="74269-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="74269-107">Tämä aihe on tarkoitettu antamaan käytännön lähestymistavan mobiiliskenaarioiden suunnitteluun ottamalla toimittajan laskujen mobiilihyväksynnän esimerkkitapaukseksi.</span><span class="sxs-lookup"><span data-stu-id="74269-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="74269-108">Tämä ohjeaihe auttaa sinua suunnittelemaan tilanteen muita variaatioita ja sitä voidaan soveltaa myös muihin tilanteisiin, jotka eivät liity toimittajan laskuihin.</span><span class="sxs-lookup"><span data-stu-id="74269-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="74269-109">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="74269-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="74269-110">Edellytys</span><span class="sxs-lookup"><span data-stu-id="74269-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="74269-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="74269-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74269-112">Mobiilikäsikirja esitiedoiksi</span><span class="sxs-lookup"><span data-stu-id="74269-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="74269-113">Mobiiliympäristö</span><span class="sxs-lookup"><span data-stu-id="74269-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="74269-114">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="74269-114">Dynamics 365 for Finance and Operations</span></span>                                                                             | <span data-ttu-id="74269-115">Ympäristö, johon on asennettu Microsoft Dynamics 365 for Operations -versio 1611 sekä Microsoft Dynamics for Operations ympäristöpäivitys 3 (Marraskuu 2016)</span><span class="sxs-lookup"><span data-stu-id="74269-115">An environment that has Microsoft Dynamics 365 for Operations version 1611 and Microsoft Dynamics for Operations platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="74269-116">Asenna hotfix-korjaus KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="74269-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="74269-117">Tehtävän tallennus voit virheellisesti tallentaa kaksi avattavan luettelon Sulje-komentoa. Tämä sisältyy Dynamics 365 for Operationsin ympäristöpäivitykseen 3 (marraskuun 2016 päivitys)</span><span class="sxs-lookup"><span data-stu-id="74269-117">Task recorder can erroneously record two Close commands for dropdown dialogs this is included in Dynamics 365 for Operation platform update 3 (November 2016 update)</span></span> |
| <span data-ttu-id="74269-118">Asenna hotfix-korjaus KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="74269-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="74269-119">Tämän päivityksen avulla liitteitä voi tarkastella mobiiliasiakkaassa. Tämä sisältyy Dynamics 365 for Operationsin ympäristöpäivitykseen 3 (marraskuun 2016 päivitys)</span><span class="sxs-lookup"><span data-stu-id="74269-119">This hotfix enables attachments to be viewed on the mobile client this is included in Dynamics 365 for Operation platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="74269-120">Asenna hotfix-korjaus KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="74269-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="74269-121">Sovelluskoodi toimittajan laskujen hyväksynnän mobiilisovellukselle. Tämä sisältyy Microsoft Dynamics AX -sovellukseen 7.0.1 (May 2016).</span><span class="sxs-lookup"><span data-stu-id="74269-121">Application code for the mobile vendor invoice approval application this is included in Microsoft Dynamics AX application 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="74269-122">Android-, iOS- tai Windows-laite, jossa on asennettuna Finance and Operationsin mobiilisovellus</span><span class="sxs-lookup"><span data-stu-id="74269-122">An Android or iOS or a Windows device that has the mobile app installed for Finance and Operations</span></span> | <span data-ttu-id="74269-123">Etsi sovellus omasta sovelluskaupastasi.</span><span class="sxs-lookup"><span data-stu-id="74269-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="74269-124">Johdanto</span><span class="sxs-lookup"><span data-stu-id="74269-124">Introduction</span></span>
<span data-ttu-id="74269-125">Toimittajalaskujen mobiilihyväksyntä vaatii nämä kolme hotfix-korjausta, jotka on mainittu "Edellytykset"-osassa.</span><span class="sxs-lookup"><span data-stu-id="74269-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="74269-126">Nämä hotfix-korjaukset eivät tarjoa työtilaa laskujen hyväksyntään.</span><span class="sxs-lookup"><span data-stu-id="74269-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="74269-127">Perustiedot työtiloista mobiiliympäristössä on mobiilikäsikirjassa, joka mainitaan "Edellytykset"-osassa.</span><span class="sxs-lookup"><span data-stu-id="74269-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="74269-128">Laskun hyväksynnän työtila on suunniteltava.</span><span class="sxs-lookup"><span data-stu-id="74269-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="74269-129">Jokainen organisaatio määrittää oman toimittajan laskujen liiketoimintaprosessinsa eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="74269-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="74269-130">Ennen kuin suunnittelet toimittajan laskujen hyväksynnän mobiilikäyttöliittymän, sinun kannattaa harkita seuraavia näkökohtia liiketoimintaprosesseista.</span><span class="sxs-lookup"><span data-stu-id="74269-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="74269-131">Ajatuksena on käyttää näitä tietopisteitä mahdollisimman paljon laitteen käyttäjäkokemuksen parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="74269-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="74269-132">Mitkä laskun otsikon kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</span><span class="sxs-lookup"><span data-stu-id="74269-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="74269-133">Mitkä laskurivien kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</span><span class="sxs-lookup"><span data-stu-id="74269-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="74269-134">Kuinka monta laskuriviä yhdessä laskussa on?</span><span class="sxs-lookup"><span data-stu-id="74269-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="74269-135">Käytä tässä 80-20-sääntö ja optimoi tärkeimmät 80 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="74269-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="74269-136">Haluavatko käyttäjät tarkastella mobiililaitteessa kirjanpidollisia jakoja (laskujen koodausta) tarkistusten aikana?</span><span class="sxs-lookup"><span data-stu-id="74269-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="74269-137">Jos vastaus tähän kysymykseen on kyllä, harkitse seuraavia kysymyksiä:</span><span class="sxs-lookup"><span data-stu-id="74269-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="74269-138">Kuinka monta kirjanpidollista jakoa (laajennettua hintaa, arvonlisäveroa, kulua, jakoa jne.) on yhdellä laskurivillä?</span><span class="sxs-lookup"><span data-stu-id="74269-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="74269-139">Käytä uudelleen 80-20-sääntöä.</span><span class="sxs-lookup"><span data-stu-id="74269-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="74269-140">Onko laskuissa myös kirjanpidolliset jaot laskuotsikossa?</span><span class="sxs-lookup"><span data-stu-id="74269-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="74269-141">Jos näin on, ovatko nämä kirjanpidolliset jaot on käytettävissä laitteessa?</span><span class="sxs-lookup"><span data-stu-id="74269-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="74269-142">Tässä ohjeaiheessa ei kerrota, kuinka muokkaa kirjanpidon jakoja, koska tätä toimintoa ei tueta tällä hetkellä mobiiliskenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="74269-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="74269-143">Haluavatko käyttäjät nähdä laskun liitteet laitteella?</span><span class="sxs-lookup"><span data-stu-id="74269-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="74269-144">Laskun hyväksyntöjen mobiilikokemuksen rakenne vaihtelee riippuen vastauksista näihin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="74269-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="74269-145">Tavoitteena on optimoida organisaation liiketoimintaprosessin mobiilikäyttökokemus.</span><span class="sxs-lookup"><span data-stu-id="74269-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="74269-146">Aiheen loppuosassa tarkastelemme kahta skenaarion versiota, jotka perustuvat eri vastauksiin edellisiin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="74269-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="74269-147">Yleisenä ohjeena voi sanoa, että kun työskentelet mobiilisuunnittelijan kanssa, muista julkaista muutokset, jotta päivityksiä ei menetettäisi.</span><span class="sxs-lookup"><span data-stu-id="74269-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="74269-148">Yksinkertaisen laskun hyväksynnän skenaarion suunnitteleminen Contosolle</span><span class="sxs-lookup"><span data-stu-id="74269-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74269-149">Skenaarion määrite</span><span class="sxs-lookup"><span data-stu-id="74269-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="74269-150">Vastaus</span><span class="sxs-lookup"><span data-stu-id="74269-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="74269-151">Mitkä laskun otsikon kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</span><span class="sxs-lookup"><span data-stu-id="74269-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="74269-152">Toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="74269-152">Vendor name</span></span></li>
<li><span data-ttu-id="74269-153">Laskun kokonaissumma</span><span class="sxs-lookup"><span data-stu-id="74269-153">Invoice total</span></span></li>
<li><span data-ttu-id="74269-154">Laskutusasiakasnumero</span><span class="sxs-lookup"><span data-stu-id="74269-154">Invoice account</span></span></li>
<li><span data-ttu-id="74269-155">Laskun numero</span><span class="sxs-lookup"><span data-stu-id="74269-155">Invoice number</span></span></li>
<li><span data-ttu-id="74269-156">Laskun päivämäärä</span><span class="sxs-lookup"><span data-stu-id="74269-156">Invoice date</span></span></li>
<li><span data-ttu-id="74269-157">Laskun kuvaus</span><span class="sxs-lookup"><span data-stu-id="74269-157">Invoice description</span></span></li>
<li><span data-ttu-id="74269-158">Eräpäivä</span><span class="sxs-lookup"><span data-stu-id="74269-158">Due date</span></span></li>
<li><span data-ttu-id="74269-159">Laskutusvaluutta</span><span class="sxs-lookup"><span data-stu-id="74269-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74269-160">Mitkä laskurivien kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</span><span class="sxs-lookup"><span data-stu-id="74269-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="74269-161">Hankintaluokka</span><span class="sxs-lookup"><span data-stu-id="74269-161">Procurement category</span></span></li>
<li><span data-ttu-id="74269-162">Määrä</span><span class="sxs-lookup"><span data-stu-id="74269-162">Quantity</span></span></li>
<li><span data-ttu-id="74269-163">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="74269-163">Unit price</span></span></li>
<li><span data-ttu-id="74269-164">Rivin nettosumma</span><span class="sxs-lookup"><span data-stu-id="74269-164">Line net amount</span></span></li>
<li><span data-ttu-id="74269-165">Valmisteveron määrä</span><span class="sxs-lookup"><span data-stu-id="74269-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74269-166">Kuinka monta laskuriviä yhdessä laskussa on?</span><span class="sxs-lookup"><span data-stu-id="74269-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="74269-167">Käytä tässä 80-20-sääntö ja optimoi tärkeimmät 80 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="74269-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="74269-168">1</span><span class="sxs-lookup"><span data-stu-id="74269-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74269-169">Haluavatko käyttäjät tarkastella mobiililaitteessa kirjanpidollisia jakoja (laskujen koodausta) tarkistusten aikana?</span><span class="sxs-lookup"><span data-stu-id="74269-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="74269-170">Kyllä</span><span class="sxs-lookup"><span data-stu-id="74269-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74269-171">Kuinka monta kirjanpidollista jakoa (laajennettua hintaa, arvonlisäveroa, kulua jne.) on yhdellä laskurivillä?</span><span class="sxs-lookup"><span data-stu-id="74269-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="74269-172">Käytä uudelleen 80-20-sääntöä.</span><span class="sxs-lookup"><span data-stu-id="74269-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="74269-173">Laajennettu hinta: 2 ALV: 0 Kulut: 0</span><span class="sxs-lookup"><span data-stu-id="74269-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74269-174">Onko laskuissa myös kirjanpidolliset jaot laskuotsikossa?</span><span class="sxs-lookup"><span data-stu-id="74269-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="74269-175">Jos näin on, ovatko nämä kirjanpidolliset jaot on käytettävissä laitteessa?</span><span class="sxs-lookup"><span data-stu-id="74269-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="74269-176">Ei käytössä</span><span class="sxs-lookup"><span data-stu-id="74269-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74269-177">Haluavatko käyttäjät nähdä laskun liitteet laitteella?</span><span class="sxs-lookup"><span data-stu-id="74269-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="74269-178">Kyllä</span><span class="sxs-lookup"><span data-stu-id="74269-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="74269-179">Luo työtila</span><span class="sxs-lookup"><span data-stu-id="74269-179">Create the workspace</span></span>

1.  <span data-ttu-id="74269-180">Avaa selaimessa Finance and Operations ja kirjaudu sisään.</span><span class="sxs-lookup"><span data-stu-id="74269-180">In a browser, open Finance and Operations, and sign in.</span></span>
2.  <span data-ttu-id="74269-181">Kun olet kirjautunut sisään, lisää **&mode=mobile** URL-osoitteeseen (kuten seuraavassa esimerkissä) ja päivitä sivu: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="74269-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="74269-182">Valitse **Asetukset** (ratas) -painike oikeassa yläkulmassa ja valitse sitten **Mobiilisovellus**.</span><span class="sxs-lookup"><span data-stu-id="74269-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="74269-183">Mobiilisovelluksen suunnitteluohjelma pitäisi tulla näkyviin samoin kuin tehtävän tallennustoiminto.</span><span class="sxs-lookup"><span data-stu-id="74269-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="74269-184">Luo uusi työtila napsauttamalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="74269-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="74269-185">Kirjoita tässä esimerkissä työtilan nimeksi **Omat hyväksynnät**.</span><span class="sxs-lookup"><span data-stu-id="74269-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="74269-186">Anna kuvaus.</span><span class="sxs-lookup"><span data-stu-id="74269-186">Enter a description.</span></span>
6.  <span data-ttu-id="74269-187">Valitse työtilan väri.</span><span class="sxs-lookup"><span data-stu-id="74269-187">Select a workspace color.</span></span> <span data-ttu-id="74269-188">Työtilan väriä käytetään tämän työtilan yleisenä tyylinä mobiilikokemuksessa.</span><span class="sxs-lookup"><span data-stu-id="74269-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="74269-189">Valitse työtilan kuvake.</span><span class="sxs-lookup"><span data-stu-id="74269-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="74269-190">Valitse **Valmis**</span><span class="sxs-lookup"><span data-stu-id="74269-190">Click **Done**</span></span>
9.  <span data-ttu-id="74269-191">Tallenna muutokset valitsemalla **Julkaise työtila**</span><span class="sxs-lookup"><span data-stu-id="74269-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="74269-192">Minulle määritetyt toimittajien laskut</span><span class="sxs-lookup"><span data-stu-id="74269-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="74269-193">Ensimmäinen mobiilisivu, joka tulee suunnitella, on luettelo laskuista, jotka on määritetty käyttäjälle tarkistettavaksi.</span><span class="sxs-lookup"><span data-stu-id="74269-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="74269-194">Voit suunnitella tämän mobiilisivun Finance and Operationsin **VendMobileInvoiceAssignedToMeListPage**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="74269-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page in Finance and Operations.</span></span> <span data-ttu-id="74269-195">Ennen kuin suoritat nämä toimet, varmista, että vähintään yksi toimittajalasku on määritetty itsellesi tarkistettavaksi, ja että laskurivillä on kaksi jakoa.</span><span class="sxs-lookup"><span data-stu-id="74269-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="74269-196">Tämä määritys täyttää tämän skenaarion vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="74269-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="74269-197">Korvaa Finance and Operationsin URL-osoitteessa valikkovaihtoehdon nimi merkkijonolla **VendMobileInvoiceAssignedToMeListPage**, jos haluat avata **Minulle määritetyt odottavat toimittajan laskut** -luettelosivun mobiiliversion **Ostoreskontra**-moduulissa.</span><span class="sxs-lookup"><span data-stu-id="74269-197">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="74269-198">Tässä sivussa näkyvät ne laskut, jotka on järjestelmässä liitetty sinulle.</span><span class="sxs-lookup"><span data-stu-id="74269-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="74269-199">Voit etsiä tietyn laskun käyttämällä suodatinta vasemmalla puolella.</span><span class="sxs-lookup"><span data-stu-id="74269-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="74269-200">Kuitenkaan tässä esimerkissä ei edellytetä tiettyä laskua.</span><span class="sxs-lookup"><span data-stu-id="74269-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="74269-201">Tarvitset vain jonkin sinulle määritetyn laskun, jonka avulla voit suunnitella mobiilisivun.</span><span class="sxs-lookup"><span data-stu-id="74269-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="74269-202">Käytettävissä olevat uudet sivut on suunniteltu erityisesti kehittämään mobiiliskenaarioita toimittajalaskuille.</span><span class="sxs-lookup"><span data-stu-id="74269-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="74269-203">Siksi sinun on käytettävä näitä sivuja.</span><span class="sxs-lookup"><span data-stu-id="74269-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="74269-204">URL-osoitteen pitäisi olla samantyyppinen seuraavan osoitteen kanssa, ja siihen siirryttyäsi sinun pitäisi nähdä oheisen kuvan mukainen sivu: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="74269-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
2.  <span data-ttu-id="74269-205">Valitse **Asetukset** (ratas) -painike oikeassa yläkulmassa ja valitse sitten **Mobiilisovellus**.</span><span class="sxs-lookup"><span data-stu-id="74269-205">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="74269-206">Valitse työtila ja sitten **Muokkaa**</span><span class="sxs-lookup"><span data-stu-id="74269-206">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="74269-207">Valitse **Lisää sivu** luodaksesi ensimmäisen mobiilisivun.</span><span class="sxs-lookup"><span data-stu-id="74269-207">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="74269-208">Kirjoita nimi, kuten **Omat toimittajalaskut** sekä kuvaus, kuten **Minulle tarkistettavaksi määritetyt toimittajalaskut**.</span><span class="sxs-lookup"><span data-stu-id="74269-208">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="74269-209">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="74269-209">Click **Done**.</span></span>
7.  <span data-ttu-id="74269-210">Valitse mobiilisivujen suunnitteluohjelmassa **Kentät**-välilehdessä **Valitse kentät**.</span><span class="sxs-lookup"><span data-stu-id="74269-210">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="74269-211">Luettelosivun sarakkeiden tulisi olla likipitäen kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="74269-211">The columns on the list page must resemble the following illustration.</span></span> <span data-ttu-id="74269-212">[![Sarakkeet Minulle määritetyt odottavat toimittajan laskut -sivulla](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="74269-212">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
8.  <span data-ttu-id="74269-213">Lisää tarvittavat sarakkeet luettelosivulta, joka on näytettävä käyttäjille mobiilisivulla.</span><span class="sxs-lookup"><span data-stu-id="74269-213">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="74269-214">Kentät näytetään loppukäyttäjille lisäämisjärjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="74269-214">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="74269-215">Ainoa tapa muuttaa kenttien järjestystä on valita kaikki kentät uudelleen.</span><span class="sxs-lookup"><span data-stu-id="74269-215">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="74269-216">Tämän skenaarion vaatimusten mukaan seuraavat kahdeksan kenttää ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="74269-216">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="74269-217">Joidenkin käyttäjien mielestä kahdeksan kenttää mobiililaitteessa saattaa kuitenkin olla liikaa.</span><span class="sxs-lookup"><span data-stu-id="74269-217">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="74269-218">Siksi näytämme vain tärkeimmät kentät mobiilissa luettelonäkymässä.</span><span class="sxs-lookup"><span data-stu-id="74269-218">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="74269-219">Muut kentät näkyvät tietonäkymässä, jonka suunnittelemme myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="74269-219">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="74269-220">Nyt lisäämme seuraavat kentät.</span><span class="sxs-lookup"><span data-stu-id="74269-220">For now, we will add the following fields.</span></span> <span data-ttu-id="74269-221">Napsauta plus-merkkiä (**+**) sarakkeissa lisätäksesi ne mobiilisivulle.</span><span class="sxs-lookup"><span data-stu-id="74269-221">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="74269-222">Toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="74269-222">Vendor name</span></span>
    - <span data-ttu-id="74269-223">Laskun kokonaissumma</span><span class="sxs-lookup"><span data-stu-id="74269-223">Invoice total</span></span>
    - <span data-ttu-id="74269-224">Laskutusasiakasnumero</span><span class="sxs-lookup"><span data-stu-id="74269-224">Invoice account</span></span>
    - <span data-ttu-id="74269-225">Laskun numero</span><span class="sxs-lookup"><span data-stu-id="74269-225">Invoice number</span></span>
    - <span data-ttu-id="74269-226">Laskun päivämäärä</span><span class="sxs-lookup"><span data-stu-id="74269-226">Invoice date</span></span>

    <span data-ttu-id="74269-227">Kun kentät on lisätty, mobiilisivun pitäisi muistuttaa seuraavaa kuvaa.</span><span class="sxs-lookup"><span data-stu-id="74269-227">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    <span data-ttu-id="74269-228">[![Sivu kenttien lisäämisen jälkeen](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="74269-228">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>
9.  <span data-ttu-id="74269-229">On myös lisättävä seuraavat sarakkeet nyt, että voimme ottaa työnkulkutoimintoja myöhemmin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="74269-229">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="74269-230">Näytä Suorita-tehtävä</span><span class="sxs-lookup"><span data-stu-id="74269-230">Show complete task</span></span>
    - <span data-ttu-id="74269-231">Näytä Delegoi-tehtävä</span><span class="sxs-lookup"><span data-stu-id="74269-231">Show delegate task</span></span>
    - <span data-ttu-id="74269-232">Näytä Peruuta-tehtävä</span><span class="sxs-lookup"><span data-stu-id="74269-232">Show recall task</span></span>
    - <span data-ttu-id="74269-233">Näytä Hylkää-tehtävä</span><span class="sxs-lookup"><span data-stu-id="74269-233">Show reject task</span></span>
    - <span data-ttu-id="74269-234">Näytä Pyydä suoritusta -tehtävä</span><span class="sxs-lookup"><span data-stu-id="74269-234">Show request completion task</span></span>
    - <span data-ttu-id="74269-235">Näytä Lähetä uudelleen -tehtävä</span><span class="sxs-lookup"><span data-stu-id="74269-235">Show resubmit task</span></span>

10. <span data-ttu-id="74269-236">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-236">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="74269-237">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-237">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="74269-238">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="74269-238">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="74269-239">Ota käyttöön **Näytä laskun loppusumma odottavien toimittajalaskujen luettelossa** Ostoreskontran parametrit -lomakkeessa kohdassa **Lasku**.</span><span class="sxs-lookup"><span data-stu-id="74269-239">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="74269-240">Huomaa, että ainoastaan ottamalla käyttöön tämän parametrin laskun kokonaissumma lasketaan näytettäväksi odottavien toimittajan laskujen luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="74269-240">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="74269-241">Tämä on uusi ominaisuus, joka kuuluu vaadittuun hotfix-korjaukseen 3208224.</span><span class="sxs-lookup"><span data-stu-id="74269-241">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="74269-242">Toimittajan laskun tiedot</span><span class="sxs-lookup"><span data-stu-id="74269-242">Vendor invoice details</span></span>

<span data-ttu-id="74269-243">Voit suunnitella laskun tietojen sivun käyttämällä Finance and Operationsin **VendMobileInvoiceHeaderDetails**-sivua.</span><span class="sxs-lookup"><span data-stu-id="74269-243">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="74269-244">Huomaa, että riippuen järjestelmässäsi olevien laskujen määrästä tällä sivulla näytetään vanhin lasku (lasku, joka on luotu ensin).</span><span class="sxs-lookup"><span data-stu-id="74269-244">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="74269-245">Voit etsiä tietyn laskun käyttämällä suodatinta vasemmalla puolella.</span><span class="sxs-lookup"><span data-stu-id="74269-245">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="74269-246">Kuitenkaan tässä esimerkissä ei edellytetä tiettyä laskua.</span><span class="sxs-lookup"><span data-stu-id="74269-246">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="74269-247">Tässä tarvitaan vain jotkin laskutiedot, että voimme suunnitella mobiilisivun.</span><span class="sxs-lookup"><span data-stu-id="74269-247">We just require some invoice data so that we can design the mobile page.</span></span> <span data-ttu-id="74269-248">[![Työnkulku-sivu](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="74269-248">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="74269-249">Korvaa Finance and Operationsin URL-osoitteessa valikkovaihtoehto nimi merkkijonolla **VendMobileInvoiceHeaderDetails**, jos haluat avata lomakkeen</span><span class="sxs-lookup"><span data-stu-id="74269-249">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>
2. <span data-ttu-id="74269-250">Avaa mobiilisivujen suunnitteluohjelma **Asetukset** (ratas) -painikkeesta.</span><span class="sxs-lookup"><span data-stu-id="74269-250">Open the mobile designer from the **Settings** (gear) button.</span></span>
3. <span data-ttu-id="74269-251">Valitse **Muokkaa**-painike käynnistääksesi muokkaustilan työtilassa.</span><span class="sxs-lookup"><span data-stu-id="74269-251">Click the **Edit** button to start edit mode in the workspace.</span></span>
4. <span data-ttu-id="74269-252">Valitse **Omat toimittajalaskut** -sivu, jonka loit aiemmin ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="74269-252">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>
5. <span data-ttu-id="74269-253">Valitse **Kentät** -välilehdessä sarakkeen otsikko **Ruudukko**.</span><span class="sxs-lookup"><span data-stu-id="74269-253">On the **Fields** tab, click the **Grid** column heading.</span></span>
6. <span data-ttu-id="74269-254">Valitse **Ominaisuudet &gt; Lisää sivu**.</span><span class="sxs-lookup"><span data-stu-id="74269-254">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="74269-255">**Huomautus:** Kun valitset **Ruudukko**-otsikon ja lisäät sivun, yhteys tietosivuun muodostetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="74269-255">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>
7. <span data-ttu-id="74269-256">Kirjoita sivun otsikko, esimerkiksi **Laskun tiedot** ja kuvaus, kuten **Näytä laskun otsikko ja rivitiedot**.</span><span class="sxs-lookup"><span data-stu-id="74269-256">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>
8. <span data-ttu-id="74269-257">Klikkaa **Valitse kentät**.</span><span class="sxs-lookup"><span data-stu-id="74269-257">Click **Select fields**.</span></span> <span data-ttu-id="74269-258">Huomaa, että kentät näytetään loppukäyttäjille lisäämisjärjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="74269-258">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="74269-259">Ainoa tapa muuttaa kenttien järjestystä on valita kaikki kentät uudelleen.</span><span class="sxs-lookup"><span data-stu-id="74269-259">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 
9. <span data-ttu-id="74269-260">Lisää seuraavat kentät otsikosta tämän skenaarion vaatimusten mukaan:</span><span class="sxs-lookup"><span data-stu-id="74269-260">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="74269-261">Toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="74269-261">Vendor name</span></span>
   - <span data-ttu-id="74269-262">Laskun kokonaissumma</span><span class="sxs-lookup"><span data-stu-id="74269-262">Invoice total</span></span>
   - <span data-ttu-id="74269-263">Laskutusasiakasnumero</span><span class="sxs-lookup"><span data-stu-id="74269-263">Invoice account</span></span>
   - <span data-ttu-id="74269-264">Laskun numero</span><span class="sxs-lookup"><span data-stu-id="74269-264">Invoice number</span></span>
   - <span data-ttu-id="74269-265">Laskun päivämäärä</span><span class="sxs-lookup"><span data-stu-id="74269-265">Invoice date</span></span>
   - <span data-ttu-id="74269-266">Laskun kuvaus</span><span class="sxs-lookup"><span data-stu-id="74269-266">Invoice description</span></span>
   - <span data-ttu-id="74269-267">Eräpäivä</span><span class="sxs-lookup"><span data-stu-id="74269-267">Due date</span></span>
   - <span data-ttu-id="74269-268">Laskutusvaluutta</span><span class="sxs-lookup"><span data-stu-id="74269-268">Invoice currency</span></span>

10. <span data-ttu-id="74269-269">Lisää seuraavat kentät sivun riviruudukosta:</span><span class="sxs-lookup"><span data-stu-id="74269-269">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="74269-270">Hankintaluokka</span><span class="sxs-lookup"><span data-stu-id="74269-270">Procurement category</span></span>
    - <span data-ttu-id="74269-271">Määrä</span><span class="sxs-lookup"><span data-stu-id="74269-271">Quantity</span></span>
    - <span data-ttu-id="74269-272">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="74269-272">Unit price</span></span>
    - <span data-ttu-id="74269-273">Rivin nettosumma</span><span class="sxs-lookup"><span data-stu-id="74269-273">Line net amount</span></span>
    - <span data-ttu-id="74269-274">Valmisteveron määrä</span><span class="sxs-lookup"><span data-stu-id="74269-274">1099 amount</span></span>

11. <span data-ttu-id="74269-275">Kun kaikki edellisten kahden vaiheen kentät on lisätty, valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="74269-275">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="74269-276">Sivun tulisi olla likipitäen kuin seuraavassa kuvassa.</span><span class="sxs-lookup"><span data-stu-id="74269-276">The page must resemble the following illustration.</span></span>
    <span data-ttu-id="74269-277">[![Sivu kenttien lisäämisen jälkeen](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="74269-277">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>
12. <span data-ttu-id="74269-278">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-278">Click **Done** to exit edit mode.</span></span>
13. <span data-ttu-id="74269-279">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-279">Click **Back** and then **Done** to exit the workspace</span></span>
14. <span data-ttu-id="74269-280">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="74269-280">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="74269-281">Työnkulkutehtävät</span><span class="sxs-lookup"><span data-stu-id="74269-281">Workflow actions</span></span>

<span data-ttu-id="74269-282">Voit lisätä työnkulkutoimintoja Finance and Operationsin **VendMobileInvoiceHeaderDetails**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="74269-282">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="74269-283">Jos haluat avata tämän sivun, korvaa valikkovaihtoehdon nimi URL-osoitteessa, kuten teit aikaisemmin.</span><span class="sxs-lookup"><span data-stu-id="74269-283">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="74269-284">Avaa sitten mobiilisivujen suunnitteluohjelma **Asetukset** (ratas) -painikkeesta.</span><span class="sxs-lookup"><span data-stu-id="74269-284">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="74269-285">Toimi seuraavien vaiheiden mukaisesti lisätäksesi työnkulkutoimintoja tietosivulle.</span><span class="sxs-lookup"><span data-stu-id="74269-285">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="74269-286">Sinulle on oltava määritettynä sopivassa tilassa olevia laskuja, joiden avulla pääset työnkulkutoimintoihin.</span><span class="sxs-lookup"><span data-stu-id="74269-286">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="74269-287">Työnkulkutoimintojen tallentaminen</span><span class="sxs-lookup"><span data-stu-id="74269-287">Record workflow actions</span></span>
1.  <span data-ttu-id="74269-288">Valitse **Muokkaa**-painike käynnistääksesi muokkaustilan työtilassa.</span><span class="sxs-lookup"><span data-stu-id="74269-288">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="74269-289">Valitse **Laskun tiedot** -sivu, jonka loit aiemmin ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="74269-289">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="74269-290">Valitse **Toiminnot**-välilehdessä **Lisää toiminto**.</span><span class="sxs-lookup"><span data-stu-id="74269-290">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="74269-291">Kirjoita toiminnon otsikko, esimerkiksi **Hyväksy** ja kuvaus, kuten **Hyväksy lasku**.</span><span class="sxs-lookup"><span data-stu-id="74269-291">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="74269-292">Huomaa, että tässä antamasi otsikko näkyy loppukäyttäjille toiminnon nimenä mobiilisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="74269-292">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="74269-293">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="74269-293">Click **Done**.</span></span>
6.  <span data-ttu-id="74269-294">Klikkaa **Valitse kentät**.</span><span class="sxs-lookup"><span data-stu-id="74269-294">Click **Select fields**.</span></span>
7.  <span data-ttu-id="74269-295">Siirry työnkulkuprosessin kautta **VendMobileInvoiceHeaderDetails**-sivulle ja suorita toiminto, jonka haluat tallentaa.</span><span class="sxs-lookup"><span data-stu-id="74269-295">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="74269-296">Varmista, että kirjoitat työnkulun kommentit tämän prosessin aikana, jotta kommenttikenttä sisältyy myös mobiilikokemukseen.</span><span class="sxs-lookup"><span data-stu-id="74269-296">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="74269-297">Kun työnkulkutoiminto on suoritettu, valitse **Valmis** viimeistelläksesi Valitse kentät -tehtävän.</span><span class="sxs-lookup"><span data-stu-id="74269-297">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="74269-298">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-298">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="74269-299">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-299">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="74269-300">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="74269-300">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="74269-301">Tallenna kaikki tarvittavat työnkulkutoiminnot toistamalla edelliset vaiheet.</span><span class="sxs-lookup"><span data-stu-id="74269-301">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="74269-302">.js-tiedoston luominen</span><span class="sxs-lookup"><span data-stu-id="74269-302">Create a .js file</span></span>
1. <span data-ttu-id="74269-303">Avaa Muistio tai Microsoft Visual Studio ja liitä seuraava koodi.</span><span class="sxs-lookup"><span data-stu-id="74269-303">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="74269-304">Tallenna tiedosto .js-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="74269-304">Save the file as a .js file.</span></span> <span data-ttu-id="74269-305">Koodilla voidaan suorittaa seuraavia toimintoja:</span><span class="sxs-lookup"><span data-stu-id="74269-305">This code does the following:</span></span>
    - <span data-ttu-id="74269-306">Se piilottaa ylimääräiset työnkulkuun liittyvät sarakkeet, jotka on lisätty aiemmin mobiililuettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="74269-306">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="74269-307">Lisäsimme nämä sarakkeet, jotta sovelluksella on nämä tiedot oikeassa asiayhteydessä, jotta se voi suorittaa seuraavan vaiheen.</span><span class="sxs-lookup"><span data-stu-id="74269-307">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="74269-308">Aktiiviseen työnkulun vaiheen perusteella se käyttää logiikkaa, joka näyttää vain kyseiset toiminnot.</span><span class="sxs-lookup"><span data-stu-id="74269-308">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="74269-309">Sivujen ja muiden ohjausobjektien nimet on oltava koodissa samat kuin työtilan nimet.</span><span class="sxs-lookup"><span data-stu-id="74269-309">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="74269-310">Lataa kooditiedoston työtilaan valitsemalla **Logiikka**-välilehti</span><span class="sxs-lookup"><span data-stu-id="74269-310">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="74269-311">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-311">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="74269-312">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-312">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="74269-313">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="74269-313">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="74269-314">Toimittajalaskujen liitteet</span><span class="sxs-lookup"><span data-stu-id="74269-314">Vendor invoice attachments</span></span>

1. <span data-ttu-id="74269-315">Valitse **Asetukset** (ratas) -painike oikeassa yläkulmassa ja valitse sitten **Mobiilisovellus**.</span><span class="sxs-lookup"><span data-stu-id="74269-315">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
2. <span data-ttu-id="74269-316">Valitse **Muokkaa**-painike käynnistääksesi muokkaustilan työtilassa.</span><span class="sxs-lookup"><span data-stu-id="74269-316">Click the **Edit** button to start edit mode in the workspace.</span></span>
3. <span data-ttu-id="74269-317">Valitse <strong>Laskun tiedot **-sivu, jonka loit aiemmin ja valitse sitten **Muokkaa</strong>.</span><span class="sxs-lookup"><span data-stu-id="74269-317">Select the <strong>Invoice details **page that you created earlier, and then click **Edit</strong>.</span></span>
4. <span data-ttu-id="74269-318">Määritä **Tiedostojen hallinta** -asetukseksi **Kyllä** alla olevan esimerkin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="74269-318">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="74269-319">**Huomautus:** Jos ei ole liitteitä ei ole tarpeen näyttää mobiililaitteessa, voit jättää tämän vaihtoehdon arvoksi **Ei**, joka on oletusasetus.</span><span class="sxs-lookup"><span data-stu-id="74269-319">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   <span data-ttu-id="74269-320">![Tiedoston hallinta](./media/docmanagement-216x300.png)</span><span class="sxs-lookup"><span data-stu-id="74269-320">![Document management](./media/docmanagement-216x300.png)</span></span>
5. <span data-ttu-id="74269-321">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-321">Click **Done** to exit edit mode.</span></span>
6. <span data-ttu-id="74269-322">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-322">Click **Back** and then **Done** to exit the workspace</span></span>
7. <span data-ttu-id="74269-323">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="74269-323">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="74269-324">Toimittajan laskujen rivijaot</span><span class="sxs-lookup"><span data-stu-id="74269-324">Vendor invoice line distributions</span></span>

<span data-ttu-id="74269-325">Tämän skenaarion vaatimukset vahvistavat, että seillä on vain rivitason jaot ja että laskulla on aina vain yksi rivi.</span><span class="sxs-lookup"><span data-stu-id="74269-325">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="74269-326">Koska tämä skenaario on yksinkertainen, mobiililaitteen käyttökokemuksenkin täytyy olla yksinkertainen, jotta käyttäjän ei tarvitse porautua alaspäin useita tasoja nähdäkseen jaot.</span><span class="sxs-lookup"><span data-stu-id="74269-326">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="74269-327">Finance and Operationsin toimittajan laskuihin sisältyy mahdollisuus näyttää kaikki jaot laskun otsikosta.</span><span class="sxs-lookup"><span data-stu-id="74269-327">Vendor invoices in Finance and Operations include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="74269-328">Tämän kokemuksen tarvitsemme mobiiliskenaariossa.</span><span class="sxs-lookup"><span data-stu-id="74269-328">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="74269-329">Tämän vuoksi käytämme **VendMobileInvoiceAllDistributionTree**-sivua suunnittellaksemme mobiiliskenaarion tämän osan.</span><span class="sxs-lookup"><span data-stu-id="74269-329">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="74269-330">Kun tiedämme vaatimukset, se auttaa päättämään, mitä tiettyä sivua käyttää ja miten tarkalleen optimoida käyttäjän mobiilikokemus, kun suunnittelemme tätä skenaariota.</span><span class="sxs-lookup"><span data-stu-id="74269-330">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="74269-331">Toisessa tilanteessa käytämme toista sivua näyttämään jaot, koska skenaarioiden vaatimukset eroavat.</span><span class="sxs-lookup"><span data-stu-id="74269-331">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="74269-332">Korvaa valikkovaihtoehdon nimi URL-osoitteessa, kuten teit aikaisemmin.</span><span class="sxs-lookup"><span data-stu-id="74269-332">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="74269-333">Sivun, joka näkyy, on muistutettava seuraavaa kuvaa.</span><span class="sxs-lookup"><span data-stu-id="74269-333">The page that appears should resemble the following illustration.</span></span>
<span data-ttu-id="74269-334">[![Kaikki jaot -sivu](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="74269-334">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>
2.  <span data-ttu-id="74269-335">Avaa mobiilisivujen suunnitteluohjelma **Asetukset** (ratas) -painikkeesta.</span><span class="sxs-lookup"><span data-stu-id="74269-335">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="74269-336">Valitse **Muokkaa**-painike käynnistääksesi muokkaustilan työtilassa.</span><span class="sxs-lookup"><span data-stu-id="74269-336">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="74269-337">**Huomautus:** Näet, että kaksi uutta sivua on luotu automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="74269-337">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="74269-338">Järjestelmä luo nämä sivut, koska otit käyttöön tiedostojen hallinnan edellisessä osassa.</span><span class="sxs-lookup"><span data-stu-id="74269-338">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="74269-339">Voit ohittaa nämä uudet sivut.</span><span class="sxs-lookup"><span data-stu-id="74269-339">You can ignore these new pages.</span></span>
4.  <span data-ttu-id="74269-340">Valitse **Lisää sivu**.</span><span class="sxs-lookup"><span data-stu-id="74269-340">Click **Add page**.</span></span>
5.  <span data-ttu-id="74269-341">Kirjoita sivun otsikko, esimerkiksi **Näytä kirjanpito**  ja kuvaus, kuten **Näytä laskun kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="74269-341">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>
6.  <span data-ttu-id="74269-342">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="74269-342">Click **Done**.</span></span>
7.  <span data-ttu-id="74269-343">Klikkaa **Kentät**-välilehdessä **Valitse kentät**, valitse seuraavat kentät Jaot-sivulta ja valitse sitten **Valmis**:</span><span class="sxs-lookup"><span data-stu-id="74269-343">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="74269-344">Summa</span><span class="sxs-lookup"><span data-stu-id="74269-344">Amount</span></span>
    2.  <span data-ttu-id="74269-345">Valuutta</span><span class="sxs-lookup"><span data-stu-id="74269-345">Currency</span></span>
    3.  <span data-ttu-id="74269-346">Kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="74269-346">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="74269-347">Emme valinneet **Kuvaus**-saraketta jakoruudukosta, koska tämän skenaarion vaatimukset vahvistivat, että vain laajennetulle hinnalle on olemassa jako.</span><span class="sxs-lookup"><span data-stu-id="74269-347">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="74269-348">Tämän vuoksi käyttäjä ei edellytä toista kenttää sen summan tyypin määrittämiseksi, jolle jako on.</span><span class="sxs-lookup"><span data-stu-id="74269-348">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="74269-349">Kuitenkin seuraavassa skenaariossa me **tulemme** käyttämään tätä tietoa, koska tämän skenaarion vaatimukset määrittävät, että muuntyyppisilläkin summilla on jakoja (kuten arvonlisävero).</span><span class="sxs-lookup"><span data-stu-id="74269-349">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>
8.  <span data-ttu-id="74269-350">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-350">Click **Done** to exit edit mode.</span></span>
9.  <span data-ttu-id="74269-351">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-351">Click **Back** and then **Done** to exit the workspace</span></span>
10. <span data-ttu-id="74269-352">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="74269-352">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="74269-353">**Näytä kirjanpito** -mobiilisivua ei ole tällä hetkellä linkitetty yhteenkään tähän mennessä suunniteltuun mobiilisivuun.</span><span class="sxs-lookup"><span data-stu-id="74269-353">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="74269-354">Koska käyttäjän pitää voida siirtyä **Näytä kirjanpito** -sivulle mobiililaitteen **Laskun tiedot** -sivulta, meidän on luotava siirtyminen **Laskun tiedot** -sivulta **Näytä kirjanpito** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="74269-354">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="74269-355">Luomme tämän siirtymisen JavaScript-lisälogiikan avulla.</span><span class="sxs-lookup"><span data-stu-id="74269-355">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="74269-356">Avaa .js-tiedosto, jonka loit aiemmin ja lisää rivit, jotka näkyvät korostettuina seuraavassa koodissa.</span><span class="sxs-lookup"><span data-stu-id="74269-356">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="74269-357">Tämä koodi tekee kaksi asiaa:</span><span class="sxs-lookup"><span data-stu-id="74269-357">This code does two things:</span></span>
    1.  <span data-ttu-id="74269-358">Sen avulla varmistetaan, että käyttäjät eivät voi siirtyä suoraan työtilasta **Näytä kirjanpito** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="74269-358">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="74269-359">Se luo siirtymisen ohjausobjektin **Laskun tiedot** -sivulta **Näytä kirjanpito** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="74269-359">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="74269-360">Sivujen ja muiden ohjausobjektien nimet on oltava koodissa samat kuin työtilan nimet.</span><span class="sxs-lookup"><span data-stu-id="74269-360">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="74269-361">Lataa kooditiedosto työtilaan ja korvaa edellinen koodi valitsemalla **Logiikka**-välilehti</span><span class="sxs-lookup"><span data-stu-id="74269-361">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="74269-362">Valitse **Valmis** poistuaksesi muokkaustilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-362">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="74269-363">Valitse **Takaisin** ja sitten **Valmis** poistuaksesi työtilasta.</span><span class="sxs-lookup"><span data-stu-id="74269-363">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="74269-364">Tallenna muutokset valitsemalla **Julkaise työtila**.</span><span class="sxs-lookup"><span data-stu-id="74269-364">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="74269-365">Valintasäännöt</span><span class="sxs-lookup"><span data-stu-id="74269-365">Validation</span></span>

<span data-ttu-id="74269-366">Avaa sovellus mobiililaitteessa ja muodosta yhteys Finance and Operations -esiintymään.</span><span class="sxs-lookup"><span data-stu-id="74269-366">From your mobile device, open the app, and connect to your Finance and Operations instance.</span></span> <span data-ttu-id="74269-367">Varmista, että kirjaudut yritykseen jossa toimittajalaskuja on määritetty sinulle tarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="74269-367">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="74269-368">Sinun pitäisi voida suorittaa seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="74269-368">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="74269-369">Nähdä **Omat hyväksynnät** -työtila.</span><span class="sxs-lookup"><span data-stu-id="74269-369">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="74269-370">Porautua **Omat hyväksynnät** -työtilaan ja nähdä **Omat toimittajalaskut** -sivun.</span><span class="sxs-lookup"><span data-stu-id="74269-370">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="74269-371">Porautua **Omat toimittajalaskut** -sivulle ja nähdä sinulle määritetyt laskut.</span><span class="sxs-lookup"><span data-stu-id="74269-371">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="74269-372">Poraudu yhteen laskuista ja tarkastele laskun otsikon ja rivien tietoja.</span><span class="sxs-lookup"><span data-stu-id="74269-372">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="74269-373">Tiedot-sivulla näet linkin liitteisiin ja tämän linkin avulla voit siirtyä liiteluetteloon ja tarkastella liitteitä.</span><span class="sxs-lookup"><span data-stu-id="74269-373">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="74269-374">Tiedot-sivulla näet linkin **Näytä kirjanpito** -sivulle ja tämän linkin avulla voit siirtyä jakosivulle ja tarkastella jakoja.</span><span class="sxs-lookup"><span data-stu-id="74269-374">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="74269-375">Valitse Tiedot-sivulla **Toiminnot**-valikko sivun alaosasta ja suorita työnkulkutoimintoja, joita sovelletaan työnkulun vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="74269-375">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="74269-376">Monimutkaisen laskun hyväksynnän skenaarion suunnitteleminen Fabrikamille</span><span class="sxs-lookup"><span data-stu-id="74269-376">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74269-377">Skenaarion määrite</span><span class="sxs-lookup"><span data-stu-id="74269-377">Scenario attribute</span></span></th>
<th><span data-ttu-id="74269-378">Vastaus</span><span class="sxs-lookup"><span data-stu-id="74269-378">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="74269-379">Mitkä laskun otsikon kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</span><span class="sxs-lookup"><span data-stu-id="74269-379">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="74269-380">Toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="74269-380">Vendor name</span></span></li>
<li><span data-ttu-id="74269-381">Laskun summa</span><span class="sxs-lookup"><span data-stu-id="74269-381">Invoice amount</span></span></li>
<li><span data-ttu-id="74269-382">Laskutusasiakasnumero</span><span class="sxs-lookup"><span data-stu-id="74269-382">Invoice account</span></span></li>
<li><span data-ttu-id="74269-383">Laskun numero</span><span class="sxs-lookup"><span data-stu-id="74269-383">Invoice number</span></span></li>
<li><span data-ttu-id="74269-384">Laskun päivämäärä</span><span class="sxs-lookup"><span data-stu-id="74269-384">Invoice date</span></span></li>
<li><span data-ttu-id="74269-385">Laskun kuvaus</span><span class="sxs-lookup"><span data-stu-id="74269-385">Invoice description</span></span></li>
<li><span data-ttu-id="74269-386">Eräpäivä</span><span class="sxs-lookup"><span data-stu-id="74269-386">Due date</span></span></li>
<li><span data-ttu-id="74269-387">Laskutusvaluutta</span><span class="sxs-lookup"><span data-stu-id="74269-387">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74269-388">Mitkä laskurivien kentät käyttäjät haluavat nähdä mobiilikäyttöliittymässä ja missä järjestyksessä?</span><span class="sxs-lookup"><span data-stu-id="74269-388">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="74269-389">Hankintaluokka</span><span class="sxs-lookup"><span data-stu-id="74269-389">Procurement category</span></span></li>
<li><span data-ttu-id="74269-390">Määrä</span><span class="sxs-lookup"><span data-stu-id="74269-390">Quantity</span></span></li>
<li><span data-ttu-id="74269-391">Yksikköhinta</span><span class="sxs-lookup"><span data-stu-id="74269-391">Unit price</span></span></li>
<li><span data-ttu-id="74269-392">Rivin nettosumma</span><span class="sxs-lookup"><span data-stu-id="74269-392">Line net amount</span></span></li>
<li><span data-ttu-id="74269-393">Valmisteveron määrä</span><span class="sxs-lookup"><span data-stu-id="74269-393">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74269-394">Kuinka monta laskuriviä yhdessä laskussa on?</span><span class="sxs-lookup"><span data-stu-id="74269-394">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="74269-395">Käytä tässä 80-20-sääntö ja optimoi tärkeimmät 80 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="74269-395">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="74269-396">5</span><span class="sxs-lookup"><span data-stu-id="74269-396">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74269-397">Haluavatko käyttäjät tarkastella mobiililaitteessa kirjanpidollisia jakoja (laskujen koodausta) tarkistusten aikana?</span><span class="sxs-lookup"><span data-stu-id="74269-397">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="74269-398">Kyllä</span><span class="sxs-lookup"><span data-stu-id="74269-398">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74269-399">Kuinka monta kirjanpidollista jakoa (laajennettua hintaa, arvonlisäveroa, kulua jne.) on yhdellä laskurivillä?</span><span class="sxs-lookup"><span data-stu-id="74269-399">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="74269-400">Käytä uudelleen 80-20-sääntöä.</span><span class="sxs-lookup"><span data-stu-id="74269-400">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="74269-401">Laajennettu hinta: 2 ALV: 2 Kulut: 2</span><span class="sxs-lookup"><span data-stu-id="74269-401">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74269-402">Onko laskuissa myös kirjanpidolliset jaot laskuotsikossa?</span><span class="sxs-lookup"><span data-stu-id="74269-402">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="74269-403">Jos näin on, ovatko nämä kirjanpidolliset jaot on käytettävissä laitteessa?</span><span class="sxs-lookup"><span data-stu-id="74269-403">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="74269-404">Ei käytössä</span><span class="sxs-lookup"><span data-stu-id="74269-404">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74269-405">Haluavatko käyttäjät nähdä laskun liitteet laitteella?</span><span class="sxs-lookup"><span data-stu-id="74269-405">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="74269-406">Kyllä</span><span class="sxs-lookup"><span data-stu-id="74269-406">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="74269-407">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="74269-407">Next steps</span></span>

<span data-ttu-id="74269-408">Skenaariolle 1 voidaan tehdä seuraavat muunnelmat perustuen skenaarion 2 vaatimuksiin.</span><span class="sxs-lookup"><span data-stu-id="74269-408">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="74269-409">Voit parantaa mobiilisovelluskokemusta tämän osan avulla.</span><span class="sxs-lookup"><span data-stu-id="74269-409">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="74269-410">Koska skenaariossa 2 odotetaan enemmän laskurivejä, seuraavat muutokset rakenteeseen auttavat optimoimaan mobiililaitteen käyttökokemusta:</span><span class="sxs-lookup"><span data-stu-id="74269-410">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="74269-411">Sen sijaan että tarkastelisit laskurivejä tietosivulla (kuten skenaariossa 1), käyttäjät voivat tarkastella rivejä erillisellä mobiilisivulla.</span><span class="sxs-lookup"><span data-stu-id="74269-411">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="74269-412">Koska tässä tilanteessa on odotettavissa useita laskun rivejä ja jos **VendMobileInvoiceAllDistributionTree** -sivua käytetään mobiilin jakosivun suunnittelussa (kuten skenaariossa 1), se voi olla hämmentävää käyttäjälle yhdistää rivit jakoihin.</span><span class="sxs-lookup"><span data-stu-id="74269-412">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="74269-413">Tämän vuoksi käytä **VendMobileInvoiceLineDistributionTree**-sivua jakosivun suunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="74269-413">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="74269-414">Parhaassa tapauksessa tässä skenaariossa jaot pitäisi näyttää laskurivin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="74269-414">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="74269-415">Varmista siksi, että käyttäjä voi porautua riviin nähdäkseen jakosivun.</span><span class="sxs-lookup"><span data-stu-id="74269-415">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="74269-416">Sivulinkkiominaisuuden avulla voit määrittää porautumisen samalla tavalla kuin otsikko- ja tietosivuille skenaariossa 1.</span><span class="sxs-lookup"><span data-stu-id="74269-416">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="74269-417">Koska skenaariossa 2 on odotettavissa useita summatyyppejä (arvonlisävero, kulut jne.), on hyödyllistä näyttää summatyypin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="74269-417">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="74269-418">(Nämä tiedot jätettiin pois skenaariossa 1).</span><span class="sxs-lookup"><span data-stu-id="74269-418">(We omitted this information in scenario 1.)</span></span>





