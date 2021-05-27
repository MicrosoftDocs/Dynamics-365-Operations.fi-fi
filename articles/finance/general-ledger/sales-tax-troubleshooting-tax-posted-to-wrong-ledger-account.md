---
title: Vero kirjataan tositteen väärälle kirjanpitotilille
description: Tässä aiheessa on vianmääritystietoja, jotka voivat auttaa, kun vero kirjataan tositteen väärälle kirjanpitotilille.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020088"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="2f462-103">Vero kirjataan tositteen väärälle kirjanpitotilille</span><span class="sxs-lookup"><span data-stu-id="2f462-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f462-104">Kirjaamisen aikana vero saatetaan kirjata tositteen väärälle kirjanpitotilille.</span><span class="sxs-lookup"><span data-stu-id="2f462-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="2f462-105">Voit ratkaista tämän ongelman noudattamalla seuraavien osien ohjeita tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="2f462-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="2f462-106">Tämän ohjeaiheen esimerkeissä myyntitilausta käytetään liiketoiminta-asiakirjana.</span><span class="sxs-lookup"><span data-stu-id="2f462-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="2f462-107">Etsi virheellisen verotapahtuman verokoodi</span><span class="sxs-lookup"><span data-stu-id="2f462-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="2f462-108">Valitse **Tositetapahtumat**-sivulla tapahtuma, jota haluat käyttää, ja valitse sitten **Kirjattu arvonlisävero**.</span><span class="sxs-lookup"><span data-stu-id="2f462-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="2f462-109">[![Kirjattu arvonlisävero -painike Tositetapahtumat-sivulla](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="2f462-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="2f462-110">Tarkista arvo **Arvonlisäverokoodi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="2f462-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="2f462-111">Tässä esimerkissä se on **VAT 19**.</span><span class="sxs-lookup"><span data-stu-id="2f462-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="2f462-112">[![Kirjattu arvonlisävero -sivun Arvonlisävero-kenttä](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="2f462-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="2f462-113">Tarkista verokoodin kirjanpidon kirjausryhmä</span><span class="sxs-lookup"><span data-stu-id="2f462-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="2f462-114">Valitse **Vero** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäverokoodit**.</span><span class="sxs-lookup"><span data-stu-id="2f462-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="2f462-115">Etsi ja valitse verokoodi sekä tarkista sitten **Kirjanpidon kirjausryhmä** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="2f462-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="2f462-116">Tässä esimerkissä se on **VAT**.</span><span class="sxs-lookup"><span data-stu-id="2f462-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="2f462-117">[![Kirjanpidon kirjausryhmä -kenttä Arvonlisäverokoodit-sivulla](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="2f462-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="2f462-118">**Kirjanpidon kirjausryhmä** -kentän arvo on linkki.</span><span class="sxs-lookup"><span data-stu-id="2f462-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="2f462-119">Jos haluat tarkastella ryhmän konfiguraation tietoja, valitse linkki.</span><span class="sxs-lookup"><span data-stu-id="2f462-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="2f462-120">Vaihtoehtoisesti voit valita ja pitää kenttää painettuna (tai napsauttaa sitä hiiren kakkospainikkeella) ja valita sitten **Näytä tiedot**.</span><span class="sxs-lookup"><span data-stu-id="2f462-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="2f462-121">[![Näytä tietoja -komento](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="2f462-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="2f462-122">Varmista **Maksettava arvonlisävero** -kentässä, että tilinumero on oikea tapahtumalajin mukaan.</span><span class="sxs-lookup"><span data-stu-id="2f462-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="2f462-123">Valitse sitten oikea tili, jolle kirjaat sen.</span><span class="sxs-lookup"><span data-stu-id="2f462-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="2f462-124">Tässä esimerkissä myyntitilauksen arvonlisävero on kirjattava arvonlisäveron kulutilille 222200.</span><span class="sxs-lookup"><span data-stu-id="2f462-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="2f462-125">[![Maksettava arvonlisävero -kenttä Kirjanpidon kirjausryhmät -sivulla](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="2f462-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="2f462-126">Seuraavassa taulukossa on tietoja kustakin **Kirjanpidon kirjausryhmät** -sivun kentästä.</span><span class="sxs-lookup"><span data-stu-id="2f462-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="2f462-127">Kenttä</span><span class="sxs-lookup"><span data-stu-id="2f462-127">Field</span></span>                  | <span data-ttu-id="2f462-128">kuvaus</span><span class="sxs-lookup"><span data-stu-id="2f462-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="2f462-129">Maksettava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="2f462-129">Sales tax payable</span></span>      | <span data-ttu-id="2f462-130">Veroviranomaiselle maksettavan lähtevän arvonlisäveron päätili.</span><span class="sxs-lookup"><span data-stu-id="2f462-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="2f462-131">Saatava arvonlisävero</span><span class="sxs-lookup"><span data-stu-id="2f462-131">Sales tax receivable</span></span>   | <span data-ttu-id="2f462-132">Veroviranomaiselta saatavien saapuvien verojen päätili.</span><span class="sxs-lookup"><span data-stu-id="2f462-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="2f462-133">Käyttöverokulu</span><span class="sxs-lookup"><span data-stu-id="2f462-133">Use tax expense</span></span>        | <span data-ttu-id="2f462-134">Päätili, jota käytetään vähennyskelpoisten käyttöverojen kirjaamiseen, joita toimittajat eivät peri tai raportoi veroviranomaiselle osana Euroopan unionin (EU) käänteistä arvonlisäveroa (GST) / harmonisoitua arvonlisäveroa (HST).</span><span class="sxs-lookup"><span data-stu-id="2f462-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="2f462-135">Tapahtumassa käytettävän arvonlisäveroryhmän arvonlisäverokoodin **Käyttövero**-vaihtoehto on valittava.</span><span class="sxs-lookup"><span data-stu-id="2f462-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="2f462-136">Tämä kenttä ei ole käytettävissä, jos **Käytä arvonlisäverotuksen sääntöjä** -vaihtoehto on valittu **Kirjanpitoparametrit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="2f462-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="2f462-137">Käyttöverovelka</span><span class="sxs-lookup"><span data-stu-id="2f462-137">Use tax payable</span></span>        | <span data-ttu-id="2f462-138">Päätili, jota käytetään veroviranomaisille maksettavien saapuvien käyttöverojen kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="2f462-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="2f462-139">Maksutili</span><span class="sxs-lookup"><span data-stu-id="2f462-139">Settlement account</span></span>     | <span data-ttu-id="2f462-140">Päätili, jolle **Maksettava käyttövero**- ja **Saatava arvonlisävero** -kentässä määritettyjen kirjanpitotilien nettosaldo kirjataan.</span><span class="sxs-lookup"><span data-stu-id="2f462-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="2f462-141">Toimittajan käteisalennus</span><span class="sxs-lookup"><span data-stu-id="2f462-141">Vendor cash discount</span></span>   | <span data-ttu-id="2f462-142">Päätili, jonne tähän kirjanpidon kirjausryhmän liitetyn arvonlisäverokoodin käteisalennukset kirjataan.</span><span class="sxs-lookup"><span data-stu-id="2f462-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="2f462-143">Asiakastapauksen alennus</span><span class="sxs-lookup"><span data-stu-id="2f462-143">Customer case discount</span></span> | <span data-ttu-id="2f462-144">Päätili, jonne tähän kirjanpidon kirjausryhmän liitetyn arvonlisäverokoodin käteisalennukset kirjataan.</span><span class="sxs-lookup"><span data-stu-id="2f462-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="2f462-145">Lisätietoja on kohdassa [Arvonlisäveron kirjanpidon kirjausryhmien määrittäminen](tasks/set-up-ledger-posting-groups-sales-tax.md).</span><span class="sxs-lookup"><span data-stu-id="2f462-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="2f462-146">Kirjanpitodimensioiden tarkistus koodin virheenkorjauksella</span><span class="sxs-lookup"><span data-stu-id="2f462-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="2f462-147">Koodissa kirjaustili määräytyy kirjanpitodimension mukaan.</span><span class="sxs-lookup"><span data-stu-id="2f462-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="2f462-148">Kirjanpitodimensio tallentaa tilin tietuetunnuksen tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="2f462-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="2f462-149">Lisää myyntitilauksen keskeytyskohta **Tax::saveAndPost()**- ja **Tax::post()** -menetelmiin.</span><span class="sxs-lookup"><span data-stu-id="2f462-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="2f462-150">Kiinnitä huomiota **\_ledgerDimension**-arvoon.</span><span class="sxs-lookup"><span data-stu-id="2f462-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="2f462-151">[![Myyntitilauksen koodinäyte, jossa on keskeytyskohta](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="2f462-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="2f462-152">Lisää ostotilauksessa keskeytyskohta **TaxPost::saveAndPost()**- ja **TaxPost::postToTaxTrans()**-menetelmiin.</span><span class="sxs-lookup"><span data-stu-id="2f462-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="2f462-153">Kiinnitä huomiota **\_ledgerDimension**-arvoon.</span><span class="sxs-lookup"><span data-stu-id="2f462-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="2f462-154">[![Ostotilauksen koodinäyte, jossa on keskeytyskohta](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="2f462-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="2f462-155">Suorita seuraava SQL-kysely, kun haluat etsiä tietokannan tilin näyttöarvon, joka perustuu kirjanpitodimension tallentamaan tietuetunnukseen.</span><span class="sxs-lookup"><span data-stu-id="2f462-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="2f462-156">[![Tietuetunnuksen näyttöarvo](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="2f462-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="2f462-157">Voit tarkistaa kutsupinon ja selvittää, mihin **_ledgerDimension** on määritetty.</span><span class="sxs-lookup"><span data-stu-id="2f462-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="2f462-158">Yleensä arvo on peräisin kohteesta **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="2f462-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="2f462-159">Tässä tapauksessa sinun on lisättävä keskeytyskohta kohteisiin **TmpTaxWorkTrans::insert()** ja **TmpTaxWorkTrans::update()** etsiäksesi, minne arvo on määritetty.</span><span class="sxs-lookup"><span data-stu-id="2f462-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="2f462-160">Määritä, onko mukautus olemassa</span><span class="sxs-lookup"><span data-stu-id="2f462-160">Determine whether customization exists</span></span>

<span data-ttu-id="2f462-161">Jos olet suorittanut edellisten osien vaiheet, mutta et ole löytänyt ongelmaa, selvitä, onko mukautus olemassa.</span><span class="sxs-lookup"><span data-stu-id="2f462-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="2f462-162">Jos mukautusta ei ole, luo Microsoftin huoltopyyntö lisätuen saamiseksi.</span><span class="sxs-lookup"><span data-stu-id="2f462-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
