---
title: Asiakirjan tilat ja elinkaari
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen sivuelementtien eri asiakirjatiloista.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b4f1c462f734b2d58843308f0f877fe18a4d9af7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002978"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="37bda-103">Asiakirjan tilat ja elinkaari</span><span class="sxs-lookup"><span data-stu-id="37bda-103">Document states and lifecycle</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="37bda-104">Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen sivuelementtien eri asiakirjatiloista.</span><span class="sxs-lookup"><span data-stu-id="37bda-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="37bda-105">Asiakirjan tilan kuvaukset</span><span class="sxs-lookup"><span data-stu-id="37bda-105">Document state descriptions</span></span>

<span data-ttu-id="37bda-106">[Sivuelementit](page-elements-overview.md)-ohjeaiheessa on sisällönhallintajärjestelmän (CMS) eri asiakirjatyyppejä.</span><span class="sxs-lookup"><span data-stu-id="37bda-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="37bda-107">Näillä asiakirjatyypeillä voi olla useita tiloja muokkaustyökalussa.</span><span class="sxs-lookup"><span data-stu-id="37bda-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="37bda-108">Asiakirjan tilat auttavat estämään tietoristiriitoja ja ottavat käyttöön versionhallinnan.</span><span class="sxs-lookup"><span data-stu-id="37bda-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="37bda-109">Ne määrittävät, ketkä voivat muuttaa asiakirjoja, milloin asiakirjoja voi muuttaa ja milloin muut voivat tarkastella muutoksia.</span><span class="sxs-lookup"><span data-stu-id="37bda-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="37bda-110">Seuraavassa taulukossa esitetään sivuelementtien mahdolliset asiakirjojen tilat Commercessa.</span><span class="sxs-lookup"><span data-stu-id="37bda-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="37bda-111">Asiakirjan tila</span><span class="sxs-lookup"><span data-stu-id="37bda-111">Document state</span></span> | <span data-ttu-id="37bda-112">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="37bda-112">Description</span></span> |
|---|---|
| <span data-ttu-id="37bda-113">Kuitattu ulos</span><span class="sxs-lookup"><span data-stu-id="37bda-113">Checked out</span></span> | <span data-ttu-id="37bda-114">Kun CMS-nimike on kuitattu ulos sinulle, mikään muu todennettu järjestelmäkäyttäjä ei voi muokata sitä.</span><span class="sxs-lookup"><span data-stu-id="37bda-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="37bda-115">Kaikki nimikkeeseen tekemäsi muutokset näkyvät vain sinulle.</span><span class="sxs-lookup"><span data-stu-id="37bda-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="37bda-116">Kuitattu sisään</span><span class="sxs-lookup"><span data-stu-id="37bda-116">Checked in</span></span> | <span data-ttu-id="37bda-117">Kun CMS-nimike kuitataan sisään, kaikki muutokset näkyvät muille todennetuille järjestelmäkäyttäjille. Käyttäjät voivat kuitata nimikkeen ulos ja muokata sitä.</span><span class="sxs-lookup"><span data-stu-id="37bda-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="37bda-118">Jokainen sisäänkuittaus luo asiakirjaversiotietueen nimikkeen historiaan.</span><span class="sxs-lookup"><span data-stu-id="37bda-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="37bda-119">Julkaistu</span><span class="sxs-lookup"><span data-stu-id="37bda-119">Published</span></span> | <span data-ttu-id="37bda-120">Kun CMS-nimike julkaistaan, se siirretään live-sivustoon. Todentamattomat ulkoiset käyttäjät voivat löytää sen verkossa.</span><span class="sxs-lookup"><span data-stu-id="37bda-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="37bda-121">Nimikkeet voidaan julkaista vain, jos ne on kuitattu sisään.</span><span class="sxs-lookup"><span data-stu-id="37bda-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="37bda-122">Tallennettu</span><span class="sxs-lookup"><span data-stu-id="37bda-122">Saved</span></span> | <span data-ttu-id="37bda-123">Uloskuitattuun CMS-nimikkeeseen tehdyt muutokset voidaan tallentaa CMS:ään ennen kuin nimike kuitataan sisään tai julkaistaan.</span><span class="sxs-lookup"><span data-stu-id="37bda-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="37bda-124">Nämä tallennetut muutokset eivät näy muille todennetuille järjestelmäkäyttäjille ennen kuin nimike kuitataan sisään.</span><span class="sxs-lookup"><span data-stu-id="37bda-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="37bda-125">Ulkoiset käyttäjät eivät näe niitä, ennen kuin nimike on julkaistu.</span><span class="sxs-lookup"><span data-stu-id="37bda-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="37bda-126">Hylätty uloskuittaus</span><span class="sxs-lookup"><span data-stu-id="37bda-126">Discarded check out</span></span> | <span data-ttu-id="37bda-127">Kun uloskuitattu CMS-nimike hylätään, kaikki tallennetut muutokset poistetaan ja nimike palautuu viimeksi sisäänkuitattuun versioon.</span><span class="sxs-lookup"><span data-stu-id="37bda-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="37bda-128">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="37bda-128">Additional resources</span></span>

[<span data-ttu-id="37bda-129">Tapoja lisästä sisältöä</span><span class="sxs-lookup"><span data-stu-id="37bda-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="37bda-130">Sivumallisanasto</span><span class="sxs-lookup"><span data-stu-id="37bda-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="37bda-131">Julkaisuryhmien kanssa työskenteleminen</span><span class="sxs-lookup"><span data-stu-id="37bda-131">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="37bda-132">Moduulien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="37bda-132">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="37bda-133">Katkelmien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="37bda-133">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="37bda-134">Mallit ja asettelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="37bda-134">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="37bda-135">Sivuston selauksen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="37bda-135">Customize site navigation</span></span>](customize-site-navigation.md)
