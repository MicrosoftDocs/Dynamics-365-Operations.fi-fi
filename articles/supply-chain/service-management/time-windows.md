---
title: Aikaikkunat
description: Voit optimoida huoltotilausrivien ajoittamisen aikaikkunoiden avulla.
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a537c2491f2540e48b6ccdccaee11b4fa8b208d9
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="time-windows"></a><span data-ttu-id="ee34c-103">Aikaikkunat</span><span class="sxs-lookup"><span data-stu-id="ee34c-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee34c-104">Voit optimoida huoltotilausrivien ajoittamisen aikaikkunoiden avulla.</span><span class="sxs-lookup"><span data-stu-id="ee34c-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="ee34c-105">Voit määrittää järjestelmän siten, että huoltotilaukset luodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="ee34c-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="ee34c-106">Voit liittää aikaikkunan määrittämien ehtojen perusteella mahdollisimman monta huoltotilausriviä mahdollisimman harvoihin huoltotilauksiin.</span><span class="sxs-lookup"><span data-stu-id="ee34c-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="ee34c-107">Aikaikkunat määrittävät, miten pitkälle huoltotilausrivi voidaan siirtää lasketusta päivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="ee34c-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="ee34c-108">Laskettu päivämäärä on päivämäärä, jolloin huoltotilausrivi on ajoitettu tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="ee34c-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="ee34c-109">Päivämäärä perustuu sen väliasetukseen ja huoltojaksoon, jonka määritit **Luo huoltotilaukset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="ee34c-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="ee34c-110">Aikaikkuna määritetään käyttämällä seuraavan taulun arvoja.</span><span class="sxs-lookup"><span data-stu-id="ee34c-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="ee34c-111">Tapa</span><span class="sxs-lookup"><span data-stu-id="ee34c-111">Method</span></span> | <span data-ttu-id="ee34c-112">kuvaus</span><span class="sxs-lookup"><span data-stu-id="ee34c-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee34c-113">Viikko</span><span class="sxs-lookup"><span data-stu-id="ee34c-113">Week</span></span>   | <span data-ttu-id="ee34c-114">Päivämäärä, jona huoltotilausrivi voidaan siirtää mille tahansa avoimelle päivälle, joka on samalla viikolla kuin alkuperäinen laskettu päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="ee34c-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="ee34c-115">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="ee34c-115">Month</span></span>  | <span data-ttu-id="ee34c-116">Päivämäärä, jona huoltotilausrivi voidaan siirtää mille tahansa avoimelle päivälle, joka on samana kuukautena kuin alkuperäinen laskettu päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="ee34c-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="ee34c-117">Huoltotilausrivin laskettu päivämäärä on esimerkiksi 15.3.2017.</span><span class="sxs-lookup"><span data-stu-id="ee34c-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="ee34c-118">Huoltotilausrivi voidaan ajoittaa mille tahansa viikonpäivälle 1.–28.2.2017.</span><span class="sxs-lookup"><span data-stu-id="ee34c-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="ee34c-119">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="ee34c-119">Manual</span></span> | <span data-ttu-id="ee34c-120">Voit määrittää huoltotilausrivin siirron päivien enimmäismäärän ennen alkuperäistä laskettua päivämäärää tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="ee34c-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="ee34c-121">Jos huoltosopimuksen riville ei ole määritetty aikaikkunaa, huoltosopimuksesta johdettu huoltotilausrivi on suoritettava täsmälleen sinä päivänä, jolle se on alun perin ajoitettu.</span><span class="sxs-lookup"><span data-stu-id="ee34c-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee34c-122">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="ee34c-122">Related topics</span></span>

[<span data-ttu-id="ee34c-123">Aikaikkunoiden luominen</span><span class="sxs-lookup"><span data-stu-id="ee34c-123">Create time windows</span></span>](create-time-windows.md)


