---
title: Numerosarjat
description: "Numerosarjoilla luodaan luettavia, yksilöllisiä tunnisteita niitä edellyttäville päätietojen tietueille ja tapahtumatietueille."
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63bf043124797b328116fd7951913eaeda6ff97b
ms.openlocfilehash: 8e3899e1ad5f4be754687c0e2d59348e7a773fd8
ms.contentlocale: fi-fi
ms.lasthandoff: 01/12/2018

---

# <a name="number-sequences"></a><span data-ttu-id="3ac49-103">Numerosarjat</span><span class="sxs-lookup"><span data-stu-id="3ac49-103">Number sequences</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3ac49-104">Numerosarjoilla luodaan luettavia, yksilöllisiä tunnisteita niitä edellyttäville päätietojen tietueille ja tapahtumatietueille.</span><span class="sxs-lookup"><span data-stu-id="3ac49-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="3ac49-105">Tunnisteen vaativaa päätiedon tietuetta tai tapahtumatietuetta kutsutaan nimellä *viite*.</span><span class="sxs-lookup"><span data-stu-id="3ac49-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="3ac49-106">Ennen kuin voit luoda viitteelle uusia tietueita, määritä numerosarja ja kohdista se viitteeseen.</span><span class="sxs-lookup"><span data-stu-id="3ac49-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="3ac49-107">Suosittelemme, että määrität numerosarjat **Organisaation hallinto** -sivujen avulla.</span><span class="sxs-lookup"><span data-stu-id="3ac49-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="3ac49-108">Jos moduulikohtaiset asetukset ovat pakollisia, voit käyttää moduulin parametrisivua määrittämään moduulin numerosarjan viitteitä.</span><span class="sxs-lookup"><span data-stu-id="3ac49-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="3ac49-109">Voit määrittää esimerkiksi kohdissa **Myyntireskontra** ja **Ostoreskontra** numerosarjaryhmiä, joilla kohdistetaan tietyt numerosarjat tietyille asiakkaille tai toimittajille.</span><span class="sxs-lookup"><span data-stu-id="3ac49-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span> 

<span data-ttu-id="3ac49-110">Kun määrität numerosarjan, sinun on määritettävä alue, joka määrittää, mitkä organisaatio käyttää numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="3ac49-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="3ac49-111">Vaikutusalue voi olla **Jaettu**, **Yritys**, **Oikeushenkilö** tai **Toimintayksikkö**.</span><span class="sxs-lookup"><span data-stu-id="3ac49-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="3ac49-112">Vieläkin tarkempia numerosarjoja saadaan yhdistämällä vaikutusalueet **Oikeushenkilö** ja **Yritys** sekä **Kirjanpidon vuosikalenterin kausi**.</span><span class="sxs-lookup"><span data-stu-id="3ac49-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span> 

<span data-ttu-id="3ac49-113">Numerosarjan muodot koostuvat segmenteistä.</span><span class="sxs-lookup"><span data-stu-id="3ac49-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="3ac49-114">Numerosarjat, joiden vaikutusalue on muu kuin **Jaettu**, voivat sisältää osia, jotka vastaavat vaikutusaluetta.</span><span class="sxs-lookup"><span data-stu-id="3ac49-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="3ac49-115">Esimerkiksi numerosarja, jonka vaikutusalue on **Oikeushenkilö**, voi sisältää yrityssegmentin.</span><span class="sxs-lookup"><span data-stu-id="3ac49-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="3ac49-116">Liittämällä vaikutusaluesegmentin numerosarjan muodossa voit tunnistaa tietyn tietueen vaikutusalueen katsomalla sen numero.</span><span class="sxs-lookup"><span data-stu-id="3ac49-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span> 

<span data-ttu-id="3ac49-117">Segmenttien, jotka vastaavat vaikutusalueita, numerosarjamuodot voivat sisältää **Vakio** ja **Aakkosnumeerinen**-segmentit.</span><span class="sxs-lookup"><span data-stu-id="3ac49-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="3ac49-118">**Vakio** -segmentti sisältää numeroita, kirjaimia tai symboleja, jotka eivät muutu.</span><span class="sxs-lookup"><span data-stu-id="3ac49-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="3ac49-119">**Aakkosnumeerinen**-segmentti sisältää joukon kirjaimia tai numeroita, jotka lisääntyvät aina, kun numeroa käytetään.</span><span class="sxs-lookup"><span data-stu-id="3ac49-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="3ac49-120">Käyttää ristikkomerkkiä (\#) edustamaan kasvavia numeroita ja et-merkkiä (&) edustamaan kasvavia kirjaimia.</span><span class="sxs-lookup"><span data-stu-id="3ac49-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="3ac49-121">Esimerkiksi muodon \#\#\#\#\#\_2017 avulla luodaan sarja 00001\_2017, 00002\_2017 jne.</span><span class="sxs-lookup"><span data-stu-id="3ac49-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

<a name="number-sequence-examples"></a><span data-ttu-id="3ac49-122">Numerosarjaesimerkit</span><span class="sxs-lookup"><span data-stu-id="3ac49-122">Number sequence examples</span></span>
------------------------

<span data-ttu-id="3ac49-123">Seuraavissa esimerkeissä näytetään, kuinka segmenttejä käytetään numerosarjamuotojen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="3ac49-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="3ac49-124">Erityisesti esimerkit osoittavat alueen segmenttien vaikutuksen.</span><span class="sxs-lookup"><span data-stu-id="3ac49-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="3ac49-125">Kuluraportin numerot</span><span class="sxs-lookup"><span data-stu-id="3ac49-125">Expense report numbers</span></span>

<span data-ttu-id="3ac49-126">Seuraavassa esimerkissä kuluraportin numerot määritetään yritykselle, jonka nimi on **CS**.</span><span class="sxs-lookup"><span data-stu-id="3ac49-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span> 

- <span data-ttu-id="3ac49-127">**Alue:** Matkalaskut</span><span class="sxs-lookup"><span data-stu-id="3ac49-127">**Area:** Travel and expense</span></span> 
- <span data-ttu-id="3ac49-128">**Viite:** Kuluraportin numero</span><span class="sxs-lookup"><span data-stu-id="3ac49-128">**Reference:** Expense report number</span></span> 
- <span data-ttu-id="3ac49-129">**Vaikutusalue:** Yritys</span><span class="sxs-lookup"><span data-stu-id="3ac49-129">**Scope:** Legal entity</span></span> 
- <span data-ttu-id="3ac49-130">**Yritys:** CS</span><span class="sxs-lookup"><span data-stu-id="3ac49-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="3ac49-131">Segmentit</span><span class="sxs-lookup"><span data-stu-id="3ac49-131">Segments</span></span>  | <span data-ttu-id="3ac49-132">Segmenttityyppi</span><span class="sxs-lookup"><span data-stu-id="3ac49-132">Segment type</span></span> | <span data-ttu-id="3ac49-133">Arvo</span><span class="sxs-lookup"><span data-stu-id="3ac49-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="3ac49-134">Segmentti 1</span><span class="sxs-lookup"><span data-stu-id="3ac49-134">Segment 1</span></span> | <span data-ttu-id="3ac49-135">Oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="3ac49-135">Legal entity</span></span> | <span data-ttu-id="3ac49-136">CS</span><span class="sxs-lookup"><span data-stu-id="3ac49-136">CS</span></span>        |
| <span data-ttu-id="3ac49-137">Segmentti 2</span><span class="sxs-lookup"><span data-stu-id="3ac49-137">Segment 2</span></span> | <span data-ttu-id="3ac49-138">Vakio</span><span class="sxs-lookup"><span data-stu-id="3ac49-138">Constant</span></span>     | <span data-ttu-id="3ac49-139">–KULU–</span><span class="sxs-lookup"><span data-stu-id="3ac49-139">-EXPENSE-</span></span> |
| <span data-ttu-id="3ac49-140">Segmentti 3</span><span class="sxs-lookup"><span data-stu-id="3ac49-140">Segment 3</span></span> | <span data-ttu-id="3ac49-141">Aakkosnumeerinen</span><span class="sxs-lookup"><span data-stu-id="3ac49-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="3ac49-142">**Esimerkki muotoillusta numerosta**: CS-KULU-0039</span><span class="sxs-lookup"><span data-stu-id="3ac49-142">**Example of formatted number**: CS-EXPENSE-0039</span></span> 

<span data-ttu-id="3ac49-143">Voit myös määrittää vastaavan numerosarjamuodon muihin yrityksiin.</span><span class="sxs-lookup"><span data-stu-id="3ac49-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="3ac49-144">Jos vaihdat vain esimerkiksi **RW**-yrityksen yritys-segmentin arvon, muotoiltu numero on RW-KULU-0039.</span><span class="sxs-lookup"><span data-stu-id="3ac49-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="3ac49-145">Voit myös vaihtaa koko numerosarjamuodon muihin yrityksiin.</span><span class="sxs-lookup"><span data-stu-id="3ac49-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="3ac49-146">Nyt voit esimerkiksi ohittaa yrityksen vaikutusalueen segmentin ja luoda muotoillun numeron, kuten Exp-0001.</span><span class="sxs-lookup"><span data-stu-id="3ac49-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="3ac49-147">Myyntitilausnumerot</span><span class="sxs-lookup"><span data-stu-id="3ac49-147">Sales order numbers</span></span>

<span data-ttu-id="3ac49-148">Seuraavassa esimerkissä myyntitilausnumerot määritetään yritystunnukselle **CEU**.</span><span class="sxs-lookup"><span data-stu-id="3ac49-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span> 

- <span data-ttu-id="3ac49-149">**Alue:** Myynti</span><span class="sxs-lookup"><span data-stu-id="3ac49-149">**Area:** Sales</span></span> 
- <span data-ttu-id="3ac49-150">**Viite:** Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="3ac49-150">**Reference:** Sales order</span></span> 
- <span data-ttu-id="3ac49-151">**Vaikutusalue:** yritys</span><span class="sxs-lookup"><span data-stu-id="3ac49-151">**Scope:** Company</span></span> 
- <span data-ttu-id="3ac49-152">**Yritys:** CEU</span><span class="sxs-lookup"><span data-stu-id="3ac49-152">**Company:** CEU</span></span>

| <span data-ttu-id="3ac49-153">Segmentit</span><span class="sxs-lookup"><span data-stu-id="3ac49-153">Segments</span></span>  | <span data-ttu-id="3ac49-154">Segmenttityyppi</span><span class="sxs-lookup"><span data-stu-id="3ac49-154">Segment type</span></span> | <span data-ttu-id="3ac49-155">Arvo</span><span class="sxs-lookup"><span data-stu-id="3ac49-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="3ac49-156">Segmentti 1</span><span class="sxs-lookup"><span data-stu-id="3ac49-156">Segment 1</span></span> | <span data-ttu-id="3ac49-157">Vakio</span><span class="sxs-lookup"><span data-stu-id="3ac49-157">Constant</span></span>     | <span data-ttu-id="3ac49-158">MT-</span><span class="sxs-lookup"><span data-stu-id="3ac49-158">SO-</span></span>      |
| <span data-ttu-id="3ac49-159">Segmentti 2</span><span class="sxs-lookup"><span data-stu-id="3ac49-159">Segment 2</span></span> | <span data-ttu-id="3ac49-160">Aakkosnumeerinen</span><span class="sxs-lookup"><span data-stu-id="3ac49-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="3ac49-161">**Esimerkki muotoillusta numerosta**: MT-0029</span><span class="sxs-lookup"><span data-stu-id="3ac49-161">**Example of formatted number**: SO-0029</span></span> 

<span data-ttu-id="3ac49-162">Vaikka vaikutusalueen segmenttiä ei ole sisällytetty muotoon, numerointi käynnistyy uudelleen jokaisen yrityksen tunnuksen kohdalla.</span><span class="sxs-lookup"><span data-stu-id="3ac49-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="3ac49-163">Jos käytät samaa muotoa kaikille yrityksen tunnuksille, samoja numeroita käytetään kussakin yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="3ac49-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="3ac49-164">Esimerkiksi myyntitilausta SO-0029 käytetään jokaisessa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="3ac49-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="3ac49-165">Voit myös vaihtaa koko numerosarjamuodon muuhun yritystunnukseen.</span><span class="sxs-lookup"><span data-stu-id="3ac49-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="3ac49-166">Ostoehdotuksen numerot</span><span class="sxs-lookup"><span data-stu-id="3ac49-166">Purchase requisition numbers</span></span>

<span data-ttu-id="3ac49-167">Seuraavassa esimerkissä ostoehdotusnumerot ovat organisaation laajuisia.</span><span class="sxs-lookup"><span data-stu-id="3ac49-167">In the following example, purchase requisition numbers are organization-wide.</span></span> 

- <span data-ttu-id="3ac49-168">**Alue:** osto</span><span class="sxs-lookup"><span data-stu-id="3ac49-168">**Area:** Purchase</span></span> 
- <span data-ttu-id="3ac49-169">**Viite:** ostoehdotus</span><span class="sxs-lookup"><span data-stu-id="3ac49-169">**Reference:** Purchase requisition</span></span> 
- <span data-ttu-id="3ac49-170">**Vaikutusalue:** Jaettu</span><span class="sxs-lookup"><span data-stu-id="3ac49-170">**Scope:** Shared</span></span>

| <span data-ttu-id="3ac49-171">Segmentit</span><span class="sxs-lookup"><span data-stu-id="3ac49-171">Segments</span></span>  | <span data-ttu-id="3ac49-172">Segmenttityyppi</span><span class="sxs-lookup"><span data-stu-id="3ac49-172">Segment type</span></span> | <span data-ttu-id="3ac49-173">Arvo</span><span class="sxs-lookup"><span data-stu-id="3ac49-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="3ac49-174">Segmentti 1</span><span class="sxs-lookup"><span data-stu-id="3ac49-174">Segment 1</span></span> | <span data-ttu-id="3ac49-175">Vakio</span><span class="sxs-lookup"><span data-stu-id="3ac49-175">Constant</span></span>     | <span data-ttu-id="3ac49-176">Tarv.</span><span class="sxs-lookup"><span data-stu-id="3ac49-176">Req</span></span>      |
| <span data-ttu-id="3ac49-177">Segmentti 2</span><span class="sxs-lookup"><span data-stu-id="3ac49-177">Segment 2</span></span> | <span data-ttu-id="3ac49-178">Aakkosnumeerinen</span><span class="sxs-lookup"><span data-stu-id="3ac49-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="3ac49-179">**Esimerkki muotoillusta numerosta**: Rek0052</span><span class="sxs-lookup"><span data-stu-id="3ac49-179">**Example of formatted number**: Req0052</span></span> 

<span data-ttu-id="3ac49-180">Vaikutusalue on **Jaettu**, joten numerosarjan muotoa käytetään koko organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="3ac49-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="3ac49-181">Et voi määrittää erilaisia numerosarjamuotoja organisaation eri osille.</span><span class="sxs-lookup"><span data-stu-id="3ac49-181">You cannot set up different number sequence formats for different parts of the organization.</span></span> 

<a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="3ac49-182">Numerosarjojen suorituskykyyn liittyviä tietoja</span><span class="sxs-lookup"><span data-stu-id="3ac49-182">Performance considerations for number sequences</span></span>
-----------------------------------------------

<span data-ttu-id="3ac49-183">Mieti seuraavia tietoja siitä, miten numerosarjat määritys voi vaikuttaa järjestelmän suorituskykyyn, ennen kuin määrität numerosarjoja.</span><span class="sxs-lookup"><span data-stu-id="3ac49-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="3ac49-184">Jatkuvat ja ei-jatkuvat numerosarjat</span><span class="sxs-lookup"><span data-stu-id="3ac49-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="3ac49-185">Numerosarjat voivat olla jatkuvia tai ei-jatkuvia.</span><span class="sxs-lookup"><span data-stu-id="3ac49-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="3ac49-186">Jatkuva numerosarja ei ohita yhtäkään numeroa, mutta numeroita ei voi käyttää peräkkäin.</span><span class="sxs-lookup"><span data-stu-id="3ac49-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="3ac49-187">Ei-jatkuvien numerosarjojen numerot käytetään sarjassa, mutta numerosarja voi ohittaa numeroita.</span><span class="sxs-lookup"><span data-stu-id="3ac49-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="3ac49-188">Jos esimerkiksi käyttäjä peruuttaa tapahtuman, numero luodaan mutta sitä ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="3ac49-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="3ac49-189">Jatkuvassa numerosarjassa sitä numeroa kierrätetään myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="3ac49-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="3ac49-190">Numerosarjassa, joka ei ole jatkuva numerosarja, numeroa ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="3ac49-190">In a non-continuous number sequence, the number is not used.</span></span> 

<span data-ttu-id="3ac49-191">Ulkoiset asiakirjat, kuten ostotilaukset, myyntitilaukset ja laskut, vaativat tavallisesti jatkuvat numerosarjat.</span><span class="sxs-lookup"><span data-stu-id="3ac49-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="3ac49-192">Kuitenkin jatkuvat numerosarjat saattavat heikentää järjestelmän vasteaikaa, koska järjestelmän on pyydettävä numeroa tietokannasta aina, kun uusi asiakirja tai tietue luodaan.</span><span class="sxs-lookup"><span data-stu-id="3ac49-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span> 

<span data-ttu-id="3ac49-193">Jos käytössä ei ole jatkuvaa numerosarja, **Esijako** voidaan ottaa käyttöön **Numerosarja**-sivun **Suorituskyky**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="3ac49-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="3ac49-194">Kun määrität ennalta kohdistettavan numeroiden määrän, järjestelmä valitsee numerot ja tallentaa ne muistiin.</span><span class="sxs-lookup"><span data-stu-id="3ac49-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="3ac49-195">Uudet numerot pyydetään tietokannasta vasta sitten, kun esijaettu määrä on käytetty.</span><span class="sxs-lookup"><span data-stu-id="3ac49-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span> 

<span data-ttu-id="3ac49-196">Elleivät säännökset vaadi jatkuvien numerosarjojen käyttöä, suosittelemme, että käytät ei-jatkuvia numerosarjoja paremman suorituskyvyn vuoksi.</span><span class="sxs-lookup"><span data-stu-id="3ac49-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="3ac49-197">Automaattinen numerosarjojen puhdistus</span><span class="sxs-lookup"><span data-stu-id="3ac49-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="3ac49-198">Järjestelmä ei voi kierrättää numeroita automaattisesti jatkuvia numerosarjoja varten sähkökatkoksen, sovellusvirheen tai muun odottamattoman vian takia.</span><span class="sxs-lookup"><span data-stu-id="3ac49-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="3ac49-199">Voit suorittaa vapautusprosessi manuaalisesti tai automaattisesti palauttaaksesi menetetyt numerot.</span><span class="sxs-lookup"><span data-stu-id="3ac49-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span> 

<span data-ttu-id="3ac49-200">Mieti palvelimen käyttö puhdistusprosessin suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="3ac49-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="3ac49-201">On suositeltavaa suorittaa vapautus erätyönä hiljaisena aikana.</span><span class="sxs-lookup"><span data-stu-id="3ac49-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>






