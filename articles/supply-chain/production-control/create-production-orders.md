---
title: Tuotantotilauksen elinkaari – yleiskatsaus
description: Tuotantotilauksen luonnin yhteydessä käynnistetään pyyntö nimikkeen luomisen käynnistämiseksi. Tuotantotilaus sisältää tietoja tuotettavasta tuotteesta, määrästä sekä suunnitellusta valmistuspäivämäärästä. Se sisältää myös tietoja kulutettavista materiaaleista ja nimikkeen tuottamisessa käytettävästä prosessista.
author: johanhoffmann
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79b1866cdca885d408aca07c546ca54aa0c3616b
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865187"
---
# <a name="production-order-lifecycle-overview"></a><span data-ttu-id="9aa17-105">Tuotantotilauksen elinkaari – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9aa17-105">Production order lifecycle overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9aa17-106">Tuotantotilauksen luonnin yhteydessä käynnistetään pyyntö nimikkeen luomisen käynnistämiseksi.</span><span class="sxs-lookup"><span data-stu-id="9aa17-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="9aa17-107">Tuotantotilaus sisältää tietoja tuotettavasta tuotteesta, määrästä sekä suunnitellusta valmistuspäivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="9aa17-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="9aa17-108">Se sisältää myös tietoja kulutettavista materiaaleista ja nimikkeen tuottamisessa käytettävästä prosessista.</span><span class="sxs-lookup"><span data-stu-id="9aa17-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="9aa17-109">Tuotantotilaus etenee tuotannon elinkaaren vaiheesta toiseen.</span><span class="sxs-lookup"><span data-stu-id="9aa17-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="9aa17-110">Kun tilaus luodaan, sen tilaksi määritetään **Luotu**.</span><span class="sxs-lookup"><span data-stu-id="9aa17-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="9aa17-111">Kun tilaus on valmis, sen tilaksi määritetään **Päättynyt**.</span><span class="sxs-lookup"><span data-stu-id="9aa17-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="9aa17-112">Käyttäjä voi määrittää kunkin vaiheen kyseisen vaiheen parametriasetuksella.</span><span class="sxs-lookup"><span data-stu-id="9aa17-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="9aa17-113">Asetus voidaan määrittää yhdelle käyttäjälle tai kaikille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="9aa17-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="9aa17-114">Tuotannon tuoterakenne ja tuotantoreititys ovat tuotantotilauksen tärkeimmät yksiköt.</span><span class="sxs-lookup"><span data-stu-id="9aa17-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="9aa17-115">Ne kopioidaan tuotantotilaukseen tuotettavaksi valitun nimikkeen ja määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="9aa17-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="9aa17-116">Tuotannon tuoterakennetta ja reititystä voidaan muokata ennen tuotantotilauksen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="9aa17-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="9aa17-117">Tuotantotilaus voidaan luoda seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="9aa17-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="9aa17-118">Luotu toteuttamalla materiaaliin kysyntään perustuva pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="9aa17-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="9aa17-119">Luotu suoraan myyntitilausriviltä tai luotaessa ja arvioitaessa ylemmän tason tuotantotilaus (tarvekohdistus).</span><span class="sxs-lookup"><span data-stu-id="9aa17-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="9aa17-120">Luo manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="9aa17-120">Created manually.</span></span>




