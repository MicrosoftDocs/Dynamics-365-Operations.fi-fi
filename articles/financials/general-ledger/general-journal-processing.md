---
title: "Kirjanpidon kirjauskansion käsittely"
description: "Tässä artikkelissa kerrotaan Microsoft Dynamics 365 for Finance and Operationsin ominaisuuksista, joiden avulla yleisen kirjauskansion käsittely on helpompaa ja joiden avulla voidaan myös varmistaa, että kerättävät tiedot ovat oikeita eikä sisäisessä tarkistuksessa ole ongelmia."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: eb46613f805999753c2ab73ffb91a6fdae04c68e
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="general-journal-processing"></a><span data-ttu-id="d7040-103">Kirjanpidon kirjauskansion käsittely</span><span class="sxs-lookup"><span data-stu-id="d7040-103">General journal processing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d7040-104">Tässä artikkelissa kerrotaan Microsoft Dynamics 365 for Finance and Operationsin ominaisuuksista, joiden avulla yleisen kirjauskansion käsittely on helpompaa ja joiden avulla voidaan myös varmistaa, että kerättävät tiedot ovat oikeita eikä sisäisessä tarkistuksessa ole ongelmia.</span><span class="sxs-lookup"><span data-stu-id="d7040-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="d7040-105">Kirjauskansioiden nimet</span><span class="sxs-lookup"><span data-stu-id="d7040-105">Journal names</span></span>

<span data-ttu-id="d7040-106">Kirjauskansioiden nimet on yksi tärkeimmistä määritettävistä alueista.</span><span class="sxs-lookup"><span data-stu-id="d7040-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="d7040-107">On hyvä ajatus määrittää määrätyt kirjauskansionimet kullekin tarkoitukselle, kuten konsernin sisäinen, jaksotusoikaisut ja virheiden korjaus.</span><span class="sxs-lookup"><span data-stu-id="d7040-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="d7040-108">Voit räätälöidä kunkin kirjauskansion nimen niin, että tietojen lisäys kullekin tarkoitukselle on helppoa ja turvallista.</span><span class="sxs-lookup"><span data-stu-id="d7040-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="d7040-109">**Kirjauskansioiden nimet**-sivulla voit määrittää seuraavat elementit:</span><span class="sxs-lookup"><span data-stu-id="d7040-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="d7040-110">**Työnkulun hyväksyntä** – Sisäisen valvonnan parantamiseksi määritä kirjauskansion työnkulkuja, jotka muodostavat oleelliset rajat tarkastus- ja hyväksyntävaiheille perustuen ehtoihin, kuten veloituksen kokonaissummaan.</span><span class="sxs-lookup"><span data-stu-id="d7040-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="d7040-111">Voit määrittää työnkulkuja yleisille kirjauskansioille **Kirjanpidon työnkulut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d7040-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="d7040-112">**Oletusarvot** – Valitse oletusarvo vastatileille, valuutoille ja taloushallinnon dimensioille.</span><span class="sxs-lookup"><span data-stu-id="d7040-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="d7040-113">**Kirjauskansion hallinta** – Voit määrittää yritystä, tilityyppiä ja segmenttiarvoja koskevia rajoituksia.</span><span class="sxs-lookup"><span data-stu-id="d7040-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="d7040-114">**Esimerkkejä**</span><span class="sxs-lookup"><span data-stu-id="d7040-114">**Examples**</span></span>

<span data-ttu-id="d7040-115">Kirjauskansion nimeä voidaan käyttää vain oikaisuihin.</span><span class="sxs-lookup"><span data-stu-id="d7040-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="d7040-116">Tässä tapauksessa voit määrittää, että vain **Kirjanpito**-tilityyppi on kelvollinen kaikissa yhtiöissä.</span><span class="sxs-lookup"><span data-stu-id="d7040-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="d7040-117">[![Kirjauskansion hallinnan tilityypit](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="d7040-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="d7040-118">Kirjauskansion nimeä voidaan käyttää vain määrätylle segmentille tai päätilien alueelle.</span><span class="sxs-lookup"><span data-stu-id="d7040-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="d7040-119">[![Kirjauskansion hallintasegmentti](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="d7040-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="d7040-120">Vaihtoehto **Automaattinen peruutus** on saatavilla yleisissä kirjauskansioissa.</span><span class="sxs-lookup"><span data-stu-id="d7040-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="d7040-121">Sinulla voi esimerkiksi alla näkyvän esimerkin mukaisesti olla jaksotusoikaisu, jossa itse tiedostoa ei ole vielä käsitelty.</span><span class="sxs-lookup"><span data-stu-id="d7040-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="d7040-122">[![Kirjauskansion takaisinkirjaukset](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="d7040-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="d7040-123">Microsoft Excelin lisäosa kirjauskansiovientejä varten tarjoaa lisäautomaatiota ja tekee tietojen syötöstä helpompaa.</span><span class="sxs-lookup"><span data-stu-id="d7040-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="d7040-124">Toiminto **Avaa rivit Excelissä** on saatavilla **Yleinen kirjauskansio-** ja **Kirjaustosite** -sivuilla.</span><span class="sxs-lookup"><span data-stu-id="d7040-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="d7040-125">Voit määrittää toistuvia kirjauskansioita **Kausikirjauskansiot**-sivulla ja siten automatisoida kirjauskansion käsittelyn.</span><span class="sxs-lookup"><span data-stu-id="d7040-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="d7040-126">Voit käyttää tositemalleja milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="d7040-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="d7040-127">**Yleiset kirjauskansiot** -sivulla löytyy **Tallenna-** ja **Valitse tositemalli** -toiminnot **Kirjaustosite**-sivulla tositerivien kohdassa **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="d7040-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="d7040-128">Liittyvät asetukset</span><span class="sxs-lookup"><span data-stu-id="d7040-128">Related setup</span></span>
<span data-ttu-id="d7040-129">Seuraavat asetukset eivät koske nimenomaan yleisiä kirjauskansioita, mutta ne auttavat takaamaan, että oikeat tiedot tulevat kirjatuiksi ja että kirjaaminen on helppoa.</span><span class="sxs-lookup"><span data-stu-id="d7040-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="d7040-130">Päätili</span><span class="sxs-lookup"><span data-stu-id="d7040-130">Main account</span></span>

<span data-ttu-id="d7040-131">Päätilin asetukset tarjoaa useita vaihtoehtoja yleisen kirjauskansion käsittelyyn:</span><span class="sxs-lookup"><span data-stu-id="d7040-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="d7040-132">**Veloitus-/Hyvitystarve** – Käytä tätä vaihtoehtoa, jos päätili on rajoitettu debet- tai kredit-tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="d7040-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="d7040-133">Asetukset tarkistetaan, kun kirjauskansio vahvistetaan tai kirjataan.</span><span class="sxs-lookup"><span data-stu-id="d7040-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="d7040-134">**Oletusvastatili**</span><span class="sxs-lookup"><span data-stu-id="d7040-134">**Default offset account**</span></span>
-   <span data-ttu-id="d7040-135">**Keskeytetty** – Keskeytä päätilille tehtävä tietojen kirjaaminen kaikkien yhtiöiden osalta tai määrättyjen yritysten osalta.</span><span class="sxs-lookup"><span data-stu-id="d7040-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="d7040-136">**Älä salli manuaalista täyttämistä** – Estä käyttäjiä täyttämästä manuaalisesti tilin arvo kirjauskansioissa.</span><span class="sxs-lookup"><span data-stu-id="d7040-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="d7040-137">**Oletusvaluutta/valuutan vahvistaminen**</span><span class="sxs-lookup"><span data-stu-id="d7040-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="d7040-138">**Yrityksen ohitukset** – Nämä asetukset liittyvät kiinteästi määriteltyyn yritykseen:</span><span class="sxs-lookup"><span data-stu-id="d7040-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="d7040-139">**Arvonlisäveron oletusarvo/vahvistaminen**</span><span class="sxs-lookup"><span data-stu-id="d7040-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="d7040-140">**Oletusdimensio** – **Ei määritetty** tai **Kiinteä arvo**.</span><span class="sxs-lookup"><span data-stu-id="d7040-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="d7040-141">**Kiinteä arvo** auttaa varmistamaan, että kaikki tälle päätilille tehtävät kirjaukset käyttävät aina dimensioarvoa, joka on määritetty **Kiinteäksi**.</span><span class="sxs-lookup"><span data-stu-id="d7040-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="d7040-142">**Kirjauksen oikeellisuustarkistus**</span><span class="sxs-lookup"><span data-stu-id="d7040-142">**Posting validation**</span></span>
    -   <span data-ttu-id="d7040-143">**Käyttäjän oikeellisuustarkistus** – Tällä vaihtoehdolla valvotaan, millä käyttäjillä on oikeus tehdä kirjauksia päätilille.</span><span class="sxs-lookup"><span data-stu-id="d7040-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="d7040-144">**Kirjaustyypin oikeellisuustarkistus** – Tällä vaihtoehdolla valvotaan, mitkä kirjaustyypit ovat sallittuja päätilillä.</span><span class="sxs-lookup"><span data-stu-id="d7040-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="d7040-145">Kirjanpitorakenteet ja lisäsääntöjen rakenteet</span><span class="sxs-lookup"><span data-stu-id="d7040-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="d7040-146">Kirjanpitorakenteet ja lisäsääntöjen rakenteet ovat erittäin tärkeitä sen varmistamisessa, että taloushallinnon raportoinnissa ja suorituskyvyn mittaamisessa tarvittavat tiedot ja asiakirjat kerätään kirjanpidon kirjauskansion käsittelyn yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="d7040-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="d7040-147">Kirjanpitorakenteiden ja lisäsääntöjen rakenteiden ansiosta voit räätälöidä tietojen syöttörutiinin.</span><span class="sxs-lookup"><span data-stu-id="d7040-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="d7040-148">Voit sallia tietojen syötön vain kussakin tilanteessa asianmukaisille taloushallinnon dimensioille sekä toimeenpanna vaatimuksen, että pakolliset ja oikeat tiedot tulevat aina kerätyiksi.</span><span class="sxs-lookup"><span data-stu-id="d7040-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="d7040-149">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="d7040-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="d7040-150">[Suunnittelu: tilikartta](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="d7040-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="d7040-151">Luo kirjauskansioiden lisäsäännöt</span><span class="sxs-lookup"><span data-stu-id="d7040-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="d7040-152">Kirjauskansioviennin luonti mallin avulla</span><span class="sxs-lookup"><span data-stu-id="d7040-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="d7040-153">Luo ja vahvista kirjauskansiot</span><span class="sxs-lookup"><span data-stu-id="d7040-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="d7040-154">Kirjaa kausittaiset kirjauskansiot</span><span class="sxs-lookup"><span data-stu-id="d7040-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="d7040-155">Käsittele kirjanpidon kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="d7040-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



