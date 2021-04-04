---
title: Tuotantotilausten vapauttaminen
description: Vapautettu tuotantotilaus on tilaus, joka on hyväksytty tuotantoon. Termillä "Vapautettu" kuvataan tuotantotilauksen elinkaaren tilaa, jossa tuotantotilaus voidaan suorittaa tuotannossa ja varastoprosesseissa.
author: johanhoffmann
manager: tfehr
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ee20983209b9900037a46d56b6213d47bf852e4
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487696"
---
# <a name="release-production-orders"></a><span data-ttu-id="b2058-104">Tuotantotilausten vapauttaminen</span><span class="sxs-lookup"><span data-stu-id="b2058-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2058-105">Vapautettu tuotantotilaus on tilaus, joka on hyväksytty tuotantoon.</span><span class="sxs-lookup"><span data-stu-id="b2058-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="b2058-106">Termillä "Vapautettu" kuvataan tuotantotilauksen elinkaaren tilaa, jossa tuotantotilaus voidaan suorittaa tuotannossa ja varastoprosesseissa.</span><span class="sxs-lookup"><span data-stu-id="b2058-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span>

## <a name="characteristics-of-the-released-state"></a><span data-ttu-id="b2058-107">Vapautettu-tilan ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b2058-107">Characteristics of the Released state</span></span>

<span data-ttu-id="b2058-108">**Vapautettu**-tila on yksi tuotantotilauksen elinkaaren tiloista.</span><span class="sxs-lookup"><span data-stu-id="b2058-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="b2058-109">Tuotantotilaukset, joiden tilana on **Vapautettu**, voidaan suorittaa tuotannossa ja varastoprosesseissa.</span><span class="sxs-lookup"><span data-stu-id="b2058-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="b2058-110">**Vapautettu**-tilalla on seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="b2058-110">The **Released** state has the following characteristics:</span></span>

- <span data-ttu-id="b2058-111">Tuotantotila voidaan siirtää **Vapautettu**-tilaan tuotantotilauksesta tai eräprosessin avulla.</span><span class="sxs-lookup"><span data-stu-id="b2058-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="b2058-112">Tuotantotilaus voidaan myös päivittää automaattisesti suunnitelluista tuotantotilauksista, jotka on vahvistettu **Vahvistuksen aikaraja** -kentässä **Pääsuunnitelma**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b2058-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
- <span data-ttu-id="b2058-113">**Vapautettu**-tila osoittaa tuotannon käyttäjille (operaattoreille), että tuotantotyöt voidaan aloittaa.</span><span class="sxs-lookup"><span data-stu-id="b2058-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
- <span data-ttu-id="b2058-114">Tuotannon dokumentit, kuten reitityskortit ja -työt sekä työkortit sisältävät tuotantotöitä koskevia tietoja, ja niitä voidaan lähettää.</span><span class="sxs-lookup"><span data-stu-id="b2058-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
- <span data-ttu-id="b2058-115">Fyysisesti varatuille materiaaleille luodaan varastotyö, jolla materiaalit kerätään tuotantotilausta varten.</span><span class="sxs-lookup"><span data-stu-id="b2058-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="b2058-116">Töiden vapauttaminen tuotantoon</span><span class="sxs-lookup"><span data-stu-id="b2058-116">Releasing jobs to the shop floor</span></span>

<span data-ttu-id="b2058-117">Kun tuotantotilaus on vapautettu, siihen liittyvät tuotantotyöt ovat näkyvissä ja valmiina rekisteröitäviksi.</span><span class="sxs-lookup"><span data-stu-id="b2058-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="b2058-118">Operaattorit voivat tehdä työrekisteröintejä, kuten Käynnistä, Pysäytä ja Valmistuminen, joko **Työkorttipääte**- tai **Työkorttilaite**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b2058-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="b2058-119">Rekisteröity aika ja määrä siirretään automaattisesti rekisteröintisivuilta tuotantokirjauskansioihin, jotta käytettyä aikaa ja määrää voidaan seurata.</span><span class="sxs-lookup"><span data-stu-id="b2058-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="b2058-120">Reitityskortit</span><span class="sxs-lookup"><span data-stu-id="b2058-120">Route cards</span></span>

<span data-ttu-id="b2058-121">Reitityskortissa on yhteenveto reitityksen ja työvaiheen asetuksista sekä työvaiheen ja työn ajoitusmenetelmistä saatavista tiedoista.</span><span class="sxs-lookup"><span data-stu-id="b2058-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="b2058-122">Reititystyöt</span><span class="sxs-lookup"><span data-stu-id="b2058-122">Route jobs</span></span>

<span data-ttu-id="b2058-123">Reititystyö luetteloi työvaiheen kunkin työn tarkat tiedot sekä asetus-, käsittely-, jonotus- ja kuljetusajat.</span><span class="sxs-lookup"><span data-stu-id="b2058-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="b2058-124">Esimerkiksi maalaaminen on työvaihe, johon saatetaan tarvita yksittäisiä töitä, kuten asetusaika, maalausprosessin suoritusaika ja kuivumisen jonotusaika.</span><span class="sxs-lookup"><span data-stu-id="b2058-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="b2058-125">Työkortit</span><span class="sxs-lookup"><span data-stu-id="b2058-125">Job cards</span></span>

<span data-ttu-id="b2058-126">Työkortti luetteloi tietyn työvaiheen yksittäiset työnumerot.</span><span class="sxs-lookup"><span data-stu-id="b2058-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="b2058-127">Kullakin sivulla näkyy yksi työ.</span><span class="sxs-lookup"><span data-stu-id="b2058-127">One job appears on each page.</span></span> <span data-ttu-id="b2058-128">Työt, jotka sisällytetään työkorttiin, sekä niiden arvioidut ajat saadaan reititys- ja työvaiheen asetustiedoista.</span><span class="sxs-lookup"><span data-stu-id="b2058-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="b2058-129">Voit avata työkortissa **Tuotantokirjauskansion rivit**, **työkortti** -sivun.</span><span class="sxs-lookup"><span data-stu-id="b2058-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="b2058-130">Operatiivisia resursseja hoitavat henkilöt voivat antaa palautetta tuotantoprosessista.</span><span class="sxs-lookup"><span data-stu-id="b2058-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="b2058-131">Esimerkiksi kulutustiedoille ja virhemäärille on omat kenttänsä.</span><span class="sxs-lookup"><span data-stu-id="b2058-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="b2058-132">Raaka-aineiden keräilyn varastotyö</span><span class="sxs-lookup"><span data-stu-id="b2058-132">Warehouse work for raw material picking</span></span>

<span data-ttu-id="b2058-133">Raaka-aineiden keräilytyö luodaan vapautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b2058-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="b2058-134">Työ luodaan vain sille materiaalimäärälle, joka tuotantotilaukselle oli varattu fyysisesti ennen tilauksen vapauttamista.</span><span class="sxs-lookup"><span data-stu-id="b2058-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="b2058-135">Raaka-aineiden keräilyn varastotyö luodaan seuraavien asetusten avulla:</span><span class="sxs-lookup"><span data-stu-id="b2058-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

- <span data-ttu-id="b2058-136">Raaka-aineiden keräilyn sijaintidirektiivi, joka määrittää, mistä varastosijainnista materiaalit keräillään</span><span class="sxs-lookup"><span data-stu-id="b2058-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
- <span data-ttu-id="b2058-137">Raaka-aineiden aaltomalli, jossa on määritetty varastotyön suorittamisen käytännöt</span><span class="sxs-lookup"><span data-stu-id="b2058-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
- <span data-ttu-id="b2058-138">Tuotannon varastosijainti, joka määrittää, minne materiaalit sijoitetaan.</span><span class="sxs-lookup"><span data-stu-id="b2058-138">A production input location that determines where materials are put</span></span>

<span data-ttu-id="b2058-139">Rekisterikilvillä hallittuja sijainteja käytettäessä voit valita, poimitaanko nimikkeen tilattu määrä vai täysi käytettävissä oleva määrä, kun käsitellään raaka-aineiden poimintatöitä.</span><span class="sxs-lookup"><span data-stu-id="b2058-139">When using license plate controlled locations, you can choose whether the ordered quantity or the full quantity available for the item should be picked while processing the raw material picking work.</span></span> <span data-ttu-id="b2058-140">tämä asetus määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="b2058-140">To set this option:</span></span>

1. <span data-ttu-id="b2058-141">Valitse **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet** ja avaa asianomainen nimike.</span><span class="sxs-lookup"><span data-stu-id="b2058-141">Go to **Product information management \> Products \> Released products** and open the relevant item.</span></span>
1. <span data-ttu-id="b2058-142">Laajenna **Varasto**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="b2058-142">Expand the **Warehouse** FastTab.</span></span>
1. <span data-ttu-id="b2058-143">Valitse **Materiaalin poiminta rekisterikilpisijainneissa**-kentälle jokin seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="b2058-143">Select one of the following options for the  **Material picking in license plate locations** field:</span></span>
    - <span data-ttu-id="b2058-144">*Tilauksen keräily*: Vain tilattu määrä kerärään.</span><span class="sxs-lookup"><span data-stu-id="b2058-144">*Order picking*: Only the ordered quantity should be picked.</span></span>
    - <span data-ttu-id="b2058-145">*Valmistelu*: Mahdollisuuksien mukaan poimitaan täysi rekisterikilvellä saatavilla oleva määrä.</span><span class="sxs-lookup"><span data-stu-id="b2058-145">*Staging*: Whenever possible, the full quantity available at the license plate should be picked.</span></span> <span data-ttu-id="b2058-146">Jotta työntekijä voi poimia rekisterikilven täyden määrän, rekisterikilpi ei saa sisältää sekaisin olevia nimikkeitä eikä erilaisia dimensioita.</span><span class="sxs-lookup"><span data-stu-id="b2058-146">For a worker to be able to pick the full license plate quantity, the license plate must not contain mixed items and must not have mixed dimensions.</span></span> <span data-ttu-id="b2058-147">Jos rekisterikilpi sisältää erilaisia dimensioita tai nimikkeitä, poiminta käsitellään samalla tavalla kuin, jos kyseessä olisi *Tilauksen keräily*.</span><span class="sxs-lookup"><span data-stu-id="b2058-147">If the license plate contains mixed dimensions or items, the pick will proceed as if it were set to *Order picking*.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]