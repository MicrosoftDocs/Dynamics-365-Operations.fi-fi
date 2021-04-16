---
title: Alkutietojen alustaminen uusissa Commerce-ympäristöissä
description: Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Dynamics 365 Commercen alustusprosessia.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9f534410b21fd97554f4e038bb14eebd5f887130
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792580"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="5f8df-103">Alkutietojen alustaminen uusissa Commerce-ympäristöissä</span><span class="sxs-lookup"><span data-stu-id="5f8df-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5f8df-104">Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Dynamics 365 Commercen alustusprosessia.</span><span class="sxs-lookup"><span data-stu-id="5f8df-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5f8df-105">Kun Commerce-ratkaisu on otettu käyttöön Microsoft Dynamics Lifecycle Servicesin (LCS) kautta, sinun on alustettava Commerce-määritys luodaksesi peruskonfiguraation tiedot.</span><span class="sxs-lookup"><span data-stu-id="5f8df-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f8df-106">Ennen kuin alustat kauppamäärityksen, varmista, että olet määrittänyt kielen ja postiosoitteen kullekin yritykselle, jolle määrität myymälöitä.</span><span class="sxs-lookup"><span data-stu-id="5f8df-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="5f8df-107">Tämä vaihe on suoritettava kullekin yritykselle, jota käytät kauppaan.</span><span class="sxs-lookup"><span data-stu-id="5f8df-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="5f8df-108">Alusta määritys noudattamalla seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="5f8df-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="5f8df-109">Käynnistä Commerce-asiakasohjelma.</span><span class="sxs-lookup"><span data-stu-id="5f8df-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="5f8df-110">Valitse **Retail ja Commerce** &gt; **Pääkonttorin asetukset** &gt; **Parametrit** &gt; **Commerce-parametrit**.</span><span class="sxs-lookup"><span data-stu-id="5f8df-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="5f8df-111">Napsauta **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="5f8df-111">Click **Initialize**.</span></span>

<span data-ttu-id="5f8df-112">Alustaminen luo seuraavat oletusmääritystiedot:</span><span class="sxs-lookup"><span data-stu-id="5f8df-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="5f8df-113">Commerce-ajastuksen työt ja alityöt</span><span class="sxs-lookup"><span data-stu-id="5f8df-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="5f8df-114">Kaupankäyntikanavan skeema</span><span class="sxs-lookup"><span data-stu-id="5f8df-114">Commerce channel schema</span></span>
- <span data-ttu-id="5f8df-115">Commercen jakeluaikataulut</span><span class="sxs-lookup"><span data-stu-id="5f8df-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="5f8df-116">Oletusmuotoiset näyttöasettelut, mukaan lukien painikeruudukot, kuvat ja teemat</span><span class="sxs-lookup"><span data-stu-id="5f8df-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="5f8df-117">Aikavyöhyketiedot</span><span class="sxs-lookup"><span data-stu-id="5f8df-117">Time zone information</span></span>
- <span data-ttu-id="5f8df-118">Myyntipisteen (POS) toiminnot:</span><span class="sxs-lookup"><span data-stu-id="5f8df-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="5f8df-119">Myyntipisteen käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="5f8df-119">POS permissions</span></span>
- <span data-ttu-id="5f8df-120">Kanavaraportit</span><span class="sxs-lookup"><span data-stu-id="5f8df-120">Channel reports</span></span>
- <span data-ttu-id="5f8df-121">Määritteen metatiedot</span><span class="sxs-lookup"><span data-stu-id="5f8df-121">Attribute metadata</span></span>
- <span data-ttu-id="5f8df-122">Yksikön tarkistusmallit</span><span class="sxs-lookup"><span data-stu-id="5f8df-122">Entity validation templates</span></span>
- <span data-ttu-id="5f8df-123">Erätyö Commerce Data Exchange -palvelun historiatietojen tyhjentämiseen</span><span class="sxs-lookup"><span data-stu-id="5f8df-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="5f8df-124">Lisäksi maksukorttiyrityksiin (PCI) liittyvät lokiinkirjaukset ovat käytössä Commercen tietokannassa.</span><span class="sxs-lookup"><span data-stu-id="5f8df-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="5f8df-125">Commerce-ajastus voidaan määrittää erikseen.</span><span class="sxs-lookup"><span data-stu-id="5f8df-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="5f8df-126">Tämä vaihtoehto mahdollistaa Commerce-ajastuksen määrityksen sen oletusasetuksille.</span><span class="sxs-lookup"><span data-stu-id="5f8df-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="5f8df-127">Kun alustus on valmis, sinun määritettävä kaupan lisätiedot.</span><span class="sxs-lookup"><span data-stu-id="5f8df-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="5f8df-128">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="5f8df-128">Here are some examples:</span></span>

- <span data-ttu-id="5f8df-129">Kaupankäynnin parametrit</span><span class="sxs-lookup"><span data-stu-id="5f8df-129">Commerce parameters</span></span>
- <span data-ttu-id="5f8df-130">Kaupankäynnin ajoitustyökalun parametrit</span><span class="sxs-lookup"><span data-stu-id="5f8df-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="5f8df-131">Commerce-kanavat</span><span class="sxs-lookup"><span data-stu-id="5f8df-131">Commerce channels</span></span>
- <span data-ttu-id="5f8df-132">Kassakoneet ja laitteet</span><span class="sxs-lookup"><span data-stu-id="5f8df-132">Registers and devices</span></span>
- <span data-ttu-id="5f8df-133">Valikoimat</span><span class="sxs-lookup"><span data-stu-id="5f8df-133">Assortments</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]