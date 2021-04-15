---
title: Ennustemallin parantaminen (esiversio)
description: Tässä ohjeaiheessa kuvataan toimintoja, joiden avulla voit parantaa ennustemallien suorituskykyä.
author: ShivamPandey-msft
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 197aba724ea68ef79c2d16028c23533d952329a9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810006"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="e004e-103">Ennustemallin parantaminen (esiversio)</span><span class="sxs-lookup"><span data-stu-id="e004e-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e004e-104">Tässä ohjeaiheessa kuvataan toimintoja, joiden avulla voit parantaa ennustemallien suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="e004e-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="e004e-105">Aloita mallin parantaminen **Asiakkaan maksuennusteet** -työtilassa Microsoft Dynamics 365 Financessa.</span><span class="sxs-lookup"><span data-stu-id="e004e-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="e004e-106">Parannusvaiheet tehdään AI Builderissa.</span><span class="sxs-lookup"><span data-stu-id="e004e-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="e004e-107">Aiempien tulosten valitseminen</span><span class="sxs-lookup"><span data-stu-id="e004e-107">Select historical outcomes</span></span>

<span data-ttu-id="e004e-108">Valitse vähintään yksi kolmesta laskun mahdollisesta lopputuloksesta: **Ajoissa**, **Myöhässä** ja **Erittäin paljon myöhässä**.</span><span class="sxs-lookup"><span data-stu-id="e004e-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="e004e-109">Valitse kaikki kolme tulosta.</span><span class="sxs-lookup"><span data-stu-id="e004e-109">All three outcomes should be selected.</span></span> <span data-ttu-id="e004e-110">Jos poistat jonkin tuloksen valinnan, laskut suodatetaan pois koulutusprosessista ja ennusteen tarkkuus vähenee.</span><span class="sxs-lookup"><span data-stu-id="e004e-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="e004e-111">[![Tulosten vahvistaminen](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="e004e-112">Jos organisaatio vaatii vain kaksi tulosta, muuta **Myöhässä**- ja **Erittäin paljon myöhässä** -kohtien rajoiksi 0 (nolla) päivää.</span><span class="sxs-lookup"><span data-stu-id="e004e-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="e004e-113">Näin voit tehokkaasti kutistaa ennusteen binaariseen **Ajoissa**- tai **Myöhässä**-tilaan.</span><span class="sxs-lookup"><span data-stu-id="e004e-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="e004e-114">Valitse kentät</span><span class="sxs-lookup"><span data-stu-id="e004e-114">Select fields</span></span>

<span data-ttu-id="e004e-115">Kun valitset malliin sisällytettävät kentät, huomaa, että luettelossa ovat kaikki Azure Data Lakeen yhdistettyjen tietojen Microsoft Dataverse -taulukon käytettävissä olevat kentät.</span><span class="sxs-lookup"><span data-stu-id="e004e-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="e004e-116">Joitakin näistä kentistä **ei** tule valita.</span><span class="sxs-lookup"><span data-stu-id="e004e-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="e004e-117">Kentät, joita ei tule valita, kuuluvat yhteen kolmesta luokasta:</span><span class="sxs-lookup"><span data-stu-id="e004e-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="e004e-118">Kenttä on pakollinen Dataverse-taulukolle, mutta Data Lakessa ei ole sen varmuuskopioita.</span><span class="sxs-lookup"><span data-stu-id="e004e-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="e004e-119">Kenttä on tunnus, eikä sen vuoksi ole järkevää käyttää sitä koneoppimistoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="e004e-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="e004e-120">Kenttä edustaa tietoja, jotka eivät ole käytettävissä ennusteen aikana.</span><span class="sxs-lookup"><span data-stu-id="e004e-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="e004e-121">Seuraavissa osissa näkyvät laskussa ja asiakasentiteeteissä käytettävissä olevat kentät ja kentät, joita **ei** tule valita koulutukseen.</span><span class="sxs-lookup"><span data-stu-id="e004e-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="e004e-122">Luokka, joka on määritetty kullekin näistä kentistä, viittaa edellä olevan luettelon luokkiin.</span><span class="sxs-lookup"><span data-stu-id="e004e-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="e004e-123">Laskun Dataverse-taulu</span><span class="sxs-lookup"><span data-stu-id="e004e-123">Invoice Dataverse table</span></span>

<span data-ttu-id="e004e-124">Seuraavassa kuvassa ovat laskutaulukolle käytettävissä olevat kentät.</span><span class="sxs-lookup"><span data-stu-id="e004e-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="e004e-125">[![Laskutaulukon käytettävissä olevat kentät](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="e004e-126">Seuraavia kenttiä ei saa valita koulutukselle:</span><span class="sxs-lookup"><span data-stu-id="e004e-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="e004e-127">**Laskutili** (luokka 2)</span><span class="sxs-lookup"><span data-stu-id="e004e-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="e004e-128">**On suljettu** (luokka 3) – Tämän kentän avulla suodatetaan laskut koulutusta (suljettu) ja ennustetta (ei suljettu) varten.</span><span class="sxs-lookup"><span data-stu-id="e004e-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="e004e-129">**Nimi** (luokka 1)</span><span class="sxs-lookup"><span data-stu-id="e004e-129">**Name** (category 1)</span></span>
- <span data-ttu-id="e004e-130">**Lähteen tunnus** (luokka 2)</span><span class="sxs-lookup"><span data-stu-id="e004e-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="e004e-131">**Lähdetietue** (luokka 2)</span><span class="sxs-lookup"><span data-stu-id="e004e-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="e004e-132">**Lähdetaulukko** (luokka 2)</span><span class="sxs-lookup"><span data-stu-id="e004e-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="e004e-133">Asiakkaan Dataverse-taulu</span><span class="sxs-lookup"><span data-stu-id="e004e-133">Customer Dataverse table</span></span>

<span data-ttu-id="e004e-134">Seuraavassa kuvassa ovat asiakastaulukolle käytettävissä olevat kentät.</span><span class="sxs-lookup"><span data-stu-id="e004e-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="e004e-135">[![Asiakastaulukon käytettävissä olevat kentät](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="e004e-136">Seuraavaa kenttää ei saa valita koulutukselle:</span><span class="sxs-lookup"><span data-stu-id="e004e-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="e004e-137">**Rivin yksilöivä avain** (luokka 2)</span><span class="sxs-lookup"><span data-stu-id="e004e-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="e004e-138">Suodattimet</span><span class="sxs-lookup"><span data-stu-id="e004e-138">Filters</span></span>

<span data-ttu-id="e004e-139">Suodattimet eivät tällä hetkellä tue asiakkaan maksuennusteen skenaariota.</span><span class="sxs-lookup"><span data-stu-id="e004e-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="e004e-140">Valitse tämän vuoksi **Ohita tämä vaihe** ja jatka Yhteenveto-sivulle.</span><span class="sxs-lookup"><span data-stu-id="e004e-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="e004e-141">[![Kohdistusmalli ja suodattimet](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="e004e-142">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="e004e-142">Privacy notice</span></span>
<span data-ttu-id="e004e-143">Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.</span><span class="sxs-lookup"><span data-stu-id="e004e-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]