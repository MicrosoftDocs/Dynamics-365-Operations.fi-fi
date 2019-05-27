---
title: Tilikauden joukkosulkeminen
description: Tässä toimintaohjeessa kuvataan, miten kausi asetetaan pitoon tai pysyvästi suljetuksi useammalle yritykselle kerralla.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2988b7ab0837cc9a3e4f1c4eaf3fe6e219fa721
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564478"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="6d0b7-103">Tilikauden joukkosulkeminen</span><span class="sxs-lookup"><span data-stu-id="6d0b7-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d0b7-104">Tässä toimintaohjeessa kuvataan, miten kausi asetetaan pitoon tai pysyvästi suljetuksi useammalle yritykselle kerralla.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="6d0b7-105">Lisäksi tehtävässä näytetään, miten käyttäjäryhmän kirjaukset voi rajoittaa tiettyihin moduuleihin.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="6d0b7-106">Valitse Kirjanpito > Kausi suljettu > Kirjanpidon kalenterit.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="6d0b7-107">Huomaa, että luettelossa näytettävät yritykset riippuvat sivulla valitusta vuosikalenterista.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="6d0b7-108">Vain valittua vuosikalenteria käyttävät yritykset näytetään.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="6d0b7-109">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-109">Click Edit.</span></span>
3. <span data-ttu-id="6d0b7-110">Valitse kausi, jonka tilaa haluat muokata.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="6d0b7-111">Valitse yritykset, joiden tilan haluat päivittää.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="6d0b7-112">Voit valita kaikki yritykset nopeasti valitsemalla valintaruudun ruudukon vasemmalla puolella.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="6d0b7-113">Valitse Päivitä moduulien käyttöoikeudet määrittääksesi tietyn moduulin kirjausoikeudet.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="6d0b7-114">Moduulin tilan voi myös päivittää yksitellen muokkaamalla tietueita ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="6d0b7-115">Painike on hyödyllinen, kun haluat päivittää usean yrityksen tietueet nopeasti.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="6d0b7-116">Valitse Sovellusmoduulissa päivitettävä moduuli.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="6d0b7-117">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-117">Click Select.</span></span>
7. <span data-ttu-id="6d0b7-118">Valitse Käyttöoikeustaso-kohtaan Kaikki, Ei mitään tai tietty käyttäjäryhmä.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="6d0b7-119">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-119">Click Select.</span></span>
    * <span data-ttu-id="6d0b7-120">Kaikki ilmaisee, että kaikilla käyttäjillä, joilla on moduulin muokkausoikeudet, voivat tehdä kirjauksia avoimena kautena.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="6d0b7-121">Ei mitään ilmaisee, että käyttäjät eivät saa kirjata moduuliin avoimena kautena.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="6d0b7-122">Tietty käyttäjäryhmä ilmaisee, että vain ryhmän jäsenet voivat kirjata moduuliin avoimena kautena.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="6d0b7-123">Valitse Päivitä.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-123">Click Update.</span></span>
9. <span data-ttu-id="6d0b7-124">Päivitä tila valitsemalla toinen kausi.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="6d0b7-125">Valitse yritykset, joiden kauden tilan haluat päivittää.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="6d0b7-126">Valitse Päivitä kauden tila ja aseta tilaksi Pidossa tai Suljettu pysyvästi.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="6d0b7-127">Avoin ilmaisee, että jos käyttäjällä on käyttöoikeus, hän voi tehdä kirjauksia kauteen.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="6d0b7-128">Pidossa-tila tarkoittaa, että kaudelle ei voi tehdä kirjauksia, mutta se voidaan avata uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="6d0b7-129">Suljettu pysyvästi -tila tarkoittaa, että kausi on suljettu, eikä sitä voi avata uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="6d0b7-130">Oikaisuja ei voi kirjata.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="6d0b7-131">Kauden sulkemista pysyvästi ei suositella, ennen kuin kaikki oikaisut ja tarkistukset ovat valmiita.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="6d0b7-132">Valitse Päivitä.</span><span class="sxs-lookup"><span data-stu-id="6d0b7-132">Click Update.</span></span>

