---
title: Asiakkaiden luotonhallintatietojen lisääminen
description: Tässä ohjeaiheessa käsitellään asiakkaan luotonhallintietojen lisäämistä.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b7ad1b8ff9f00dba41c02e6426662a03c6c6211b
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015204"
---
# <a name="add-credit-management-information-for-customers"></a><span data-ttu-id="09e47-103">Asiakkaiden luotonhallintatietojen lisääminen</span><span class="sxs-lookup"><span data-stu-id="09e47-103">Add credit management information for customers</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="09e47-104">Kun luotonhallintaa ohjaavat parametrit on määritetty, voit lisätä lisää tietoja kustakin asiakkaasta.</span><span class="sxs-lookup"><span data-stu-id="09e47-104">After you've set up the parameters that control credit management, you can add more details for each customer.</span></span> <span data-ttu-id="09e47-105">Nämä tiedot ohjaavat luotonhallintaprosesseja, ja ne antavat myös lisätietoja, joiden avulla perintäryhmän jäsenet voivat hallita asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="09e47-105">These details control the credit management processes, and they also provide additional information that helps members of the collections team manage customers.</span></span>

## <a name="customer-information"></a><span data-ttu-id="09e47-106">Asiakastiedot</span><span class="sxs-lookup"><span data-stu-id="09e47-106">Customer information</span></span>

<span data-ttu-id="09e47-107">Asiakastiedot lisätään **Kaikki asiakkaat** -sivun **Luotonvalvonta**-pikavälilehdessä (**Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**).</span><span class="sxs-lookup"><span data-stu-id="09e47-107">You can add the customer details on the **Credit and collections** FastTab of the **All customers** page (**Account receivable \> Customers \> All customers**).</span></span>

1. <span data-ttu-id="09e47-108">Valitse **Rajoittamaton luottoraja** -asetukseksi **Kyllä**, jos asiakasta ei rajoiteta millään luottorajatestillä.</span><span class="sxs-lookup"><span data-stu-id="09e47-108">Set the **Unlimited credit limit** option to **Yes** if the customer should not be limited by any credit limit tests.</span></span>
2. <span data-ttu-id="09e47-109">Valitse **Ohita luotohallinnassa** -asetukseksi **Kyllä**, jos luotonhallintaprosessien aikana yleensä tehtävät toimet ohitetaan asiakkaan kohdalla.</span><span class="sxs-lookup"><span data-stu-id="09e47-109">Set the **Exclude from credit management** option to **Yes** to exclude the customer from any actions that usually occur during credit management processes.</span></span>
3. <span data-ttu-id="09e47-110">Valitse asiakkaan luotonhallintaryhmä.</span><span class="sxs-lookup"><span data-stu-id="09e47-110">Select the credit management group for the customer.</span></span>
4. <span data-ttu-id="09e47-111">Voit laskea luottorajan asiakkaan valuuttana antamalla **Luottaraja asiakkaan valuuttana** -kentässä asiakkaan luottorajan.</span><span class="sxs-lookup"><span data-stu-id="09e47-111">To calculate the credit limit in the customer's currency, in the **Credit limit in customer's currency** field, enter the customer's credit limit.</span></span> <span data-ttu-id="09e47-112">Yritysvaluutan luottoraja muunnetaan käyttämällä vaihtokursseja, jotka luotonhallinnan parametreissa valittu luottorajan vaihtokurssin tyyppi määrittää.</span><span class="sxs-lookup"><span data-stu-id="09e47-112">The credit limit in the company currency will be converted by using the exchange rates that are defined by the credit limit exchange rate type that is selected in the Credit management parameters.</span></span>
5. <span data-ttu-id="09e47-113">Anna **Viimeksi tarkistettu** -kenttään päivämäärä, jolloin luottopäällikkö viimeksi tarkisti asiakkaan luottorajan.</span><span class="sxs-lookup"><span data-stu-id="09e47-113">In the **Last review date** field, enter the date when the customer's credit limit was last reviewed by a credit manager.</span></span>
6. <span data-ttu-id="09e47-114">Anna **Seuraava ajoitettu tarkistuspäivä** -kenttään päivämäärä, jolloin asiakkaan luottotarkistus ja -päivitys on ajoitettu.</span><span class="sxs-lookup"><span data-stu-id="09e47-114">In the **Next scheduled review date** field, enter the date when the customer is scheduled for credit review and update.</span></span>
7. <span data-ttu-id="09e47-115">Anna **Hyväksyttävä luottoraja** -kenttään korkein luottoraja, joka voidaan määrittää asiakkaalle asiakkaan luottotietojen arvioinnin perusteella.</span><span class="sxs-lookup"><span data-stu-id="09e47-115">In the **Eligible credit limit** field, enter the highest credit limit that can be assigned to the customer, based on your review of that customer's credit history.</span></span> <span data-ttu-id="09e47-116">Hyväksyttävän luottorajan arvo ei ole välttämättä sama kuin **Luotonvalvonta**-pikavälilehdessä oleva luottoraja.</span><span class="sxs-lookup"><span data-stu-id="09e47-116">The eligible credit limit can differ from the credit limit that is shown on the **Credit and collections** FastTab.</span></span>
8. <span data-ttu-id="09e47-117">Anna **Hyväksyttävän luottorajan valuutta** -kenttään hyväksyttävän luottorajan valuutta.</span><span class="sxs-lookup"><span data-stu-id="09e47-117">In the **Eligible credit limit currency** field, enter the currency of the eligible credit limit.</span></span>
9. <span data-ttu-id="09e47-118">Anna **Hyväksyttävän luottorajan päivämäärä** -kenttään päivämäärä, jolloin hyväksyttävä luottoraja luotiin.</span><span class="sxs-lookup"><span data-stu-id="09e47-118">In the **Eligible credit limit date** field, enter the date when the eligible credit limit was created.</span></span>
10. <span data-ttu-id="09e47-119">Anna **Luottotilin tila** -kenttään asiakkaan luottotilin tila.</span><span class="sxs-lookup"><span data-stu-id="09e47-119">In the **Credit account status** field, enter the credit account status of the customer.</span></span>
11. <span data-ttu-id="09e47-120">Anna **Tilan syy** -kenttään tilin tilaan liitetty syy.</span><span class="sxs-lookup"><span data-stu-id="09e47-120">In the **Status reason** field, enter the reason that is associated the account status.</span></span>
12. <span data-ttu-id="09e47-121">Kun **Luottolaitoksen kautta**-asetuksena on **Kyllä**, asiakkaan ilmaistaan olevan määritetty luottolaitokseen.</span><span class="sxs-lookup"><span data-stu-id="09e47-121">Set the **With agency** option to **Yes** to indicate that the customer is currently assigned to a credit agency.</span></span> <span data-ttu-id="09e47-122">Tämä arvo on tarkoitettu vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="09e47-122">This value is for informational purposes only.</span></span> <span data-ttu-id="09e47-123">Sitä ei käytetä luotonhallintaprosesseissa.</span><span class="sxs-lookup"><span data-stu-id="09e47-123">It isn't used in any credit management processes.</span></span>
13. <span data-ttu-id="09e47-124">Kun **Omistusoikeus**-asetuksena on **Kyllä**, omistusoikeutta säilytetään yrityksen puolesta.</span><span class="sxs-lookup"><span data-stu-id="09e47-124">Set the **Title held** option to **Yes** to indicate that a title is held for the company.</span></span> <span data-ttu-id="09e47-125">Tämä arvo on tarkoitettu vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="09e47-125">This value is for informational purposes only.</span></span> <span data-ttu-id="09e47-126">Sitä ei käytetä luotonhallintaprosessissa.</span><span class="sxs-lookup"><span data-stu-id="09e47-126">It isn't used in any credit management process.</span></span>
14. <span data-ttu-id="09e47-127">Anna **Yrityksen aloituspäivämäärä** -kenttään päivämäärä, jolloin asiakas aloitti yritystoimintansa.</span><span class="sxs-lookup"><span data-stu-id="09e47-127">In the **Business started date** field, enter the date when the customer first started to do business.</span></span> <span data-ttu-id="09e47-128">Tätä tietoa käytetään riskipisteitä luotaessa.</span><span class="sxs-lookup"><span data-stu-id="09e47-128">This information is used when risk scores are created.</span></span>
15. <span data-ttu-id="09e47-129">Anna **Asiakas alkaen** -kenttään päivämäärä, jolloin asiakkaan ensimmäiset tapahtumat käsiteltiin.</span><span class="sxs-lookup"><span data-stu-id="09e47-129">In the **Customer since** field, enter the date when the first transactions were processed for the customer.</span></span> <span data-ttu-id="09e47-130">Tätä tietoa käytetään riskipisteitä luotaessa.</span><span class="sxs-lookup"><span data-stu-id="09e47-130">This information is used when risk scores are created.</span></span>
16. <span data-ttu-id="09e47-131">Kirjoita muistiinpanoja, jotka auttaa luottoryhmää arvioimaan asiakkaan luottokelpoisuutta.</span><span class="sxs-lookup"><span data-stu-id="09e47-131">Enter notes that the credit team can use to further evaluate the customer's credit worthiness.</span></span>

<span data-ttu-id="09e47-132">Huomaa, että osa **Asiakas**-sivulla näkyvistä tiedoista on luotu toisessa prosessissa:</span><span class="sxs-lookup"><span data-stu-id="09e47-132">Note that some of the information that is shown on the **Customer** page is created by another process:</span></span>

- <span data-ttu-id="09e47-133">**Luottorajan vanhentumispäivä** -kentässä on päivämäärä, jolloin luottoraja vanhenee.</span><span class="sxs-lookup"><span data-stu-id="09e47-133">The **Credit limit expiration date** field shows the date when the credit limit will expire.</span></span> <span data-ttu-id="09e47-134">Jos kenttää ei määritetä, asiakkaan luottoraja ei vanhene.</span><span class="sxs-lookup"><span data-stu-id="09e47-134">If you don't set this field, the customer's credit limit won't expire.</span></span>
- <span data-ttu-id="09e47-135">**Luottorajan päivämäärä** -kentässä on päivämäärä, jolloin luottoraja luotiin.</span><span class="sxs-lookup"><span data-stu-id="09e47-135">The **Credit limit date** field shows the date when the credit limit was created.</span></span> <span data-ttu-id="09e47-136">Tämä kenttä päivitetään aina, kun luottorajaa muutetaan.</span><span class="sxs-lookup"><span data-stu-id="09e47-136">This field is updated whenever the credit limit is adjusted.</span></span>
- <span data-ttu-id="09e47-137">Väliaikaiset luottorajat ohittavat asiakkaan kausikohtaisen luottorajan.</span><span class="sxs-lookup"><span data-stu-id="09e47-137">Temporary credit limits override the customer credit limit for a period.</span></span> <span data-ttu-id="09e47-138">Niitä käytetään luottorajan sijaan laskemaan kokonaisluottoraja.</span><span class="sxs-lookup"><span data-stu-id="09e47-138">They are used instead of the credit limit to calculate the total credit limit.</span></span> <span data-ttu-id="09e47-139">Nämä tiedot näkyvät vain, jos käytössä aktiivinen luottoraja.</span><span class="sxs-lookup"><span data-stu-id="09e47-139">This information is shown only if there is an active credit limit.</span></span> <span data-ttu-id="09e47-140">Voit lisätä tilapäisiä luottorajoja luottorajaoikaisuilla.</span><span class="sxs-lookup"><span data-stu-id="09e47-140">You can add temporary credit limits through credit limit adjustments.</span></span>
- <span data-ttu-id="09e47-141">**Vakuus tai takaukset** -kentässä on niiden vakuuksien ja takausten kokonaismäärä, jotka voivat nostaa asiakkaan luottorajaa.</span><span class="sxs-lookup"><span data-stu-id="09e47-141">The **Insurance and guarantees** field shows the total value of insurance and guarantees that can increase the credit limit for the customer.</span></span>
- <span data-ttu-id="09e47-142">**Kokonaisluottoraja**-kentässä on asiakkaan lopullinen luottoraja.</span><span class="sxs-lookup"><span data-stu-id="09e47-142">The **Total credit limit** field shows the final credit limit for the customer.</span></span> <span data-ttu-id="09e47-143">Kokonaisluottoraja sisältää vakuudet ja takaukset sekä väliaikaiset luottorajat.</span><span class="sxs-lookup"><span data-stu-id="09e47-143">The total credit limit includes insurance and guarantees, and temporary credit limits.</span></span>

## <a name="temporary-credit-limits"></a><span data-ttu-id="09e47-144">Väliaikaiset luottorajat</span><span class="sxs-lookup"><span data-stu-id="09e47-144">Temporary credit limits</span></span>

<span data-ttu-id="09e47-145">Väliaikaiset luottorajat ohittavat asiakkaan määritetyn kauden luottorajat.</span><span class="sxs-lookup"><span data-stu-id="09e47-145">Temporary credit limits override customer credit limits for a defined period.</span></span> <span data-ttu-id="09e47-146">Voit lisätä väliaikaisia luottorajoja luottorajaoikaisuilla.</span><span class="sxs-lookup"><span data-stu-id="09e47-146">You can add temporary credit limits by using credit limit adjustments.</span></span> <span data-ttu-id="09e47-147">Luottorajaoikaisujen avulla luottopäälliköt voivat päivittää yhden asiakkaan, asiakasryhmän tai kaikkien asiakkaiden luottorajat ja vanhentumispäivät käyttämällä kirjausprosessia.</span><span class="sxs-lookup"><span data-stu-id="09e47-147">Credit limit adjustments let credit managers update the credit limits and expiration dates of a single customer, a group of customers, or all customers through a posting process.</span></span>

<span data-ttu-id="09e47-148">Voit luoda luottorajan oikaisumerkintöjä **Luottorajaoikaisut**-sivulla (**Luotonhallinta \> Luottorajaoikaisut \> Luottorajaoikaisut**).</span><span class="sxs-lookup"><span data-stu-id="09e47-148">You can create credit limit adjustment entries on the **Credit limit adjustments** page (**Credit management \> Credit limit adjustments \> Credit limit adjustments**).</span></span>

## <a name="create-insurance-policies-and-guarantees"></a><span data-ttu-id="09e47-149">Vakuussopimusten ja takausten luominen</span><span class="sxs-lookup"><span data-stu-id="09e47-149">Create insurance policies and guarantees</span></span>

<span data-ttu-id="09e47-150">Voit luoda kullekin asiakkaalle vähintään yhden vakuussopimuksen ja takauksen.</span><span class="sxs-lookup"><span data-stu-id="09e47-150">You can create one or more insurance policies and guarantees for each customer.</span></span> <span data-ttu-id="09e47-151">Voit sitten laskea niiden avulla, minkälainen on yrityksesi riski, kun se antaa luottoa asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="09e47-151">You can then use them to calculate the exposure that your company has when it offers credit to a customer.</span></span> <span data-ttu-id="09e47-152">Vakuussopimukset ja takaukset voidaan sisällyttää myös asiakkaan luottorajaan.</span><span class="sxs-lookup"><span data-stu-id="09e47-152">Insurance policies and guarantees can also be included in the credit limit for a customer.</span></span>

<span data-ttu-id="09e47-153">Voit luoda vakuussopimuksia ja takauksia **Kaikki asiakkaat** -sivulla (**Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**).</span><span class="sxs-lookup"><span data-stu-id="09e47-153">You can create insurance policies and guarantees on the **All customers** page (**Accounts receivable \> Customers \> All customers**).</span></span> <span data-ttu-id="09e47-154">Valitse ensin asiakas ja valitse sitten toimintoruudussa **Luotonhallinta**-välilehdessä **Vakuus ja takaukset**.</span><span class="sxs-lookup"><span data-stu-id="09e47-154">Select a customer, and then, on the Action Pane, on the **Credit management** tab, select **Insurance and guarantees**.</span></span>

> [!NOTE]
> <span data-ttu-id="09e47-155">Seuraavassa menettelyssä valitaan vakuuttaja tai takaaja yleisestä osoitekirjasta.</span><span class="sxs-lookup"><span data-stu-id="09e47-155">In the following procedure, you select an insurer or guarantor from the global address book.</span></span> <span data-ttu-id="09e47-156">Niinpä ennen tämän menettelyn aloittamista on varmistettava, että vakuuttajat ja takaajat on lisätty yleiseen osoitekirjaan.</span><span class="sxs-lookup"><span data-stu-id="09e47-156">Therefore, before you begin this procedure, you must make sure that the insurers and guarantors have been added to the global address book.</span></span>

1. <span data-ttu-id="09e47-157">Valitse **Tunniste**-kentässä **Takaus** tai **Vakuus**.</span><span class="sxs-lookup"><span data-stu-id="09e47-157">In the **Identifier** field, enter **Guarantee** or **Insurance**.</span></span>
2. <span data-ttu-id="09e47-158">Valitse **Takauksen tai vakuuden tyyppi** -kentässä jokin aiemmin määritetyistä takaus- tai vakuustyypeistä.</span><span class="sxs-lookup"><span data-stu-id="09e47-158">In the **Guarantee/Insurance type** field, select one of the guarantee or insurance types that you previously set up.</span></span>
3. <span data-ttu-id="09e47-159">Valitse **Vakuuttaja tai takaaja** -kentässä vakuuttaja tai takaaja yleisestä osoitekirjasta.</span><span class="sxs-lookup"><span data-stu-id="09e47-159">In the **Insurer/Guarantor** field, select the insurer or guarantor from the global address book.</span></span> 
4. <span data-ttu-id="09e47-160">Jos **Tunniste**-kentässä on valittu **Vakuus**, valitse **Sopimuksen kattavuustyyppi** -kentässä jokin aiemmin määritetyistä kattavuustyypeistä.</span><span class="sxs-lookup"><span data-stu-id="09e47-160">If you selected **Insurance** in the **Identifier** field, in the **Policy coverage type** field, select one of the coverage types that you previously set up.</span></span> <span data-ttu-id="09e47-161">Takaukselle ei voi valita sopimuksen kattavuustyyppiä.</span><span class="sxs-lookup"><span data-stu-id="09e47-161">You can't select a policy coverage type for a guarantee.</span></span>
5. <span data-ttu-id="09e47-162">Anna **Tunnus**-kentässä sopimuksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="09e47-162">In the **Identification** field, enter the ID of the policy.</span></span> <span data-ttu-id="09e47-163">Tämä tunnus on yleensä sopimusnumero.</span><span class="sxs-lookup"><span data-stu-id="09e47-163">This ID is usually a policy number.</span></span>
6. <span data-ttu-id="09e47-164">Anna **Voimassa**-kentässä vakuussopimuksen tai takauksen aloituspäivä.</span><span class="sxs-lookup"><span data-stu-id="09e47-164">In the **Effective** field, enter the start date of the insurance policy or guarantee.</span></span>
7. <span data-ttu-id="09e47-165">Anna **Päättyminen**-kentässä päivämäärä, jolloin vakuussopimus tai takaus.</span><span class="sxs-lookup"><span data-stu-id="09e47-165">In the **Expiration** field, enter the date when the insurance policy or guarantee.</span></span> <span data-ttu-id="09e47-166">päättyy.</span><span class="sxs-lookup"><span data-stu-id="09e47-166">expires.</span></span>
8. <span data-ttu-id="09e47-167">Anna **Arvo**-kentässä vakuussopimuksen tai takauksen arvo.</span><span class="sxs-lookup"><span data-stu-id="09e47-167">In the **Value** field, enter the value of the insurance policy or guarantee.</span></span> <span data-ttu-id="09e47-168">Tämä arvo on sopimuksen täysi arvo.</span><span class="sxs-lookup"><span data-stu-id="09e47-168">This value is the full value of the policy.</span></span>
9. <span data-ttu-id="09e47-169">Valitse **Valuutta** -kentässä sopimuksen arvon valuutta.</span><span class="sxs-lookup"><span data-stu-id="09e47-169">In the **Currency** field, select the currency for the policy value.</span></span> 
10. <span data-ttu-id="09e47-170">Määritä **Päivitä luottoraja** -kentässä prosenttiosuudeksi **0**–**100**.</span><span class="sxs-lookup"><span data-stu-id="09e47-170">In the **Update credit limit** field, specify a percentage between **0** and **100**.</span></span> <span data-ttu-id="09e47-171">Tätä prosenttiosuutta käytetään sopimuksen arvoon ja luottorajalaskelmissa käytettävää luottorajaa nostetaan tuloksena olevan summan verran.</span><span class="sxs-lookup"><span data-stu-id="09e47-171">This percentage will be applied to the policy value, and the resulting amount will be used to increase the credit limit that is used in credit limit calculations.</span></span> <span data-ttu-id="09e47-172">Laskettu arvo näkyy **Kokonaisluottoraja, vakuus ja takaukset** -kohdassa **Asiakkaat**-sivun **Luotonvalvonta**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="09e47-172">The calculated value is shown under **Total credit limit, Insurance and Guarantees** on the **Credit and collections** FastTab of the **Customers** page.</span></span>

    <span data-ttu-id="09e47-173">Tässä on esimerkki:</span><span class="sxs-lookup"><span data-stu-id="09e47-173">Here is an example:</span></span>

    - <span data-ttu-id="09e47-174">Luottoraja (A) on 100 000.</span><span class="sxs-lookup"><span data-stu-id="09e47-174">The credit limit (A) is 100,000.</span></span>
    - <span data-ttu-id="09e47-175">Sopimuksen arvo (B) on 50 000.</span><span class="sxs-lookup"><span data-stu-id="09e47-175">The policy value (B) is 50,000.</span></span>
    - <span data-ttu-id="09e47-176">**Päivitetty luottoraja** -prosentti (C) on 50,00.</span><span class="sxs-lookup"><span data-stu-id="09e47-176">The **Update credit limit** percentage (C) is 50.00.</span></span>
    
    <span data-ttu-id="09e47-177">Tässä tapauksessa todellinen luottoraja is 125 000 (= A + \[B × C\]).</span><span class="sxs-lookup"><span data-stu-id="09e47-177">In this case, the effective credit limit is 125,000 (= A + \[B × C\]).</span></span>

11. <span data-ttu-id="09e47-178">**Sisältyy riskiin** -valintaruudun valinta pienentää luottorajalaskelmiin käytettävää luottorajaa sopimuksen täydellä arvolla.</span><span class="sxs-lookup"><span data-stu-id="09e47-178">Select the **Included in exposure** check box to reduce the credit limit that is used in credit limit calculations by the full value of the policy.</span></span> <span data-ttu-id="09e47-179">Jos tämä valintaruutu valitaan, arvoa, joka lasketaan **Päivitä luottoraja** -prosenttia määritettäessä, ei käytetä luottorajalaskelmissa.</span><span class="sxs-lookup"><span data-stu-id="09e47-179">If this check box is selected, the value that is calculated when the **Update credit limit** percentage is specified won't be used in credit limit calculations.</span></span>

    <span data-ttu-id="09e47-180">Tässä on esimerkki:</span><span class="sxs-lookup"><span data-stu-id="09e47-180">Here is an example:</span></span>

    - <span data-ttu-id="09e47-181">Luottoraja (A) on 100 000.</span><span class="sxs-lookup"><span data-stu-id="09e47-181">The credit limit (A) is 100,000.</span></span>
    - <span data-ttu-id="09e47-182">Sopimuksen arvo (B) on 50 000.</span><span class="sxs-lookup"><span data-stu-id="09e47-182">The policy value (B) is 50,000.</span></span>
    - <span data-ttu-id="09e47-183">**Päivitetty luottoraja** -prosentti (C) on 50,00.</span><span class="sxs-lookup"><span data-stu-id="09e47-183">The **Update credit limit** percentage (C) is 50.00.</span></span>

    <span data-ttu-id="09e47-184">Tässä tapauksessa todellinen luottoraja is 125 000 (= A + \[B × C\]).</span><span class="sxs-lookup"><span data-stu-id="09e47-184">In this case, the effective credit limit is 125,000 (= A + \[B × C\]).</span></span>
    
    <span data-ttu-id="09e47-185">Jos kuitenkin **Sisältyy riskiin** -valintaruutu valitaan, **Päivitä luottoraja** -kohdan arvo 50 000 (= 50,00 prosenttia 100 000:sta) poistetaan ja riskiarvoksi tulee 75 000 (= A + \[B × C\] – B).</span><span class="sxs-lookup"><span data-stu-id="09e47-185">However, if you select the **Included in exposure** check box, the **Update credit limit** value of 50,000 (= 50.00 percent of 100,000) is removed, and the exposure value is 75,000 (= A + \[B × C\] – B).</span></span>