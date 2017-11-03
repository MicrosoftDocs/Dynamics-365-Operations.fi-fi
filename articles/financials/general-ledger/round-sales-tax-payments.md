---
title: "Arvonlisäveromaksut ja pyöristyssäännöt"
description: "Tässä artikkelissa kerrotaan, miten ALV-viranomaisten pyöristyssäännön määrittäminen toimii, ja miten arvonlisäverosaldo pyöristetään arvonlisäverotyön arvonlisäveron selvityksen ja kirjauksen aikana."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 13470282efc6b9135e86355cf8071b841aad3071
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="e997b-103">Arvonlisäveromaksut ja pyöristyssäännöt</span><span class="sxs-lookup"><span data-stu-id="e997b-103">Sales tax payments and rounding rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e997b-104">Tässä artikkelissa kerrotaan, miten ALV-viranomaisten pyöristyssäännön määrittäminen toimii, ja miten arvonlisäverosaldo pyöristetään arvonlisäverotyön arvonlisäveron selvityksen ja kirjauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="e997b-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="e997b-105">Arvonlisäverot täytyy ilmoittaa ja maksaa säännöllisesti.</span><span class="sxs-lookup"><span data-stu-id="e997b-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="e997b-106">Tämä voidaan tehdä suorittamalla arvonlisäveron tilitys- ja kirjausprosessi Arvonlisävero-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e997b-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="e997b-107">Kauden arvonlisävero tilitetään arvonlisäverotilejä vastaan, ja alv-saldo kirjataan arvonlisäveron maksutilille.</span><span class="sxs-lookup"><span data-stu-id="e997b-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="e997b-108">Arvonlisäveron maksutilille kirjattu alv-saldo voidaan pyöristää veroviranomaisten ohjeiden mukaan määrittämällä Arvonlisävero-sivulla pyöristyssääntö.</span><span class="sxs-lookup"><span data-stu-id="e997b-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="e997b-109">Pyöristysero kirjataan arvonlisäveron pyöristystilille, joka valitaan kirjanpidossa Automaattisten tapahtumien tilit -kentästä.</span><span class="sxs-lookup"><span data-stu-id="e997b-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="e997b-110">Seuraavassa esimerkissä on kuvattu arvonlisäveron pyöristyssäännön toimintaa.</span><span class="sxs-lookup"><span data-stu-id="e997b-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="e997b-111">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="e997b-111">Example:</span></span>

<span data-ttu-id="e997b-112">Kauden arvonlisävero näyttää hyvityssaldoksi -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="e997b-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="e997b-113">Yritys on perinyt arvonlisäveroja enemmän kuin maksanut.</span><span class="sxs-lookup"><span data-stu-id="e997b-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="e997b-114">Yrityksellä on siten arvonlisäverovelkaa.</span><span class="sxs-lookup"><span data-stu-id="e997b-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="e997b-115">Yritys haluaa käyttää pyöristysmenetelmää, joka pyöristää saldon lähimpään 1,00 euroon.</span><span class="sxs-lookup"><span data-stu-id="e997b-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="e997b-116">Alv-kirjanpidosta vastaava käyttäjä tekee seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="e997b-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="e997b-117">Valitse Vero &gt; Välilliset verot &gt; Arvonlisävero &gt; Alv-viranomaiset.</span><span class="sxs-lookup"><span data-stu-id="e997b-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="e997b-118">Valitse Yleinen-pikavälilehdessä Pyöristystapa-kentästä Normaali.</span><span class="sxs-lookup"><span data-stu-id="e997b-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="e997b-119">Syötä Pyöristys-kenttään arvoksi 1,00.</span><span class="sxs-lookup"><span data-stu-id="e997b-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="e997b-120">Kun arvonlisävero täytyy maksaa, avaa Tilitä ja kirjaa arvonlisävero -sivu.</span><span class="sxs-lookup"><span data-stu-id="e997b-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="e997b-121">(Valitse Vero &gt; Ilmoitukset &gt; Arvonlisävero &gt; Tilitä ja kirjaa arvonlisävero.)</span><span class="sxs-lookup"><span data-stu-id="e997b-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="e997b-122">Arvonlisäveron maksutilillä oleva alv-velka (98 765,43) pyöristetään arvoon 98 765.</span><span class="sxs-lookup"><span data-stu-id="e997b-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="e997b-123">Seuraavassa taulukossa on esitetty, miten summa 98 765,43 summa pyöristetään käyttämällä kutakin Alv-viranomaiset-sivulla Pyöristystapa-kentästä valittavissa olevaa pyöristysmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="e997b-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="e997b-124">Pyöristystapavaihtoehto</span><span class="sxs-lookup"><span data-stu-id="e997b-124">Rounding form option</span></span>                | <span data-ttu-id="e997b-125">Pyöristysarvo = 0,01</span><span class="sxs-lookup"><span data-stu-id="e997b-125">Round-off value = 0.01</span></span> | <span data-ttu-id="e997b-126">Pyöristysarvo = 0,10</span><span class="sxs-lookup"><span data-stu-id="e997b-126">Round-off value = 0.10</span></span> | <span data-ttu-id="e997b-127">Pyöristysarvo = 1,00</span><span class="sxs-lookup"><span data-stu-id="e997b-127">Round-off value = 1.00</span></span> | <span data-ttu-id="e997b-128">Pyöristysarvo = 100,00</span><span class="sxs-lookup"><span data-stu-id="e997b-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="e997b-129">Normaali</span><span class="sxs-lookup"><span data-stu-id="e997b-129">Normal</span></span>                              | <span data-ttu-id="e997b-130">98 765,43</span><span class="sxs-lookup"><span data-stu-id="e997b-130">98,765.43</span></span>              | <span data-ttu-id="e997b-131">98 765,40</span><span class="sxs-lookup"><span data-stu-id="e997b-131">98,765.40</span></span>              | <span data-ttu-id="e997b-132">98 765,00</span><span class="sxs-lookup"><span data-stu-id="e997b-132">98,765.00</span></span>              | <span data-ttu-id="e997b-133">98 800,00</span><span class="sxs-lookup"><span data-stu-id="e997b-133">98,800.00</span></span>                |
| <span data-ttu-id="e997b-134">Alaspäin</span><span class="sxs-lookup"><span data-stu-id="e997b-134">Downward</span></span>                            | <span data-ttu-id="e997b-135">98 765,43</span><span class="sxs-lookup"><span data-stu-id="e997b-135">98,765.43</span></span>              | <span data-ttu-id="e997b-136">98 765,40</span><span class="sxs-lookup"><span data-stu-id="e997b-136">98,765.40</span></span>              | <span data-ttu-id="e997b-137">98 765,00</span><span class="sxs-lookup"><span data-stu-id="e997b-137">98,765.00</span></span>              | <span data-ttu-id="e997b-138">98 700,00</span><span class="sxs-lookup"><span data-stu-id="e997b-138">98,700.00</span></span>                |
| <span data-ttu-id="e997b-139">Pyöristys</span><span class="sxs-lookup"><span data-stu-id="e997b-139">Rounding-up</span></span>                         | <span data-ttu-id="e997b-140">98 765,43</span><span class="sxs-lookup"><span data-stu-id="e997b-140">98,765.43</span></span>              | <span data-ttu-id="e997b-141">98 765,50</span><span class="sxs-lookup"><span data-stu-id="e997b-141">98,765.50</span></span>              | <span data-ttu-id="e997b-142">98 766,00</span><span class="sxs-lookup"><span data-stu-id="e997b-142">98,766.00</span></span>              | <span data-ttu-id="e997b-143">98 800,00</span><span class="sxs-lookup"><span data-stu-id="e997b-143">98,800.00</span></span>                |
| <span data-ttu-id="e997b-144">Oma etu, maksettavien saldo</span><span class="sxs-lookup"><span data-stu-id="e997b-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="e997b-145">98 765,43</span><span class="sxs-lookup"><span data-stu-id="e997b-145">98,765.43</span></span>              | <span data-ttu-id="e997b-146">98 765,40</span><span class="sxs-lookup"><span data-stu-id="e997b-146">98,765.40</span></span>              | <span data-ttu-id="e997b-147">98 765,00</span><span class="sxs-lookup"><span data-stu-id="e997b-147">98,765.00</span></span>              | <span data-ttu-id="e997b-148">98 700,00</span><span class="sxs-lookup"><span data-stu-id="e997b-148">98,700.00</span></span>                |
| <span data-ttu-id="e997b-149">Oma etu, saatavien saldo</span><span class="sxs-lookup"><span data-stu-id="e997b-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="e997b-150">98 765,43</span><span class="sxs-lookup"><span data-stu-id="e997b-150">98,765.43</span></span>              | <span data-ttu-id="e997b-151">98 765,50</span><span class="sxs-lookup"><span data-stu-id="e997b-151">98,765.50</span></span>              | <span data-ttu-id="e997b-152">98 766,00</span><span class="sxs-lookup"><span data-stu-id="e997b-152">98,766.00</span></span>              | <span data-ttu-id="e997b-153">98 800,00</span><span class="sxs-lookup"><span data-stu-id="e997b-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="e997b-154">Jos valitset Oma etu, pyöristys tehdään aina yrityksen eduksi.</span><span class="sxs-lookup"><span data-stu-id="e997b-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="e997b-155">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="e997b-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="e997b-156">Arvonlisäveron yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e997b-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="e997b-157">Arvonlisäveromaksun luominen</span><span class="sxs-lookup"><span data-stu-id="e997b-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="e997b-158">Myyntitapahtumien luominen asiakirjoihin</span><span class="sxs-lookup"><span data-stu-id="e997b-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="e997b-159">Näytä kirjatut arvonlisäverotapahtumat</span><span class="sxs-lookup"><span data-stu-id="e997b-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)



