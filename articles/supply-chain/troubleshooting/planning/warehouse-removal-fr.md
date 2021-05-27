---
title: Varaston kysynnän ennustedimensiota ei voi poistaa ennusteriveistä
description: Varaston kysynnän ennustedimensiota ei voi poistaa ennusteriveistä.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026476"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="5cc6a-103">Varaston kysynnän ennustedimensiota ei voi poistaa ennusteriveistä</span><span class="sxs-lookup"><span data-stu-id="5cc6a-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="5cc6a-104">Tietopankin numero: 4614408</span><span class="sxs-lookup"><span data-stu-id="5cc6a-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="5cc6a-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="5cc6a-105">Symptoms</span></span>

<span data-ttu-id="5cc6a-106">Tämä ongelma ilmenee, kun **Varasto**-dimensiota ei ole määritetty **Ennustedimensiot**-välilehdellä **Kysynnän ennusteen parametri** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="5cc6a-107">**Varasto**-sarake näkyy kuitenkin **Kysynnän ennuste** -sivulla (**Pääsuunnittelu \> Ennuste \> Manuaalinen ennusteyksikkö \> Kysynnän ennusteen rivit**).</span><span class="sxs-lookup"><span data-stu-id="5cc6a-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="5cc6a-108">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="5cc6a-108">Resolution</span></span>

<span data-ttu-id="5cc6a-109">**Ennustedimensiot**-välilehden asetukset **Kysynnän ennusteen parametri** -sivulla ei vaikuta **Kysynnän ennuste** -sivuun.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="5cc6a-110">Ne ohjaavat perusennustetta, joka luodaan ja näkyy oikaistussa kysyntäennusteessa.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="5cc6a-111">Ne eivät kuitenkaan ohjaa dimensioita, joita "todellinen" kysyntäennuste edellyttää.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="5cc6a-112">Valtuuttamalla **Oikaistu kysynnän ennuste** -sivulla näkyvät tietueet voit muuntaa ne ennustemallin "todellisiksi" ennustetapahtumiksi.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="5cc6a-113">Tätä mallia voidaan sitten käyttää pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="5cc6a-114">**Kysynnän ennuste** -sivulla kysynnän ennusteen riveillä näkyvät "todellisen" ennusteen dimensiot ovat osa varastodimensioita.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="5cc6a-115">(Käyttäytyminen muistuttaa myyntitilausrivien toimintatapaa.) Jos järjestelmää ei ole määritetty käyttämään **varastoa** pakollisena varastodimensiona, voit piilottaa sarakkeen mukauttamalla sivun.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
