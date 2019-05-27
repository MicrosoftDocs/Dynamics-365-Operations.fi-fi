---
title: Ehdota käyttöomaisuuden hankintaa
description: Näiden ohjeiden avulla voit hankkia käyttöomaisuutta käyttöomaisuuden kirjauskansion hankintaehdotuksen avulla.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1891206bb266b126eccfa789b8c8062c9bfa688b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570877"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="7d09f-103">Ehdota käyttöomaisuuden hankintaa</span><span class="sxs-lookup"><span data-stu-id="7d09f-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d09f-104">Näiden ohjeiden avulla voit hankkia käyttöomaisuutta käyttöomaisuuden kirjauskansion hankintaehdotuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="7d09f-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="7d09f-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="7d09f-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="7d09f-106">Valitse Käyttöomaisuus > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="7d09f-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="7d09f-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7d09f-107">Click New.</span></span>
3. <span data-ttu-id="7d09f-108">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d09f-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="7d09f-109">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="7d09f-109">Click Lines.</span></span>
5. <span data-ttu-id="7d09f-110">Valitse Ehdotukset.</span><span class="sxs-lookup"><span data-stu-id="7d09f-110">Click Proposals.</span></span>
6. <span data-ttu-id="7d09f-111">Valitse Hankintaehdotus.</span><span class="sxs-lookup"><span data-stu-id="7d09f-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="7d09f-112">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="7d09f-112">Click Filter.</span></span>
8. <span data-ttu-id="7d09f-113">Tyhjennä aiemmat arvot valitsemalla Palauta.</span><span class="sxs-lookup"><span data-stu-id="7d09f-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="7d09f-114">Valitse käyttöomaisuuserän numeron rivi.</span><span class="sxs-lookup"><span data-stu-id="7d09f-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="7d09f-115">Syötä tai valitse arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d09f-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="7d09f-116">Määritä muut ehdot käyttöomaisuuserille, jotka haluat hakea tämän ehdotuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="7d09f-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="7d09f-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7d09f-117">Click OK.</span></span>
12. <span data-ttu-id="7d09f-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7d09f-118">Click OK.</span></span>
    * <span data-ttu-id="7d09f-119">Tarkista luodut tapahtumarivit.</span><span class="sxs-lookup"><span data-stu-id="7d09f-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="7d09f-120">Hankintaehdotukseen sisällytetään vain se käyttöomaisuuserä, jonka hankintapäivämäärä ja -hinta on määritetty kirjassa.</span><span class="sxs-lookup"><span data-stu-id="7d09f-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="7d09f-121">Valitse Kirjat-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7d09f-121">Click the Books tab.</span></span>
14. <span data-ttu-id="7d09f-122">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="7d09f-122">Click Post.</span></span>

