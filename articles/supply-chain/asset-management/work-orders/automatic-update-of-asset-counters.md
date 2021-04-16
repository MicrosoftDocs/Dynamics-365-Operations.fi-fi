---
title: Resurssilaskureiden automaattinen päivitys
description: Tässä ohjeaiheessa kuvataan resurssilaskureiden automaattista päivitystä resurssien hallinnassa.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f15aea2f867de6f0bcf01ecfd046efc44581a1ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820439"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="90b1d-103">Resurssilaskureiden automaattinen päivitys</span><span class="sxs-lookup"><span data-stu-id="90b1d-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90b1d-104">Katso lisätietoja resurssilaskureiden manuaalisesta rekisteröinnistä kohdasta [Resurssilaskureiden manuaalinen päivitys](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="90b1d-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="90b1d-105">Lisätietoja resurssilaskureiden määrittämisestä esitetään kohdassa [Laskurit](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="90b1d-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="90b1d-106">Laskuriarvot voidaan päivittää myös automaattisesti tuotantorekisteröinneistä tuotantotuntien tai tuotantomäärän (eli tuotetun määrän) perusteella.</span><span class="sxs-lookup"><span data-stu-id="90b1d-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="90b1d-107">Tämä päivitys suoritetaan **Päivitä resurssilaskurit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="90b1d-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="90b1d-108">Voit päivittää yhden tai useita käyttöomaisuuksia määrittämällä yhden parametrin (**Alkamispäivämäärä**).</span><span class="sxs-lookup"><span data-stu-id="90b1d-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="90b1d-109">Tämä parametri määrittää tuotantorekisteröintien (tuotantotuntien tai tuotantomäärien) aloituspäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="90b1d-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="90b1d-110">Toisin sanoen se määrittää, mistä päivämäärästä alkaen laskureiden arvoja päivitetään.</span><span class="sxs-lookup"><span data-stu-id="90b1d-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="90b1d-111">Kaikki resurssit, jotka liittyvät resurssiin *ja* joilla on resurssilaskurit, jotka on määritetty päivitettäviksi tuotetun määrän tai tuotantotuntien perusteella, sisällytetään automaattiseen päivitykseen.</span><span class="sxs-lookup"><span data-stu-id="90b1d-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="90b1d-112">Uudet laskuriarvot luodaan.</span><span class="sxs-lookup"><span data-stu-id="90b1d-112">New counter values will be created.</span></span>

<span data-ttu-id="90b1d-113">Tuotantomäärään perustuvien laskureiden osalta määrään sisältyvät sekä rekisteröity tavaramäärä että rekisteröity virhemäärä.</span><span class="sxs-lookup"><span data-stu-id="90b1d-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="90b1d-114">Jos tuotantomäärän rekisteröinnissä käytettävä yksikkö eroaa määrään käytettävän laskurin yksiköstä, määrä muunnetaan vastaamaan laskurin yksikköä.</span><span class="sxs-lookup"><span data-stu-id="90b1d-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="90b1d-115">Kuten edellä mainittiin, automaattiset laskurit voidaan päivittää tuotannon rekisteröinneistä.</span><span class="sxs-lookup"><span data-stu-id="90b1d-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="90b1d-116">Siksi käyttöomaisuuserän, jonka laskurit haluat päivittää automaattisesti, on oltava yhteydessä resurssiin (koneeseen).</span><span class="sxs-lookup"><span data-stu-id="90b1d-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="90b1d-117">Kun resurssille on rekisteröity tuotettuja määriä tai tuotantotunteja, voit päivittää liittyvät käyttöomaisuuslaskurit.</span><span class="sxs-lookup"><span data-stu-id="90b1d-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="90b1d-118">Valitse **Resurssienhallinta** > **Kausittainen** > **Resurssit** > **Päivitä resurssilaskurit**.</span><span class="sxs-lookup"><span data-stu-id="90b1d-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="90b1d-119">Valitse automaattisen päivityksen aloituspäivämäärä **Aloituspäivämäärä**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="90b1d-119">In the **From date** field, select the start date of the automatic update.</span></span>

    >[!NOTE]
    ><span data-ttu-id="90b1d-120">Tämän kentän päivämäärä on "keskeneräiset työt" -päivämäärä kohdasta **Reititystapahtumat** (**Tuotannonhallinta** > **Kyselyt ja raportit** > **Tuotanto** > **Reititystapahtumat** > **Fyysinen päivämäärä** -kenttä).</span><span class="sxs-lookup"><span data-stu-id="90b1d-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="90b1d-121">**Sisällytettävät tietueet** -pikavälilehdellä voit valita tiettyjä resursseja tai resurssityyppejä automaattisesti päivitettäväksi.</span><span class="sxs-lookup"><span data-stu-id="90b1d-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="90b1d-122">Tee tarvittavat valinnat ja valitse **Suodata**.</span><span class="sxs-lookup"><span data-stu-id="90b1d-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="90b1d-123">**Suorita taustalla** -pikavälilehdessä voit määrittää automaattisen päivityksen erätyönä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="90b1d-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

    <span data-ttu-id="90b1d-124">Seuraavassa kuvassa on esimerkki **Päivitä resurssilaskurit** -valintaikkunasta.</span><span class="sxs-lookup"><span data-stu-id="90b1d-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

    ![Kuva 1](media/12-work-orders.png)

5. <span data-ttu-id="90b1d-126">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="90b1d-126">Select **OK**.</span></span> 

<span data-ttu-id="90b1d-127">Kun automaattinen resurssilaskureiden päivitys on tehty, voit tarkastella resurssiin liittyviä laskurirekisteröintejä **Resurssilaskurit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="90b1d-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="90b1d-128">Valitse **Resurssienhallinta** > **Yhteiset** > **Resurssit** > **Kaikki resurssit**, valitse resurssit ja valitse sitten **Laskurit** toimintoruudun **Ennaltaehkäisevä**-ryhmän **Resurssit**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="90b1d-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="90b1d-129">Sivulta **Resurssilaskurien kokonaissumma** voit saada yleiskuvan kaikkien resurssien kaikkien laskurityyppien viimeisimmistä rekisteröinneistä.</span><span class="sxs-lookup"><span data-stu-id="90b1d-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="90b1d-130">Valitse **Resurssienhallinta** > **Kyselyt** > **Resurssit** > **Resurssien koostettu arvo**.</span><span class="sxs-lookup"><span data-stu-id="90b1d-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="90b1d-131">Tämä sivu muistuttaa sivua **Resurssilaskurit**, mutta et voi lisätä tai muokata rekisteröintejä.</span><span class="sxs-lookup"><span data-stu-id="90b1d-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="90b1d-132">Se on vain yleiskatsausta varten.</span><span class="sxs-lookup"><span data-stu-id="90b1d-132">It's for overview only.</span></span>

<span data-ttu-id="90b1d-133">Seuraavassa kuvassa on esimerkki **Resurssien koostettu arvo** -sivusta.</span><span class="sxs-lookup"><span data-stu-id="90b1d-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![Kuva 2](media/13-work-orders.png)

<span data-ttu-id="90b1d-135">Huomaa seuraavat seikat:</span><span class="sxs-lookup"><span data-stu-id="90b1d-135">Note the following points:</span></span>

- <span data-ttu-id="90b1d-136">Voit edelleen luoda manuaalisia laskuriarvon rekisteröintejä automaattisesti päivitettäviä laskurityyppejä varten.</span><span class="sxs-lookup"><span data-stu-id="90b1d-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="90b1d-137">Lisätietoja on kohdassa [Resurssilaskureiden manuaalinen päivitys](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="90b1d-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="90b1d-138">Voit määrittää toisiin laskureihin liittyviä laskureita.</span><span class="sxs-lookup"><span data-stu-id="90b1d-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="90b1d-139">Tällöin liittyvät laskurit päivitetään automaattisesti samalla kun päälaskuri päivitetään.</span><span class="sxs-lookup"><span data-stu-id="90b1d-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="90b1d-140">Lisätietoja resurssilaskureiden määrittämisestä esitetään kohdassa [Laskurit](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="90b1d-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]