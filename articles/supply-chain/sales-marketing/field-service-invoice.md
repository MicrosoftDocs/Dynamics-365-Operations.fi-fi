---
title: Field Servicen sopimuslaskujen synkronointi Finance and Operationsin vapaatekstilaskuihin
description: Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Field Servicen sopimuslaskut synkronoidaan Microsoft Dynamics 365 for Finance and Operationsiin vapaatekstilaskuihin.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560160"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="06051-103">Field Servicen sopimuslaskujen synkronointi Finance and Operationsin vapaatekstilaskuihin</span><span class="sxs-lookup"><span data-stu-id="06051-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="06051-104">Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Field Servicen sopimuslaskut synkronoidaan Microsoft Dynamics 365 for Finance and Operationsiin vapaatekstilaskuihin.</span><span class="sxs-lookup"><span data-stu-id="06051-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="06051-105">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="06051-105">Templates and tasks</span></span>

<span data-ttu-id="06051-106">Field Servicen sopimuslaskut synkronoidaan Finance and Operationsin vapaatekstilaskuihin seuraavien mallien ja taustalla olevien tehtävien avulla.</span><span class="sxs-lookup"><span data-stu-id="06051-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="06051-107">**Mallin nimi Tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="06051-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="06051-108">Sopimuslaskut (Field Servicestä Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="06051-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="06051-109">**Tehtävien nimet tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="06051-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="06051-110">Laskun ylätunnisteet</span><span class="sxs-lookup"><span data-stu-id="06051-110">Invoice headers</span></span>
- <span data-ttu-id="06051-111">Laskurivit</span><span class="sxs-lookup"><span data-stu-id="06051-111">Invoice lines</span></span>

<span data-ttu-id="06051-112">Seuraavat synkronointi tarvitaan, ennen kuin sopimuslaskut voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="06051-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="06051-113">Tilit (Salesista Fin and Opsiin) – suora</span><span class="sxs-lookup"><span data-stu-id="06051-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="06051-114">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="06051-114">Entity set</span></span>

| <span data-ttu-id="06051-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="06051-115">Field Service</span></span>  | <span data-ttu-id="06051-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="06051-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="06051-117">laskut</span><span class="sxs-lookup"><span data-stu-id="06051-117">invoices</span></span>       | <span data-ttu-id="06051-118">CDS-asiakkaan vapaatekstilaskujen otsikot</span><span class="sxs-lookup"><span data-stu-id="06051-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="06051-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="06051-119">invoicedetails</span></span> | <span data-ttu-id="06051-120">CDS-asiakkaan vapaatekstilaskujen rivit</span><span class="sxs-lookup"><span data-stu-id="06051-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="06051-121">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="06051-121">Entity flow</span></span>

<span data-ttu-id="06051-122">Field Servicen sopimukset luodut laskut voidaan synkronoida Finance and Operationsiin Common Data Service (CDS) -palvelun tietojen integrointiprojektina.</span><span class="sxs-lookup"><span data-stu-id="06051-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="06051-123">Näiden laskujen päivitykset synkronoidaan Finance and Operationsin vapaatekstilaskuihin, jos vapaatekstilaskun kirjanpidollinen tila on **Käsittelyssä**.</span><span class="sxs-lookup"><span data-stu-id="06051-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="06051-124">Sen jälkeen kun vapaatekstilasku on kirjattu Finance and Operationsissa ja kirjanpidolliseksi tilaksi on päivitetty **Valmis**, päivityksiä ei voi enää synkronoida Field Servicestä.</span><span class="sxs-lookup"><span data-stu-id="06051-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="06051-125">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="06051-125">Field Service CRM solution</span></span>

<span data-ttu-id="06051-126">**Sisältää sopimuksesta peräisin olevia rivejä** -kenttä on lisätty **Lasku**-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="06051-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="06051-127">Tämän kentän avulla voi varmistaa, että vain sopimuksesta luodut laskut synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="06051-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="06051-128">Arvo on **tosi**, jos laskussa on vähintään yksi sopimuksesta peräisin oleva laskurivi.</span><span class="sxs-lookup"><span data-stu-id="06051-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="06051-129">**On peräisin sopimuksesta** -kenttä on lisätty **Laskurivi**-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="06051-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="06051-130">Tämän kentän avulla voi varmistaa, että vain sopimuksesta luodut laskurivit synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="06051-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="06051-131">Arvo on **tosi**, jos laskurivi on peräisin sopimuksesta.</span><span class="sxs-lookup"><span data-stu-id="06051-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="06051-132">**Laskun päivämäärä** on pakollinen kenttä Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="06051-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="06051-133">Tämän vuoksi kentässä on Field Service -arvo ennen synkronointia.</span><span class="sxs-lookup"><span data-stu-id="06051-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="06051-134">Seuraava logiikka lisättiin, jotta tämä vaatimus toteutuisi:</span><span class="sxs-lookup"><span data-stu-id="06051-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="06051-135">Jos **Laskun päivämäärä** -kenttä on tyhjä **Lasku**-yksikössä (eli siinä ei ole arvoa), siksi määritetään se kuluva päivä, jolloin sopimuksesta peräisin oleva laskurivi lisätään.</span><span class="sxs-lookup"><span data-stu-id="06051-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="06051-136">Käyttäjä voi muuttaa **Laskun päivämäärä** -kenttää.</span><span class="sxs-lookup"><span data-stu-id="06051-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="06051-137">Kun käyttäjä kuitenkin yrittää tallentaa sopimuksesta peräisin olevan laskun, hänen vastaanottaa liiketoimintaprosessin virheen, jos laskun **Laskun päivämäärä** -kenttä on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="06051-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="06051-138">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="06051-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="06051-139">Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="06051-139">In Finance and Operations</span></span>

<span data-ttu-id="06051-140">Laskun alkuperä on määritettävä integraatiota varten, jotta Finance and Operationsin Field Servicen sopimuslaskuista luodut vapaatekstilaskut voidaan erottaa.</span><span class="sxs-lookup"><span data-stu-id="06051-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="06051-141">Kun laskun alkuperän tyyppi on **Sopimuksen laskun integrointi**, **Ulkoisen laskun numero** -kenttä näkyy **Myyntilasku**-ylätunnisteessa.</span><span class="sxs-lookup"><span data-stu-id="06051-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="06051-142">Sen lisäksi että **Ulkoisen laskun numero** näkyy ylätunnisteessa, sen tietojen avulla voidaan varmistaa, että Field Servicen sopimuslaskuista luodut laskut suodatetaan pois synkronoitaessa laskuja Finance and Operationsista Field Serviceeen.</span><span class="sxs-lookup"><span data-stu-id="06051-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="06051-143">Valitse **Myyntireskontra** \> **Asetukset** \> **Laskun alkuperän koodit**.</span><span class="sxs-lookup"><span data-stu-id="06051-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="06051-144">Luo uusi laskun alkuperä valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="06051-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="06051-145">Anna **Laskun alkuperä** -kentässä laskun alkuperän nimi, kuten **FS**.</span><span class="sxs-lookup"><span data-stu-id="06051-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="06051-146">Kirjoita **Kuvaus**-kenttään kuvaus, kuten **Field Servicen sopimuslasku**.</span><span class="sxs-lookup"><span data-stu-id="06051-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="06051-147">Valitse **Alkuperän tyypin määritys** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="06051-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="06051-148">Valitse **Laskun alkuperän tyyppi** -kentässä **Sopimuksen laskun integrointi**.</span><span class="sxs-lookup"><span data-stu-id="06051-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="06051-149">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="06051-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="06051-150">Tietojen integrointiprojektissa</span><span class="sxs-lookup"><span data-stu-id="06051-150">In the Data Integration project</span></span>

<span data-ttu-id="06051-151">Tehtävä: **Laskurivit**</span><span class="sxs-lookup"><span data-stu-id="06051-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="06051-152">Varmista, että Finance and Operationsin kentän **Päätilin näyttöarvon** oletusarvo päivitetään vastaamaan haluttua arvoa.</span><span class="sxs-lookup"><span data-stu-id="06051-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="06051-153">Oletusmallin arvo on **401100**.</span><span class="sxs-lookup"><span data-stu-id="06051-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="06051-154">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="06051-154">Template mapping in Data integration</span></span>

<span data-ttu-id="06051-155">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="06051-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a><span data-ttu-id="06051-156">Sopimuslaskut (Field Servicestä Fin and Opsiin): Laskuotsikot</span><span class="sxs-lookup"><span data-stu-id="06051-156">Agreement invoices (Field Service to Fin and Ops): Invoice headers</span></span>

<span data-ttu-id="06051-157">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="06051-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a><span data-ttu-id="06051-158">Sopimuslaskut (Field Servicestä Fin and Opsiin): Laskurivit</span><span class="sxs-lookup"><span data-stu-id="06051-158">Agreement invoices (Field Service to Fin and Ops): Invoice lines</span></span>

<span data-ttu-id="06051-159">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="06051-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>
