---
title: Luotonvalvonnan yleiskatsaus
description: Tässä ohjeaiheessa on luotonvalvonnan toimintojen yleiskatsaus.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 67e0b3d1058e5fc085f51577ccf0b79e51546de0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442737"
---
# <a name="credit-and-collections-overview"></a><span data-ttu-id="0b247-103">Luotonvalvonnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0b247-103">Credit and collections overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b247-104">Voit hallita asiakkaiden luottorajoja ja suorittaa tarvittaessa perintätehtäviä.</span><span class="sxs-lookup"><span data-stu-id="0b247-104">You can manage credit limits for your customers and perform collection activities when they become necessary.</span></span>

## <a name="credit-management"></a><span data-ttu-id="0b247-105">Luotonhallinta</span><span class="sxs-lookup"><span data-stu-id="0b247-105">Credit management</span></span>

<span data-ttu-id="0b247-106">Asiakkaan luotonhallinnan avulla voit hallita luottorajoja ja hallita myyntitilausten siirtymistä kirjausprosessissa luotujen luottosääntöjen perusteella.</span><span class="sxs-lookup"><span data-stu-id="0b247-106">Customer credit management lets you manage credit limits and control the flow of sales orders through the posting process, based on credit rules that you create.</span></span>

<span data-ttu-id="0b247-107">Luotonhallintaprosessi voi sisältää seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="0b247-107">The credit management process can include any of the following steps:</span></span>

- <span data-ttu-id="0b247-108">Lisätietoja asiakkaan luottokelpoisuudesta antavien luottomääritteiden päivittäminen.</span><span class="sxs-lookup"><span data-stu-id="0b247-108">Update credit attributes for customers to provide additional information about their credit worthiness.</span></span>
- <span data-ttu-id="0b247-109">Luottorajojen luonti asiakkaille käyttämällä luottorajan oikaisuja.</span><span class="sxs-lookup"><span data-stu-id="0b247-109">Create credit limits for customers by using credit limit adjustments.</span></span>
- <span data-ttu-id="0b247-110">Väliaikaisten luottorajojen luonti asiakkaille käyttämällä luottorajan oikaisuja.</span><span class="sxs-lookup"><span data-stu-id="0b247-110">Create temporary credit limits for customers by using credit limit adjustments.</span></span> <span data-ttu-id="0b247-111">Tällä tavoin luottorajaa voidaan nostaa tai laskea väliaikaisesti liiketoimintatarpeiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="0b247-111">In this way, you can temporarily increase or decrease customer credit limits, based on business requirements.</span></span>
- <span data-ttu-id="0b247-112">Luottorajaan mahdollisesti vaikuttavien tietojen, kuten vakuus- tai takaustietojen, lisääminen.</span><span class="sxs-lookup"><span data-stu-id="0b247-112">Add information that can affect the credit limit, such as information about insurance and guarantees.</span></span>
- <span data-ttu-id="0b247-113">Asiakkaat yhteen liittävien asiakkaan luottoryhmien luominen siten, että ne voivat jakaa yhden luottorajan.</span><span class="sxs-lookup"><span data-stu-id="0b247-113">Create customer credit groups that link customers together so that they share a single credit limit.</span></span>
- <span data-ttu-id="0b247-114">Riskipisteiden määrittäminen asiakkaille ja näiden pistemäärien käyttäminen luomaan luottorajoja kyseisille asiakkaille automaattisesti luottorajan oikaisujen avulla.</span><span class="sxs-lookup"><span data-stu-id="0b247-114">Assign risk scores to customers, and then use the scores to automatically generate credit limits for those customers through credit limit adjustments.</span></span>
- <span data-ttu-id="0b247-115">Estosääntöjen luominen asettamaan tilaus pitoon jonkin kirjausprosessin aikana esimerkiksi seuraavien seikkojen perusteella: riski, maksuehdot, luottorajat, erääntyneet summat ja käytetyn luottorajan prosenttiosuus.</span><span class="sxs-lookup"><span data-stu-id="0b247-115">Create blocking rules that put an order on hold during one or more posting processes, based on factors such as risk, payment terms, credit limits, overdue amounts, and the percentage of the credit limit that has been used.</span></span>
- <span data-ttu-id="0b247-116">Pidossa olevien myyntitilausluettelon hallinta, pitosyiden tarkastelu ja ongelmien ratkaiseminen.</span><span class="sxs-lookup"><span data-stu-id="0b247-116">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate issues.</span></span>
- <span data-ttu-id="0b247-117">Myyntitilausten vapauttaminen ja niiden jatkaminen kirjausprosessin läpi.</span><span class="sxs-lookup"><span data-stu-id="0b247-117">Release sales orders so that they continue through the posting process.</span></span>
- <span data-ttu-id="0b247-118">Työnkulun määrittäminen hallitsemaan luottorajan muutosten ja myyntitilausten vapauttamisen hyväksymistä.</span><span class="sxs-lookup"><span data-stu-id="0b247-118">Set up a workflow to manage the approval of credit limit changes and sales order releases.</span></span>

## <a name="collections-management"></a><span data-ttu-id="0b247-119">Perinnän hallinta</span><span class="sxs-lookup"><span data-stu-id="0b247-119">Collections management</span></span>

<span data-ttu-id="0b247-120">**Perintä**-sivu on keskitetty näkymä myyntireskontran perimistietojen hallitaan.</span><span class="sxs-lookup"><span data-stu-id="0b247-120">The **Collections** page provides a centralized view where accounts receivable collections information is managed.</span></span> <span data-ttu-id="0b247-121">Perintäjohtajat voivat hallita perintää tästä keskitetystä näkymästä.</span><span class="sxs-lookup"><span data-stu-id="0b247-121">Collections managers can use this centralized view to manage collections.</span></span> <span data-ttu-id="0b247-122">Perimisasiamiehet voivat aloittaa perintäprosessin joko ennalta määritettyjen ehtojen mukaan muodostettavasta asiakasluettelosta tai **Asiakkaat**-sivulta.</span><span class="sxs-lookup"><span data-stu-id="0b247-122">Collections agents can begin the collections process either from customer lists that are generated by using predefined collection criteria or from the **Customers** page.</span></span>

<span data-ttu-id="0b247-123">Ennen kuin aloitat perinnän määrittämisen tai perinnän käyttämisen, on hyvä ymmärtää seuraavat käsitteet:</span><span class="sxs-lookup"><span data-stu-id="0b247-123">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="0b247-124">Asiakkaan erääntymistilannevedokset sisältävät erääntyneet saldotiedot tietyltä aikajaksolta.</span><span class="sxs-lookup"><span data-stu-id="0b247-124">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="0b247-125">Perinnän asiakaspoolit helpottavat työn organisointia.</span><span class="sxs-lookup"><span data-stu-id="0b247-125">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="0b247-126">Perimisasiamiehet voivat ylläpitää omia asiakaspoolejaan.</span><span class="sxs-lookup"><span data-stu-id="0b247-126">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="0b247-127">Luettelosivuilla voi järjestää perinnän asiakkaita, tehtäviä ja tapauksia.</span><span class="sxs-lookup"><span data-stu-id="0b247-127">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="0b247-128">Kaikki asiakkaan perintätiedot yhdellä sivulla, jolta voit ryhtyä toimenpiteisiin.</span><span class="sxs-lookup"><span data-stu-id="0b247-128">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="0b247-129">Korkojen ja maksujen peruuttaminen, palauttaminen tai kääntäminen yhdellä toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="0b247-129">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="0b247-130">Poistotapahtumia voidaan luoda yhdessä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="0b247-130">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="0b247-131">Ei katetta (NSF) -maksut voidaan käsitellä yhdessä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="0b247-131">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="0b247-132">Näiden käsitteiden kuvaukset ovat kohdassa [Perinnän hallinnan keskeiset käsitteet](./cm-collections-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="0b247-132">For descriptions of these concepts, see [Collections management key concepts](./cm-collections-concepts.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b247-133">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0b247-133">Additional resources</span></span>

[<span data-ttu-id="0b247-134">Asiakkaan luotonhallinnan parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0b247-134">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="0b247-135">Asiakkaan luotonhallinnan määritystiedot</span><span class="sxs-lookup"><span data-stu-id="0b247-135">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="0b247-136">Asiakkaan luotonhallintatietojen lisääminen</span><span class="sxs-lookup"><span data-stu-id="0b247-136">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="0b247-137">Asiakasluottoryhmät</span><span class="sxs-lookup"><span data-stu-id="0b247-137">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="0b247-138">Asiakkaan luottorajan oikaisut</span><span class="sxs-lookup"><span data-stu-id="0b247-138">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="0b247-139">Myyntitilausten luottorajapidot</span><span class="sxs-lookup"><span data-stu-id="0b247-139">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="0b247-140">Asiakkaan luotonhallinnan kausittaiset tehtävät</span><span class="sxs-lookup"><span data-stu-id="0b247-140">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)
