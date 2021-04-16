---
title: Varastotoimintojen vianmääritys
description: Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita varastotoimintojen käytössä voi esiintyä.
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 24e41e35b3e810c509a16b91fffd1e796ab9d134
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832055"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="8db19-103">Varastotoimintojen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="8db19-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8db19-104">Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita varastotoimintojen käytössä voi esiintyä.</span><span class="sxs-lookup"><span data-stu-id="8db19-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="8db19-105">En löydä varastokirjauskansioiden avattavaa Työnkulku-valintaikkunaa.</span><span class="sxs-lookup"><span data-stu-id="8db19-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8db19-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="8db19-106">Issue description</span></span>

<span data-ttu-id="8db19-107">Avattavaa **Työnkulku**-valintaikkunaa ei ole kirjauskansiosivulla tai liittyvät työnkulkutoiminnot eivät ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="8db19-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="8db19-108">Ongelman esiintymiselle on kolme syytä, jotka käsitellään seuraavissa alakohdissa.</span><span class="sxs-lookup"><span data-stu-id="8db19-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="8db19-109">Ongelman ratkaisu 1</span><span class="sxs-lookup"><span data-stu-id="8db19-109">Issue resolution 1</span></span>

<span data-ttu-id="8db19-110">Jos ongelma koskee kaikki käyttäjiä, syynä voi olla se, että hyväksynnän työnkulkua ei ole määritetty kyseiselle kirjauskansiolle.</span><span class="sxs-lookup"><span data-stu-id="8db19-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="8db19-111">Korjaa ongelma seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8db19-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="8db19-112">Valitse **Varastonhallinta &gt; Asetukset &gt; Kirjauskansioiden nimet &gt; Varasto**.</span><span class="sxs-lookup"><span data-stu-id="8db19-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="8db19-113">Valitse luetteloruudussa kirjauskansion nimi ja avaa kirjauskansion asetukset.</span><span class="sxs-lookup"><span data-stu-id="8db19-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="8db19-114">Määritä **Yleinen**-pikavälilehdessä **Hyväksyntätyönkulku** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="8db19-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="8db19-115">Jos järjestelmä pyytää vahvistamaan muutoksen, valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8db19-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="8db19-116">Valitse **Työnkulku**-kentässä työnkulku, jota haluat käyttää valitussa kirjauskansiossa.</span><span class="sxs-lookup"><span data-stu-id="8db19-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="8db19-117">Ongelman ratkaisu 2</span><span class="sxs-lookup"><span data-stu-id="8db19-117">Issue resolution 2</span></span>

<span data-ttu-id="8db19-118">Jos työnkulku käyttää mukautettua koodia, ongelmia voi esiintyä järjestelmän päivityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="8db19-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="8db19-119">Esimerkiksi **Lähetä**-painike näkyy kirjauskansion työnkulussa harmaana, joten lähetystä ei voi hyväksyä painikkeen valinnalla.</span><span class="sxs-lookup"><span data-stu-id="8db19-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="8db19-120">Jos **Lähetä**-painike näkyy harmaana, työnkulkua on ehkä mukautettu. Tämä tarkoittaa sitä, että työnkulun menetelmää `canSubmitToWorkflow()` kohdassa `FormDataUtil` on laajennettu.</span><span class="sxs-lookup"><span data-stu-id="8db19-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="8db19-121">Tämä ongelma korjataan muuttamalla tapaa, jolla `canSubmitToWorkflow()`-menetelmä laajennetaan käyttämään rakennetta seuraavassa esimerkissä.</span><span class="sxs-lookup"><span data-stu-id="8db19-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="8db19-122">Ongelman ratkaisu 3</span><span class="sxs-lookup"><span data-stu-id="8db19-122">Issue resolution 3</span></span>

<span data-ttu-id="8db19-123">Jos ongelma koskee vain muutamia käyttäjiä, kyseisillä käyttäjillä ei ehkä ole suojausoikeuksia, joita tarvitaan työnkulkutoimintojen suorittamiseen varastokirjauskansioissa.</span><span class="sxs-lookup"><span data-stu-id="8db19-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="8db19-124">Varmista, että kullakin käyttäjällä, joita on ongelma koskee, on *Ylläpidä varastokirjauskansion työnkulkua* -suojausoikeus.</span><span class="sxs-lookup"><span data-stu-id="8db19-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="8db19-125">Tämä oikeus määritetään oletusarvoisesti velvollisuudelle, jolla on sama nimi, ja kyseistä velvollisuutta käytetään *Varastotyöntekijä*- ja *Varastopäällikkö*-rooleissa.</span><span class="sxs-lookup"><span data-stu-id="8db19-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="8db19-126">Varastokirjauskansio jää järjestelmän lukitsemaan tilaan, eikä työnkulun erätyö toimi.</span><span class="sxs-lookup"><span data-stu-id="8db19-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8db19-127">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="8db19-127">Issue description</span></span>

<span data-ttu-id="8db19-128">Jokin toiminto on lukinnut varastokirjauskansion eikä sitä vapauteta.</span><span class="sxs-lookup"><span data-stu-id="8db19-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="8db19-129">Jos esimerkiksi tuntematon virhe esiintyy kirjauksen aikana (sillä kirjaus on järjestelmän lukitustoiminto), kirjauskansio voi jäädä järjestelmän lukitsemaan tilaan.</span><span class="sxs-lookup"><span data-stu-id="8db19-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="8db19-130">Siinä tapauksessa työnkulun työnimikkeen käsittelijä ilmoittaa virheen, kun se tarkistaa lukituksen.</span><span class="sxs-lookup"><span data-stu-id="8db19-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8db19-131">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="8db19-131">Issue resolution</span></span>

<span data-ttu-id="8db19-132">Kirjaudu Supply Chain Managementin SQL Server -esiintymään ja tarkista, onko **InventJournalTable.SystemBlocked**-asetuksena *1*.</span><span class="sxs-lookup"><span data-stu-id="8db19-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="8db19-133">Jos näin on, varmista, ettei kirjauskansio ole lukitussa tilassa ja nollaa sitten **InventJournalTable.SystemBlocked**-asetukseksi *0*.</span><span class="sxs-lookup"><span data-stu-id="8db19-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="8db19-134">Varastokirjauskansion työnkulku ei valmistu koskaan eikä kirjauskansiota voi muokata tai kirjata</span><span class="sxs-lookup"><span data-stu-id="8db19-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8db19-135">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="8db19-135">Issue description</span></span>

<span data-ttu-id="8db19-136">Kun kirjauskansion hyväksyntätyönkulku lähetetään, työnkulun käsittely lakkaa vastaamasta eikä kirjauskansioita voi muokata tai käsitellä.</span><span class="sxs-lookup"><span data-stu-id="8db19-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8db19-137">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="8db19-137">Issue resolution</span></span>

<span data-ttu-id="8db19-138">On useita syitä, miksi työnkulun käsittely ei ehkä valmistu.</span><span class="sxs-lookup"><span data-stu-id="8db19-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="8db19-139">Tarkista seuraavat:</span><span class="sxs-lookup"><span data-stu-id="8db19-139">Check for the following issues:</span></span>

- <span data-ttu-id="8db19-140">Valitse **Varastonhallinta &gt; Asetukset &gt; Varastonhallinnan työkulut** ja tarkastele ongelmallisen työnkulun määritystä.</span><span class="sxs-lookup"><span data-stu-id="8db19-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="8db19-141">Lisätietoja on kohdassa [Varastokirjauskansioin hyväksyntätyönkulut](inventory-journal-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="8db19-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="8db19-142">Työnkulussa voi esiintyä poikkeus tai virhe.</span><span class="sxs-lookup"><span data-stu-id="8db19-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="8db19-143">Tarkastele ongelmallisen työnkulun työnimikehistoriaa ja katso, onko siinä työnkulun päättävää sovellusvirhettä.</span><span class="sxs-lookup"><span data-stu-id="8db19-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="8db19-144">Varastokirjauskansio voidaan päivittää tai sitä voi muokata vain, jos se on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="8db19-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="8db19-145">Jos peruutus on aktivoitu, voit yrittää peruuttaa kirjauskansion.</span><span class="sxs-lookup"><span data-stu-id="8db19-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="8db19-146">Työnkulun erätyön suorittamisen keskeyttämiseen voi olla useita syitä.</span><span class="sxs-lookup"><span data-stu-id="8db19-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="8db19-147">Työnkulkukehyksen ongelma voi aiheuttaa osan näistä syistä.</span><span class="sxs-lookup"><span data-stu-id="8db19-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="8db19-148">Varastokirjauskansion työnkulun ehtoja käytetään vain kirjauskansiotasolla, ei rivitasolla</span><span class="sxs-lookup"><span data-stu-id="8db19-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="8db19-149">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="8db19-149">Issue description</span></span>

<span data-ttu-id="8db19-150">Tämä ongelma voi esiintyä esimerkiksi yritettäessä määrittää varastokirjauskansion työnkulun ehtoa kustannuksen summan perusteella.</span><span class="sxs-lookup"><span data-stu-id="8db19-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="8db19-151">Ehdon määrityksen mukaan vaihe 1 suoritetaan vain, kun kustannuksen summa on alle 100.</span><span class="sxs-lookup"><span data-stu-id="8db19-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="8db19-152">Sen jälkeen toisen ehdon määrityksen mukaan vaihe 2 suoritetaan vain, kun kustannuksen summa on yhtä suuri tai suurempi kuin 100.</span><span class="sxs-lookup"><span data-stu-id="8db19-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="8db19-153">Kun työnkulku sitten suoritetaan, työnkulkuhistoria näyttää vain yhden rivin ja ensimmäisen ehdon arviontina on aina *tosi* lähetetystä arvosta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="8db19-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="8db19-154">Ongelman kiertotapa</span><span class="sxs-lookup"><span data-stu-id="8db19-154">Issue workaround</span></span>

<span data-ttu-id="8db19-155">Nykyisessä julkaisussa varastokirjauskansion työnkulun ehtoja käytetään vain kirjauskansiotasolla, ei rivitasolla.</span><span class="sxs-lookup"><span data-stu-id="8db19-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="8db19-156">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="8db19-156">This behavior is by design.</span></span> <span data-ttu-id="8db19-157">Ehdon ehdot kannattaa määrittää vain kirjauskansiotason määritteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="8db19-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="8db19-158">Varastoluettelo-sivun suodatinruutu ei suodata tuloksia odotetusti</span><span class="sxs-lookup"><span data-stu-id="8db19-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8db19-159">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="8db19-159">Issue description</span></span>

<span data-ttu-id="8db19-160">**Varastoluettelo**-sivun suodatinruudun suodattimet eivät suodata tuloksia odotetusti</span><span class="sxs-lookup"><span data-stu-id="8db19-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8db19-161">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="8db19-161">Issue resolution</span></span>

<span data-ttu-id="8db19-162">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="8db19-162">This behavior is by design.</span></span>

<span data-ttu-id="8db19-163"> *\*Varastoluettelo*\*-sivu kootaan yksityiskohtaisesta käytettävissä olevan varaston taulukosta, joka sisältää kaikki käytettävissä olevat dimensiot.</span><span class="sxs-lookup"><span data-stu-id="8db19-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="8db19-164">Tämän sivun luettelo on kuitenkin yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="8db19-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="8db19-165">Näin ollen se saattaa yhdistää rivit lähdetaulukosta koostamalla arvot näytettävän dimension mukaan.</span><span class="sxs-lookup"><span data-stu-id="8db19-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="8db19-166">Suodatinruudussa määritettyjä suodattimia käytetään lähdetaulukossa, ei koostetussa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="8db19-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="8db19-167">Tämä toiminta voi joskus tuottaa odottamattomia tuloksia, kuten [näissä esimerkeissä](inventory-on-hand-list.md#examples).</span><span class="sxs-lookup"><span data-stu-id="8db19-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="8db19-168"> [Ruudukossa olevia suodattimia](inventory-on-hand-list.md#grid-filters) kuitenkin \*käytetään* koostettuun luetteloon.</span><span class="sxs-lookup"><span data-stu-id="8db19-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="8db19-169">Nämä suodattimet sisältävät sekä pikasuodattimen ruudukon yläosassa että kunkin sarakeotsikon suodattimen.</span><span class="sxs-lookup"><span data-stu-id="8db19-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="8db19-170">Yksikkö ja yksikkömäärä eivät toimi oikein varastokirjauskansiossa</span><span class="sxs-lookup"><span data-stu-id="8db19-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8db19-171">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="8db19-171">Issue description</span></span>

<span data-ttu-id="8db19-172">Jompikumpi seuraavista ongelmista tai molemmat ongelmat voivat esiintyä, kun varastokirjauskansiossa käytetään yksikköjä ja määriä:</span><span class="sxs-lookup"><span data-stu-id="8db19-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="8db19-173">Yksiköt tai yksikkömäärät eivät näy varastokirjauskansiossa, kun vapautetun tuotteen muunnosyksikkö on määritetty eikä yksikköä voi muuttaa varastokirjauskansiossa.</span><span class="sxs-lookup"><span data-stu-id="8db19-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="8db19-174">Vaikka **Määrä**- ja **Yksikkö**-kentät näkyvät varastokirjauskansiossa, **Yksikkömäärä**-kenttä ei näy.</span><span class="sxs-lookup"><span data-stu-id="8db19-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="8db19-175">Jos yksikköä muutetaan, määrä annetaan ja kirjauskansio kirjataan, kirjauskansiossa näkyy edelleen kyseiseen määrän alkuperäinen mittayksikkö.</span><span class="sxs-lookup"><span data-stu-id="8db19-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8db19-176">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="8db19-176">Issue resolution</span></span>

<span data-ttu-id="8db19-177">Korjaa tämä ongelma seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8db19-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="8db19-178">Varmista **Ominaisuuksien hallinta** -työtilassa, että *Mittayksikköä ja yksikkömäärää käytetään varastokirjauskansioissa* -toiminto on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8db19-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="8db19-179">Tämä toiminto lisää **Yksikkö**- ja **Yksikkömäärä**-kentät kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="8db19-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="8db19-180">Kun toiminto on otettu käyttöön, käytä **Määrä**-, **Yksikkömäärä**- ja **Yksikkö**-kenttiä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="8db19-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="8db19-181">**Määrä** – Määritä määrä käyttämällä vapautetulle tuotteelle määritettyä oletusyksikköä.</span><span class="sxs-lookup"><span data-stu-id="8db19-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="8db19-182">Oletusyksikköä ei kuitenkaan näytetä tässä.</span><span class="sxs-lookup"><span data-stu-id="8db19-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="8db19-183">Jos muunto on määritetty oletusyksikön ja **Yksikkö**-kentässä valitun yksikön välille, **Määrä**-kenttä päivitetään automaattisesti **Yksikkömäärä**- ja **Yksikkö**-kenttien valintojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="8db19-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="8db19-184">**Yksikkömäärä** – määritä määrä käyttämällä **Yksikkö**-kentässä valittua yksikköä.</span><span class="sxs-lookup"><span data-stu-id="8db19-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="8db19-185">**Yksikkö** – valitse **Yksikkömäärä**-kentässä olevassa arvossa käytettävä yksikkö.</span><span class="sxs-lookup"><span data-stu-id="8db19-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="8db19-186">Seuraava virhesanoma avautui: Varastointiyksikön desimaalien enimmäismäärä on 0.</span><span class="sxs-lookup"><span data-stu-id="8db19-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8db19-187">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="8db19-187">Issue description</span></span>

<span data-ttu-id="8db19-188">Kun varastotapahtuma tai varastovaraus yritetään kirjata, seuraava virhesanoma avautuu: Varastointiyksikön desimaalien enimmäismäärä on 0.</span><span class="sxs-lookup"><span data-stu-id="8db19-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="8db19-189">Tämä ongelma esiintyy, kun varastotapahtuman määräksi määritetään desimaaliarvo, joka on kentän tukemaa tarkkuustasoa pienempi.</span><span class="sxs-lookup"><span data-stu-id="8db19-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="8db19-190">Varastotapahtuman määräksi on esimerkiksi määritetty *0,5*, mutta määränä tuetaan vain kokonaislukua.</span><span class="sxs-lookup"><span data-stu-id="8db19-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="8db19-191">Tämän vuoksi arvon pitäisi olla *1* eikä *0,5*.</span><span class="sxs-lookup"><span data-stu-id="8db19-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8db19-192">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="8db19-192">Issue resolution</span></span>

1. <span data-ttu-id="8db19-193">Seuraavan komentosarjan suorittaminen SQL Server -esiintymässä pyöristää varastotapahtumien määrät.</span><span class="sxs-lookup"><span data-stu-id="8db19-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="8db19-194">Tämä komentosarja korjaa **inventTrans**-taulukon arvot.</span><span class="sxs-lookup"><span data-stu-id="8db19-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="8db19-195">Käytettävissä olevan varaston yhdenmukaisuustarkistuksen suorittaminen siten, että **korjaa virhe** -vaihtoehto on valittu.</span><span class="sxs-lookup"><span data-stu-id="8db19-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="8db19-196">Näin tarkistetaan, että **inventSum**-taulukossa on oikeat arvot.</span><span class="sxs-lookup"><span data-stu-id="8db19-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8db19-197">On suositeltavaa, että komentosarjaa muokataan huolellisesti ympäristöön sopivaksi ja että se testataan testiympäristössä ja sen tuloksena saatava tiedot tarkistetaan, ennen kuin komentosarja suoritetaan tuotantoympäristössä.</span><span class="sxs-lookup"><span data-stu-id="8db19-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]