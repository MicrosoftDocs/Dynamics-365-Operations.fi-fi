---
title: Käyttöhallinnan raporttinäkymä
description: Tässä ohjeaiheessa on tietoja sähköisen laskutuksen palvelun käyttöhallinnan raporttinäkymän käytöstä ja yhteensopivana pysymisestä.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130503"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="5ae28-103">Käyttöhallinnan raporttinäkymä</span><span class="sxs-lookup"><span data-stu-id="5ae28-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ae28-104">**Käyttöhallinta**-raporttinäkymän avulla voit valvoa sähköisen laskutuksen palvelun käyttöä ja näin ollen auttaa organisaatiota pysymään yhteensopivana sen kuukausittaisen käytön kannalta.</span><span class="sxs-lookup"><span data-stu-id="5ae28-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="5ae28-105">Yhteensopivuus määräytyy lähetysvolyymien laskennan avulla ja vertaamalla sitä lähetysten hankittuun volyymiin. Näin määritetään kaikki hankitun volyymin ja käytetyn volyymin väliset poikkeamat.</span><span class="sxs-lookup"><span data-stu-id="5ae28-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="5ae28-106">Raporttinäkymä sisältää seuraavat mittarit:</span><span class="sxs-lookup"><span data-stu-id="5ae28-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="5ae28-107">Yksi kustannusmittari, jonka avulla voit valvoa kulutusta lisenssien noudattamiseksi:</span><span class="sxs-lookup"><span data-stu-id="5ae28-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="5ae28-108">Käyttö kuukausittain (vienti)</span><span class="sxs-lookup"><span data-stu-id="5ae28-108">Usage per month (export)</span></span>

- <span data-ttu-id="5ae28-109">Kolme operatiivista mittaria, joiden avulla seurataan sähköisen laskutuksen palvelun käyttöä hallintatarkoituksissa:</span><span class="sxs-lookup"><span data-stu-id="5ae28-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="5ae28-110">Käyttö ominaisuuksien mukaan</span><span class="sxs-lookup"><span data-stu-id="5ae28-110">Usage by feature</span></span>
    - <span data-ttu-id="5ae28-111">Käyttö ympäristön mukaan</span><span class="sxs-lookup"><span data-stu-id="5ae28-111">Usage by environment</span></span>
    - <span data-ttu-id="5ae28-112">Käyttö kuukausittain (tuonti)</span><span class="sxs-lookup"><span data-stu-id="5ae28-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="5ae28-113">Mittareiden vaikutusalue</span><span class="sxs-lookup"><span data-stu-id="5ae28-113">Measurement scope</span></span>

- <span data-ttu-id="5ae28-114">Mittayksikkö:</span><span class="sxs-lookup"><span data-stu-id="5ae28-114">Unit of measure:</span></span> 

    <span data-ttu-id="5ae28-115">**Käyttöhallinta**-raporttinäkymä laskee liiketoimintatiedostojen lähetykset ja tuodut sähköiset laskut.</span><span class="sxs-lookup"><span data-stu-id="5ae28-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="5ae28-116">Organisaatio:</span><span class="sxs-lookup"><span data-stu-id="5ae28-116">Organization:</span></span> 

    <span data-ttu-id="5ae28-117">Laskenta tehdään organisaatiosi vuokraajatunnuksen perusteella riippumatta Microsoft Dynamics 365 Financen tai Dynamics 365 Supply Chain Managementin esiintymien lukumäärästä tai niiden yksiköiden lukumäärästä, joissa sähköinen laskutuspalvelu on käytössä.</span><span class="sxs-lookup"><span data-stu-id="5ae28-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="5ae28-118">Mittari: Käyttö kuukaudessa (vienti)</span><span class="sxs-lookup"><span data-stu-id="5ae28-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="5ae28-119">Tässä mittarissa on tietoja sähköisistä laskuista, joita organisaatio lähettää määritetyn kauden aikana.</span><span class="sxs-lookup"><span data-stu-id="5ae28-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="5ae28-120">Alue</span><span class="sxs-lookup"><span data-stu-id="5ae28-120">Scope</span></span>
- <span data-ttu-id="5ae28-121">Financesta ja Supply Chain Managementista sähköiselle laskutuspalvelulle lähetettyjen liiketoiminta-asiakirjojen määrä riippumatta siitä, kuinka monta riviä nämä liiketoiminta-asiakirjat sisältävät.</span><span class="sxs-lookup"><span data-stu-id="5ae28-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="5ae28-122">Lähetettyjen liiketoiminta-asiakirjojen määrä, jonka sähköinen laskutuspalvelu käsittelee onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="5ae28-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="5ae28-123">Asiakirjaa käsitellään onnistuneesti, kun toimintoasetuksissa määritettyjen toimenpiteiden työnkulku on valmis.</span><span class="sxs-lookup"><span data-stu-id="5ae28-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="5ae28-124">Kun sähköinen lasku lähetetään ulkoiseen Internet-palveluun, laskenta ei riipu Internet-palvelun käsittelyn tuloksista (hyväksytty, hylätty tai skeeman oikeellisuustarkistusvirhe).</span><span class="sxs-lookup"><span data-stu-id="5ae28-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="5ae28-125">Jos Internet-palvelu on vastaanottanut sähköisen laskutuksen palvelun vastaanottaneen ja vastannut pyyntöön, lähetys lasketaan kelvolliseksi.</span><span class="sxs-lookup"><span data-stu-id="5ae28-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="5ae28-126">**Poikkeus:** Yritysasiakirjoja ei lasketa, jos ne lähetetään uudelleen Financesta tai Supply Chain Managementista sähköiseen laskutuspalveluun esimerkiksi tilanteissa, joissa saman liiketoiminta-asiakirjan uudelleenlähetys vaaditaan sähköisen laskun tilan muuttamiseksi.</span><span class="sxs-lookup"><span data-stu-id="5ae28-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="5ae28-127">Esimerkiksi Brasilian sähköisen laskutuksen (veroasiakirjan) lähetys lasketaan kelvolliseksi, mutta sen peruutuspyyntöä ei lasketa.</span><span class="sxs-lookup"><span data-stu-id="5ae28-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="5ae28-128">Laskelma</span><span class="sxs-lookup"><span data-stu-id="5ae28-128">Calculation</span></span>

<span data-ttu-id="5ae28-129">Saldo lasketaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="5ae28-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="5ae28-130">Saldo = Maksuton + Ostettu - Käytetty</span><span class="sxs-lookup"><span data-stu-id="5ae28-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="5ae28-131">Jossa:</span><span class="sxs-lookup"><span data-stu-id="5ae28-131">Where:</span></span>

- <span data-ttu-id="5ae28-132">Maksuton:</span><span class="sxs-lookup"><span data-stu-id="5ae28-132">Free:</span></span>
  
    <span data-ttu-id="5ae28-133">Maksuton määrä liikeasiakirjoja, jotka asiakas voi lähettää kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="5ae28-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="5ae28-134">Mukana on 100 liiketoiminta-asiakirjan paketti, joka voidaan lähettää sähköiseen laskutuspalveluun.</span><span class="sxs-lookup"><span data-stu-id="5ae28-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="5ae28-135">Maksuton määrä ei ole kumulatiivinen, eikä jäljelle jäävä saldoa siirretä seuraavalle jaksolle.</span><span class="sxs-lookup"><span data-stu-id="5ae28-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="5ae28-136">Ostettu:</span><span class="sxs-lookup"><span data-stu-id="5ae28-136">Purchased:</span></span>
  
    <span data-ttu-id="5ae28-137">1 000 liiketoiminta-asiakirjan paketti, joka voidaan lähettää sähköiseen laskutuspalveluun.</span><span class="sxs-lookup"><span data-stu-id="5ae28-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="5ae28-138">Tämä paketti on hankittava organisaatiollesi kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="5ae28-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="5ae28-139">Ostettu määrä ei ole kumulatiivinen, eikä jäljelle jäävä saldoa siirretä seuraavalle jaksolle.</span><span class="sxs-lookup"><span data-stu-id="5ae28-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="5ae28-140">Käytetty:</span><span class="sxs-lookup"><span data-stu-id="5ae28-140">Used:</span></span> 

    <span data-ttu-id="5ae28-141">Sähköisen laskutuksen palveluun lähetettyjen liiketoimintatiedostojen määrä määritettyjen ehtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="5ae28-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="5ae28-142">Jos organisaatiosi aikoo ylittää 100 maksuttoman lähetyksen kuukausittaisen määrän, osta suurin volyymi varmistaaksesi, että olet edelleen Microsoftin sähköisen laskutuksen lisenssikäytännön mukainen.</span><span class="sxs-lookup"><span data-stu-id="5ae28-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="5ae28-143">Tällä hetkellä ostetut volyymit on syötettävä manuaalisesti hankintapäivämäärän mukaan useassa 1 000:n lähetyksen paketissa.</span><span class="sxs-lookup"><span data-stu-id="5ae28-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="5ae28-144">Mittari: Käyttö ominaisuuden mukaan</span><span class="sxs-lookup"><span data-stu-id="5ae28-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="5ae28-145">Tässä mittarissa näkyy sähköisten laskutusominaisuuksien käyttö sähköisten laskujen lähettämiseksi määritettynä ajanjaksona.</span><span class="sxs-lookup"><span data-stu-id="5ae28-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="5ae28-146">Laskenta:</span><span class="sxs-lookup"><span data-stu-id="5ae28-146">Calculation:</span></span>
  
    <span data-ttu-id="5ae28-147">Käytetty = kuinka monta kertaa kutakin sähköistä laskutustoimintoa on käytetty, kun liikeasiakirjoja on lähetetty sähköiseen laskutuspalveluun.</span><span class="sxs-lookup"><span data-stu-id="5ae28-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="5ae28-148">Mittari: Käyttö ympäristön mukaan</span><span class="sxs-lookup"><span data-stu-id="5ae28-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="5ae28-149">Tässä mittarissa näkyy sähköisen laskutuksen palveluympäristöjen käyttö määritettynä aikana.</span><span class="sxs-lookup"><span data-stu-id="5ae28-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="5ae28-150">Laskenta:</span><span class="sxs-lookup"><span data-stu-id="5ae28-150">Calculation:</span></span>
    
    <span data-ttu-id="5ae28-151">Käytetty = kuinka monta kertaa kutakin sähköisen laskutuksen palveluympäristöä on käytetty, kun liikeasiakirjoja on lähetetty sähköiseen laskutuspalveluun.</span><span class="sxs-lookup"><span data-stu-id="5ae28-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="5ae28-152">Mittari: Käyttö kuukaudessa (tuonti)</span><span class="sxs-lookup"><span data-stu-id="5ae28-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="5ae28-153">Tässä mittarissa näkyy, kuinka paljon sähköisiä laskuja on tuotu sähköisen laskutuksen kautta Financeen ja Supply Chain Managementiin määritetyllä kaudella.</span><span class="sxs-lookup"><span data-stu-id="5ae28-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="5ae28-154">Alue:</span><span class="sxs-lookup"><span data-stu-id="5ae28-154">Scope:</span></span>

    <span data-ttu-id="5ae28-155">Financeen ja Supply Chain Managementiin tuodut sähköiset laskut riippumatta kyseisten sähköisten laskujen rivien lukumäärästä.</span><span class="sxs-lookup"><span data-stu-id="5ae28-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="5ae28-156">Laskenta:</span><span class="sxs-lookup"><span data-stu-id="5ae28-156">Calculation:</span></span>

    <span data-ttu-id="5ae28-157">Vastaanotettu = Financeen ja Supply Chain Managementiin tuotujen sähköisten laskujen määrä.</span><span class="sxs-lookup"><span data-stu-id="5ae28-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="5ae28-158">Funktiot</span><span class="sxs-lookup"><span data-stu-id="5ae28-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="5ae28-159">Osto</span><span class="sxs-lookup"><span data-stu-id="5ae28-159">Purchase</span></span>

<span data-ttu-id="5ae28-160">Valitse **Kuukausittainen käyttö (vienti)** -välilehdessä **Osto**, jos haluat rekisteröidä hankittujen lähetysten määrän manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="5ae28-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="5ae28-161">Valitse jollekin päivälle **Uusi** ja määritä tuona päivänä hankittujen **pakettien** määrä.</span><span class="sxs-lookup"><span data-stu-id="5ae28-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="5ae28-162">**Määrä** lasketaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="5ae28-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="5ae28-163">Määrä = Paketit \* 1 000</span><span class="sxs-lookup"><span data-stu-id="5ae28-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="5ae28-164">Laskettu **Määrä** vastaa **Ostettu**-arvoa **Käyttö kuukaudessa (vienti)** -mittarissa.</span><span class="sxs-lookup"><span data-stu-id="5ae28-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="5ae28-165">Päivitys</span><span class="sxs-lookup"><span data-stu-id="5ae28-165">Update</span></span>

<span data-ttu-id="5ae28-166">Päivitä laskelma ja päivitä sivulla ja kaaviossa näkyvät tiedot valitsemalla toimintoruudussa **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="5ae28-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="5ae28-167">Palauta historiatiedot</span><span class="sxs-lookup"><span data-stu-id="5ae28-167">Reset history data</span></span>

<span data-ttu-id="5ae28-168">Valitse toimintoruudussa **Nollaa historiatiedot** ja päivitä tietokanta, josta mittarit lasketaan.</span><span class="sxs-lookup"><span data-stu-id="5ae28-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="5ae28-169">**Käyttöhallinta**-koontinäyttö ei näytä rahasummia.</span><span class="sxs-lookup"><span data-stu-id="5ae28-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="5ae28-170">Sen sijaan siinä näkyy vain laskettujen lähetysten ja tuotujen tiedostojen määrä.</span><span class="sxs-lookup"><span data-stu-id="5ae28-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
