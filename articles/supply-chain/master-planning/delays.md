---
title: Viiveet
description: Tässä ohjeaiheessa on tietoja pääsuunnittelun viivästyspäivistä. Viivästyspäivä on realistinen eräpäivä, jonka tapahtuma saa, jos pääsuunnittelun laskema aikaisin toimituspäivä on myöhempi kuin pyydetty päivämäärä.
author: roxanadiaconu
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4216ed1d9b981eee94cfd4c621abd1da99111512
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813672"
---
# <a name="delays"></a><span data-ttu-id="653c1-104">Viiveet</span><span class="sxs-lookup"><span data-stu-id="653c1-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="653c1-105">Tässä ohjeaiheessa on tietoja pääsuunnittelun viivästyspäivistä.</span><span class="sxs-lookup"><span data-stu-id="653c1-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="653c1-106">Viivästyspäivä on realistinen eräpäivä, jonka tapahtuma saa, jos pääsuunnittelun laskema aikaisin toimituspäivä on myöhempi kuin pyydetty päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="653c1-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="653c1-107">Pääsuunnittelu voi laskea tapahtumalle aikaisimman täyttymispäivämäärän läpimenoaikojen, materiaalin saatavuuden ja suunnittelun erilaisten parametrien perusteella.</span><span class="sxs-lookup"><span data-stu-id="653c1-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="653c1-108">Jos pääsuunnittelu laskee tilauspäivämäärän, joka on aiempi kuin kuluva päivämäärä, tilausta ei voi täyttää ajoissa.</span><span class="sxs-lookup"><span data-stu-id="653c1-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="653c1-109">Tämän vuoksi tilaus viivästyy.</span><span class="sxs-lookup"><span data-stu-id="653c1-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="653c1-110">Tässä tapauksessa pääsuunnittelu suunnittelee tilauksen edelleen kuluvasta päivämäärästä ja sisällyttää läpimenoajat.</span><span class="sxs-lookup"><span data-stu-id="653c1-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="653c1-111">Läpimenoajat lasketaan alatason osanimikkeistä alkaen.</span><span class="sxs-lookup"><span data-stu-id="653c1-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="653c1-112">Tämän jälkeen tilaukselle määritetään viivästyspäivä.</span><span class="sxs-lookup"><span data-stu-id="653c1-112">The order then receives a delayed date.</span></span> <span data-ttu-id="653c1-113">Viivästyspäivä on nykyisiin tietoihin perustuva realistinen eräpäivä.</span><span class="sxs-lookup"><span data-stu-id="653c1-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="653c1-114">Pääsuunnittelu laskee myös viivästymispäivien määrän.</span><span class="sxs-lookup"><span data-stu-id="653c1-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="653c1-115">Joissakin tilanteissa viivästyspäivää ei välttämättä käytetä. Näin voi käydä esimerkiksi silloin, kun käyttäjät tietävät voivansa jouduttaa läpimenoaikoja valitsemalla vaihtoehtoisen toimitustavan.</span><span class="sxs-lookup"><span data-stu-id="653c1-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="653c1-116">Voit määrittää kattavuusryhmän viivästysten laskentatavat.</span><span class="sxs-lookup"><span data-stu-id="653c1-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="653c1-117">Voit liittää kattavuusryhmän nimikkeeseen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="653c1-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="653c1-118">**Pääsuunnittelun parametrit** -sivulla voit määrittää viivästymisten laskennan aloitusajan.</span><span class="sxs-lookup"><span data-stu-id="653c1-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="653c1-119">Jos tilaus täyttyy tämän jälkeen, tilauksen viivästyspäivään lisätään yksi päivä.</span><span class="sxs-lookup"><span data-stu-id="653c1-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="653c1-120">Aiemmissa versioissa laskettuja viiveitä kutsuttiin *viivästyssanomiksi*, viivästyspäivää *viivästyspäiväksi* ja viivästynyttä tapahtumaa *tulevaisuuteen määritetyksi tapahtumaksi*.</span><span class="sxs-lookup"><span data-stu-id="653c1-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="653c1-121">Tuotantoasetusten rajoitetut viiveet useilla tuoterakennetasoilla</span><span class="sxs-lookup"><span data-stu-id="653c1-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="653c1-122">Kun käsittelet useita tuoterakennetasoja sisältävien tuotantomääritysten viiveitä, on tärkeää huomata, että vain suoraan nimikkeen yläpuolella (tuoterakennerakenteessa) olevat nimikkeet, jotka aiheuttavat viivästyksen, päivitetään viiveellä osana pääsuunnittelun ajoaikaa.</span><span class="sxs-lookup"><span data-stu-id="653c1-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="653c1-123">Muut tuoterakennerakenteen nimikkeet eivät saa sitä viivettä, jota käytetään, ennen kuin ensimmäinen pääsuunnittelu suoritetaan, kun ylimmän tason suunniteltu tilaus hyväksytään tai vahvistetaan.</span><span class="sxs-lookup"><span data-stu-id="653c1-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="653c1-124">Voit välttää tämän tunnetun rajoituksen valitsemalla tuoterakennerakenteen yläosassa olevat tuotantotilaukset, joiden viiveet on hyväksytty (tai vahvistettu) ennen seuraavaa pääsuunnitteluajoa.</span><span class="sxs-lookup"><span data-stu-id="653c1-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="653c1-125">Näin viivästyneen hyväksytyn suunnitellun tuotantotilauksen viivästyminen säilytetään ja kaikki pohjana olevat komponentit päivitetään vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="653c1-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="653c1-126">Toimenpidesanomien avulla voidaan myös tunnistaa suunnitellut tilaukset, jotka voidaan siirtää myöhempään päivään tuoterakennerakenteen muiden viivästysten vuoksi.</span><span class="sxs-lookup"><span data-stu-id="653c1-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="653c1-127">Haluttu päivämäärä</span><span class="sxs-lookup"><span data-stu-id="653c1-127">Desired date</span></span>

<span data-ttu-id="653c1-128">**Suunniteltu tilaus** -sivulta **Viiveitä** -välilehdeltä löytyy **Haluttu päivämäärä** suunnitellulle tilaukselle.</span><span class="sxs-lookup"><span data-stu-id="653c1-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="653c1-129">Suunnitellun tilauksen haluttu päivämäärä on viivästysten peruspäivä, joka on laskettu päivämäärä, joka vastaa **Vaadittua päivämäärää**, joka on laskettu kohteesta **Nettotarve**.</span><span class="sxs-lookup"><span data-stu-id="653c1-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="653c1-130">Jos suunniteltu tilaus on Tuoterakenteen tuotantorivi tai kanban-rivi, kyseinen päivämäärä perustuu **Tarvepäivään** ja haluttua päivää ei näytetä **suunnitellun tilauksen** sivulla.</span><span class="sxs-lookup"><span data-stu-id="653c1-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="653c1-131">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="653c1-131">Additional resources</span></span>
--------

[<span data-ttu-id="653c1-132">Kattavuusasetukset</span><span class="sxs-lookup"><span data-stu-id="653c1-132">Coverage settings</span></span>](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]