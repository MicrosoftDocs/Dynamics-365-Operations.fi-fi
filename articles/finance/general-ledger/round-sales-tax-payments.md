---
title: Arvonlisäveromaksut ja pyöristyssäännöt
description: Tässä artikkelissa kerrotaan, miten ALV-viranomaisten pyöristyssäännön määrittäminen toimii, ja miten arvonlisäverosaldo pyöristetään arvonlisäverotyön arvonlisäveron selvityksen ja kirjauksen aikana.
author: ShylaThompson
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: pacheren
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97f1a30c541a302755826bb8f77205bc060ec159
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897183"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="b9a2d-103">Arvonlisäveromaksut ja pyöristyssäännöt</span><span class="sxs-lookup"><span data-stu-id="b9a2d-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9a2d-104">Tässä artikkelissa kerrotaan, miten ALV-viranomaisten pyöristyssäännön määrittäminen toimii, ja miten arvonlisäverosaldo pyöristetään arvonlisäverotyön arvonlisäveron selvityksen ja kirjauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="b9a2d-105">Arvonlisäverot täytyy ilmoittaa ja maksaa säännöllisesti.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="b9a2d-106">Tämä voidaan tehdä suorittamalla arvonlisäveron tilitys- ja kirjausprosessi Arvonlisävero-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="b9a2d-107">Kauden arvonlisävero tilitetään arvonlisäverotilejä vastaan, ja alv-saldo kirjataan arvonlisäveron maksutilille.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="b9a2d-108">Arvonlisäveron maksutilille kirjattu alv-saldo voidaan pyöristää veroviranomaisten ohjeiden mukaan määrittämällä Arvonlisävero-sivulla pyöristyssääntö.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="b9a2d-109">Pyöristysero kirjataan arvonlisäveron pyöristystilille, joka valitaan kirjanpidossa Automaattisten tapahtumien tilit -kentästä.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="b9a2d-110">Seuraavassa esimerkissä on kuvattu arvonlisäveron pyöristyssäännön toimintaa.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="b9a2d-111">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="b9a2d-111">Examples</span></span>

<span data-ttu-id="b9a2d-112">Kauden arvonlisävero näyttää hyvityssaldoksi -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="b9a2d-113">Yritys on perinyt arvonlisäveroja enemmän kuin maksanut.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="b9a2d-114">Yrityksellä on siten arvonlisäverovelkaa.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="b9a2d-115">Yritys haluaa käyttää pyöristysmenetelmää, joka pyöristää saldon lähimpään 1,00 euroon.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="b9a2d-116">Alv-kirjanpidosta vastaava käyttäjä tekee seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="b9a2d-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="b9a2d-117">Valitse **Vero** > **Välilliset verot** > **Arvonlisävero** > **Alv-viranomaiset**.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="b9a2d-118">Valitse **Yleinen**-pikavälilehdessä **Pyöristystapa**-kentästä **Normaali**.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="b9a2d-119">Syötä **Pyöristys**-kenttään arvoksi 1,00.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="b9a2d-120">Kun arvonlisävero täytyy maksaa veroviranomaisille, avaa **Verot** > **Ilmoitukset** > **arvonlisävero** > **Vahvista ja kirjaa arvonlisävero**.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="b9a2d-121">Voit nähdä, että arvonlisäveron maksutilillä oleva alv-velka **98 765,43** pyöristetään arvoon **98 765**.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="b9a2d-122">Seuraavassa taulukossa on esitetty, miten summa 98 765,43 summa pyöristetään käyttämällä kutakin **Alv-viranomaiset**-sivulla **Pyöristystapa**-kentästä valittavissa olevaa pyöristysmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="b9a2d-123">Jos pyöristysarvo on määritetty arvoon 0,00, toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b9a2d-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="b9a2d-124">Pyöristyksessä pyöristyskäyttäytyminen on sama kuin **pyöristyksessä = 0,01**.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="b9a2d-125">**Pyöristyslomakkeen vaihtoehdot**, **alaspäin**, **pyöristäminen** ja **oma etu**, käyttäytyvät samoin kuin **pyöristys = 1,00**.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="b9a2d-126">Pyöristystapavaihtoehto</span><span class="sxs-lookup"><span data-stu-id="b9a2d-126">Rounding form option</span></span>                | <span data-ttu-id="b9a2d-127">Pyöristysarvo = 0,01</span><span class="sxs-lookup"><span data-stu-id="b9a2d-127">Round-off value = 0.01</span></span> | <span data-ttu-id="b9a2d-128">Pyöristysarvo = 0,10</span><span class="sxs-lookup"><span data-stu-id="b9a2d-128">Round-off value = 0.10</span></span> | <span data-ttu-id="b9a2d-129">Pyöristysarvo = 1,00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-129">Round-off value = 1.00</span></span> | <span data-ttu-id="b9a2d-130">Pyöristysarvo = 100,00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-130">Round-off value = 100.00</span></span> | <span data-ttu-id="b9a2d-131">Pyöristysarvo = 0,00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="b9a2d-132">Normaali</span><span class="sxs-lookup"><span data-stu-id="b9a2d-132">Normal</span></span>                              | <span data-ttu-id="b9a2d-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="b9a2d-133">98,765.43</span></span>              | <span data-ttu-id="b9a2d-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="b9a2d-134">98,765.40</span></span>              | <span data-ttu-id="b9a2d-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-135">98,765.00</span></span>              | <span data-ttu-id="b9a2d-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-136">98,800.00</span></span>                | <span data-ttu-id="b9a2d-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="b9a2d-137">98,765.43</span></span>                |
| <span data-ttu-id="b9a2d-138">Alaspäin</span><span class="sxs-lookup"><span data-stu-id="b9a2d-138">Downward</span></span>                            | <span data-ttu-id="b9a2d-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="b9a2d-139">98,765.43</span></span>              | <span data-ttu-id="b9a2d-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="b9a2d-140">98,765.40</span></span>              | <span data-ttu-id="b9a2d-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-141">98,765.00</span></span>              | <span data-ttu-id="b9a2d-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-142">98,700.00</span></span>                | <span data-ttu-id="b9a2d-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-143">98,765.00</span></span>                |
| <span data-ttu-id="b9a2d-144">Pyöristys</span><span class="sxs-lookup"><span data-stu-id="b9a2d-144">Rounding-up</span></span>                         | <span data-ttu-id="b9a2d-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="b9a2d-145">98,765.43</span></span>              | <span data-ttu-id="b9a2d-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="b9a2d-146">98,765.50</span></span>              | <span data-ttu-id="b9a2d-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-147">98,766.00</span></span>              | <span data-ttu-id="b9a2d-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-148">98,800.00</span></span>                | <span data-ttu-id="b9a2d-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-149">98,766.00</span></span>                |
| <span data-ttu-id="b9a2d-150">Oma etu, maksettavien saldo</span><span class="sxs-lookup"><span data-stu-id="b9a2d-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="b9a2d-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="b9a2d-151">98,765.43</span></span>              | <span data-ttu-id="b9a2d-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="b9a2d-152">98,765.40</span></span>              | <span data-ttu-id="b9a2d-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-153">98,765.00</span></span>              | <span data-ttu-id="b9a2d-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-154">98,700.00</span></span>                | <span data-ttu-id="b9a2d-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-155">98,765.00</span></span>                |
| <span data-ttu-id="b9a2d-156">Oma etu, saatavien saldo</span><span class="sxs-lookup"><span data-stu-id="b9a2d-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="b9a2d-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="b9a2d-157">98,765.43</span></span>              | <span data-ttu-id="b9a2d-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="b9a2d-158">98,765.50</span></span>              | <span data-ttu-id="b9a2d-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-159">98,766.00</span></span>              | <span data-ttu-id="b9a2d-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-160">98,800.00</span></span>                | <span data-ttu-id="b9a2d-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="b9a2d-162">Normaali pyöristys ja pyöristyksen tarkkuus on 0,01</span><span class="sxs-lookup"><span data-stu-id="b9a2d-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="b9a2d-163">Pyöristys</span><span class="sxs-lookup"><span data-stu-id="b9a2d-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="b9a2d-164">Laskentaprosessi</span><span class="sxs-lookup"><span data-stu-id="b9a2d-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="b9a2d-165">round(1.015, 0.01) = 1.02</span><span class="sxs-lookup"><span data-stu-id="b9a2d-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="b9a2d-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="b9a2d-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="b9a2d-167">102 \* 0.01 = 1.02</span><span class="sxs-lookup"><span data-stu-id="b9a2d-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="b9a2d-168">round(1.014, 0.01) = 1.01</span><span class="sxs-lookup"><span data-stu-id="b9a2d-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="b9a2d-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="b9a2d-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="b9a2d-170">101 \* 0.01 = 1.01</span><span class="sxs-lookup"><span data-stu-id="b9a2d-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="b9a2d-171">round(1.011, 0.02) = 1.02</span><span class="sxs-lookup"><span data-stu-id="b9a2d-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="b9a2d-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="b9a2d-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="b9a2d-173">51 \* 0.02 = 1.02</span><span class="sxs-lookup"><span data-stu-id="b9a2d-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="b9a2d-174">round(1.009, 0.02) = 1.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="b9a2d-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="b9a2d-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="b9a2d-176">50 \* 0.02 = 1.00</span><span class="sxs-lookup"><span data-stu-id="b9a2d-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="b9a2d-177">Jos valitset Oma etu, pyöristys tehdään aina yrityksen eduksi.</span><span class="sxs-lookup"><span data-stu-id="b9a2d-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="b9a2d-178">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="b9a2d-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="b9a2d-179">Arvonlisäveron yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b9a2d-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="b9a2d-180">Arvonlisäveromaksun luominen</span><span class="sxs-lookup"><span data-stu-id="b9a2d-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="b9a2d-181">Luo arvonlisäverotapahtumia asiakirjoihin</span><span class="sxs-lookup"><span data-stu-id="b9a2d-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="b9a2d-182">Näytä kirjatut arvonlisäverotapahtumat</span><span class="sxs-lookup"><span data-stu-id="b9a2d-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- <span data-ttu-id="b9a2d-183">[pyöristysfunktio](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="b9a2d-183">[round Function](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
