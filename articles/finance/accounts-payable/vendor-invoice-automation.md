---
title: Toimittajan laskuautomaatio
description: Tässä ohjeaiheessa kerrotaan ominaisuuksista, joita voidaan käyttää toimittajalaskujen päästä päähän -automatisointiin. Tämä koskee myös laskuja, jotka sisältävät liitteitä.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
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
ms.openlocfilehash: ba986afb5c17c7a317b47d1e9cf4ae57ac29da97
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177595"
---
# <a name="vendor-invoice-automation"></a><span data-ttu-id="a2d5d-103">Toimittajan laskuautomaatio</span><span class="sxs-lookup"><span data-stu-id="a2d5d-103">Vendor invoice automation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2d5d-104">Tässä ohjeaiheessa kerrotaan ominaisuuksista, joita voidaan käyttää toimittajalaskujen päästä päähän -automatisointiin. Tämä koskee myös laskuja, jotka sisältävät liitteitä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="a2d5d-105">Organisaatiot, jotka haluavat helpottaa ostoreskontran prosessejaan, määrittelevät usein laskutusprosessin yhdeksi tärkeimmäksi tehostettavaksi prosessialueeksi.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="a2d5d-106">Usein nämä organisaatiot siirtävät paperilaskujen käsittelyn ulkoiselle optisten merkkien tunnistuksen (OCR) palveluntarjoajalle.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="a2d5d-107">Ne saavat koneellisesti luettavat laskun metatiedot ja jokaisen laskun skannatun kuvan.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="a2d5d-108">Automaation avuksi luodaan "viimeisen osuuden" ratkaisu, joka mahdollistaa näiden artefaktien käytön laskutusjärjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="a2d5d-109">Nyt tämä viimeisen osuuden automaatio on valmiiksi käytössä laskuautomaatioratkaisun avulla.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-109">Now this “last mile” automation is enabled out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="a2d5d-110">Ratkaisukonteksti</span><span class="sxs-lookup"><span data-stu-id="a2d5d-110">Solution context</span></span>

<span data-ttu-id="a2d5d-111">Laskuautomaatioratkaisu tuo käyttöön vakiokäyttöliittymän, joka sisällyttää laskun metatiedot laskun otsikkoon ja laskutusriveille sekä mahdolliset laskuliitteet.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="a2d5d-112">Mikä tahansa ulkoinen järjestelmä, joka voi luoda tämän käyttöliittymän kanssa yhteensopivia artefakteja, voi lähettää syötteen laskujen ja liitteiden automaattista käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="a2d5d-113">Seuraavassa kuvassa on esimerkkitilanne integroinnista, jossa Contoso on tehnyt yhteistyötä OCR-palveluntarjoajan kanssa toimittajan laskun käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="a2d5d-114">Contoson palveluntarjoajat lähettävät laskuja palveluntarjoajalle sähköpostitse.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="a2d5d-115">Palveluntarjoajan luo OCR-käsittelyn avulla laskun metatiedot (otsikon ja/tai rivit) ja skannatun kuvan laskusta.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="a2d5d-116">Integrointitaso muuntaa sitten nämä artefaktit yhteensopivaan muotoon.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-116">An integration layer then transforms these artifacts so that they can be consumed.</span></span>

![Esimerkkiskenaario integroinnista](media/vendor_invoice_automation_01.png)

<span data-ttu-id="a2d5d-118">Edellisestä skenaariosta on useita mahdollisia versioita, jos laskun integrointi on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="a2d5d-119">Toinen käyttöliittymän käyttötapa on tietojen siirtäminen laskujen ja liitteiden luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-119">Data migration is another use case where this interface can be used to create invoices and attachments.</span></span>

### <a name="solution-components"></a><span data-ttu-id="a2d5d-120">Ratkaisukomponentit</span><span class="sxs-lookup"><span data-stu-id="a2d5d-120">Solution components</span></span>

<span data-ttu-id="a2d5d-121">Seuraavat komponentit sisältyvät kattavaan ratkaisuun:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="a2d5d-122">Laskuotsikon, laskurivien ja laskun liitteiden tietoyksiköt</span><span class="sxs-lookup"><span data-stu-id="a2d5d-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="a2d5d-123">Laskujen poikkeusten käsittely</span><span class="sxs-lookup"><span data-stu-id="a2d5d-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="a2d5d-124">Laskujen liitteiden rinnakkainen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="a2d5d-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="a2d5d-125">Tämä aiheohje sisältää myös näiden ratkaisukomponenttien yksityiskohtaiset kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="a2d5d-126">Tietoyksiköt</span><span class="sxs-lookup"><span data-stu-id="a2d5d-126">Data entities</span></span>

<span data-ttu-id="a2d5d-127">Datapaketti on työyksikkö, joka on lähetettävä, jotta laskujen otsikot, laskurivit ja laskujen liitteet voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-127">A data package is the unit of work that must be sent so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="a2d5d-128">Seuraavia tietoyksiköitä käytetään datapaketin muodostavien artefaktien luomiseen:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="a2d5d-129">Toimittajan laskun otsikko</span><span class="sxs-lookup"><span data-stu-id="a2d5d-129">Vendor invoice header</span></span>
+ <span data-ttu-id="a2d5d-130">Toimittajan laskurivi</span><span class="sxs-lookup"><span data-stu-id="a2d5d-130">Vendor invoice line</span></span>
+ <span data-ttu-id="a2d5d-131">Toimittajan laskun asiakirjaliite</span><span class="sxs-lookup"><span data-stu-id="a2d5d-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="a2d5d-132">Toimittajan laskun asiakirjaliite on uusi toiminnon osana esiteltävä tietoyksikkö.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="a2d5d-133">Toimittajan laskun otsikkoa on muokattu siten, että se tukee liitteitä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="a2d5d-134">Toimittajan laskuriviyksikköä ei ole muutettu tämän toiminnon osalta.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="a2d5d-135">Tässä ohjeaiheessa ei anneta tarkkaa datapaketin määritystä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-135">This topic doesn’t give a detailed definition of a data package.</span></span> <span data-ttu-id="a2d5d-136">Tässä ei myöskään selitetä, miten datapaketit luodaan.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-136">It also doesn’t explain how to create data packages.</span></span> <span data-ttu-id="a2d5d-137">Lisätietoja on ohjeaiheessa [Tietoyksikköjen ja -pakettien kehikko](../../dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="a2d5d-137">For this information, see [Data entities and packages framework](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

<span data-ttu-id="a2d5d-138">Noudata näitä vaiheita, kun haluat luoda nopeasti testitietoja, jotka sisältävät laskuja ja -liitteitä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-138">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="a2d5d-139">Kirjaudu sisään esiintymääsi.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-139">Sign in to your instance.</span></span>
1. <span data-ttu-id="a2d5d-140">Valitse **Ostoreskontra** > **Laskut** > **Avoimet toimittajan laskut**.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-140">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="a2d5d-141">Luo laskuja, joissa on rivejä ja liitteitä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-141">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2d5d-142">Liitteiden on oltava otsikon liitteitä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-142">The attachments must be header attachments.</span></span> <span data-ttu-id="a2d5d-143">Toimittajan laskun asiakirjaliiteyksiköt eivät tue tällä hetkellä riviliitteitä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-143">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="a2d5d-144">Avaa **Tietojen hallinta** -työtila.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-144">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="a2d5d-145">Luo vientityö, joka sisältää toimittajan laskun otsikko-, toimittajan laskun rivi- ja toimittajan laskun asiakirjaliite -yksiköt.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-145">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="a2d5d-146">Vie tiedot.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-146">Export the data.</span></span>
1. <span data-ttu-id="a2d5d-147">Lataa viedyt tiedot pakettina.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-147">Download the exported data as a package.</span></span> <span data-ttu-id="a2d5d-148">Voit käyttää pakettia tietojen tuontiin kohde-esiintymiin testausta varten.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-148">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="a2d5d-149">Yritys määrittäminen laskua varten</span><span class="sxs-lookup"><span data-stu-id="a2d5d-149">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="a2d5d-150">Tietopakettien kautta tuodut laskut voidaan liittää ne omistaviin yrityksiin kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-150">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="a2d5d-151">Laskuja käsittelevä tuontityö tuo sen samaan yritykseen, jossa työ oli ajoitettu **Tietojen hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-151">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="a2d5d-152">Toisin sanoen työn yritys määrittää yrityksen, jolle lasku kuuluu.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-152">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="a2d5d-153">Jos laskuja sisältävä tietopaketti lähetetään Financeen, kutsuja (toisin sanoen integrointisovellus, joka suoritetaan Financen ulkopuolella) voi erikseen mainita yritystunnuksen HTTP-pyynnössä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-153">When the data package that contains invoices is sent to Finance, the caller (that is, the integration application that runs outside of Finance) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="a2d5d-154">Tässä tapauksessa yrityskonteksti, jossa käsittelytyö suoritetaan Financessa, sekä laskut tuodaan yritykseen, joka siirrettiin HTTP-pyynnön kautta.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-154">In this case, the company context in which the processing job runs in Finance is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="a2d5d-155">Tämä on vakiotyyppinen tietojen hallintatoiminto.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-155">This behavior is standard data management behavior.</span></span> <span data-ttu-id="a2d5d-156">Tämä on selitetty laskujen yhteydessä vain kattavuuden vuoksi.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-156">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="a2d5d-157">Poikkeuksen käsittely</span><span class="sxs-lookup"><span data-stu-id="a2d5d-157">Exception processing</span></span>

<span data-ttu-id="a2d5d-158">Skenaarioissa, joissa toimittajalaskut tulevat Finance and Operations -palveluun integroinnin kautta, ostoreskontratiimin jäsenellä on oltava helppo tapa käsitellä poikkeuksia tai epäonnistuneita laskuja ja keino luoda odottavia laskuja epäonnistuneista laskuista.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-158">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="a2d5d-159">Toimittajan laskujen poikkeusten käsittely on nyt osa Finance and Operations -palvelua.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-159">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="a2d5d-160">Poikkeusluettelo-sivu</span><span class="sxs-lookup"><span data-stu-id="a2d5d-160">Exceptions list page</span></span>

<span data-ttu-id="a2d5d-161">Uusi laskun poikkeusten luettelosivu on kohdassa **Ostoreskontra** > **Laskut** > **Epäonnistuneet tuonnit** > **Toimittajan laskut, joiden tuonti epäonnistui**.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-161">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="a2d5d-162">Tällä sivulla näkyvät kaikki toimittajalaskujen otsikkotietueet Toimittajan laskun otsikko ‑tietoyksikön väliaikaisesta taulukosta.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-162">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="a2d5d-163">Huomaa, että samaa tietueita voidaan tarkastella **Tietojen hallinta** -työtilasta, jossa voit myös suorittaa samat toiminnot, jotka ovat käytössä poikkeusten käsittelytoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-163">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="a2d5d-164">Poikkeuksien käsittelytoiminnon käyttöliittymä on kuitenkin optimoitu toimintokäyttäjää varten.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-164">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![Poikkeusluettelo-sivu](media/vendor_invoice_automation_02.png)

<span data-ttu-id="a2d5d-166">Tämä luettelosivulta sisältää seuraavat kentät, jotka saadaan syötteen kautta:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-166">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="a2d5d-167">**Yritys** – Yritys, joka omistaa laskun</span><span class="sxs-lookup"><span data-stu-id="a2d5d-167">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="a2d5d-168">**Virhesanoma** – Virhesanoma, jonka tiedonhallinta-sovelluskehys muodostaa selitykseksi, miksi laskua ei voitu luoda</span><span class="sxs-lookup"><span data-stu-id="a2d5d-168">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="a2d5d-169">**Numero** – Laskunumero</span><span class="sxs-lookup"><span data-stu-id="a2d5d-169">**Number** – The invoice number</span></span>
+ <span data-ttu-id="a2d5d-170">**Laskutusasiakasnumero**</span><span class="sxs-lookup"><span data-stu-id="a2d5d-170">**Invoice account**</span></span>
+ <span data-ttu-id="a2d5d-171">**Nimi** – Toimittajan nimi</span><span class="sxs-lookup"><span data-stu-id="a2d5d-171">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="a2d5d-172">**Toimittajanro**</span><span class="sxs-lookup"><span data-stu-id="a2d5d-172">**Vendor account**</span></span>
+ <span data-ttu-id="a2d5d-173">**Ostotilauksen numero** – Ostotilauksen numero laskuun</span><span class="sxs-lookup"><span data-stu-id="a2d5d-173">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="a2d5d-174">**Kirjauspäivä**</span><span class="sxs-lookup"><span data-stu-id="a2d5d-174">**Posting date**</span></span>
+ <span data-ttu-id="a2d5d-175">**Laskun päivämäärä**</span><span class="sxs-lookup"><span data-stu-id="a2d5d-175">**Invoice date**</span></span>
+ <span data-ttu-id="a2d5d-176">**Laskun kuvaus**</span><span class="sxs-lookup"><span data-stu-id="a2d5d-176">**Invoice description**</span></span>
+ <span data-ttu-id="a2d5d-177">**Valuutta**</span><span class="sxs-lookup"><span data-stu-id="a2d5d-177">**Currency**</span></span>
+ <span data-ttu-id="a2d5d-178">**Loki**</span><span class="sxs-lookup"><span data-stu-id="a2d5d-178">**Log**</span></span>
+ <span data-ttu-id="a2d5d-179">**Riviviite** – Tunnus, joka saadaan ulkoisesta järjestelmästä</span><span class="sxs-lookup"><span data-stu-id="a2d5d-179">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2d5d-180">Riviviite ei ole laskun tunnus.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-180">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="a2d5d-181">Tällä luettelosivulta on myös esikatseluruutu, jota voit käyttää seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-181">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="a2d5d-182">Tarkastele koko virhesanomaa laajentamatta taulukon **Virhesanoma**-saraketta.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-182">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="a2d5d-183">Tarkastele laskun koko liiteluetteloa, jos laskussa on liitteitä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-183">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="a2d5d-184">Luettelosivun tukee seuraavia toimia:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-184">The list page supports the following actions:</span></span>

+ <span data-ttu-id="a2d5d-185">**Muokkaa** – Avaa poikkeustietue muokkaustilassa siten, että voit korjata ongelmia.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-185">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="a2d5d-186">**Asetukset** – Luettelosivuilla käytettävissä olevien vakiovaihtoehtojen tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-186">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="a2d5d-187">Voit käyttää **Lisää työtilaan** -asetusta ja kiinnittää työtilaasi poikkeusluettelosivun luettelona tai ruutuna.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-187">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="a2d5d-188">Poikkeustiedot-sivu</span><span class="sxs-lookup"><span data-stu-id="a2d5d-188">Exception details page</span></span>

<span data-ttu-id="a2d5d-189">Käynnistäessäsi muokkaustilan näyttöön tulee poikkeustiedot-sivu laskuista, joissa on ongelmia.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-189">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="a2d5d-190">Jos liitteitä on paljon, lasku ja oletusliite näkyvät rinnakkain Poikkeustiedot-sivulla.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-190">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![Poikkeustiedot-sivu](media/vendor_invoice_automation_03.png)

<span data-ttu-id="a2d5d-192">Edellisessä kuvassa ei toimittajan laskun otsikkoon tullut yhtään riviä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-192">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="a2d5d-193">Tämän vuoksi riviosa on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-193">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="a2d5d-194">Poikkeustiedot-sivu tukee seuraava toimintoa:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-194">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="a2d5d-195">**Luo odottava lasku** – Kun laskun ongelmat on korjattu poikkeuskäsittelyn yhteydessä, voit luoda laskun valitsemalla tämän painikkeen.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-195">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="a2d5d-196">Odottavien laskujen luominen tapahtuu taustalla (asynkronisena työvaiheena).</span><span class="sxs-lookup"><span data-stu-id="a2d5d-196">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="a2d5d-197">Jaettu palvelu vs. organisaatioperusteinen poikkeusten käsittely</span><span class="sxs-lookup"><span data-stu-id="a2d5d-197">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="a2d5d-198">Poikkeusluettelo-sivu tukee vakiotyyppisiä suojausrakenteita, joita **Tietojen hallinta** -työtila tukee väliaikaisten tiedostojen käsittelyssä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-198">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="a2d5d-199">Laskun tuontityö voidaan suojata seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-199">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="a2d5d-200">Käyttäjäroolikohtainen</span><span class="sxs-lookup"><span data-stu-id="a2d5d-200">By user role</span></span>
+ <span data-ttu-id="a2d5d-201">Käyttäjäkohtainen</span><span class="sxs-lookup"><span data-stu-id="a2d5d-201">By user</span></span>
+ <span data-ttu-id="a2d5d-202">Yrityskohtainen</span><span class="sxs-lookup"><span data-stu-id="a2d5d-202">By legal entity</span></span>

![Tuontityö, joka on suojattu käyttäjärooli- ja yrityskohtaisesti](media/vendor_invoice_automation_04.png)

<span data-ttu-id="a2d5d-204">Jos suojaus on konfiguroitu laskun tuontityötä varten, poikkeusluettelosivu noudattaa kyseisiä asetuksia.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-204">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="a2d5d-205">Käyttäjät näkevät ainoastaan ne laskun poikkeustietueet, jotka tämä asetus sallii.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-205">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="a2d5d-206">Esimerkiksi Contoso on päättänyt käsitellä laskun poikkeuksia yrityskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-206">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="a2d5d-207">Siksi suojaus on määritetty laskun tuontityölle siten, että yrityksen A käyttäjä näkee ainoastaan laskun poikkeukset yrityksessä A ja yrityksen B käyttäjä näkee ainoastaan laskun poikkeukset yrityksessä B. Tämä asetus mahdollistaa tehtävien eriyttämisen laskun poikkeusten hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-207">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="a2d5d-208">Contoso voi myös päättää ettei se pakota mitään suojausta, jotta samat käyttäjät voivat prosessoida laskun poikkeuksia kaikissa yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-208">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="a2d5d-209">Tämä asetus mahdollistaa jaetut palvelut -skenaarion laskun poikkeusten hallintaa varten.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-209">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="a2d5d-210">Liitteiden rinnakkainen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="a2d5d-210">Side-by-side attachment viewer</span></span>

<span data-ttu-id="a2d5d-211">Seuraavilla sivuilla, joita käytetään laskutusprosessiin, on nyt liitteiden tarkastelutoiminto toimittajan laskujen helppoa tarkastelua varten:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-211">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="a2d5d-212">**Poikkeusten käsittely**</span><span class="sxs-lookup"><span data-stu-id="a2d5d-212">**Exception handling**</span></span>
+ <span data-ttu-id="a2d5d-213">**Odottavat toimittajan laskut** -sivu (käytettävissä myös laskun tarkistusprosessissa)</span><span class="sxs-lookup"><span data-stu-id="a2d5d-213">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="a2d5d-214">**Laskukirjauskansio** -kyselysivu (kirjatuille laskuille)</span><span class="sxs-lookup"><span data-stu-id="a2d5d-214">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="a2d5d-215">Liitteen tarkastelutoiminnon päätoiminto:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-215">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="a2d5d-216">Kaikkien liitetiedostotyyppien tarkastelu joita tiedostojen hallinta tukee (tiedostot, kuvat, URL-osoitteet ja huomautukset).</span><span class="sxs-lookup"><span data-stu-id="a2d5d-216">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="a2d5d-217">Monisivuisten TIFF-tiedojen tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-217">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="a2d5d-218">Suorita seuraavat toiminnot kuvatiedostoille:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-218">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="a2d5d-219">Korosta kuvan osia.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-219">Highlight parts of the image.</span></span>
  + <span data-ttu-id="a2d5d-220">Estä kuvan osia.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-220">Block parts of the image.</span></span>
  + <span data-ttu-id="a2d5d-221">Lisää huomautuksia kuvaan.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-221">Add annotations to the image.</span></span>
  + <span data-ttu-id="a2d5d-222">Suurenna ja pienennä kuvaa.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-222">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="a2d5d-223">Panoroi kuvaa.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-223">Pan the image.</span></span>
  + <span data-ttu-id="a2d5d-224">Peruuta toiminto ja tee se uudelleen.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-224">Undo and redo actions.</span></span>
  + <span data-ttu-id="a2d5d-225">Sovita kuvan koko.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-225">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="a2d5d-226">Nämä toiminnot ovat käytettävissä vain kuvatiedostoille (JPEG TIFF, PNG jne.).</span><span class="sxs-lookup"><span data-stu-id="a2d5d-226">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="a2d5d-227">Näillä toiminnoilla kuvaan tekemäsi muutokset tallennetaan kuvatiedostoon.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-227">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="a2d5d-228">Tällä hetkellä liitteen tarkastelutoiminto ei sisällä versionhallinta- tai tarkistusominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-228">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="a2d5d-229">Oletusliite</span><span class="sxs-lookup"><span data-stu-id="a2d5d-229">Default attachment</span></span>

<span data-ttu-id="a2d5d-230">Jos toimittajalaskussa on useampia kuin yksi liite , voit määrittää yhden asiakirjan oletusliitteeksi **Liitteet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-230">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="a2d5d-231">**On oletusliite** -asetus on tämän toiminnon osaksi lisätty uusi asetus.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-231">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="a2d5d-232">Tämä asetus on käytettävissä myös toimittajan laskujen asiakirjaliite -tietoyksikössä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-232">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="a2d5d-233">Näin oletusliite voidaan määrittää integrointien avulla.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-233">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="a2d5d-234">Ainoastaan yksi tiedosto voidaan määrittää oletusliitteeksi.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-234">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="a2d5d-235">Määritettyäsi asiakirjan oletusliitteeksi se näytetään automaattisesti liitteen katseluohjelmassa laskun avaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-235">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="a2d5d-236">Jos et määritä mitään asiakirjaa oletusliitteeksi, liitteen katseluohjelma ei näytetä automaattisesti mitään liitettä laskun avaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-236">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="a2d5d-237">Näytä/piilota laskun liitteet</span><span class="sxs-lookup"><span data-stu-id="a2d5d-237">Show/hide invoice attachments</span></span>

<span data-ttu-id="a2d5d-238">Uudella painikkeella, joka on käytettävissä **Poikkeuksen käsittely**, **Odottava lasku** ja **Laskukirjauskansio** -kyselysivuilla, voit näyttää tai piilottaa liitteiden tarkastelutoiminnon.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-238">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="a2d5d-239">Suojaus</span><span class="sxs-lookup"><span data-stu-id="a2d5d-239">Security</span></span>

<span data-ttu-id="a2d5d-240">Seuraavia liitteen katseluohjelman toimintoja ohjataan roolipohjaisen suojauksen kautta:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-240">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="a2d5d-241">Korostus</span><span class="sxs-lookup"><span data-stu-id="a2d5d-241">Highlighting</span></span>
+ <span data-ttu-id="a2d5d-242">Esto</span><span class="sxs-lookup"><span data-stu-id="a2d5d-242">Block</span></span>
+ <span data-ttu-id="a2d5d-243">Huomautus</span><span class="sxs-lookup"><span data-stu-id="a2d5d-243">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="a2d5d-244">Odottavat toimittajan laskut -sivu</span><span class="sxs-lookup"><span data-stu-id="a2d5d-244">Pending vendor invoices page</span></span>

<span data-ttu-id="a2d5d-245">Seuraavat oikeudet mahdollistavat vain luku -tyyppiset käyttöoikeudet tai luku-/kirjoitus-oikeudet liitteen katseluohjelmassa korostamis-, esto- ja huomautustoiminnoille:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-245">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="a2d5d-246">**Ylläpidä toimittajan laskun kuvan** – Tämä oikeus antaa luku-/kirjoitusoikeudet.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-246">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="a2d5d-247">**Näytä toimittajan laskun kuva** – Tämä oikeus antaa vain luku -oikeudet.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-247">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="a2d5d-248">Seuraavat tehtävät antavat vain luku -oikeudet tai luku-/kirjoitusoikeudet liitteen katseluohjelmalle näissä toiminnoissa:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-248">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="a2d5d-249">**Toimittajan laskujen ylläpito** : Toimittajan laskujen kuvan ylläpito-oikeus on annettu tälle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-249">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="a2d5d-250">**Kohdista kyselyjä toimittajan laskujen tilaan** : Toimittajan laskujen kuvan tarkasteluoikeus on annettu tälle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-250">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="a2d5d-251">Seuraavat roolit antavat vain luku -oikeudet tai luku-/kirjoitusoikeudet liitteen katseluohjelmalle näissä toiminnoissa:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-251">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="a2d5d-252">**Ostoreskontra-assistentti** ja **Ostoreskontrapäällikkö**: Toimittajan laskujen ylläpito -tehtävä on annettu näille rooleille.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-252">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="a2d5d-253">**Ostoreskontra-assistentti**, **Ostoreskontrapäällikkö**, **Ostoreskontran keskitetty maksuliikenneassistentti** ja **Ostoreskontran maksuliikenneassistentti**: Kohdista kyselyjä toimittajan laskujen tilaan -velvollisuus on liitetty näihin rooleihin.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-253">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="a2d5d-254">Laskun poikkeustiedot -sivu</span><span class="sxs-lookup"><span data-stu-id="a2d5d-254">Invoice exception details page</span></span>

<span data-ttu-id="a2d5d-255">Seuraavat oikeudet mahdollistavat vain luku -tyyppiset käyttöoikeudet tai luku-/kirjoitus-oikeudet liitteen katseluohjelmassa korostamis-, esto- ja huomautustoiminnoille.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-255">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="a2d5d-256">Valmiiksi määritetyillä rooleilla, jotka mainitaan tässä osassa, on vain luku -oikeudet laskun kuviin liitteen katseluohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-256">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="a2d5d-257">Jos roolilla pitää olla myös kirjoitusoikeus kuviin, jos annat kirjoitusoikeudet kyseiselle roolille käyttämällä oikeuksia ja velvollisuuksia, jotka on kuvattu tässä.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-257">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="a2d5d-258">**Ylläpidä toimittajan laskun otsikon yksikön kuvaa**: Oikeus sisältää luku-/kirjoitusoikeudet laskun kuviin liitteen katseluohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-258">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="a2d5d-259">**Tarkastele toimittajan laskun otsikon yksikön kuvaa**: Oikeus sisältää vain luku -oikeudet laskun kuvaan liitteen katseluohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-259">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="a2d5d-260">Seuraavat tehtävät antavat vain luku -oikeudet liitteen katseluohjelmalle näissä toiminnoissa:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-260">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="a2d5d-261">**Toimittajan laskujen ylläpito** : Toimittajan laskujen otsikko -yksikön kuvan ylläpito-oikeus on annettu tälle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-261">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="a2d5d-262">Seuraavat roolit antavat vain luku -oikeudet liitteen katseluohjelmalle näissä toiminnoissa:</span><span class="sxs-lookup"><span data-stu-id="a2d5d-262">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="a2d5d-263">**Ostoreskontra-assistentti** ja **Ostoreskontrapäällikkö**: Toimittajan laskujen ylläpito -tehtävä on annettu näille rooleille.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-263">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="a2d5d-264">Oletusarvoisesti jos käyttäjärooli antaa muokkausoikeudet mille tahansa sivulle, käyttäjällä on myös muokkausoikeudet liitteen katseluohjelmassa korostus-, esto- ja huomautustoimintojen osalta.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-264">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="a2d5d-265">Jos kuitenkin esiintyy skenaarioita, joissa tietyllä roolilla on oltava muokkausoikeudet sivulla mutta ei liitteen katseluohjelmassa, voidaan käyttää edellä olevassa luettelossa esitettyjä ja käyttötapaukseen soveltuvia oikeuksia.</span><span class="sxs-lookup"><span data-stu-id="a2d5d-265">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>