---
title: Online-tilauksen ja asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen
description: Tässä aiheessa kerrotaan, miten online-tilauksen ja asynkronisen asiakastilauksen tapahtumia muokataan ja tarkistetaan Microsoft Dynamics 365 Commercessa.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0fee5ef7ad61e9581e7b2797bb1bd26b1a48ddbd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221771"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="e1312-103">Online-tilauksen ja asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="e1312-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1312-104">Tässä aiheessa kerrotaan, miten online-tilauksen ja asynkronisen asiakastilauksen tapahtumia muokataan ja tarkistetaan Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="e1312-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e1312-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e1312-105">Overview</span></span>

<span data-ttu-id="e1312-106">Commerce-sovelluksen versioiden 10.0.5 ja 10.0.6 välillä lisättiin itsepalvelutukkutapahtumien (kuten myynti ja palautus) ja kassanhallintatapahtumien (kuten liukuva merkintä ja maksuvälineen poisto) muokkauksen tuki.</span><span class="sxs-lookup"><span data-stu-id="e1312-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="e1312-107">Commerce-sovelluksen versiossa 10.0.7 lisättiin online-tilaustapahtumien ja asynkronisten asiakastilaustapahtumien muokkauksen tuki.</span><span class="sxs-lookup"><span data-stu-id="e1312-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="e1312-108">Tilaustapahtumien muokkaaminen ja tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="e1312-108">Edit and audit order transactions</span></span>

<span data-ttu-id="e1312-109">Voit muokata ja tarkistaa Commerce-pääkonttorisovelluksen tapahtumia seuraamalla alla olevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e1312-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e1312-110">Asenna [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span><span class="sxs-lookup"><span data-stu-id="e1312-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="e1312-111">Määritä **Tilaus**-pikavälilehden **Asiakastilaukset**-välilehden **Vähittäismyynnin parametrit** -sivun **Tilauksen synkronointivirheiden estokoodi** -kohdassa estokoodi.</span><span class="sxs-lookup"><span data-stu-id="e1312-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="e1312-112">Avaa **Myymälän myyntitiedot** -työtila.</span><span class="sxs-lookup"><span data-stu-id="e1312-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="e1312-113">**Online-tilauksen synkronointivirheet**- ja **Asiakastilauksen synkronointivirheet** -ruuduissa on vähittäismyyntitapahtuman sivun esisuodatettu näkymä.</span><span class="sxs-lookup"><span data-stu-id="e1312-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="e1312-114">Ne näyttävät tapahtumatietueet, joiden vastaavan tilaustyypin synkronointi epäonnistui.</span><span class="sxs-lookup"><span data-stu-id="e1312-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="e1312-115">Avaa **Online-tilauksen synkronointivirheet**- tai **Asiakastilauksen synkronointivirheet** -sivu.</span><span class="sxs-lookup"><span data-stu-id="e1312-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="e1312-116">Valitse tietue, jonka synkronointivirheen tietoja haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="e1312-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="e1312-117">**Synkronoinnin tila** -pikavälilehdessä ovat seuraavat virhetiedot:</span><span class="sxs-lookup"><span data-stu-id="e1312-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="e1312-118">Odottavan tilauksen tila</span><span class="sxs-lookup"><span data-stu-id="e1312-118">Pending order status</span></span>
    - <span data-ttu-id="e1312-119">Tilausvirheen tiedot</span><span class="sxs-lookup"><span data-stu-id="e1312-119">Order error details</span></span>
    - <span data-ttu-id="e1312-120">Muokkauksen päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="e1312-120">Modified date and time</span></span>
    - <span data-ttu-id="e1312-121">Uudelleenyrityslaskuri</span><span class="sxs-lookup"><span data-stu-id="e1312-121">Retry count</span></span>

1. <span data-ttu-id="e1312-122">Jos virheen tiedot osoittavat, että tietuetta on korjattava, valitse **Office Add-in** ja valitse sitten **Muokkaa valittua tapahtumaa**.</span><span class="sxs-lookup"><span data-stu-id="e1312-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="e1312-123">Valitun tapahtuman tiedot sisältävä Excel-tiedosto avataan.</span><span class="sxs-lookup"><span data-stu-id="e1312-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="e1312-124">Jos muokattava tapahtuma on online-tilaustapahtuma, Excel-tiedosto sisältää seuraavat laskentataulukot:</span><span class="sxs-lookup"><span data-stu-id="e1312-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="e1312-125">**Tapahtuma** – Tässä laskentataulukossa ovat tapahtuman otsikkotiedot.</span><span class="sxs-lookup"><span data-stu-id="e1312-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="e1312-126">**Myyntitapahtuma** – Tässä laskentataulukossa ovat tapahtuman rivitiedot.</span><span class="sxs-lookup"><span data-stu-id="e1312-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="e1312-127">**Maksutapahtumat** – Tässä laskentataulukossa ovat tapahtuman maksurivien tiedot.</span><span class="sxs-lookup"><span data-stu-id="e1312-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="e1312-128">**Alennustapahtumat** – Tässä laskentataulukossa ovat tapahtuman alennukseen liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="e1312-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="e1312-129">**Verotapahtumat** – Tässä laskentataulukossa ovat tapahtuman veroihin liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="e1312-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="e1312-130">**kulutapahtumat** – Tässä laskentataulukossa ovat tapahtuman kuluihin liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="e1312-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="e1312-131">Jos muokattava tapahtuma on asynkroninen asiakastilaustapahtuma, Excel-tiedosto sisältää seuraavat laskentataulukot:</span><span class="sxs-lookup"><span data-stu-id="e1312-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="e1312-132">**Rivit** – Tässä laskentataulukossa ovat tapahtuman otsikko- ja rivitiedot.</span><span class="sxs-lookup"><span data-stu-id="e1312-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="e1312-133">**Maksut** – Tässä laskentataulukossa ovat tapahtuman maksurivien tiedot.</span><span class="sxs-lookup"><span data-stu-id="e1312-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="e1312-134">**Alennukset** – Tässä laskentataulukossa ovat tapahtuman alennukseen liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="e1312-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="e1312-135">**Verot** –Tässä laskentataulukossa ovat tapahtuman veroihin liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="e1312-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="e1312-136">**Kulut** – Tässä laskentataulukossa ovat tapahtuman kuluihin liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="e1312-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="e1312-137">Syötä Excel-tiedoston **Odottava tilauksen tila** -kenttään **Muokkaus** ja julkaise muutos.</span><span class="sxs-lookup"><span data-stu-id="e1312-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="e1312-138">Näin voit estää sen, että erätilassa suoritettava **Synkronoi tilaus** -työ ohittaa tämän tietueen käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="e1312-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="e1312-139">Excel-tiedostossa muokataan soveltuvia kenttiä. Tämän jälkeen tiedot ladataan takaisin Commerce-pääkonttorisovellukseen Dynamics Excel -lisäosan julkaisutoiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="e1312-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="e1312-140">Kun tiedot on julkaistu, ne näkyvät järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="e1312-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="e1312-141">Julkaisemisen aikana käyttäjien tekemiä muutoksia ei tarkisteta.</span><span class="sxs-lookup"><span data-stu-id="e1312-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="e1312-142">Voit tarkastella muutosten täydellistä kirjausketjua valitsemalla otsikkotason muutoksille **Näytä kirjausketju** -kohdan **Vähittäismyyntitapahtuma**-otsikossa soveltuvan tapahtumasivun osassa ja tietueessa.</span><span class="sxs-lookup"><span data-stu-id="e1312-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="e1312-143">Esimerkiksi kaikki myyntiriveihin liittyvät muutokset näkyvät **Myyntitapahtumat**-sivulla ja maksuihin liittyvät muutokset **Maksutapahtumat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e1312-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="e1312-144">Seuraavia tarkistustietoja muutetaan:</span><span class="sxs-lookup"><span data-stu-id="e1312-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="e1312-145">Muokkauksen päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="e1312-145">Modified date and time</span></span>
    - <span data-ttu-id="e1312-146">Kenttä</span><span class="sxs-lookup"><span data-stu-id="e1312-146">Field</span></span>
    - <span data-ttu-id="e1312-147">Vanha arvo</span><span class="sxs-lookup"><span data-stu-id="e1312-147">Old value</span></span>
    - <span data-ttu-id="e1312-148">Uusi arvo</span><span class="sxs-lookup"><span data-stu-id="e1312-148">New value</span></span>
    - <span data-ttu-id="e1312-149">Muokannut</span><span class="sxs-lookup"><span data-stu-id="e1312-149">Modified by</span></span>

1. <span data-ttu-id="e1312-150">Kun muutokset on tehty ja julkaistu, valitse **Synkronoi tilaus**, jos haluat aloittaa synkronointiprosessin heti.</span><span class="sxs-lookup"><span data-stu-id="e1312-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="e1312-151">Vaihtoehtoisesti voit odottaa, että erätilassa suoritettava synkronointiprosessi käsittelee tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="e1312-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="e1312-152">Kun tilaukset on synkronoitu, ne asetetaan oletusarvoisesti estotilaan Commerce-parametrien määrittämän estokoodin mukaan.</span><span class="sxs-lookup"><span data-stu-id="e1312-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="e1312-153">Tilausten esto on poistettava, ennen kuin tilaukset voidaan käsitellä edelleen tilauksen täyttämistä tai muuta toimintoa varten.</span><span class="sxs-lookup"><span data-stu-id="e1312-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1312-154">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e1312-154">Additional resources</span></span>

[<span data-ttu-id="e1312-155">Kassanhallinnan ja itsepalvelutukun hallintatapahtumien muokkaaminen ja tarkastaminen</span><span class="sxs-lookup"><span data-stu-id="e1312-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="e1312-156">Vähittäismyyntitapahtumien taloushallinnon dimensioiden muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e1312-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="e1312-157">Excel-työkirjan luominen vähittäismyyntitapahtumien muokkaamista varten</span><span class="sxs-lookup"><span data-stu-id="e1312-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="e1312-158">Kenttien lisääminen Excel-työkirjaan vähittäismyyntitapahtumien muokkaamista varten</span><span class="sxs-lookup"><span data-stu-id="e1312-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]