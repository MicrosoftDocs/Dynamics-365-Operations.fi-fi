---
title: ALV:n palautus matkalaskuissa
description: Tässä ohjeaiheessa kerrotaan, miten kelvollisten arvonlisävero- eli ALV-tapahtumien palautukset saadaan.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70a53282bf1d140cb24108fe98e48aa82f783be5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177532"
---
# <a name="vat-recovery-in-expense-management"></a><span data-ttu-id="9c4bd-103">ALV:n palautus matkalaskuissa</span><span class="sxs-lookup"><span data-stu-id="9c4bd-103">VAT recovery in Expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c4bd-104">Saadakseen kelvollisten ALV-tapahtumien palautukset yrityksen tai organisaation tunnistettava, kerättävä, varmistettava ja lähettävä tarkat tiedot.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-104">To receive refunds on eligible value-added tax (VAT) transactions, a company or organization must identify, collect, verify, and submit accurate information.</span></span> <span data-ttu-id="9c4bd-105">Tämä prosessi sisältää useita tehtäviä ja yrityksen koon mukaan se voi koskea useita työntekijöitä tai rooleja.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-105">This process includes multiple tasks and, depending on the size of your company, can include several employees or roles.</span></span>

<span data-ttu-id="9c4bd-106">ALV:n palauttaminen kulujenhallinnan avulla edellyttää, että seuraavat edellytykset toteutuvat:</span><span class="sxs-lookup"><span data-stu-id="9c4bd-106">To recover VAT by using Expense management, the following prerequisites must be completed:</span></span>

- <span data-ttu-id="9c4bd-107">Verokoodit on luotava maille/alueille, jotka kohdistetaan kululuokkiin.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-107">Tax codes must be created for countries/regions that are allocated to expense categories.</span></span>
- <span data-ttu-id="9c4bd-108">Jokaiselle verokoodille on luotava arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-108">A sales tax group must be created for each tax code.</span></span>
- <span data-ttu-id="9c4bd-109">Jokaiselle arvonlisäveroryhmälle on luotava nimikkeen arvonlisäverokoodi.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-109">An item sales tax code must be created for each sales tax group.</span></span>

<span data-ttu-id="9c4bd-110">Kun edellytykset täyttyvät, työntekijät voivat pyytää ALV-tapahtumien palautusta seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-110">After the prerequisites are completed, employees follow these steps to request refunds for VAT transactions.</span></span>

1. <span data-ttu-id="9c4bd-111">Anna kuluraportissa luottokorttitapahtumien verotiedot, jotta kelvolliset ALV-tapahtuvat voidaan tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-111">On an expense report, enter tax information about credit card transactions to identify eligible VAT refunds.</span></span>
2. <span data-ttu-id="9c4bd-112">Varmista, että kaikki verotiedot on annettu, ja kirjaa sitten kuluraportti.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-112">Make sure that all tax information is complete, and then post the expense report.</span></span>
3. <span data-ttu-id="9c4bd-113">Käsittele kulut, jotka ovat kelvollisia kansainväliseen ALV-palautukseen.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-113">Process expenses that are eligible for international VAT recovery.</span></span>
4. <span data-ttu-id="9c4bd-114">Kirjaa kansainväliset palautukset lähettämällä ALV-palautustiedot ulkopuoliselle toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-114">Send VAT recovery data to the third-party vendor to file international recovery returns.</span></span>
5. <span data-ttu-id="9c4bd-115">Käsittele kotimaisten ALV-palautusten kulut.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-115">Process expenses for domestic VAT recovery.</span></span>

<span data-ttu-id="9c4bd-116">Seuraavissa osissa on esimerkkejä, joista näkee, miten Contoson työntekijät suorittavat kunkin tehtävän.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-116">The following sections provide examples that show how Contoso employees complete each step.</span></span>

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a><span data-ttu-id="9c4bd-117">Anna kuluraportissa luottokorttitapahtumien verotiedot, jotta kelvolliset ALV-tapahtuvat voidaan tunnistaa</span><span class="sxs-lookup"><span data-stu-id="9c4bd-117">On an expense report, enter tax information about credit card transactions to identify eligible VAT refunds</span></span>

<span data-ttu-id="9c4bd-118">Nancy on Yhdysvalloissa toimiva Contoson myyntiedustaja, joka palasi äskettäin Isoon-Britanniaan suuntautuneelta myyntimatkalta.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-118">Nancy, a Contoso sales representative who is based in the US, recently returned from a sales trip to the United Kingdom.</span></span> <span data-ttu-id="9c4bd-119">Hän maksoi matkan aikana joitakin aterioita omalla luottokortillaan.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-119">During her trip, she incurred some personal credit card expenses for meals.</span></span> <span data-ttu-id="9c4bd-120">Nancyn on nyt luotava kuluraportti kulujen täsmäyttämistä varten.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-120">Nancy must now create an expense report to reconcile her expenses.</span></span>

<span data-ttu-id="9c4bd-121">Kun Nancy antaa tietoja kuluraportissa, hänen valitsee **Iso-Britannia** **Muokkaa kuluraporttia** -sivun **Maa/alue**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-121">When Nancy enters information on her expense report, she selects **United Kingdom** in the **Country/region** field on the **Edit expense report** page.</span></span> <span data-ttu-id="9c4bd-122">Arvonlisäveroryhmien luettelo suodatetaan sitten näyttämään vain ryhmät, jotka koskevat Isoa-Britanniaa.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-122">The list of sales tax groups is then filtered so that it shows only the groups that apply to the United Kingdom.</span></span> <span data-ttu-id="9c4bd-123">Nancy valitsee **Iso-Britannia 001** -arvonlisäveroryhmän ja valitse sitten **Ateriat**-nimikkeen alv-ryhmä.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-123">Nancy selects the **United Kingdom 001** sales tax group and then selects the **Meals** item sales tax group.</span></span> <span data-ttu-id="9c4bd-124">Hän lisää sitten uuden tapahtuman majoitukselle.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-124">She then adds a new transaction for her lodging.</span></span> <span data-ttu-id="9c4bd-125">Koska Ison-Britannian kohdalla on majoitukselle vain yksi alv-ryhmä ja nimikkeen alv-ryhmä, nämä tiedot täytetään automaattisesti Nancyn kuluraporttiin.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-125">Because there is only one sales tax group and item sales tax group for lodging in the United Kingdom, this information is automatically filled in on Nancy's expense report.</span></span>

<span data-ttu-id="9c4bd-126">Contoson käytännön mukaisesti kaikilla kuluilla on oltava vastaava kuitti.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-126">Per Contoso policy, all expenses must have a matching receipt.</span></span> <span data-ttu-id="9c4bd-127">Tämän vuoksi Nancy saa kuluraportin tallennuksen yhteydessä ilmoituksen, jonka mukaan hänen on liitettävä jokaisen kuluraportissa mainitun tapahtuman kuitti.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-127">Therefore, when Nancy saves her expense report, she receives a message that states that she must attach a receipt for each transaction that she listed on her expense report.</span></span> <span data-ttu-id="9c4bd-128">Nancy varmistaa, että on liittänyt kunkin tapahtuman kuitin digitaalisena kuvana kuluraporttiin ja lähettää raportin sitten hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-128">Nancy verifies that she has attached a digital image of each transaction receipt to her expense report and then submits her report for approval.</span></span> <span data-ttu-id="9c4bd-129">Hän lähettää sitten paperikuitit taustajärjestelmän käsittelyryhmälle.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-129">She then sends the paper receipts to the back-office processing team.</span></span> <span data-ttu-id="9c4bd-130">Tämä ryhmä lähettää alv-palautustiedot ulkopuoliselle toimittajalle. Tämä toimittaja kirjaa Contoson kansainväliset alv-palautukset.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-130">This team will send the VAT recovery data to the third-party vendor that files international VAT recovery returns for Contoso.</span></span>

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a><span data-ttu-id="9c4bd-131">Varmista, että kaikki verotiedot on annettu, ja kirjaa sitten kuluraportti</span><span class="sxs-lookup"><span data-stu-id="9c4bd-131">Make sure that all tax information is complete, and then post the expense report</span></span>

<span data-ttu-id="9c4bd-132">April on Contoson ostoreskontran koordinaattori, ja hänen on annettava kuluraportista puuttuvat verotiedot, ennen kuin raportti voidaan kirjata.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-132">April, the Accounts payable coordinator for Contoso, must enter any tax information that is missing from an expense report before the report can be posted.</span></span> <span data-ttu-id="9c4bd-133">Hän avaa **Kuluraportin tiedot** -sivun ja näkee Nancyn hyväksytyn kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-133">She opens the **Expense report details** page and sees Nancy's approved expense report.</span></span> <span data-ttu-id="9c4bd-134">April avaa sitten kuluraportin voidakseen katsoa tapahtumien tiedot.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-134">April then opens the expense report to view the details of the transactions.</span></span> <span data-ttu-id="9c4bd-135">Hän huomaa, ettei Nancy antanut yhden tapahtuman nimikkeen alv-ryhmää.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-135">She sees that Nancy didn't enter an item sales tax group for one of the transactions.</span></span> <span data-ttu-id="9c4bd-136">Koska näitä tietoja ei ole annettu, April ei voi kirjata kuluraporttia.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-136">Because this information isn't provided, April can't post the expense report.</span></span> <span data-ttu-id="9c4bd-137">Tämän vuoksi April etsii kulujen hallinnan **Verokonfiguraatiot**-sivulta kyseisen maan/alueen ja tapahtumatyypin oikean nimikkeen alv-ryhmän.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-137">Therefore, April looks on the **Tax configurations** page in Expense management, and finds the appropriate item sales tax group for the country/region and the transaction type.</span></span> <span data-ttu-id="9c4bd-138">April voi nyt kirjata kuluraportin kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-138">April can now post the expense report to the general ledger.</span></span>

<span data-ttu-id="9c4bd-139">Kun April kirjaa kuluraportin, ALV-palautuskelpoinen työnimike luodaan.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-139">When April posts the expense report, a VAT recoverable work item is created.</span></span> <span data-ttu-id="9c4bd-140">Tämä työnimike määritetään taustajärjestelmän käsittelyryhmän jäsenelle.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-140">This work item is assigned to a member of the back-office processing team.</span></span> <span data-ttu-id="9c4bd-141">April saa ilmoituksen, joka vahvistaa kirjauksen onnistumisen.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-141">April receives a message that confirms that posting was successful.</span></span> <span data-ttu-id="9c4bd-142">Tässä ilmoituksessa on myös luettelo palautusta varten tunnistettujen ALV-tapahtumien määrä.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-142">This message also lists the number of VAT transactions that were identified for recovery.</span></span>

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a><span data-ttu-id="9c4bd-143">Käsittele kulut, jotka ovat kelvollisia kansainväliseen ALV-palautukseen</span><span class="sxs-lookup"><span data-stu-id="9c4bd-143">Process expenses that are eligible for international VAT recovery</span></span>

<span data-ttu-id="9c4bd-144">Arnie on Contoson taustajärjestelmän käsittelyryhmän jäsen, jonka vastuulla on vahvistaa, että kaikki ALV-palautukseen tarvittavat tiedot sisältyvät kuluraportteihin.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-144">Arnie, a member of Contoso's back-office processing team, is responsible for confirming that all the required information for VAT recovery is included on expense reports.</span></span> <span data-ttu-id="9c4bd-145">Hän avaa **Kulujen veronpalautus** -sivun ja valitsee Nancyn lähettämän kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-145">He opens the **Expense tax recovery** page and selects the expense report that Nancy submitted.</span></span> <span data-ttu-id="9c4bd-146">Arnie varmistaa, että kaikki tarvittavat kuitit ovat liitteinä ja että annetut alv-ryhmät ja nimikkeen alv-koodit ovat oikein.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-146">Arnie verifies that all the required receipts are attached, and that the correct sales tax group and item sales tax codes were entered.</span></span>

<span data-ttu-id="9c4bd-147">Kun Arnie vastaanottaa Nancyn lähettämät paperikuitit, hän vertaa paperikuitteja digitaalikuitteihin ja muuttaa sitten kuluraportin tilaksi **Valmis palautukseen**.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-147">When Arnie receives the paper receipts from Nancy, he verifies the paper receipts against the digital receipts and then changes the status of the expense report to **Ready for recovery**.</span></span>

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a><span data-ttu-id="9c4bd-148">Kirjaa kansainväliset palautukset lähettämällä ALV-palautustiedot ulkopuoliselle toimittajalle</span><span class="sxs-lookup"><span data-stu-id="9c4bd-148">Send VAT recovery data to the third-party vendor to file international recovery returns</span></span>

<span data-ttu-id="9c4bd-149">Kun Arnie on valmis lähettämään kuluraportin tiedot ALV-palautukset kirjaavalle ulkopuoliselle toimittajalle, hän avaa **Kulujen veronpalautus** -sivun.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-149">When Arnie is ready to send the expense report data to the third-party vendor that will file the VAT recovery returns, he opens the **Expense tax recovery** page.</span></span> <span data-ttu-id="9c4bd-150">Hän suodattaa sivun näyttämään vain kuluraportit, joilla on merkintä **Valmis palautukseen**.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-150">He filters the page so that it shows only the expense reports that are marked as **Ready for recovery**.</span></span> <span data-ttu-id="9c4bd-151">Arnie valitsee sitten **Tiedosto** &gt; **Vie Exceliin**.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-151">Arnie then selects **File** &gt; **Export to Excel**.</span></span> <span data-ttu-id="9c4bd-152">Kuluraporttien alv-tiedot viedään Microsoft Excel -laskentataulukkoon.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-152">The VAT information from the expense reports is exported to a Microsoft Excel worksheet.</span></span> <span data-ttu-id="9c4bd-153">Arnie lähettää tämän laskentataulukon ulkopuoliselle toimittajalle ja sisällyttää viestin, jonka mukaan paperikuitit on lähetetty kuriiritoimituksena.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-153">Arnie submits this worksheet to the third-party vendor and includes a message that states that the paper receipts have been sent by courier.</span></span>

## <a name="process-expenses-for-domestic-vat-recovery"></a><span data-ttu-id="9c4bd-154">Käsittele kotimaisten ALV-palautusten kulut</span><span class="sxs-lookup"><span data-stu-id="9c4bd-154">Process expenses for domestic VAT recovery</span></span>

<span data-ttu-id="9c4bd-155">Arnien on varmistettava, että kuluraportin tapahtuvat ovat ALV-palautuskelpoisia ja että digitaaliset kuitit ovat raporttien liitteenä.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-155">Arnie must verify that the expense report transactions are eligible for VAT recovery, and that the digital receipts are attached to the reports.</span></span> <span data-ttu-id="9c4bd-156">Arnie aloittaa kotimaisten palautukseen oikeutettujen kulujen käsittelyn avaamalla **Kulujen veronpalautus** -sivun ja valitsemalla varmistettavan kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-156">To start to process eligible expenses for domestic recovery, Arnie opens the **Expense tax recovery** page and selects the expense report that requires verification.</span></span> <span data-ttu-id="9c4bd-157">Hän varmistaa, että kuitit ovat yrityksen eikä työntekijän nimissä.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-157">He verifies that receipts are in the name of the company instead of the employee.</span></span> <span data-ttu-id="9c4bd-158">Kuittien on oltava ALV-palautuksia varten yrityksen nimissä.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-158">For VAT recovery, receipts must be in the name of the company.</span></span> <span data-ttu-id="9c4bd-159">Arnie vahvistaa sitten, että käytetyt ALV-ryhmän ja nimikkeen alv-koodit ovat oikeita.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-159">Arnie then confirms that the correct sales tax group and item sales tax codes were applied.</span></span>

<span data-ttu-id="9c4bd-160">Kun Arnie saa paperikuitit, hän muuttaa kuluraportin tilaksi **Valmis palautukseen**.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-160">When Arnie receives the paper receipts, he changes the status of the expense report to **Ready for recovery**.</span></span> <span data-ttu-id="9c4bd-161">Hän voi sitten kirjata palautuksen soveltuvalle veroviranomaiselle.</span><span class="sxs-lookup"><span data-stu-id="9c4bd-161">He can then file the return with the appropriate tax authority.</span></span> <span data-ttu-id="9c4bd-162">Tässä tapauksessa soveltuva yhdysvaltalainen veronviranomainen IRS (Internal Revenue Service).</span><span class="sxs-lookup"><span data-stu-id="9c4bd-162">In this case, the appropriate tax authority in the US is the Internal Revenue Service (IRS).</span></span>