---
title: Intian Vero vähennettynä lähteissä (TDS) -yhteenveto
description: Tämä ohjeaihe sisältää yksityiskohtaisia tietoja Intian Vero vähennettynä lähteissä (TDS) -aiheesta. TDS-dokumentaatio sisältää tämän ominaisuuden toiminnot.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023221"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="49c8d-104">Intian Vero vähennettynä lähteissä (TDS) -yhteenveto</span><span class="sxs-lookup"><span data-stu-id="49c8d-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49c8d-105">Tämä ohjeaihe sisältää yksityiskohtaisia tietoja Intian Vero vähennettynä lähteissä (TDS) -aiheesta.</span><span class="sxs-lookup"><span data-stu-id="49c8d-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="49c8d-106">TDS-dokumentaatio sisältää tämän ominaisuuden toiminnot.</span><span class="sxs-lookup"><span data-stu-id="49c8d-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="49c8d-107">Siinä kerrotaan myös, miten TDS:n perusasetukset tehdään, tapahtumien TDS lasketaan, TDS-selvitysprosessi suoritetaan, TDS-sertifikaattien numerot kirjataan ja TDS-kyselyt, TDS-lausekkeet ja TDS-sertifikaatit luodaan.</span><span class="sxs-lookup"><span data-stu-id="49c8d-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="49c8d-108">Dokumentaatio sisältää seuraavat aiheet:</span><span class="sxs-lookup"><span data-stu-id="49c8d-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="49c8d-109">TDS:n perusasetus</span><span class="sxs-lookup"><span data-stu-id="49c8d-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="49c8d-110">Kaavan suunnittelu- ja raja-arvotoiminto, jota käytetään TDS-laskennassa</span><span class="sxs-lookup"><span data-stu-id="49c8d-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="49c8d-111">Laskujen, maksujen, velkakirjojen ja konsernin sisäisten tapahtumien TDS:n laskeminen</span><span class="sxs-lookup"><span data-stu-id="49c8d-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="49c8d-112">Kausittainen TDS-selvitysprosessi ja TDS-summien tilitys TDS-viranomaistoimittajille</span><span class="sxs-lookup"><span data-stu-id="49c8d-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="49c8d-113">TDS-sertifikaattien numeroiden ja päivämäärien kirjaaminen ja päivittäminen</span><span class="sxs-lookup"><span data-stu-id="49c8d-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="49c8d-114">Johdanto TDS:ään</span><span class="sxs-lookup"><span data-stu-id="49c8d-114">Introduction to TDS</span></span>

<span data-ttu-id="49c8d-115">Tuloverolaissa 1961 palvelun vastaanottaja vähentää tuloveron lähteestä ennakkomaksun tai saldon laskennan aikaan sen mukaan, kumpi on ensin.</span><span class="sxs-lookup"><span data-stu-id="49c8d-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="49c8d-116">Maksun suorittajan on vähennettävä veron summa ja maksettava vain nettosaldo palvelun tarjoajalle.</span><span class="sxs-lookup"><span data-stu-id="49c8d-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="49c8d-117">TDS:ää käytetään palveluissa, jotka valtio määrittää, ja vero vähennetään hintojen avulla, jotka valtio määrittää ajanjaksolle.</span><span class="sxs-lookup"><span data-stu-id="49c8d-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="49c8d-118">Vähennys perustuu sen yksikön tilaan, joka vastaanottaa maksun tai tarjoaa palvelun.</span><span class="sxs-lookup"><span data-stu-id="49c8d-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="49c8d-119">Tiloja voivat olla **Yksittäinen**, **Hindujen jakamaton perhe** (**HUF**), **Yritys**, **Firma**, **Henkilöyhdistys** (**AOP**), **Yksilöiden elin** (**BOI**) ja **Paikallinen viranomainen**.</span><span class="sxs-lookup"><span data-stu-id="49c8d-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="49c8d-120">Seuraavissa osissa on luettelo palveluista, joissa TDS on käytössä, kuten Intian hallitus on määrittänyt.</span><span class="sxs-lookup"><span data-stu-id="49c8d-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="49c8d-121">**Asukkaat**</span><span class="sxs-lookup"><span data-stu-id="49c8d-121">**Residents**</span></span>

- <span data-ttu-id="49c8d-122">Tulot palkoista (§ 192)</span><span class="sxs-lookup"><span data-stu-id="49c8d-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="49c8d-123">Tulot arvopapereiden koroista (§ 193)</span><span class="sxs-lookup"><span data-stu-id="49c8d-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="49c8d-124">Tulot osingosta (§ 194)</span><span class="sxs-lookup"><span data-stu-id="49c8d-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="49c8d-125">Tulot korosta (§ 194A)</span><span class="sxs-lookup"><span data-stu-id="49c8d-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="49c8d-126">Tulot arpajaisista tai tehtävistä (§ 194B)</span><span class="sxs-lookup"><span data-stu-id="49c8d-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="49c8d-127">Voitto hevoskilpailuista jne. (§ 194BB)</span><span class="sxs-lookup"><span data-stu-id="49c8d-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="49c8d-128">Urakoitsijat ja alihankkijat (§ 194C)</span><span class="sxs-lookup"><span data-stu-id="49c8d-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="49c8d-129">Vakuutuskomissio (§ 194D)</span><span class="sxs-lookup"><span data-stu-id="49c8d-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="49c8d-130">Tulot kansallisen säästöjärjestelmän talletuksista (§ 194EE)</span><span class="sxs-lookup"><span data-stu-id="49c8d-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="49c8d-131">Tulot sijoitusrahastosta tai UTI:stä (§ 194F)</span><span class="sxs-lookup"><span data-stu-id="49c8d-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="49c8d-132">Palkkiot, korvaukset, palkinnot jne. myynnistä tai arpajaisista (§ 194G)</span><span class="sxs-lookup"><span data-stu-id="49c8d-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="49c8d-133">Komissio- tai välittäjämaksu (§ 194H)</span><span class="sxs-lookup"><span data-stu-id="49c8d-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="49c8d-134">Vuokra (§ 194I)</span><span class="sxs-lookup"><span data-stu-id="49c8d-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="49c8d-135">Ammattipalvelu (§ 194J)</span><span class="sxs-lookup"><span data-stu-id="49c8d-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="49c8d-136">Tulot yksiköistä (§ 194K)</span><span class="sxs-lookup"><span data-stu-id="49c8d-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="49c8d-137">Korvauksen maksaminen tietyn kiinteän omaisuuden hankinnasta (§ 194LA)</span><span class="sxs-lookup"><span data-stu-id="49c8d-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="49c8d-138">**Ulkomailla asuvat**</span><span class="sxs-lookup"><span data-stu-id="49c8d-138">**Non-residents**</span></span>

- <span data-ttu-id="49c8d-139">Maksut ulkomailla asuville urheilijoille tai urheiluliitolle (§ 194E)</span><span class="sxs-lookup"><span data-stu-id="49c8d-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="49c8d-140">Muut summat (§ 195)</span><span class="sxs-lookup"><span data-stu-id="49c8d-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="49c8d-141">Tulot, jotka koskevat ulkomailla asuvien yksiköitä (§ 196A)</span><span class="sxs-lookup"><span data-stu-id="49c8d-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="49c8d-142">Tulot ulkomaan valuutan joukkovelkakirjoista tai intialaisen yrityksen osakkeista (§ 196C)</span><span class="sxs-lookup"><span data-stu-id="49c8d-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="49c8d-143">Ulkomaisten institutionaalisten sijoittajien tulot arvopapereista (§ 196D)</span><span class="sxs-lookup"><span data-stu-id="49c8d-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="49c8d-144">Palkka ja kaikki muut positiiviset tulot missä tahansa tulotasossa (§ 192)</span><span class="sxs-lookup"><span data-stu-id="49c8d-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="49c8d-145">Korko arvopapereista (§ 193)</span><span class="sxs-lookup"><span data-stu-id="49c8d-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="49c8d-146">Muut korot kuin arvopapereiden korot (§ 194A)</span><span class="sxs-lookup"><span data-stu-id="49c8d-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="49c8d-147">Maksut urakoitsijoille ja alihankkijoille (§ 194C)</span><span class="sxs-lookup"><span data-stu-id="49c8d-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="49c8d-148">Voitot arpajaisista tai ristisanatehtävistä (§ 194B)</span><span class="sxs-lookup"><span data-stu-id="49c8d-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="49c8d-149">Voitot hevoskilpailuista (§ 194BB)</span><span class="sxs-lookup"><span data-stu-id="49c8d-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="49c8d-150">Vakuutustoimikunta, joka kattaa kaikki maksut vakuutusliiketoiminnan hankinnasta (§ 194D)</span><span class="sxs-lookup"><span data-stu-id="49c8d-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="49c8d-151">Muut korot kuin arvopapereille maksettavat korot, jotka maksetaan ulkomailla asuville, jotka eivät ole yhtiöitä, tai ulkomaisille yrityksille (§ 195)</span><span class="sxs-lookup"><span data-stu-id="49c8d-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="49c8d-152">Maksu ulkomailla asuvalle urheilijalle, mukaan lukien urheilija- tai urheiluliitto tai -laitos.</span><span class="sxs-lookup"><span data-stu-id="49c8d-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="49c8d-153">Ulkomailla asuvien urheilijoiden tapauksessa maksut mainoksista sekä kaikista Intian peleistä/urheilulajeista peräisin olevista artikkeleista sanomalehdissä, aikakauslehdissä jne.</span><span class="sxs-lookup"><span data-stu-id="49c8d-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="49c8d-154">sisältyvät (§ 194E)</span><span class="sxs-lookup"><span data-stu-id="49c8d-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="49c8d-155">Maksu NSS:n \[National Savings Scheme\] mukaisista talletuksista (§ 194EE)</span><span class="sxs-lookup"><span data-stu-id="49c8d-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="49c8d-156">Sijoitusrahaston tai UTI: n suorittaman osuuksien takaisinoston maksu (§ 194F)</span><span class="sxs-lookup"><span data-stu-id="49c8d-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="49c8d-157">Komissio- tai välittäjämaksu (§ 194H)</span><span class="sxs-lookup"><span data-stu-id="49c8d-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="49c8d-158">Vuokramaksu (§ 194I)</span><span class="sxs-lookup"><span data-stu-id="49c8d-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="49c8d-159">Maksujen maksaminen ammatillisia tai teknisiä palveluita varten (§ 194J)</span><span class="sxs-lookup"><span data-stu-id="49c8d-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="49c8d-160">Palkkiot arpajaisten lippujen kauppiaille, jakelijoille, ostajille ja myyjille, mukaan lukien korvaus tai palkinto tällaisista lipuista (§ 194G)</span><span class="sxs-lookup"><span data-stu-id="49c8d-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="49c8d-161">Ostettujen yksiköiden tulot ulkomaan valuuttana tai pitkäaikaisena pääoman voittona, jotka ovat peräisin näiden ulkomaan valuuttana ostettujen yksiköiden siirrosta (§ 196B)</span><span class="sxs-lookup"><span data-stu-id="49c8d-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="49c8d-162">Velkakirjoista ja osakkeista maksetun koron tai osingon maksaminen ulkomailla asuville (§ 196C)</span><span class="sxs-lookup"><span data-stu-id="49c8d-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="49c8d-163">TDS lasketaan ostoista, myynnistä, myyntipalautuksista, hyvityslaskuista, käyttöomaisuushankinnoista, ennakkomaksuista, ennakkomaksuista, velkakirjoista, työverosta ja konsernin sisäisistä tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="49c8d-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="49c8d-164">Intian nykyisessä veroskenaariossa TDS:ää ei lasketa myyntitapahtumien perusteella.</span><span class="sxs-lookup"><span data-stu-id="49c8d-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="49c8d-165">Järjestelmä sisältää kuitenkin provision, joka laskee myynnin tapahtumien TDS-palautuskelpoisen määrän erityisesti konserniyritysten välisissä tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="49c8d-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="49c8d-166">TDS:n laskenta ottaa aina huomioon TDS-komponentille määritetyn raja-arvon ja poikkeusrajan.</span><span class="sxs-lookup"><span data-stu-id="49c8d-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="49c8d-167">Kausittainen TDS-selvitysprosessi on suoritettava ja TDS-maksut täytyy selvittää TDS-järjestelmän toimittajien kanssa.</span><span class="sxs-lookup"><span data-stu-id="49c8d-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="49c8d-168">Toimittajilta tai asiakkailta vastaanotettujen TDS-todistusten sertifikaattien numeroita ja päivämääriä voi tallentaa ja päivittää.</span><span class="sxs-lookup"><span data-stu-id="49c8d-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="49c8d-169">Lisäksi lomakkeen 26Q ja lomakkeen 27Q neljännesvuosittaiset ilmoitukset ja TDS:n lomakkeen 16A todistus voidaan luoda talousosastossa.</span><span class="sxs-lookup"><span data-stu-id="49c8d-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="49c8d-170">TDS:n määrittäminen ja käyttö</span><span class="sxs-lookup"><span data-stu-id="49c8d-170">Setting up and working with TDS</span></span>

<span data-ttu-id="49c8d-171">Seuraavassa on yhteenveto TDS:n asetus- ja käsittelyprosessista:</span><span class="sxs-lookup"><span data-stu-id="49c8d-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="49c8d-172">**TDS:n asetukset:**</span><span class="sxs-lookup"><span data-stu-id="49c8d-172">**TDS setup:**</span></span>

    - <span data-ttu-id="49c8d-173">Parametrien asetukset:</span><span class="sxs-lookup"><span data-stu-id="49c8d-173">Parameter setup:</span></span>

        - <span data-ttu-id="49c8d-174">Aktivoi kirjanpidon parametreissa TDS:ään liittyvät parametrit.</span><span class="sxs-lookup"><span data-stu-id="49c8d-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="49c8d-175">Määritä kirjanpidon parametreissa ennakonpidätysmaksujen numerosarja.</span><span class="sxs-lookup"><span data-stu-id="49c8d-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="49c8d-176">Määritä myyntireskontran ja ostoreskontran parametrit.</span><span class="sxs-lookup"><span data-stu-id="49c8d-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="49c8d-177">Perusasetukset:</span><span class="sxs-lookup"><span data-stu-id="49c8d-177">Basic setup:</span></span>

        - <span data-ttu-id="49c8d-178">Määritä yrityksen, asiakkaiden ja toimittajien TDS-rekisterinumerot.</span><span class="sxs-lookup"><span data-stu-id="49c8d-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="49c8d-179">Määritä TDS-komponenttiryhmät.</span><span class="sxs-lookup"><span data-stu-id="49c8d-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="49c8d-180">Määritä TDS-komponentit, liitä niihin TDS-komponenttiryhmät ja määritä niiden raja-arvo ja poikkeusraja.</span><span class="sxs-lookup"><span data-stu-id="49c8d-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="49c8d-181">Määritä TDS-viranomaiset.</span><span class="sxs-lookup"><span data-stu-id="49c8d-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="49c8d-182">Määritä TDS- tilityskaudet.</span><span class="sxs-lookup"><span data-stu-id="49c8d-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="49c8d-183">Määritä TDS-verokoodit ja liitä niihin TDS-komponentit.</span><span class="sxs-lookup"><span data-stu-id="49c8d-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="49c8d-184">Määritä TDS-veroryhmät ja liitä niihin TDS-verokoodit.</span><span class="sxs-lookup"><span data-stu-id="49c8d-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="49c8d-185">Kaavan suunnittelutoiminnossa voit määrittää kaavan TDS:n laskemiseksi TDS-ryhmälle.</span><span class="sxs-lookup"><span data-stu-id="49c8d-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="49c8d-186">Tallenna TDS-huojennustodistuksen numerot.</span><span class="sxs-lookup"><span data-stu-id="49c8d-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="49c8d-187">Kirjanpitotilit ja yrityksen asetukset:</span><span class="sxs-lookup"><span data-stu-id="49c8d-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="49c8d-188">Määritä TDS:n osto- ja myyntireskontran kirjanpitotilit.</span><span class="sxs-lookup"><span data-stu-id="49c8d-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="49c8d-189">Määritä TAN-numero ja vähennystyyppinen luokka yritykselle.</span><span class="sxs-lookup"><span data-stu-id="49c8d-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="49c8d-190">Muut asetukset:</span><span class="sxs-lookup"><span data-stu-id="49c8d-190">Other setup:</span></span>

        - <span data-ttu-id="49c8d-191">Määritä maksusuunnitelma, joka sisältää TDS-kohdistuksen.</span><span class="sxs-lookup"><span data-stu-id="49c8d-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="49c8d-192">Määritä TDS-viranomaisen maksujen maksukulutyyppi.</span><span class="sxs-lookup"><span data-stu-id="49c8d-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="49c8d-193">Määritä toimittajien ja asiakkaiden TDS-ryhmien, pysyvien tilinumeroiden ja TAN-koodien tiedot.</span><span class="sxs-lookup"><span data-stu-id="49c8d-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="49c8d-194">**TDS-laskenta tapahtumissa:**</span><span class="sxs-lookup"><span data-stu-id="49c8d-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="49c8d-195">Laskut ja maksut</span><span class="sxs-lookup"><span data-stu-id="49c8d-195">Invoices and payments</span></span>
    - <span data-ttu-id="49c8d-196">Velkakirjat</span><span class="sxs-lookup"><span data-stu-id="49c8d-196">Promissory notes</span></span>
    - <span data-ttu-id="49c8d-197">Ennakkomaksut</span><span class="sxs-lookup"><span data-stu-id="49c8d-197">Advance payments</span></span>
    - <span data-ttu-id="49c8d-198">Ennakkomaksut</span><span class="sxs-lookup"><span data-stu-id="49c8d-198">Prepayments</span></span>

3. <span data-ttu-id="49c8d-199">**TDS-tilitys:**</span><span class="sxs-lookup"><span data-stu-id="49c8d-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="49c8d-200">Kausittainen TDS-selvitysprosessi</span><span class="sxs-lookup"><span data-stu-id="49c8d-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="49c8d-201">TDS-maksujen tilitys TDS-viranomaistoimittajille ja TDS:n challan-tietojen luominen</span><span class="sxs-lookup"><span data-stu-id="49c8d-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="49c8d-202">**TDS-kyselyt, -lausekkeet ja -sertifikaatti:**</span><span class="sxs-lookup"><span data-stu-id="49c8d-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="49c8d-203">TDS-sertifikaattien numeroiden ja päivämäärien kirjaaminen ja päivittäminen.</span><span class="sxs-lookup"><span data-stu-id="49c8d-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="49c8d-204">Luo TDS-kysely ja kirjattu TDS-kysely.</span><span class="sxs-lookup"><span data-stu-id="49c8d-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="49c8d-205">Luo lomakkeen 27A, lomakkeen 26Q ja lomakkeen 27Q neljännesvuosittaiset TDS- ja e-TDS-laskelmat.</span><span class="sxs-lookup"><span data-stu-id="49c8d-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="49c8d-206">Luo lomakkeen 16A TDS-sertifikaatti.</span><span class="sxs-lookup"><span data-stu-id="49c8d-206">Generate a Form 16A TDS certificate.</span></span>
