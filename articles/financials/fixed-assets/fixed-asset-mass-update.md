---
title: Käyttöomaisuuden laajamittainen päivitys
description: Jos käytät kirjoja, voit vaihtaa samaan kirjaan kuuluvien käyttöomaisuuserien muodostamien ryhmien poistomenetelmiä.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30b9aaaabcac09c9147c350422924a23f785c0ce
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840406"
---
# <a name="fixed-asset-mass-update"></a><span data-ttu-id="7d393-103">Käyttöomaisuuden laajamittainen päivitys</span><span class="sxs-lookup"><span data-stu-id="7d393-103">Fixed asset mass update</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d393-104">Jos käytät kirjoja, voit vaihtaa samaan kirjaan kuuluvien käyttöomaisuuserien muodostamien ryhmien poistomenetelmiä.</span><span class="sxs-lookup"><span data-stu-id="7d393-104">If you use books, you can change the depreciation conventions for groups of assets that are part of the same book.</span></span>

<span data-ttu-id="7d393-105">Esimerkiksi jos toimit Yhdysvalloissa ja sijoitit yli 40 prosenttia käyttöomaisuudesta huoltoon neljännen vuosineljänneksen aikana, sinun on käytettävä vuosineljänneksen puolivälin poistomenetelmää.</span><span class="sxs-lookup"><span data-stu-id="7d393-105">For example, if you are in the United States, and you put more than 40 percent of your assets in service during the fourth quarter of the year, you must use the mid-quarter depreciation convention.</span></span> <span data-ttu-id="7d393-106">Voit käyttää joukkopäivitystä kaikkien uutta poistomenetelmää edellyttävien käyttöomaisuuserien poistomenetelmän vaihtamiseen.</span><span class="sxs-lookup"><span data-stu-id="7d393-106">You can use the process for a mass update to change all assets that require the new depreciation convention.</span></span> 

<span data-ttu-id="7d393-107">Kun päivität käyttöomaisuuserien poistomenetelmän, kaikki kyseisten käyttöomaisuuserien poistotapahtumat poistetaan.</span><span class="sxs-lookup"><span data-stu-id="7d393-107">When you update the depreciation convention for assets, you delete all depreciation transactions that exist for those assets.</span></span> <span data-ttu-id="7d393-108">Samalla poistetaan kaikki kyseisiin käyttöomaisuuseriin liittyvät poistojen oikaisutapahtumat, bonuspoistotapahtumat sekä lisäpoistotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="7d393-108">You also delete all transactions for depreciation adjustments, transactions for bonus depreciation, and transactions for extraordinary depreciation for those assets.</span></span> 

<span data-ttu-id="7d393-109">Voidaksesi päivittää jo poistettujen käyttöomaisuuserien poistomenetelmän, sinun on ensin poistettava olemassa olevat poistotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="7d393-109">To update the depreciation convention for assets that have already been disposed of, you must first delete the existing disposal transactions.</span></span> <span data-ttu-id="7d393-110">Sinun on poistettava myös kaikki tapahtumat, jotka on luotu poistoprosessia varten.</span><span class="sxs-lookup"><span data-stu-id="7d393-110">You must also delete all transactions that were generated because of the disposal process.</span></span> 

<span data-ttu-id="7d393-111">Päivitettyäsi käyttöomaisuuserien poistomenetelmän, voit käsitellä kunkin käyttöomaisuuserän poiston ja lisäpoiston.</span><span class="sxs-lookup"><span data-stu-id="7d393-111">After you update the depreciation convention for assets, you can process depreciation and extraordinary depreciation for each asset.</span></span> <span data-ttu-id="7d393-112">Voit myös tehdä poistoihin tarvittaessa manuaalisia oikaisuja.</span><span class="sxs-lookup"><span data-stu-id="7d393-112">You can also make manual depreciation adjustments, if any adjustments are required.</span></span>





