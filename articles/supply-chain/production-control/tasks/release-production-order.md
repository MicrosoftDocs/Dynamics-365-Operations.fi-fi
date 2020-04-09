---
title: Tuotantotilauksen vapauttaminen
description: Tässä menettelyssä näytetään, miten tuotantotilaus vapautetaan.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e98adea620d74bdb7a90cedc9b256d9883b27525
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148953"
---
# <a name="release-a-production-order"></a><span data-ttu-id="ff586-103">Tuotantotilauksen vapauttaminen</span><span class="sxs-lookup"><span data-stu-id="ff586-103">Release a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff586-104">Tässä menettelyssä näytetään, miten tuotantotilaus vapautetaan.</span><span class="sxs-lookup"><span data-stu-id="ff586-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="ff586-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="ff586-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ff586-106">Tämä on neljäs seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.</span><span class="sxs-lookup"><span data-stu-id="ff586-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="ff586-107">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="ff586-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="ff586-108">Valitse ruudukossa tuotantotilaus, jonka tila on Ajoitettu.</span><span class="sxs-lookup"><span data-stu-id="ff586-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="ff586-109">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="ff586-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="ff586-110">Valitse Vapauta.</span><span class="sxs-lookup"><span data-stu-id="ff586-110">Click Release.</span></span>
    * <span data-ttu-id="ff586-111">Voit vahvistaa tällä sivulla valittujen tuotantotilausten vapautuksen.</span><span class="sxs-lookup"><span data-stu-id="ff586-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="ff586-112">Lisää tilauksia valitsemalla Valitse.</span><span class="sxs-lookup"><span data-stu-id="ff586-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="ff586-113">Vapautusvaihe osoittaa, milloin tuotantotilaus vapautetaan tuotannon työnohjaukseen. Tällöin työnohjauksen käyttäjät voivat raportoida tuotannon töiden etenemisestä.</span><span class="sxs-lookup"><span data-stu-id="ff586-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="ff586-114">Töiden käsittelyä koskevaa tärkeää tietoa sisältävät tuotannon dokumentit voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="ff586-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="ff586-115">Raaka-aineiden keräilyä koskeva varastotyö luodaan nimikkeille, jotka on määritetty varastoprosessia varten.</span><span class="sxs-lookup"><span data-stu-id="ff586-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="ff586-116">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="ff586-116">Click the General tab.</span></span>
    * <span data-ttu-id="ff586-117">Määritä, mitkä tuotantoraportit tulostetaan.</span><span class="sxs-lookup"><span data-stu-id="ff586-117">Select which production reports should be printed.</span></span> <span data-ttu-id="ff586-118">Työkortti-raportti tulostaa sivun jokaisesta ajoitetusta työstä. Se vaatii tuotantotilauksen ajoituksen työtasolla.</span><span class="sxs-lookup"><span data-stu-id="ff586-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="ff586-119">Raportti sisältää tietoja ajoituksen aloitus- ja päättymisajasta, tuotettavasta määrästä ja työn suorittavasta resurssista.</span><span class="sxs-lookup"><span data-stu-id="ff586-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="ff586-120">Reititystyöt-raportti kerää samat tiedot samalla sivulla, mutta ei tulosta sivua kunkin työn kohdalla.</span><span class="sxs-lookup"><span data-stu-id="ff586-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="ff586-121">Reitityskortti-raportti näyttää ainoastaan toiminnot, ei töitä.</span><span class="sxs-lookup"><span data-stu-id="ff586-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="ff586-122">Tämän vuoksi töiden ajoittaminen ei ole pakollista tässä raportissa, mutta sitä voidaan käyttää, kun tuotantotilaukset on ajoitettu työvaiheen tasolla.</span><span class="sxs-lookup"><span data-stu-id="ff586-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="ff586-123">Valitse Tulosta reitityskortti -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="ff586-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="ff586-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ff586-124">Click OK.</span></span>
7. <span data-ttu-id="ff586-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ff586-125">Close the page.</span></span>

