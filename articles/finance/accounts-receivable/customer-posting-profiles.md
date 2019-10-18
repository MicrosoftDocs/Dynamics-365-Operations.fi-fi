---
title: Asiakkaan kirjausprofiilit
description: Asiakkaan kirjausprofiilit ohjaavat asiakastapahtumien kirjausta kirjanpitoon.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bb2784d70e99c3c3443bed1b8cb040552b5b6f6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189059"
---
# <a name="customer-posting-profiles"></a><span data-ttu-id="6a10b-103">Asiakkaan kirjausprofiilit</span><span class="sxs-lookup"><span data-stu-id="6a10b-103">Customer posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a10b-104">Asiakkaan kirjausprofiilit ohjaavat asiakastapahtumien kirjausta kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="6a10b-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="6a10b-105">Asiakkaan kirjausprofiilit</span><span class="sxs-lookup"><span data-stu-id="6a10b-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="6a10b-106">Voit määrittää asiakkaan kirjausprofiilin avulla kirjanpitotilejä ja asiakirja-asetuksia kaikille asiakkaille, asiakasryhmällä tai yhdelle asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="6a10b-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="6a10b-107">Näitä asetuksia käytetään, kun luot myyntitilauksia, vapaatekstilaskuja, käteismaksuja, maksukehotuksia ja korkolaskuja.</span><span class="sxs-lookup"><span data-stu-id="6a10b-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="6a10b-108">Voit valita joissakin tapahtumissa eri kirjausprofiilin, joka ohittaa tällä sivulla tapahtumille määritetyn kirjausprofiilin.</span><span class="sxs-lookup"><span data-stu-id="6a10b-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="6a10b-109">Oletuskirjausprofiili määritetään Myyntireskontran parametrit -sivun Kirjanpito ja arvonlisävero -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="6a10b-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="6a10b-110">Oletuskirjausprofiili sisällytetään sitten automaattisesti uusien asiakirjojen otsikkoon, jossa voit vaihtaa tarvittaessa toisen kirjausprofiilin.</span><span class="sxs-lookup"><span data-stu-id="6a10b-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="6a10b-111">Voit liittää tapahtuman kirjaustyyppejä sisältäviä kirjausprofiileja myös Tapahtuman kirjausmääritykset -sivulla.</span><span class="sxs-lookup"><span data-stu-id="6a10b-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="6a10b-112">Kirjausmäärityksillä määritetään asiakastapahtumien kirjaus kirjanpitoon kirjausprofiilien sijasta.</span><span class="sxs-lookup"><span data-stu-id="6a10b-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="6a10b-113">Kirjausprofiilin luonti</span><span class="sxs-lookup"><span data-stu-id="6a10b-113">Creating a posting profile</span></span>
<span data-ttu-id="6a10b-114">Määritä valittua kirjausprofiilia käyttävät tapahtumien kirjaukset, joita käytetään kirjanpitotileillä.</span><span class="sxs-lookup"><span data-stu-id="6a10b-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="6a10b-115">Valitse valitulle kirjausprofiilille tilikoodi ja mahdollinen tili- tai ryhmänumero.</span><span class="sxs-lookup"><span data-stu-id="6a10b-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="6a10b-116">Kirjauksen aikana jokaiselle tapahtumalle sopivin kirjausprofiilin etsitään hakemalla sopivin tilikoodi-, tilinumero- tai ryhmä- ja numeroyhdistelmää seuraavassa järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="6a10b-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="6a10b-117">**Tilikoodi**-kentän arvo</span><span class="sxs-lookup"><span data-stu-id="6a10b-117">**Account code** field value</span></span> | <span data-ttu-id="6a10b-118">**Tilin/ryhmän numero** -kentän arvo</span><span class="sxs-lookup"><span data-stu-id="6a10b-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="6a10b-119">Haun prioriteetti</span><span class="sxs-lookup"><span data-stu-id="6a10b-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="6a10b-120">**Taulu**</span><span class="sxs-lookup"><span data-stu-id="6a10b-120">**Table**</span></span>                    | <span data-ttu-id="6a10b-121">Määrätty asiakastili</span><span class="sxs-lookup"><span data-stu-id="6a10b-121">Specific customer account</span></span>                       | <span data-ttu-id="6a10b-122">1</span><span class="sxs-lookup"><span data-stu-id="6a10b-122">1</span></span>               |
| <span data-ttu-id="6a10b-123">**Ryhmä**</span><span class="sxs-lookup"><span data-stu-id="6a10b-123">**Group**</span></span>                    | <span data-ttu-id="6a10b-124">Asiakkaalle määritetty asiakasryhmä</span><span class="sxs-lookup"><span data-stu-id="6a10b-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="6a10b-125">2</span><span class="sxs-lookup"><span data-stu-id="6a10b-125">2</span></span>               |
| <span data-ttu-id="6a10b-126">**Kaikki**</span><span class="sxs-lookup"><span data-stu-id="6a10b-126">**All**</span></span>                      | <span data-ttu-id="6a10b-127">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="6a10b-127">Blank</span></span>                                           | <span data-ttu-id="6a10b-128">3</span><span class="sxs-lookup"><span data-stu-id="6a10b-128">3</span></span>               |

<span data-ttu-id="6a10b-129">Jos haluat määrittää kaikille asiakastapahtumille saman kirjausprofiilin, määritä vain yksi kirjausprofiili Tilikoodi-kentässä arvolla Kaikki.</span><span class="sxs-lookup"><span data-stu-id="6a10b-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="6a10b-130">Määritä kirjausprofiili määrittämällä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6a10b-130">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6a10b-131">Kenttä</span><span class="sxs-lookup"><span data-stu-id="6a10b-131">Field</span></span></th>
<th><span data-ttu-id="6a10b-132">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="6a10b-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6a10b-133"><strong>Kirjausprofiili</strong></span><span class="sxs-lookup"><span data-stu-id="6a10b-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="6a10b-134">Anna kirjausprofiilin koodi.</span><span class="sxs-lookup"><span data-stu-id="6a10b-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="6a10b-135">Voit esimerkiksi luoda kaksi kirjausprofiilia, jotta asiakassaldot saadaan yhdelle tilille kansallisena valuuttana ja toiselle ulkomaan valuuttana.</span><span class="sxs-lookup"><span data-stu-id="6a10b-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="6a10b-136">Ensimmäisen tilin nimi voi olla vaikkapa Kansallinen ja toisen Ulkomainen.</span><span class="sxs-lookup"><span data-stu-id="6a10b-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a10b-137"><strong>Kuvaus</strong></span><span class="sxs-lookup"><span data-stu-id="6a10b-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="6a10b-138">Anna kirjausprofiilin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="6a10b-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="6a10b-139">Tätä käytetään vain helpottamaan kirjausprofiilin tunnistamista, kun sivua tarkastellaan.</span><span class="sxs-lookup"><span data-stu-id="6a10b-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a10b-140"><strong>Tilikoodi</strong></span><span class="sxs-lookup"><span data-stu-id="6a10b-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="6a10b-141">Määritä, koskeeko kirjausprofiili yhtä asiakasta, asiakasryhmää vai kaikki asiakkaita:</span><span class="sxs-lookup"><span data-stu-id="6a10b-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="6a10b-142"><strong>Taulu</strong> – Kirjausprofiili koskee yksittäistä asiakasta.</span><span class="sxs-lookup"><span data-stu-id="6a10b-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="6a10b-143">Valitse asiakastili Tilin/ryhmän numero -kentässä.</span><span class="sxs-lookup"><span data-stu-id="6a10b-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="6a10b-144"><strong>Ryhmä</strong> – Kirjausprofiili koskee asiakasryhmää.</span><span class="sxs-lookup"><span data-stu-id="6a10b-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="6a10b-145">Valitse asiakasryhmä Tilin/ryhmän numero -kentässä.</span><span class="sxs-lookup"><span data-stu-id="6a10b-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="6a10b-146"><strong>Kaikki</strong> – Kirjausprofiili koskee kaikkia asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="6a10b-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="6a10b-147">Jätä Tilin/ryhmän numero -kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="6a10b-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a10b-148"><strong>Tilin/ryhmän numero</strong></span><span class="sxs-lookup"><span data-stu-id="6a10b-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="6a10b-149">Jos Taulu on valittu Tilikoodi-kentässä, valitse kirjausprofiiliin liitetyn asiakkaan tilinumero.</span><span class="sxs-lookup"><span data-stu-id="6a10b-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="6a10b-150">Jos Ryhmä on valittu, valitse asiakasryhmä.</span><span class="sxs-lookup"><span data-stu-id="6a10b-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="6a10b-151">Jos Kaikki on valittu, jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="6a10b-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a10b-152"><strong>Reskontratili</strong></span><span class="sxs-lookup"><span data-stu-id="6a10b-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="6a10b-153">Valitse kirjanpitotili, jota käytetään asiakkaan yhteenvetotilinä kirjausprofiiliin liitetyillä asiakkailla.</span><span class="sxs-lookup"><span data-stu-id="6a10b-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a10b-154"><strong>Selvitystili</strong></span><span class="sxs-lookup"><span data-stu-id="6a10b-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="6a10b-155">Valitse kassavirtaennusteissa käytettävä maksuvalmiustili.</span><span class="sxs-lookup"><span data-stu-id="6a10b-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="6a10b-156">Tämä kentässä näkyy vain, jos kassavirtaennusteet ovat käytössä.</span><span class="sxs-lookup"><span data-stu-id="6a10b-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a10b-157"><strong>Arvonlisäveron ennakkomaksut</strong></span><span class="sxs-lookup"><span data-stu-id="6a10b-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="6a10b-158">Valitse arvonlisäveron tili etuajassa saatuja maksuja varten.</span><span class="sxs-lookup"><span data-stu-id="6a10b-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Seteli" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="6a10b-160"><strong>Huomautus</strong></span><span class="sxs-lookup"><span data-stu-id="6a10b-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6a10b-161">Määritä Myyntireskontran parametrit -sivulla kirjausprofiili, jota käytetään, kun maksu on merkitty ennakkomaksuksi.</span><span class="sxs-lookup"><span data-stu-id="6a10b-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a10b-162"><strong>Alennustili</strong></span><span class="sxs-lookup"><span data-stu-id="6a10b-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="6a10b-163">Valitse alennusvelkojen kirjanpitotili</span><span class="sxs-lookup"><span data-stu-id="6a10b-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a10b-164"><strong>Maksukehotukset</strong></span><span class="sxs-lookup"><span data-stu-id="6a10b-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="6a10b-165">Valitse maksukehotussarjan tunnus, jota käytetään asiakkaille, joille kirjausprofiili on määritetty.</span><span class="sxs-lookup"><span data-stu-id="6a10b-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a10b-166"><strong>Korkoryhmä</strong></span><span class="sxs-lookup"><span data-stu-id="6a10b-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="6a10b-167">Valitse korkokoodi, jolla lasketaan korko asiakkaille, joille kirjausprofiili on määritetty.</span><span class="sxs-lookup"><span data-stu-id="6a10b-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="6a10b-168">**Taulurajoitukset**</span><span class="sxs-lookup"><span data-stu-id="6a10b-168">**Table restrictions**</span></span>

<span data-ttu-id="6a10b-169">Määritä tapahtumille, joilla on valittu kirjausprofiili, tilitetäänkö tapahtumat automaattisesti, lasketaanko korko ja annetaanko maksukehotukset.</span><span class="sxs-lookup"><span data-stu-id="6a10b-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="6a10b-170">Voit myös valita tili, jota käytetään, kun valittuun kirjausprofiiliin liittyvät tapahtumat suljetaan.</span><span class="sxs-lookup"><span data-stu-id="6a10b-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="6a10b-171">Määritä kirjausprofiili määrittämällä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6a10b-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="6a10b-172">Kenttä</span><span class="sxs-lookup"><span data-stu-id="6a10b-172">Field</span></span>                 | <span data-ttu-id="6a10b-173">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="6a10b-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a10b-174">**Tilitys**</span><span class="sxs-lookup"><span data-stu-id="6a10b-174">**Settlement**</span></span>        | <span data-ttu-id="6a10b-175">Ota tämän kirjausprofiilin sisältävien tapahtuvien automaattinen tilitys käyttöön valitsemalla tämä asetus.</span><span class="sxs-lookup"><span data-stu-id="6a10b-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="6a10b-176">Jos tämä asetus poistetaan käytöstä, tapahtumat on tilitettävä manuaalisesti Tilitä avoimet tapahtumat- tai Lisää asiakkaan maksuja -sivulla.</span><span class="sxs-lookup"><span data-stu-id="6a10b-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="6a10b-177">**Kiinnostuksen kohteet**</span><span class="sxs-lookup"><span data-stu-id="6a10b-177">**Interest**</span></span>          | <span data-ttu-id="6a10b-178">Valitse tämä asetus, jos korko on laskettava tätä profiilia käyttävien asiakastilien jäljellä oleville saldoille.</span><span class="sxs-lookup"><span data-stu-id="6a10b-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="6a10b-179">Jos tämän asetuksen valinta poistetaan, korkoa ei lasketa näille asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="6a10b-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="6a10b-180">**Maksukehotus**</span><span class="sxs-lookup"><span data-stu-id="6a10b-180">**Collection letter**</span></span> | <span data-ttu-id="6a10b-181">Valitse tämä asetus, jos maksukehotuksen on luotava tätä profiilia käyttäville asiakastileille.</span><span class="sxs-lookup"><span data-stu-id="6a10b-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="6a10b-182">Jos tämän asetuksen valinta poistetaan, maksukehotuksia ei luoda näille asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="6a10b-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="6a10b-183">**Sulje**</span><span class="sxs-lookup"><span data-stu-id="6a10b-183">**Close**</span></span>             | <span data-ttu-id="6a10b-184">Valitse toinen kirjausprofiili, jota siirrytään käyttämään, kun tämän kirjausprofiilin tapahtumia suljetaan.</span><span class="sxs-lookup"><span data-stu-id="6a10b-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="6a10b-185">Tapahtuma katsotaan suljetuksi, kun se on selvitetty kokonaan.</span><span class="sxs-lookup"><span data-stu-id="6a10b-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="6a10b-186">Lisätietoja on ohjeaiheessa [Asiakkaan maksujen yleiskatsaus](../cash-bank-management/tasks/customer-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6a10b-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>
