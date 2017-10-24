---
title: Valtuuta oikaistu ennuste
description: "Kaikkia ennusteen tietoja ei tarvitse valtuuttaa heti. Tässä artikkelissa kerrotaan, miten voit määrittää kauden, jolle ennuste on valtuutettu. Siinä myös kerrotaan, miten voit valtuuttaa ennusteen määrätyille yrityksille ja ennustemalleille."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 399a7a21ec71fe50e280ccb24699cda76d571990
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="8e7be-105">Valtuuta oikaistu ennuste</span><span class="sxs-lookup"><span data-stu-id="8e7be-105">Authorize an adjusted forecast</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8e7be-106">Kaikkia ennusteen tietoja ei tarvitse valtuuttaa heti.</span><span class="sxs-lookup"><span data-stu-id="8e7be-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="8e7be-107">Tässä artikkelissa kerrotaan, miten voit määrittää kauden, jolle ennuste on valtuutettu.</span><span class="sxs-lookup"><span data-stu-id="8e7be-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="8e7be-108">Siinä myös kerrotaan, miten voit valtuuttaa ennusteen määrätyille yrityksille ja ennustemalleille.</span><span class="sxs-lookup"><span data-stu-id="8e7be-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="8e7be-109">Kaikkia ennusteen tietoja ei tarvitse valtuuttaa heti.</span><span class="sxs-lookup"><span data-stu-id="8e7be-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="8e7be-110">Voit määrittää sen kauden alkamis- ja päättymispäivät, jolle ennuste on valtuutettu.</span><span class="sxs-lookup"><span data-stu-id="8e7be-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="8e7be-111">Tämän toiminnon avulla voit lukita määrätyt aikajaksot.</span><span class="sxs-lookup"><span data-stu-id="8e7be-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="8e7be-112">Määrittämäsi alkamis- ja päättymispäivämäärät pitää vastata sen säilön alkamis- ja päättymispäivämääriä, jossa ennuste luodaan.</span><span class="sxs-lookup"><span data-stu-id="8e7be-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="8e7be-113">Järjestelmä pakottaa tämän rajoituksen ja säätää automaattisesti päivämäärät, jos muutos on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="8e7be-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="8e7be-114">Sivun **Valtuutus** välilehdellä **Tiedot** voit tarkastella viimeksi luotuja ennusteen tietoja.</span><span class="sxs-lookup"><span data-stu-id="8e7be-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="8e7be-115">Voit valita yritykset ja ennustemallit, jotka valtuuttavat ennusteen käyttöön otettavaksi.</span><span class="sxs-lookup"><span data-stu-id="8e7be-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="8e7be-116">Oletuksena tämä ruudukko sisältää kaikki yritykset, joille ennustettu kysyntä on luotu.</span><span class="sxs-lookup"><span data-stu-id="8e7be-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="8e7be-117">Kullakin yrityksellä ennustemalli, joka vastaa nykyistä, pääsuunnitteluparametreissa määritettyä ennustesuunnitelmaa, on valmiiksi täytetty.</span><span class="sxs-lookup"><span data-stu-id="8e7be-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="8e7be-118">Voit kuitenkin muuttaa tätä ennustemallia miksi tahansa kyseiselle yritykselle kuuluvaksi ennustemalliksi.</span><span class="sxs-lookup"><span data-stu-id="8e7be-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="8e7be-119">Jos kysynnän ennusteen tietoja ei ole luotu valitulle yritykselle, saat tuontihetkellä varoitussanoman.</span><span class="sxs-lookup"><span data-stu-id="8e7be-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="8e7be-120">On erittäin tärkeää, että ymmärrät, miten **Tallenna kysynnän perusennusteeseen tehdyt manuaaliset oikaisut** -valintaruutu toimii.</span><span class="sxs-lookup"><span data-stu-id="8e7be-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="8e7be-121">Jos olet tehnyt manuaalisia oikaisuja tilastolliseen perusennusteeseen, oikaistut arvot on valtuutettu käytettäväksi, vaikka tämä valintaruutu olisi tyhjä.</span><span class="sxs-lookup"><span data-stu-id="8e7be-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="8e7be-122">Muutokset kuitenkin hylätään valtuutuksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="8e7be-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="8e7be-123">Näin ollen, seuraavan kerran kun ennuste luodaan, tämä ennuste on vain tilastollinen ennuste, eikä sillä ole manuaalisia ohituksia, vaikka **Siirrä manuaaliset oikaisut kysynnän ennusteeseen** -valintaruutu on valittuna.</span><span class="sxs-lookup"><span data-stu-id="8e7be-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="8e7be-124">Voit näin ollen harkita **Tallenna kysynnän perusennusteeseen tehdyt manuaaliset oikaisut** -valintaruutumekanismia, jonka avulla voit säilyttää tai hylätä kaikki manuaaliset muutokset.</span><span class="sxs-lookup"><span data-stu-id="8e7be-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="see-also"></a><span data-ttu-id="8e7be-125">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="8e7be-125">See also</span></span>
--------

[<span data-ttu-id="8e7be-126">Manuaalisten oikaisujen tekeminen perusennusteeseen</span><span class="sxs-lookup"><span data-stu-id="8e7be-126">Making manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="8e7be-127">Ennusteen tarkkuuden valvonta</span><span class="sxs-lookup"><span data-stu-id="8e7be-127">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)




