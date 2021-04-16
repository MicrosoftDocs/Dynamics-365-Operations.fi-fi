---
title: Ehdota käyttöomaisuuden hankintaa
description: Näiden ohjeiden avulla voit hankkia käyttöomaisuutta käyttöomaisuuden kirjauskansion hankintaehdotuksen avulla.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817160"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="b188e-103">Ehdota käyttöomaisuuden hankintaa</span><span class="sxs-lookup"><span data-stu-id="b188e-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b188e-104">Näiden ohjeiden avulla voit hankkia käyttöomaisuutta käyttöomaisuuden kirjauskansion hankintaehdotuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="b188e-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="b188e-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="b188e-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="b188e-106">Jos aiot hankkia käyttöomaisuuden käyttöomaisuuden ehdotuskirjauskansion avulla, ensin on luotava käyttöomaisuustietue ja sitten määritettävä hankintahinta käyttöomaisuuskirjassa.</span><span class="sxs-lookup"><span data-stu-id="b188e-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="b188e-107">Käyttöomaisuuden hankintaehdotuksen luominen</span><span class="sxs-lookup"><span data-stu-id="b188e-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="b188e-108">Luo käyttöomaisuuden hankintaehdotus seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b188e-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="b188e-109">Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="b188e-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="b188e-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b188e-110">Select **New**.</span></span>
3. <span data-ttu-id="b188e-111">Anna tai valitse arvo **Nimi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b188e-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="b188e-112">Valitse toimintoruudussa **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="b188e-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="b188e-113">Valitse **Ehdotukset**.</span><span class="sxs-lookup"><span data-stu-id="b188e-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="b188e-114">Valitse **Hankintaehdotus**.</span><span class="sxs-lookup"><span data-stu-id="b188e-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="b188e-115">Valitse **Suodata**.</span><span class="sxs-lookup"><span data-stu-id="b188e-115">Select **Filter**.</span></span> <span data-ttu-id="b188e-116">Tyhjennä aiemmat arvot valitsemalla **Palauta**.</span><span class="sxs-lookup"><span data-stu-id="b188e-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="b188e-117">Valitse **Käyttöomaisuuserän numero** -rivi.</span><span class="sxs-lookup"><span data-stu-id="b188e-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="b188e-118">Anna tai valitse arvo **Ehdot**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b188e-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="b188e-119">Määritä muut ehdot käyttöomaisuuserille, jotka haluat hakea tämän ehdotuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="b188e-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="b188e-120">Poistu ruudusta valitsemalla **OK** kahdesti.</span><span class="sxs-lookup"><span data-stu-id="b188e-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="b188e-121">Tarkista, että tapahtumarivit on luotu.</span><span class="sxs-lookup"><span data-stu-id="b188e-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="b188e-122">Hankintaehdotukseen sisällytetään vain se käyttöomaisuuserä, jonka hankintapäivämäärä ja -hinta on määritetty kirjassa.</span><span class="sxs-lookup"><span data-stu-id="b188e-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="b188e-123">Valitse sivulla **Kirjat**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="b188e-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="b188e-124">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="b188e-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="b188e-125">Sisällytä taloushallinnon oletusdimensiot hankintaehdotukseen</span><span class="sxs-lookup"><span data-stu-id="b188e-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="b188e-126">Hankintatapahtuma voidaan luoda Excel-apuohjelman avulla valitsemalla **Käyttöomaisuus > Kirjauskansioviennit > Käyttöomaisuuserän kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="b188e-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="b188e-127">Luo uusi kirjauskansio, siirry sivun **Rivit**-osaan, valitse Excel-kuvake ja valitse sitten käyttöomaisuuspäiväkirjan rivi.</span><span class="sxs-lookup"><span data-stu-id="b188e-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="b188e-128">Järjestelmä luo ja avaa kirjauskansiorivejä edustavan Excel-mallin.</span><span class="sxs-lookup"><span data-stu-id="b188e-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="b188e-129">Voit lisätä malliin päiväkirjarivien lisättävät tiedot ja julkaista tiedot sitten takaisin järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="b188e-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="b188e-130">Jos valitulle käyttöomaisuuskirjalle ja vastaaville Excel-malliin syötetyille käyttöomaisuuserille on määritetty oletusdimensiot, taloushallinnon oletusdimensioita kutsutaan käyttöomaisuuskirjan päätiedoista, kun kirjauskansio julkaistaan Excelistä järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="b188e-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="b188e-131">Jos haluat sisällyttää taloushallinnon dimensiot käyttöomaisuuskirjaan automaattisesti, kun julkaiset käyttöomaisuuskirjauskansion Excel-apuohjelmasta, oletusdimensiot on määritettävä etukäteen.</span><span class="sxs-lookup"><span data-stu-id="b188e-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
