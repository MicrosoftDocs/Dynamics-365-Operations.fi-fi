---
title: Palkanlaskennan alkusaldojen antaminen
description: "Tässä ohjeaiheessa käsitellään vaiheet, joilla ansiokoodien, vähennysten, etujen ja verojen alkusaldot annetaan. Kumppanit arvostavat näitä tietoja, sillä niiden avulla tiedot voidaan siirtää toisesta järjestelmästä uuteen käyttöönotettuun palkanlaskentaan."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 1e7bdfca55e1bdaba0b5ebdf55b46744e584ab2c
ms.contentlocale: fi-fi
ms.lasthandoff: 12/18/2018

---

# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="d23e0-104">Palkanlaskennan alkusaldojen antaminen</span><span class="sxs-lookup"><span data-stu-id="d23e0-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d23e0-105">Tässä ohjeaiheessa käsitellään vaiheet, joilla ansiokoodien, vähennysten, etujen ja verojen alkusaldot annetaan.</span><span class="sxs-lookup"><span data-stu-id="d23e0-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="d23e0-106">Kumppanit arvostavat näitä tietoja, sillä niiden avulla he voivat siirtää tiedot toisesta järjestelmästä uuteen käyttöönotettuun palkanlaskentaan.</span><span class="sxs-lookup"><span data-stu-id="d23e0-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="d23e0-107">Palkanlaskennan alkusaldojen antamista varten tarkistetaan seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="d23e0-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="d23e0-108">Työntekijätietueet on viety järjestelmään ja ne ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="d23e0-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="d23e0-109">Seuraavat tiedot on määritetty työntekijöille:</span><span class="sxs-lookup"><span data-stu-id="d23e0-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="d23e0-110">Maksujaksot ja maksukaudet</span><span class="sxs-lookup"><span data-stu-id="d23e0-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="d23e0-111">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="d23e0-111">Earning codes</span></span>
    - <span data-ttu-id="d23e0-112">Verot</span><span class="sxs-lookup"><span data-stu-id="d23e0-112">Taxes</span></span>
    - <span data-ttu-id="d23e0-113">Edut ja vähennykset</span><span class="sxs-lookup"><span data-stu-id="d23e0-113">Benefits and deductions</span></span>

- <span data-ttu-id="d23e0-114">Yrityksen on pitänyt valita päivämäärä, johon palkanlaskennat alkusaldot voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="d23e0-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="d23e0-115">Vanhasta järjestelmästä kerättiin tiedot kaikista ansioista, eduista ja vähennyksistä, edun osuuksista, työntekijän verotuksesta sekä työnantajan verotuksesta ja vuoden alusta kertyneistä summista.</span><span class="sxs-lookup"><span data-stu-id="d23e0-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="d23e0-116">Harkitse, kuinka yksityiskohtaisia tietoja tarvitset, kun aloitat alkusaldojen antamisen suunnittelun.</span><span class="sxs-lookup"><span data-stu-id="d23e0-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="d23e0-117">Useimmat yritykset ilmoittavat yhden, konsolidoidun vuoden alusta kertyneen summan.</span><span class="sxs-lookup"><span data-stu-id="d23e0-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="d23e0-118">Jos tietojen on kuitenkin oltava yksityiskohtaisempia, saldot voidaan ilmoittaa neljännesvuosittain.</span><span class="sxs-lookup"><span data-stu-id="d23e0-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="d23e0-119">Tarvittavan tarkkuustason päättäminen määrittää, kuinka monta manuaalista maksuilmoitusta on luotava kullekin työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="d23e0-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="d23e0-120">Jos kyse on summasta vuoden alusta, kullekin työntekijälle tarvitaan vain yksi manuaalinen ilmoitus.</span><span class="sxs-lookup"><span data-stu-id="d23e0-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="d23e0-121">Voit tehdä ilmoituksen käyttämällä edellisen järjestelmän viimeisen maksuilmoituksen vuoden alusta kertynyttä summaa uuteen palkanlaskentajärjestelmään ilmoitettavana summana.</span><span class="sxs-lookup"><span data-stu-id="d23e0-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="d23e0-122">Seuraavassa esimerkissä näytetään, miten työntekijän palkanlaskennan alkusaldot, mukaan lukien ansiokoodit, edut ja vähennykset sekä verot, annetaan.</span><span class="sxs-lookup"><span data-stu-id="d23e0-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="d23e0-123">Jos kyse olisi aidosta esimerkistä, jokaiselle ansiokoodille, edun vähennykselle, edun osuudelle sekä työntekijän ja työnantajan verotukselle olisi rivinimike, johon lisätty summa olisi summa vuoden alusta.</span><span class="sxs-lookup"><span data-stu-id="d23e0-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="d23e0-124">Käytä tätä koodi- ja summaluetteloa luodessasi ansio- ja maksuilmoituksen manuaalisesti siten, että kirjanpito on poistettu käytöstä, palkanlaskennan alkusaldojen tuontia varten.</span><span class="sxs-lookup"><span data-stu-id="d23e0-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="d23e0-125">Kirjanpito poistetaan käytöstä, koska et halua kirjata tätä alkusaldon maksuilmoitusta kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="d23e0-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="d23e0-126">Se tehtiin vanhassa järjestelmässä ja siirtyy uuteen järjestelmään, kun määrität alkusaldot kirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="d23e0-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="d23e0-127">A.</span><span class="sxs-lookup"><span data-stu-id="d23e0-127">A.</span></span> <span data-ttu-id="d23e0-128">Palkanlaskennan alkusaldoissa käytettävien ansiokoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d23e0-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="d23e0-129">Varmista palkanlaskennan alkusaldoja annettaessa, että Salli ansioilmoitushintojen muokkaus -vaihtoehto otettiin käyttöön, kun käytettävät ansiokoodit määritettiin.</span><span class="sxs-lookup"><span data-stu-id="d23e0-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="d23e0-130">Kun vaihtoehto on käytössä, voit antaa summat manuaalisesti vanhasta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="d23e0-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="d23e0-131">B.</span><span class="sxs-lookup"><span data-stu-id="d23e0-131">B.</span></span> <span data-ttu-id="d23e0-132">Alkusaldon sisältävän ansioilmoituksen luominen työntekijälle</span><span class="sxs-lookup"><span data-stu-id="d23e0-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="d23e0-133">Tässä vaiheessa kullekin työntekijälle luodaan manuaalisesti vanhan järjestelmän viimeisen maksukauden ansioilmoitus, joka luo ansioilmoitusrivit uuteen palkanlaskentajärjestelmään.</span><span class="sxs-lookup"><span data-stu-id="d23e0-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="d23e0-134">Lisää yksi rivi kullekin ansiokoodille sekä summalle vuoden alusta ja tunneille.</span><span class="sxs-lookup"><span data-stu-id="d23e0-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="d23e0-135">Mallivaiheet ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="d23e0-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="d23e0-136">Avaa **Kaikki ansioilmoitukset** -sivu ja valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d23e0-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="d23e0-137">Kirjoita seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d23e0-137">Enter the following:</span></span> 

    | <span data-ttu-id="d23e0-138">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d23e0-138">Field</span></span>      | <span data-ttu-id="d23e0-139">Arvo</span><span class="sxs-lookup"><span data-stu-id="d23e0-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="d23e0-140">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="d23e0-140">Worker</span></span>     | <span data-ttu-id="d23e0-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="d23e0-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="d23e0-142">Maksujakso</span><span class="sxs-lookup"><span data-stu-id="d23e0-142">Pay cycle</span></span>  | <span data-ttu-id="d23e0-143">sm</span><span class="sxs-lookup"><span data-stu-id="d23e0-143">sm</span></span>                    |
    | <span data-ttu-id="d23e0-144">Maksukausi</span><span class="sxs-lookup"><span data-stu-id="d23e0-144">Pay period</span></span> | <span data-ttu-id="d23e0-145">16.6.2017–30.6.2017</span><span class="sxs-lookup"><span data-stu-id="d23e0-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="d23e0-146">Anna **Ansioilmoitusrivi**-välilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="d23e0-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="d23e0-147">Rivi 1: **Ansioilmoitusrivi**-välilehti</span><span class="sxs-lookup"><span data-stu-id="d23e0-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="d23e0-148">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d23e0-148">Field</span></span>            | <span data-ttu-id="d23e0-149">Arvo</span><span class="sxs-lookup"><span data-stu-id="d23e0-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="d23e0-150">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="d23e0-150">Earnings code</span></span>    | <span data-ttu-id="d23e0-151">Normaali palkka</span><span class="sxs-lookup"><span data-stu-id="d23e0-151">Regular pay</span></span> |
    | <span data-ttu-id="d23e0-152">Määrä</span><span class="sxs-lookup"><span data-stu-id="d23e0-152">Quantity</span></span>         | <span data-ttu-id="d23e0-153">1,00</span><span class="sxs-lookup"><span data-stu-id="d23e0-153">1.00</span></span>        |
    | <span data-ttu-id="d23e0-154">Alue</span><span class="sxs-lookup"><span data-stu-id="d23e0-154">Rage</span></span>             | <span data-ttu-id="d23e0-155">30 000</span><span class="sxs-lookup"><span data-stu-id="d23e0-155">30,000</span></span>      |
    | <span data-ttu-id="d23e0-156">Rivin erittely -välilehti</span><span class="sxs-lookup"><span data-stu-id="d23e0-156">Line details tab</span></span> |             |
    | <span data-ttu-id="d23e0-157">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="d23e0-157">Manual</span></span>           | <span data-ttu-id="d23e0-158">(merkitty)</span><span class="sxs-lookup"><span data-stu-id="d23e0-158">(marked)</span></span>    |

    <span data-ttu-id="d23e0-159">Rivi 2: **Ansioilmoitusrivi**-välilehti</span><span class="sxs-lookup"><span data-stu-id="d23e0-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="d23e0-160">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d23e0-160">Field</span></span>            | <span data-ttu-id="d23e0-161">Arvo</span><span class="sxs-lookup"><span data-stu-id="d23e0-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="d23e0-162">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="d23e0-162">Earnings code</span></span>    | <span data-ttu-id="d23e0-163">Bonus</span><span class="sxs-lookup"><span data-stu-id="d23e0-163">Bonus</span></span>    |
    | <span data-ttu-id="d23e0-164">Määrä</span><span class="sxs-lookup"><span data-stu-id="d23e0-164">Quantity</span></span>         | <span data-ttu-id="d23e0-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="d23e0-165">1.0000</span></span>   |
    | <span data-ttu-id="d23e0-166">Osuus</span><span class="sxs-lookup"><span data-stu-id="d23e0-166">Rate</span></span>             | <span data-ttu-id="d23e0-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="d23e0-167">4250.00</span></span>  |
    | <span data-ttu-id="d23e0-168">Rivin erittely -välilehti</span><span class="sxs-lookup"><span data-stu-id="d23e0-168">Line details tab</span></span> |          |
    | <span data-ttu-id="d23e0-169">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="d23e0-169">Manual</span></span>           | <span data-ttu-id="d23e0-170">(merkitty)</span><span class="sxs-lookup"><span data-stu-id="d23e0-170">(marked)</span></span> |

    <span data-ttu-id="d23e0-171">Rivi 3: **Ansioilmoitusrivi**-välilehti</span><span class="sxs-lookup"><span data-stu-id="d23e0-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="d23e0-172">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d23e0-172">Field</span></span>           | <span data-ttu-id="d23e0-173">Arvo</span><span class="sxs-lookup"><span data-stu-id="d23e0-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="d23e0-174">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="d23e0-174">Earnings code</span></span>   | <span data-ttu-id="d23e0-175">Provisio</span><span class="sxs-lookup"><span data-stu-id="d23e0-175">Commission</span></span> |
    | <span data-ttu-id="d23e0-176">Määrä</span><span class="sxs-lookup"><span data-stu-id="d23e0-176">Quantity</span></span>        | <span data-ttu-id="d23e0-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="d23e0-177">1.0000</span></span>     |
    | <span data-ttu-id="d23e0-178">Osuus</span><span class="sxs-lookup"><span data-stu-id="d23e0-178">Rate</span></span>            | <span data-ttu-id="d23e0-179">! 299,00</span><span class="sxs-lookup"><span data-stu-id="d23e0-179">!,299.00</span></span>   |
    | <span data-ttu-id="d23e0-180">Osuus</span><span class="sxs-lookup"><span data-stu-id="d23e0-180">Rate</span></span>            | <span data-ttu-id="d23e0-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="d23e0-181">1,299.00</span></span>   |
    | <span data-ttu-id="d23e0-182">Rivin erittely -välilehti</span><span class="sxs-lookup"><span data-stu-id="d23e0-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="d23e0-183">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="d23e0-183">Manual</span></span>          | <span data-ttu-id="d23e0-184">(merkitty)</span><span class="sxs-lookup"><span data-stu-id="d23e0-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="d23e0-185">**Manuaalinen**-liukusäätimen asetukseksi on määritettävä **Kyllä** jokaisen ansioilmoitusrivin **Rivin erittely** -välilehdessä, jotta palkanlaskennan alkusaldot annetaan jokaiselle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="d23e0-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="d23e0-186">Valitse **Toiminto**-ruudussa **Vapauta ansioilmoitus** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="d23e0-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="d23e0-187">Avaa **Luo maksuilmoitukset** -sivulla valitsemalla **Toiminto**-ruudussa **Maksuilmoitus** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="d23e0-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="d23e0-188">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d23e0-188">Field</span></span>              | <span data-ttu-id="d23e0-189">Arvo</span><span class="sxs-lookup"><span data-stu-id="d23e0-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="d23e0-190">Maksupäivä</span><span class="sxs-lookup"><span data-stu-id="d23e0-190">Payment date</span></span>       | <span data-ttu-id="d23e0-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="d23e0-191">6/30/2017</span></span> |
    | <span data-ttu-id="d23e0-192">Maksusuorituksen tyyppi</span><span class="sxs-lookup"><span data-stu-id="d23e0-192">Payment run type</span></span>   | <span data-ttu-id="d23e0-193">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="d23e0-193">Manual</span></span>    |
    | <span data-ttu-id="d23e0-194">Poista kirjanpito käytöstä</span><span class="sxs-lookup"><span data-stu-id="d23e0-194">Disable accounting</span></span> |   <span data-ttu-id="d23e0-195">Kyllä</span><span class="sxs-lookup"><span data-stu-id="d23e0-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="d23e0-196">Tämä on käytettävissä vain, kun maksusuoritustyyppi on manuaalinen ja kun käyttäjä haluaa poistaa maksusuorituksen kirjanpidon käytöstä.</span><span class="sxs-lookup"><span data-stu-id="d23e0-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="d23e0-197">Valitse **OK** ja sulje **Infoloki**.</span><span class="sxs-lookup"><span data-stu-id="d23e0-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="d23e0-198">Miksi Poista kirjanpito käytöstä -liukusäätimen asetuksiksi on valittava Kyllä maksuilmoituksia luotaessa?</span><span class="sxs-lookup"><span data-stu-id="d23e0-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="d23e0-199">Kun liukusäätimen asetuksena **Kyllä**, maksuilmoituksen rivin jakaminen ja vienti estetään kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="d23e0-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="d23e0-200">Kirjanpidon summat päivitettiin aiemmin, kun vanhan järjestelmän tilien saldot vietiin.</span><span class="sxs-lookup"><span data-stu-id="d23e0-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="d23e0-201">Palkanlaskennan alkusaldojen viennin avulla voit luoda raportteja, jotka sisältävät aiempien vuosien tiedot sekä tunnistusrajat etuja ja verotusta varten.</span><span class="sxs-lookup"><span data-stu-id="d23e0-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="d23e0-202">C.</span><span class="sxs-lookup"><span data-stu-id="d23e0-202">C.</span></span> <span data-ttu-id="d23e0-203">Työntekijöiden maksuilmoitusten luominen</span><span class="sxs-lookup"><span data-stu-id="d23e0-203">Create pay statements for employees</span></span>

<span data-ttu-id="d23e0-204">Kun olet luonut alkusaldot sisältävät maksuilmoitukset, sinun on tarkistettava, että maksuilmoitukset vastaavat palkanlaskennan tietoja.</span><span class="sxs-lookup"><span data-stu-id="d23e0-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="d23e0-205">Sinun on myös päivitettävä etu- ja verotustiedot manuaalisesti vastaamaan aiemman palkanlaskentajärjestelmän tietoja.</span><span class="sxs-lookup"><span data-stu-id="d23e0-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="d23e0-206">Kun olet tarkistanut, että aiemman palkkalaskentajärjestelmään summat vastaavat nykyisten maksuilmoitusten summia, maksuilmoitukset on viimeisteltävä.</span><span class="sxs-lookup"><span data-stu-id="d23e0-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="d23e0-207">Avaa **Kaikki maksuilmoitukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="d23e0-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="d23e0-208">Korosta Michael Redmondin viimeksi luotu maksuilmoitus</span><span class="sxs-lookup"><span data-stu-id="d23e0-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="d23e0-209">Avaa **Maksuilmoitus**-sivu valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="d23e0-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="d23e0-210">Avaa **Edun vähennykset** -välilehti ja anna seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="d23e0-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="d23e0-211">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d23e0-211">Field</span></span>             | <span data-ttu-id="d23e0-212">Arvo</span><span class="sxs-lookup"><span data-stu-id="d23e0-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="d23e0-213">Etu</span><span class="sxs-lookup"><span data-stu-id="d23e0-213">Benefit</span></span>           | <span data-ttu-id="d23e0-214">Vähennyssumma</span><span class="sxs-lookup"><span data-stu-id="d23e0-214">Deduction amount</span></span> |
    | <span data-ttu-id="d23e0-215">Lisäeläkemaksut (Yhdysvalloissa 401K)</span><span class="sxs-lookup"><span data-stu-id="d23e0-215">401K</span></span>              | <span data-ttu-id="d23e0-216">Liity</span><span class="sxs-lookup"><span data-stu-id="d23e0-216">Participate</span></span>      |
    | <span data-ttu-id="d23e0-217">Hammashuolto</span><span class="sxs-lookup"><span data-stu-id="d23e0-217">Dental</span></span>            | <span data-ttu-id="d23e0-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="d23e0-218">SubSp</span></span>            |
    | <span data-ttu-id="d23e0-219">Huolettavien kulut</span><span class="sxs-lookup"><span data-stu-id="d23e0-219">Dep care spending</span></span> | <span data-ttu-id="d23e0-220">Liity</span><span class="sxs-lookup"><span data-stu-id="d23e0-220">Participate</span></span>      |
    | <span data-ttu-id="d23e0-221">Näkö</span><span class="sxs-lookup"><span data-stu-id="d23e0-221">Vision</span></span>            | <span data-ttu-id="d23e0-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="d23e0-222">SupSp</span></span>            |

5. <span data-ttu-id="d23e0-223">Anna **Edun osuudet** -välilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="d23e0-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="d23e0-224">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d23e0-224">Field</span></span>   | <span data-ttu-id="d23e0-225">Arvo</span><span class="sxs-lookup"><span data-stu-id="d23e0-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="d23e0-226">Etu</span><span class="sxs-lookup"><span data-stu-id="d23e0-226">Benefit</span></span> | <span data-ttu-id="d23e0-227">Osuussumma</span><span class="sxs-lookup"><span data-stu-id="d23e0-227">Contribution amount</span></span> |
    | <span data-ttu-id="d23e0-228">Lisäeläkemaksut (Yhdysvalloissa 401K)</span><span class="sxs-lookup"><span data-stu-id="d23e0-228">401K</span></span>    | <span data-ttu-id="d23e0-229">Liity</span><span class="sxs-lookup"><span data-stu-id="d23e0-229">Participate</span></span>         |
    | <span data-ttu-id="d23e0-230">Hammashuolto</span><span class="sxs-lookup"><span data-stu-id="d23e0-230">Dental</span></span>  | <span data-ttu-id="d23e0-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="d23e0-231">SubSp</span></span>               |
    | <span data-ttu-id="d23e0-232">Näkö</span><span class="sxs-lookup"><span data-stu-id="d23e0-232">Vision</span></span>  | <span data-ttu-id="d23e0-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="d23e0-233">SubSp</span></span>               |

6. <span data-ttu-id="d23e0-234">Anna **Verovähennykset** -välilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="d23e0-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="d23e0-235">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d23e0-235">Field</span></span>           | <span data-ttu-id="d23e0-236">Arvo</span><span class="sxs-lookup"><span data-stu-id="d23e0-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="d23e0-237">Alv-koodi</span><span class="sxs-lookup"><span data-stu-id="d23e0-237">Tax code</span></span>        | <span data-ttu-id="d23e0-238">Vähennyssumma</span><span class="sxs-lookup"><span data-stu-id="d23e0-238">Deduction amount</span></span> |
    | <span data-ttu-id="d23e0-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="d23e0-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="d23e0-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="d23e0-240">1600.00</span></span>          |
    | <span data-ttu-id="d23e0-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="d23e0-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="d23e0-242">825.75</span><span class="sxs-lookup"><span data-stu-id="d23e0-242">825.75</span></span>           |

7. <span data-ttu-id="d23e0-243">Anna **Vero-osuudet** -välilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="d23e0-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="d23e0-244">Valitse **Laske**.</span><span class="sxs-lookup"><span data-stu-id="d23e0-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="d23e0-245">Tarkista, että työntekijän maksuilmoituksen loppusumma vastaa vanhan järjestelmän vuoden alusta kertynyttä summaa.</span><span class="sxs-lookup"><span data-stu-id="d23e0-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="d23e0-246">Seuraavan vaiheen viimeistelyn voit jättää odottamaan, kunnes yleiset tarkistukset voi tehdä koostetusti kaikille palkkailmoituksille.</span><span class="sxs-lookup"><span data-stu-id="d23e0-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="d23e0-247">Kun kaikki on maksuilmoitukset on tarkistettu voit viimeistellä ne.</span><span class="sxs-lookup"><span data-stu-id="d23e0-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="d23e0-248">Samaa prosessi voidaan toistaa tarvittaessa erikseen kullekin edellisen vuoden vuosineljänneksille.</span><span class="sxs-lookup"><span data-stu-id="d23e0-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="d23e0-249">Se on tarpeellista vain, jos asiakas haluat nähdä tiedot neljännesvuosittain ilman, että tiedot olisi tarkistettava vanhasta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="d23e0-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="d23e0-250">Työntekijän alkusaldoa antaessa tapahtuu virhe</span><span class="sxs-lookup"><span data-stu-id="d23e0-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="d23e0-251">Tapahtumat voidaan peruuttaa ja antaa uudelleen.</span><span class="sxs-lookup"><span data-stu-id="d23e0-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="d23e0-252">Voit peruuttaa tapahtuman suorittamalla seuraavat vaiheet **Kaikki maksuilmoitukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d23e0-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="d23e0-253">Valitse **Palauta**.</span><span class="sxs-lookup"><span data-stu-id="d23e0-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="d23e0-254">Valitse **Kyllä**, kun sanoma "Kun palautat tämän maksuilmoituksen, maksuilmoitukselle luodaan vastakirjauksena palautusmaksuilmoitus.</span><span class="sxs-lookup"><span data-stu-id="d23e0-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="d23e0-255">Kumpaakaan maksuilmoitusta ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="d23e0-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="d23e0-256">Haluatko palauttaa tämän maksuilmoituksen?"</span><span class="sxs-lookup"><span data-stu-id="d23e0-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="d23e0-257">avautuu näyttöön.</span><span class="sxs-lookup"><span data-stu-id="d23e0-257">displays.</span></span> 

<span data-ttu-id="d23e0-258">Kun olet peruuttanut maksuilmoitukset, voit luoda työntekijälle uuden maksuilmoituksen aiemmin luodusta ansioilmoituksesta.</span><span class="sxs-lookup"><span data-stu-id="d23e0-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="d23e0-259">Muista korjata kaikki ansioilmoituksen virheelliset rivit ennen uuden maksuilmoituksen luontia ja luo sitten uudet maksuilmoitukset oikeilla summilla.</span><span class="sxs-lookup"><span data-stu-id="d23e0-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 

