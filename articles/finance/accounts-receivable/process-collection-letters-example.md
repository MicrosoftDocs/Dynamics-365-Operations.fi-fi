---
title: Käsittele maksukehotuksia – esimerkki
description: Tämä ohjeaihe käy läpi esimerkin, jossa käsitellään maksukehotuksen luonti-, tulostus- ja kirjausprosessia.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1b80532463d86dd59b867fca2ee24675396ce717
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826344"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="8d00e-103">Käsittele maksukehotuksia – esimerkki</span><span class="sxs-lookup"><span data-stu-id="8d00e-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8d00e-104">Tämä ohjeaihe käy läpi esimerkin, jossa käsitellään maksukehotuksen luonti-, tulostus- ja kirjausprosessia.</span><span class="sxs-lookup"><span data-stu-id="8d00e-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="8d00e-105">Esimerkki perustuu **Ohita maksut ja hyvityslaskut laskettaessa maksukehotuskoodia** -toimintoon luotonvalvonnassa.</span><span class="sxs-lookup"><span data-stu-id="8d00e-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="8d00e-106">Se käyttää USMF-demoyrityksen ja uuden asiakkaan,US-045:n tietoja.</span><span class="sxs-lookup"><span data-stu-id="8d00e-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="8d00e-107">Aloita kohdassa **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat** valitsemalla **Uusi** ja kirjoita sitten tarvittavat tiedot, jotta asiakas US-045 luodaan.</span><span class="sxs-lookup"><span data-stu-id="8d00e-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="8d00e-108">Noudata näitä vaiheita, kun olet valmis.</span><span class="sxs-lookup"><span data-stu-id="8d00e-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="8d00e-109">Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Määritä maksukehotusten järjestys** ja määritä maksukehotusten järjestys seuraavassa asiakkaan kirjausprofiiliin liitetyssä taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="8d00e-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="8d00e-110">Maksukehotuksen koodi</span><span class="sxs-lookup"><span data-stu-id="8d00e-110">Collection   letter code</span></span>      |     <span data-ttu-id="8d00e-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="8d00e-111">Description</span></span>                           |     <span data-ttu-id="8d00e-112">Valuutta</span><span class="sxs-lookup"><span data-stu-id="8d00e-112">Currency</span></span>      |     <span data-ttu-id="8d00e-113">Päätili</span><span class="sxs-lookup"><span data-stu-id="8d00e-113">Main   account</span></span>        |     <span data-ttu-id="8d00e-114">Lisämaksu valuuttana</span><span class="sxs-lookup"><span data-stu-id="8d00e-114">Fee   in currency</span></span>     |     <span data-ttu-id="8d00e-115">Minimi yli</span><span class="sxs-lookup"><span data-stu-id="8d00e-115">Minimum   over</span></span>        |     <span data-ttu-id="8d00e-116">Päivien esto</span><span class="sxs-lookup"><span data-stu-id="8d00e-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="8d00e-117">Maksukehotus 1</span><span class="sxs-lookup"><span data-stu-id="8d00e-117">Collection   letter 1</span></span>         |     <span data-ttu-id="8d00e-118">Toinen ilmoitus ja lisämaksu</span><span class="sxs-lookup"><span data-stu-id="8d00e-118">Second   notification with fee</span></span>        |     <span data-ttu-id="8d00e-119">USD</span><span class="sxs-lookup"><span data-stu-id="8d00e-119">USD</span></span>           |                           |     <span data-ttu-id="8d00e-120">0,00</span><span class="sxs-lookup"><span data-stu-id="8d00e-120">0.00</span></span>                  |     <span data-ttu-id="8d00e-121">0,00</span><span class="sxs-lookup"><span data-stu-id="8d00e-121">0.00</span></span>                  |     <span data-ttu-id="8d00e-122">2</span><span class="sxs-lookup"><span data-stu-id="8d00e-122">2</span></span>                 |
|     <span data-ttu-id="8d00e-123">Maksukehotus 2</span><span class="sxs-lookup"><span data-stu-id="8d00e-123">Collection   letter 2</span></span>         |     <span data-ttu-id="8d00e-124">Toinen ilmoitus ja lisämaksu</span><span class="sxs-lookup"><span data-stu-id="8d00e-124">Second   notification with fee</span></span>        |     <span data-ttu-id="8d00e-125">USC</span><span class="sxs-lookup"><span data-stu-id="8d00e-125">USC</span></span>           |     <span data-ttu-id="8d00e-126">403150</span><span class="sxs-lookup"><span data-stu-id="8d00e-126">403150</span></span>                |     <span data-ttu-id="8d00e-127">20.00</span><span class="sxs-lookup"><span data-stu-id="8d00e-127">20.00</span></span>                 |     <span data-ttu-id="8d00e-128">10.00</span><span class="sxs-lookup"><span data-stu-id="8d00e-128">10.00</span></span>                 |     <span data-ttu-id="8d00e-129">3</span><span class="sxs-lookup"><span data-stu-id="8d00e-129">3</span></span>                 |
|     <span data-ttu-id="8d00e-130">Perittävä</span><span class="sxs-lookup"><span data-stu-id="8d00e-130">Collection</span></span>                    |     <span data-ttu-id="8d00e-131">Viimeinen ilmoitus ja lisämaksu</span><span class="sxs-lookup"><span data-stu-id="8d00e-131">Final   notification with fee</span></span>         |     <span data-ttu-id="8d00e-132">USD</span><span class="sxs-lookup"><span data-stu-id="8d00e-132">USD</span></span>           |     <span data-ttu-id="8d00e-133">403150</span><span class="sxs-lookup"><span data-stu-id="8d00e-133">403150</span></span>                |     <span data-ttu-id="8d00e-134">50.00</span><span class="sxs-lookup"><span data-stu-id="8d00e-134">50.00</span></span>                 |     <span data-ttu-id="8d00e-135">100.00</span><span class="sxs-lookup"><span data-stu-id="8d00e-135">100.00</span></span>                |     <span data-ttu-id="8d00e-136">15</span><span class="sxs-lookup"><span data-stu-id="8d00e-136">15</span></span>                |

<span data-ttu-id="8d00e-137">Seuraavassa kuvassa on taulukossa näkyvät tiedot, kuten ne näkyvät **maksukehotussivulla**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="8d00e-138">[![Maksukehotusjärjestyksen määrittäminen](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="8d00e-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="8d00e-139">Tässä esimerkissä on nyt määritettävä kaksi parametria.</span><span class="sxs-lookup"><span data-stu-id="8d00e-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="8d00e-140">Valitse ensin **Luotonvalvonta \> Asetukset \> Myyntireskontran parametrit** ja toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="8d00e-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="8d00e-141">Määritä **Perintä**-välilehdessä **Ohita maksut ja hyvityslaskut laskettaessa maksukehotuskoodia** -arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="8d00e-142">Varmista, että **Luo maksukehotus per** -kentän arvoksi on määritetty **Asiakas**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="8d00e-143">[![Myyntireskontran parametrien määrittäminen perintää varten](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="8d00e-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="8d00e-144">Siirry kohtaan **Myyntireskontra \> Laskut \> Kaikki vapaatekstilaskut**, valitse **Uusi** ja noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="8d00e-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="8d00e-145">Valitse **Asiakastili**-kentässä **US-045**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="8d00e-146">Lisää **Laskun päivämäärä** -kenttään **15.1.2021**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="8d00e-147">Syötä **Eräpäivä**-kenttään arvo **16.1.2021**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="8d00e-148">Kirjoita **Laskurivit**-pikavälilehden **Päätili**-kenttään **401100**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="8d00e-149">Kirjoita **Yksikköhinta**-kentässä **500.00**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="8d00e-150">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-150">Select **Post**.</span></span>

    <span data-ttu-id="8d00e-151">Sinun on nyt kirjoitettava asiakkaalle kaksi hyvityslaskua.</span><span class="sxs-lookup"><span data-stu-id="8d00e-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="8d00e-152">Valitse **Uusi** ja toimi sitten seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="8d00e-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="8d00e-153">Valitse **Asiakastili**-kentässä **US-045**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="8d00e-154">Lisää **Laskun päivämäärä** -kenttään **15.1.2021**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="8d00e-155">Syötä **Eräpäivä**-kenttään arvo **16.1.2021**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="8d00e-156">Kirjoita **Laskurivit**-pikavälilehden **Päätili**-kenttään **401100**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="8d00e-157">Syötä **Yksikköhinta**-kentän arvoksi **-100,00**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="8d00e-158">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-158">Select **Post**.</span></span>

5. <span data-ttu-id="8d00e-159">Toista vaihe 4, mutta kirjoita **Yksikköhinta**-kenttään **-200,00**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="8d00e-160">Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat** ja valitse asiakas **US-045**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="8d00e-161">Tämän jälkeen voit tarkistaa aiemmin kirjaamiasi asiakastapahtumia valitsemalla toimintoruudusta **Tapahtumat \> Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="8d00e-162">[![Kirjattujen asiakastapahtumien tarkistaminen](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="8d00e-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="8d00e-163">Asiakkaalle US-045 on nyt luotava maksukehotuksia.</span><span class="sxs-lookup"><span data-stu-id="8d00e-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="8d00e-164">Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Luo maksukehotukset** ja noudata seuravia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="8d00e-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="8d00e-165">Määritä **Lasku**- ja **Hyvityslasku**-asetuksiksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="8d00e-166">Oletusarvon mukaan **Maksukehotus**-kentän arvoksi tulee **Perittävää asiakasta kohti**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="8d00e-167">Lisää **Maksukehotuksen päivämäärä** -kenttään **19.1.2021**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="8d00e-168">Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** ja lisää sitten **Asiakastili**-kentässä asiakas **US-045**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="8d00e-169">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-169">Select **OK**.</span></span>
    5. <span data-ttu-id="8d00e-170">Luo maksukehotukset valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="8d00e-171">Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Tarkastele ja käsittele maksukehotuksia** ja noudata seuravia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="8d00e-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="8d00e-172">Huomaa, että sekä otsikon että tapahtumarivien maksukehotuskoodi on **Maksukehotus 1**, koska tämä maksukehotus on sarjan ensimmäinen maksukehotus.</span><span class="sxs-lookup"><span data-stu-id="8d00e-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="8d00e-173">(Jos haluat tarkastella tapahtumarivejä, sinun on ehkä valittava **Tapahtumat**-pikavälilehti.)</span><span class="sxs-lookup"><span data-stu-id="8d00e-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="8d00e-174">[![Saman maksukehotuskoodin tarkistaminen otsikossa ja riveillä](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="8d00e-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="8d00e-175">Valitse toimintoruudussa **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="8d00e-176">Lisää **Kirjauspäivämäärä** -kenttään **19.1.2021**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="8d00e-177">Asiakkaalle US-045 on jälleen luotava maksukehotuksia.</span><span class="sxs-lookup"><span data-stu-id="8d00e-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="8d00e-178">Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Luo maksukehotukset** ja noudata seuravia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="8d00e-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="8d00e-179">Määritä **Lasku**- ja **Hyvityslasku**-asetuksiksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="8d00e-180">Oletusarvon mukaan **Maksukehotus**-kentän arvoksi tulee **Perittävää asiakasta kohti**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="8d00e-181">Lisää **Maksukehotuksen päivämäärä** -kenttään **23.1.2021**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="8d00e-182">Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** ja lisää sitten **Asiakastili**-kentässä asiakas **US-045**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="8d00e-183">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-183">Select **OK**.</span></span>
    5. <span data-ttu-id="8d00e-184">Luo maksukehotukset valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="8d00e-185">Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Tarkastele ja käsittele maksukehotuksia** ja noudata seuravia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="8d00e-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="8d00e-186">Huomaa, että otsikon maksukehotuskoodi on **Maksukehotus 1**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="8d00e-187">Tapahtumarivien koodi on kuitenkin **Maksukehotus 2**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="8d00e-188">[![Eri maksukehotuskoodien tarkistaminen otsikossa ja riveillä](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="8d00e-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="8d00e-189">Koodit ovat eri, koska **Ohita maksut ja hyvityslaskut laskettaessa maksukehotuskoodia** -arvoksi on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="8d00e-190">Älä kirjaa tätä maksukehotusta.</span><span class="sxs-lookup"><span data-stu-id="8d00e-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="8d00e-191">Siirry kohtaan **Luotonvalvonta \> Asetukset \> Myyntireskontran parametrit** ja määritä sitten **Perintä**-välilehdessä **Ohita maksut ja hyvityslaskut laskettaessa maksukehotuskoodia** -asetukseksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="8d00e-192">[![Määritetään Ohita maksut ja hyvityslaskut laskettaessa maksukehotuskoodia -asetukseksi Ei](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="8d00e-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="8d00e-193">Asiakkaalle US-045 on jälleen luotava maksukehotuksia.</span><span class="sxs-lookup"><span data-stu-id="8d00e-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="8d00e-194">Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Luo maksukehotukset** ja noudata seuravia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="8d00e-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="8d00e-195">Määritä **Lasku**- ja **Hyvityslasku**-asetuksiksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="8d00e-196">Oletusarvon mukaan **Maksukehotus**-kentän arvoksi tulee **Perittävää asiakasta kohti**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="8d00e-197">Lisää **Maksukehotuksen päivämäärä** -kenttään **23.1.2021**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="8d00e-198">Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** ja lisää sitten **Asiakastili**-kentässä asiakas **US-045**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="8d00e-199">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-199">Select **OK**.</span></span>
    5. <span data-ttu-id="8d00e-200">Luo maksukehotukset valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="8d00e-201">Siirry kohtaan **Luotonvalvonta \> Maksukehotus \> Tarkastele ja käsittele maksukehotuksia** ja huomaa, että sekä otsikon että tapahtumarivien maksukehotuskoodi on **Maksukehotus 2**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="8d00e-202">[![Näytetään taas, että sama maksukehotuskoodi on otsikossa ja riveillä](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="8d00e-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="8d00e-203">Sama koodi on molemmissa paikoissa, koska **Ohita maksut ja hyvityslaskut laskettaessa maksukehotuskoodia** -arvoksi on määritetty nyt **Ei**.</span><span class="sxs-lookup"><span data-stu-id="8d00e-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
