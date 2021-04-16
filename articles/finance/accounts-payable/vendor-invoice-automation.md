---
title: Skannattujen asiakirjojen laskuautomaatio
description: Tässä ohjeaiheessa kerrotaan ominaisuuksista, joita voidaan käyttää toimittajalaskujen päästä päähän -automatisointiin. Tämä koskee myös laskuja, jotka sisältävät liitteitä.
author: abruer
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d776ad4eda623f55a69d81eefd0e88842d9da401
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841234"
---
# <a name="invoice-automation-for-scanned-documents"></a><span data-ttu-id="15205-103">Skannattujen tiedostojen laskujen automatisointi</span><span class="sxs-lookup"><span data-stu-id="15205-103">Invoice automation for scanned documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15205-104">Tässä ohjeaiheessa kerrotaan tietoyksiköistä, joita voidaan käyttää toimittajalaskujen päästä päähän -automatisointiin. Tämä koskee myös laskuja, jotka sisältävät liitteitä.</span><span class="sxs-lookup"><span data-stu-id="15205-104">This topic explains the data entities that are available for end-to-end automation of vendor invoices, including invoices with attachments.</span></span>

<span data-ttu-id="15205-105">Organisaatiot, jotka haluavat helpottaa ostoreskontran prosessejaan, määrittelevät usein laskutusprosessin yhdeksi tärkeimmäksi tehostettavaksi prosessialueeksi.</span><span class="sxs-lookup"><span data-stu-id="15205-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="15205-106">Usein nämä organisaatiot siirtävät paperilaskujen käsittelyn ulkoiselle optisten merkkien tunnistuksen (OCR) palveluntarjoajalle.</span><span class="sxs-lookup"><span data-stu-id="15205-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="15205-107">Ne saavat koneellisesti luettavat laskun metatiedot ja jokaisen laskun skannatun kuvan.</span><span class="sxs-lookup"><span data-stu-id="15205-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="15205-108">Automaation avuksi luodaan "viimeisen osuuden" ratkaisu, joka mahdollistaa näiden artefaktien käytön laskutusjärjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="15205-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="15205-109">Nyt tämä viimeisen osuuden automaatio on valmiiksi käytössä laskuautomaatioratkaisun avulla.</span><span class="sxs-lookup"><span data-stu-id="15205-109">Now this “last mile” automation is enabled out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="15205-110">Ratkaisukonteksti</span><span class="sxs-lookup"><span data-stu-id="15205-110">Solution context</span></span>

<span data-ttu-id="15205-111">Laskuautomaatioratkaisu tuo käyttöön vakiokäyttöliittymän, joka sisällyttää laskun metatiedot laskun otsikkoon ja laskutusriveille sekä mahdolliset laskuliitteet.</span><span class="sxs-lookup"><span data-stu-id="15205-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="15205-112">Mikä tahansa ulkoinen järjestelmä, joka voi luoda tämän käyttöliittymän kanssa yhteensopivia artefakteja, voi lähettää syötteen laskujen ja liitteiden automaattista käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="15205-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="15205-113">Seuraavassa kuvassa on esimerkkitilanne integroinnista, jossa Contoso on tehnyt yhteistyötä OCR-palveluntarjoajan kanssa toimittajan laskun käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="15205-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="15205-114">Contoson palveluntarjoajat lähettävät laskuja palveluntarjoajalle sähköpostitse.</span><span class="sxs-lookup"><span data-stu-id="15205-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="15205-115">Palveluntarjoajan luo OCR-käsittelyn avulla laskun metatiedot (otsikon ja/tai rivit) ja skannatun kuvan laskusta.</span><span class="sxs-lookup"><span data-stu-id="15205-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="15205-116">Integrointitaso muuntaa sitten nämä artefaktit yhteensopivaan muotoon.</span><span class="sxs-lookup"><span data-stu-id="15205-116">An integration layer then transforms these artifacts so that they can be consumed.</span></span>

![Esimerkkiskenaario integroinnista](media/vendor_invoice_automation_01.png)

<span data-ttu-id="15205-118">Edellisestä skenaariosta on useita mahdollisia versioita, jos laskun integrointi on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="15205-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="15205-119">Toinen käyttöliittymän käyttötapa on tietojen siirtäminen laskujen ja liitteiden luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="15205-119">Data migration is another use case where this interface can be used to create invoices and attachments.</span></span>

### <a name="solution-components"></a><span data-ttu-id="15205-120">Ratkaisukomponentit</span><span class="sxs-lookup"><span data-stu-id="15205-120">Solution components</span></span>

<span data-ttu-id="15205-121">Seuraavat komponentit sisältyvät kattavaan ratkaisuun:</span><span class="sxs-lookup"><span data-stu-id="15205-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="15205-122">Laskuotsikon, laskurivien ja laskun liitteiden tietoyksiköt</span><span class="sxs-lookup"><span data-stu-id="15205-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="15205-123">Laskujen poikkeusten käsittely</span><span class="sxs-lookup"><span data-stu-id="15205-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="15205-124">Laskujen liitteiden rinnakkainen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="15205-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="15205-125">Tämä aiheohje sisältää myös näiden ratkaisukomponenttien yksityiskohtaiset kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="15205-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="15205-126">Tietoyksiköt</span><span class="sxs-lookup"><span data-stu-id="15205-126">Data entities</span></span>

<span data-ttu-id="15205-127">Datapaketti on työyksikkö, joka on lähetettävä, jotta laskujen otsikot, laskurivit ja laskujen liitteet voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="15205-127">A data package is the unit of work that must be sent so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="15205-128">Seuraavia tietoyksiköitä käytetään datapaketin muodostavien artefaktien luomiseen:</span><span class="sxs-lookup"><span data-stu-id="15205-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="15205-129">Toimittajan laskun otsikko</span><span class="sxs-lookup"><span data-stu-id="15205-129">Vendor invoice header</span></span>
+ <span data-ttu-id="15205-130">Toimittajan laskurivi</span><span class="sxs-lookup"><span data-stu-id="15205-130">Vendor invoice line</span></span>
+ <span data-ttu-id="15205-131">Toimittajan laskun asiakirjaliite</span><span class="sxs-lookup"><span data-stu-id="15205-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="15205-132">Toimittajan laskun asiakirjaliite on uusi toiminnon osana esiteltävä tietoyksikkö.</span><span class="sxs-lookup"><span data-stu-id="15205-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="15205-133">Toimittajan laskun otsikkoa on muokattu siten, että se tukee liitteitä.</span><span class="sxs-lookup"><span data-stu-id="15205-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="15205-134">Toimittajan laskuriviyksikköä ei ole muutettu tämän toiminnon osalta.</span><span class="sxs-lookup"><span data-stu-id="15205-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="15205-135">Lisätietoja tietopaketeista on kohdassa [Tietojen hallinnan yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="15205-135">For detailed information about data packages, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span> <span data-ttu-id="15205-136">Lisätietoja tietopakettien luonnista tietojen hallinnan työtilassa on kohdassa [Tietopakettien käsittely ja kuluttaminen Dynamics 365 Finance and Operations -sovellusratkaisussa](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="15205-136">For information about how to create data packages using the data management workspace, see [Process and consume data packages in Dynamics 365 Finance and Operations apps solution](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span></span>

<span data-ttu-id="15205-137">Noudata näitä vaiheita, kun haluat luoda nopeasti testitietoja, jotka sisältävät laskuja ja -liitteitä.</span><span class="sxs-lookup"><span data-stu-id="15205-137">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="15205-138">Kirjaudu sisään esiintymääsi.</span><span class="sxs-lookup"><span data-stu-id="15205-138">Sign in to your instance.</span></span>
1. <span data-ttu-id="15205-139">Valitse **Ostoreskontra** > **Laskut** > **Avoimet toimittajan laskut**.</span><span class="sxs-lookup"><span data-stu-id="15205-139">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="15205-140">Luo laskuja, joissa on rivejä ja liitteitä.</span><span class="sxs-lookup"><span data-stu-id="15205-140">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="15205-141">Liitteiden on oltava otsikon liitteitä.</span><span class="sxs-lookup"><span data-stu-id="15205-141">The attachments must be header attachments.</span></span> <span data-ttu-id="15205-142">Toimittajan laskun asiakirjaliiteyksiköt eivät tue tällä hetkellä riviliitteitä.</span><span class="sxs-lookup"><span data-stu-id="15205-142">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="15205-143">Avaa **Tietojen hallinta** -työtila.</span><span class="sxs-lookup"><span data-stu-id="15205-143">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="15205-144">Luo vientityö, joka sisältää toimittajan laskun otsikko-, toimittajan laskun rivi- ja toimittajan laskun asiakirjaliite -yksiköt.</span><span class="sxs-lookup"><span data-stu-id="15205-144">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="15205-145">Vie tiedot.</span><span class="sxs-lookup"><span data-stu-id="15205-145">Export the data.</span></span>
1. <span data-ttu-id="15205-146">Lataa viedyt tiedot pakettina.</span><span class="sxs-lookup"><span data-stu-id="15205-146">Download the exported data as a package.</span></span> <span data-ttu-id="15205-147">Voit käyttää pakettia tietojen tuontiin kohde-esiintymiin testausta varten.</span><span class="sxs-lookup"><span data-stu-id="15205-147">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="15205-148">Yritys määrittäminen laskua varten</span><span class="sxs-lookup"><span data-stu-id="15205-148">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="15205-149">Tietopakettien kautta tuodut laskut voidaan liittää ne omistaviin yrityksiin kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="15205-149">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="15205-150">Laskuja käsittelevä tuontityö tuo sen samaan yritykseen, jossa työ oli ajoitettu **Tietojen hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="15205-150">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="15205-151">Toisin sanoen työn yritys määrittää yrityksen, jolle lasku kuuluu.</span><span class="sxs-lookup"><span data-stu-id="15205-151">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="15205-152">Jos laskuja sisältävä tietopaketti lähetetään Financeen, kutsuja (toisin sanoen integrointisovellus, joka suoritetaan Financen ulkopuolella) voi erikseen mainita yritystunnuksen HTTP-pyynnössä.</span><span class="sxs-lookup"><span data-stu-id="15205-152">When the data package that contains invoices is sent to Finance, the caller (that is, the integration application that runs outside of Finance) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="15205-153">Tässä tapauksessa yrityskonteksti, jossa käsittelytyö suoritetaan Financessa, sekä laskut tuodaan yritykseen, joka siirrettiin HTTP-pyynnön kautta.</span><span class="sxs-lookup"><span data-stu-id="15205-153">In this case, the company context in which the processing job runs in Finance is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="15205-154">Tämä on vakiotyyppinen tietojen hallintatoiminto.</span><span class="sxs-lookup"><span data-stu-id="15205-154">This behavior is standard data management behavior.</span></span> <span data-ttu-id="15205-155">Tämä on selitetty laskujen yhteydessä vain kattavuuden vuoksi.</span><span class="sxs-lookup"><span data-stu-id="15205-155">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="15205-156">Poikkeuksen käsittely</span><span class="sxs-lookup"><span data-stu-id="15205-156">Exception processing</span></span>

<span data-ttu-id="15205-157">Skenaarioissa, joissa toimittajalaskut tulevat Finance and Operationsiin integroinnin avulla, ostoreskontratiimin jäsenellä on oltava helppo tapa käsitellä poikkeuksia tai epäonnistuneita laskuja ja keino luoda odottavia laskuja epäonnistuneista laskuista.</span><span class="sxs-lookup"><span data-stu-id="15205-157">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="15205-158">Toimittajan laskujen poikkeusten käsittely on nyt osa Finance and Operationsia.</span><span class="sxs-lookup"><span data-stu-id="15205-158">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="vendor-invoices-that-failed-to-import-list-page"></a><span data-ttu-id="15205-159">Luettelosivulle tuonnissa epäonnistuneet toimittajan laskut</span><span class="sxs-lookup"><span data-stu-id="15205-159">Vendor invoices that failed to import list page</span></span>

<span data-ttu-id="15205-160">Uusi laskun poikkeusten luettelosivu on kohdassa **Ostoreskontra** > **Laskut** > **Epäonnistuneet tuonnit** > **Toimittajan laskut, joiden tuonti epäonnistui**.</span><span class="sxs-lookup"><span data-stu-id="15205-160">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="15205-161">Tällä sivulla näkyvät kaikki toimittajalaskujen otsikkotietueet Toimittajan laskun otsikko ‑tietoyksikön väliaikaisesta taulukosta.</span><span class="sxs-lookup"><span data-stu-id="15205-161">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="15205-162">Huomaa, että voit tarkastella samoja tietueita **Tietojen hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="15205-162">Note that you can view the same records from the **Data management** workspace.</span></span> <span data-ttu-id="15205-163">**Tietojen hallinta** -työtilassa voit myös suorittaa samat toiminnot, jotka ovat käytössä poikkeusten käsittelytoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="15205-163">You can also perform the same actions that are provided in the exception handling feature from the **Data management** workspace.</span></span> <span data-ttu-id="15205-164">Poikkeusten käsittelytoiminto on optimoitu toiminnalliselle käyttäjälle, mikä helpottaa käyttöä.</span><span class="sxs-lookup"><span data-stu-id="15205-164">The exception handling feature has been optimized for a functional user, which makes it easier to use.</span></span>

![Poikkeusluettelo-sivu](media/vendor_invoice_automation_02.png)

<span data-ttu-id="15205-166">Tämä luettelosivulta sisältää seuraavat kentät, jotka saadaan syötteen kautta:</span><span class="sxs-lookup"><span data-stu-id="15205-166">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="15205-167">**Yritys** – Yritys, joka omistaa laskun</span><span class="sxs-lookup"><span data-stu-id="15205-167">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="15205-168">**Virhesanoma** – Virhesanoma, jonka tiedonhallinta-sovelluskehys muodostaa selitykseksi, miksi laskua ei voitu luoda</span><span class="sxs-lookup"><span data-stu-id="15205-168">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="15205-169">**Numero** – Laskunumero</span><span class="sxs-lookup"><span data-stu-id="15205-169">**Number** – The invoice number</span></span>
+ <span data-ttu-id="15205-170">**Laskutusasiakasnumero**</span><span class="sxs-lookup"><span data-stu-id="15205-170">**Invoice account**</span></span>
+ <span data-ttu-id="15205-171">**Nimi** – Toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="15205-171">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="15205-172">**Toimittajanro**</span><span class="sxs-lookup"><span data-stu-id="15205-172">**Vendor account**</span></span>
+ <span data-ttu-id="15205-173">**Ostotilauksen numero** – Ostotilauksen numero laskuun</span><span class="sxs-lookup"><span data-stu-id="15205-173">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="15205-174">**Kirjauspäivä**</span><span class="sxs-lookup"><span data-stu-id="15205-174">**Posting date**</span></span>
+ <span data-ttu-id="15205-175">**Laskun päivämäärä**</span><span class="sxs-lookup"><span data-stu-id="15205-175">**Invoice date**</span></span>
+ <span data-ttu-id="15205-176">**Laskun kuvaus**</span><span class="sxs-lookup"><span data-stu-id="15205-176">**Invoice description**</span></span>
+ <span data-ttu-id="15205-177">**Valuutta**</span><span class="sxs-lookup"><span data-stu-id="15205-177">**Currency**</span></span>
+ <span data-ttu-id="15205-178">**Loki**</span><span class="sxs-lookup"><span data-stu-id="15205-178">**Log**</span></span>
+ <span data-ttu-id="15205-179">**Riviviite** – Tunnus, joka saadaan ulkoisesta järjestelmästä</span><span class="sxs-lookup"><span data-stu-id="15205-179">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="15205-180">Riviviite ei ole laskun tunnus.</span><span class="sxs-lookup"><span data-stu-id="15205-180">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="15205-181">Tällä luettelosivulta on myös esikatseluruutu, jota voit käyttää seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="15205-181">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="15205-182">Tarkastele koko virhesanomaa laajentamatta taulukon **Virhesanoma**-saraketta.</span><span class="sxs-lookup"><span data-stu-id="15205-182">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>

<span data-ttu-id="15205-183">Luettelosivun tukee seuraavia toimia:</span><span class="sxs-lookup"><span data-stu-id="15205-183">The list page supports the following actions:</span></span>

+ <span data-ttu-id="15205-184">**Muokkaa** – Avaa poikkeustietue muokkaustilassa siten, että voit korjata ongelmia.</span><span class="sxs-lookup"><span data-stu-id="15205-184">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="15205-185">**Asetukset** – Luettelosivuilla käytettävissä olevien vakiovaihtoehtojen tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="15205-185">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="15205-186">Voit käyttää **Lisää työtilaan** -asetusta ja kiinnittää työtilaasi poikkeusluettelosivun luettelona tai ruutuna.</span><span class="sxs-lookup"><span data-stu-id="15205-186">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="vendor-invoices-that-failed-to-import-details-page"></a><span data-ttu-id="15205-187">Tietosivulle tuonnissa epäonnistuneet toimittajan laskut</span><span class="sxs-lookup"><span data-stu-id="15205-187">Vendor invoices that failed to import details page</span></span>

<span data-ttu-id="15205-188">Kun aloitat muokkaustilan, avautuu **Tietosivulle tuonnissa epäonnistuneet toimittajan laskut** laskulle, jossa on ongelmia.</span><span class="sxs-lookup"><span data-stu-id="15205-188">When you start edit mode, the **Vendor invoices that failed to import details** page for the invoice that has issues will open.</span></span> <span data-ttu-id="15205-189">Jos liitteen sisältävässä laskussa on ongelmia, liite ei näy.</span><span class="sxs-lookup"><span data-stu-id="15205-189">If there are issues with an invoice that has an attachment, the attachment won't be displayed.</span></span> <span data-ttu-id="15205-190">Liite on liitettävä laskuun uudelleen.</span><span class="sxs-lookup"><span data-stu-id="15205-190">The attachment must be re-attached to the invoice.</span></span>

<span data-ttu-id="15205-191">Jos **Tietosivulle tuonnissa epäonnistuneet toimittajan laskut** -sivulla voit luoda odottavan laskun.</span><span class="sxs-lookup"><span data-stu-id="15205-191">The **Vendor invoices that failed to import details** page lets you create a pending invoice.</span></span> <span data-ttu-id="15205-192">Kun laskun ongelmat on korjattu poikkeuskäsittelyn yhteydessä, voit luoda odottavan laskun valitsemalla tämän **Luo odottava lasku** -painikkeen.</span><span class="sxs-lookup"><span data-stu-id="15205-192">After you’ve fixed the issues on an invoice as part of processing an exception, select the **Create pending invoice** button to create the pending invoice.</span></span> <span data-ttu-id="15205-193">Odottava lasku luodaan taustalle.</span><span class="sxs-lookup"><span data-stu-id="15205-193">The pending invoice will be created in the background.</span></span> 

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="15205-194">Jaettu palvelu vs. organisaatioperusteinen poikkeusten käsittely</span><span class="sxs-lookup"><span data-stu-id="15205-194">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="15205-195">Poikkeusluettelo-sivu tukee vakiotyyppisiä suojausrakenteita, joita **Tietojen hallinta** -työtila tukee väliaikaisten tiedostojen käsittelyssä.</span><span class="sxs-lookup"><span data-stu-id="15205-195">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="15205-196">Laskun tuontityö voidaan suojata seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="15205-196">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="15205-197">Käyttäjäroolikohtainen</span><span class="sxs-lookup"><span data-stu-id="15205-197">By user role</span></span>
+ <span data-ttu-id="15205-198">Käyttäjäkohtainen</span><span class="sxs-lookup"><span data-stu-id="15205-198">By user</span></span>
+ <span data-ttu-id="15205-199">Yrityskohtainen</span><span class="sxs-lookup"><span data-stu-id="15205-199">By legal entity</span></span>

![Tuontityö, joka on suojattu käyttäjärooli- ja yrityskohtaisesti](media/vendor_invoice_automation_04.png)

<span data-ttu-id="15205-201">Jos suojaus on konfiguroitu laskun tuontityötä varten, poikkeusluettelosivu noudattaa kyseisiä asetuksia.</span><span class="sxs-lookup"><span data-stu-id="15205-201">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="15205-202">Käyttäjät näkevät ainoastaan ne laskun poikkeustietueet, jotka tämä asetus sallii.</span><span class="sxs-lookup"><span data-stu-id="15205-202">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="15205-203">Esimerkiksi Contoso on päättänyt käsitellä laskun poikkeuksia yrityskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="15205-203">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="15205-204">Siksi suojaus on määritetty laskun tuontityölle siten, että yrityksen A käyttäjä näkee ainoastaan laskun poikkeukset yrityksessä A ja yrityksen B käyttäjä näkee ainoastaan laskun poikkeukset yrityksessä B. Tämä asetus mahdollistaa tehtävien eriyttämisen laskun poikkeusten hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="15205-204">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="15205-205">Contoso voi myös päättää ettei se pakota mitään suojausta, jotta samat käyttäjät voivat prosessoida laskun poikkeuksia kaikissa yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="15205-205">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="15205-206">Tämä asetus mahdollistaa jaetut palvelut -skenaarion laskun poikkeusten hallintaa varten.</span><span class="sxs-lookup"><span data-stu-id="15205-206">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="15205-207">Liitteiden rinnakkainen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="15205-207">Side-by-side attachment viewer</span></span>

<span data-ttu-id="15205-208">Seuraavilla sivuilla, joita käytetään laskutusprosessiin, on nyt liitteiden tarkastelutoiminto toimittajan laskujen helppoa tarkastelua varten:</span><span class="sxs-lookup"><span data-stu-id="15205-208">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="15205-209">**Poikkeusten käsittely**</span><span class="sxs-lookup"><span data-stu-id="15205-209">**Exception handling**</span></span>
+ <span data-ttu-id="15205-210">**Odottavat toimittajan laskut** -sivu (käytettävissä myös laskun tarkistusprosessissa)</span><span class="sxs-lookup"><span data-stu-id="15205-210">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="15205-211">**Laskukirjauskansio** -kyselysivu (kirjatuille laskuille)</span><span class="sxs-lookup"><span data-stu-id="15205-211">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="15205-212">Liitteen tarkastelutoiminnon päätoiminto:</span><span class="sxs-lookup"><span data-stu-id="15205-212">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="15205-213">Kaikkien liitetiedostotyyppien tarkastelu joita tiedostojen hallinta tukee (tiedostot, kuvat, URL-osoitteet ja huomautukset).</span><span class="sxs-lookup"><span data-stu-id="15205-213">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="15205-214">Monisivuisten TIFF-tiedojen tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="15205-214">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="15205-215">Suorita seuraavat toiminnot kuvatiedostoille:</span><span class="sxs-lookup"><span data-stu-id="15205-215">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="15205-216">Korosta kuvan osia.</span><span class="sxs-lookup"><span data-stu-id="15205-216">Highlight parts of the image.</span></span>
  + <span data-ttu-id="15205-217">Estä kuvan osia.</span><span class="sxs-lookup"><span data-stu-id="15205-217">Block parts of the image.</span></span>
  + <span data-ttu-id="15205-218">Lisää huomautuksia kuvaan.</span><span class="sxs-lookup"><span data-stu-id="15205-218">Add annotations to the image.</span></span>
  + <span data-ttu-id="15205-219">Suurenna ja pienennä kuvaa.</span><span class="sxs-lookup"><span data-stu-id="15205-219">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="15205-220">Panoroi kuvaa.</span><span class="sxs-lookup"><span data-stu-id="15205-220">Pan the image.</span></span>
  + <span data-ttu-id="15205-221">Peruuta toiminto ja tee se uudelleen.</span><span class="sxs-lookup"><span data-stu-id="15205-221">Undo and redo actions.</span></span>
  + <span data-ttu-id="15205-222">Sovita kuvan koko.</span><span class="sxs-lookup"><span data-stu-id="15205-222">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="15205-223">Nämä toiminnot ovat käytettävissä vain kuvatiedostoille (JPEG TIFF, PNG jne.).</span><span class="sxs-lookup"><span data-stu-id="15205-223">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="15205-224">Näillä toiminnoilla kuvaan tekemäsi muutokset tallennetaan kuvatiedostoon.</span><span class="sxs-lookup"><span data-stu-id="15205-224">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="15205-225">Tällä hetkellä liitteen tarkastelutoiminto ei sisällä versionhallinta- tai tarkistusominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="15205-225">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="15205-226">Oletusliite</span><span class="sxs-lookup"><span data-stu-id="15205-226">Default attachment</span></span>

<span data-ttu-id="15205-227">Jos toimittajalaskussa on useampia kuin yksi liite , voit määrittää yhden asiakirjan oletusliitteeksi **Liitteet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="15205-227">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="15205-228">**On oletusliite** -asetus on tämän toiminnon osaksi lisätty uusi asetus.</span><span class="sxs-lookup"><span data-stu-id="15205-228">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="15205-229">Tämä asetus on käytettävissä myös toimittajan laskujen asiakirjaliite -tietoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="15205-229">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="15205-230">Näin oletusliite voidaan määrittää integrointien avulla.</span><span class="sxs-lookup"><span data-stu-id="15205-230">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="15205-231">Ainoastaan yksi tiedosto voidaan määrittää oletusliitteeksi.</span><span class="sxs-lookup"><span data-stu-id="15205-231">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="15205-232">Määritettyäsi asiakirjan oletusliitteeksi se näytetään automaattisesti liitteen katseluohjelmassa laskun avaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="15205-232">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="15205-233">Jos et määritä mitään asiakirjaa oletusliitteeksi, liitteen katseluohjelma ei näytetä automaattisesti mitään liitettä laskun avaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="15205-233">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="15205-234">Näytä/piilota laskun liitteet</span><span class="sxs-lookup"><span data-stu-id="15205-234">Show/hide invoice attachments</span></span>

<span data-ttu-id="15205-235">Uudella painikkeella, joka on käytettävissä **Poikkeuksen käsittely**, **Odottava lasku** ja **Laskukirjauskansio** -kyselysivuilla, voit näyttää tai piilottaa liitteiden tarkastelutoiminnon.</span><span class="sxs-lookup"><span data-stu-id="15205-235">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

## <a name="security"></a><span data-ttu-id="15205-236">Suojaus</span><span class="sxs-lookup"><span data-stu-id="15205-236">Security</span></span>

<span data-ttu-id="15205-237">Seuraavia liitteen katseluohjelman toimintoja ohjataan roolipohjaisen suojauksen kautta:</span><span class="sxs-lookup"><span data-stu-id="15205-237">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="15205-238">Korostus</span><span class="sxs-lookup"><span data-stu-id="15205-238">Highlighting</span></span>
+ <span data-ttu-id="15205-239">Esto</span><span class="sxs-lookup"><span data-stu-id="15205-239">Block</span></span>
+ <span data-ttu-id="15205-240">Huomautus</span><span class="sxs-lookup"><span data-stu-id="15205-240">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="15205-241">Odottavat toimittajan laskut -sivu</span><span class="sxs-lookup"><span data-stu-id="15205-241">Pending vendor invoices page</span></span>

<span data-ttu-id="15205-242">Seuraavat oikeudet mahdollistavat vain luku -tyyppiset käyttöoikeudet tai luku-/kirjoitus-oikeudet liitteen katseluohjelmassa korostamis-, esto- ja huomautustoiminnoille:</span><span class="sxs-lookup"><span data-stu-id="15205-242">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="15205-243">**Ylläpidä toimittajan laskun kuvan** – Tämä oikeus antaa luku-/kirjoitusoikeudet.</span><span class="sxs-lookup"><span data-stu-id="15205-243">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="15205-244">**Näytä toimittajan laskun kuva** – Tämä oikeus antaa vain luku -oikeudet.</span><span class="sxs-lookup"><span data-stu-id="15205-244">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="15205-245">Seuraavat tehtävät antavat vain luku -oikeudet tai luku-/kirjoitusoikeudet liitteen katseluohjelmalle näissä toiminnoissa:</span><span class="sxs-lookup"><span data-stu-id="15205-245">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="15205-246">**Toimittajan laskujen ylläpito** : Toimittajan laskujen kuvan ylläpito-oikeus on annettu tälle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="15205-246">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="15205-247">**Kohdista kyselyjä toimittajan laskujen tilaan** : Toimittajan laskujen kuvan tarkasteluoikeus on annettu tälle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="15205-247">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="15205-248">Seuraavat roolit antavat vain luku -oikeudet tai luku-/kirjoitusoikeudet liitteen katseluohjelmalle näissä toiminnoissa:</span><span class="sxs-lookup"><span data-stu-id="15205-248">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="15205-249">**Ostoreskontra-assistentti** ja **Ostoreskontrapäällikkö**: Toimittajan laskujen ylläpito -tehtävä on annettu näille rooleille.</span><span class="sxs-lookup"><span data-stu-id="15205-249">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="15205-250">**Ostoreskontra-assistentti**, **Ostoreskontrapäällikkö**, **Ostoreskontran keskitetty maksuliikenneassistentti** ja **Ostoreskontran maksuliikenneassistentti**: Kohdista kyselyjä toimittajan laskujen tilaan -velvollisuus on liitetty näihin rooleihin.</span><span class="sxs-lookup"><span data-stu-id="15205-250">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="vendor-invoice-attachment"></a><span data-ttu-id="15205-251">Toimittajalaskun liite</span><span class="sxs-lookup"><span data-stu-id="15205-251">Vendor invoice attachment</span></span>

<span data-ttu-id="15205-252">Seuraavat oikeudet mahdollistavat vain luku -tyyppiset käyttöoikeudet tai luku-/kirjoitus-oikeudet liitteen katseluohjelmassa korostamis-, esto- ja huomautustoiminnoille.</span><span class="sxs-lookup"><span data-stu-id="15205-252">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="15205-253">Valmiiksi määritetyillä rooleilla, jotka mainitaan tässä osassa, on vain luku -oikeudet laskun kuviin liitteen katseluohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="15205-253">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="15205-254">Jos roolilla pitää olla myös kirjoitusoikeus kuviin, jos annat kirjoitusoikeudet kyseiselle roolille käyttämällä oikeuksia ja velvollisuuksia, jotka on kuvattu tässä.</span><span class="sxs-lookup"><span data-stu-id="15205-254">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="15205-255">**Ylläpidä toimittajan laskun otsikon yksikön kuvaa**: Oikeus sisältää luku-/kirjoitusoikeudet laskun kuviin liitteen katseluohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="15205-255">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="15205-256">**Tarkastele toimittajan laskun otsikon yksikön kuvaa**: Oikeus sisältää vain luku -oikeudet laskun kuvaan liitteen katseluohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="15205-256">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="15205-257">Seuraavat tehtävät antavat vain luku -oikeudet liitteen katseluohjelmalle näissä toiminnoissa:</span><span class="sxs-lookup"><span data-stu-id="15205-257">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="15205-258">**Toimittajan laskujen ylläpito** : Toimittajan laskujen otsikko -yksikön kuvan ylläpito-oikeus on annettu tälle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="15205-258">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="15205-259">Seuraavat roolit antavat vain luku -oikeudet liitteen katseluohjelmalle näissä toiminnoissa:</span><span class="sxs-lookup"><span data-stu-id="15205-259">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="15205-260">**Ostoreskontra-assistentti** ja **Ostoreskontrapäällikkö**: Toimittajan laskujen ylläpito -tehtävä on annettu näille rooleille.</span><span class="sxs-lookup"><span data-stu-id="15205-260">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="15205-261">Oletusarvoisesti jos käyttäjärooli antaa muokkausoikeudet mille tahansa sivulle, käyttäjällä on myös muokkausoikeudet liitteen katseluohjelmassa korostus-, esto- ja huomautustoimintojen osalta.</span><span class="sxs-lookup"><span data-stu-id="15205-261">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="15205-262">Jos kuitenkin esiintyy skenaarioita, joissa tietyllä roolilla on oltava muokkausoikeudet sivulla mutta ei liitteen katseluohjelmassa, voidaan käyttää edellä olevassa luettelossa esitettyjä ja käyttötapaukseen soveltuvia oikeuksia.</span><span class="sxs-lookup"><span data-stu-id="15205-262">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]