---
title: Asiakirjan tilat ja elinkaari
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen sivuelementtien eri asiakirjatiloista.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 457b1ac7afb8cad57399572acf429d208db917af
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230531"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="2fc5e-103">Asiakirjan tilat ja elinkaari</span><span class="sxs-lookup"><span data-stu-id="2fc5e-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2fc5e-104">Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen sivuelementtien eri asiakirjatiloista.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="2fc5e-105">Asiakirjan tilan kuvaukset</span><span class="sxs-lookup"><span data-stu-id="2fc5e-105">Document state descriptions</span></span>

<span data-ttu-id="2fc5e-106">[Sivuelementit](page-elements-overview.md)-ohjeaiheessa on sisällönhallintajärjestelmän (CMS) eri asiakirjatyyppejä.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="2fc5e-107">Näillä asiakirjatyypeillä voi olla useita tiloja muokkaustyökalussa.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="2fc5e-108">Asiakirjan tilat auttavat estämään tietoristiriitoja ja ottavat käyttöön versionhallinnan.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="2fc5e-109">Ne määrittävät, ketkä voivat muuttaa asiakirjoja, milloin asiakirjoja voi muuttaa ja milloin muut voivat tarkastella muutoksia.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="2fc5e-110">Seuraavassa taulukossa esitetään sivuelementtien mahdolliset asiakirjojen tilat Commercessa.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="2fc5e-111">Asiakirjan tila</span><span class="sxs-lookup"><span data-stu-id="2fc5e-111">Document state</span></span>      | <span data-ttu-id="2fc5e-112">Sivustonmuodostimen toiminta</span><span class="sxs-lookup"><span data-stu-id="2fc5e-112">Site builder action</span></span>        | <span data-ttu-id="2fc5e-113">kuvaus</span><span class="sxs-lookup"><span data-stu-id="2fc5e-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="2fc5e-114">Kuitattu ulos</span><span class="sxs-lookup"><span data-stu-id="2fc5e-114">Checked out</span></span>         | <span data-ttu-id="2fc5e-115">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-115">Select **Edit**.</span></span>           | <span data-ttu-id="2fc5e-116">Asiakirja kuitataan ulos.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="2fc5e-117">Kun asiakirja on tässä tilassa, muut todennetut järjestelmän käyttäjät eivät voi muuttaa sitä, ja kaikki tiedostoon tekemäsi muutokset näkyvät vain sinulle.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="2fc5e-118">Tallennettu</span><span class="sxs-lookup"><span data-stu-id="2fc5e-118">Saved</span></span>               | <span data-ttu-id="2fc5e-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-119">Select **Save**.</span></span>           | <span data-ttu-id="2fc5e-120">Uloskuitattuun tiedostoon tehdyt muutokset tallennetaan tietokantaan, mutta asiakirjaa ei ole vielä kuitattu sisään tai julkaistu.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="2fc5e-121">Tallennetut muutokset eivät näy muille todennetuille järjestelmäkäyttäjille ennen kuin laatija valitsee **Lopeta muokkaaminen**.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="2fc5e-122">Ulkoiset käyttäjät eivät näe niitä, ennen kuin nimike on julkaistu.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="2fc5e-123">Hylätty uloskuittaus</span><span class="sxs-lookup"><span data-stu-id="2fc5e-123">Discarded check out</span></span> | <span data-ttu-id="2fc5e-124">Valitse **Hylkää muokkaukset**.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="2fc5e-125">Kaikki uloskuitattuun tiedostoon tehdyt muutokset hylätään, ja nimike palautuu viimeksi kuitattuun versioon.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="2fc5e-126">Kuitattu sisään</span><span class="sxs-lookup"><span data-stu-id="2fc5e-126">Checked in</span></span>          | <span data-ttu-id="2fc5e-127">Valitse **Viimeistele muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-127">Select **Finish editing**.</span></span> | <span data-ttu-id="2fc5e-128">Muokattu asiakirja kuitataan sisään.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-128">The edited document is checked in.</span></span> <span data-ttu-id="2fc5e-129">Kaikki muutokset näkyvät muille todennetuille järjestelmän käyttäjille, ja käyttäjät voivat muokata tiedostoa.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="2fc5e-130">Jokainen sisäänkuittaus luo asiakirjaversiotietueen nimikkeen historiaan.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="2fc5e-131">Julkaistu</span><span class="sxs-lookup"><span data-stu-id="2fc5e-131">Published</span></span>           | <span data-ttu-id="2fc5e-132">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-132">Select **Publish**.</span></span>        | <span data-ttu-id="2fc5e-133">Tiedosto julkaistaan, ja muutokset siirretään Live-sivustoon ja ulkoiset käyttäjät voivat löytää ne.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="2fc5e-134">Nimikkeet voidaan julkaista vain, jos ne on ensin kuitattu sisään valitsemalla **Lopeta muokkaaminen**.</span><span class="sxs-lookup"><span data-stu-id="2fc5e-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="2fc5e-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2fc5e-135">Additional resources</span></span>

[<span data-ttu-id="2fc5e-136">Tapoja lisästä sisältöä</span><span class="sxs-lookup"><span data-stu-id="2fc5e-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="2fc5e-137">Sivumallisanasto</span><span class="sxs-lookup"><span data-stu-id="2fc5e-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="2fc5e-138">Julkaisuryhmien kanssa työskenteleminen</span><span class="sxs-lookup"><span data-stu-id="2fc5e-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="2fc5e-139">Kanavienvälisen jakamisen käyttöönottaminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="2fc5e-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="2fc5e-140">Moduulien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="2fc5e-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="2fc5e-141">Katkelmien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="2fc5e-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="2fc5e-142">Mallit ja asettelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2fc5e-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="2fc5e-143">Sivuston selauksen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="2fc5e-143">Customize site navigation</span></span>](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]