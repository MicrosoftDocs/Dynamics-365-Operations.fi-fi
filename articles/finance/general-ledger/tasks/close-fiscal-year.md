---
title: Tilikauden sulkeminen
description: Tässä toimintaohjeessa selvitetään tilinkauden lopetusprosessi, joka siirtää saldot uuteen tilikauteen.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 593ab5b45cc0c2e1a8b876aa89de014fd9df1a13
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442848"
---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="b0529-103">Tilikauden sulkeminen</span><span class="sxs-lookup"><span data-stu-id="b0529-103">Close the fiscal year</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0529-104">Tässä toimintaohjeessa selvitetään tilinkauden lopetusprosessi, joka siirtää saldot uuteen tilikauteen.</span><span class="sxs-lookup"><span data-stu-id="b0529-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="b0529-105">Vahvista tilikauden lopetuksen parametrit</span><span class="sxs-lookup"><span data-stu-id="b0529-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="b0529-106">Valitse **Siirtymisruutu > Moduulit > Kirjanpito > Kirjanpidon asetukset > Kirjanpitoparametrit**.</span><span class="sxs-lookup"><span data-stu-id="b0529-106">Go to **Navigation pane > Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="b0529-107">Laajenna **Tilikauden lopetus** -osa.</span><span class="sxs-lookup"><span data-stu-id="b0529-107">Expand the **Fiscal year close** section.</span></span>
3. <span data-ttu-id="b0529-108">Valitse Kyllä tai Ei -arvo asetukselle **Poista päätöstapahtumat siirron yhteydessä**.</span><span class="sxs-lookup"><span data-stu-id="b0529-108">Select 'Yes' or 'No' for the **Delete close-of-year transactions during transfer** option.</span></span>
    
    <span data-ttu-id="b0529-109">Jos tilikausi on jo päätetty ja tilikauden lopetus suoritetaan uudelleen, tämä asetus on tärkeä.</span><span class="sxs-lookup"><span data-stu-id="b0529-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="b0529-110">Jos arvoksi asetetaan Kyllä, edellisen tilikauden lopetustosite poistetaan ja uusi tosite luodaan kaikkien tilien alkusaldoille.</span><span class="sxs-lookup"><span data-stu-id="b0529-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="b0529-111">Jos arvoksi asetetaan Ei, edellinen tosite säilytetään ja uusi tosite luodaan vain oikaisutapahtumille, jotka kirjattiin tilikauden lopetuksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b0529-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>

4. <span data-ttu-id="b0529-112">Valitse Kyllä- tai Ei-arvo asetukselle **Luo päätöstapahtumat siirron yhteydessä**.</span><span class="sxs-lookup"><span data-stu-id="b0529-112">Select 'Yes' or 'No' for the **Create closing transactions during transfer** option.</span></span>

    <span data-ttu-id="b0529-113">Jos arvoksi asetetaan Kyllä, luodaan kaksi tapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="b0529-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="b0529-114">Yksi tosite luodaan lopetettavaan tilivuoteen, jotta tuloskirjanpitotilit ovat tasassa, ja toinen tosite luodaan seuraavaan tilivuoteen alkusaldoille.</span><span class="sxs-lookup"><span data-stu-id="b0529-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="b0529-115">Jos arvo on Ei, yksi tosite luodaan uuden tilikauden alkusaldoille.</span><span class="sxs-lookup"><span data-stu-id="b0529-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  

5. <span data-ttu-id="b0529-116">Valitse Kyllä- tai Ei-arvo asetukselle **Muuta tilivuoden tilaksi pysyvästi suljettu**.</span><span class="sxs-lookup"><span data-stu-id="b0529-116">Select 'Yes' or 'No' for the **Set fiscal year status to permanently closed** option.</span></span>

    <span data-ttu-id="b0529-117">Jos arvoksi on asetettu Kyllä, tilikauden tilaksi asetetaan olla Suljettu pysyvästi.</span><span class="sxs-lookup"><span data-stu-id="b0529-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="b0529-118">Koska pysyvästi suljettua kautta ei voi avata uudelleen, on parasta asettaa tämän asetuksen arvoksi Ei.</span><span class="sxs-lookup"><span data-stu-id="b0529-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  

6. <span data-ttu-id="b0529-119">Valitse Kyllä- tai Ei-arvo asetukselle **Tositenumero syötettävä manuaalisesti tilikauden lopetusprosessin aikana**.</span><span class="sxs-lookup"><span data-stu-id="b0529-119">Select 'Yes' or 'No' for the **Voucher number must be filled in during the year end close** option.</span></span>

    <span data-ttu-id="b0529-120">Jos arvoksi asetetaan Kyllä, tositenumero on syötettävä manuaalisesti tilikauden lopetusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="b0529-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="b0529-121">Tositenumeron luomiseen ei käytetä numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="b0529-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="b0529-122">On suositeltavinta arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b0529-122">It's a best practice to set this to Yes.</span></span>  

7. <span data-ttu-id="b0529-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b0529-123">Close the page.</span></span>
8. <span data-ttu-id="b0529-124">Valitse **Kirjanpito > Kausi suljettu > Tilikauden lopetus**.</span><span class="sxs-lookup"><span data-stu-id="b0529-124">Go to **General ledger > Period close > Year end close**.</span></span>
9. <span data-ttu-id="b0529-125">Luo tilikauden lopetusmalli valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b0529-125">Click **New** to create a year-end close template.</span></span>

    <span data-ttu-id="b0529-126">Mallin voi luoda yritysjoukolle, jolle tilikauden lopetus suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="b0529-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="b0529-127">Tätä mallia voidaan käyttää uudelleen vuodesta toiseen.</span><span class="sxs-lookup"><span data-stu-id="b0529-127">This template can be reused year after year.</span></span>  

10. <span data-ttu-id="b0529-128">Kirjoita **Ryhmän nimi** -kenttään tilikauden lopetusmallin nimi.</span><span class="sxs-lookup"><span data-stu-id="b0529-128">In the **Group name** field, enter a year-end close template name..</span></span>
11. <span data-ttu-id="b0529-129">Valitse **Kirjanpidon vuosikalenteri** -kentässä tilikausi, jolle malli luodaan.</span><span class="sxs-lookup"><span data-stu-id="b0529-129">In the **Fiscal calendar** field, select the fiscal year for which the template will be created.</span></span>

    <span data-ttu-id="b0529-130">Vain yritykset, jotka käyttävät samaa tilikautta, voidaan liittää tilikauden lopetusmallin ryhmään.</span><span class="sxs-lookup"><span data-stu-id="b0529-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="b0529-131">Tämä johtuu siitä, että tilikauden lopetus tehdään valitsemalla tilikausi, ei päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b0529-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  

12. <span data-ttu-id="b0529-132">Valitse **toimintoruudussa** **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b0529-132">On the **Action pane**, click **Save**.</span></span>
13. <span data-ttu-id="b0529-133">Valitse **Oikeushenkilöt** -osasta **Lisää** valitaksesi tämän mallin juridiset entiteetit.</span><span class="sxs-lookup"><span data-stu-id="b0529-133">In the **Legal entities** section, click **Add** to select the legal entities for this template.</span></span>
    
    <span data-ttu-id="b0529-134">Yritykset voidaan lisätä joko valitsemalla ne tai valitsemalla organisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="b0529-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="b0529-135">Organisaatiohierarkiasta lisätään ainoastaan yritykset, joilla on sama tilikausi.</span><span class="sxs-lookup"><span data-stu-id="b0529-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  

14. <span data-ttu-id="b0529-136">Valitse joko yritykset tai organisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="b0529-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="b0529-137">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0529-137">Click **OK**.</span></span>
16. <span data-ttu-id="b0529-138">Valitse Kyllä tai Ei asetuksessa **Siirrä tasedimensiot**.</span><span class="sxs-lookup"><span data-stu-id="b0529-138">Select 'Yes' or 'No' in the **Transfer balance sheet dimension**.</span></span>

    <span data-ttu-id="b0529-139">Suositeltavinta on asettaa tämän asetuksen arvoksi Kyllä tasetileille.</span><span class="sxs-lookup"><span data-stu-id="b0529-139">It's best practice to set this option to Yes for Balance sheet accounts.</span></span> <span data-ttu-id="b0529-140">Tämä säilyttää kirjattujen tapahtumien taloushallinnon dimensiot, kun alkusaldot luodaan tasetileille.</span><span class="sxs-lookup"><span data-stu-id="b0529-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span> <span data-ttu-id="b0529-141">Tulostileille voit valita, säilytetäänkö taloushallinnon dimensiot (Sulje kaikki), kun saldot siirretään jakamattomiin voittoihin tai voit valita, että taloushallinnon dimension vaihdetaan eri dimensioarvoihin (Sulje yksi).</span><span class="sxs-lookup"><span data-stu-id="b0529-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="b0529-142">Jos valitset arvoksi Sulje yksi, voit määrittää tietyn dimensioarvon kullekin dimensiolle tai halutessaan myös jättää arvon tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="b0529-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  

17. <span data-ttu-id="b0529-143">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b0529-143">Click **Save**.</span></span>
18. <span data-ttu-id="b0529-144">Aloita tilikauden lopetus valitsemalla **Suorita tilikauden lopetus** **toimintoruudusta**.</span><span class="sxs-lookup"><span data-stu-id="b0529-144">Start the year-end close by choosing **Run fiscal close** on the **Action Pane**.</span></span> <span data-ttu-id="b0529-145">Tilikauden lopetus ajetaan valitulle mallille.</span><span class="sxs-lookup"><span data-stu-id="b0529-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="b0529-146">Valitse kaikki mallin yritykset tai niiden osajoukko, joille tilikauden lopetus suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="b0529-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>

    <span data-ttu-id="b0529-147">Kun tilikauden lopetus ajetaan ensimmäisen kerran, useimmat organisaatiot tuottavat alkusaldot ajamalla tilikauden lopetuksen kaikille mallin yrityksille.</span><span class="sxs-lookup"><span data-stu-id="b0529-147">When first running the year-end close, to get beginning balance,s most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="b0529-148">Jos oikaisuja tehdään lopetuksen jälkeen, tilikauden lopetuksen voi ajaa vain niille yrityksille, joilla oikaisuja on.</span><span class="sxs-lookup"><span data-stu-id="b0529-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  

20. <span data-ttu-id="b0529-149">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0529-149">Click **OK**.</span></span>
21. <span data-ttu-id="b0529-150">Valitse lopetettava tilikausi.</span><span class="sxs-lookup"><span data-stu-id="b0529-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="b0529-151">Kirjoita arvo kenttään **Tosite**.</span><span class="sxs-lookup"><span data-stu-id="b0529-151">In the **Voucher field**, type a value.</span></span> <span data-ttu-id="b0529-152">Se on suositeltavinta sisällyttää tilikausi tositteen numeroon, jotta luotu tilikauden lopetustosite on helpompi löytää.</span><span class="sxs-lookup"><span data-stu-id="b0529-152">It's best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="b0529-153">Tilikauden lopetus ajetaan oletusarvoisesti eräajona.</span><span class="sxs-lookup"><span data-stu-id="b0529-153">The year-end close defaults to run in batch.</span></span> <span data-ttu-id="b0529-154">On suositeltavinta ajaa pitkään kestävät prosessit eräajona.</span><span class="sxs-lookup"><span data-stu-id="b0529-154">It's best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="b0529-155">Tämä on yleensä pitkäkestoinen prosessi, minkä vuoksi oletusasetus on eräajon käyttäminen.</span><span class="sxs-lookup"><span data-stu-id="b0529-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="b0529-156">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0529-156">Click **OK**.</span></span>

