---
title: Eränumero tyhjennetään, kun uusi erätunnus valitaan
description: Kun tarkastelet keräysluettelon kirjauskansioriviä, Eränumero-kentän arvo poistetaan, jos valitset uuden arvon Erätunnus-kentästä.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026458"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a><span data-ttu-id="6dc02-103">Eränumero tyhjennetään, kun uusi erätunnus valitaan</span><span class="sxs-lookup"><span data-stu-id="6dc02-103">Batch number is cleared when a new lot ID is selected</span></span>

<span data-ttu-id="6dc02-104">Tietopankin numero: 4613107</span><span class="sxs-lookup"><span data-stu-id="6dc02-104">KB number: 4613107</span></span>

## <a name="symptoms"></a><span data-ttu-id="6dc02-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="6dc02-105">Symptoms</span></span>

<span data-ttu-id="6dc02-106">Kun tarkastelet keräysluettelon kirjauskansioriviä, **Eränumero**-kentän arvo poistetaan, jos valitset uuden arvon **Erätunnus**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="6dc02-106">When you're reviewing a picking list journal line, the value in the **Batch number** field is cleared if you select a new value in the **Lot ID** field.</span></span>

## <a name="resolution"></a><span data-ttu-id="6dc02-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="6dc02-107">Resolution</span></span>

<span data-ttu-id="6dc02-108">Järjestelmä käyttäytyy suunnitellulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="6dc02-108">The system is behaving as designed.</span></span> <span data-ttu-id="6dc02-109">Jos muutat erätunnuksen, muutat nimikekontekstia.</span><span class="sxs-lookup"><span data-stu-id="6dc02-109">If you change the lot ID, you change the item context.</span></span> <span data-ttu-id="6dc02-110">Näin ollen eränumero nollataan.</span><span class="sxs-lookup"><span data-stu-id="6dc02-110">Therefore, the batch number is reset.</span></span>

<span data-ttu-id="6dc02-111">Jos haluat liittää eränumeron erätunnukseen, erätunnus on määritettävä ensin.</span><span class="sxs-lookup"><span data-stu-id="6dc02-111">To associate the batch number with a lot ID, you must set the lot ID first.</span></span>