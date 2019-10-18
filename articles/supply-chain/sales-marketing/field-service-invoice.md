---
title: Field Servicen sopimuslaskujen synkronointi Supply Chain Managementin vapaatekstilaskuihin
description: Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Dynamics 365 Field Servicen sopimuslaskut synkronoidaan Dynamics 365 Supply Chain Managementiin vapaatekstilaskuihin.
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
ms.openlocfilehash: 3ca0014dc8bc1c70670a3cf85527eee0ef44865f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249862"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="81987-103">Field Servicen sopimuslaskujen synkronointi Supply Chain Managementin vapaatekstilaskuihin</span><span class="sxs-lookup"><span data-stu-id="81987-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="81987-104">Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Dynamics 365 Field Servicen sopimuslaskut synkronoidaan Dynamics 365 Supply Chain Managementiin vapaatekstilaskuihin.</span><span class="sxs-lookup"><span data-stu-id="81987-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="81987-105">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="81987-105">Templates and tasks</span></span>

<span data-ttu-id="81987-106">Field Servicen sopimuslaskut synkronoidaan Supply Chain Managementin vapaatekstilaskuihin seuraavien mallien ja taustalla olevien tehtävien avulla.</span><span class="sxs-lookup"><span data-stu-id="81987-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="81987-107">**Mallin nimi Tietojen integroinnissa**</span><span class="sxs-lookup"><span data-stu-id="81987-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="81987-108">Sopimuslaskut (Field Servicesta Supply Chain Managementiin)</span><span class="sxs-lookup"><span data-stu-id="81987-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="81987-109">**Tietojen integrointiprojektin tehtävien nimet**</span><span class="sxs-lookup"><span data-stu-id="81987-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="81987-110">Laskun ylätunnisteet</span><span class="sxs-lookup"><span data-stu-id="81987-110">Invoice headers</span></span>
- <span data-ttu-id="81987-111">Laskurivit</span><span class="sxs-lookup"><span data-stu-id="81987-111">Invoice lines</span></span>

<span data-ttu-id="81987-112">Seuraavat synkronointi tarvitaan, ennen kuin sopimuslaskut voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="81987-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="81987-113">Asiakkaat (Salesista Supply Chain Managementiin) - suora</span><span class="sxs-lookup"><span data-stu-id="81987-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="81987-114">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="81987-114">Entity set</span></span>

| <span data-ttu-id="81987-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="81987-115">Field Service</span></span>  | <span data-ttu-id="81987-116">Toimitusketjun hallinta</span><span class="sxs-lookup"><span data-stu-id="81987-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="81987-117">laskut</span><span class="sxs-lookup"><span data-stu-id="81987-117">invoices</span></span>       | <span data-ttu-id="81987-118">CDS-asiakkaan vapaatekstilaskujen otsikot</span><span class="sxs-lookup"><span data-stu-id="81987-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="81987-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="81987-119">invoicedetails</span></span> | <span data-ttu-id="81987-120">CDS-asiakkaan vapaatekstilaskujen rivit</span><span class="sxs-lookup"><span data-stu-id="81987-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="81987-121">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="81987-121">Entity flow</span></span>

<span data-ttu-id="81987-122">Field Servicen sopimukset luodut laskut voidaan synkronoida Supply Chain Managementiin Common Data Service -palvelun tietojen integrointiprojektina.</span><span class="sxs-lookup"><span data-stu-id="81987-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Common Data Service Data integration project.</span></span> <span data-ttu-id="81987-123">Näiden laskujen päivitykset synkronoidaan Supply Chain Managementin vapaatekstilaskuihin, jos vapaatekstilaskun kirjanpidollinen tila on **Käsittelyssä**.</span><span class="sxs-lookup"><span data-stu-id="81987-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="81987-124">Sen jälkeen kun vapaatekstilasku on kirjattu Supply Chain Managementissa ja kirjanpidolliseksi tilaksi on päivitetty **Valmis**, päivityksiä ei voi enää synkronoida Field Servicestä.</span><span class="sxs-lookup"><span data-stu-id="81987-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="81987-125">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="81987-125">Field Service CRM solution</span></span>

<span data-ttu-id="81987-126">**Sisältää sopimuksesta peräisin olevia rivejä** -kenttä on lisätty **Lasku**-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="81987-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="81987-127">Tämän kentän avulla voi varmistaa, että vain sopimuksesta luodut laskut synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="81987-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="81987-128">Arvo on **tosi**, jos laskussa on vähintään yksi sopimuksesta peräisin oleva laskurivi.</span><span class="sxs-lookup"><span data-stu-id="81987-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="81987-129">**On peräisin sopimuksesta** -kenttä on lisätty **Laskurivi**-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="81987-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="81987-130">Tämän kentän avulla voi varmistaa, että vain sopimuksesta luodut laskurivit synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="81987-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="81987-131">Arvo on **tosi**, jos laskurivi on peräisin sopimuksesta.</span><span class="sxs-lookup"><span data-stu-id="81987-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="81987-132">**Laskun päivämäärä** on pakollinen kenttä Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="81987-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="81987-133">Tämän vuoksi kentässä on Field Service -arvo ennen synkronointia.</span><span class="sxs-lookup"><span data-stu-id="81987-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="81987-134">Seuraava logiikka lisättiin, jotta tämä vaatimus toteutuisi:</span><span class="sxs-lookup"><span data-stu-id="81987-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="81987-135">Jos **Laskun päivämäärä** -kenttä on tyhjä **Lasku**-yksikössä (eli siinä ei ole arvoa), siksi määritetään se kuluva päivä, jolloin sopimuksesta peräisin oleva laskurivi lisätään.</span><span class="sxs-lookup"><span data-stu-id="81987-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="81987-136">Käyttäjä voi muuttaa **Laskun päivämäärä** -kenttää.</span><span class="sxs-lookup"><span data-stu-id="81987-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="81987-137">Kun käyttäjä kuitenkin yrittää tallentaa sopimuksesta peräisin olevan laskun, hänen vastaanottaa liiketoimintaprosessin virheen, jos laskun **Laskun päivämäärä** -kenttä on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="81987-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="81987-138">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="81987-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="81987-139">Supply Chain Managementiin</span><span class="sxs-lookup"><span data-stu-id="81987-139">In Supply Chain Management</span></span>

<span data-ttu-id="81987-140">Laskun alkuperä on määritettävä integraatiota varten, jotta Supply Chain Managementiin Field Servicen sopimuslaskuista luodut vapaatekstilaskut voidaan erottaa.</span><span class="sxs-lookup"><span data-stu-id="81987-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="81987-141">Kun laskun alkuperän tyyppi on **Sopimuksen laskun integrointi**, **Ulkoisen laskun numero** -kenttä näkyy **Myyntilasku**-ylätunnisteessa.</span><span class="sxs-lookup"><span data-stu-id="81987-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="81987-142">Sen lisäksi että **Ulkoisen laskun numero** näkyy ylätunnisteessa, sen tietojen avulla voidaan varmistaa, että Field Servicen sopimuslaskuista luodut laskut suodatetaan pois synkronoitaessa laskuja Supply Chain Managementista Field Serviceeen.</span><span class="sxs-lookup"><span data-stu-id="81987-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="81987-143">Valitse **Myyntireskontra** \> **Asetukset** \> **Laskun alkuperän koodit**.</span><span class="sxs-lookup"><span data-stu-id="81987-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="81987-144">Luo uusi laskun alkuperä valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="81987-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="81987-145">Anna **Laskun alkuperä** -kentässä laskun alkuperän nimi, kuten **FS**.</span><span class="sxs-lookup"><span data-stu-id="81987-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="81987-146">Kirjoita **Kuvaus**-kenttään kuvaus, kuten **Field Servicen sopimuslasku**.</span><span class="sxs-lookup"><span data-stu-id="81987-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="81987-147">Valitse **Alkuperän tyypin määritys** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="81987-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="81987-148">Valitse **Laskun alkuperän tyyppi** -kentässä **Sopimuksen laskun integrointi**.</span><span class="sxs-lookup"><span data-stu-id="81987-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="81987-149">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="81987-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="81987-150">Tietojen integrointiprojektissa</span><span class="sxs-lookup"><span data-stu-id="81987-150">In the Data Integration project</span></span>

<span data-ttu-id="81987-151">Tehtävä: **Laskurivit**</span><span class="sxs-lookup"><span data-stu-id="81987-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="81987-152">Varmista, että Supply Chain Managementin kentän **Päätilin näyttöarvon** oletusarvo päivitetään vastaamaan haluttua arvoa.</span><span class="sxs-lookup"><span data-stu-id="81987-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="81987-153">Oletusmallin arvo on **401100**.</span><span class="sxs-lookup"><span data-stu-id="81987-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="81987-154">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="81987-154">Template mapping in Data integration</span></span>

<span data-ttu-id="81987-155">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="81987-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="81987-156">Sopimuslaskut (Field Servicesta Supply Chain Managementiin): Laskujen otsikot</span><span class="sxs-lookup"><span data-stu-id="81987-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="81987-157">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="81987-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="81987-158">Sopimuslaskut (Field Servicesta Supply Chain Managementiin): Laskurivit</span><span class="sxs-lookup"><span data-stu-id="81987-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="81987-159">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="81987-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>
