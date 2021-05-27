---
title: Viimeinen testauspäivämäärä -kenttää ei päivitetä, kun useita laatutilauksia luodaan
description: Viimeinen testauspäivämäärä -kenttää ei päivitetä, kun useita laatutilauksia luodaan.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026484"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="71623-103">Viimeinen testauspäivämäärä -kenttää ei päivitetä, kun useita laatutilauksia luodaan</span><span class="sxs-lookup"><span data-stu-id="71623-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="71623-104">Tietopankin numero: 4612803</span><span class="sxs-lookup"><span data-stu-id="71623-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="71623-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="71623-105">Symptoms</span></span>

<span data-ttu-id="71623-106">**Viimeinen testauspäivämäärä** -kenttää ei päivitetä, kun useita laatutilauksia luodaan.</span><span class="sxs-lookup"><span data-stu-id="71623-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="71623-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="71623-107">Resolution</span></span>

<span data-ttu-id="71623-108">Järjestelmä käyttäytyy suunnitellulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="71623-108">The system is behaving as designed.</span></span> <span data-ttu-id="71623-109">Viimeinen testauspäivämäärä ei liity laatutilauksiin.</span><span class="sxs-lookup"><span data-stu-id="71623-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="71623-110">Se tallentaa päivämäärän, jolloin valmiit tavarat on ensin ostettu tai valmistettu.</span><span class="sxs-lookup"><span data-stu-id="71623-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="71623-111">Tätä päivämäärää käytetään suositeltavan säilyvyysajan laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="71623-111">This date is used to calculate the shelf life advice date.</span></span>
