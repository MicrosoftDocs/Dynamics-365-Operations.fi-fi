---
title: Käyttöomaisuuserien liittäminen vuokrasopimuksiin
description: Tässä ohjeaiheessa kerrotaan, miten aiemmin luotu käyttöomaisuuserä liitetään uuteen vuokrasopimukseen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d627633e43c2e6f5cad90dfe4100ff95a71541f7
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442974"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="0e05a-103">Käyttöomaisuuserien liittäminen vuokrasopimuksiin</span><span class="sxs-lookup"><span data-stu-id="0e05a-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e05a-104">Tässä ohjeaiheessa kerrotaan, miten aiemmin luotu käyttöomaisuuserä liitetään uuteen vuokrasopimukseen.</span><span class="sxs-lookup"><span data-stu-id="0e05a-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="0e05a-105">Kun liität käyttöomaisuuserän vuokrasopimukseen, käyttöoikeusomaisuuserän arvo alkuperäisen tuloutuksen aikana on käyttöomaisuuserän hankintakustannus.</span><span class="sxs-lookup"><span data-stu-id="0e05a-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="0e05a-106">Ennen kuin voit liittää käyttöomaisuuserän vuokrasopimukseen, sinun on luotava käyttöomaisuuserälle tietue Käyttöomaisuuserät-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="0e05a-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="0e05a-107">Tämän jälkeen luodaan vuokrasopimus ja linkitetään siihen resurssi **Vuokrasopimusyhteenveto**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="0e05a-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="0e05a-108">Lisää vuokrasopimus noudattamalla kohdan [Lisää tai kopioi vuokrasopimukset](add-lease.md) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="0e05a-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="0e05a-109">Valitse **Lisää vuokrasopimus** -sivun **Käyttöomaisuusnumero**-kentässä resurssi, jota ei ole vielä hankittu.</span><span class="sxs-lookup"><span data-stu-id="0e05a-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="0e05a-110">Valitse **Kirjat** ja vahvista maksuaikataulu.</span><span class="sxs-lookup"><span data-stu-id="0e05a-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="0e05a-111">Valitse **Alkuperäinen tunnustaminen**.</span><span class="sxs-lookup"><span data-stu-id="0e05a-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="0e05a-112">Valitse **Resurssin leasingkirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="0e05a-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="0e05a-113">Vuokrasopimuksen alkuperäinen tuloutuksen kirjauskansiovienti veloittaa summasta käyttöomaisuuden, joka yleensä veloitetaan käyttöoikeusomaisuuserän tililtä.</span><span class="sxs-lookup"><span data-stu-id="0e05a-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="0e05a-114">Voit nyt tarkastella käyttöomaisuuserän tapahtumatyyppiä ja kirjaa.</span><span class="sxs-lookup"><span data-stu-id="0e05a-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="0e05a-115">Valitse **Kirjauskansion tiedot**.</span><span class="sxs-lookup"><span data-stu-id="0e05a-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="0e05a-116">Valitse **Rivit**, jos haluat tarkastella kirjauskansioviennin yksittäisiä rivejä.</span><span class="sxs-lookup"><span data-stu-id="0e05a-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="0e05a-117">Valitse resurssin sisältävä kirjauskansiorivi ja valitse sitten **Käyttöomaisuuserät**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="0e05a-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="0e05a-118">**Käyttöomaisuuserät**-välilehdessä näkyy tapahtumatyyppi ja kirja.</span><span class="sxs-lookup"><span data-stu-id="0e05a-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="0e05a-119">Oletusarvoisesti **Tapahtumatyyppi**-kentän arvoksi on määritetty **Hankinta** ja **Kirja**-kentän arvoksi käyttöomaisuuden nykyinen kirja.</span><span class="sxs-lookup"><span data-stu-id="0e05a-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="0e05a-120">Kun olet kirjannut alkuperäisen tuloutuksen kirjauskansioviennin, tapahtuma näkyy käyttöomaisuuserän hankintatapahtumana.</span><span class="sxs-lookup"><span data-stu-id="0e05a-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="0e05a-121">Voit tarkastella tapahtumataulukkoa siirtymällä kohtaan **Käyttöomaisuuserät \> Käyttöomaisuuserät \> Käyttöomaisuuserät**, valitsemalla soveltuvan käyttöomaisuuden ja valitsemalla sitten **Arvostukset**.</span><span class="sxs-lookup"><span data-stu-id="0e05a-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="0e05a-122">Näet, että alkuperäinen tuloutuksen kirjauskansiovienti on luonut määritetyn käyttöomaisuuserän hankintatapahtuman.</span><span class="sxs-lookup"><span data-stu-id="0e05a-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="0e05a-123">Käyttöomaisuus voidaan nyt poistaa Käyttöomaisuuserät-kohdan vakiopoistotoimintojen avulla.</span><span class="sxs-lookup"><span data-stu-id="0e05a-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="0e05a-124">Lisätietoja poistosta on kohdassa [Poistomenetelmät ja -käytännöt](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="0e05a-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="0e05a-125">Jos käyttöomaisuus liitetään vuokrasopimukseen, **Resurssin poisto** ja **Vuokrasopimuksen arvonalennus** -painikkeet eivät ole käytössä resurssin vuokrauksessa.</span><span class="sxs-lookup"><span data-stu-id="0e05a-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="0e05a-126">Voit tarkastella resurssin poistoa ja vuokrasopimuksen arvonalennustapahtumia Käyttöomaisuuserät-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="0e05a-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="0e05a-127">**Resurssitapahtumat**-painike, joka avaa kyselylomakkeen, on myös poistettu käytöstä.</span><span class="sxs-lookup"><span data-stu-id="0e05a-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="0e05a-128">Voit avata myös **Resurssitapahtumat**-kyselyn Käyttöomaisuuserät-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="0e05a-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  
