---
title: Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (17. syyskuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talent Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 09/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6586761fc62c13c701e8a8f61e15eedc66e2f751
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304227"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-17-2018"></a><span data-ttu-id="9e590-103">Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (17. syyskuuta 2018)</span><span class="sxs-lookup"><span data-stu-id="9e590-103">What's new or changed in Dynamics 365 for Talent Core HR (September 17, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9e590-104">**Koontiversio 8.1.154.0**</span><span class="sxs-lookup"><span data-stu-id="9e590-104">**Build 8.1.154.0**</span></span>

<span data-ttu-id="9e590-105">Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="9e590-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a><span data-ttu-id="9e590-106">Lomat ja poissaolot – Jaksotettu aika työtuntien mukaan</span><span class="sxs-lookup"><span data-stu-id="9e590-106">Leave and Absence – Accrue time based on hours worked</span></span>

<span data-ttu-id="9e590-107">Lomasuunnitelmiin on lisätty uusi jaksotustyyppi.</span><span class="sxs-lookup"><span data-stu-id="9e590-107">A new accrual type has been added to Leave plans.</span></span> <span data-ttu-id="9e590-108">Jaksotusaikataulu voi nyt perustua palvelukuukausiin tai työtunteihin.</span><span class="sxs-lookup"><span data-stu-id="9e590-108">The accrual schedule can now be based on months of service or hours worked.</span></span> <span data-ttu-id="9e590-109">Lisätietoja on kohdassa [Jaksotettu poissaolo työtuntien mukaan](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="9e590-109">For more information, see [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

## <a name="platform-update-18"></a><span data-ttu-id="9e590-110">Ympäristöpäivitys 18</span><span class="sxs-lookup"><span data-stu-id="9e590-110">Platform update 18</span></span>

<span data-ttu-id="9e590-111">Ympäristöpäivitys 18 on nyt osa Talent-versiota.</span><span class="sxs-lookup"><span data-stu-id="9e590-111">Platform update 18 is now part of the Talent release.</span></span> 

-   <span data-ttu-id="9e590-112">Pakolliset ja muut kentät voidaan piilottaa mukautuksen kautta.</span><span class="sxs-lookup"><span data-stu-id="9e590-112">Mandatory and other fields can be hidden via personalization.</span></span> <span data-ttu-id="9e590-113">Käyttäjä voi näin luoda yksinkertaistetun kokemuksen, jossa liiketoimintalogiikan oletusarvojen mukaan määritettyjä pakollisia kenttiä ei näytetä.</span><span class="sxs-lookup"><span data-stu-id="9e590-113">This allows a user to create a simplified experience where mandatory fields that are defaulted by business logic are not shown.</span></span> <span data-ttu-id="9e590-114">Pakolliset piilotetut kentät näkyvät myös tilapäisesti, jos ne ovat tyhjiä, kun yritetään tallennusta.</span><span class="sxs-lookup"><span data-stu-id="9e590-114">Hidden mandatory fields are also temporarily made visible if they are empty when a save is attempted.</span></span>

-   <span data-ttu-id="9e590-115">Ympäristöpäivityksessä 18 Talent-verkkoasiakasohjelma kohdistaa nyt sen visuaaliset elementit Microsoft Fluent Designin kanssa.</span><span class="sxs-lookup"><span data-stu-id="9e590-115">In Platform update 18, the Talent web client now aligns its visuals with Microsoft Fluent Design.</span></span>

    -   <span data-ttu-id="9e590-116">Kun kentät ovat "Luku-tilassa", voit siirtyä muokkaukseen valitsemalla kentissä muokkausvaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="9e590-116">When fields are in “read mode”, you can simply select the edit option in the fields to switch the form to edit.</span></span>

    -   <span data-ttu-id="9e590-117">Muutokset siihen, miten kentät näkyvät Luku-tilassa.</span><span class="sxs-lookup"><span data-stu-id="9e590-117">Changes in how fields display when in read mode.</span></span>

    -   <span data-ttu-id="9e590-118">Työtilojen ja sivujen otsikot näkyvät lihavoituna.</span><span class="sxs-lookup"><span data-stu-id="9e590-118">Headings in workspaces and pages are bold.</span></span>

-   <span data-ttu-id="9e590-119">Hakujen korvaamattomuustoimintoa on parannettu.</span><span class="sxs-lookup"><span data-stu-id="9e590-119">The behavior of non-replacing lookups has been improved.</span></span> <span data-ttu-id="9e590-120">Lisätietoja on kohdassa [Hakujen korvaamattomuustoiminnon parantaminen](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span><span class="sxs-lookup"><span data-stu-id="9e590-120">For more information, see [Improved behavior for non-replacing lookups](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span></span>

## <a name="bug-fixes"></a><span data-ttu-id="9e590-121">Ohjelmavirhekorjaukset</span><span class="sxs-lookup"><span data-stu-id="9e590-121">Bug fixes</span></span>

<span data-ttu-id="9e590-122">Tämä versio sisältää useita muita ohjelmavirhekorjauksia, mukaan lukien viittaukset ACA:aan, ADA:aan ja I9:een ovat nyt käytössä vain yhdysvaltalaisissa yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="9e590-122">This release includes several additional bug fixes, including references to ACA, ADA, and I9 now will only be enabled in US companies.</span></span>
