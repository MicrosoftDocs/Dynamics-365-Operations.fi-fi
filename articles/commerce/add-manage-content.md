---
title: Tapoja lisästä sisältöä
description: Tässä ohjeaiheessa käsitellään yleisesti sisällönhallinnan aloittamista käyttämällä Microsoft Dynamics 365 Commercen sivustonmuodostimen verkonmuokkaustyökaluja sekä annetaan joitakin asiaan liittyviä linkkejä.
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
ms.openlocfilehash: eb0b1c3f77bb71ba04c9110ed25fb80c2f2e61f4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208060"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="78db4-103">Tapoja lisästä sisältöä</span><span class="sxs-lookup"><span data-stu-id="78db4-103">Ways to add content</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="78db4-104">Tässä ohjeaiheessa käsitellään yleisesti sisällönhallintaa käyttämällä Microsoft Dynamics 365 Commercen sivustonmuodostimen verkonmuokkaustyökaluja sekä annetaan linkkejä asiaan liittyvään ohjeistukseen.</span><span class="sxs-lookup"><span data-stu-id="78db4-104">This topic provides an overview and links to documentation about how to manage content using the Microsoft Dynamics 365 Commerce site builder web authoring toolset.</span></span>

## <a name="overview"></a><span data-ttu-id="78db4-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="78db4-105">Overview</span></span>

<span data-ttu-id="78db4-106">Sivuston ulkoasua, ulkoasua ja sisältöä voi muuttaa monella tavalla.</span><span class="sxs-lookup"><span data-stu-id="78db4-106">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="78db4-107">Tarvittavan mukautustason mukaan monien näiden muutosten toteuttaminen on mahdollista myös muille kuin kehittäjälle käyttämällä sivustonmuodostinta, joka on Dynamics 365 Commerceen sisältävä verkonmuokkaustyökalupaketti.</span><span class="sxs-lookup"><span data-stu-id="78db4-107">Depending on the required level of customization, many of these changes can be implemented by non-developers within site builder, the web authoring toolset included with Dynamics 365 Commerce.</span></span> <span data-ttu-id="78db4-108">Sivustonmuodostimessa voi muodostaa malleja, valita teemoja sekä valita ja määrittää moduuleja koodia kirjoittamatta.</span><span class="sxs-lookup"><span data-stu-id="78db4-108">Site builder enables you to build templates, select themes, and select and configure modules without writing any code.</span></span> <span data-ttu-id="78db4-109">Sen sijaan kehitystaitoja vaaditaan uuden teeman tai moduulin luomisessa, koska sähköisen kaupankäynnin SDK:n ja Microsoft Dynamics Lifecycle Services (LCS) -palvelun kehitystyönkulkua on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="78db4-109">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="78db4-110">Seuraavat ohjeaiheet ovat hyviä lähtökohtia, jotka auttavat ymmärtämään, miten sivuston sisältöä lisätään ja hallitaan.</span><span class="sxs-lookup"><span data-stu-id="78db4-110">The following topics are good jumping off points to start understanding how to add and manage site content.</span></span> <span data-ttu-id="78db4-111">Useimmat mainitut ohjeaiheet keskittyvät sivuston alueille, joiden käyttöön ei tarvita kehittäjää.</span><span class="sxs-lookup"><span data-stu-id="78db4-111">Most of the topics listed focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="78db4-112">Joissakin käsitellään perustason sisällön muokkausta, kun taas toiset keskittyvät sivuston ylläpitotehtäviin.</span><span class="sxs-lookup"><span data-stu-id="78db4-112">Some address basic content editing, while others focus on site administrator tasks.</span></span> <span data-ttu-id="78db4-113">Kussakin ohjeaiheessa mainitaan, jos tietyt tehtävät voivat edellyttää SDK-tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="78db4-113">Each of these topics will denote specific tasks might require SDK work.</span></span> <span data-ttu-id="78db4-114">Kussakin ohjeaiheessa oletetaan, että sivusto on jo valmisteltu ja että sivuston sivustonmuodostimen työkalujen käyttöoikeus on saatu.</span><span class="sxs-lookup"><span data-stu-id="78db4-114">Each topic assumes that you have already provisioned a site and been granted access to the site builder toolset for your site.</span></span>

<span data-ttu-id="78db4-115">Aloita valitsemalla jokin seuraavista ohjeaiheista.</span><span class="sxs-lookup"><span data-stu-id="78db4-115">Select one of the following topics to get started.</span></span>

- <span data-ttu-id="78db4-116">Voit tutustua sivustonmuodostimessa ja tässä ohjeistuksessa käytettyihin sisällönhallinnan terminologiaa kohdassa [Sivumallisanasto](page-elements-overview.md).</span><span class="sxs-lookup"><span data-stu-id="78db4-116">To familiarize yourself with the content management terminology used in site builder and within this documentation, see [Page model glossary](page-elements-overview.md).</span></span>
- <span data-ttu-id="78db4-117">Lisätietoja moduulien toiminnasta sisällönhallinnan työnkuluissa on kohdassa [Moduulien käyttäminen](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="78db4-117">To understand how modules work within content management workflows, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="78db4-118">Lisätietoja aiemmin luodun sivustosivun tekstin, kuvien tai videoiden muuttamisesta on kohdassa [Moduulien käsitteleminen](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="78db4-118">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="78db4-119">Lisätietoja sisällönhallinnan tehostamisesta ja joustavuuden lisäämisestä katkelmien avulla on kohdassa [Katkelmien käyttäminen](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="78db4-119">To see how fragments can make content management more efficient and flexible, see [Work with fragments](work-with-fragments.md).</span></span>
- <span data-ttu-id="78db4-120">Lisätietoja verkkosisällön tekijöiden brändinmukaisesta sisällön tuottamisesta on kohdissa [Mallit ja asettelut – yleiskatsaus](templates-layouts-overview.md) ja [Mallien käyttäminen](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="78db4-120">To help ensure a successful on-brand authoring experience for web content authors, see [Templates and layouts overview](templates-layouts-overview.md) and [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="78db4-121">Lisätietoja sivustosivun osien uudelleenjärjestämisestä on kohdassa [Asettelujen käsitteleminen](work-with-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="78db4-121">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="78db4-122">Lisätietoja sivustosivujen fonttien, värien ja yleisen ulkoasun muuttamisesta on kohdassa [Sivuston teeman valitseminen](select-site-theme.md) tai [Työskentely CSS-korvaustiedostojen kanssa](css-override-files.md).</span><span class="sxs-lookup"><span data-stu-id="78db4-122">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md) or [Work with CSS over-ride files](css-override-files.md).</span></span>
- <span data-ttu-id="78db4-123">Lisätietoja siirtymisvaihtoehtojen järjestämisestä uudelleen tai uusien lisäämisestä on kohdassa [Sivuston selauksen mukauttaminen](customize-site-navigation.md).</span><span class="sxs-lookup"><span data-stu-id="78db4-123">To rearrange or add new navigation options, see [Customize site navigation](customize-site-navigation.md).</span></span>
- <span data-ttu-id="78db4-124">Lisätietoja monenlaisten rinnakkaisten verkkosisällön muutosten vaiheistamisesta, esikatselemisesta ja julkaisemisesta on kohdassa [Julkaisuryhmien kanssa työskenteleminen](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="78db4-124">To learn how to stage, preview, and publish a broad set of concurrent web content changes, see [Work with publish groups](publish-groups.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="78db4-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="78db4-125">Additional resources</span></span>

[<span data-ttu-id="78db4-126">Muokkaussivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="78db4-126">Authoring page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="78db4-127">Sivumallisanasto</span><span class="sxs-lookup"><span data-stu-id="78db4-127">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="78db4-128">Asiakirjan tilat ja elinkaari</span><span class="sxs-lookup"><span data-stu-id="78db4-128">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="78db4-129">Kanavienvälisen jakamisen käyttöönottaminen ja käyttäminen</span><span class="sxs-lookup"><span data-stu-id="78db4-129">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]