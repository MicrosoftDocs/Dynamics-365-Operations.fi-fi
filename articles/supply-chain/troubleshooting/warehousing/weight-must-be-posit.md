---
title: Painon on oltava positiivinen
description: Painon on oltava positiivinen
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924300"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="17196-103">Painon on oltava positiivinen</span><span class="sxs-lookup"><span data-stu-id="17196-103">Weight must be positive</span></span>

<span data-ttu-id="17196-104">Virhekoodi: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="17196-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="17196-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="17196-105">Symptoms</span></span>

<span data-ttu-id="17196-106">Järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="17196-106">The system shows the following error message:</span></span>

> <span data-ttu-id="17196-107">Painon on oltava positiivinen.</span><span class="sxs-lookup"><span data-stu-id="17196-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="17196-108">Syy</span><span class="sxs-lookup"><span data-stu-id="17196-108">Cause</span></span>

<span data-ttu-id="17196-109">**Bruttopaino**-kentän arvoksi määritetään *0* (nolla) tai negatiivinen arvo.</span><span class="sxs-lookup"><span data-stu-id="17196-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="17196-110">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="17196-110">Resolution</span></span>

<span data-ttu-id="17196-111">Jos haluat määrittää painon, seuraa jotakin näistä vaiheista.</span><span class="sxs-lookup"><span data-stu-id="17196-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="17196-112">Määritä arvo **Bruttopaino**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="17196-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="17196-113">Valitse sitten yksikkö avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="17196-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="17196-114">Valitse **Hae järjestelmän paino** laskeaksesi **Bruttopaino**-arvon.</span><span class="sxs-lookup"><span data-stu-id="17196-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
