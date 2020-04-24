---
title: Tulevien elämäntapahtumien määrittäminen
description: Voit ajoittaa tulevia elämäntapahtumia Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 134152bb8ae2b9f42b59cc9202e244435a607eba
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230082"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="3dc2e-103">Tulevien elämäntapahtumien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3dc2e-103">Configure future life events</span></span>

<span data-ttu-id="3dc2e-104">Voit ajoittaa tulevia elämäntapahtumia Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="3dc2e-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="3dc2e-105">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Tulevat elämäntapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="3dc2e-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="3dc2e-106">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="3dc2e-106">Select **New**.</span></span>

3. <span data-ttu-id="3dc2e-107">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="3dc2e-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3dc2e-108">Kenttä</span><span class="sxs-lookup"><span data-stu-id="3dc2e-108">Field</span></span> | <span data-ttu-id="3dc2e-109">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="3dc2e-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3dc2e-110">Elinkaaritapahtuman päivämäärä</span><span class="sxs-lookup"><span data-stu-id="3dc2e-110">Life event date</span></span> | <span data-ttu-id="3dc2e-111">Järjestelmä käsittelee kaikki rekisteröintijakson aikana tähän päivämäärään mennessä toteutuneet tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="3dc2e-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="3dc2e-112">Elinkaaritapahtuma on kirjattu</span><span class="sxs-lookup"><span data-stu-id="3dc2e-112">Life event logged</span></span> | <span data-ttu-id="3dc2e-113">Elämäntapahtuman lokiin kirjaamisen päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="3dc2e-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="3dc2e-114">Lokityyppi</span><span class="sxs-lookup"><span data-stu-id="3dc2e-114">Log type</span></span> | <span data-ttu-id="3dc2e-115">Näyttää, onko toiminto jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="3dc2e-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="3dc2e-116">- **Päivitys** – Muutos olemassa olevaan tietueeseen, joka seuraa elämäntapahtumia</span><span class="sxs-lookup"><span data-stu-id="3dc2e-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="3dc2e-117">- **Lisää** – Uuden elämäntapahtumatietueen luonti</span><span class="sxs-lookup"><span data-stu-id="3dc2e-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="3dc2e-118">Elinkaaritapahtuman tyypin tunnus</span><span class="sxs-lookup"><span data-stu-id="3dc2e-118">Life event type ID</span></span> | <span data-ttu-id="3dc2e-119">Elämäntapahtumatyypin yksilöllinen tunniste.</span><span class="sxs-lookup"><span data-stu-id="3dc2e-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="3dc2e-120">Elinkaaritapahtuman tyyppi</span><span class="sxs-lookup"><span data-stu-id="3dc2e-120">Life event type</span></span> | <span data-ttu-id="3dc2e-121">Työntekijän eturekisteröinnin päivittämisen katalysaattori.</span><span class="sxs-lookup"><span data-stu-id="3dc2e-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="3dc2e-122">Lisätietoja on osassa Elämäntapahtumien käynnistimet.</span><span class="sxs-lookup"><span data-stu-id="3dc2e-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="3dc2e-123">Tila</span><span class="sxs-lookup"><span data-stu-id="3dc2e-123">Status</span></span> | <span data-ttu-id="3dc2e-124">Onko elämäntapahtuma käsitelty.</span><span class="sxs-lookup"><span data-stu-id="3dc2e-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="3dc2e-125">Linja</span><span class="sxs-lookup"><span data-stu-id="3dc2e-125">Line</span></span> | <span data-ttu-id="3dc2e-126">Tulevan elämäntapahtuman rivinumero.</span><span class="sxs-lookup"><span data-stu-id="3dc2e-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="3dc2e-127">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3dc2e-127">Select **Save**.</span></span> 
