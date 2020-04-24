---
title: Asiakirjan tilat ja elinkaari
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen sivuelementtien eri asiakirjatiloista.
author: phinneyridge
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 4a00f1c363e5ecb0e3e64637a8f487c48df2df72
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261510"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="2298d-103">Asiakirjan tilat ja elinkaari</span><span class="sxs-lookup"><span data-stu-id="2298d-103">Document states and lifecycle</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2298d-104">Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen sivuelementtien eri asiakirjatiloista.</span><span class="sxs-lookup"><span data-stu-id="2298d-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="2298d-105">Asiakirjan tilan kuvaukset</span><span class="sxs-lookup"><span data-stu-id="2298d-105">Document state descriptions</span></span>

<span data-ttu-id="2298d-106">[Sivuelementit](page-elements-overview.md)-ohjeaiheessa on sisällönhallintajärjestelmän (CMS) eri asiakirjatyyppejä.</span><span class="sxs-lookup"><span data-stu-id="2298d-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="2298d-107">Näillä asiakirjatyypeillä voi olla useita tiloja muokkaustyökalussa.</span><span class="sxs-lookup"><span data-stu-id="2298d-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="2298d-108">Asiakirjan tilat auttavat estämään tietoristiriitoja ja ottavat käyttöön versionhallinnan.</span><span class="sxs-lookup"><span data-stu-id="2298d-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="2298d-109">Ne määrittävät, ketkä voivat muuttaa asiakirjoja, milloin asiakirjoja voi muuttaa ja milloin muut voivat tarkastella muutoksia.</span><span class="sxs-lookup"><span data-stu-id="2298d-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="2298d-110">Seuraavassa taulukossa esitetään sivuelementtien mahdolliset asiakirjojen tilat Commercessa.</span><span class="sxs-lookup"><span data-stu-id="2298d-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="2298d-111">Asiakirjan tila</span><span class="sxs-lookup"><span data-stu-id="2298d-111">Document state</span></span>      | <span data-ttu-id="2298d-112">Sivustonmuodostimen toiminta</span><span class="sxs-lookup"><span data-stu-id="2298d-112">Site builder action</span></span>        | <span data-ttu-id="2298d-113">kuvaus</span><span class="sxs-lookup"><span data-stu-id="2298d-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="2298d-114">Kuitattu ulos</span><span class="sxs-lookup"><span data-stu-id="2298d-114">Checked out</span></span>         | <span data-ttu-id="2298d-115">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="2298d-115">Select **Edit**.</span></span>           | <span data-ttu-id="2298d-116">Asiakirja kuitataan ulos.</span><span class="sxs-lookup"><span data-stu-id="2298d-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="2298d-117">Kun asiakirja on tässä tilassa, muut todennetut järjestelmän käyttäjät eivät voi muuttaa sitä, ja kaikki tiedostoon tekemäsi muutokset näkyvät vain sinulle.</span><span class="sxs-lookup"><span data-stu-id="2298d-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="2298d-118">Tallennettu</span><span class="sxs-lookup"><span data-stu-id="2298d-118">Saved</span></span>               | <span data-ttu-id="2298d-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2298d-119">Select **Save**.</span></span>           | <span data-ttu-id="2298d-120">Uloskuitattuun tiedostoon tehdyt muutokset tallennetaan tietokantaan, mutta asiakirjaa ei ole vielä kuitattu sisään tai julkaistu.</span><span class="sxs-lookup"><span data-stu-id="2298d-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="2298d-121">Tallennetut muutokset eivät näy muille todennetuille järjestelmäkäyttäjille ennen kuin laatija valitsee **Lopeta muokkaaminen**.</span><span class="sxs-lookup"><span data-stu-id="2298d-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="2298d-122">Ulkoiset käyttäjät eivät näe niitä, ennen kuin nimike on julkaistu.</span><span class="sxs-lookup"><span data-stu-id="2298d-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="2298d-123">Hylätty uloskuittaus</span><span class="sxs-lookup"><span data-stu-id="2298d-123">Discarded check out</span></span> | <span data-ttu-id="2298d-124">Valitse **Hylkää muokkaukset**.</span><span class="sxs-lookup"><span data-stu-id="2298d-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="2298d-125">Kaikki uloskuitattuun tiedostoon tehdyt muutokset hylätään, ja nimike palautuu viimeksi kuitattuun versioon.</span><span class="sxs-lookup"><span data-stu-id="2298d-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="2298d-126">Kuitattu sisään</span><span class="sxs-lookup"><span data-stu-id="2298d-126">Checked in</span></span>          | <span data-ttu-id="2298d-127">Valitse **Viimeistele muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="2298d-127">Select **Finish editing**.</span></span> | <span data-ttu-id="2298d-128">Muokattu asiakirja kuitataan sisään.</span><span class="sxs-lookup"><span data-stu-id="2298d-128">The edited document is checked in.</span></span> <span data-ttu-id="2298d-129">Kaikki muutokset näkyvät muille todennetuille järjestelmän käyttäjille, ja käyttäjät voivat muokata tiedostoa.</span><span class="sxs-lookup"><span data-stu-id="2298d-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="2298d-130">Jokainen sisäänkuittaus luo asiakirjaversiotietueen nimikkeen historiaan.</span><span class="sxs-lookup"><span data-stu-id="2298d-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="2298d-131">Julkaistu</span><span class="sxs-lookup"><span data-stu-id="2298d-131">Published</span></span>           | <span data-ttu-id="2298d-132">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="2298d-132">Select **Publish**.</span></span>        | <span data-ttu-id="2298d-133">Tiedosto julkaistaan, ja muutokset siirretään Live-sivustoon ja ulkoiset käyttäjät voivat löytää ne.</span><span class="sxs-lookup"><span data-stu-id="2298d-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="2298d-134">Nimikkeet voidaan julkaista vain, jos ne on ensin kuitattu sisään valitsemalla **Lopeta muokkaaminen**.</span><span class="sxs-lookup"><span data-stu-id="2298d-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="2298d-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2298d-135">Additional resources</span></span>

[<span data-ttu-id="2298d-136">Tapoja lisästä sisältöä</span><span class="sxs-lookup"><span data-stu-id="2298d-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="2298d-137">Sivumallisanasto</span><span class="sxs-lookup"><span data-stu-id="2298d-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="2298d-138">Julkaisuryhmien kanssa työskenteleminen</span><span class="sxs-lookup"><span data-stu-id="2298d-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="2298d-139">Moduulien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="2298d-139">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="2298d-140">Katkelmien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="2298d-140">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="2298d-141">Mallit ja asettelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2298d-141">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="2298d-142">Sivuston selauksen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="2298d-142">Customize site navigation</span></span>](customize-site-navigation.md)
