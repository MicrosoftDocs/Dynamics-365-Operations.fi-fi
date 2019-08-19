---
title: Kirjanpidon kirjauskansion käsittely
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Finance and Operationsin ominaisuuksista, joiden avulla yleisen kirjauskansion käsittely on helpompaa ja jonka avulla voidaan myös varmistaa, että kerättävät tiedot ovat oikeita eikä sisäisessä tarkistuksessa ole ongelmia.
author: ShylaThompson
manager: AnnBe
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7efd250428f7675b96674dd02e3aeccefe653fe
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839228"
---
# <a name="general-journal-processing"></a><span data-ttu-id="5600b-103">Kirjanpidon kirjauskansion käsittely</span><span class="sxs-lookup"><span data-stu-id="5600b-103">General journal processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5600b-104">Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Finance and Operationsin ominaisuuksista, joiden avulla yleisen kirjauskansion käsittely on helpompaa ja jonka avulla voidaan myös varmistaa, että kerättävät tiedot ovat oikeita eikä sisäisessä tarkistuksessa ole ongelmia.</span><span class="sxs-lookup"><span data-stu-id="5600b-104">This topic describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help ensure that correct data is captured and internal control isn't compromised.</span></span>  

## <a name="journal-names"></a><span data-ttu-id="5600b-105">Kirjauskansioiden nimet</span><span class="sxs-lookup"><span data-stu-id="5600b-105">Journal names</span></span>

<span data-ttu-id="5600b-106">Kirjauskansioiden nimet on yksi tärkeimmistä määritettävistä alueista.</span><span class="sxs-lookup"><span data-stu-id="5600b-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="5600b-107">On hyvä ajatus määrittää määrätyt kirjauskansionimet kullekin tarkoitukselle, kuten konsernin sisäinen, jaksotusoikaisut ja virheiden korjaus.</span><span class="sxs-lookup"><span data-stu-id="5600b-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="5600b-108">Voit räätälöidä kunkin kirjauskansion nimen niin, että tietojen lisäys kullekin tarkoitukselle on helppoa ja turvallista.</span><span class="sxs-lookup"><span data-stu-id="5600b-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="5600b-109">**Kirjauskansioiden nimet**-sivulla voit määrittää seuraavat elementit:</span><span class="sxs-lookup"><span data-stu-id="5600b-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="5600b-110">**Työnkulun hyväksyntä** – Sisäisen valvonnan parantamiseksi määritä kirjauskansion työnkulkuja, jotka muodostavat oleelliset rajat tarkastus- ja hyväksyntävaiheille perustuen ehtoihin, kuten veloituksen kokonaissummaan.</span><span class="sxs-lookup"><span data-stu-id="5600b-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="5600b-111">Voit määrittää työnkulkuja yleisille kirjauskansioille **Kirjanpidon työnkulut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="5600b-111">You set up workflows for the general journals on the **General ledger workflows** page.</span></span>
-   <span data-ttu-id="5600b-112">**Oletusarvot** – Valitse oletusarvo vastatileille, valuutoille ja taloushallinnon dimensioille.</span><span class="sxs-lookup"><span data-stu-id="5600b-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="5600b-113">**Kirjauskansion hallinta** – Voit määrittää yritystä, tilityyppiä ja segmenttiarvoja koskevia rajoituksia.</span><span class="sxs-lookup"><span data-stu-id="5600b-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="5600b-114">**Esimerkkejä**</span><span class="sxs-lookup"><span data-stu-id="5600b-114">**Examples**</span></span>

<span data-ttu-id="5600b-115">Kirjauskansion nimeä voidaan käyttää vain oikaisuihin.</span><span class="sxs-lookup"><span data-stu-id="5600b-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="5600b-116">Tässä tapauksessa voit määrittää, että vain **Kirjanpito**-tilityyppi on kelvollinen kaikissa yhtiöissä.</span><span class="sxs-lookup"><span data-stu-id="5600b-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> 

<span data-ttu-id="5600b-117">[![Kirjauskansion hallinnan tilityypit](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="5600b-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="5600b-118">Kirjauskansion nimeä voidaan käyttää vain määrätylle segmentille tai päätilien alueelle.</span><span class="sxs-lookup"><span data-stu-id="5600b-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> 

<span data-ttu-id="5600b-119">[![Kirjauskansion hallintasegmentti](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="5600b-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="5600b-120">Vaihtoehto **Automaattinen peruutus** on saatavilla yleisissä kirjauskansioissa.</span><span class="sxs-lookup"><span data-stu-id="5600b-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="5600b-121">Sinulla voi esimerkiksi alla näkyvän esimerkin mukaisesti olla jaksotusoikaisu, jossa itse tiedostoa ei ole vielä käsitelty.</span><span class="sxs-lookup"><span data-stu-id="5600b-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="5600b-122">[![Kirjauskansion takaisinkirjaukset](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="5600b-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="5600b-123">Microsoft Excelin lisäosa kirjauskansiovientejä varten tarjoaa lisäautomaatiota ja tekee tietojen syötöstä helpompaa.</span><span class="sxs-lookup"><span data-stu-id="5600b-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="5600b-124">Toiminto **Avaa rivit Excelissä** on saatavilla **Yleinen kirjauskansio-** ja **Kirjaustosite** -sivuilla.</span><span class="sxs-lookup"><span data-stu-id="5600b-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="5600b-125">Voit määrittää toistuvia kirjauskansioita **Kausikirjauskansiot**-sivulla ja siten automatisoida kirjauskansion käsittelyn.</span><span class="sxs-lookup"><span data-stu-id="5600b-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="5600b-126">Voit käyttää tositemalleja milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="5600b-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="5600b-127">**Yleiset kirjauskansiot** -sivulla löytyy **Tallenna-** ja **Valitse tositemalli** -toiminnot **Kirjaustosite**-sivulla tositerivien kohdassa **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="5600b-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="5600b-128">Liittyvät asetukset</span><span class="sxs-lookup"><span data-stu-id="5600b-128">Related setup</span></span>
<span data-ttu-id="5600b-129">Seuraavat asetukset eivät koske pelkästään yleisiä kirjauskansioita vaan auttavat takaamaan, että oikeat tiedot tulevat kirjatuiksi ja että kirjaaminen on helppoa.</span><span class="sxs-lookup"><span data-stu-id="5600b-129">The following setup isn't specific to general journals, but will help ensure that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="5600b-130">Päätili</span><span class="sxs-lookup"><span data-stu-id="5600b-130">Main account</span></span>

<span data-ttu-id="5600b-131">Päätilin asetukset tarjoaa useita vaihtoehtoja yleisen kirjauskansion käsittelyyn:</span><span class="sxs-lookup"><span data-stu-id="5600b-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="5600b-132">**Veloitus-/Hyvitystarve** – Käytä tätä vaihtoehtoa, jos päätili on rajoitettu debet- tai kredit-tapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="5600b-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="5600b-133">Asetukset tarkistetaan, kun kirjauskansio vahvistetaan tai kirjataan.</span><span class="sxs-lookup"><span data-stu-id="5600b-133">The setup is verified when a journal is validated or posted.</span></span>

-   <span data-ttu-id="5600b-134">**Oletusvastatili**</span><span class="sxs-lookup"><span data-stu-id="5600b-134">**Default offset account**</span></span>
-   <span data-ttu-id="5600b-135">**Keskeytetty** – Keskeytä päätilille tehtävä tietojen kirjaaminen kaikkien tai tiettyjen yhtiöiden osalta.</span><span class="sxs-lookup"><span data-stu-id="5600b-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entity.</span></span>
-   <span data-ttu-id="5600b-136">**Älä salli manuaalista täyttämistä** – Estä käyttäjiä täyttämästä manuaalisesti tilin arvo kirjauskansioissa.</span><span class="sxs-lookup"><span data-stu-id="5600b-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="5600b-137">**Oletusvaluutta/valuutan vahvistaminen**</span><span class="sxs-lookup"><span data-stu-id="5600b-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="5600b-138">**Yrityksen ohitukset** – Nämä asetukset liittyvät kiinteästi määriteltyyn yritykseen:</span><span class="sxs-lookup"><span data-stu-id="5600b-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="5600b-139">**Arvonlisäveron oletusarvo/vahvistaminen**</span><span class="sxs-lookup"><span data-stu-id="5600b-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="5600b-140">**Oletusdimensio** – **Ei määritetty** tai **Kiinteä arvo**.</span><span class="sxs-lookup"><span data-stu-id="5600b-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="5600b-141">**Kiinteä arvo** auttaa varmistamaan, että kaikki tälle päätilille tehtävät kirjaukset käyttävät aina dimensioarvoa, jonka tilaksi on määritetty **Kiinteä**.</span><span class="sxs-lookup"><span data-stu-id="5600b-141">**Fixed value** will help ensure that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="5600b-142">**Kirjauksen oikeellisuustarkistus**</span><span class="sxs-lookup"><span data-stu-id="5600b-142">**Posting validation**</span></span>
    -   <span data-ttu-id="5600b-143">**Käyttäjän oikeellisuustarkistus** – Tällä vaihtoehdolla valvotaan, millä käyttäjillä on oikeus tehdä kirjauksia päätilille.</span><span class="sxs-lookup"><span data-stu-id="5600b-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="5600b-144">**Kirjaustyypin oikeellisuustarkistus** – Tällä vaihtoehdolla valvotaan, mitkä kirjaustyypit ovat sallittuja päätilillä.</span><span class="sxs-lookup"><span data-stu-id="5600b-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="5600b-145">Kirjanpitorakenteet ja lisäsääntöjen rakenteet</span><span class="sxs-lookup"><span data-stu-id="5600b-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="5600b-146">Kirjanpitorakenteet ja lisäsääntöjen rakenteet ovat erittäin tärkeitä sen varmistamisessa, että taloushallinnon raportoinnissa ja suorituskyvyn mittaamisessa tarvittavat tiedot ja asiakirjat kerätään kirjauskansion käsittelyn ja muun dokumentaation yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="5600b-146">Accounting structures and advanced rules structures are extremely important for ensuring that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="5600b-147">Kirjanpitorakenteiden ja lisäsääntöjen rakenteiden ansiosta voit räätälöidä tietojen syöttörutiinin.</span><span class="sxs-lookup"><span data-stu-id="5600b-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="5600b-148">Voit sallia tietojen syötön vain kussakin tilanteessa asianmukaisille taloushallinnon dimensioille sekä määrätä vaatimuksen siitä, että kerätään aina vaadittuja ja oikeita tietoja.</span><span class="sxs-lookup"><span data-stu-id="5600b-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that required and accurate data always be captured.</span></span>

<span data-ttu-id="5600b-149">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="5600b-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="5600b-150">[Suunnittelu: tilikartta](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="5600b-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="5600b-151">Luo kirjauskansioiden lisäsäännöt</span><span class="sxs-lookup"><span data-stu-id="5600b-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="5600b-152">Kirjauskansioviennin luonti mallin avulla</span><span class="sxs-lookup"><span data-stu-id="5600b-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="5600b-153">Luo ja vahvista kirjauskansiot</span><span class="sxs-lookup"><span data-stu-id="5600b-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="5600b-154">Kausittaisten kirjauskansioiden kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="5600b-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="5600b-155">Käsittele kirjanpidon kohdistuskirjauskansio</span><span class="sxs-lookup"><span data-stu-id="5600b-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a><span data-ttu-id="5600b-156">Kirjauksen simulointi</span><span class="sxs-lookup"><span data-stu-id="5600b-156">Simulate posting</span></span>
<span data-ttu-id="5600b-157">Löydät **Kirjauksen simulointi** -kohdan useimpien kirjauskansioiden **Vahvista**-valikosta.</span><span class="sxs-lookup"><span data-stu-id="5600b-157">You can find **Simulate posting** on the **Validate** menu for most journals.</span></span> <span data-ttu-id="5600b-158">Kun vahvistat kirjauskansion **Vahvista**-toiminnon avulla, järjestelmä testaa kirjauskansiota tiettyjen virhetilanteiden varalta.</span><span class="sxs-lookup"><span data-stu-id="5600b-158">When you validate a journal using the **Validate** function, the system tests the journal for specific error conditions.</span></span> <span data-ttu-id="5600b-159">Jos käytät **Kirjauksen simulointi** -toimintoa, järjestelmä suorittaa kaikki samat prosessit, jotka suoritetaan kirjauksen aikana kirjauskansiota kirjaamatta.</span><span class="sxs-lookup"><span data-stu-id="5600b-159">If you use the **Simulate posting** function, the system runs all of the same processes that are run during posting without actually posting the journal.</span></span> <span data-ttu-id="5600b-160">Voit siten tarkastella näytettyjä kirjausviestejä, korjata mahdollisesti löytämäsi virheet ja kirjata sitten kirjauskansion napsauttamalla **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="5600b-160">You can then review the posting messages that are displayed, fix any errors that you find, and then click the **Post** menu to post the journal.</span></span> 

<span data-ttu-id="5600b-161">**Kirjauksen simulointi** ei ole käytettävissä eräkäsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="5600b-161">**Simulate posting** is not available for batch processing.</span></span> <span data-ttu-id="5600b-162">Käytettävissä on kuitenkin koodi, jonka avulla voidaan simuloida eräkirjausta, ja kehittäjät voivat ulottaa koodin lisäämään tämän toiminnon.</span><span class="sxs-lookup"><span data-stu-id="5600b-162">However, there is code available to simulate posting in batch and developers can extend the code to add that functionality.</span></span>  
