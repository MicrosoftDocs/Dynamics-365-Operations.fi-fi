---
title: Palkanlaskennan alkusaldojen antaminen
description: Tässä ohjeaiheessa käsitellään vaiheet, joilla ansiokoodien, vähennysten, etujen ja verojen alkusaldot annetaan. Kumppanit arvostavat näitä tietoja, sillä niiden avulla tiedot voidaan siirtää toisesta järjestelmästä uuteen käyttöönotettuun palkanlaskentaan.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 209636d6416a784d298bcfb134f5486c1f5cf202
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568542"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="8d98b-104">Palkanlaskennan alkusaldojen antaminen</span><span class="sxs-lookup"><span data-stu-id="8d98b-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8d98b-105">Tässä ohjeaiheessa käsitellään vaiheet, joilla ansiokoodien, vähennysten, etujen ja verojen alkusaldot annetaan.</span><span class="sxs-lookup"><span data-stu-id="8d98b-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="8d98b-106">Kumppanit arvostavat näitä tietoja, sillä niiden avulla he voivat siirtää tiedot toisesta järjestelmästä uuteen käyttöönotettuun palkanlaskentaan.</span><span class="sxs-lookup"><span data-stu-id="8d98b-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="8d98b-107">Palkanlaskennan alkusaldojen antamista varten tarkistetaan seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="8d98b-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="8d98b-108">Työntekijätietueet on viety järjestelmään ja ne ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="8d98b-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="8d98b-109">Seuraavat tiedot on määritetty työntekijöille:</span><span class="sxs-lookup"><span data-stu-id="8d98b-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="8d98b-110">Maksujaksot ja maksukaudet</span><span class="sxs-lookup"><span data-stu-id="8d98b-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="8d98b-111">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="8d98b-111">Earning codes</span></span>
    - <span data-ttu-id="8d98b-112">Verot</span><span class="sxs-lookup"><span data-stu-id="8d98b-112">Taxes</span></span>
    - <span data-ttu-id="8d98b-113">Edut ja vähennykset</span><span class="sxs-lookup"><span data-stu-id="8d98b-113">Benefits and deductions</span></span>

- <span data-ttu-id="8d98b-114">Yrityksen on pitänyt valita päivämäärä, johon palkanlaskennat alkusaldot voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="8d98b-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="8d98b-115">Vanhasta järjestelmästä kerättiin tiedot kaikista ansioista, eduista ja vähennyksistä, edun osuuksista, työntekijän verotuksesta sekä työnantajan verotuksesta ja vuoden alusta kertyneistä summista.</span><span class="sxs-lookup"><span data-stu-id="8d98b-115">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="8d98b-116">Harkitse, kuinka yksityiskohtaisia tietoja tarvitset, kun aloitat alkusaldojen antamisen suunnittelun.</span><span class="sxs-lookup"><span data-stu-id="8d98b-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="8d98b-117">Useimmat yritykset ilmoittavat yhden, konsolidoidun vuoden alusta kertyneen summan.</span><span class="sxs-lookup"><span data-stu-id="8d98b-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="8d98b-118">Jos tietojen on kuitenkin oltava yksityiskohtaisempia, saldot voidaan ilmoittaa neljännesvuosittain.</span><span class="sxs-lookup"><span data-stu-id="8d98b-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="8d98b-119">Tarvittavan tarkkuustason päättäminen määrittää, kuinka monta manuaalista maksuilmoitusta on luotava kullekin työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="8d98b-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="8d98b-120">Jos kyse on summasta vuoden alusta, kullekin työntekijälle tarvitaan vain yksi manuaalinen ilmoitus.</span><span class="sxs-lookup"><span data-stu-id="8d98b-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="8d98b-121">Voit tehdä tämän käyttämällä edellisen järjestelmän viimeisen maksuilmoituksen vuoden alusta kertynyttä summaa uuteen palkanlaskentajärjestelmään ilmoitettavana summana.</span><span class="sxs-lookup"><span data-stu-id="8d98b-121">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="8d98b-122">Seuraavassa esimerkissä näytetään, miten työntekijän palkanlaskennan alkusaldot, mukaan lukien ansiokoodit, edut ja vähennykset sekä verot, annetaan.</span><span class="sxs-lookup"><span data-stu-id="8d98b-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="8d98b-123">Jos kyse olisi aidosta esimerkistä, jokaiselle ansiokoodille, edun vähennykselle, edun osuudelle sekä työntekijän ja työnantajan verotukselle olisi rivinimike, johon lisätty summa olisi summa vuoden alusta.</span><span class="sxs-lookup"><span data-stu-id="8d98b-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="8d98b-124">Käytä tätä koodi- ja summaluetteloa luodessasi ansio- ja maksuilmoituksen manuaalisesti siten, että kirjanpito on poistettu käytöstä, palkanlaskennan alkusaldojen tuontia varten.</span><span class="sxs-lookup"><span data-stu-id="8d98b-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="8d98b-125">Kirjanpito poistetaan käytöstä, koska et halua kirjata tätä alkusaldon maksuilmoitusta kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="8d98b-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="8d98b-126">Se tehtiin vanhassa järjestelmässä ja siirtyy uuteen järjestelmään, kun määrität alkusaldot kirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="8d98b-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="8d98b-127">A.</span><span class="sxs-lookup"><span data-stu-id="8d98b-127">A.</span></span> <span data-ttu-id="8d98b-128">Palkanlaskennan alkusaldoissa käytettävien ansiokoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8d98b-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="8d98b-129">Varmista palkanlaskennan alkusaldoja annettaessa, että Salli ansioilmoitushintojen muokkaus -vaihtoehto otettiin käyttöön, kun käytettävät ansiokoodit määritettiin.</span><span class="sxs-lookup"><span data-stu-id="8d98b-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="8d98b-130">Kun vaihtoehto on käytössä, voit antaa summat manuaalisesti vanhasta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="8d98b-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="8d98b-131">B.</span><span class="sxs-lookup"><span data-stu-id="8d98b-131">B.</span></span> <span data-ttu-id="8d98b-132">Alkusaldon sisältävän ansioilmoituksen luominen työntekijälle</span><span class="sxs-lookup"><span data-stu-id="8d98b-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="8d98b-133">Tässä vaiheessa kullekin työntekijälle luodaan manuaalisesti vanhan järjestelmän viimeisen maksukauden ansioilmoitus, joka luo ansioilmoitusrivit uuteen palkanlaskentajärjestelmään.</span><span class="sxs-lookup"><span data-stu-id="8d98b-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="8d98b-134">Lisää yksi rivi kullekin ansiokoodille sekä summalle vuoden alusta ja tunneille.</span><span class="sxs-lookup"><span data-stu-id="8d98b-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="8d98b-135">Mallivaiheet ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="8d98b-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="8d98b-136">Avaa **Kaikki ansioilmoitukset** -sivu ja valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8d98b-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="8d98b-137">Kirjoita seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="8d98b-137">Enter the following:</span></span> 

    | <span data-ttu-id="8d98b-138">Kenttä</span><span class="sxs-lookup"><span data-stu-id="8d98b-138">Field</span></span>      | <span data-ttu-id="8d98b-139">Arvo</span><span class="sxs-lookup"><span data-stu-id="8d98b-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="8d98b-140">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="8d98b-140">Worker</span></span>     | <span data-ttu-id="8d98b-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="8d98b-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="8d98b-142">Maksujakso</span><span class="sxs-lookup"><span data-stu-id="8d98b-142">Pay cycle</span></span>  | <span data-ttu-id="8d98b-143">sm</span><span class="sxs-lookup"><span data-stu-id="8d98b-143">sm</span></span>                    |
    | <span data-ttu-id="8d98b-144">Maksukausi</span><span class="sxs-lookup"><span data-stu-id="8d98b-144">Pay period</span></span> | <span data-ttu-id="8d98b-145">16.6.2017–30.6.2017</span><span class="sxs-lookup"><span data-stu-id="8d98b-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="8d98b-146">Anna **Ansioilmoitusrivi**-välilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="8d98b-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="8d98b-147">Rivi 1: **Ansioilmoitusrivi**-välilehti</span><span class="sxs-lookup"><span data-stu-id="8d98b-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="8d98b-148">Kenttä</span><span class="sxs-lookup"><span data-stu-id="8d98b-148">Field</span></span>            | <span data-ttu-id="8d98b-149">Arvo</span><span class="sxs-lookup"><span data-stu-id="8d98b-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="8d98b-150">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="8d98b-150">Earnings code</span></span>    | <span data-ttu-id="8d98b-151">Normaali palkka</span><span class="sxs-lookup"><span data-stu-id="8d98b-151">Regular pay</span></span> |
    | <span data-ttu-id="8d98b-152">Määrä</span><span class="sxs-lookup"><span data-stu-id="8d98b-152">Quantity</span></span>         | <span data-ttu-id="8d98b-153">1.00</span><span class="sxs-lookup"><span data-stu-id="8d98b-153">1.00</span></span>        |
    | <span data-ttu-id="8d98b-154">Osuus</span><span class="sxs-lookup"><span data-stu-id="8d98b-154">Rate</span></span>             | <span data-ttu-id="8d98b-155">30,000</span><span class="sxs-lookup"><span data-stu-id="8d98b-155">30,000</span></span>      |
    | <span data-ttu-id="8d98b-156">Rivin erittely -välilehti</span><span class="sxs-lookup"><span data-stu-id="8d98b-156">Line details tab</span></span> |             |
    | <span data-ttu-id="8d98b-157">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="8d98b-157">Manual</span></span>           | <span data-ttu-id="8d98b-158">(merkitty)</span><span class="sxs-lookup"><span data-stu-id="8d98b-158">(marked)</span></span>    |

    <span data-ttu-id="8d98b-159">Rivi 2: **Ansioilmoitusrivi**-välilehti</span><span class="sxs-lookup"><span data-stu-id="8d98b-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="8d98b-160">Kenttä</span><span class="sxs-lookup"><span data-stu-id="8d98b-160">Field</span></span>            | <span data-ttu-id="8d98b-161">Arvo</span><span class="sxs-lookup"><span data-stu-id="8d98b-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="8d98b-162">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="8d98b-162">Earnings code</span></span>    | <span data-ttu-id="8d98b-163">Bonus</span><span class="sxs-lookup"><span data-stu-id="8d98b-163">Bonus</span></span>    |
    | <span data-ttu-id="8d98b-164">Määrä</span><span class="sxs-lookup"><span data-stu-id="8d98b-164">Quantity</span></span>         | <span data-ttu-id="8d98b-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="8d98b-165">1.0000</span></span>   |
    | <span data-ttu-id="8d98b-166">Osuus</span><span class="sxs-lookup"><span data-stu-id="8d98b-166">Rate</span></span>             | <span data-ttu-id="8d98b-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="8d98b-167">4250.00</span></span>  |
    | <span data-ttu-id="8d98b-168">Rivin erittely -välilehti</span><span class="sxs-lookup"><span data-stu-id="8d98b-168">Line details tab</span></span> |          |
    | <span data-ttu-id="8d98b-169">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="8d98b-169">Manual</span></span>           | <span data-ttu-id="8d98b-170">(merkitty)</span><span class="sxs-lookup"><span data-stu-id="8d98b-170">(marked)</span></span> |

    <span data-ttu-id="8d98b-171">Rivi 3: **Ansioilmoitusrivi**-välilehti</span><span class="sxs-lookup"><span data-stu-id="8d98b-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="8d98b-172">Kenttä</span><span class="sxs-lookup"><span data-stu-id="8d98b-172">Field</span></span>           | <span data-ttu-id="8d98b-173">Arvo</span><span class="sxs-lookup"><span data-stu-id="8d98b-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="8d98b-174">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="8d98b-174">Earnings code</span></span>   | <span data-ttu-id="8d98b-175">Provisio</span><span class="sxs-lookup"><span data-stu-id="8d98b-175">Commission</span></span> |
    | <span data-ttu-id="8d98b-176">Määrä</span><span class="sxs-lookup"><span data-stu-id="8d98b-176">Quantity</span></span>        | <span data-ttu-id="8d98b-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="8d98b-177">1.0000</span></span>     |
    | <span data-ttu-id="8d98b-178">Osuus</span><span class="sxs-lookup"><span data-stu-id="8d98b-178">Rate</span></span>            | <span data-ttu-id="8d98b-179">! 299,00</span><span class="sxs-lookup"><span data-stu-id="8d98b-179">!,299.00</span></span>   |
    | <span data-ttu-id="8d98b-180">Osuus</span><span class="sxs-lookup"><span data-stu-id="8d98b-180">Rate</span></span>            | <span data-ttu-id="8d98b-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="8d98b-181">1,299.00</span></span>   |
    | <span data-ttu-id="8d98b-182">Rivin erittely -välilehti</span><span class="sxs-lookup"><span data-stu-id="8d98b-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="8d98b-183">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="8d98b-183">Manual</span></span>          | <span data-ttu-id="8d98b-184">(merkitty)</span><span class="sxs-lookup"><span data-stu-id="8d98b-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="8d98b-185">**Manuaalinen**-liukusäätimen asetukseksi on määritettävä **Kyllä** jokaisen ansioilmoitusrivin **Rivin erittely** -välilehdessä, jotta palkanlaskennan alkusaldot annetaan jokaiselle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="8d98b-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="8d98b-186">Valitse **Toiminto**-ruudussa **Vapauta ansioilmoitus** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="8d98b-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="8d98b-187">Avaa **Luo maksuilmoitukset** -sivulla valitsemalla **Toiminto**-ruudussa **Maksuilmoitus** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="8d98b-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="8d98b-188">Kenttä</span><span class="sxs-lookup"><span data-stu-id="8d98b-188">Field</span></span>              | <span data-ttu-id="8d98b-189">Arvo</span><span class="sxs-lookup"><span data-stu-id="8d98b-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="8d98b-190">Maksupäivä</span><span class="sxs-lookup"><span data-stu-id="8d98b-190">Payment date</span></span>       | <span data-ttu-id="8d98b-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="8d98b-191">6/30/2017</span></span> |
    | <span data-ttu-id="8d98b-192">Maksusuorituksen tyyppi</span><span class="sxs-lookup"><span data-stu-id="8d98b-192">Payment run type</span></span>   | <span data-ttu-id="8d98b-193">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="8d98b-193">Manual</span></span>    |
    | <span data-ttu-id="8d98b-194">Poista kirjanpito käytöstä</span><span class="sxs-lookup"><span data-stu-id="8d98b-194">Disable accounting</span></span> |   <span data-ttu-id="8d98b-195">Kyllä</span><span class="sxs-lookup"><span data-stu-id="8d98b-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="8d98b-196">Tämä on käytettävissä vain, kun maksusuoritustyyppi on manuaalinen ja kun käyttäjä haluaa poistaa maksusuorituksen kirjanpidon käytöstä.</span><span class="sxs-lookup"><span data-stu-id="8d98b-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="8d98b-197">Valitse **OK** ja sulje **Infoloki**.</span><span class="sxs-lookup"><span data-stu-id="8d98b-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="8d98b-198">Miksi Poista kirjanpito käytöstä -liukusäätimen asetuksiksi on valittava Kyllä maksuilmoituksia luotaessa?</span><span class="sxs-lookup"><span data-stu-id="8d98b-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="8d98b-199">Kun liukusäätimen asetuksena on **Kyllä**, maksuilmoituksen rivin jakaminen ja vienti kirjanpitoon estetään.</span><span class="sxs-lookup"><span data-stu-id="8d98b-199">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="8d98b-200">Kirjanpidon summat päivitettiin aiemmin, kun vanhan järjestelmän tilien saldot vietiin.</span><span class="sxs-lookup"><span data-stu-id="8d98b-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="8d98b-201">Palkanlaskennan alkusaldojen viennin avulla voit luoda raportteja, jotka sisältävät aiempien vuosien tiedot sekä tunnistusrajat etuja ja verotusta varten.</span><span class="sxs-lookup"><span data-stu-id="8d98b-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="8d98b-202">C.</span><span class="sxs-lookup"><span data-stu-id="8d98b-202">C.</span></span> <span data-ttu-id="8d98b-203">Työntekijöiden maksuilmoitusten luominen</span><span class="sxs-lookup"><span data-stu-id="8d98b-203">Create pay statements for employees</span></span>

<span data-ttu-id="8d98b-204">Kun olet luonut alkusaldot sisältävät maksuilmoitukset, sinun on tarkistettava, että maksuilmoitukset vastaavat palkanlaskennan tietoja.</span><span class="sxs-lookup"><span data-stu-id="8d98b-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="8d98b-205">Sinun on myös päivitettävä etu- ja verotustiedot manuaalisesti vastaamaan aiemman palkanlaskentajärjestelmän tietoja.</span><span class="sxs-lookup"><span data-stu-id="8d98b-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="8d98b-206">Kun olet tarkistanut, että aiemman palkkalaskentajärjestelmään summat vastaavat nykyisten maksuilmoitusten summia, maksuilmoitukset on viimeisteltävä.</span><span class="sxs-lookup"><span data-stu-id="8d98b-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="8d98b-207">Avaa **Kaikki maksuilmoitukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="8d98b-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="8d98b-208">Korosta Michael Redmondin viimeksi luotu maksuilmoitus</span><span class="sxs-lookup"><span data-stu-id="8d98b-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="8d98b-209">Avaa **Maksuilmoitus**-sivu valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="8d98b-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="8d98b-210">Avaa **Edun vähennykset** -välilehti ja anna seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="8d98b-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="8d98b-211">Kenttä</span><span class="sxs-lookup"><span data-stu-id="8d98b-211">Field</span></span>             | <span data-ttu-id="8d98b-212">Arvo</span><span class="sxs-lookup"><span data-stu-id="8d98b-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="8d98b-213">Etu</span><span class="sxs-lookup"><span data-stu-id="8d98b-213">Benefit</span></span>           | <span data-ttu-id="8d98b-214">Vähennyssumma</span><span class="sxs-lookup"><span data-stu-id="8d98b-214">Deduction amount</span></span> |
    | <span data-ttu-id="8d98b-215">Lisäeläkemaksut (Yhdysvalloissa 401K)</span><span class="sxs-lookup"><span data-stu-id="8d98b-215">401K</span></span>              | <span data-ttu-id="8d98b-216">Liity</span><span class="sxs-lookup"><span data-stu-id="8d98b-216">Participate</span></span>      |
    | <span data-ttu-id="8d98b-217">Hammashuolto</span><span class="sxs-lookup"><span data-stu-id="8d98b-217">Dental</span></span>            | <span data-ttu-id="8d98b-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="8d98b-218">SubSp</span></span>            |
    | <span data-ttu-id="8d98b-219">Huolettavien kulut</span><span class="sxs-lookup"><span data-stu-id="8d98b-219">Dep care spending</span></span> | <span data-ttu-id="8d98b-220">Liity</span><span class="sxs-lookup"><span data-stu-id="8d98b-220">Participate</span></span>      |
    | <span data-ttu-id="8d98b-221">Näkö</span><span class="sxs-lookup"><span data-stu-id="8d98b-221">Vision</span></span>            | <span data-ttu-id="8d98b-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="8d98b-222">SupSp</span></span>            |

5. <span data-ttu-id="8d98b-223">Anna **Edun osuudet** -välilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="8d98b-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="8d98b-224">Kenttä</span><span class="sxs-lookup"><span data-stu-id="8d98b-224">Field</span></span>   | <span data-ttu-id="8d98b-225">Arvo</span><span class="sxs-lookup"><span data-stu-id="8d98b-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="8d98b-226">Etu</span><span class="sxs-lookup"><span data-stu-id="8d98b-226">Benefit</span></span> | <span data-ttu-id="8d98b-227">Osuussumma</span><span class="sxs-lookup"><span data-stu-id="8d98b-227">Contribution amount</span></span> |
    | <span data-ttu-id="8d98b-228">Lisäeläkemaksut (Yhdysvalloissa 401K)</span><span class="sxs-lookup"><span data-stu-id="8d98b-228">401K</span></span>    | <span data-ttu-id="8d98b-229">Liity</span><span class="sxs-lookup"><span data-stu-id="8d98b-229">Participate</span></span>         |
    | <span data-ttu-id="8d98b-230">Hammashuolto</span><span class="sxs-lookup"><span data-stu-id="8d98b-230">Dental</span></span>  | <span data-ttu-id="8d98b-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="8d98b-231">SubSp</span></span>               |
    | <span data-ttu-id="8d98b-232">Näkö</span><span class="sxs-lookup"><span data-stu-id="8d98b-232">Vision</span></span>  | <span data-ttu-id="8d98b-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="8d98b-233">SubSp</span></span>               |

6. <span data-ttu-id="8d98b-234">Anna **Verovähennykset** -välilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="8d98b-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="8d98b-235">Kenttä</span><span class="sxs-lookup"><span data-stu-id="8d98b-235">Field</span></span>           | <span data-ttu-id="8d98b-236">Arvo</span><span class="sxs-lookup"><span data-stu-id="8d98b-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="8d98b-237">Alv-koodi</span><span class="sxs-lookup"><span data-stu-id="8d98b-237">Tax code</span></span>        | <span data-ttu-id="8d98b-238">Vähennyssumma</span><span class="sxs-lookup"><span data-stu-id="8d98b-238">Deduction amount</span></span> |
    | <span data-ttu-id="8d98b-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="8d98b-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="8d98b-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="8d98b-240">1600.00</span></span>          |
    | <span data-ttu-id="8d98b-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="8d98b-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="8d98b-242">825.75</span><span class="sxs-lookup"><span data-stu-id="8d98b-242">825.75</span></span>           |

7. <span data-ttu-id="8d98b-243">Anna **Vero-osuudet** -välilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="8d98b-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="8d98b-244">Valitse **Laske**.</span><span class="sxs-lookup"><span data-stu-id="8d98b-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="8d98b-245">Tarkista, että työntekijän maksuilmoituksen loppusumma vastaa vanhan järjestelmän vuoden alusta kertynyttä summaa.</span><span class="sxs-lookup"><span data-stu-id="8d98b-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="8d98b-246">Seuraavan vaiheen viimeistelyn voit jättää odottamaan, kunnes yleiset tarkistukset voi tehdä koostetusti kaikille palkkailmoituksille.</span><span class="sxs-lookup"><span data-stu-id="8d98b-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="8d98b-247">Kun kaikki on maksuilmoitukset on tarkistettu voit viimeistellä ne.</span><span class="sxs-lookup"><span data-stu-id="8d98b-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="8d98b-248">Samaa prosessi voidaan toistaa tarvittaessa erikseen kullekin edellisen vuoden vuosineljänneksille.</span><span class="sxs-lookup"><span data-stu-id="8d98b-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="8d98b-249">Se on tarpeellista vain, jos asiakas haluat nähdä tiedot neljännesvuosittain ilman, että tiedot olisi tarkistettava vanhasta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="8d98b-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="8d98b-250">Työntekijän alkusaldoa antaessa tapahtuu virhe</span><span class="sxs-lookup"><span data-stu-id="8d98b-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="8d98b-251">Tapahtumat voidaan peruuttaa ja antaa uudelleen.</span><span class="sxs-lookup"><span data-stu-id="8d98b-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="8d98b-252">Voit peruuttaa tapahtuman suorittamalla seuraavat vaiheet **Kaikki maksuilmoitukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="8d98b-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="8d98b-253">Valitse **Palauta**.</span><span class="sxs-lookup"><span data-stu-id="8d98b-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="8d98b-254">Valitse **Kyllä**, kun sanoma "Kun palautat tämän maksuilmoituksen, maksuilmoitukselle luodaan vastakirjauksena palautusmaksuilmoitus.</span><span class="sxs-lookup"><span data-stu-id="8d98b-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="8d98b-255">Kumpaakaan maksuilmoitusta ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="8d98b-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="8d98b-256">Haluatko palauttaa tämän maksuilmoituksen?"</span><span class="sxs-lookup"><span data-stu-id="8d98b-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="8d98b-257">avautuu näyttöön.</span><span class="sxs-lookup"><span data-stu-id="8d98b-257">displays.</span></span> 

<span data-ttu-id="8d98b-258">Kun olet peruuttanut maksuilmoitukset, voit luoda työntekijälle uuden maksuilmoituksen aiemmin luodusta ansioilmoituksesta.</span><span class="sxs-lookup"><span data-stu-id="8d98b-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="8d98b-259">Muista korjata kaikki ansioilmoituksen virheelliset rivit ennen uuden maksuilmoituksen luontia ja luo sitten uudet maksuilmoitukset oikeilla summilla.</span><span class="sxs-lookup"><span data-stu-id="8d98b-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]