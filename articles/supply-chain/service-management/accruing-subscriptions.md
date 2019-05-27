---
title: Ylläpitosopimusten jaksottaminen
description: Huollon ylläpitosopimuksissa tuotot jaksotetaan manuaalisesti maksutapahtuman laskutuspäivämäärää seuraaville kausille.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a183e17749c04b407eb17155ecb1363e96ade18a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546637"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="24116-103">Ylläpitosopimusten jaksottaminen</span><span class="sxs-lookup"><span data-stu-id="24116-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="24116-104">Huollon ylläpitosopimuksissa tuotot jaksotetaan manuaalisesti maksutapahtuman laskutuspäivämäärää seuraaville kausille.</span><span class="sxs-lookup"><span data-stu-id="24116-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="24116-105">Jaksotuskaudet luodaan ylläpitosopimusmaksulle määrittämällesi laskutuskaudelle, ja ne perustuvat ylläpitosopimuksen kausikoodiin.</span><span class="sxs-lookup"><span data-stu-id="24116-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="24116-106">Jaksotetun tuoton voi palauttaa.</span><span class="sxs-lookup"><span data-stu-id="24116-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="24116-107">Palauta hyvitysten jaksotukset</span><span class="sxs-lookup"><span data-stu-id="24116-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="24116-108">Jos hyvität laskutettuja ylläpitosopimuksen summia, voit palauttaa jaksotetut summat kahden eri menetelmän avulla.</span><span class="sxs-lookup"><span data-stu-id="24116-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="24116-109">Kukin jaksotetun tuoton tapahtuma on palautettava erikseen ennen hyvityslaskuehdotuksen luomista tapahtumalle.</span><span class="sxs-lookup"><span data-stu-id="24116-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="24116-110">Tämä on manuaalinen menetelmä.</span><span class="sxs-lookup"><span data-stu-id="24116-110">This is the manual method.</span></span> <span data-ttu-id="24116-111">(manuaalinen)</span><span class="sxs-lookup"><span data-stu-id="24116-111">(manual)</span></span>

  - <span data-ttu-id="24116-112">Voit valita jaksotetun summan palautuksen hyvityslaskun kirjauspäivänä tai jaksotuksen alkuperäisenä kirjauspäivämääränä.</span><span class="sxs-lookup"><span data-stu-id="24116-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="24116-113">Lisätietoja on kohdassa [Ylläpitosopimuksen parametrit (lomake)](https://technet.microsoft.com/en-us/library/aa619615.aspx).</span><span class="sxs-lookup"><span data-stu-id="24116-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/en-us/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="24116-114">Määritä edellytykset</span><span class="sxs-lookup"><span data-stu-id="24116-114">Setup requirements</span></span>

<span data-ttu-id="24116-115">Jotta tuoton voi jaksottaa, varmista, että seuraavat tietovaatimukset täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="24116-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="24116-116">Tiliasetukset</span><span class="sxs-lookup"><span data-stu-id="24116-116">Account setup</span></span>

<span data-ttu-id="24116-117">**KET - ylläpitosopimus**- ja **Jaksotettu tuotto - ylläpitosopimus** -tilit on määritettävä **Projekti**-moduulissa.</span><span class="sxs-lookup"><span data-stu-id="24116-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="24116-118">Kun jaksotettu tuotto kirjataan, jaksotetulla summalla veloitetaan **KET - tilaus** -tiliä ja hyvitetään **Jaksotettu tuotto - ylläpitosopimus** -tiliä.</span><span class="sxs-lookup"><span data-stu-id="24116-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="24116-119">Tilien määrittäminen ylläpitosopimuksen tuoton jaksottamisen</span><span class="sxs-lookup"><span data-stu-id="24116-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="24116-120">Valitse **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Kirjaus** \> **Kirjanpidon asetukset**.</span><span class="sxs-lookup"><span data-stu-id="24116-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="24116-121">Valitse **Tuottotilit**-välilehti ja valitse **KET - yYlläpitosopimus** tai **Jaksotettu tuotto - ylläpitosopimus** tilien määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="24116-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="24116-122">Ylläpitosopimusryhmän asetukset</span><span class="sxs-lookup"><span data-stu-id="24116-122">Subscription group setup</span></span>

<span data-ttu-id="24116-123">**Jaksota tuotot** -valintaruudun on oltava valittuna, jotta ylläpitosopimuksen tuotto voidaan jaksottaa.</span><span class="sxs-lookup"><span data-stu-id="24116-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="24116-124">Valintaruutu on **Ylläpitosopimusryhmät**-lomakkeessa ryhmälle, joka on liitetty ylläpitosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="24116-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="24116-125">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltotilaukset** \> **Ylläpitosopimusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="24116-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="24116-126">Tuoton jaksottamisen käyttöönotto ylläpitosopimusryhmälle</span><span class="sxs-lookup"><span data-stu-id="24116-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="24116-127">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltotilaukset** \> **Ylläpitosopimusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="24116-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="24116-128">Kaudet</span><span class="sxs-lookup"><span data-stu-id="24116-128">Periods</span></span>

<span data-ttu-id="24116-129">Laskutuskauden koodi on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="24116-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="24116-130">Jos et halua käyttää tuottojen jaksotukseen samoja aikavälejä kuin laskutukseen, myös jaksotuskausi on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="24116-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="24116-131">Seuraavassa taulukossa on yhteenveto siitä, mitä jaksotuskausia voi määrittää millekin laskutuskausille:</span><span class="sxs-lookup"><span data-stu-id="24116-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="24116-132">Laskutuskausi</span><span class="sxs-lookup"><span data-stu-id="24116-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="24116-133">Jaksotuskaudet</span><span class="sxs-lookup"><span data-stu-id="24116-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24116-134"><strong>Vuosia</strong></span><span class="sxs-lookup"><span data-stu-id="24116-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24116-135"><strong>Vuosia</strong></span><span class="sxs-lookup"><span data-stu-id="24116-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="24116-136"><strong>Vuosineljännes</strong></span><span class="sxs-lookup"><span data-stu-id="24116-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="24116-137"><strong>Kuukausi</strong></span><span class="sxs-lookup"><span data-stu-id="24116-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="24116-138"><strong>Päivä</strong></span><span class="sxs-lookup"><span data-stu-id="24116-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24116-139"><strong>Vuosineljännes</strong></span><span class="sxs-lookup"><span data-stu-id="24116-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24116-140"><strong>Vuosineljännes</strong></span><span class="sxs-lookup"><span data-stu-id="24116-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="24116-141"><strong>Kuukausi</strong></span><span class="sxs-lookup"><span data-stu-id="24116-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="24116-142"><strong>Päivä</strong></span><span class="sxs-lookup"><span data-stu-id="24116-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24116-143"><strong>Kuukausi</strong></span><span class="sxs-lookup"><span data-stu-id="24116-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24116-144"><strong>Kuukausi</strong></span><span class="sxs-lookup"><span data-stu-id="24116-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="24116-145"><strong>Päivä</strong></span><span class="sxs-lookup"><span data-stu-id="24116-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24116-146"><strong>Viikko</strong></span><span class="sxs-lookup"><span data-stu-id="24116-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24116-147"><strong>Päivä</strong></span><span class="sxs-lookup"><span data-stu-id="24116-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24116-148"><strong>Päivä</strong></span><span class="sxs-lookup"><span data-stu-id="24116-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="24116-149"><strong>Päivä</strong></span><span class="sxs-lookup"><span data-stu-id="24116-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24116-150">Laskutuskauden määrittäminen on pakollinen osa ylläpitosopimusryhmän asetuksia.</span><span class="sxs-lookup"><span data-stu-id="24116-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="24116-151">Voit määrittää myös ylläpitosopimusryhmän jaksotuskauden.</span><span class="sxs-lookup"><span data-stu-id="24116-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="24116-152">Jos määrität ylläpitosopimusryhmälle jaksotuskauden, ohjelma ehdottaa tätä kautta **Kausikoodi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="24116-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="24116-153">Tämä kenttä sisältyy **Ylläpitosopimuksen tuoton jaksottaminen** -lomakkeeseen ylläpitosopimuksen tuottoa jaksotettaessa.</span><span class="sxs-lookup"><span data-stu-id="24116-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="24116-154">Jaksotuskausi kuuluu kuitenkin ylläpitosopimusryhmän valinnaisiin tietoihin.</span><span class="sxs-lookup"><span data-stu-id="24116-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="24116-155">Avaa <STRONG>Ylläpitosopimuksen tuoton jaksottaminen</STRONG> -lomake käyttämällä seuraavaa polkua.</span><span class="sxs-lookup"><span data-stu-id="24116-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="24116-156">Valitse <STRONG>Huoltohallinta</STRONG> &gt; <STRONG>Kausittainen</STRONG> &gt; <STRONG>Huoltotilaukset</STRONG> &gt; <STRONG>Jaksota ylläpitosopimuksen tuotto</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="24116-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="24116-157">Tapahtumat</span><span class="sxs-lookup"><span data-stu-id="24116-157">Transactions</span></span>

<span data-ttu-id="24116-158">Voit määrittää, kuinka monta kirjanpitotapahtumaa luodaan, kun jaksotettu tuotto kirjataan.</span><span class="sxs-lookup"><span data-stu-id="24116-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="24116-159">Määritä ylläpitosopimuksissa, luodaanko kirjanpidon tapahtumat kokonaissummana vai riveittäin.</span><span class="sxs-lookup"><span data-stu-id="24116-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="24116-160">Jaksotetuille tapahtumille näytettävien kirjaustietojen tason määrittäminen</span><span class="sxs-lookup"><span data-stu-id="24116-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="24116-161">Valitse **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Projektinhallinnan ja kirjanpidon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="24116-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="24116-162">Valitse **Taloushallinto**-välilehden **Laskutus**-kentästä **Yhteensä** tai **Rivi**.</span><span class="sxs-lookup"><span data-stu-id="24116-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="24116-163">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="24116-163">See also</span></span>

[<span data-ttu-id="24116-164">Jaksota ylläpitosopimuksen tuotto</span><span class="sxs-lookup"><span data-stu-id="24116-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  


