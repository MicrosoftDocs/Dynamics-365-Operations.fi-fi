---
title: Tiedostojen ja tositteiden numeroiminen aikajärjestyksessä
description: Tässä aiheessa kerrotaan, miten sovellettavissa asiakirjoissa ja niihin liittyvissä tositteissa määritetään ja käytetään aikajärjestyksessä olevia numeroita.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: fe533052b0e5b04a7d27b954ba644761c631d6d7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838858"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="16776-103">Tiedostojen ja tositteiden numeroiminen aikajärjestyksessä</span><span class="sxs-lookup"><span data-stu-id="16776-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="16776-104">Joissakin maissa asiakirjojen ja niihin liittyvien tositteiden numeroinnissa on lakisääteinen vaatimus aikajärjestyksestä.</span><span class="sxs-lookup"><span data-stu-id="16776-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="16776-105">Kausien on tuettava aikajärjestystä.</span><span class="sxs-lookup"><span data-stu-id="16776-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="16776-106">Kaikkien aiempien kausien numeroiden on oltava pienempiä kuin myöhempiin kausiin kuuluvat numerot.</span><span class="sxs-lookup"><span data-stu-id="16776-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="16776-107">Tämän vaatimuksen täyttämiseksi on toteutettu aikajärjestyksessä numeroinnin toiminto.</span><span class="sxs-lookup"><span data-stu-id="16776-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="16776-108">Tässä aiheessa kerrotaan, miten sovellettavissa asiakirjoissa ja niihin liittyvissä tositteissa määritetään ja käytetään aikajärjestyksessä olevia numeroita.</span><span class="sxs-lookup"><span data-stu-id="16776-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="16776-109">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="16776-109">Prerequisites</span></span>

<span data-ttu-id="16776-110">Ota Ominaisuuksien hallinta -työtilassa käyttöön **Kronologinen numerointi** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="16776-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="16776-111">Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="16776-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="16776-112">Aikajärjestyksessä numeroimisen konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="16776-112">Configure chronological numbering</span></span>

<span data-ttu-id="16776-113">Aikajärjestyksessä numeroiminen vaikuttaa seuraaviin asiakirjoihin.</span><span class="sxs-lookup"><span data-stu-id="16776-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="16776-114">**Myyntireskontra**</span><span class="sxs-lookup"><span data-stu-id="16776-114">**Accounts receivable**</span></span>
- <span data-ttu-id="16776-115">Myyntilasku</span><span class="sxs-lookup"><span data-stu-id="16776-115">Customer invoice</span></span>
- <span data-ttu-id="16776-116">Asiakkaan laskutosite</span><span class="sxs-lookup"><span data-stu-id="16776-116">Customer invoice voucher</span></span>
- <span data-ttu-id="16776-117">Myynnin hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="16776-117">Sales credit note</span></span>
- <span data-ttu-id="16776-118">Myynnin hyvityslaskutosite</span><span class="sxs-lookup"><span data-stu-id="16776-118">Sales credit note voucher</span></span>
- <span data-ttu-id="16776-119">Vapaatekstilasku</span><span class="sxs-lookup"><span data-stu-id="16776-119">Free text invoice</span></span>
- <span data-ttu-id="16776-120">Vapaamuotoinen laskutosite</span><span class="sxs-lookup"><span data-stu-id="16776-120">Free text invoice voucher</span></span>
- <span data-ttu-id="16776-121">Vapaamuotoinen hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="16776-121">Free text credit note</span></span>
- <span data-ttu-id="16776-122">Vapaamuotoinen hyvityslaskutosite</span><span class="sxs-lookup"><span data-stu-id="16776-122">Free text credit note voucher</span></span>
- <span data-ttu-id="16776-123">Pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="16776-123">Packing slip</span></span>
- <span data-ttu-id="16776-124">Pakkausluettelon tosite</span><span class="sxs-lookup"><span data-stu-id="16776-124">Packing slip voucher</span></span>
- <span data-ttu-id="16776-125">Pakkausluettelon korjaustosite</span><span class="sxs-lookup"><span data-stu-id="16776-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="16776-126">Korkolaskutosite</span><span class="sxs-lookup"><span data-stu-id="16776-126">Interest note voucher</span></span>
- <span data-ttu-id="16776-127">Maksukehotustosite</span><span class="sxs-lookup"><span data-stu-id="16776-127">Collection letter voucher</span></span>

<span data-ttu-id="16776-128">**Ostoreskontra**</span><span class="sxs-lookup"><span data-stu-id="16776-128">**Accounts payable**</span></span>
- <span data-ttu-id="16776-129">Laskutustosite</span><span class="sxs-lookup"><span data-stu-id="16776-129">Invoice voucher</span></span>
- <span data-ttu-id="16776-130">Hyvityslaskutosite</span><span class="sxs-lookup"><span data-stu-id="16776-130">Credit note voucher</span></span>
- <span data-ttu-id="16776-131">Tuotteen vastaanoton tosite</span><span class="sxs-lookup"><span data-stu-id="16776-131">Product receipt voucher</span></span>

<span data-ttu-id="16776-132">**Projektinhallinta**</span><span class="sxs-lookup"><span data-stu-id="16776-132">**Project management**</span></span>
- <span data-ttu-id="16776-133">Lasku</span><span class="sxs-lookup"><span data-stu-id="16776-133">Invoice</span></span>
- <span data-ttu-id="16776-134">Laskutustosite</span><span class="sxs-lookup"><span data-stu-id="16776-134">Invoice voucher</span></span>
- <span data-ttu-id="16776-135">Hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="16776-135">Credit note</span></span>
- <span data-ttu-id="16776-136">Hyvityslaskutosite</span><span class="sxs-lookup"><span data-stu-id="16776-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="16776-137">Numerosarjojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="16776-137">Define number sequences</span></span>

<span data-ttu-id="16776-138">Voit määrittää numerosarjat kohdassa **Organisaation hallinta** > **Numerosarjat** > **Numerosarjat**.</span><span class="sxs-lookup"><span data-stu-id="16776-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="16776-139">Voit määrittää tarvittavan määrän numerosarjoja, jotka kattavat tarvittavien asiakirjojen kaudet.</span><span class="sxs-lookup"><span data-stu-id="16776-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="16776-140">Määritä kullekin numerosarjalle yritys.</span><span class="sxs-lookup"><span data-stu-id="16776-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="16776-141">Numerosarjojen segmentit on määritettävä niin, että ne antavat kausien aikajärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="16776-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="16776-142">Segmenttien nimet voivat esimerkiksi sisältää erityisen etuliitteen, joka yksilöi tietyn kauden.</span><span class="sxs-lookup"><span data-stu-id="16776-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Numerosarjojen määritys](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="16776-144">Numerosarjaryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="16776-144">Configure number sequence groups</span></span>

<span data-ttu-id="16776-145">Voit määrittää numerosarjaryhmiä kohdassa **Myyntireskontra** > **Määritys** > **Myyntireskontran parametrit**.</span><span class="sxs-lookup"><span data-stu-id="16776-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="16776-146">Määritä **Numerosarjat**-välilehdessä niin monta numerosarjaryhmää kuin on tarpeen tarvittavien kausien kattamiseksi.</span><span class="sxs-lookup"><span data-stu-id="16776-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="16776-147">Valitse kullekin ryhmälle **Viite**-osasta jokin tuetuista tiedostoviitteistä ja viittaa **Numerosarjan koodi** -kentässä numerosarjaan, joka oli aiemmin luotu kyseiselle jaksolle.</span><span class="sxs-lookup"><span data-stu-id="16776-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Numerosarjaryhmän määritys](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="16776-149">Konfiguroi numerosarjaryhmät samalla tavalla **Ostoreskontra**- ja **Projektinhallinta ja kirjanpito** -moduuleissa.</span><span class="sxs-lookup"><span data-stu-id="16776-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="16776-150">Numerosarjaryhmien kronologian määrittäminen</span><span class="sxs-lookup"><span data-stu-id="16776-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="16776-151">Voit määrittää numerosarjaryhmien kronologian kohdassa **Organisaation hallinto** > **Numerosarjat** > **Kronologiset numerosarjaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="16776-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="16776-152">Määritä numerosarjaryhmien käytettävyysehdot.</span><span class="sxs-lookup"><span data-stu-id="16776-152">Define the applicability conditions for number sequence groups.</span></span>

![Kronologisten numeroiden asetukset](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="16776-154">Kenttä</span><span class="sxs-lookup"><span data-stu-id="16776-154">Field</span></span>            | <span data-ttu-id="16776-155">kuvaus</span><span class="sxs-lookup"><span data-stu-id="16776-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16776-156">Voimassa</span><span class="sxs-lookup"><span data-stu-id="16776-156">Effective</span></span>  | <span data-ttu-id="16776-157">Numerosarjaryhmän käytettävyyden alkamispäivä.</span><span class="sxs-lookup"><span data-stu-id="16776-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="16776-158">Vanhentumisaika</span><span class="sxs-lookup"><span data-stu-id="16776-158">Expiration</span></span>      | <span data-ttu-id="16776-159">Numerosarjaryhmän käytettävyyden päättymispäivä.</span><span class="sxs-lookup"><span data-stu-id="16776-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="16776-160">Jos päättymispäivää ei käytetä, valitse **Ei koskaan**.</span><span class="sxs-lookup"><span data-stu-id="16776-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="16776-161">Numerosarjaryhmä</span><span class="sxs-lookup"><span data-stu-id="16776-161">Number sequence group</span></span> | <span data-ttu-id="16776-162">Numerosarjaryhmä, jota käytetään asiakirjan numeroiden tuottamiseen kauden aikana.</span><span class="sxs-lookup"><span data-stu-id="16776-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="16776-163">Alkuperäinen numerosarjaryhmä</span><span class="sxs-lookup"><span data-stu-id="16776-163">Original number sequence group</span></span> | <span data-ttu-id="16776-164">Tätä numerosarjaryhmän koodia käytetään lisäsuodattimena, kun tiedostoille on jo määritetty tietty *pysyvä* numerosarjaryhmä.</span><span class="sxs-lookup"><span data-stu-id="16776-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="16776-165">Tyhjä arvo katsotaan tietyksi arvoksi.</span><span class="sxs-lookup"><span data-stu-id="16776-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="16776-166">Jos haluat ohittaa esimääritetyn ryhmän, käytä tämän asetuksen **Oletus**-asetusta.</span><span class="sxs-lookup"><span data-stu-id="16776-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="16776-167">Oletus</span><span class="sxs-lookup"><span data-stu-id="16776-167">Default</span></span> | <span data-ttu-id="16776-168">Jos tämä on otettu käyttöön, järjestelmä ohittaa esimääritetyn asiakirjanumerosarjaryhmän ja käyttää vain kauden alkamis- ja päättymispäivämääriä käytettävyyden analyysissa.</span><span class="sxs-lookup"><span data-stu-id="16776-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="16776-169">Jos tämä kohta on poistettu käytöstä, järjestelmä käyttää valinnassa yhdistelmää **Voimassa** + **Vanhentumisaika** + **Alkuperäinen numerosarjaryhmä**.</span><span class="sxs-lookup"><span data-stu-id="16776-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="16776-170">Asiakirjan kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="16776-170">Document posting</span></span>
<span data-ttu-id="16776-171">Kun kirjaat tiedoston, tiedostolle määritetään asianmukainen numerosarjaryhmä, joka perustuu asiakirjan kirjauspäivämäärään. Sen jälkeen tiedostonumero luodaan tunnistetun numerosarjan perusteella.</span><span class="sxs-lookup"><span data-stu-id="16776-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="16776-172">Järjestelmä antaa viestin numerosarjaryhmän määritykseen liittyen.</span><span class="sxs-lookup"><span data-stu-id="16776-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Asiakirjan numero](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="16776-174">Joissakin maissa asiakirjanumeroinnissa on käytössä erityinen logiikka.</span><span class="sxs-lookup"><span data-stu-id="16776-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="16776-175">Tällöin maakohtainen logiikka korvaa **Kronologinen numerointi** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="16776-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
