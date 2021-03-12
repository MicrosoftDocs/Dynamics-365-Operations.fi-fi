---
title: Kirjattujen vuokratapahtumien palauttaminen
description: Tässä ohjeaiheessa kerrotaan, miten kirjattu vuokratapahtuma palautetaan. Kaikki resurssien vuokrauksen kautta luodut tapahtumat voidaan palauttaa.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3e4908ddab2650e5ff7e4a28bf916604d165d08c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969525"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="c650d-104">Kirjattujen vuokratapahtumien palauttaminen</span><span class="sxs-lookup"><span data-stu-id="c650d-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c650d-105">Kaikki resurssien vuokrauksen kautta luodut tapahtumat voidaan palauttaa.</span><span class="sxs-lookup"><span data-stu-id="c650d-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="c650d-106">Resurssin vuokrauksen kautta palautetut tapahtumat päivittävät vuokratietoja.</span><span class="sxs-lookup"><span data-stu-id="c650d-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="c650d-107">Näin ollen ne myös päivittävät vuokrasopimusvelan kirjanpitoarvot ja käyttöoikeusomaisuuserän.</span><span class="sxs-lookup"><span data-stu-id="c650d-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="c650d-108">Voit luoda vuokraukselle palautustapahtuman seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="c650d-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="c650d-109">Valitse **Vuokratapahtumat**- tai **Velkatapahtumat**-sivulla tapahtuma ja valitse sitten **Palauta tapahtuma**.</span><span class="sxs-lookup"><span data-stu-id="c650d-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="c650d-110">Näyttöön tulevassa valintaikkunassa voit muokata päivämäärää, jolloin palautuskirjaus kirjataan.</span><span class="sxs-lookup"><span data-stu-id="c650d-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="c650d-111">Oletusarvoisesti **Päivämäärä**-kenttään määritetään valitun tapahtuman kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="c650d-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="c650d-112">Palautusvientiä ei voi kirjata valitun tapahtuman alkuperäinen kirjauspäivämäärää aiemmin.</span><span class="sxs-lookup"><span data-stu-id="c650d-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="c650d-113">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c650d-113">Select **OK**.</span></span> <span data-ttu-id="c650d-114">Kirjataan kirjauskansiovienti, joka palauttaa valitun viennin.</span><span class="sxs-lookup"><span data-stu-id="c650d-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="c650d-115">Palautus näkyy **Resurssitapahtumat**- tai **Velkatapahtumat**-sivulla. Sivulla näkyvä nykyisen saldon netto yhteensä päivitetään.</span><span class="sxs-lookup"><span data-stu-id="c650d-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="c650d-116">Kun valitset **Käänteinen jäljitys**, näkyviin tulee valintaikkuna, jossa näkyvät sekä alkuperäiset tapahtumat että palautetut tapahtumat ja linkitetty numero, joka näkyy *jäljitysnumerona*.</span><span class="sxs-lookup"><span data-stu-id="c650d-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="c650d-117">Jos haluat helpottaa palautusten ymmärtämistä ja parantaa näkyvyyttä, voit jäljittää myös palautuksia käyttämällä vuokra-aikatauluja.</span><span class="sxs-lookup"><span data-stu-id="c650d-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="c650d-118">**Viimeisin kirjauskansion numero** -kentässä **Aikataulu**-sivulla on tapahtumien kirjauskansioiden numerot.</span><span class="sxs-lookup"><span data-stu-id="c650d-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="c650d-119">Kun tapahtuma palautetaan, tähän kenttään päivittyy palautustapahtuman kirjauskansionumero.</span><span class="sxs-lookup"><span data-stu-id="c650d-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="c650d-120">Lisäksi valitaan **Palautettu**-valintaruutu. Se osoittaa, että tapahtuma on palautettu. **Kirjattu**-kenttä valitaan.</span><span class="sxs-lookup"><span data-stu-id="c650d-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="c650d-121">Palautetun tapahtuman peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="c650d-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="c650d-122">Voit peruuttaa palautetun tapahtuman seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="c650d-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="c650d-123">Valitse **Aikataulu**-sivulla tai **Tapahtumat**-sivulla alkuperäinen tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="c650d-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="c650d-124">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="c650d-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="c650d-125">Jos olet valinnut tapahtuman **Aikataulu**-sivulla, tee seuraavat vaiheet ja luo kirjauskansio kohdassa [Kuukausittaisten kirjauskansiovientien luominen eränä](create-monthly-journals-batch.md).</span><span class="sxs-lookup"><span data-stu-id="c650d-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="c650d-126">Kirjauskansio on kirjattava manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="c650d-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="c650d-127">Jos valitsit tapahtuman **Tapahtumat**-sivulla, valitse **Palauta tapahtuma**.</span><span class="sxs-lookup"><span data-stu-id="c650d-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="c650d-128">Näyttöön tulee sanoma, jossa kerrotaan tämän peruutuksen olevan aiemman palautuksen peruutus, ja että voit muokata tämän peruutuksen kirjauspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="c650d-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="c650d-129">Yleiset yrityksen tarkistukset, jotka vaikuttavat päivämääriin, voidaan kuitenkin syöttää **Päivämäärä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c650d-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="c650d-130">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c650d-130">Select **OK**.</span></span> <span data-ttu-id="c650d-131">Kirjataan kirjauskansiovienti, joka palauttaa valitun viennin.</span><span class="sxs-lookup"><span data-stu-id="c650d-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="c650d-132">Palautus näkyy **Tapahtumat**-sivulla. Nykyisen saldon netto yhteensä palautetaan ensimmäistä palautusta edeltäväksi arvoksi.</span><span class="sxs-lookup"><span data-stu-id="c650d-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="c650d-133">Näin peruutuksen vaikutus saldoihin vältetään.</span><span class="sxs-lookup"><span data-stu-id="c650d-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="c650d-134">Kun valitset **Käänteinen jäljitys**, näyttöön tulee valintaruutu, jossa näkyvät sekä alkuperäiset tapahtumat että palautetut tapahtumat linkitetyn jäljitysnumeron kanssa.</span><span class="sxs-lookup"><span data-stu-id="c650d-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="c650d-135">Voit myös jäljittää peruutuksia käyttämällä soveltuvaa **Aikataulut**-sivua.</span><span class="sxs-lookup"><span data-stu-id="c650d-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="c650d-136">**Käänteinen**-kenttä tyhjennetään, kun taas **Kirjauskansio kirjattu** -kenttä valitaan.</span><span class="sxs-lookup"><span data-stu-id="c650d-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="c650d-137">Lisäksi **Viimeisin kirjauskansionumero** -kenttään päivitetään peruutustapahtuman kirjauskansionumero ja **Kirjauskansionumero**-kenttään päivitetään palautuskirjauskansionumero.</span><span class="sxs-lookup"><span data-stu-id="c650d-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>
