---
title: Alusta Retail-ympäristöissä alkutiedot
description: Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Dynamics 365 Commercein alustusprosessia.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e2833c32d557ec3d2dc80808222d1d47860ce6ea
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022431"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="cf8d3-103">Alkutietojen alustaminen uusissa Retail-ympäristöissä</span><span class="sxs-lookup"><span data-stu-id="cf8d3-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf8d3-104">Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Dynamics 365 Commercein alustusprosessia.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cf8d3-105">Kun Commerce-ratkaisu on otettu käyttöön Microsoft Dynamics Lifecycle Servicesin (LCS) kautta, sinun on alustettava Commerce-määritys luodaksesi peruskonfiguraation tiedot.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf8d3-106">Ennen kuin alustat kauppamäärityksen, varmista, että olet määrittänyt kielen ja postiosoitteen kullekin yritykselle, jolle määrität myymälöitä.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="cf8d3-107">Tämä vaihe on suoritettava kullekin yritykselle, jota käytät kauppaan.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="cf8d3-108">Alusta määritys noudattamalla seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="cf8d3-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="cf8d3-109">Käynnistä Commerce-asiakasohjelma.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="cf8d3-110">Valitse **Retail ja Commerce** &gt; **Pääkonttorin asetukset** &gt; **Parametrit** &gt; **Commerce-parametrit**.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="cf8d3-111">Napsauta **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-111">Click **Initialize**.</span></span>

<span data-ttu-id="cf8d3-112">Alustaminen luo seuraavat oletusmääritystiedot:</span><span class="sxs-lookup"><span data-stu-id="cf8d3-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="cf8d3-113">Commerce-ajastuksen työt ja alityöt</span><span class="sxs-lookup"><span data-stu-id="cf8d3-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="cf8d3-114">Kaupankäyntikanavan skeema</span><span class="sxs-lookup"><span data-stu-id="cf8d3-114">Commerce channel schema</span></span>
- <span data-ttu-id="cf8d3-115">Commercen jakeluaikataulut</span><span class="sxs-lookup"><span data-stu-id="cf8d3-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="cf8d3-116">Oletusmuotoiset näyttöasettelut, mukaan lukien painikeruudukot, kuvat ja teemat</span><span class="sxs-lookup"><span data-stu-id="cf8d3-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="cf8d3-117">Aikavyöhyketiedot</span><span class="sxs-lookup"><span data-stu-id="cf8d3-117">Time zone information</span></span>
- <span data-ttu-id="cf8d3-118">Myyntipisteen (POS) toiminnot:</span><span class="sxs-lookup"><span data-stu-id="cf8d3-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="cf8d3-119">Myyntipisteen käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="cf8d3-119">POS permissions</span></span>
- <span data-ttu-id="cf8d3-120">Kanavaraportit</span><span class="sxs-lookup"><span data-stu-id="cf8d3-120">Channel reports</span></span>
- <span data-ttu-id="cf8d3-121">Määritteen metatiedot</span><span class="sxs-lookup"><span data-stu-id="cf8d3-121">Attribute metadata</span></span>
- <span data-ttu-id="cf8d3-122">Yksikön tarkistusmallit</span><span class="sxs-lookup"><span data-stu-id="cf8d3-122">Entity validation templates</span></span>
- <span data-ttu-id="cf8d3-123">Erätyö Commerce Data Exchange -palvelun historiatietojen tyhjentämiseen</span><span class="sxs-lookup"><span data-stu-id="cf8d3-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="cf8d3-124">Lisäksi maksukorttiyrityksiin (PCI) liittyvät lokiinkirjaukset ovat käytössä Commercen tietokannassa.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="cf8d3-125">Commerce-ajastus voidaan määrittää erikseen.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="cf8d3-126">Tämä vaihtoehto mahdollistaa Commerce-ajastuksen määrityksen sen oletusasetuksille.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="cf8d3-127">Kun alustus on valmis, sinun määritettävä kaupan lisätiedot.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="cf8d3-128">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="cf8d3-128">Here are some examples:</span></span>

- <span data-ttu-id="cf8d3-129">Kaupankäynnin parametrit</span><span class="sxs-lookup"><span data-stu-id="cf8d3-129">Commerce parameters</span></span>
- <span data-ttu-id="cf8d3-130">Kaupankäynnin ajoitustyökalun parametrit</span><span class="sxs-lookup"><span data-stu-id="cf8d3-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="cf8d3-131">Commerce-kanavat</span><span class="sxs-lookup"><span data-stu-id="cf8d3-131">Commerce channels</span></span>
- <span data-ttu-id="cf8d3-132">Kassakoneet ja laitteet</span><span class="sxs-lookup"><span data-stu-id="cf8d3-132">Registers and devices</span></span>
- <span data-ttu-id="cf8d3-133">Valikoimat</span><span class="sxs-lookup"><span data-stu-id="cf8d3-133">Assortments</span></span>