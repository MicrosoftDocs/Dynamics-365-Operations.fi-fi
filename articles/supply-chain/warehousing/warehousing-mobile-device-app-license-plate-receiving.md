---
title: Rekisterikilpi, joka vastaanottaa Warehousing mobile appin kautta
description: Tässä ohjeaiheessa selitetään, kuinka Warehousing Mobile App määritetään tukemaan rekisterikilven vastaanottoprosessin käyttöä fyysisen varaston vastaanottamiseen.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 98cd608edea1d5365d0d3532244f1fcdb6293d3c
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261326"
---
# <a name="license-plate-receiving-via-the-warehousing-mobile-app"></a><span data-ttu-id="85a48-103">Rekisterikilpi, joka vastaanottaa Warehousing mobile appin kautta</span><span class="sxs-lookup"><span data-stu-id="85a48-103">License plate receiving via the Warehousing mobile app</span></span>

<span data-ttu-id="85a48-104">Tässä ohjeaiheessa selitetään, kuinka Warehousing Mobile App määritetään niin ,että se tukee rekisterikilven vastaanottoprosessin käyttöä fyysisen varaston vastaanottamiseen.</span><span class="sxs-lookup"><span data-stu-id="85a48-104">This topic explains how to set up the Warehousing mobile app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="85a48-105">Tämän toiminnon avulla voit nopeasti kirjata saapuvaa varastoa koskevan vastaanoton, joka liittyy ennakkoilmoitukseen (ASN).</span><span class="sxs-lookup"><span data-stu-id="85a48-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="85a48-106">Järjestelmä luo automaattisesti ASN-arvon, kun siirtotilauksen lähetys suoritetaan varastoinnin hallintaprosessien avulla.</span><span class="sxs-lookup"><span data-stu-id="85a48-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="85a48-107">Ostotilausprosessin aikana ASN voidaan tallentaa manuaalisesti, tai se voidaan tuoda automaattisesti käyttämällä saapuvan ASN-tietoyksikkö prosessia.</span><span class="sxs-lookup"><span data-stu-id="85a48-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="85a48-108">ASN-tiedot linkitetään kuormiin ja lähetyksiin *pakkausrakenteiden*kautta, joissa kuormalavat (päärekisterikilvet) voivat sisältää palvelupyyntöjä (sisäkkäisiä rekisterikilpiä).</span><span class="sxs-lookup"><span data-stu-id="85a48-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="85a48-109">Kun käytetään sisäkkäisten rekisterikilpien pakkausrakenteita, järjestelmä tallentaa varastotapahtumien määrän pääkäyttöoikeusrekisterikilpeen.</span><span class="sxs-lookup"><span data-stu-id="85a48-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="85a48-110">Jos haluat käynnistää fyysisen käytettävissä olevan varaston siirtämisen pääkäyttöoikeusrekisterikilvestä sisäkkäisiin rekisteritietoihin perustuen, mobiililaitteen on määritettävä pakkausrakenteen tietojen perusteella valikkovaihtoehto, joka perustuu *pakkauksen sisäkkäinen rekisterikilpi* -töiden luomisprosessiin.</span><span class="sxs-lookup"><span data-stu-id="85a48-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="85a48-111">Vastaanottavan yhteenvetosivun näyttäminen tai ohittaminen</span><span class="sxs-lookup"><span data-stu-id="85a48-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="85a48-112">Voit käyttää *ohjausobjektia, näytetäänkö vastaanottavan yhteenvetosivun mobiililaitteissa* -ominaisuutta, jotta saat lisätietoja fyysisen varastoinnin sovelluskulusta osana rekisterikilven vastaanottoprosessia.</span><span class="sxs-lookup"><span data-stu-id="85a48-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed Warehouse app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="85a48-113">Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="85a48-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="85a48-114">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="85a48-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="85a48-115">**Ominaisuuksien hallinta** -työtilassa tämä ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="85a48-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="85a48-116">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="85a48-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="85a48-117">**Ominaisuuden nimi:** *Määrittää, näytetäänkö vastaanottava yhteenvetosivu mobiililaitteissa*</span><span class="sxs-lookup"><span data-stu-id="85a48-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="85a48-118">Kun tämä toiminto on otettu käyttöön, kannettavien laitteiden valikkokohteet, jotka koskevat rekisteritietoja tai rekisterikilven vastaanottoa ja hyllytystä, sisältävät **näytön vastaanottamisen yhteenvetosivu** -asetuksen.</span><span class="sxs-lookup"><span data-stu-id="85a48-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="85a48-119">Tällä asetuksella on seuraavat vaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="85a48-119">This setting has the following options:</span></span>

- <span data-ttu-id="85a48-120">**Näytä yksityiskohtainen yhteenveto** – Rekisterikilven vastaanottamisen aikana työntekijät näkevät ylimääräisen sivun, jossa näkyvät kaikki ASN-tiedot.</span><span class="sxs-lookup"><span data-stu-id="85a48-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="85a48-121">**Ohita yhteenveto** – Työntekijät eivät näe kaikkia ASN-tietoja.</span><span class="sxs-lookup"><span data-stu-id="85a48-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="85a48-122">Varastotyöntekijät eivät voi määrittää käsittelykoodia tai lisätä poikkeuksia vastaanottoprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="85a48-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="85a48-123">Estä siirtotilauksen lähettämien rekisterikilpien käyttö muissa varastoissa kuin kohdevarastossa</span><span class="sxs-lookup"><span data-stu-id="85a48-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="85a48-124">Rekisterikilven vastaanottoprosessia ei voi käyttää, jos ASN sisältää rekisterikilven tunnuksen, joka on jo olemassa ja jolla on fyysisiä käytettävissä olevia tietoja varastosijainnissa, joka ei ole sama kuin varastosijainti, jossa rekisterikilpi rekisteröidään.</span><span class="sxs-lookup"><span data-stu-id="85a48-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="85a48-125">Siirtotilausten tapauksissa, joissa kuljetusvarasto ei jäljitä rekisterikilpiä (eikä näin ollen myöskään kirjaa fyysistä käytettävissä olevaa varastoa rekisterikilpeä kohden), voit käyttää *Estä siirtotilauksen mukana toimitettuja rekisterikilpiä käytettäväksi muissa varastoissa kuin kohdevarastossa* -toimintoa, joka estää kauttakuljetuksessa olevien rekisterikilpien fyysisten käytettävissä olevien päivitysten käytön.</span><span class="sxs-lookup"><span data-stu-id="85a48-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="85a48-126">Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="85a48-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="85a48-127">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="85a48-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="85a48-128">**Ominaisuuksien hallinta** -työtilassa tämä ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="85a48-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="85a48-129">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="85a48-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="85a48-130">**Ominaisuuden nimi:** *Estä siirtotilauksen lähettämien rekisterikilpien käyttö muissa varastoissa kuin kohdevarastossa*</span><span class="sxs-lookup"><span data-stu-id="85a48-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="85a48-131">Voit hallita toimintoja, kun tämä toiminto on käytettävissä, noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="85a48-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="85a48-132">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="85a48-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="85a48-133">Määritä **Yleinen**-välilehden **Rekisterikilvet**-pikavälilehdessä, että **Kuljetusvaraston rekisterikilpikäytäntö** -kenttä on jokin seuraavista arvoista:</span><span class="sxs-lookup"><span data-stu-id="85a48-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="85a48-134">**Salli ei-seurattujen rekisterikilpien uudelleenkäyttö** – Järjestelmä toimii samalla tavalla kuin se toimii, kun *Estä siirtotilauksen toimittamien rekisterikilpien käyttö muissa varastoissa kuin kohdevarasto* -toiminto ei ole käytössä.</span><span class="sxs-lookup"><span data-stu-id="85a48-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="85a48-135">Tämä arvo on oletusasetus, kun aktivoit ominaisuuden ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="85a48-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="85a48-136">**Ei-seuratun rekisterikilven uudelleenkäytön estäminen** – Kohdevarastossa sallitaan vain käytettävissä olevat päivitykset, jotka liittyvät toimitettuun rekisterikilpeen, kunnes siirtotilaus on vastaanotettu.</span><span class="sxs-lookup"><span data-stu-id="85a48-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="85a48-137">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="85a48-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="85a48-138">Lisätietoja mobiililaitteiden valikkokohteista on kohdassa [Mobiililaitteiden määrittäminen varastotyötä varten](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="85a48-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
