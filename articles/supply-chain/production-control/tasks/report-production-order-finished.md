---
title: Tuotantotilauksen ilmoittaminen valmiiksi
description: "Tässä menettelyssä näytetään, miten tuotantotilaus ilmoitetaan valmiiksi."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a8aceb273f940b0c01c4ca0f45bd8a16968f6f4f
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="3032f-103">Tuotantotilauksen ilmoittaminen valmiiksi</span><span class="sxs-lookup"><span data-stu-id="3032f-103">Report a production order as finished</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3032f-104">Tässä menettelyssä näytetään, miten tuotantotilaus ilmoitetaan valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="3032f-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="3032f-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="3032f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3032f-106">Tämä on kuudesta seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.</span><span class="sxs-lookup"><span data-stu-id="3032f-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="3032f-107">Tuotantotilauksen ilmoittaminen valmiiksi</span><span class="sxs-lookup"><span data-stu-id="3032f-107">Report a production order as finished</span></span>
1. <span data-ttu-id="3032f-108">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="3032f-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="3032f-109">Valitse tuotantotilaus, jonka tila on Aloitettu.</span><span class="sxs-lookup"><span data-stu-id="3032f-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="3032f-110">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="3032f-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="3032f-111">Valitse Ilmoita automaattisesti valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="3032f-111">Click Report as finished.</span></span>
    * <span data-ttu-id="3032f-112">Voit vahvistaa tällä sivulla valmiiksi ilmoitettavan lopullisen tuotteen määrän.</span><span class="sxs-lookup"><span data-stu-id="3032f-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="3032f-113">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="3032f-113">Click the General tab.</span></span>
5. <span data-ttu-id="3032f-114">Määritä Hyväksytty määrä -asetukseksi 18.</span><span class="sxs-lookup"><span data-stu-id="3032f-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="3032f-115">Määritä Virhemäärä-asetukseksi 2.</span><span class="sxs-lookup"><span data-stu-id="3032f-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="3032f-116">Valitse Virheen syy -kentässä Materiaali.</span><span class="sxs-lookup"><span data-stu-id="3032f-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="3032f-117">Valitse Lopeta työ -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="3032f-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="3032f-118">Valitse Hyväksy virhe -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="3032f-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="3032f-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3032f-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="3032f-120">Tarkista valmiiksi ilmoitettujen kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="3032f-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="3032f-121">Valitse toimintoruudussa Näytä.</span><span class="sxs-lookup"><span data-stu-id="3032f-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="3032f-122">Valitse Ilmoitettu valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="3032f-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="3032f-123">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3032f-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3032f-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3032f-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3032f-125">Valmiiksi ilmoitettujen kirjauskansio on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="3032f-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="3032f-126">Jos haluat tehdä oikaisuja kirjauskansioon, voit luoda manuaalisesti uuden kirjauskansion muutosten tekemistä varten.</span><span class="sxs-lookup"><span data-stu-id="3032f-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  

