---
title: Palkanlaskennan alkusaldojen antaminen
description: Tässä ohjeaiheessa käsitellään vaiheet, joilla ansiokoodien, vähennysten, etujen ja verojen alkusaldot annetaan.
author: andreabichsel
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
ms.openlocfilehash: 9272828fe5d6e0bf131ea66353a0d5c3c7b1c4bd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752147"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="ad2ac-103">Palkanlaskennan alkusaldojen syöttäminen</span><span class="sxs-lookup"><span data-stu-id="ad2ac-103">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad2ac-104">Tässä ohjeaiheessa käsitellään vaiheet, joilla ansiokoodien, vähennysten, etujen ja verojen alkusaldot annetaan.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-104">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="ad2ac-105">Kumppanit arvostavat näitä tietoja, sillä niiden avulla he voivat siirtää tiedot toisesta järjestelmästä uuteen käyttöönotettuun palkanlaskentaan.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-105">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="ad2ac-106">Palkanlaskennan alkusaldojen antamista varten tarkistetaan seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="ad2ac-106">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="ad2ac-107">Työntekijätietueet on viety järjestelmään ja ne ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-107">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="ad2ac-108">Seuraavat tiedot on määritetty työntekijöille:</span><span class="sxs-lookup"><span data-stu-id="ad2ac-108">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="ad2ac-109">Maksujaksot ja maksukaudet</span><span class="sxs-lookup"><span data-stu-id="ad2ac-109">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="ad2ac-110">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="ad2ac-110">Earning codes</span></span>
    - <span data-ttu-id="ad2ac-111">Verot</span><span class="sxs-lookup"><span data-stu-id="ad2ac-111">Taxes</span></span>
    - <span data-ttu-id="ad2ac-112">Edut ja vähennykset</span><span class="sxs-lookup"><span data-stu-id="ad2ac-112">Benefits and deductions</span></span>

- <span data-ttu-id="ad2ac-113">Yrityksen on pitänyt valita päivämäärä, johon palkanlaskennat alkusaldot voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-113">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="ad2ac-114">Vanhasta järjestelmästä kerättiin tiedot kaikista ansioista, eduista ja vähennyksistä, edun osuuksista, työntekijän verotuksesta sekä työnantajan verotuksesta ja vuoden alusta kertyneistä summista.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-114">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="ad2ac-115">Harkitse, kuinka yksityiskohtaisia tietoja tarvitset, kun aloitat alkusaldojen antamisen suunnittelun.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-115">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="ad2ac-116">Useimmat yritykset ilmoittavat yhden, konsolidoidun vuoden alusta kertyneen summan.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-116">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="ad2ac-117">Jos tietojen on kuitenkin oltava yksityiskohtaisempia, saldot voidaan ilmoittaa neljännesvuosittain.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-117">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="ad2ac-118">Tarvittavan tarkkuustason päättäminen määrittää, kuinka monta manuaalista maksuilmoitusta on luotava kullekin työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-118">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="ad2ac-119">Jos kyse on summasta vuoden alusta, kullekin työntekijälle tarvitaan vain yksi manuaalinen ilmoitus.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-119">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="ad2ac-120">Voit tehdä tämän käyttämällä edellisen järjestelmän viimeisen maksuilmoituksen vuoden alusta kertynyttä summaa uuteen palkanlaskentajärjestelmään ilmoitettavana summana.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-120">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="ad2ac-121">Seuraavassa esimerkissä näytetään, miten työntekijän palkanlaskennan alkusaldot, mukaan lukien ansiokoodit, edut ja vähennykset sekä verot, annetaan.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-121">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="ad2ac-122">Jos kyse olisi aidosta esimerkistä, jokaiselle ansiokoodille, edun vähennykselle, edun osuudelle sekä työntekijän ja työnantajan verotukselle olisi rivinimike, johon lisätty summa olisi summa vuoden alusta.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-122">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="ad2ac-123">Käytä tätä koodi- ja summaluetteloa luodessasi ansio- ja maksuilmoituksen manuaalisesti siten, että kirjanpito on poistettu käytöstä, palkanlaskennan alkusaldojen tuontia varten.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-123">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="ad2ac-124">Kirjanpito poistetaan käytöstä, koska et halua kirjata tätä alkusaldon maksuilmoitusta kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-124">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="ad2ac-125">Se tehtiin vanhassa järjestelmässä ja siirtyy uuteen järjestelmään, kun määrität alkusaldot kirjanpidossa.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-125">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="ad2ac-126">A.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-126">A.</span></span> <span data-ttu-id="ad2ac-127">Palkanlaskennan alkusaldoissa käytettävien ansiokoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ad2ac-127">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="ad2ac-128">Varmista palkanlaskennan alkusaldoja annettaessa, että Salli ansioilmoitushintojen muokkaus -vaihtoehto otettiin käyttöön, kun käytettävät ansiokoodit määritettiin.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-128">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="ad2ac-129">Kun vaihtoehto on käytössä, voit antaa summat manuaalisesti vanhasta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-129">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="ad2ac-130">B.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-130">B.</span></span> <span data-ttu-id="ad2ac-131">Alkusaldon sisältävän ansioilmoituksen luominen työntekijälle</span><span class="sxs-lookup"><span data-stu-id="ad2ac-131">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="ad2ac-132">Tässä vaiheessa kullekin työntekijälle luodaan manuaalisesti vanhan järjestelmän viimeisen maksukauden ansioilmoitus, joka luo ansioilmoitusrivit uuteen palkanlaskentajärjestelmään.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-132">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="ad2ac-133">Lisää yksi rivi kullekin ansiokoodille sekä summalle vuoden alusta ja tunneille.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-133">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="ad2ac-134">Mallivaiheet ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="ad2ac-134">The sample steps are as follows:</span></span>

1. <span data-ttu-id="ad2ac-135">Avaa **Kaikki ansioilmoitukset** -sivu ja valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-135">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="ad2ac-136">Kirjoita seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="ad2ac-136">Enter the following:</span></span> 

    | <span data-ttu-id="ad2ac-137">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-137">Field</span></span>      | <span data-ttu-id="ad2ac-138">Arvo</span><span class="sxs-lookup"><span data-stu-id="ad2ac-138">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="ad2ac-139">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-139">Worker</span></span>     | <span data-ttu-id="ad2ac-140">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="ad2ac-140">Michael Redmond</span></span>       |
    | <span data-ttu-id="ad2ac-141">Maksujakso</span><span class="sxs-lookup"><span data-stu-id="ad2ac-141">Pay cycle</span></span>  | <span data-ttu-id="ad2ac-142">sm</span><span class="sxs-lookup"><span data-stu-id="ad2ac-142">sm</span></span>                    |
    | <span data-ttu-id="ad2ac-143">Maksukausi</span><span class="sxs-lookup"><span data-stu-id="ad2ac-143">Pay period</span></span> | <span data-ttu-id="ad2ac-144">16.6.2017–30.6.2017</span><span class="sxs-lookup"><span data-stu-id="ad2ac-144">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="ad2ac-145">Anna **Ansioilmoitusrivi**-välilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ad2ac-145">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="ad2ac-146">Rivi 1: **Ansioilmoitusrivi**-välilehti</span><span class="sxs-lookup"><span data-stu-id="ad2ac-146">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="ad2ac-147">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-147">Field</span></span>            | <span data-ttu-id="ad2ac-148">Arvo</span><span class="sxs-lookup"><span data-stu-id="ad2ac-148">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="ad2ac-149">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="ad2ac-149">Earnings code</span></span>    | <span data-ttu-id="ad2ac-150">Normaali palkka</span><span class="sxs-lookup"><span data-stu-id="ad2ac-150">Regular pay</span></span> |
    | <span data-ttu-id="ad2ac-151">Määrä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-151">Quantity</span></span>         | <span data-ttu-id="ad2ac-152">1.00</span><span class="sxs-lookup"><span data-stu-id="ad2ac-152">1.00</span></span>        |
    | <span data-ttu-id="ad2ac-153">Osuus</span><span class="sxs-lookup"><span data-stu-id="ad2ac-153">Rate</span></span>             | <span data-ttu-id="ad2ac-154">30,000</span><span class="sxs-lookup"><span data-stu-id="ad2ac-154">30,000</span></span>      |
    | <span data-ttu-id="ad2ac-155">Rivin erittely -välilehti</span><span class="sxs-lookup"><span data-stu-id="ad2ac-155">Line details tab</span></span> |             |
    | <span data-ttu-id="ad2ac-156">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="ad2ac-156">Manual</span></span>           | <span data-ttu-id="ad2ac-157">(merkitty)</span><span class="sxs-lookup"><span data-stu-id="ad2ac-157">(marked)</span></span>    |

    <span data-ttu-id="ad2ac-158">Rivi 2: **Ansioilmoitusrivi**-välilehti</span><span class="sxs-lookup"><span data-stu-id="ad2ac-158">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="ad2ac-159">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-159">Field</span></span>            | <span data-ttu-id="ad2ac-160">Arvo</span><span class="sxs-lookup"><span data-stu-id="ad2ac-160">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="ad2ac-161">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="ad2ac-161">Earnings code</span></span>    | <span data-ttu-id="ad2ac-162">Bonus</span><span class="sxs-lookup"><span data-stu-id="ad2ac-162">Bonus</span></span>    |
    | <span data-ttu-id="ad2ac-163">Määrä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-163">Quantity</span></span>         | <span data-ttu-id="ad2ac-164">1.0000</span><span class="sxs-lookup"><span data-stu-id="ad2ac-164">1.0000</span></span>   |
    | <span data-ttu-id="ad2ac-165">Osuus</span><span class="sxs-lookup"><span data-stu-id="ad2ac-165">Rate</span></span>             | <span data-ttu-id="ad2ac-166">4250.00</span><span class="sxs-lookup"><span data-stu-id="ad2ac-166">4250.00</span></span>  |
    | <span data-ttu-id="ad2ac-167">Rivin erittely -välilehti</span><span class="sxs-lookup"><span data-stu-id="ad2ac-167">Line details tab</span></span> |          |
    | <span data-ttu-id="ad2ac-168">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="ad2ac-168">Manual</span></span>           | <span data-ttu-id="ad2ac-169">(merkitty)</span><span class="sxs-lookup"><span data-stu-id="ad2ac-169">(marked)</span></span> |

    <span data-ttu-id="ad2ac-170">Rivi 3: **Ansioilmoitusrivi**-välilehti</span><span class="sxs-lookup"><span data-stu-id="ad2ac-170">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="ad2ac-171">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-171">Field</span></span>           | <span data-ttu-id="ad2ac-172">Arvo</span><span class="sxs-lookup"><span data-stu-id="ad2ac-172">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="ad2ac-173">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="ad2ac-173">Earnings code</span></span>   | <span data-ttu-id="ad2ac-174">Provisio</span><span class="sxs-lookup"><span data-stu-id="ad2ac-174">Commission</span></span> |
    | <span data-ttu-id="ad2ac-175">Määrä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-175">Quantity</span></span>        | <span data-ttu-id="ad2ac-176">1.0000</span><span class="sxs-lookup"><span data-stu-id="ad2ac-176">1.0000</span></span>     |
    | <span data-ttu-id="ad2ac-177">Osuus</span><span class="sxs-lookup"><span data-stu-id="ad2ac-177">Rate</span></span>            | <span data-ttu-id="ad2ac-178">! 299,00</span><span class="sxs-lookup"><span data-stu-id="ad2ac-178">!,299.00</span></span>   |
    | <span data-ttu-id="ad2ac-179">Osuus</span><span class="sxs-lookup"><span data-stu-id="ad2ac-179">Rate</span></span>            | <span data-ttu-id="ad2ac-180">1,299.00</span><span class="sxs-lookup"><span data-stu-id="ad2ac-180">1,299.00</span></span>   |
    | <span data-ttu-id="ad2ac-181">Rivin erittely -välilehti</span><span class="sxs-lookup"><span data-stu-id="ad2ac-181">Line detail tab</span></span> |            |
    | <span data-ttu-id="ad2ac-182">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="ad2ac-182">Manual</span></span>          | <span data-ttu-id="ad2ac-183">(merkitty)</span><span class="sxs-lookup"><span data-stu-id="ad2ac-183">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="ad2ac-184">**Manuaalinen**-liukusäätimen asetukseksi on määritettävä **Kyllä** jokaisen ansioilmoitusrivin **Rivin erittely** -välilehdessä, jotta palkanlaskennan alkusaldot annetaan jokaiselle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-184">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="ad2ac-185">Valitse **Toiminto**-ruudussa **Vapauta ansioilmoitus** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-185">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="ad2ac-186">Avaa **Luo maksuilmoitukset** -sivulla valitsemalla **Toiminto**-ruudussa **Maksuilmoitus** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ad2ac-186">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="ad2ac-187">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-187">Field</span></span>              | <span data-ttu-id="ad2ac-188">Arvo</span><span class="sxs-lookup"><span data-stu-id="ad2ac-188">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="ad2ac-189">Maksupäivä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-189">Payment date</span></span>       | <span data-ttu-id="ad2ac-190">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="ad2ac-190">6/30/2017</span></span> |
    | <span data-ttu-id="ad2ac-191">Maksusuorituksen tyyppi</span><span class="sxs-lookup"><span data-stu-id="ad2ac-191">Payment run type</span></span>   | <span data-ttu-id="ad2ac-192">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="ad2ac-192">Manual</span></span>    |
    | <span data-ttu-id="ad2ac-193">Poista kirjanpito käytöstä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-193">Disable accounting</span></span> |   <span data-ttu-id="ad2ac-194">Kyllä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-194">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="ad2ac-195">Tämä on käytettävissä vain, kun maksusuoritustyyppi on manuaalinen ja kun käyttäjä haluaa poistaa maksusuorituksen kirjanpidon käytöstä.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-195">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="ad2ac-196">Valitse **OK** ja sulje **Infoloki**.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-196">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="ad2ac-197">Miksi Poista kirjanpito käytöstä -liukusäätimen asetuksiksi on valittava Kyllä maksuilmoituksia luotaessa?</span><span class="sxs-lookup"><span data-stu-id="ad2ac-197">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="ad2ac-198">Kun liukusäätimen asetuksena on **Kyllä**, maksuilmoituksen rivin jakaminen ja vienti kirjanpitoon estetään.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-198">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="ad2ac-199">Kirjanpidon summat päivitettiin aiemmin, kun vanhan järjestelmän tilien saldot vietiin.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-199">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="ad2ac-200">Palkanlaskennan alkusaldojen viennin avulla voit luoda raportteja, jotka sisältävät aiempien vuosien tiedot sekä tunnistusrajat etuja ja verotusta varten.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-200">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="ad2ac-201">C.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-201">C.</span></span> <span data-ttu-id="ad2ac-202">Työntekijöiden maksuilmoitusten luominen</span><span class="sxs-lookup"><span data-stu-id="ad2ac-202">Create pay statements for employees</span></span>

<span data-ttu-id="ad2ac-203">Kun olet luonut alkusaldot sisältävät maksuilmoitukset, sinun on tarkistettava, että maksuilmoitukset vastaavat palkanlaskennan tietoja.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-203">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="ad2ac-204">Sinun on myös päivitettävä etu- ja verotustiedot manuaalisesti vastaamaan aiemman palkanlaskentajärjestelmän tietoja.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-204">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="ad2ac-205">Kun olet tarkistanut, että aiemman palkkalaskentajärjestelmään summat vastaavat nykyisten maksuilmoitusten summia, maksuilmoitukset on viimeisteltävä.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-205">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="ad2ac-206">Avaa **Kaikki maksuilmoitukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-206">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="ad2ac-207">Korosta Michael Redmondin viimeksi luotu maksuilmoitus</span><span class="sxs-lookup"><span data-stu-id="ad2ac-207">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="ad2ac-208">Avaa **Maksuilmoitus**-sivu valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-208">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="ad2ac-209">Avaa **Edun vähennykset** -välilehti ja anna seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ad2ac-209">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="ad2ac-210">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-210">Field</span></span>             | <span data-ttu-id="ad2ac-211">Arvo</span><span class="sxs-lookup"><span data-stu-id="ad2ac-211">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="ad2ac-212">Etu</span><span class="sxs-lookup"><span data-stu-id="ad2ac-212">Benefit</span></span>           | <span data-ttu-id="ad2ac-213">Vähennyssumma</span><span class="sxs-lookup"><span data-stu-id="ad2ac-213">Deduction amount</span></span> |
    | <span data-ttu-id="ad2ac-214">Lisäeläkemaksut (Yhdysvalloissa 401K)</span><span class="sxs-lookup"><span data-stu-id="ad2ac-214">401K</span></span>              | <span data-ttu-id="ad2ac-215">Liity</span><span class="sxs-lookup"><span data-stu-id="ad2ac-215">Participate</span></span>      |
    | <span data-ttu-id="ad2ac-216">Hammashuolto</span><span class="sxs-lookup"><span data-stu-id="ad2ac-216">Dental</span></span>            | <span data-ttu-id="ad2ac-217">SubSp</span><span class="sxs-lookup"><span data-stu-id="ad2ac-217">SubSp</span></span>            |
    | <span data-ttu-id="ad2ac-218">Huolettavien kulut</span><span class="sxs-lookup"><span data-stu-id="ad2ac-218">Dep care spending</span></span> | <span data-ttu-id="ad2ac-219">Liity</span><span class="sxs-lookup"><span data-stu-id="ad2ac-219">Participate</span></span>      |
    | <span data-ttu-id="ad2ac-220">Näkö</span><span class="sxs-lookup"><span data-stu-id="ad2ac-220">Vision</span></span>            | <span data-ttu-id="ad2ac-221">SupSp</span><span class="sxs-lookup"><span data-stu-id="ad2ac-221">SupSp</span></span>            |

5. <span data-ttu-id="ad2ac-222">Anna **Edun osuudet** -välilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ad2ac-222">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="ad2ac-223">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-223">Field</span></span>   | <span data-ttu-id="ad2ac-224">Arvo</span><span class="sxs-lookup"><span data-stu-id="ad2ac-224">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="ad2ac-225">Etu</span><span class="sxs-lookup"><span data-stu-id="ad2ac-225">Benefit</span></span> | <span data-ttu-id="ad2ac-226">Osuussumma</span><span class="sxs-lookup"><span data-stu-id="ad2ac-226">Contribution amount</span></span> |
    | <span data-ttu-id="ad2ac-227">Lisäeläkemaksut (Yhdysvalloissa 401K)</span><span class="sxs-lookup"><span data-stu-id="ad2ac-227">401K</span></span>    | <span data-ttu-id="ad2ac-228">Liity</span><span class="sxs-lookup"><span data-stu-id="ad2ac-228">Participate</span></span>         |
    | <span data-ttu-id="ad2ac-229">Hammashuolto</span><span class="sxs-lookup"><span data-stu-id="ad2ac-229">Dental</span></span>  | <span data-ttu-id="ad2ac-230">SubSp</span><span class="sxs-lookup"><span data-stu-id="ad2ac-230">SubSp</span></span>               |
    | <span data-ttu-id="ad2ac-231">Näkö</span><span class="sxs-lookup"><span data-stu-id="ad2ac-231">Vision</span></span>  | <span data-ttu-id="ad2ac-232">SubSp</span><span class="sxs-lookup"><span data-stu-id="ad2ac-232">SubSp</span></span>               |

6. <span data-ttu-id="ad2ac-233">Anna **Verovähennykset** -välilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ad2ac-233">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="ad2ac-234">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ad2ac-234">Field</span></span>           | <span data-ttu-id="ad2ac-235">Arvo</span><span class="sxs-lookup"><span data-stu-id="ad2ac-235">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="ad2ac-236">Alv-koodi</span><span class="sxs-lookup"><span data-stu-id="ad2ac-236">Tax code</span></span>        | <span data-ttu-id="ad2ac-237">Vähennyssumma</span><span class="sxs-lookup"><span data-stu-id="ad2ac-237">Deduction amount</span></span> |
    | <span data-ttu-id="ad2ac-238">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="ad2ac-238">USA-FED-ER-FICA</span></span> | <span data-ttu-id="ad2ac-239">1600.00</span><span class="sxs-lookup"><span data-stu-id="ad2ac-239">1600.00</span></span>          |
    | <span data-ttu-id="ad2ac-240">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="ad2ac-240">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="ad2ac-241">825.75</span><span class="sxs-lookup"><span data-stu-id="ad2ac-241">825.75</span></span>           |

7. <span data-ttu-id="ad2ac-242">Anna **Vero-osuudet** -välilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="ad2ac-242">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="ad2ac-243">Valitse **Laske**.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-243">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="ad2ac-244">Tarkista, että työntekijän maksuilmoituksen loppusumma vastaa vanhan järjestelmän vuoden alusta kertynyttä summaa.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-244">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="ad2ac-245">Seuraavan vaiheen viimeistelyn voit jättää odottamaan, kunnes yleiset tarkistukset voi tehdä koostetusti kaikille palkkailmoituksille.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-245">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="ad2ac-246">Kun kaikki on maksuilmoitukset on tarkistettu voit viimeistellä ne.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-246">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="ad2ac-247">Samaa prosessi voidaan toistaa tarvittaessa erikseen kullekin edellisen vuoden vuosineljänneksille.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-247">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="ad2ac-248">Se on tarpeellista vain, jos asiakas haluat nähdä tiedot neljännesvuosittain ilman, että tiedot olisi tarkistettava vanhasta järjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-248">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="ad2ac-249">Työntekijän alkusaldoa antaessa tapahtuu virhe</span><span class="sxs-lookup"><span data-stu-id="ad2ac-249">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="ad2ac-250">Tapahtumat voidaan peruuttaa ja antaa uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-250">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="ad2ac-251">Voit peruuttaa tapahtuman suorittamalla seuraavat vaiheet **Kaikki maksuilmoitukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-251">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="ad2ac-252">Valitse **Palauta**.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-252">Click **Reverse**.</span></span>
2. <span data-ttu-id="ad2ac-253">Valitse **Kyllä**, kun sanoma "Kun palautat tämän maksuilmoituksen, maksuilmoitukselle luodaan vastakirjauksena palautusmaksuilmoitus.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-253">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="ad2ac-254">Kumpaakaan maksuilmoitusta ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-254">Neither pay statement can be edited.</span></span> <span data-ttu-id="ad2ac-255">Haluatko palauttaa tämän maksuilmoituksen?"</span><span class="sxs-lookup"><span data-stu-id="ad2ac-255">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="ad2ac-256">avautuu näyttöön.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-256">displays.</span></span> 

<span data-ttu-id="ad2ac-257">Kun olet peruuttanut maksuilmoitukset, voit luoda työntekijälle uuden maksuilmoituksen aiemmin luodusta ansioilmoituksesta.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-257">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="ad2ac-258">Muista korjata kaikki ansioilmoituksen virheelliset rivit ennen uuden maksuilmoituksen luontia ja luo sitten uudet maksuilmoitukset oikeilla summilla.</span><span class="sxs-lookup"><span data-stu-id="ad2ac-258">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]