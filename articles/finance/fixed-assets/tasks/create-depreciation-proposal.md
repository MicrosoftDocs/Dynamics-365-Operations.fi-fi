---
title: Luo poistoehdotus
description: Tässä ohjeaiheessa kuvataan, kuinka poiston eräehdotukset toimivat ja kuinka poisto ehdotetaan käyttöomaisuuserille.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 90c24e9d89c055ea95ca5f25cd85ef4042476a90
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187058"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="3e77d-103">Luo poistoehdotus</span><span class="sxs-lookup"><span data-stu-id="3e77d-103">Create a depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3e77d-104">Tässä ohjeaiheessa kuvataan, kuinka poiston eräehdotukset toimivat ja kuinka poisto ehdotetaan käyttöomaisuuserille.</span><span class="sxs-lookup"><span data-stu-id="3e77d-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="3e77d-105">Tässä tehtävässä käytetään USMF-esittely-yritystä ja kirjanpitäjän roolia.</span><span class="sxs-lookup"><span data-stu-id="3e77d-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="3e77d-106">Luo poistoehdotus</span><span class="sxs-lookup"><span data-stu-id="3e77d-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="3e77d-107">Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Kirjauskansioviennit > Luo poistoehdotus**.</span><span class="sxs-lookup"><span data-stu-id="3e77d-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="3e77d-108">Valitse **Kirjauskansion nimi**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="3e77d-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="3e77d-109">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3e77d-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="3e77d-110">Valitse **Tee yhteenveto poistoista** -valintaruutu kootaksesi kuukausittaiset poistot yhdelle kirjauskansioriville.</span><span class="sxs-lookup"><span data-stu-id="3e77d-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="3e77d-111">Jos esimerkiksi Päivämäärään-arvo on 31. maaliskuuta 2015, seuraava kuvaus muodostetaan: Poistot alkaen 31. tammikuuta 2015.</span><span class="sxs-lookup"><span data-stu-id="3e77d-111">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="3e77d-112">Ehdotettavien kirjauskansiorivien **Päivämäärä**-kenttään määritetään sitten 31. maaliskuuta 2015.</span><span class="sxs-lookup"><span data-stu-id="3e77d-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="3e77d-113">Poistoehdotus voidaan suodattaa käyttöomaisuuserän, käyttöomaisuusryhmän tai muun ehdon avulla käyttämällä **Suodatus**-vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="3e77d-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="3e77d-114">Kun käytössä on **Luo hankinta- tai poistoehdotus käyttöomaisuudelle** -lomake, voit ehdottaa erille poistoa.</span><span class="sxs-lookup"><span data-stu-id="3e77d-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="3e77d-115">Tätä suositellaan suuremmille ehdotuksille, jotka käyttävät enemmän järjestelmäresursseja.</span><span class="sxs-lookup"><span data-stu-id="3e77d-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="3e77d-116">Jos valitset erävaihtoehdon, voit edelleen suorittaa muita tehtäviä samaan aikaan.</span><span class="sxs-lookup"><span data-stu-id="3e77d-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="3e77d-117">Kun näin poiston ehdottaa, poisto lasketaan käyttöomaisuuden arvomalleille.</span><span class="sxs-lookup"><span data-stu-id="3e77d-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="3e77d-118">Valitse **Luo kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="3e77d-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="3e77d-119">Poistotapahtumien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="3e77d-119">Review depreciation entries</span></span>
1. <span data-ttu-id="3e77d-120">Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="3e77d-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="3e77d-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="3e77d-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3e77d-122">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="3e77d-122">Select **Lines**.</span></span>
4. <span data-ttu-id="3e77d-123">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="3e77d-123">Select **Post**.</span></span>
