---
title: Resurssit ja työtilaukset
description: Tässä ohjeaiheessa kerrotaan resursseista ja työtilauksista resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c2500a695fcffe0d60ac13b1b74cda4322b0e14
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206884"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="6a6c2-103">Resurssit ja työtilaukset</span><span class="sxs-lookup"><span data-stu-id="6a6c2-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6a6c2-104">Tässä ohjeaiheessa kerrotaan resursseista ja työtilauksista resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="6a6c2-105">Resurssit ja työtilaukset ovat resurssien hallinnan keskeisiä osia.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="6a6c2-106">*Resurssi* on kone tai koneen osa, joka vaatii jatkuvaa ylläpitoa ja huoltoa.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="6a6c2-107">Resursseja voidaan luoda hierarkkisessa rakenteessa, ja ne voivat liittyä toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="6a6c2-108">Ylläpitotöitä voidaan suunnitella kaikilla resurssirakenteen tasoilla.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="6a6c2-109">Eri tiedot, kuten tuotetiedot ja resurssien määritykset sekä vaaditut huoltosuunnitelmat määritetään kullekin resurssille.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="6a6c2-110">Seuraavassa kuvassa on yhteenveto resurssin tiedoista ja resurssien liitoksista työtyyppeihin.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="6a6c2-111">Punaista tekstiä käytetään esimerkeissä, jotka näyttävät periytymisen ja riippuvuudet.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![Kaavio, jossa resurssitiedot näkyvät suhteessa työtyyppeihin](media/05-overview-image.png)

<span data-ttu-id="6a6c2-113">Jokaisella työtilauksella on työtilaustyyppi, kuten ennakoiva kunnossapito, korjaava kunnossapito tai tarkastus.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="6a6c2-114">Työtilaus sisältää vähintään yhden työtilaustyön.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="6a6c2-115">Jokainen työtilauksen työ määrittää työn, joka on suoritettava resurssille ja siihen liittyvälle työtyypille.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="6a6c2-116">Esimerkkejä liittyvistä työtyypeistä ovat 10 000 km, 50 000 km ja 1 vuoden huolto sekä turvallisuustarkastus.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="6a6c2-117">Yksi työtilaus voi liittyä useisiin resursseihin.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="6a6c2-118">Seuraavassa kuvassa on yhteenveto työtilauksen tärkeimmistä tiedoista.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-118">The following illustration shows an overview of the key data in a work order.</span></span>

![Kaavio, jossa näkyvät työtilauksen olennaisimmat tiedot](media/06-overview-image.png)

<span data-ttu-id="6a6c2-120">Työtilaus voi liittyä toiseen työtilaukseen, ja työtyypit voivat sisältää työtilauksen muodostavat seuraavat työt.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="6a6c2-121">Työtilausten välillä ei yleensä ole riippuvuuksia.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="6a6c2-122">Tämän vuoksi ne voivat muuttaa työtilauksen elinkaaren tilaa ja ne voidaan ajoittaa toisistaan riippumatta.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="6a6c2-123">Työtilauksia voidaan luoda eri tavoilla, jotka liittyvät korjaaviin, ennaltaehkäiseviin tai reaktiivisiin ylläpitotöihin.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="6a6c2-124">Voit luoda työtilauksia myös manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-124">You can also create work orders manually.</span></span> <span data-ttu-id="6a6c2-125">Seuraavassa kuvassa on yleiskuvaus työtilausten automaattista tai manuaalista luomista koskevasta prosessista.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![Kaavio, jossa näkyy työtilausten automaattinen tai manuaalinen luonti](media/07-overview-image.png)

<span data-ttu-id="6a6c2-127">Useita vaiheita on suoritettava, kun haluat ajoittaa ja suorittaa ylläpitotyön työtilaukselle.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="6a6c2-128">Seuraavassa kuvassa on yhteenveto työtilauksen käsittelystä.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-128">The following illustration shows an overview of the processing for a work order.</span></span>

![Kaavio, jossa näkyy yleiskatsaus työtilauksen prosessointiin](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="6a6c2-130">Yleensä kun työskentelet Dynamics 365 Supply Chain Managementissa ja **Resurssien hallinta** -moduulissa, valitset **Uusi** luodaksesi uuden tietueen, valitset **Muokkaa** päivittääksesi aiemmin luodun tietueen ja valitset **Tallenna** tallentaaksesi uusia tai muokattuja tietoja.</span><span class="sxs-lookup"><span data-stu-id="6a6c2-130">In general, when you work in Dynamics 365 Supply Chain Management and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>
