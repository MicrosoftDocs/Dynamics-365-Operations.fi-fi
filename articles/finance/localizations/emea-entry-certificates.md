---
title: EU-saapumistodistus
description: Tässä artikkelissa on tietoja Euroopan unionin (EU) saapumistodistuksista.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bf074f54448dd10f190263c09e731c4f4b7a61c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839771"
---
# <a name="eu-entry-certificates"></a><span data-ttu-id="e5f4a-103">EU-saapumistodistukset</span><span class="sxs-lookup"><span data-stu-id="e5f4a-103">EU entry certificates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5f4a-104">Tässä artikkelissa on tietoja Euroopan unionin (EU) saapumistodistuksista.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-104">This article provides information about European Union (EU) entry certificates.</span></span>

<span data-ttu-id="e5f4a-105">Voit suorittaa seuraavat Euroopan unionin (EU) saapumistodistuksen tehtävät:</span><span class="sxs-lookup"><span data-stu-id="e5f4a-105">You can complete the following tasks for a European Union (EU) entry certificate:</span></span>

-   <span data-ttu-id="e5f4a-106">Luo ja julkaise EU-saapumistodistus yhdessä pakkausluettelon tai myyntilaskun kanssa nimikkeiden tai palveluiden toimittamiseksi EU-maihin tai EU-alueille.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-106">Create and issue an EU entry certificate together with a packing slip or customer invoice for the delivery of items or services to EU countries/regions.</span></span>
-   <span data-ttu-id="e5f4a-107">Vastaanota EU-asiakkaan allekirjoittama merkinnän varmenne.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-107">Receive the EU entry certificate that is signed by an EU customer.</span></span>
-   <span data-ttu-id="e5f4a-108">Lataa allekirjoitettu EU-saapumistodistus, joka on vastaanotettu joko asiakkaalta tai kolmannelta osapuolelta, joka on vastuussa nimikkeiden toimittamisesta asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-108">Upload the signed EU entry certificate that is received either from the customer or from a third party who is responsible for delivering items to the customer.</span></span>
-   <span data-ttu-id="e5f4a-109">Liitä ladattu EU-merkinnän sertifikaatti myyntilaskuun.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-109">Associate the uploaded EU entry certificate with a customer invoice.</span></span>
-   <span data-ttu-id="e5f4a-110">Päivitä ladatun EU-merkinnän varmenteen tila.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-110">Update the status of the uploaded EU entry certificate.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e5f4a-111">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="e5f4a-111">Prerequisites</span></span>
<span data-ttu-id="e5f4a-112">Seuraavassa taulukossa esitellään edellytykset, joiden on täytyttävä ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-112">The following table shows the prerequisites that must be in place before you start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5f4a-113">Luokka</span><span class="sxs-lookup"><span data-stu-id="e5f4a-113">Category</span></span></th>
<th><span data-ttu-id="e5f4a-114">Edellytys</span><span class="sxs-lookup"><span data-stu-id="e5f4a-114">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5f4a-115">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="e5f4a-115">Country/region</span></span></td>
<td><span data-ttu-id="e5f4a-116">Yrityksen ensisijainen osoitteen on oltava EU-jäsenvaltiossa.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-116">The primary address of the legal entity must be in a EU member state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5f4a-117">Liittyvät määritystehtävät</span><span class="sxs-lookup"><span data-stu-id="e5f4a-117">Related set up tasks</span></span></td>
<td><ul>
<li><span data-ttu-id="e5f4a-118">Valitse <strong>Myyntireskontran parametrit</strong> -sivulla vaihtoehdot <strong>Ota käyttöön merkinnän varmenteen hallinta</strong> ja <strong>Ota käyttöön merkinnän varmenteen myöntäminen</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-118">On the <strong>Accounts receivable parameters</strong> page, select the <strong>Enable entry certificate management</strong> and <strong>Enable entry certificate issuing</strong> options.</span></span></li>
<li><span data-ttu-id="e5f4a-119">Valitse <strong>Asiakkaat</strong>-sivun <strong>Lasku ja toimitus</strong> -pikavälilehdessä <strong>Merkinnän varmenne tarvitaan</strong> osoittamaan, että EU-saapumistodistus on pakollinen asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-119">On the <strong>Customers</strong> page, on the <strong>Invoice and delivery</strong> FastTab, select the <strong>Entry certificate required</strong> option to indicate that an EU entry certificate is mandatory for the customer.</span></span> <span data-ttu-id="e5f4a-120">Myönnä asiakkaalle yrityksen EU-saapumisilmoitus valitsemalla <strong>Myönnä merkinnän varmenne</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-120">Select the <strong>Issue entry certificate</strong> option to issue an EU entry certificate of the legal entity to the customer.</span></span></li>
<li><span data-ttu-id="e5f4a-121">Valitse <strong>Myyntireskontran parametrit</strong> -sivulla <strong>Merkinnän varmenne</strong> -viitteeksi numerosarjakoodi.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-121">On the <strong>Accounts receivable parameters</strong> page, select a number sequence code for the <strong>Entry certificate</strong> reference.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5f4a-122">Liittyvät tapahtumat</span><span class="sxs-lookup"><span data-stu-id="e5f4a-122">Related transactions</span></span></td>
<td><ul>
<li><span data-ttu-id="e5f4a-123">Luo asiakastili.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-123">Create a customer account.</span></span></li>
<li><span data-ttu-id="e5f4a-124">Luo myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-124">Create a sales order.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a><span data-ttu-id="e5f4a-125">EU-saapumistodistuksen luominen, rekisteröidään ja lataaminen</span><span class="sxs-lookup"><span data-stu-id="e5f4a-125">Creating, registering, and uploading an EU entry certificate</span></span>
<span data-ttu-id="e5f4a-126">Voit luoda EU-merkinnän varmenne automaattisesti vai manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-126">You can create an EU entry certificate automatically or manually.</span></span> <span data-ttu-id="e5f4a-127">EU-merkinnän sertifikaatti luodaan ja tulostetaan automaattisesti, kun kirjaat pakkausluettelon tai asiakkaan laskun käyttämällä **Pakkausluettelon kirjaus**- tai **Laskun kirjaus** -sivua.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-127">An EU entry certificate is created and printed automatically when you post a packing slip or invoice for a customer by using the **Packing slip posting** page or the **Posting invoice** page.</span></span> <span data-ttu-id="e5f4a-128">Voit luoda tai uudelleentulostaa EU-saapumistodistuksen manuaalisesti asiakaslaskulle **Laskukirjauskansio**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-128">To manually create or reprint an EU entry certificate for a customer invoice, use the **Invoice journal** page.</span></span> <span data-ttu-id="e5f4a-129">Voit myös antaa **Merkinnän varmenteen tosite** -sivulla tietoja kolmannen osapuolen myöntämästä EU-saapumistodistuksesta.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-129">Additionally, you can use the **Entry certificate journal** page to enter details about an EU entry certificate that is issued by a third party.</span></span>

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a><span data-ttu-id="e5f4a-130">EU-saapumistodistuksen luominen automaattisesti tai manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="e5f4a-130">Creating an EU entry certificate automatically or manually</span></span>

<span data-ttu-id="e5f4a-131">Voit luoda EU-saapumistodistuksia automaattisesti pakkausluettelon avulla **Kaikki myyntitilaukset** -sivulla tai laskun avulla **Myyntitilaus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-131">You can create an EU entry certificate automatically by using a packing slip on the **All sales orders** page or by using an invoice on the **Sales order** page.</span></span> <span data-ttu-id="e5f4a-132">Voit luoda EU-saapumistodistuksen manuaalisesti laskun avulla **Laskukirjauskansio**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-132">To manually create an EU entry certificate, you can use an invoice on the **Invoice journal** page.</span></span> <span data-ttu-id="e5f4a-133">Laskun todistuksen tila on kuitenkin muutettava ennen EU-saapumistodistuksen luontia manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-133">However, you must change the certification status of the invoice before you manually create an EU entry certificate.</span></span>

### <a name="registering-an-eu-entry-certificate"></a><span data-ttu-id="e5f4a-134">EU-saapumistodistuksen rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="e5f4a-134">Registering an EU entry certificate</span></span>

<span data-ttu-id="e5f4a-135">Jos rekisteröinti on pakollinen, voit rekisteröidä kolmannen osapuolen myöntämän EU-saapumistodistuksen **Merkinnän varmenteen tosite** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-135">If registration is required, you can use the **Entry certificate journal** page to register an EU entry certificate that is issued by a third party.</span></span>

### <a name="uploading-a-received-eu-entry-certificate"></a><span data-ttu-id="e5f4a-136">Vastaanotetun EU-saapumistodistuksen lataaminen</span><span class="sxs-lookup"><span data-stu-id="e5f4a-136">Uploading a received EU entry certificate</span></span>

<span data-ttu-id="e5f4a-137">Lataa EU-asiakkaan allekirjoittama EU-saapumistodistus **Liitteet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-137">Use the **Attachments** page to upload a received EU entry certificate that is signed by an EU customer.</span></span> <span data-ttu-id="e5f4a-138">Kun todistus on ladattu, voit liittää sen laskuun näyttönä nimikkeiden toimituksesta.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-138">After the certificate is uploaded, you can associate it with an invoice as proof that the items were delivered.</span></span> <span data-ttu-id="e5f4a-139">Tämä näyttö on pakollinen, jos on tehtävä lasku, joka ei sisällä arvonlisäveroa (ALV). Sitä käytetään myös tilintarkastuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-139">This proof is required if you must issue an invoice that doesn't include value-added tax (VAT), and it's also used during auditing.</span></span>

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a><span data-ttu-id="e5f4a-140">Valinnainen: Todistuksen tilan ja laskun tulostustilan päivittäminen</span><span class="sxs-lookup"><span data-stu-id="e5f4a-140">Optional: Updating the certification status and printing status of an invoice</span></span>

<span data-ttu-id="e5f4a-141">Voit päivittää saapumistodistuksen tilan ja myyntilaskun tulostustilan **Laskukirjauskansio**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-141">You can update the entry certification status and printing status of a customer invoice by using the **Invoice journal** page.</span></span>

## <a name="technical-information-for-system-administrators"></a><span data-ttu-id="e5f4a-142">Teknisiä tietoja järjestelmänvalvojille</span><span class="sxs-lookup"><span data-stu-id="e5f4a-142">Technical information for system administrators</span></span>
<span data-ttu-id="e5f4a-143">Jos sinulla ei ole niiden sivujen käyttöoikeutta, joita käytetään tämän tehtävän suorittamiseen, ota yhteys järjestelmänvalvojaan ja anna seuraavassa taulukossa näkyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="e5f4a-143">If you don't have access to the pages that are used to complete this task, contact your system administrator, and provide the information that is shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5f4a-144">Luokka</span><span class="sxs-lookup"><span data-stu-id="e5f4a-144">Category</span></span></th>
<th><span data-ttu-id="e5f4a-145">Edellytys</span><span class="sxs-lookup"><span data-stu-id="e5f4a-145">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5f4a-146">Käyttöoikeusroolit ja velvollisuudet</span><span class="sxs-lookup"><span data-stu-id="e5f4a-146">Security roles and duties</span></span></td>
<td><span data-ttu-id="e5f4a-147">Jos haluat määrittää ja luoda EU-merkinnän varmenteita nimikkeille tai palveluille, sinun on oltava sellaisen käyttöoikeusroolin jäsen, johon sisältyy seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="e5f4a-147">To set up and create EU entry certificates for items or services, you must be a member of a security role that includes the following duties:</span></span>
<ul>
<li><span data-ttu-id="e5f4a-148"><strong>Myyntireskontran käsittelijä</strong> (CustInvoiceAccountsReceivableClerk)</span><span class="sxs-lookup"><span data-stu-id="e5f4a-148"><strong>Accounts receivable clerk</strong> (CustInvoiceAccountsReceivableClerk)</span></span></li>
<li><span data-ttu-id="e5f4a-149"><strong>Asiakaspalvelun edustaja</strong> (TradeCustomerServiceRepresentative)</span><span class="sxs-lookup"><span data-stu-id="e5f4a-149"><strong>Customer service representative</strong> (TradeCustomerServiceRepresentative)</span></span></li>
<li><span data-ttu-id="e5f4a-150"><strong>Myyjä</strong> (TradeSalesClerk)</span><span class="sxs-lookup"><span data-stu-id="e5f4a-150"><strong>Sales clerk</strong> (TradeSalesClerk)</span></span></li>
<li><span data-ttu-id="e5f4a-151"><strong>Kuljetushenkilö</strong> (InventShippingClerk)</span><span class="sxs-lookup"><span data-stu-id="e5f4a-151"><strong>Shipping clerk</strong> (InventShippingClerk)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]