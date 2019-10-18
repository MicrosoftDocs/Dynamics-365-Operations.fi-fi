---
title: Toimittajan kirjausprofiilit
description: Toimittajan kirjausprofiilit ohjaavat toimittajatapahtumien kirjaamista kirjanpitoon.
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43450c5f7ab8295b896b591880da9d0bddd955cf
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189289"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="4ba89-103">Toimittajan kirjausprofiilit</span><span class="sxs-lookup"><span data-stu-id="4ba89-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ba89-104">Toimittajan kirjausprofiilit ohjaavat toimittajatapahtumien kirjaamista kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="4ba89-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="4ba89-105">Toimittajan kirjausprofiilit</span><span class="sxs-lookup"><span data-stu-id="4ba89-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="4ba89-106">Voit määrittää toimittajan kirjausprofiilin avulla kirjanpitotilejä ja asiakirja-asetuksia kaikille toimittajille, toimittajaryhmälle tai yhdelle toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="4ba89-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors, or a single vendor.</span></span> <span data-ttu-id="4ba89-107">Näitä asetuksia käytetään, kun luot ostotilauksia, toimittajan laskuja ja käteismaksuja.</span><span class="sxs-lookup"><span data-stu-id="4ba89-107">These settings will be used when you create purchase orders, vendor invoices, and cash payments.</span></span> <span data-ttu-id="4ba89-108">Voit valita joissakin tapahtumissa eri kirjausprofiilin, joka ohittaa tällä sivulla tapahtumille määritetyn kirjausprofiilin.</span><span class="sxs-lookup"><span data-stu-id="4ba89-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions on this page.</span></span> <span data-ttu-id="4ba89-109">Oletuskirjausprofiili määritetään **Ostoreskontran parametrit** -sivun **Kirjanpito ja arvonlisävero** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="4ba89-109">The default posting profile is defined on the **Ledger and Sales Tax** FastTab on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="4ba89-110">Oletuskirjausprofiili sisällytetään sitten automaattisesti uusien asiakirjojen otsikkoon, jossa voit vaihtaa tarvittaessa toisen kirjausprofiilin.</span><span class="sxs-lookup"><span data-stu-id="4ba89-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile, if needed.</span></span>

<span data-ttu-id="4ba89-111">Voit liittää tapahtuman kirjaustyyppejä sisältäviä kirjausprofiileja myös **Tapahtuman kirjausmääritykset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4ba89-111">You can also associate posting definitions with transaction posting types on the **Transaction posting definitions** page.</span></span> <span data-ttu-id="4ba89-112">Kirjausmäärityksillä määritetään toimittajatapahtumien kirjaus kirjanpitoon kirjausprofiilien sijasta.</span><span class="sxs-lookup"><span data-stu-id="4ba89-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="4ba89-113">Kirjausprofiilin luonti</span><span class="sxs-lookup"><span data-stu-id="4ba89-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="4ba89-114">**Asetukset**</span><span class="sxs-lookup"><span data-stu-id="4ba89-114">**Setup**</span></span>

<span data-ttu-id="4ba89-115">Määritä valittua kirjausprofiilia käyttävät tapahtumien kirjaukset, joita käytetään kirjanpitotileillä.</span><span class="sxs-lookup"><span data-stu-id="4ba89-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="4ba89-116">Valitse valitulle kirjausprofiilille tilikoodi ja mahdollinen tili- tai ryhmänumero.</span><span class="sxs-lookup"><span data-stu-id="4ba89-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="4ba89-117">Kirjauksen aikana jokaiselle tapahtumalle sopivin kirjausprofiilin etsitään hakemalla sopivin tilikoodi-, tilinumero- tai ryhmä- ja numeroyhdistelmää seuraavassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="4ba89-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority.</span></span>

| <span data-ttu-id="4ba89-118">**Tilikoodi**-kentän arvo</span><span class="sxs-lookup"><span data-stu-id="4ba89-118">**Account code** field value</span></span> | <span data-ttu-id="4ba89-119">**Tilin/ryhmän numero** -kentän arvo</span><span class="sxs-lookup"><span data-stu-id="4ba89-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="4ba89-120">Haun prioriteetti</span><span class="sxs-lookup"><span data-stu-id="4ba89-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="4ba89-121">**Taulu**</span><span class="sxs-lookup"><span data-stu-id="4ba89-121">**Table**</span></span>                    | <span data-ttu-id="4ba89-122">Tietty toimittajatili</span><span class="sxs-lookup"><span data-stu-id="4ba89-122">Specific vendor account</span></span>                     | <span data-ttu-id="4ba89-123">1</span><span class="sxs-lookup"><span data-stu-id="4ba89-123">1</span></span>               |
| <span data-ttu-id="4ba89-124">**Ryhmä**</span><span class="sxs-lookup"><span data-stu-id="4ba89-124">**Group**</span></span>                    | <span data-ttu-id="4ba89-125">Toimittajaryhmä, johon toimittaja on määritetty</span><span class="sxs-lookup"><span data-stu-id="4ba89-125">Vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="4ba89-126">2</span><span class="sxs-lookup"><span data-stu-id="4ba89-126">2</span></span>               |
| <span data-ttu-id="4ba89-127">**Kaikki**</span><span class="sxs-lookup"><span data-stu-id="4ba89-127">**All**</span></span>                      | <span data-ttu-id="4ba89-128">Tyhjä</span><span class="sxs-lookup"><span data-stu-id="4ba89-128">Blank</span></span>                                       | <span data-ttu-id="4ba89-129">3</span><span class="sxs-lookup"><span data-stu-id="4ba89-129">3</span></span>               |

<span data-ttu-id="4ba89-130">Jos haluat määrittää kaikille toimittajatapahtumille saman kirjausprofiilin, määritä vain yksi kirjausprofiili **Tilikoodi**-kentässä arvolla **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="4ba89-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with **All** in the **Account code** field.</span></span> <span data-ttu-id="4ba89-131">Määritä kirjausprofiili määrittämällä seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="4ba89-131">Specify the following values to set up your posting profile.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4ba89-132">Kenttä</span><span class="sxs-lookup"><span data-stu-id="4ba89-132">Field</span></span></th>
<th><span data-ttu-id="4ba89-133">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="4ba89-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4ba89-134"><strong>Kirjausprofiili</strong></span><span class="sxs-lookup"><span data-stu-id="4ba89-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="4ba89-135">Anna kirjausprofiilin koodi.</span><span class="sxs-lookup"><span data-stu-id="4ba89-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="4ba89-136">Voit esimerkiksi luoda kaksi kirjausprofiilia, jotta toimittajasaldot saadaan yhdelle tilille kansallisena valuuttana ja toiselle ulkomaan valuuttana.</span><span class="sxs-lookup"><span data-stu-id="4ba89-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="4ba89-137">Ensimmäisen tilin nimi voi olla vaikkapa Kansallinen ja toisen Ulkomainen.</span><span class="sxs-lookup"><span data-stu-id="4ba89-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ba89-138"><strong>Kuvaus</strong></span><span class="sxs-lookup"><span data-stu-id="4ba89-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="4ba89-139">Anna kirjausprofiilin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="4ba89-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ba89-140"><strong>Tilikoodi</strong></span><span class="sxs-lookup"><span data-stu-id="4ba89-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="4ba89-141">Määritä, käytetäänkö kirjausprofiilia tietyn toimittajan, toimittajaryhmän vai kaikkien toimittajien kohdalla:</span><span class="sxs-lookup"><span data-stu-id="4ba89-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="4ba89-142"><strong>Taulu</strong> – Kirjausprofiili koskee yksittäistä toimittajaa.</span><span class="sxs-lookup"><span data-stu-id="4ba89-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="4ba89-143">Valitse toimittajatili <strong>Tilin/ryhmän numero</strong> -kentässä.</span><span class="sxs-lookup"><span data-stu-id="4ba89-143">Select the vendor account in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="4ba89-144"><strong>Ryhmä</strong> – Kirjausprofiili koskee toimittajaryhmää.</span><span class="sxs-lookup"><span data-stu-id="4ba89-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="4ba89-145">Valitse toimittajaryhmä <strong>Tilin/ryhmän numero</strong> -kentässä.</span><span class="sxs-lookup"><span data-stu-id="4ba89-145">Select the vendor group in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="4ba89-146"><strong>Kaikki</strong> – Kirjausprofiili koskee kaikkia toimittajia.</span><span class="sxs-lookup"><span data-stu-id="4ba89-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="4ba89-147">Jätä <strong>Tilin/ryhmän numero</strong> -kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="4ba89-147">Leave the <strong>Account/Group number</strong> field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ba89-148"><strong>Tilin/ryhmän numero</strong></span><span class="sxs-lookup"><span data-stu-id="4ba89-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="4ba89-149">Jos <strong>Taulu</strong> on valittu <strong>Tilikoodi</strong>-kentässä, valitse kirjausprofiiliin liitetyn toimittajan tilinumero.</span><span class="sxs-lookup"><span data-stu-id="4ba89-149">If <strong>Table</strong> is selected in the <strong>Account code</strong> field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="4ba89-150">Jos <strong>Ryhmä</strong> valitaan, valitse toimittajaryhmä.</span><span class="sxs-lookup"><span data-stu-id="4ba89-150">If <strong>Group</strong> is selected, select a vendor group.</span></span> <span data-ttu-id="4ba89-151">Jos <strong>Kaikki</strong> on valittu, jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="4ba89-151">If <strong>All</strong> is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ba89-152"><strong>Reskontratili</strong></span><span class="sxs-lookup"><span data-stu-id="4ba89-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="4ba89-153">Valitse kirjanpitotili, jota käytetään yhteenvetotilinä kirjausprofiiliin liitetyillä toimittajilla.</span><span class="sxs-lookup"><span data-stu-id="4ba89-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span> <span data-ttu-id="4ba89-154">Tämän päätilin <strong>Älä salli manuaalista määritystä</strong> -parametri merkitään.</span><span class="sxs-lookup"><span data-stu-id="4ba89-154">The <strong>Do not allow manual entry</strong> parameter for this main account will be marked.</span></span> <span data-ttu-id="4ba89-155">Jos poistat tämän tilin myöhemmin kirjausprofiilista, tarkista <strong>Älä salli manuaalista määritystä</strong> -asetus <strong>Päätilit</strong>-sivulla.</span><span class="sxs-lookup"><span data-stu-id="4ba89-155">If you subsequently remove this account from the posting profile, validate the <strong>Do not allow manual entry</strong> setting on the <strong>Main accounts</strong> page.</span></span> 
<p><span data-ttu-id="4ba89-156"><strong>Huomautus:</strong>Jos <strong>Kirjanpitoparametrit</strong>-sivulla valitaan <strong>Käytä kirjausmäärityksiä</strong> -asetus, yhteenvetotilin sijaista käytetään toimittajan laskutapahtuman kirjausmääritystä.</span><span class="sxs-lookup"><span data-stu-id="4ba89-156"><strong>Note:</strong> If the <strong>Use posting definitions</strong> option is selected on the <strong>General ledger parameters</strong> page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ba89-157"><strong>Selvitystili</strong></span><span class="sxs-lookup"><span data-stu-id="4ba89-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="4ba89-158">Valitse kassavirtaennusteissa käytettävä maksuvalmiustili.</span><span class="sxs-lookup"><span data-stu-id="4ba89-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="4ba89-159">Tämä kenttä on käytettävissä vain, kun kassavirtaennusteet on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4ba89-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ba89-160"><strong>Arvonlisäveron ennakkomaksut</strong></span><span class="sxs-lookup"><span data-stu-id="4ba89-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="4ba89-161">Valitse arvonlisäveron tili etuajassa saatuja maksuja varten.</span><span class="sxs-lookup"><span data-stu-id="4ba89-161">Select the account for sales tax payments that are received in advance.</span></span>
<p><span data-ttu-id="4ba89-162"><strong>Huomautus:</strong> <strong>Kirjaus</strong>-profiili, jota käytetään, kun maksu merkitään ennakkomaksuksi, valitaan <strong>Ostoreskontran parametrit</strong> -sivun <strong>Kirjanpito ja arvonlisävero</strong> -alueen <strong>Ennakkomaksukirjauskansion kirjausprofiili</strong> -kentässä.</span><span class="sxs-lookup"><span data-stu-id="4ba89-162"><strong>Note:</strong> The posting profile that is used when the payment is marked as a prepayment is selected in the <strong>Posting</strong> profile with <strong>Prepayment journal voucher</strong> field in the <strong>Ledger and sales tax</strong> area on the <strong>Accounts payable parameters</strong> page.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ba89-163"><strong>Saapuminen</strong></span><span class="sxs-lookup"><span data-stu-id="4ba89-163"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="4ba89-164">Valitse se kirjanpitotili, jolle hyväksymistä odottavien toimittajan laskujen tiedot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="4ba89-164">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="4ba89-165">Tiedot tallennetaan laskurekisterikirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="4ba89-165">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="4ba89-166">Oletetaan esimerkiksi, että käyttäjä tallentaa toimittajan laskujen perustiedot laskurekisteriin, kun laskut vastaanotetaan.</span><span class="sxs-lookup"><span data-stu-id="4ba89-166">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="4ba89-167">Kun laskurekisteri kirjataan, tapahtumat kirjataan tässä ja <strong>Vastatili</strong>-kentässä annetulle tilille.</span><span class="sxs-lookup"><span data-stu-id="4ba89-167">When the invoice register is posted, the transactions are posted to the account that is entered here and in the <strong>Offset account</strong> field.</span></span> <span data-ttu-id="4ba89-168">Kun laskut hyväksytään, velka siirretään saapumistililtä toimittajan reskontratilille.</span><span class="sxs-lookup"><span data-stu-id="4ba89-168">When the invoices are approved, the debt is transferred from the arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ba89-169"><strong>Vastatili</strong></span><span class="sxs-lookup"><span data-stu-id="4ba89-169"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="4ba89-170">Valitse se kirjanpitotili, jota käytetään hyväksymistä odottavien, laskurekisterin kautta päivitettävien toimittajan laskujen vastakirjauksiin.</span><span class="sxs-lookup"><span data-stu-id="4ba89-170">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="4ba89-171">Vastatili toimii saapumistileille kirjattujen tapahtumien vastatilinä.</span><span class="sxs-lookup"><span data-stu-id="4ba89-171">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="4ba89-172">Niinpä tili sisältääkin ostot toimittajilta, joita ei ole vielä hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="4ba89-172">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="4ba89-173">**Taulurajoitukset**</span><span class="sxs-lookup"><span data-stu-id="4ba89-173">**Table restrictions**</span></span>

<span data-ttu-id="4ba89-174">Määritä tapahtumille, joilla on valittu kirjausprofiili, tilitetäänkö tapahtumat automaattisesti, lasketaanko korko ja annetaanko maksukehotukset.</span><span class="sxs-lookup"><span data-stu-id="4ba89-174">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="4ba89-175">Voit myös valita tili, jota käytetään, kun valittuun kirjausprofiiliin liittyvät tapahtumat suljetaan.</span><span class="sxs-lookup"><span data-stu-id="4ba89-175">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="4ba89-176">Määritä kirjausprofiili määrittämällä seuraavat arvot</span><span class="sxs-lookup"><span data-stu-id="4ba89-176">Specify the following values to set up your posting profile</span></span>

| <span data-ttu-id="4ba89-177">Kenttä</span><span class="sxs-lookup"><span data-stu-id="4ba89-177">Field</span></span>          | <span data-ttu-id="4ba89-178">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="4ba89-178">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ba89-179">**Tilitys**</span><span class="sxs-lookup"><span data-stu-id="4ba89-179">**Settlement**</span></span> | <span data-ttu-id="4ba89-180">Ota tämän kirjausprofiilin sisältävien tapahtumien automaattinen tilitys käyttöön valitsemalla tämä asetus.</span><span class="sxs-lookup"><span data-stu-id="4ba89-180">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="4ba89-181">Jos tämä asetus poistetaan käytöstä, tapahtumat on tilitettävä manuaalisesti **Tilitä avoimet tapahtumat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4ba89-181">If this option is cleared, you must manually settle transactions by using the **Settle open transactions** page.</span></span> |
| <span data-ttu-id="4ba89-182">**Peruuta**</span><span class="sxs-lookup"><span data-stu-id="4ba89-182">**Cancel**</span></span>     | <span data-ttu-id="4ba89-183">Valitse tämä asetus, jos haluat mahdollisuuden tämän kirjausprofiilin sisältävien tapahtumien peruuttamiseen.</span><span class="sxs-lookup"><span data-stu-id="4ba89-183">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="4ba89-184">**Sulje**</span><span class="sxs-lookup"><span data-stu-id="4ba89-184">**Close**</span></span>      | <span data-ttu-id="4ba89-185">Valitse toinen kirjausprofiili, jota siirrytään käyttämään, kun tämän kirjausprofiilin tapahtumia suljetaan.</span><span class="sxs-lookup"><span data-stu-id="4ba89-185">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="4ba89-186">Tapahtuma katsotaan suljetuksi, kun se on selvitetty kokonaan.</span><span class="sxs-lookup"><span data-stu-id="4ba89-186">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |
