---
title: Viiveet
description: Tässä ohjeaiheessa on tietoja pääsuunnittelun viivästyspäivistä. Viivästyspäivä on realistinen eräpäivä, jonka tapahtuma saa, jos pääsuunnittelun laskema aikaisin toimituspäivä on myöhempi kuin pyydetty päivämäärä.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c26fedf15118a304469604527c33a25871356be
ms.sourcegitcommit: 8eac5eee94bb32143df44c82a2dfdbe903967af8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/20/2019
ms.locfileid: "878307"
---
# <a name="delays"></a><span data-ttu-id="cd785-104">Viiveet</span><span class="sxs-lookup"><span data-stu-id="cd785-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd785-105">Tässä ohjeaiheessa on tietoja pääsuunnittelun viivästyspäivistä.</span><span class="sxs-lookup"><span data-stu-id="cd785-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="cd785-106">Viivästyspäivä on realistinen eräpäivä, jonka tapahtuma saa, jos pääsuunnittelun laskema aikaisin toimituspäivä on myöhempi kuin pyydetty päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="cd785-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="cd785-107">Pääsuunnittelu voi laskea tapahtumalle aikaisimman täyttymispäivämäärän läpimenoaikojen, materiaalin saatavuuden ja suunnittelun erilaisten parametrien perusteella.</span><span class="sxs-lookup"><span data-stu-id="cd785-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="cd785-108">Jos pääsuunnittelu laskee tilauspäivämäärän, joka on aiempi kuin kuluva päivämäärä, tilausta ei voi täyttää ajoissa.</span><span class="sxs-lookup"><span data-stu-id="cd785-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="cd785-109">Tämän vuoksi tilaus viivästyy.</span><span class="sxs-lookup"><span data-stu-id="cd785-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="cd785-110">Tässä tapauksessa pääsuunnittelu suunnittelee tilauksen edelleen kuluvasta päivämäärästä ja sisällyttää läpimenoajat.</span><span class="sxs-lookup"><span data-stu-id="cd785-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="cd785-111">Läpimenoajat lasketaan alatason osanimikkeistä alkaen.</span><span class="sxs-lookup"><span data-stu-id="cd785-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="cd785-112">Tämän jälkeen tilaukselle määritetään viivästyspäivä.</span><span class="sxs-lookup"><span data-stu-id="cd785-112">The order then receives a delayed date.</span></span> <span data-ttu-id="cd785-113">Viivästyspäivä on nykyisiin tietoihin perustuva realistinen eräpäivä.</span><span class="sxs-lookup"><span data-stu-id="cd785-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="cd785-114">Pääsuunnittelu laskee myös viivästymispäivien määrän.</span><span class="sxs-lookup"><span data-stu-id="cd785-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="cd785-115">Joissakin tilanteissa viivästyspäivää ei välttämättä käytetä. Näin voi käydä esimerkiksi silloin, kun käyttäjät tietävät voivansa jouduttaa läpimenoaikoja valitsemalla vaihtoehtoisen toimitustavan.</span><span class="sxs-lookup"><span data-stu-id="cd785-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="cd785-116">Voit määrittää kattavuusryhmän viivästysten laskentatavat.</span><span class="sxs-lookup"><span data-stu-id="cd785-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="cd785-117">Voit liittää kattavuusryhmän nimikkeeseen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="cd785-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="cd785-118">**Pääsuunnittelun parametrit** -sivulla voit määrittää viivästymisten laskennan aloitusajan.</span><span class="sxs-lookup"><span data-stu-id="cd785-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="cd785-119">Jos tilaus täyttyy tämän jälkeen, tilauksen viivästyspäivään lisätään yksi päivä.</span><span class="sxs-lookup"><span data-stu-id="cd785-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> <span data-ttu-id="cd785-120">[!HUOMAUTUS} Aiemmissa versioissa laskettuja viiveitä kutsuttiin *viivästyssanomiksi*, viivästyspäivää *lasketuksi viivästyspäiväksi* ja viivästynyttä tapahtumaa *tulevaisuuteen määritetyksi tapahtumaksi*.</span><span class="sxs-lookup"><span data-stu-id="cd785-120">[!NOTE} In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="desired-date"></a><span data-ttu-id="cd785-121">Haluttu päivämäärä</span><span class="sxs-lookup"><span data-stu-id="cd785-121">Desired date</span></span>

<span data-ttu-id="cd785-122">**Suunniteltu tilaus** -sivulta **Viiveitä** -välilehdeltä löytyy **Haluttu päivämäärä** suunnitellulle tilaukselle.</span><span class="sxs-lookup"><span data-stu-id="cd785-122">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="cd785-123">Suunnitellun tilauksen haluttu päivämäärä on viivästysten peruspäivä, joka on laskettu päivämäärä, joka vastaa **Vaadittua päivämäärää**, joka on laskettu kohteesta **Nettotarve**.</span><span class="sxs-lookup"><span data-stu-id="cd785-123">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="cd785-124">Jos suunniteltu tilaus on Tuoterakenteen tuotantorivi tai kanban-rivi, kyseinen päivämäärä perustuu **Tarvepäivään** ja haluttua päivää ei näytetä **suunnitellun tilauksen** sivulla.</span><span class="sxs-lookup"><span data-stu-id="cd785-124">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="cd785-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="cd785-125">Additional resources</span></span>
--------

[<span data-ttu-id="cd785-126">Kattavuusasetukset</span><span class="sxs-lookup"><span data-stu-id="cd785-126">Coverage settings</span></span>](coverage-settings.md)
