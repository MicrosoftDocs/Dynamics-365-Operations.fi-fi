---
title: Tuotantotilausten vapauttaminen
description: Vapautettu tuotantotilaus on tilaus, joka on hyväksytty tuotantoon. Termillä "Vapautettu" kuvataan tuotantotilauksen elinkaaren tilaa, jossa tuotantotilaus voidaan suorittaa tuotannossa ja varastoprosesseissa.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 400c2786d80681827829286e6e9667b4d51612c4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "339369"
---
# <a name="release-production-orders"></a><span data-ttu-id="50f2b-104">Tuotantotilausten vapauttaminen</span><span class="sxs-lookup"><span data-stu-id="50f2b-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50f2b-105">Vapautettu tuotantotilaus on tilaus, joka on hyväksytty tuotantoon.</span><span class="sxs-lookup"><span data-stu-id="50f2b-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="50f2b-106">Termillä "Vapautettu" kuvataan tuotantotilauksen elinkaaren tilaa, jossa tuotantotilaus voidaan suorittaa tuotannossa ja varastoprosesseissa.</span><span class="sxs-lookup"><span data-stu-id="50f2b-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span> 

<a name="characteristics-of-the-released-state"></a><span data-ttu-id="50f2b-107">Vapautettu-tilan ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="50f2b-107">Characteristics of the Released state</span></span>
-------------------------------------

<span data-ttu-id="50f2b-108">**Vapautettu**-tila on yksi tuotantotilauksen elinkaaren tiloista.</span><span class="sxs-lookup"><span data-stu-id="50f2b-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="50f2b-109">Tuotantotilaukset, joiden tilana on **Vapautettu**, voidaan suorittaa tuotannossa ja varastoprosesseissa.</span><span class="sxs-lookup"><span data-stu-id="50f2b-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="50f2b-110">**Vapautettu**-tilalla on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="50f2b-110">The **Released** state has the following characteristics:</span></span>

-   <span data-ttu-id="50f2b-111">Tuotantotila voidaan siirtää **Vapautettu**-tilaan tuotantotilauksesta tai eräprosessin avulla.</span><span class="sxs-lookup"><span data-stu-id="50f2b-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="50f2b-112">Tuotantotilaus voidaan myös päivittää automaattisesti suunnitelluista tuotantotilauksista, jotka on vahvistettu **Vahvistuksen aikaraja** -kentässä **Pääsuunnitelma**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="50f2b-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
-   <span data-ttu-id="50f2b-113">**Vapautettu**-tila osoittaa tuotannon käyttäjille (operaattoreille), että tuotantotyöt voidaan aloittaa.</span><span class="sxs-lookup"><span data-stu-id="50f2b-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
-   <span data-ttu-id="50f2b-114">Tuotannon dokumentit, kuten reitityskortit ja -työt sekä työkortit sisältävät tuotantotöitä koskevia tietoja, ja niitä voidaan lähettää.</span><span class="sxs-lookup"><span data-stu-id="50f2b-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
-   <span data-ttu-id="50f2b-115">Fyysisesti varatuille materiaaleille luodaan varastotyö, jolla materiaalit kerätään tuotantotilausta varten.</span><span class="sxs-lookup"><span data-stu-id="50f2b-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="50f2b-116">Töiden vapauttaminen tuotantoon</span><span class="sxs-lookup"><span data-stu-id="50f2b-116">Releasing jobs to the shop floor</span></span>
<span data-ttu-id="50f2b-117">Kun tuotantotilaus on vapautettu, siihen liittyvät tuotantotyöt ovat näkyvissä ja valmiina rekisteröitäviksi.</span><span class="sxs-lookup"><span data-stu-id="50f2b-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="50f2b-118">Operaattorit voivat tehdä työrekisteröintejä, kuten Käynnistä, Pysäytä ja Valmistuminen, joko **Työkorttipääte**- tai **Työkorttilaite**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="50f2b-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="50f2b-119">Rekisteröity aika ja määrä siirretään automaattisesti rekisteröintisivuilta tuotantokirjauskansioihin, jotta käytettyä aikaa ja määrää voidaan seurata.</span><span class="sxs-lookup"><span data-stu-id="50f2b-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="50f2b-120">Reitityskortit</span><span class="sxs-lookup"><span data-stu-id="50f2b-120">Route cards</span></span>
<span data-ttu-id="50f2b-121">Reitityskortissa on yhteenveto reitityksen ja työvaiheen asetuksista sekä työvaiheen ja työn ajoitusmenetelmistä saatavista tiedoista.</span><span class="sxs-lookup"><span data-stu-id="50f2b-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="50f2b-122">Reititystyöt</span><span class="sxs-lookup"><span data-stu-id="50f2b-122">Route jobs</span></span>
<span data-ttu-id="50f2b-123">Reititystyö luetteloi työvaiheen kunkin työn tarkat tiedot sekä asetus-, käsittely-, jonotus- ja kuljetusajat.</span><span class="sxs-lookup"><span data-stu-id="50f2b-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="50f2b-124">Esimerkiksi maalaaminen on työvaihe, johon saatetaan tarvita yksittäisiä töitä, kuten asetusaika, maalausprosessin suoritusaika ja kuivumisen jonotusaika.</span><span class="sxs-lookup"><span data-stu-id="50f2b-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="50f2b-125">Työkortit</span><span class="sxs-lookup"><span data-stu-id="50f2b-125">Job cards</span></span>
<span data-ttu-id="50f2b-126">Työkortti luetteloi tietyn työvaiheen yksittäiset työnumerot.</span><span class="sxs-lookup"><span data-stu-id="50f2b-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="50f2b-127">Kullakin sivulla näkyy yksi työ.</span><span class="sxs-lookup"><span data-stu-id="50f2b-127">One job appears on each page.</span></span> <span data-ttu-id="50f2b-128">Työt, jotka sisällytetään työkorttiin, sekä niiden arvioidut ajat saadaan reititys- ja työvaiheen asetustiedoista.</span><span class="sxs-lookup"><span data-stu-id="50f2b-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="50f2b-129">Voit avata työkortissa **Tuotantokirjauskansion rivit**, **työkortti** -sivun.</span><span class="sxs-lookup"><span data-stu-id="50f2b-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="50f2b-130">Operatiivisia resursseja hoitavat henkilöt voivat antaa palautetta tuotantoprosessista.</span><span class="sxs-lookup"><span data-stu-id="50f2b-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="50f2b-131">Esimerkiksi kulutustiedoille ja virhemäärille on omat kenttänsä.</span><span class="sxs-lookup"><span data-stu-id="50f2b-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="50f2b-132">Raaka-aineiden keräilyn varastotyö</span><span class="sxs-lookup"><span data-stu-id="50f2b-132">Warehouse work for raw material picking</span></span>
<span data-ttu-id="50f2b-133">Raaka-aineiden keräilytyö luodaan vapautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="50f2b-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="50f2b-134">Työ luodaan vain sille materiaalimäärälle, joka tuotantotilaukselle oli varattu fyysisesti ennen tilauksen vapauttamista.</span><span class="sxs-lookup"><span data-stu-id="50f2b-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="50f2b-135">Raaka-aineiden keräilyn varastotyö luodaan seuraavien asetusten avulla:</span><span class="sxs-lookup"><span data-stu-id="50f2b-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

-   <span data-ttu-id="50f2b-136">Raaka-aineiden keräilyn sijaintidirektiivi, joka määrittää, mistä varastosijainnista materiaalit keräillään</span><span class="sxs-lookup"><span data-stu-id="50f2b-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
-   <span data-ttu-id="50f2b-137">Raaka-aineiden aaltomalli, jossa on määritetty varastotyön suorittamisen käytännöt</span><span class="sxs-lookup"><span data-stu-id="50f2b-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
-   <span data-ttu-id="50f2b-138">Tuotannon varastosijainti, joka määrittää, minne materiaalit sijoitetaan.</span><span class="sxs-lookup"><span data-stu-id="50f2b-138">A production input location that determines where materials are put</span></span>




