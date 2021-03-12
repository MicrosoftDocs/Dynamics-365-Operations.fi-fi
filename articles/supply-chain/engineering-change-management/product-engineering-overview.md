---
title: Suunnittelun muutostenhallinnan yleiskuvaus
description: Tässä aiheessa on yleiskatsaus suunnittelun muutostenhallintaan, jonka avulla voi suunnitella ja hallita tuotteen versiointia sekä hallita tuotteen elinkaaria ja suunnittelun muutoksia.
author: t-benebo
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b081cd8d56217b8cf76db824c29482d453fc9ea3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001945"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="eb6cb-103">Suunnittelun muutostenhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="eb6cb-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="eb6cb-104">Toiminnon yhteenveto</span><span class="sxs-lookup"><span data-stu-id="eb6cb-104">Feature summary</span></span>

<span data-ttu-id="eb6cb-105">Valmistajat tarvitset nykyisin tehokasta tuotetietojen hallintaa, versionhallintaa ja suunnittelun muutoksenhallintaa, jotta ne menestyisivät jatkuvasti lyhenevistä tuotteiden elinkaaresta, kasvavista laatu- ja luotettavuusvaatimuksista sekä entistä tarkemmasta tuotteiden turvallisuustarkkailusta huolimatta.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="eb6cb-106">Suunnittelun muutostenhallinta tuo rakennetta ja täsmällisyyttä tuotetietojen hallintaprosessiin sekä mahdollistaa tuotteiden hallitun määrittämisen, vapauttamisen ja korjaamiseen työnkulkujen avulla.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="eb6cb-107"> Tuoteversioiden ja suunnittelun muutostenhallinnan ansiosta suunnittelun muutokset voidaan dokumentoida, niiden vaikutus voidaan arvioida ja ne voidaan ottaa käyttöön koko tuotteen elinkaaren ajan.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="eb6cb-108">Suunnittelun muutostenhallinta auttaa suunnittelemaan ja hallitsemaan tuotteen versiointia sekä hallitsemaan tuotteen elinkaaria ja suunnittelun muutoksia.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="eb6cb-109">Tärkeimmät toiminnot:</span><span class="sxs-lookup"><span data-stu-id="eb6cb-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="eb6cb-110">Tuotteen versiointi</span><span class="sxs-lookup"><span data-stu-id="eb6cb-110">Product versioning</span></span>
- <span data-ttu-id="eb6cb-111">Parannettujen tuotteen vapautustoimintojen avulla voidaan ylläpitää tuotteen päätietoja yhdessä yrityksessä (suunnitteluyritys) ja julkaista täysin määritetyt vapautetut tuotteet muihin yrityksiin</span><span class="sxs-lookup"><span data-stu-id="eb6cb-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="eb6cb-112">Säännöt, joilla tarkistetaan, että pakolliset tiedot on annettu ennen tuoteversion aktivointia (valmiustarkistukset)</span><span class="sxs-lookup"><span data-stu-id="eb6cb-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="eb6cb-113">Parannettu tuotteen elinkaaren hallinta valvomalla tarkasti, milloin vapautettua tuotetta voidaan käyttää tietyissä liiketoimintaprosesseissa</span><span class="sxs-lookup"><span data-stu-id="eb6cb-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="eb6cb-114">Työnkulkujen tukemat suunnittelun muutospyynnöt</span><span class="sxs-lookup"><span data-stu-id="eb6cb-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="eb6cb-115">Työnkulkujen tukemat suunnittelun muutostilaukset</span><span class="sxs-lookup"><span data-stu-id="eb6cb-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="eb6cb-116">Edellä oleva video ([Dynamics 365 Supply Chain Managementin muutostenhallinnan ominaisuudet](https://youtu.be/N313FqvRuBc)) sisältyy [Finance and Operations -toistoluetteloon](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on saatavana YouTubessa.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-engineering-change-management-for-your-system"></a><span data-ttu-id="eb6cb-117">Järjestelmän suunnittelun muutostenhallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="eb6cb-117">Turn on engineering change management for your system</span></span>

<span data-ttu-id="eb6cb-118">Ota ensimmäiseksi muutostenhallinta käyttöön seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-118">First, turn on engineering change management by following these steps.</span></span>

1. <span data-ttu-id="eb6cb-119">Mene [Toimintojen hallintaan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eb6cb-119">Go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
1. <span data-ttu-id="eb6cb-120">Tarkista päivitysten saatavuus.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-120">Check for updates.</span></span>
1. <span data-ttu-id="eb6cb-121">Ota käyttöön **Suunnittelun muutostenhallinta** -niminen toiminto.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-121">Turn on the feature that is named **Engineering Change Management**.</span></span>

<span data-ttu-id="eb6cb-122">Ota seuraavaksi käyttöön **suunnittelun muutostenhallinnan** määritysavain seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-122">Next, turn on the **Engineering Change Management** configuration key by following these steps.</span></span>

1. <span data-ttu-id="eb6cb-123">Siirrä järjestelmä ylläpitotilaan kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-123">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="eb6cb-124">Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-124">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="eb6cb-125">Laajenna **Kauppa**-solmu ja valitse **Suunnittelun muutostenhallinta** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-125">Expand the **Trade** node, and select the **Engineering Change Management** check box.</span></span>
1. <span data-ttu-id="eb6cb-126">Poista järjestelmän ylläpitotila käytöstä kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-126">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
