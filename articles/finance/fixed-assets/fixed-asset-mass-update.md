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
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ccccfd3168cf132453b41a74c57f4fd2629fb22
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994887"
---
# <a name="fixed-asset-mass-update"></a><span data-ttu-id="8c11d-103">Käyttöomaisuuden laajamittainen päivitys</span><span class="sxs-lookup"><span data-stu-id="8c11d-103">Fixed asset mass update</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c11d-104">Jos käytät kirjoja, voit vaihtaa samaan kirjaan kuuluvien käyttöomaisuuserien muodostamien ryhmien poistomenetelmiä.</span><span class="sxs-lookup"><span data-stu-id="8c11d-104">If you use books, you can change the depreciation conventions for groups of assets that are part of the same book.</span></span>

<span data-ttu-id="8c11d-105">Esimerkiksi jos toimit Yhdysvalloissa ja sijoitit yli 40 prosenttia käyttöomaisuudesta huoltoon neljännen vuosineljänneksen aikana, sinun on käytettävä vuosineljänneksen puolivälin poistomenetelmää.</span><span class="sxs-lookup"><span data-stu-id="8c11d-105">For example, if you are in the United States, and you put more than 40 percent of your assets in service during the fourth quarter of the year, you must use the mid-quarter depreciation convention.</span></span> <span data-ttu-id="8c11d-106">Voit käyttää joukkopäivitystä kaikkien uutta poistomenetelmää edellyttävien käyttöomaisuuserien poistomenetelmän vaihtamiseen.</span><span class="sxs-lookup"><span data-stu-id="8c11d-106">You can use the process for a mass update to change all assets that require the new depreciation convention.</span></span> 

<span data-ttu-id="8c11d-107">Kun päivität käyttöomaisuuserien poistomenetelmän, kaikki kyseisten käyttöomaisuuserien poistotapahtumat poistetaan.</span><span class="sxs-lookup"><span data-stu-id="8c11d-107">When you update the depreciation convention for assets, you delete all depreciation transactions that exist for those assets.</span></span> <span data-ttu-id="8c11d-108">Samalla poistetaan kaikki kyseisiin käyttöomaisuuseriin liittyvät poistojen oikaisutapahtumat, bonuspoistotapahtumat sekä lisäpoistotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="8c11d-108">You also delete all transactions for depreciation adjustments, transactions for bonus depreciation, and transactions for extraordinary depreciation for those assets.</span></span> 

<span data-ttu-id="8c11d-109">Voidaksesi päivittää jo poistettujen käyttöomaisuuserien poistomenetelmän, sinun on ensin poistettava olemassa olevat poistotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="8c11d-109">To update the depreciation convention for assets that have already been disposed of, you must first delete the existing disposal transactions.</span></span> <span data-ttu-id="8c11d-110">Sinun on poistettava myös kaikki tapahtumat, jotka on luotu poistoprosessia varten.</span><span class="sxs-lookup"><span data-stu-id="8c11d-110">You must also delete all transactions that were generated because of the disposal process.</span></span> 

<span data-ttu-id="8c11d-111">Päivitettyäsi käyttöomaisuuserien poistomenetelmän, voit käsitellä kunkin käyttöomaisuuserän poiston ja lisäpoiston.</span><span class="sxs-lookup"><span data-stu-id="8c11d-111">After you update the depreciation convention for assets, you can process depreciation and extraordinary depreciation for each asset.</span></span> <span data-ttu-id="8c11d-112">Voit myös tehdä poistoihin tarvittaessa manuaalisia oikaisuja.</span><span class="sxs-lookup"><span data-stu-id="8c11d-112">You can also make manual depreciation adjustments, if any adjustments are required.</span></span>





