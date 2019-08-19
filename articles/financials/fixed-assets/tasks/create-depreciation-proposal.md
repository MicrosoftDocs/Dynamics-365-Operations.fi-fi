---
title: Luo poistoehdotus
description: Tässä menettelyssä kuvataan, kuinka poiston eräehdotukset toimivat ja kuinka poisto ehdotetaan käyttöomaisuuserille.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07146adfe1ead2b6e06e3c323963f8c012381b76
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839998"
---
# <a name="create-depreciation-proposal"></a><span data-ttu-id="496dc-103">Luo poistoehdotus</span><span class="sxs-lookup"><span data-stu-id="496dc-103">Create depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="496dc-104">Tässä menettelyssä kuvataan, kuinka poiston eräehdotukset toimivat ja kuinka poisto ehdotetaan käyttöomaisuuserille.</span><span class="sxs-lookup"><span data-stu-id="496dc-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="496dc-105">Tässä tehtävässä käytetään USMF-esittely-yritystä ja kirjanpitäjän roolia.</span><span class="sxs-lookup"><span data-stu-id="496dc-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="496dc-106">Luo poistoehdotus</span><span class="sxs-lookup"><span data-stu-id="496dc-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="496dc-107">Siirry kohtaan Käyttöomaisuus > Kirjauskansioviennit > Luo poistoehdotus.</span><span class="sxs-lookup"><span data-stu-id="496dc-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="496dc-108">Avaa haku valitsemalla Kirjauskansion nimi -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="496dc-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="496dc-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="496dc-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="496dc-110">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="496dc-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="496dc-111">Valitse Tee yhteenveto poistoista -valintaruutu kootaksesi kuukausittaiset poistot yhdelle kirjauskansioriville.</span><span class="sxs-lookup"><span data-stu-id="496dc-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="496dc-112">Jos esimerkiksi Päivämäärään-arvo on 31. maaliskuuta 2015, seuraava kuvaus muodostetaan: Poistot alkaen 31. tammikuuta 2015.</span><span class="sxs-lookup"><span data-stu-id="496dc-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="496dc-113">Ehdotettavien kirjauskansiorivien Päivämäärä-kenttään määritetään sitten 31. maaliskuuta 2015.</span><span class="sxs-lookup"><span data-stu-id="496dc-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="496dc-114">Poistoehdotus voidaan suodattaa käyttöomaisuuserän, käyttöomaisuusryhmän tai muun ehdon avulla käyttämällä Suodatus-vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="496dc-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="496dc-115">Kun käytössä on Luo hankinta- tai poistoehdotus käyttöomaisuudelle -lomake, voit ehdottaa erille poistoa.</span><span class="sxs-lookup"><span data-stu-id="496dc-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="496dc-116">Tätä suositellaan suuremmille ehdotuksille, jotka käyttävät enemmän järjestelmäresursseja.</span><span class="sxs-lookup"><span data-stu-id="496dc-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="496dc-117">Jos valitset erävaihtoehdon, voit edelleen suorittaa muita tehtäviä samaan aikaan.</span><span class="sxs-lookup"><span data-stu-id="496dc-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="496dc-118">Kun näin poiston ehdottaa, poisto lasketaan käyttöomaisuuden arvomalleille.</span><span class="sxs-lookup"><span data-stu-id="496dc-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="496dc-119">Valitse Luo kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="496dc-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="496dc-120">Poistotapahtumien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="496dc-120">Review depreciation entries</span></span>
1. <span data-ttu-id="496dc-121">Valitse Käyttöomaisuus > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="496dc-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="496dc-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="496dc-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="496dc-123">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="496dc-123">Click Lines.</span></span>
4. <span data-ttu-id="496dc-124">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="496dc-124">Click Post.</span></span>

