---
title: Skannattujen asiakirjojen laskuautomaatio
description: Tässä ohjeaiheessa kerrotaan ominaisuuksista, joita voidaan käyttää toimittajalaskujen päästä päähän -automatisointiin. Tämä koskee myös laskuja, jotka sisältävät liitteitä.
author: abruer
manager: AnnBe
ms.date: 05/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6d19d0e10f477e498e8f0fff1f431bc4bfdd9a1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442711"
---
# <a name="invoice-automation-for-scanned-documents"></a><span data-ttu-id="074e0-103">Skannattujen asiakirjojen laskuautomaatio</span><span class="sxs-lookup"><span data-stu-id="074e0-103">Invoice automation for scanned documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="074e0-104">Tässä ohjeaiheessa kerrotaan ominaisuuksista, joita voidaan käyttää toimittajalaskujen päästä päähän -automatisointiin. Tämä koskee myös laskuja, jotka sisältävät liitteitä.</span><span class="sxs-lookup"><span data-stu-id="074e0-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="074e0-105">Organisaatiot, jotka haluavat helpottaa ostoreskontran prosessejaan, määrittelevät usein laskutusprosessin yhdeksi tärkeimmäksi tehostettavaksi prosessialueeksi.</span><span class="sxs-lookup"><span data-stu-id="074e0-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="074e0-106">Usein nämä organisaatiot siirtävät paperilaskujen käsittelyn ulkoiselle optisten merkkien tunnistuksen (OCR) palveluntarjoajalle.</span><span class="sxs-lookup"><span data-stu-id="074e0-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="074e0-107">Ne saavat koneellisesti luettavat laskun metatiedot ja jokaisen laskun skannatun kuvan.</span><span class="sxs-lookup"><span data-stu-id="074e0-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="074e0-108">Automaation avuksi luodaan "viimeisen osuuden" ratkaisu, joka mahdollistaa näiden artefaktien käytön laskutusjärjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="074e0-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="074e0-109">Nyt tämä viimeisen osuuden automaatio on valmiiksi käytössä laskuautomaatioratkaisun avulla.</span><span class="sxs-lookup"><span data-stu-id="074e0-109">Now this “last mile” automation is enabled out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="074e0-110">Ratkaisukonteksti</span><span class="sxs-lookup"><span data-stu-id="074e0-110">Solution context</span></span>

<span data-ttu-id="074e0-111">Laskuautomaatioratkaisu tuo käyttöön vakiokäyttöliittymän, joka sisällyttää laskun metatiedot laskun otsikkoon ja laskutusriveille sekä mahdolliset laskuliitteet.</span><span class="sxs-lookup"><span data-stu-id="074e0-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="074e0-112">Mikä tahansa ulkoinen järjestelmä, joka voi luoda tämän käyttöliittymän kanssa yhteensopivia artefakteja, voi lähettää syötteen laskujen ja liitteiden automaattista käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="074e0-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="074e0-113">Seuraavassa kuvassa on esimerkkitilanne integroinnista, jossa Contoso on tehnyt yhteistyötä OCR-palveluntarjoajan kanssa toimittajan laskun käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="074e0-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="074e0-114">Contoson palveluntarjoajat lähettävät laskuja palveluntarjoajalle sähköpostitse.</span><span class="sxs-lookup"><span data-stu-id="074e0-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="074e0-115">Palveluntarjoajan luo OCR-käsittelyn avulla laskun metatiedot (otsikon ja/tai rivit) ja skannatun kuvan laskusta.</span><span class="sxs-lookup"><span data-stu-id="074e0-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="074e0-116">Integrointitaso muuntaa sitten nämä artefaktit yhteensopivaan muotoon.</span><span class="sxs-lookup"><span data-stu-id="074e0-116">An integration layer then transforms these artifacts so that they can be consumed.</span></span>

![Esimerkkiskenaario integroinnista](media/vendor_invoice_automation_01.png)

<span data-ttu-id="074e0-118">Edellisestä skenaariosta on useita mahdollisia versioita, jos laskun integrointi on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="074e0-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="074e0-119">Toinen käyttöliittymän käyttötapa on tietojen siirtäminen laskujen ja liitteiden luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="074e0-119">Data migration is another use case where this interface can be used to create invoices and attachments.</span></span>

### <a name="solution-components"></a><span data-ttu-id="074e0-120">Ratkaisukomponentit</span><span class="sxs-lookup"><span data-stu-id="074e0-120">Solution components</span></span>

<span data-ttu-id="074e0-121">Seuraavat komponentit sisältyvät kattavaan ratkaisuun:</span><span class="sxs-lookup"><span data-stu-id="074e0-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="074e0-122">Laskuotsikon, laskurivien ja laskun liitteiden tietoyksiköt</span><span class="sxs-lookup"><span data-stu-id="074e0-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="074e0-123">Laskujen poikkeusten käsittely</span><span class="sxs-lookup"><span data-stu-id="074e0-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="074e0-124">Laskujen liitteiden rinnakkainen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="074e0-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="074e0-125">Tämä aiheohje sisältää myös näiden ratkaisukomponenttien yksityiskohtaiset kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="074e0-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="074e0-126">Tietoyksiköt</span><span class="sxs-lookup"><span data-stu-id="074e0-126">Data entities</span></span>

<span data-ttu-id="074e0-127">Datapaketti on työyksikkö, joka on lähetettävä, jotta laskujen otsikot, laskurivit ja laskujen liitteet voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="074e0-127">A data package is the unit of work that must be sent so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="074e0-128">Seuraavia tietoyksiköitä käytetään datapaketin muodostavien artefaktien luomiseen:</span><span class="sxs-lookup"><span data-stu-id="074e0-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="074e0-129">Toimittajan laskun otsikko</span><span class="sxs-lookup"><span data-stu-id="074e0-129">Vendor invoice header</span></span>
+ <span data-ttu-id="074e0-130">Toimittajan laskurivi</span><span class="sxs-lookup"><span data-stu-id="074e0-130">Vendor invoice line</span></span>
+ <span data-ttu-id="074e0-131">Toimittajan laskun asiakirjaliite</span><span class="sxs-lookup"><span data-stu-id="074e0-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="074e0-132">Toimittajan laskun asiakirjaliite on uusi toiminnon osana esiteltävä tietoyksikkö.</span><span class="sxs-lookup"><span data-stu-id="074e0-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="074e0-133">Toimittajan laskun otsikkoa on muokattu siten, että se tukee liitteitä.</span><span class="sxs-lookup"><span data-stu-id="074e0-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="074e0-134">Toimittajan laskuriviyksikköä ei ole muutettu tämän toiminnon osalta.</span><span class="sxs-lookup"><span data-stu-id="074e0-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="074e0-135">Lisätietoja tietopaketeista on kohdassa [Tietojen hallinnan yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="074e0-135">For detailed information about data packages, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span> <span data-ttu-id="074e0-136">Lisätietoja tietopakettien luonnista tietojen hallinnan työtilassa on kohdassa [Tietopakettien käsittely ja kuluttaminen Dynamics 365 Finance and Operations -sovellusratkaisussa](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="074e0-136">For information about how to create data packages using the data management workspace, see [Process and consume data packages in Dynamics 365 Finance and Operations apps solution](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span></span>

<span data-ttu-id="074e0-137">Noudata näitä vaiheita, kun haluat luoda nopeasti testitietoja, jotka sisältävät laskuja ja -liitteitä.</span><span class="sxs-lookup"><span data-stu-id="074e0-137">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="074e0-138">Kirjaudu sisään esiintymääsi.</span><span class="sxs-lookup"><span data-stu-id="074e0-138">Sign in to your instance.</span></span>
1. <span data-ttu-id="074e0-139">Valitse **Ostoreskontra** > **Laskut** > **Avoimet toimittajan laskut**.</span><span class="sxs-lookup"><span data-stu-id="074e0-139">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="074e0-140">Luo laskuja, joissa on rivejä ja liitteitä.</span><span class="sxs-lookup"><span data-stu-id="074e0-140">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="074e0-141">Liitteiden on oltava otsikon liitteitä.</span><span class="sxs-lookup"><span data-stu-id="074e0-141">The attachments must be header attachments.</span></span> <span data-ttu-id="074e0-142">Toimittajan laskun asiakirjaliiteyksiköt eivät tue tällä hetkellä riviliitteitä.</span><span class="sxs-lookup"><span data-stu-id="074e0-142">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="074e0-143">Avaa **Tietojen hallinta** -työtila.</span><span class="sxs-lookup"><span data-stu-id="074e0-143">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="074e0-144">Luo vientityö, joka sisältää toimittajan laskun otsikko-, toimittajan laskun rivi- ja toimittajan laskun asiakirjaliite -yksiköt.</span><span class="sxs-lookup"><span data-stu-id="074e0-144">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="074e0-145">Vie tiedot.</span><span class="sxs-lookup"><span data-stu-id="074e0-145">Export the data.</span></span>
1. <span data-ttu-id="074e0-146">Lataa viedyt tiedot pakettina.</span><span class="sxs-lookup"><span data-stu-id="074e0-146">Download the exported data as a package.</span></span> <span data-ttu-id="074e0-147">Voit käyttää pakettia tietojen tuontiin kohde-esiintymiin testausta varten.</span><span class="sxs-lookup"><span data-stu-id="074e0-147">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="074e0-148">Yritys määrittäminen laskua varten</span><span class="sxs-lookup"><span data-stu-id="074e0-148">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="074e0-149">Tietopakettien kautta tuodut laskut voidaan liittää ne omistaviin yrityksiin kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="074e0-149">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="074e0-150">Laskuja käsittelevä tuontityö tuo sen samaan yritykseen, jossa työ oli ajoitettu **Tietojen hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="074e0-150">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="074e0-151">Toisin sanoen työn yritys määrittää yrityksen, jolle lasku kuuluu.</span><span class="sxs-lookup"><span data-stu-id="074e0-151">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="074e0-152">Jos laskuja sisältävä tietopaketti lähetetään Financeen, kutsuja (toisin sanoen integrointisovellus, joka suoritetaan Financen ulkopuolella) voi erikseen mainita yritystunnuksen HTTP-pyynnössä.</span><span class="sxs-lookup"><span data-stu-id="074e0-152">When the data package that contains invoices is sent to Finance, the caller (that is, the integration application that runs outside of Finance) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="074e0-153">Tässä tapauksessa yrityskonteksti, jossa käsittelytyö suoritetaan Financessa, sekä laskut tuodaan yritykseen, joka siirrettiin HTTP-pyynnön kautta.</span><span class="sxs-lookup"><span data-stu-id="074e0-153">In this case, the company context in which the processing job runs in Finance is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="074e0-154">Tämä on vakiotyyppinen tietojen hallintatoiminto.</span><span class="sxs-lookup"><span data-stu-id="074e0-154">This behavior is standard data management behavior.</span></span> <span data-ttu-id="074e0-155">Tämä on selitetty laskujen yhteydessä vain kattavuuden vuoksi.</span><span class="sxs-lookup"><span data-stu-id="074e0-155">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="074e0-156">Poikkeuksen käsittely</span><span class="sxs-lookup"><span data-stu-id="074e0-156">Exception processing</span></span>

<span data-ttu-id="074e0-157">Skenaarioissa, joissa toimittajalaskut tulevat Finance and Operationsiin integroinnin avulla, ostoreskontratiimin jäsenellä on oltava helppo tapa käsitellä poikkeuksia tai epäonnistuneita laskuja ja keino luoda odottavia laskuja epäonnistuneista laskuista.</span><span class="sxs-lookup"><span data-stu-id="074e0-157">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="074e0-158">Toimittajan laskujen poikkeusten käsittely on nyt osa Finance and Operationsia.</span><span class="sxs-lookup"><span data-stu-id="074e0-158">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="074e0-159">Poikkeusluettelo-sivu</span><span class="sxs-lookup"><span data-stu-id="074e0-159">Exceptions list page</span></span>

<span data-ttu-id="074e0-160">Uusi laskun poikkeusten luettelosivu on kohdassa **Ostoreskontra** > **Laskut** > **Epäonnistuneet tuonnit** > **Toimittajan laskut, joiden tuonti epäonnistui**.</span><span class="sxs-lookup"><span data-stu-id="074e0-160">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="074e0-161">Tällä sivulla näkyvät kaikki toimittajalaskujen otsikkotietueet Toimittajan laskun otsikko ‑tietoyksikön väliaikaisesta taulukosta.</span><span class="sxs-lookup"><span data-stu-id="074e0-161">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="074e0-162">Huomaa, että samaa tietueita voidaan tarkastella **Tietojen hallinta** -työtilasta, jossa voit myös suorittaa samat toiminnot, jotka ovat käytössä poikkeusten käsittelytoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="074e0-162">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="074e0-163">Poikkeuksien käsittelytoiminnon käyttöliittymä on kuitenkin optimoitu toimintokäyttäjää varten.</span><span class="sxs-lookup"><span data-stu-id="074e0-163">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![Poikkeusluettelo-sivu](media/vendor_invoice_automation_02.png)

<span data-ttu-id="074e0-165">Tämä luettelosivulta sisältää seuraavat kentät, jotka saadaan syötteen kautta:</span><span class="sxs-lookup"><span data-stu-id="074e0-165">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="074e0-166">**Yritys** – Yritys, joka omistaa laskun</span><span class="sxs-lookup"><span data-stu-id="074e0-166">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="074e0-167">**Virhesanoma** – Virhesanoma, jonka tiedonhallinta-sovelluskehys muodostaa selitykseksi, miksi laskua ei voitu luoda</span><span class="sxs-lookup"><span data-stu-id="074e0-167">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="074e0-168">**Numero** – Laskunumero</span><span class="sxs-lookup"><span data-stu-id="074e0-168">**Number** – The invoice number</span></span>
+ <span data-ttu-id="074e0-169">**Laskutusasiakasnumero**</span><span class="sxs-lookup"><span data-stu-id="074e0-169">**Invoice account**</span></span>
+ <span data-ttu-id="074e0-170">**Nimi** – Toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="074e0-170">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="074e0-171">**Toimittajanro**</span><span class="sxs-lookup"><span data-stu-id="074e0-171">**Vendor account**</span></span>
+ <span data-ttu-id="074e0-172">**Ostotilauksen numero** – Ostotilauksen numero laskuun</span><span class="sxs-lookup"><span data-stu-id="074e0-172">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="074e0-173">**Kirjauspäivä**</span><span class="sxs-lookup"><span data-stu-id="074e0-173">**Posting date**</span></span>
+ <span data-ttu-id="074e0-174">**Laskun päivämäärä**</span><span class="sxs-lookup"><span data-stu-id="074e0-174">**Invoice date**</span></span>
+ <span data-ttu-id="074e0-175">**Laskun kuvaus**</span><span class="sxs-lookup"><span data-stu-id="074e0-175">**Invoice description**</span></span>
+ <span data-ttu-id="074e0-176">**Valuutta**</span><span class="sxs-lookup"><span data-stu-id="074e0-176">**Currency**</span></span>
+ <span data-ttu-id="074e0-177">**Loki**</span><span class="sxs-lookup"><span data-stu-id="074e0-177">**Log**</span></span>
+ <span data-ttu-id="074e0-178">**Riviviite** – Tunnus, joka saadaan ulkoisesta järjestelmästä</span><span class="sxs-lookup"><span data-stu-id="074e0-178">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="074e0-179">Riviviite ei ole laskun tunnus.</span><span class="sxs-lookup"><span data-stu-id="074e0-179">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="074e0-180">Tällä luettelosivulta on myös esikatseluruutu, jota voit käyttää seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="074e0-180">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="074e0-181">Tarkastele koko virhesanomaa laajentamatta taulukon **Virhesanoma**-saraketta.</span><span class="sxs-lookup"><span data-stu-id="074e0-181">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="074e0-182">Tarkastele laskun koko liiteluetteloa, jos laskussa on liitteitä.</span><span class="sxs-lookup"><span data-stu-id="074e0-182">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="074e0-183">Luettelosivun tukee seuraavia toimia:</span><span class="sxs-lookup"><span data-stu-id="074e0-183">The list page supports the following actions:</span></span>

+ <span data-ttu-id="074e0-184">**Muokkaa** – Avaa poikkeustietue muokkaustilassa siten, että voit korjata ongelmia.</span><span class="sxs-lookup"><span data-stu-id="074e0-184">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="074e0-185">**Asetukset** – Luettelosivuilla käytettävissä olevien vakiovaihtoehtojen tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="074e0-185">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="074e0-186">Voit käyttää **Lisää työtilaan** -asetusta ja kiinnittää työtilaasi poikkeusluettelosivun luettelona tai ruutuna.</span><span class="sxs-lookup"><span data-stu-id="074e0-186">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="074e0-187">Poikkeustiedot-sivu</span><span class="sxs-lookup"><span data-stu-id="074e0-187">Exception details page</span></span>

<span data-ttu-id="074e0-188">Käynnistäessäsi muokkaustilan näyttöön tulee poikkeustiedot-sivu laskuista, joissa on ongelmia.</span><span class="sxs-lookup"><span data-stu-id="074e0-188">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="074e0-189">Jos liitteitä on paljon, lasku ja oletusliite näkyvät rinnakkain Poikkeustiedot-sivulla.</span><span class="sxs-lookup"><span data-stu-id="074e0-189">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![Poikkeustiedot-sivu](media/vendor_invoice_automation_03.png)

<span data-ttu-id="074e0-191">Edellisessä kuvassa ei toimittajan laskun otsikkoon tullut yhtään riviä.</span><span class="sxs-lookup"><span data-stu-id="074e0-191">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="074e0-192">Tämän vuoksi riviosa on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="074e0-192">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="074e0-193">Poikkeustiedot-sivu tukee seuraava toimintoa:</span><span class="sxs-lookup"><span data-stu-id="074e0-193">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="074e0-194">**Luo odottava lasku** – Kun laskun ongelmat on korjattu poikkeuskäsittelyn yhteydessä, voit luoda laskun valitsemalla tämän painikkeen.</span><span class="sxs-lookup"><span data-stu-id="074e0-194">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="074e0-195">Odottavien laskujen luominen tapahtuu taustalla (asynkronisena työvaiheena).</span><span class="sxs-lookup"><span data-stu-id="074e0-195">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="074e0-196">Jaettu palvelu vs. organisaatioperusteinen poikkeusten käsittely</span><span class="sxs-lookup"><span data-stu-id="074e0-196">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="074e0-197">Poikkeusluettelo-sivu tukee vakiotyyppisiä suojausrakenteita, joita **Tietojen hallinta** -työtila tukee väliaikaisten tiedostojen käsittelyssä.</span><span class="sxs-lookup"><span data-stu-id="074e0-197">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="074e0-198">Laskun tuontityö voidaan suojata seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="074e0-198">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="074e0-199">Käyttäjäroolikohtainen</span><span class="sxs-lookup"><span data-stu-id="074e0-199">By user role</span></span>
+ <span data-ttu-id="074e0-200">Käyttäjäkohtainen</span><span class="sxs-lookup"><span data-stu-id="074e0-200">By user</span></span>
+ <span data-ttu-id="074e0-201">Yrityskohtainen</span><span class="sxs-lookup"><span data-stu-id="074e0-201">By legal entity</span></span>

![Tuontityö, joka on suojattu käyttäjärooli- ja yrityskohtaisesti](media/vendor_invoice_automation_04.png)

<span data-ttu-id="074e0-203">Jos suojaus on konfiguroitu laskun tuontityötä varten, poikkeusluettelosivu noudattaa kyseisiä asetuksia.</span><span class="sxs-lookup"><span data-stu-id="074e0-203">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="074e0-204">Käyttäjät näkevät ainoastaan ne laskun poikkeustietueet, jotka tämä asetus sallii.</span><span class="sxs-lookup"><span data-stu-id="074e0-204">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="074e0-205">Esimerkiksi Contoso on päättänyt käsitellä laskun poikkeuksia yrityskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="074e0-205">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="074e0-206">Siksi suojaus on määritetty laskun tuontityölle siten, että yrityksen A käyttäjä näkee ainoastaan laskun poikkeukset yrityksessä A ja yrityksen B käyttäjä näkee ainoastaan laskun poikkeukset yrityksessä B. Tämä asetus mahdollistaa tehtävien eriyttämisen laskun poikkeusten hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="074e0-206">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="074e0-207">Contoso voi myös päättää ettei se pakota mitään suojausta, jotta samat käyttäjät voivat prosessoida laskun poikkeuksia kaikissa yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="074e0-207">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="074e0-208">Tämä asetus mahdollistaa jaetut palvelut -skenaarion laskun poikkeusten hallintaa varten.</span><span class="sxs-lookup"><span data-stu-id="074e0-208">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="074e0-209">Liitteiden rinnakkainen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="074e0-209">Side-by-side attachment viewer</span></span>

<span data-ttu-id="074e0-210">Seuraavilla sivuilla, joita käytetään laskutusprosessiin, on nyt liitteiden tarkastelutoiminto toimittajan laskujen helppoa tarkastelua varten:</span><span class="sxs-lookup"><span data-stu-id="074e0-210">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="074e0-211">**Poikkeusten käsittely**</span><span class="sxs-lookup"><span data-stu-id="074e0-211">**Exception handling**</span></span>
+ <span data-ttu-id="074e0-212">**Odottavat toimittajan laskut** -sivu (käytettävissä myös laskun tarkistusprosessissa)</span><span class="sxs-lookup"><span data-stu-id="074e0-212">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="074e0-213">**Laskukirjauskansio** -kyselysivu (kirjatuille laskuille)</span><span class="sxs-lookup"><span data-stu-id="074e0-213">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="074e0-214">Liitteen tarkastelutoiminnon päätoiminto:</span><span class="sxs-lookup"><span data-stu-id="074e0-214">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="074e0-215">Kaikkien liitetiedostotyyppien tarkastelu joita tiedostojen hallinta tukee (tiedostot, kuvat, URL-osoitteet ja huomautukset).</span><span class="sxs-lookup"><span data-stu-id="074e0-215">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="074e0-216">Monisivuisten TIFF-tiedojen tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="074e0-216">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="074e0-217">Suorita seuraavat toiminnot kuvatiedostoille:</span><span class="sxs-lookup"><span data-stu-id="074e0-217">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="074e0-218">Korosta kuvan osia.</span><span class="sxs-lookup"><span data-stu-id="074e0-218">Highlight parts of the image.</span></span>
  + <span data-ttu-id="074e0-219">Estä kuvan osia.</span><span class="sxs-lookup"><span data-stu-id="074e0-219">Block parts of the image.</span></span>
  + <span data-ttu-id="074e0-220">Lisää huomautuksia kuvaan.</span><span class="sxs-lookup"><span data-stu-id="074e0-220">Add annotations to the image.</span></span>
  + <span data-ttu-id="074e0-221">Suurenna ja pienennä kuvaa.</span><span class="sxs-lookup"><span data-stu-id="074e0-221">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="074e0-222">Panoroi kuvaa.</span><span class="sxs-lookup"><span data-stu-id="074e0-222">Pan the image.</span></span>
  + <span data-ttu-id="074e0-223">Peruuta toiminto ja tee se uudelleen.</span><span class="sxs-lookup"><span data-stu-id="074e0-223">Undo and redo actions.</span></span>
  + <span data-ttu-id="074e0-224">Sovita kuvan koko.</span><span class="sxs-lookup"><span data-stu-id="074e0-224">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="074e0-225">Nämä toiminnot ovat käytettävissä vain kuvatiedostoille (JPEG TIFF, PNG jne.).</span><span class="sxs-lookup"><span data-stu-id="074e0-225">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="074e0-226">Näillä toiminnoilla kuvaan tekemäsi muutokset tallennetaan kuvatiedostoon.</span><span class="sxs-lookup"><span data-stu-id="074e0-226">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="074e0-227">Tällä hetkellä liitteen tarkastelutoiminto ei sisällä versionhallinta- tai tarkistusominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="074e0-227">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="074e0-228">Oletusliite</span><span class="sxs-lookup"><span data-stu-id="074e0-228">Default attachment</span></span>

<span data-ttu-id="074e0-229">Jos toimittajalaskussa on useampia kuin yksi liite , voit määrittää yhden asiakirjan oletusliitteeksi **Liitteet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="074e0-229">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="074e0-230">**On oletusliite** -asetus on tämän toiminnon osaksi lisätty uusi asetus.</span><span class="sxs-lookup"><span data-stu-id="074e0-230">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="074e0-231">Tämä asetus on käytettävissä myös toimittajan laskujen asiakirjaliite -tietoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="074e0-231">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="074e0-232">Näin oletusliite voidaan määrittää integrointien avulla.</span><span class="sxs-lookup"><span data-stu-id="074e0-232">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="074e0-233">Ainoastaan yksi tiedosto voidaan määrittää oletusliitteeksi.</span><span class="sxs-lookup"><span data-stu-id="074e0-233">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="074e0-234">Määritettyäsi asiakirjan oletusliitteeksi se näytetään automaattisesti liitteen katseluohjelmassa laskun avaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="074e0-234">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="074e0-235">Jos et määritä mitään asiakirjaa oletusliitteeksi, liitteen katseluohjelma ei näytetä automaattisesti mitään liitettä laskun avaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="074e0-235">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="074e0-236">Näytä/piilota laskun liitteet</span><span class="sxs-lookup"><span data-stu-id="074e0-236">Show/hide invoice attachments</span></span>

<span data-ttu-id="074e0-237">Uudella painikkeella, joka on käytettävissä **Poikkeuksen käsittely**, **Odottava lasku** ja **Laskukirjauskansio** -kyselysivuilla, voit näyttää tai piilottaa liitteiden tarkastelutoiminnon.</span><span class="sxs-lookup"><span data-stu-id="074e0-237">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="074e0-238">Suojaus</span><span class="sxs-lookup"><span data-stu-id="074e0-238">Security</span></span>

<span data-ttu-id="074e0-239">Seuraavia liitteen katseluohjelman toimintoja ohjataan roolipohjaisen suojauksen kautta:</span><span class="sxs-lookup"><span data-stu-id="074e0-239">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="074e0-240">Korostus</span><span class="sxs-lookup"><span data-stu-id="074e0-240">Highlighting</span></span>
+ <span data-ttu-id="074e0-241">Esto</span><span class="sxs-lookup"><span data-stu-id="074e0-241">Block</span></span>
+ <span data-ttu-id="074e0-242">Huomautus</span><span class="sxs-lookup"><span data-stu-id="074e0-242">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="074e0-243">Odottavat toimittajan laskut -sivu</span><span class="sxs-lookup"><span data-stu-id="074e0-243">Pending vendor invoices page</span></span>

<span data-ttu-id="074e0-244">Seuraavat oikeudet mahdollistavat vain luku -tyyppiset käyttöoikeudet tai luku-/kirjoitus-oikeudet liitteen katseluohjelmassa korostamis-, esto- ja huomautustoiminnoille:</span><span class="sxs-lookup"><span data-stu-id="074e0-244">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="074e0-245">**Ylläpidä toimittajan laskun kuvan** – Tämä oikeus antaa luku-/kirjoitusoikeudet.</span><span class="sxs-lookup"><span data-stu-id="074e0-245">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="074e0-246">**Näytä toimittajan laskun kuva** – Tämä oikeus antaa vain luku -oikeudet.</span><span class="sxs-lookup"><span data-stu-id="074e0-246">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="074e0-247">Seuraavat tehtävät antavat vain luku -oikeudet tai luku-/kirjoitusoikeudet liitteen katseluohjelmalle näissä toiminnoissa:</span><span class="sxs-lookup"><span data-stu-id="074e0-247">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="074e0-248">**Toimittajan laskujen ylläpito** : Toimittajan laskujen kuvan ylläpito-oikeus on annettu tälle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="074e0-248">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="074e0-249">**Kohdista kyselyjä toimittajan laskujen tilaan** : Toimittajan laskujen kuvan tarkasteluoikeus on annettu tälle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="074e0-249">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="074e0-250">Seuraavat roolit antavat vain luku -oikeudet tai luku-/kirjoitusoikeudet liitteen katseluohjelmalle näissä toiminnoissa:</span><span class="sxs-lookup"><span data-stu-id="074e0-250">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="074e0-251">**Ostoreskontra-assistentti** ja **Ostoreskontrapäällikkö**: Toimittajan laskujen ylläpito -tehtävä on annettu näille rooleille.</span><span class="sxs-lookup"><span data-stu-id="074e0-251">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="074e0-252">**Ostoreskontra-assistentti**, **Ostoreskontrapäällikkö**, **Ostoreskontran keskitetty maksuliikenneassistentti** ja **Ostoreskontran maksuliikenneassistentti**: Kohdista kyselyjä toimittajan laskujen tilaan -velvollisuus on liitetty näihin rooleihin.</span><span class="sxs-lookup"><span data-stu-id="074e0-252">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="074e0-253">Laskun poikkeustiedot -sivu</span><span class="sxs-lookup"><span data-stu-id="074e0-253">Invoice exception details page</span></span>

<span data-ttu-id="074e0-254">Seuraavat oikeudet mahdollistavat vain luku -tyyppiset käyttöoikeudet tai luku-/kirjoitus-oikeudet liitteen katseluohjelmassa korostamis-, esto- ja huomautustoiminnoille.</span><span class="sxs-lookup"><span data-stu-id="074e0-254">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="074e0-255">Valmiiksi määritetyillä rooleilla, jotka mainitaan tässä osassa, on vain luku -oikeudet laskun kuviin liitteen katseluohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="074e0-255">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="074e0-256">Jos roolilla pitää olla myös kirjoitusoikeus kuviin, jos annat kirjoitusoikeudet kyseiselle roolille käyttämällä oikeuksia ja velvollisuuksia, jotka on kuvattu tässä.</span><span class="sxs-lookup"><span data-stu-id="074e0-256">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="074e0-257">**Ylläpidä toimittajan laskun otsikon yksikön kuvaa**: Oikeus sisältää luku-/kirjoitusoikeudet laskun kuviin liitteen katseluohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="074e0-257">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="074e0-258">**Tarkastele toimittajan laskun otsikon yksikön kuvaa**: Oikeus sisältää vain luku -oikeudet laskun kuvaan liitteen katseluohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="074e0-258">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="074e0-259">Seuraavat tehtävät antavat vain luku -oikeudet liitteen katseluohjelmalle näissä toiminnoissa:</span><span class="sxs-lookup"><span data-stu-id="074e0-259">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="074e0-260">**Toimittajan laskujen ylläpito** : Toimittajan laskujen otsikko -yksikön kuvan ylläpito-oikeus on annettu tälle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="074e0-260">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="074e0-261">Seuraavat roolit antavat vain luku -oikeudet liitteen katseluohjelmalle näissä toiminnoissa:</span><span class="sxs-lookup"><span data-stu-id="074e0-261">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="074e0-262">**Ostoreskontra-assistentti** ja **Ostoreskontrapäällikkö**: Toimittajan laskujen ylläpito -tehtävä on annettu näille rooleille.</span><span class="sxs-lookup"><span data-stu-id="074e0-262">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="074e0-263">Oletusarvoisesti jos käyttäjärooli antaa muokkausoikeudet mille tahansa sivulle, käyttäjällä on myös muokkausoikeudet liitteen katseluohjelmassa korostus-, esto- ja huomautustoimintojen osalta.</span><span class="sxs-lookup"><span data-stu-id="074e0-263">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="074e0-264">Jos kuitenkin esiintyy skenaarioita, joissa tietyllä roolilla on oltava muokkausoikeudet sivulla mutta ei liitteen katseluohjelmassa, voidaan käyttää edellä olevassa luettelossa esitettyjä ja käyttötapaukseen soveltuvia oikeuksia.</span><span class="sxs-lookup"><span data-stu-id="074e0-264">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>
