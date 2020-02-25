---
title: Tulevien elämäntapahtumien määrittäminen
description: Voit ajoittaa tulevia elämäntapahtumia Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 655070e52e3d1f43ca6904ce3218582868f193fe
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008897"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="921a2-103">Tulevien elämäntapahtumien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="921a2-103">Configure future life events</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="921a2-104">Voit ajoittaa tulevia elämäntapahtumia Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="921a2-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="921a2-105">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Tulevat elämäntapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="921a2-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="921a2-106">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="921a2-106">Select **New**.</span></span>

3. <span data-ttu-id="921a2-107">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="921a2-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="921a2-108">Kenttä</span><span class="sxs-lookup"><span data-stu-id="921a2-108">Field</span></span> | <span data-ttu-id="921a2-109">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="921a2-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="921a2-110">Elinkaaritapahtuman päivämäärä</span><span class="sxs-lookup"><span data-stu-id="921a2-110">Life event date</span></span> | <span data-ttu-id="921a2-111">Järjestelmä käsittelee kaikki rekisteröintijakson aikana tähän päivämäärään mennessä toteutuneet tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="921a2-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="921a2-112">Elinkaaritapahtuma on kirjattu</span><span class="sxs-lookup"><span data-stu-id="921a2-112">Life event logged</span></span> | <span data-ttu-id="921a2-113">Elämäntapahtuman lokiin kirjaamisen päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="921a2-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="921a2-114">Lokityyppi</span><span class="sxs-lookup"><span data-stu-id="921a2-114">Log type</span></span> | <span data-ttu-id="921a2-115">Näyttää, onko toiminto jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="921a2-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="921a2-116">- **Päivitys** – Muutos olemassa olevaan tietueeseen, joka seuraa elämäntapahtumia</span><span class="sxs-lookup"><span data-stu-id="921a2-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="921a2-117">- **Lisää** – Uuden elämäntapahtumatietueen luonti</span><span class="sxs-lookup"><span data-stu-id="921a2-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="921a2-118">Elinkaaritapahtuman tyypin tunnus</span><span class="sxs-lookup"><span data-stu-id="921a2-118">Life event type ID</span></span> | <span data-ttu-id="921a2-119">Elämäntapahtumatyypin yksilöllinen tunniste.</span><span class="sxs-lookup"><span data-stu-id="921a2-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="921a2-120">Elinkaaritapahtuman tyyppi</span><span class="sxs-lookup"><span data-stu-id="921a2-120">Life event type</span></span> | <span data-ttu-id="921a2-121">Työntekijän eturekisteröinnin päivittämisen katalysaattori.</span><span class="sxs-lookup"><span data-stu-id="921a2-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="921a2-122">Lisätietoja on osassa Elämäntapahtumien käynnistimet.</span><span class="sxs-lookup"><span data-stu-id="921a2-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="921a2-123">Tila</span><span class="sxs-lookup"><span data-stu-id="921a2-123">Status</span></span> | <span data-ttu-id="921a2-124">Onko elämäntapahtuma käsitelty.</span><span class="sxs-lookup"><span data-stu-id="921a2-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="921a2-125">Linja</span><span class="sxs-lookup"><span data-stu-id="921a2-125">Line</span></span> | <span data-ttu-id="921a2-126">Tulevan elämäntapahtuman rivinumero.</span><span class="sxs-lookup"><span data-stu-id="921a2-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="921a2-127">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="921a2-127">Select **Save**.</span></span> 
