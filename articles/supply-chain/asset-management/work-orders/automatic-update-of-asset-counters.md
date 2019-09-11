---
title: Resurssilaskureiden automaattinen päivitys
description: Tässä ohjeaiheessa kuvataan resurssilaskureiden automaattista päivitystä resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875637"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="c9627-103">Resurssilaskureiden automaattinen päivitys</span><span class="sxs-lookup"><span data-stu-id="c9627-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c9627-104">Edellisessä osassa on kuvattu käyttöomaisuuslaskureiden manuaalinen rekisteröiminen.</span><span class="sxs-lookup"><span data-stu-id="c9627-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="c9627-105">Käyttöomaisuuslaskureiden määritys on kuvattu [Laskurit](../setup-for-objects/counters.md)-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="c9627-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="c9627-106">Laskuriarvot voidaan päivittää myös automaattisesti tuotantorekisteröinneistä tuotantotuntien tai tuotantomäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="c9627-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="c9627-107">Tämä tehdään kohdassa **Päivitä resurssilaskurit**.</span><span class="sxs-lookup"><span data-stu-id="c9627-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="c9627-108">Voit päivittää yhden tai useita käyttöomaisuuksia lisäämällä yhden parametrin (**Alkamispäivämäärä**).</span><span class="sxs-lookup"><span data-stu-id="c9627-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="c9627-109">Tämä parametri määrittää tuotantorekisteröintien alkamispäivän (tunnit tai tuotetut määrät) eli alkamispäivämäärän, josta lähtien laskurin arvot päivitetään.</span><span class="sxs-lookup"><span data-stu-id="c9627-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="c9627-110">Kaikki resurssit, jotka liittyvät resurssiin *ja* joilla on käyttöomaisuuslaskurit, jotka on määritetty päivitettäviksi tuotetun määrän tai tuotantotuntien perusteella, sisällytetään automaattiseen päivitykseen ja uudet laskuriarvot luodaan.</span><span class="sxs-lookup"><span data-stu-id="c9627-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="c9627-111">Liittyvät, tuotantomäärään, hyvään tuotantomäärään ja huonoon tuotantomäärään perustuvat laskurit, sisällytetään laskentaan.</span><span class="sxs-lookup"><span data-stu-id="c9627-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="c9627-112">Jos tuotetun määrän rekisteröinnissä käytettävä yksikkö poikkeaa laskussa käytetystä yksiköstä, määrä muunnetaan vastaamaan laskuriyksikköä.</span><span class="sxs-lookup"><span data-stu-id="c9627-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="c9627-113">Kuten edellä mainittiin, automaattiset laskurit voidaan päivittää tuotannon rekisteröinneistä.</span><span class="sxs-lookup"><span data-stu-id="c9627-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="c9627-114">Siksi käyttöomaisuuserän, jonka laskurit haluat päivittää automaattisesti, on oltava yhteydessä resurssiin (koneeseen).</span><span class="sxs-lookup"><span data-stu-id="c9627-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="c9627-115">Seuraavissa kuvauksissa on yhteenveto tuotantotilausten asetuksista ja käsittelystä (**Tuotannonhallinta**-moduulissa), jota käytetään käyttöomaisuuserän laskureiden automaattisen päivityksen pohjana **Resurssien hallinta** -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="c9627-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="c9627-116">Kun resurssille on rekisteröity tuotettuja määriä tai tuotantotunteja, voit päivittää liittyvät käyttöomaisuuslaskurit.</span><span class="sxs-lookup"><span data-stu-id="c9627-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="c9627-117">Valitse **resurssien hallinta** > **Kausittainen** > **resurssit** > **Päivitä resurssilaskurit**.</span><span class="sxs-lookup"><span data-stu-id="c9627-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="c9627-118">Valitse automaattisen päivityksen aloituspäivämäärä **Aloituspäivämäärä**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="c9627-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="c9627-119">Tämän kentän päivämäärä on "keskeneräiset työt" -päivämäärä kohdasta **Reititystapahtumat** (**Tuotannonhallinta** > **Kyselyt ja raportit** > **Tuotanto** > **Reititystapahtumat** > **Fyysinen päivämäärä** -kenttä).</span><span class="sxs-lookup"><span data-stu-id="c9627-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="c9627-120">Jos haluat määrittää tiettyjen resurssien, resurssityyppien tai kohderesurssien automaattiset päivitykset valitsemalla **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** ja valitse sitten haluamasi kohteet.</span><span class="sxs-lookup"><span data-stu-id="c9627-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="c9627-121">**Suorita taustalla** -pikavälilehdessä voit määrittää automaattisen päivityksen erätyönä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="c9627-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![Kuva 1](media/12-work-orders.png)

5. <span data-ttu-id="c9627-123">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9627-123">Click **OK**.</span></span> <span data-ttu-id="c9627-124">Kun automaattinen käyttöomaisuuslaskurin päivitys on valmis, voit nähdä käyttöomaisuuteen liittyvät laskurirekisteröinnit kohdassa **Resurssilaskurit** (**Resurssien hallinta** > **Yhteiset** > **Resurssit** > **Kaikki resurssit** > valitse käyttöomaisuus > **Laskurit**-painike).</span><span class="sxs-lookup"><span data-stu-id="c9627-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="c9627-125">Kohdassa **Resurssilaskurien kokonaissumma**voit saada yleiskuvan kaikkien omaisuuserien kaikkien laskurityyppien viimeisimmistä rekisteröinneistä.</span><span class="sxs-lookup"><span data-stu-id="c9627-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="c9627-126">Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssit** > **Resurssien koostettu arvo**.</span><span class="sxs-lookup"><span data-stu-id="c9627-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="c9627-127">Näkymä on hyvin samankaltainen kuin **Resurssilaskurit**, mutta et voi lisätä tai muokata **Resurssien koostettu arvo** -kohdan rekisteröintejä.</span><span class="sxs-lookup"><span data-stu-id="c9627-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="c9627-128">Se on vain yleiskatsausta varten.</span><span class="sxs-lookup"><span data-stu-id="c9627-128">It is for overview only.</span></span>

![Kuva 2](media/13-work-orders.png)


- <span data-ttu-id="c9627-130">On edelleen mahdollista luoda manuaaliset laskuriarvon rekisteröinnit automaattisesti päivitettäviä laskurityyppejä varten.</span><span class="sxs-lookup"><span data-stu-id="c9627-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="c9627-131">Lisätietoja on Resurssilaskureiden manuaalinen päivitys-osassa.</span><span class="sxs-lookup"><span data-stu-id="c9627-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="c9627-132">Voit määrittää toiseen laskuriin liittyviä laskureita, mikä tarkoittaa, että kun laskuri päivitetään, siihen liittyvät laskurit päivitetään automaattisesti samaan aikaan.</span><span class="sxs-lookup"><span data-stu-id="c9627-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="c9627-133">Lisätietoja liittyvien laskurien määrittämisestä on kohdassa [Laskurit](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="c9627-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
