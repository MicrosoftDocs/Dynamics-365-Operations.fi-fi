---
title: Ehdota käyttöomaisuuden hankintaa
description: Näiden ohjeiden avulla voit hankkia käyttöomaisuutta käyttöomaisuuden kirjauskansion hankintaehdotuksen avulla.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b35b13dc266fd5bccde437526400832d394b9aa
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839902"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="f9e1b-103">Ehdota käyttöomaisuuden hankintaa</span><span class="sxs-lookup"><span data-stu-id="f9e1b-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9e1b-104">Näiden ohjeiden avulla voit hankkia käyttöomaisuutta käyttöomaisuuden kirjauskansion hankintaehdotuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="f9e1b-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="f9e1b-106">Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="f9e1b-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-107">Select **New**.</span></span>
3. <span data-ttu-id="f9e1b-108">Anna tai valitse arvo **Nimi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="f9e1b-109">Valitse toimintoruudussa **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="f9e1b-110">Valitse **Ehdotukset**.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="f9e1b-111">Valitse **Hankintaehdotus**.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="f9e1b-112">Valitse **Suodata**.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-112">Select **Filter**.</span></span> <span data-ttu-id="f9e1b-113">Tyhjennä aiemmat arvot valitsemalla **Palauta**.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="f9e1b-114">Valitse **Käyttöomaisuuserän numero** -rivi.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="f9e1b-115">Anna tai valitse arvo **Ehdot**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="f9e1b-116">Määritä muut ehdot käyttöomaisuuserille, jotka haluat hakea tämän ehdotuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="f9e1b-117">Poistu ruudusta valitsemalla **OK** kahdesti.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="f9e1b-118">Tarkista luodut tapahtumarivit.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="f9e1b-119">Hankintaehdotukseen sisällytetään vain se käyttöomaisuuserä, jonka hankintapäivämäärä ja -hinta on määritetty kirjassa.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="f9e1b-120">Valitse sivulla **Kirjat**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="f9e1b-121">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-121">Select **Post**.</span></span>

