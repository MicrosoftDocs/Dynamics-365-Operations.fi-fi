---
title: Työtä ei ole estetty
description: Työtä ei ole estetty
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924201"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="ef817-103">Työtä ei ole estetty</span><span class="sxs-lookup"><span data-stu-id="ef817-103">Work isn't blocked</span></span>

<span data-ttu-id="ef817-104">Virhekoodi: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="ef817-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="ef817-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="ef817-105">Symptoms</span></span>

<span data-ttu-id="ef817-106">Järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="ef817-106">The system shows the following error message:</span></span>

> <span data-ttu-id="ef817-107">Työtä tunnuksella %1 ei ole estetty.</span><span class="sxs-lookup"><span data-stu-id="ef817-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="ef817-108">Syy</span><span class="sxs-lookup"><span data-stu-id="ef817-108">Cause</span></span>

<span data-ttu-id="ef817-109">**Estetty aalto** -asetuksen arvo aallossa on *Ei*.</span><span class="sxs-lookup"><span data-stu-id="ef817-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="ef817-110">Työn estoa ei voi poistaa, koska se ei ole estettynä.</span><span class="sxs-lookup"><span data-stu-id="ef817-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="ef817-111">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ef817-111">Resolution</span></span>

 <span data-ttu-id="ef817-112">Vain työn, jonka **Estetty aalto** -asetuksen arvona on *Kyllä*, esto voidaan poistaa.</span><span class="sxs-lookup"><span data-stu-id="ef817-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
