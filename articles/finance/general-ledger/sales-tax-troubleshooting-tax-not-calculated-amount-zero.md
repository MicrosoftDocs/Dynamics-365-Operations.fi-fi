---
title: Veroa ei lasketa tai veron summa on nolla.
description: Tässä aiheessa on vianmääritystietoja, jotka voivat auttaa, kun veron summa on 0 (nolla) tai veroa ei lasketa.
author: shtao
ms.date: 04/01/2021
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
ms.openlocfilehash: c398579a0a408e7f5625a3e801a967955c4b1e5b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020112"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="1f87b-103">Veroa ei lasketa tai veron summa on nolla.</span><span class="sxs-lookup"><span data-stu-id="1f87b-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f87b-104">Tapahtuman rivisumma ei ole välttämättä 0 (nolla), mutta joko veroa ei lasketa tai laskettu verosumma on 0.</span><span class="sxs-lookup"><span data-stu-id="1f87b-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="1f87b-105">Voit ratkaista tämän ongelman noudattamalla seuraavien osien ohjeita tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="1f87b-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="1f87b-106">Tarkista, että tapahtuma on valinnut verokoodit oikein</span><span class="sxs-lookup"><span data-stu-id="1f87b-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="1f87b-107">Jos tapahtuma ei valitse oikeita verokoodeja tai jos se ei valitse mitään verokoodeja, veroja ei lasketa sen perusteella.</span><span class="sxs-lookup"><span data-stu-id="1f87b-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="1f87b-108">Tarkista, että tapahtuma on valinnut verokoodit oikein, näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="1f87b-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="1f87b-109">Varmista tapahtumarivin **Rivitiedot**-pikavälilehden **Asetukset**-välilehden **Arvonlisävero**-osassa, että oikeat veroryhmät ovat valittuina **Nimikkeen arvonlisäveroryhmä**- ja **Arvonlisäveroryhmä**-kentissä.</span><span class="sxs-lookup"><span data-stu-id="1f87b-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="1f87b-110">Jos oikeat veroryhmät eivät ole valittuina, valitse ne.</span><span class="sxs-lookup"><span data-stu-id="1f87b-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="1f87b-111">[![Nimikkeen arvonlisäveroryhmä- ja Arvonlisäveroryhmä-kentät](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="1f87b-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="1f87b-112">Siirry kohtaan **Vero** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäveroryhmät**.</span><span class="sxs-lookup"><span data-stu-id="1f87b-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="1f87b-113">Valitse haluamasi arvonlisäveroryhmä ja tee sitten huomautus **Arvonlisäverokoodi**-kentän verokoodista **Asetukset**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="1f87b-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="1f87b-114">[![Arvonlisäveroryhmät-sivu](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="1f87b-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="1f87b-115">Siirry kohtaan **VeroTax** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäveroryhmät**.</span><span class="sxs-lookup"><span data-stu-id="1f87b-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="1f87b-116">Valitse asianmukainen nimikkeen arvonlisäveroryhmä ja varmista **Asetukset**-pikavälilehdessä, että **Arvonlisäverokoodi**-kentän verokoodi vastaa arvonlisäveroryhmän verokoodia.</span><span class="sxs-lookup"><span data-stu-id="1f87b-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="1f87b-117">[![Nimikkeiden arvonlisäveroryhmät -sivu](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="1f87b-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="1f87b-118">Jos verokoodit eivät täsmää, päivitä yhden ryhmän arvonlisäverokoodi.</span><span class="sxs-lookup"><span data-stu-id="1f87b-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="1f87b-119">Varmista, että valittuja verokoodeja ei ole vapautettu ja että niiden veroprosenttiarvo on oikea.</span><span class="sxs-lookup"><span data-stu-id="1f87b-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="1f87b-120">Jos verokoodit ovat vapautettuja tai jos veroprosentti on 0 (nolla), veron laskentatulos on 0.</span><span class="sxs-lookup"><span data-stu-id="1f87b-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="1f87b-121">Seuraavia ohjeita noudattamalla voit määrittää, ovatko valitut verokoodit vapautettuja, ja tarkistaa, että veroihin sovelletaan oikeaa veroprosenttia.</span><span class="sxs-lookup"><span data-stu-id="1f87b-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="1f87b-122">Siirry kohtaan **Vero** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäveroryhmät**.</span><span class="sxs-lookup"><span data-stu-id="1f87b-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="1f87b-123">Valitse haluamasi arvonlisäveroryhmä ja varmista sitten **Asetukset**-pikavälilehdessä, että **Vapautus**-valintaruutua ei ole.</span><span class="sxs-lookup"><span data-stu-id="1f87b-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="1f87b-124">Jos se on valittuna, poista valinta.</span><span class="sxs-lookup"><span data-stu-id="1f87b-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="1f87b-125">[![Arvonlisäveroryhmät-sivun Vapautus-valintaruutu](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="1f87b-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="1f87b-126">Valitse **Vero** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäverokoodit**.</span><span class="sxs-lookup"><span data-stu-id="1f87b-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="1f87b-127">Valitse asianmukainen arvonlisäverokoodi ja varmista sitten, että **Arvo**-kentän veroprosenttiarvo ei ole 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="1f87b-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="1f87b-128">Jos arvo on 0, päivitä kenttä niin, että sen arvoksi on määritetty oikea veroprosentti.</span><span class="sxs-lookup"><span data-stu-id="1f87b-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="1f87b-129">[![Arvonlisäverokoodin arvot -sivun Arvo-kenttä](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="1f87b-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="1f87b-130">Määritä, onko oikea verosumma nolla</span><span class="sxs-lookup"><span data-stu-id="1f87b-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="1f87b-131">Joissakin tilanteissa verosumma 0 (nolla) on oikea.</span><span class="sxs-lookup"><span data-stu-id="1f87b-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="1f87b-132">Seuraavia ohjeita noudattamalla voit määrittää, onko tapahtumalle oikea verosumma 0.</span><span class="sxs-lookup"><span data-stu-id="1f87b-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="1f87b-133">Siirry kohtaan **Kirjanpito** \> **Kirjanpidon asetukset** \> **Kirjanpitoparametrit**.</span><span class="sxs-lookup"><span data-stu-id="1f87b-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="1f87b-134">**Arvonlisävero**-välilehden **Laskentatapa**-kentässä vahvista, että **Yhteensä** on valittuna.</span><span class="sxs-lookup"><span data-stu-id="1f87b-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="1f87b-135">[![Kirjanpitoparametrit-sivun Laskentatapa-kenttä](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="1f87b-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="1f87b-136">Valitse **Vero** \> **Välilliset verot** \> **Arvonlisävero** \> **Arvonlisäverokoodit**.</span><span class="sxs-lookup"><span data-stu-id="1f87b-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="1f87b-137">Valitse asianmukainen arvonlisäverokoodi, valitse **Laskenta** \> **Alv-rajan peruste** ja vahvista, että alv-rajan perusteen arvona on **Laskun saldon nettosumma** tai **Laskun loppusumma muut arvonlisäverosummat mukaan luettuna**.</span><span class="sxs-lookup"><span data-stu-id="1f87b-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="1f87b-138">Lisätietoja on kohdassa [Laskun loppusumma muut arvonlisäverosummat mukaan luettuna](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span><span class="sxs-lookup"><span data-stu-id="1f87b-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="1f87b-139">Jos oikeat arvot on määritetty vaiheissa 2 ja 4, määritä, onko tapahtuman kokonaissumma 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="1f87b-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="1f87b-140">Jos kokonaissumma on 0, odotettu tulos on veron summa 0.</span><span class="sxs-lookup"><span data-stu-id="1f87b-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="1f87b-141">Koska veron laskenta perustuu laskun saldon kokonaissummaan eikä summaa ole rivi riviltä, veron summa 0 kohdistetaan kullekin riville veron laskennan jälkeen.</span><span class="sxs-lookup"><span data-stu-id="1f87b-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="1f87b-142">Määritä, onko mukautus olemassa</span><span class="sxs-lookup"><span data-stu-id="1f87b-142">Determine whether customization exists</span></span>

<span data-ttu-id="1f87b-143">Jos olet suorittanut edellisten osien vaiheet, mutta et ole löytänyt ongelmaa, selvitä, onko mukautus olemassa.</span><span class="sxs-lookup"><span data-stu-id="1f87b-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="1f87b-144">Jos mukautusta ei ole, luo Microsoftin huoltopyyntö lisätuen saamiseksi.</span><span class="sxs-lookup"><span data-stu-id="1f87b-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
