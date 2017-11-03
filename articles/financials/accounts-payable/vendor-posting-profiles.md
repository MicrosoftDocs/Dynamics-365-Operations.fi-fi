---
title: Toimittajan kirjausprofiilit
description: Toimittajan kirjausprofiilit ohjaavat toimittajatapahtumien kirjaamista kirjanpitoon.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7bf37ff484323fb05a35419889f2f89ab124fb27
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-posting-profiles"></a><span data-ttu-id="7ab36-103">Toimittajan kirjausprofiilit</span><span class="sxs-lookup"><span data-stu-id="7ab36-103">Vendor posting profiles</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7ab36-104">Toimittajan kirjausprofiilit ohjaavat toimittajatapahtumien kirjaamista kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="7ab36-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="7ab36-105">Toimittajan kirjausprofiilit</span><span class="sxs-lookup"><span data-stu-id="7ab36-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="7ab36-106">Voit määrittää toimittajan kirjausprofiilin avulla kirjanpitotilejä ja asiakirja-asetuksia kaikille toimittajille, toimittajaryhmälle tai yhdelle toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="7ab36-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors or a single vendor.</span></span> <span data-ttu-id="7ab36-107">Näitä asetuksia käytetään, kun luot ostotilauksia, toimittajan laskuja ja käteismaksuja.</span><span class="sxs-lookup"><span data-stu-id="7ab36-107">These settings will be used when you create purchase orders, vendor invoices and cash payments.</span></span> <span data-ttu-id="7ab36-108">Voit valita joissakin tapahtumissa eri kirjausprofiilin, joka ohittaa tällä sivulla tapahtumille määritetyn kirjausprofiilin.</span><span class="sxs-lookup"><span data-stu-id="7ab36-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> <span data-ttu-id="7ab36-109">Oletuskirjausprofiili määritetään Ostoreskontran parametrit -sivun Kirjanpito ja arvonlisävero -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="7ab36-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts payable parameters page.</span></span> <span data-ttu-id="7ab36-110">Oletuskirjausprofiili sisällytetään sitten automaattisesti uusien asiakirjojen otsikkoon, jossa voit vaihtaa tarvittaessa toisen kirjausprofiilin.</span><span class="sxs-lookup"><span data-stu-id="7ab36-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="7ab36-111">Voit liittää tapahtuman kirjaustyyppejä sisältäviä kirjausprofiileja myös Tapahtuman kirjausmääritykset -sivulla.</span><span class="sxs-lookup"><span data-stu-id="7ab36-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="7ab36-112">Kirjausmäärityksillä määritetään toimittajatapahtumien kirjaus kirjanpitoon kirjausprofiilien sijasta.</span><span class="sxs-lookup"><span data-stu-id="7ab36-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="7ab36-113">Kirjausprofiilin luonti</span><span class="sxs-lookup"><span data-stu-id="7ab36-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="7ab36-114">**Asetukset**</span><span class="sxs-lookup"><span data-stu-id="7ab36-114">**Setup**</span></span>

<span data-ttu-id="7ab36-115">Määritä valittua kirjausprofiilia käyttävät tapahtumien kirjaukset, joita käytetään kirjanpitotileillä.</span><span class="sxs-lookup"><span data-stu-id="7ab36-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="7ab36-116">Valitse valitulle kirjausprofiilille tilikoodi ja mahdollinen tili- tai ryhmänumero.</span><span class="sxs-lookup"><span data-stu-id="7ab36-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="7ab36-117">Kirjauksen aikana jokaiselle tapahtumalle sopivin kirjausprofiilin etsitään hakemalla sopivin tilikoodi-, tilinumero- tai ryhmä- ja numeroyhdistelmää seuraavassa järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="7ab36-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="7ab36-118">**Tilikoodi**-kentän arvo</span><span class="sxs-lookup"><span data-stu-id="7ab36-118">**Account code** field value</span></span> | <span data-ttu-id="7ab36-119">**Tilin/ryhmän numero** -kentän arvo</span><span class="sxs-lookup"><span data-stu-id="7ab36-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="7ab36-120">Haun prioriteetti</span><span class="sxs-lookup"><span data-stu-id="7ab36-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="7ab36-121">**Taulu**</span><span class="sxs-lookup"><span data-stu-id="7ab36-121">**Table**</span></span>                    | <span data-ttu-id="7ab36-122">Tietty toimittajatili</span><span class="sxs-lookup"><span data-stu-id="7ab36-122">Specific vendor account</span></span>                     | <span data-ttu-id="7ab36-123">1</span><span class="sxs-lookup"><span data-stu-id="7ab36-123">1</span></span>               |
| <span data-ttu-id="7ab36-124">**Ryhmä**</span><span class="sxs-lookup"><span data-stu-id="7ab36-124">**Group**</span></span>                    | <span data-ttu-id="7ab36-125">toimittajaryhmä, johon toimittaja on määritetty</span><span class="sxs-lookup"><span data-stu-id="7ab36-125">vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="7ab36-126">2</span><span class="sxs-lookup"><span data-stu-id="7ab36-126">2</span></span>               |
| <span data-ttu-id="7ab36-127">**Kaikki**</span><span class="sxs-lookup"><span data-stu-id="7ab36-127">**All**</span></span>                      | <span data-ttu-id="7ab36-128">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="7ab36-128">Blank</span></span>                                       | <span data-ttu-id="7ab36-129">3</span><span class="sxs-lookup"><span data-stu-id="7ab36-129">3</span></span>               |

<span data-ttu-id="7ab36-130">Jos haluat määrittää kaikille toimittajatapahtumille saman kirjausprofiilin, määritä vain yksi kirjausprofiili Tilikoodi-kentässä arvolla Kaikki.</span><span class="sxs-lookup"><span data-stu-id="7ab36-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="7ab36-131">Määritä kirjausprofiili määrittämällä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="7ab36-131">Specify the following values to set up your posting profile:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ab36-132">Kenttä</span><span class="sxs-lookup"><span data-stu-id="7ab36-132">Field</span></span></th>
<th><span data-ttu-id="7ab36-133">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="7ab36-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ab36-134"><strong>Kirjausprofiili</strong></span><span class="sxs-lookup"><span data-stu-id="7ab36-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="7ab36-135">Anna kirjausprofiilin koodi.</span><span class="sxs-lookup"><span data-stu-id="7ab36-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="7ab36-136">Voit esimerkiksi luoda kaksi kirjausprofiilia, jotta toimittajasaldot saadaan yhdelle tilille kansallisena valuuttana ja toiselle ulkomaan valuuttana.</span><span class="sxs-lookup"><span data-stu-id="7ab36-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="7ab36-137">Ensimmäisen tilin nimi voi olla vaikkapa Kansallinen ja toisen Ulkomainen.</span><span class="sxs-lookup"><span data-stu-id="7ab36-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ab36-138"><strong>Kuvaus</strong></span><span class="sxs-lookup"><span data-stu-id="7ab36-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="7ab36-139">Anna kirjausprofiilin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="7ab36-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ab36-140"><strong>Tilikoodi</strong></span><span class="sxs-lookup"><span data-stu-id="7ab36-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="7ab36-141">Määritä, käytetäänkö kirjausprofiilia tietyn toimittajan, toimittajaryhmän vai kaikkien toimittajien kohdalla:</span><span class="sxs-lookup"><span data-stu-id="7ab36-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="7ab36-142"><strong>Taulu</strong> – Kirjausprofiili koskee yksittäistä toimittajaa.</span><span class="sxs-lookup"><span data-stu-id="7ab36-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="7ab36-143">Valitse toimittajatili Tilin/ryhmän numero -kentässä.</span><span class="sxs-lookup"><span data-stu-id="7ab36-143">Select the vendor account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="7ab36-144"><strong>Ryhmä</strong> – Kirjausprofiili koskee toimittajaryhmää.</span><span class="sxs-lookup"><span data-stu-id="7ab36-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="7ab36-145">Valitse toimittajaryhmä Tilin/ryhmän numero -kentässä.</span><span class="sxs-lookup"><span data-stu-id="7ab36-145">Select the vendor group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="7ab36-146"><strong>Kaikki</strong> – Kirjausprofiili koskee kaikkia toimittajia.</span><span class="sxs-lookup"><span data-stu-id="7ab36-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="7ab36-147">Jätä Tilin/ryhmän numero -kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="7ab36-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ab36-148"><strong>Tilin/ryhmän numero</strong></span><span class="sxs-lookup"><span data-stu-id="7ab36-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="7ab36-149">Jos Taulu on valittu Tilikoodi-kentässä, valitse kirjausprofiiliin liitetyn toimittajan tilinumero.</span><span class="sxs-lookup"><span data-stu-id="7ab36-149">If Table is selected in the Account code field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="7ab36-150">Jos Ryhmä valitaan, valitse toimittajaryhmä.</span><span class="sxs-lookup"><span data-stu-id="7ab36-150">If Group is selected, select a vendor group.</span></span> <span data-ttu-id="7ab36-151">Jos Kaikki on valittu, jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="7ab36-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ab36-152"><strong>Reskontratili</strong></span><span class="sxs-lookup"><span data-stu-id="7ab36-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="7ab36-153">Valitse kirjanpitotili, jota käytetään yhteenvetotilinä kirjausprofiiliin liitetyillä toimittajilla.</span><span class="sxs-lookup"><span data-stu-id="7ab36-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7ab36-154"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Huomautus</span><span class="sxs-lookup"><span data-stu-id="7ab36-154"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="7ab36-155"><strong>Huomautus</strong></span><span class="sxs-lookup"><span data-stu-id="7ab36-155"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ab36-156">Jos Kirjanpitoparametrit-sivulla valitaan Käytä kirjausmäärityksiä -asetus, yhteenvetotilin sijaista käytetään toimittajan laskutapahtuman kirjausmääritystä.</span><span class="sxs-lookup"><span data-stu-id="7ab36-156">If the Use posting definitions toggle is selected in the General ledger parameters page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ab36-157"><strong>Selvitystili</strong></span><span class="sxs-lookup"><span data-stu-id="7ab36-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="7ab36-158">Valitse kassavirtaennusteissa käytettävä maksuvalmiustili.</span><span class="sxs-lookup"><span data-stu-id="7ab36-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="7ab36-159">Tämä kenttä on käytettävissä vain, kun kassavirtaennusteet on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="7ab36-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ab36-160"><strong>Arvonlisäveron ennakkomaksut</strong></span><span class="sxs-lookup"><span data-stu-id="7ab36-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="7ab36-161">Valitse arvonlisäveron tili etuajassa saatuja maksuja varten.</span><span class="sxs-lookup"><span data-stu-id="7ab36-161">Select the account for sales tax payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7ab36-162"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Huomautus</span><span class="sxs-lookup"><span data-stu-id="7ab36-162"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="7ab36-163"><strong>Huomautus</strong></span><span class="sxs-lookup"><span data-stu-id="7ab36-163"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ab36-164">Kirjausprofiili, jota käytetään, kun maksu merkitään ennakkomaksuksi, valitaan Ostoreskontran parametrit -sivun Kirjanpito ja arvonlisävero -alueen Ennakkomaksukirjauskansion kirjausprofiili -kentässä.</span><span class="sxs-lookup"><span data-stu-id="7ab36-164">The posting profile that is used when the payment is marked as a prepayment is selected in the Posting profile with prepayment journal voucher field in the Ledger and sales tax area of the Accounts payable parameters page.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ab36-165"><strong>Saapuminen</strong></span><span class="sxs-lookup"><span data-stu-id="7ab36-165"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="7ab36-166">Valitse se kirjanpitotili, jolle hyväksymistä odottavien toimittajan laskujen tiedot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="7ab36-166">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="7ab36-167">Tiedot tallennetaan laskurekisterikirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="7ab36-167">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="7ab36-168">Oletetaan esimerkiksi, että käyttäjä tallentaa toimittajan laskujen perustiedot laskurekisteriin, kun laskut vastaanotetaan.</span><span class="sxs-lookup"><span data-stu-id="7ab36-168">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="7ab36-169">Kun laskurekisteri kirjataan, tapahtumat kirjataan tässä ja Vastatili-kentässä annetulle tilille.</span><span class="sxs-lookup"><span data-stu-id="7ab36-169">When the invoice register is posted, the transactions are posted to the account that is entered here and in the Offset account field.</span></span> <span data-ttu-id="7ab36-170">Kun laskut hyväksytään, velka siirretään saapumistililtä toimittajan reskontratilille.</span><span class="sxs-lookup"><span data-stu-id="7ab36-170">When the invoices are approved, the debt is transferred from the Arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ab36-171"><strong>Vastatili</strong></span><span class="sxs-lookup"><span data-stu-id="7ab36-171"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="7ab36-172">Valitse se kirjanpitotili, jota käytetään hyväksymistä odottavien, laskurekisterin kautta päivitettävien toimittajan laskujen vastakirjauksiin.</span><span class="sxs-lookup"><span data-stu-id="7ab36-172">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="7ab36-173">Vastatili toimii saapumistileille kirjattujen tapahtumien vastatilinä.</span><span class="sxs-lookup"><span data-stu-id="7ab36-173">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="7ab36-174">Niinpä tili sisältääkin ostot toimittajilta, joita ei ole vielä hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="7ab36-174">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>
 

### <a name="table-restrictions"></a><span data-ttu-id="7ab36-175">**Taulurajoitukset**</span><span class="sxs-lookup"><span data-stu-id="7ab36-175">**Table restrictions**</span></span>

<span data-ttu-id="7ab36-176">Määritä tapahtumille, joilla on valittu kirjausprofiili, tilitetäänkö tapahtumat automaattisesti, lasketaanko korko ja annetaanko maksukehotukset.</span><span class="sxs-lookup"><span data-stu-id="7ab36-176">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="7ab36-177">Voit myös valita tili, jota käytetään, kun valittuun kirjausprofiiliin liittyvät tapahtumat suljetaan.</span><span class="sxs-lookup"><span data-stu-id="7ab36-177">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="7ab36-178">Määritä kirjausprofiili määrittämällä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="7ab36-178">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="7ab36-179">Kenttä</span><span class="sxs-lookup"><span data-stu-id="7ab36-179">Field</span></span>          | <span data-ttu-id="7ab36-180">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="7ab36-180">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab36-181">**Tilitys**</span><span class="sxs-lookup"><span data-stu-id="7ab36-181">**Settlement**</span></span> | <span data-ttu-id="7ab36-182">Ota tämän kirjausprofiilin sisältävien tapahtumien automaattinen tilitys käyttöön valitsemalla tämä asetus.</span><span class="sxs-lookup"><span data-stu-id="7ab36-182">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="7ab36-183">Jos tämä asetus poistetaan käytöstä, tapahtumat on tilitettävä manuaalisesti Tilitä avoimet tapahtumat -sivulla.</span><span class="sxs-lookup"><span data-stu-id="7ab36-183">If this option is cleared, you must manually settle transactions by using the Settle open transactions page.</span></span> |
| <span data-ttu-id="7ab36-184">**Peruuta**</span><span class="sxs-lookup"><span data-stu-id="7ab36-184">**Cancel**</span></span>     | <span data-ttu-id="7ab36-185">Valitse tämä asetus, jos haluat mahdollisuuden tämän kirjausprofiilin sisältävien tapahtumien peruuttamiseen.</span><span class="sxs-lookup"><span data-stu-id="7ab36-185">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="7ab36-186">**Sulje**</span><span class="sxs-lookup"><span data-stu-id="7ab36-186">**Close**</span></span>      | <span data-ttu-id="7ab36-187">Valitse toinen kirjausprofiili, jota siirrytään käyttämään, kun tämän kirjausprofiilin tapahtumia suljetaan.</span><span class="sxs-lookup"><span data-stu-id="7ab36-187">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="7ab36-188">Tapahtuma katsotaan suljetuksi, kun se on selvitetty kokonaan.</span><span class="sxs-lookup"><span data-stu-id="7ab36-188">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |






