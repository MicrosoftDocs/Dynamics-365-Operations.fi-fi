--- 
title: Luo poistoehdotus
description: "Tässä menettelyssä kuvataan, kuinka poiston eräehdotukset toimivat ja kuinka poisto ehdotetaan käyttöomaisuuserille."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1e563d11e2877597787a7d73fb220906f683f365
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="769a6-103">Luo poistoehdotus</span><span class="sxs-lookup"><span data-stu-id="769a6-103">Create a depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="769a6-104">Tässä menettelyssä kuvataan, kuinka poiston eräehdotukset toimivat ja kuinka poisto ehdotetaan käyttöomaisuuserille.</span><span class="sxs-lookup"><span data-stu-id="769a6-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="769a6-105">Tässä tehtävässä käytetään USMF-esittely-yritystä ja kirjanpitäjän roolia.</span><span class="sxs-lookup"><span data-stu-id="769a6-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="769a6-106">Luo poistoehdotus</span><span class="sxs-lookup"><span data-stu-id="769a6-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="769a6-107">Siirry kohtaan Käyttöomaisuus > Kirjauskansioviennit > Luo poistoehdotus.</span><span class="sxs-lookup"><span data-stu-id="769a6-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="769a6-108">Avaa haku valitsemalla Kirjauskansion nimi -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="769a6-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="769a6-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="769a6-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="769a6-110">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="769a6-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="769a6-111">Valitse Tee yhteenveto poistoista -valintaruutu kootaksesi kuukausittaiset poistot yhdelle kirjauskansioriville.</span><span class="sxs-lookup"><span data-stu-id="769a6-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="769a6-112">Jos esimerkiksi Päivämäärään-arvo on 31. maaliskuuta 2015, seuraava kuvaus muodostetaan: Poistot alkaen 31. tammikuuta 2015.</span><span class="sxs-lookup"><span data-stu-id="769a6-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="769a6-113">Ehdotettavien kirjauskansiorivien Päivämäärä-kenttään määritetään sitten 31. maaliskuuta 2015.</span><span class="sxs-lookup"><span data-stu-id="769a6-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="769a6-114">Poistoehdotus voidaan suodattaa käyttöomaisuuserän, käyttöomaisuusryhmän tai muun ehdon avulla käyttämällä Suodatus-vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="769a6-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="769a6-115">Kun käytössä on Luo hankinta- tai poistoehdotus käyttöomaisuudelle -lomake, voit ehdottaa erille poistoa.</span><span class="sxs-lookup"><span data-stu-id="769a6-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="769a6-116">Tätä suositellaan suuremmille ehdotuksille, jotka käyttävät enemmän järjestelmäresursseja.</span><span class="sxs-lookup"><span data-stu-id="769a6-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="769a6-117">Jos valitset erävaihtoehdon, voit edelleen suorittaa muita tehtäviä samaan aikaan.</span><span class="sxs-lookup"><span data-stu-id="769a6-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="769a6-118">Kun näin poiston ehdottaa, poisto lasketaan käyttöomaisuuden arvomalleille.</span><span class="sxs-lookup"><span data-stu-id="769a6-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="769a6-119">Valitse Luo kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="769a6-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="769a6-120">Poistotapahtumien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="769a6-120">Review depreciation entries</span></span>
1. <span data-ttu-id="769a6-121">Valitse Käyttöomaisuus > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="769a6-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="769a6-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="769a6-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="769a6-123">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="769a6-123">Click Lines.</span></span>
4. <span data-ttu-id="769a6-124">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="769a6-124">Click Post.</span></span>


