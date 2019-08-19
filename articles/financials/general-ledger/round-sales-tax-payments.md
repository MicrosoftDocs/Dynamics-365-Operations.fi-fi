---
title: Arvonlisäveromaksut ja pyöristyssäännöt
description: Tässä artikkelissa kerrotaan, miten ALV-viranomaisten pyöristyssäännön määrittäminen toimii, ja miten arvonlisäverosaldo pyöristetään arvonlisäverotyön arvonlisäveron selvityksen ja kirjauksen aikana.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834995"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="f0071-103">Arvonlisäveromaksut ja pyöristyssäännöt</span><span class="sxs-lookup"><span data-stu-id="f0071-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0071-104">Tässä artikkelissa kerrotaan, miten ALV-viranomaisten pyöristyssäännön määrittäminen toimii, ja miten arvonlisäverosaldo pyöristetään arvonlisäverotyön arvonlisäveron selvityksen ja kirjauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="f0071-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="f0071-105">Arvonlisäverot täytyy ilmoittaa ja maksaa säännöllisesti.</span><span class="sxs-lookup"><span data-stu-id="f0071-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="f0071-106">Tämä voidaan tehdä suorittamalla arvonlisäveron tilitys- ja kirjausprosessi Arvonlisävero-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f0071-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="f0071-107">Kauden arvonlisävero tilitetään arvonlisäverotilejä vastaan, ja alv-saldo kirjataan arvonlisäveron maksutilille.</span><span class="sxs-lookup"><span data-stu-id="f0071-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="f0071-108">Arvonlisäveron maksutilille kirjattu alv-saldo voidaan pyöristää veroviranomaisten ohjeiden mukaan määrittämällä Arvonlisävero-sivulla pyöristyssääntö.</span><span class="sxs-lookup"><span data-stu-id="f0071-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="f0071-109">Pyöristysero kirjataan arvonlisäveron pyöristystilille, joka valitaan kirjanpidossa Automaattisten tapahtumien tilit -kentästä.</span><span class="sxs-lookup"><span data-stu-id="f0071-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="f0071-110">Seuraavassa esimerkissä on kuvattu arvonlisäveron pyöristyssäännön toimintaa.</span><span class="sxs-lookup"><span data-stu-id="f0071-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="f0071-111">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="f0071-111">Examples</span></span>

<span data-ttu-id="f0071-112">Kauden arvonlisävero näyttää hyvityssaldoksi -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="f0071-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="f0071-113">Yritys on perinyt arvonlisäveroja enemmän kuin maksanut.</span><span class="sxs-lookup"><span data-stu-id="f0071-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="f0071-114">Yrityksellä on siten arvonlisäverovelkaa.</span><span class="sxs-lookup"><span data-stu-id="f0071-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="f0071-115">Yritys haluaa käyttää pyöristysmenetelmää, joka pyöristää saldon lähimpään 1,00 euroon.</span><span class="sxs-lookup"><span data-stu-id="f0071-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="f0071-116">Alv-kirjanpidosta vastaava käyttäjä tekee seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="f0071-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="f0071-117">Valitse Vero &gt; Välilliset verot &gt; Arvonlisävero &gt; Alv-viranomaiset.</span><span class="sxs-lookup"><span data-stu-id="f0071-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="f0071-118">Valitse Yleinen-pikavälilehdessä Pyöristystapa-kentästä Normaali.</span><span class="sxs-lookup"><span data-stu-id="f0071-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="f0071-119">Syötä Pyöristys-kenttään arvoksi 1,00.</span><span class="sxs-lookup"><span data-stu-id="f0071-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="f0071-120">Kun arvonlisävero täytyy maksaa, avaa Tilitä ja kirjaa arvonlisävero -sivu.</span><span class="sxs-lookup"><span data-stu-id="f0071-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="f0071-121">(Valitse Vero &gt; Ilmoitukset &gt; Arvonlisävero &gt; Tilitä ja kirjaa arvonlisävero.)</span><span class="sxs-lookup"><span data-stu-id="f0071-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="f0071-122">Arvonlisäveron maksutilillä oleva alv-velka (98 765,43) pyöristetään arvoon 98 765.</span><span class="sxs-lookup"><span data-stu-id="f0071-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="f0071-123">Seuraavassa taulukossa on esitetty, miten summa 98 765,43 summa pyöristetään käyttämällä kutakin Alv-viranomaiset-sivulla Pyöristystapa-kentästä valittavissa olevaa pyöristysmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="f0071-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="f0071-124">Pyöristystapavaihtoehto</span><span class="sxs-lookup"><span data-stu-id="f0071-124">Rounding form option</span></span>                | <span data-ttu-id="f0071-125">Pyöristysarvo = 0,01</span><span class="sxs-lookup"><span data-stu-id="f0071-125">Round-off value = 0.01</span></span> | <span data-ttu-id="f0071-126">Pyöristysarvo = 0,10</span><span class="sxs-lookup"><span data-stu-id="f0071-126">Round-off value = 0.10</span></span> | <span data-ttu-id="f0071-127">Pyöristysarvo = 1,00</span><span class="sxs-lookup"><span data-stu-id="f0071-127">Round-off value = 1.00</span></span> | <span data-ttu-id="f0071-128">Pyöristysarvo = 100,00</span><span class="sxs-lookup"><span data-stu-id="f0071-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="f0071-129">Normaali</span><span class="sxs-lookup"><span data-stu-id="f0071-129">Normal</span></span>                              | <span data-ttu-id="f0071-130">98 765,43</span><span class="sxs-lookup"><span data-stu-id="f0071-130">98,765.43</span></span>              | <span data-ttu-id="f0071-131">98 765,40</span><span class="sxs-lookup"><span data-stu-id="f0071-131">98,765.40</span></span>              | <span data-ttu-id="f0071-132">98 765,00</span><span class="sxs-lookup"><span data-stu-id="f0071-132">98,765.00</span></span>              | <span data-ttu-id="f0071-133">98 800,00</span><span class="sxs-lookup"><span data-stu-id="f0071-133">98,800.00</span></span>                |
| <span data-ttu-id="f0071-134">Alaspäin</span><span class="sxs-lookup"><span data-stu-id="f0071-134">Downward</span></span>                            | <span data-ttu-id="f0071-135">98 765,43</span><span class="sxs-lookup"><span data-stu-id="f0071-135">98,765.43</span></span>              | <span data-ttu-id="f0071-136">98 765,40</span><span class="sxs-lookup"><span data-stu-id="f0071-136">98,765.40</span></span>              | <span data-ttu-id="f0071-137">98 765,00</span><span class="sxs-lookup"><span data-stu-id="f0071-137">98,765.00</span></span>              | <span data-ttu-id="f0071-138">98 700,00</span><span class="sxs-lookup"><span data-stu-id="f0071-138">98,700.00</span></span>                |
| <span data-ttu-id="f0071-139">Pyöristys</span><span class="sxs-lookup"><span data-stu-id="f0071-139">Rounding-up</span></span>                         | <span data-ttu-id="f0071-140">98 765,43</span><span class="sxs-lookup"><span data-stu-id="f0071-140">98,765.43</span></span>              | <span data-ttu-id="f0071-141">98 765,50</span><span class="sxs-lookup"><span data-stu-id="f0071-141">98,765.50</span></span>              | <span data-ttu-id="f0071-142">98 766,00</span><span class="sxs-lookup"><span data-stu-id="f0071-142">98,766.00</span></span>              | <span data-ttu-id="f0071-143">98 800,00</span><span class="sxs-lookup"><span data-stu-id="f0071-143">98,800.00</span></span>                |
| <span data-ttu-id="f0071-144">Oma etu, maksettavien saldo</span><span class="sxs-lookup"><span data-stu-id="f0071-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="f0071-145">98 765,43</span><span class="sxs-lookup"><span data-stu-id="f0071-145">98,765.43</span></span>              | <span data-ttu-id="f0071-146">98 765,40</span><span class="sxs-lookup"><span data-stu-id="f0071-146">98,765.40</span></span>              | <span data-ttu-id="f0071-147">98 765,00</span><span class="sxs-lookup"><span data-stu-id="f0071-147">98,765.00</span></span>              | <span data-ttu-id="f0071-148">98 700,00</span><span class="sxs-lookup"><span data-stu-id="f0071-148">98,700.00</span></span>                |
| <span data-ttu-id="f0071-149">Oma etu, saatavien saldo</span><span class="sxs-lookup"><span data-stu-id="f0071-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="f0071-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="f0071-150">98,765.43</span></span>              | <span data-ttu-id="f0071-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="f0071-151">98,765.50</span></span>              | <span data-ttu-id="f0071-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="f0071-152">98,766.00</span></span>              | <span data-ttu-id="f0071-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="f0071-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="f0071-154">Ei pyöristystä, koska pyöristys on 0,00</span><span class="sxs-lookup"><span data-stu-id="f0071-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="f0071-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span><span class="sxs-lookup"><span data-stu-id="f0071-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="f0071-156">Normaali pyöristys ja pyöristyksen tarkkuus on 0,01</span><span class="sxs-lookup"><span data-stu-id="f0071-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="f0071-157">Pyöristys</span><span class="sxs-lookup"><span data-stu-id="f0071-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="f0071-158">Laskentaprosessi</span><span class="sxs-lookup"><span data-stu-id="f0071-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="f0071-159">round(1.015, 0.01) = 1.02</span><span class="sxs-lookup"><span data-stu-id="f0071-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="f0071-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="f0071-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="f0071-161">102 \* 0.01 = 1.02</span><span class="sxs-lookup"><span data-stu-id="f0071-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="f0071-162">round(1.014, 0.01) = 1.01</span><span class="sxs-lookup"><span data-stu-id="f0071-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="f0071-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="f0071-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="f0071-164">101 \* 0.01 = 1.01</span><span class="sxs-lookup"><span data-stu-id="f0071-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="f0071-165">round(1.011, 0.02) = 1.02</span><span class="sxs-lookup"><span data-stu-id="f0071-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="f0071-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="f0071-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="f0071-167">51 \* 0.02 = 1.02</span><span class="sxs-lookup"><span data-stu-id="f0071-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="f0071-168">round(1.009, 0.02) = 1.00</span><span class="sxs-lookup"><span data-stu-id="f0071-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="f0071-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="f0071-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="f0071-170">50 \* 0.02 = 1.00</span><span class="sxs-lookup"><span data-stu-id="f0071-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="f0071-171">Jos valitset Oma etu, pyöristys tehdään aina yrityksen eduksi.</span><span class="sxs-lookup"><span data-stu-id="f0071-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="f0071-172">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="f0071-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="f0071-173">Arvonlisäveron yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f0071-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="f0071-174">Arvonlisäveromaksun luominen</span><span class="sxs-lookup"><span data-stu-id="f0071-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="f0071-175">Myyntitapahtumien luominen asiakirjoihin</span><span class="sxs-lookup"><span data-stu-id="f0071-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="f0071-176">Näytä kirjatut arvonlisäverotapahtumat</span><span class="sxs-lookup"><span data-stu-id="f0071-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="f0071-177">pyöristysfunktio</span><span class="sxs-lookup"><span data-stu-id="f0071-177">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


