---
title: Kulutusraporttien luominen
description: Tässä ohjeaiheessa kerrotaan, kuinka kulutusraportit luodaan resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d978f8b991211e477dd8f766fe67432d9d493d0
ms.sourcegitcommit: c0b581e4c647b6c47bc14d1d7bfe267832afecba
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/21/2019
ms.locfileid: "1913084"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="2f446-103">Kulutusraporttien luominen</span><span class="sxs-lookup"><span data-stu-id="2f446-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="2f446-104">Kun olet luonut ja kirjannut työtilausten kulutusrekisteröinnit käyttöomaisuuden hallinnassa, käytettävissä on kaksi raporttia kulutuksen yksityiskohtien näyttämistä varten.</span><span class="sxs-lookup"><span data-stu-id="2f446-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="2f446-105">Resurssien kulutusraportti</span><span class="sxs-lookup"><span data-stu-id="2f446-105">Asset consumption report</span></span>

<span data-ttu-id="2f446-106">Kun työtilausten kulutus on kirjattu, voit tulostaa käyttöomaisuuden kulutusraportin.</span><span class="sxs-lookup"><span data-stu-id="2f446-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="2f446-107">Raportissa näkyvät käyttöomaisuudelle kirjatut tunnit, tuntikustannukset, nimikekustannukset ja kulut.</span><span class="sxs-lookup"><span data-stu-id="2f446-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="2f446-108">Valitse **Resurssien hallinta** > **raportit** > **Resurssit** > **Resurssien kulutus**.</span><span class="sxs-lookup"><span data-stu-id="2f446-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="2f446-109">Valitse **Resurssien kulutus** -valintaikkunassa parametrit ja erittelytaso, jotka haluat nähdä, valitsemalla asianmukaisissa vaihtopainikkeissa "kyllä" ja lisäämällä toiminnallisen sijainnin taso **Näytä**-osaan.</span><span class="sxs-lookup"><span data-stu-id="2f446-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting "Yes" on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="2f446-110">**Tasot** -kentän avulla voit määrittää, miten yksityiskohtaisia resurssiriveistä haluat liittyen toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="2f446-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> <span data-ttu-id="2f446-111">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoinen toiminnallinen sijaintirakenne, kaikki toimintosijainnin resurssit näkyvät ylimmällä tasolla, joten rivi voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="2f446-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="2f446-112">Jos lisäät arvon "0" **Tasot**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki resurssit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="2f446-112">If you insert the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
    - <span data-ttu-id="2f446-113">Valitse "kyllä" **Kaikkien aliresurssien summa** -vaihtopainikkeessa, jos haluat nähdä kunkin alakäyttöomaisuuserän summat raportissa.</span><span class="sxs-lookup"><span data-stu-id="2f446-113">Select "Yes" on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="2f446-114">Valitse päivämääräväli **Päivämäärät** -osassa.</span><span class="sxs-lookup"><span data-stu-id="2f446-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="2f446-115">Valitse **Kohde-** pikavälilehdessä, jos haluat näyttää raportin näytössä, tulostaa sen tai tallentaa sen tiedostona tai sähköpostina.</span><span class="sxs-lookup"><span data-stu-id="2f446-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="2f446-116">Voit tarvittaessa valita tietyt raportissa näytettävät käyttöomaisuudet.</span><span class="sxs-lookup"><span data-stu-id="2f446-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="2f446-117">Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin**ja lisää käyttöomaisuudet, jotka haluat sisällyttää raporttiin.</span><span class="sxs-lookup"><span data-stu-id="2f446-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="2f446-118">Luo raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f446-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="2f446-119">Työtilauksen kulutusraportti</span><span class="sxs-lookup"><span data-stu-id="2f446-119">Work order consumption report</span></span>

<span data-ttu-id="2f446-120">Kun työtilausten kulutus on kirjattu, voit tulostaa työtilauksen kulutusraportin.</span><span class="sxs-lookup"><span data-stu-id="2f446-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="2f446-121">Raportissa näkyvät työtilauksille kirjatut tunnit, tuntikustannukset, nimikekustannukset ja kulut.</span><span class="sxs-lookup"><span data-stu-id="2f446-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="2f446-122">Valitse **Resurssien hallinta** > **Raportit** > **Työtilaukset** > **Työtilauksen kulutus**.</span><span class="sxs-lookup"><span data-stu-id="2f446-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="2f446-123">Valitse **Työtilauksen kulutus** -valintaikkunassa raporttiin sisällytettävät parametrit valitsemalla "kyllä" **Näytä**-osion asianmukaisissa vaihtopainikkeissa.</span><span class="sxs-lookup"><span data-stu-id="2f446-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting "Yes" on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="2f446-124">Valitse päivämääräväli **Päivämäärät** -osassa.</span><span class="sxs-lookup"><span data-stu-id="2f446-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="2f446-125">Valitse **Kohde-** pikavälilehdessä, jos haluat näyttää raportin näytössä, tulostaa sen tai tallentaa sen tiedostona tai sähköpostina.</span><span class="sxs-lookup"><span data-stu-id="2f446-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="2f446-126">Voit tarvittaessa valita tietyt raportissa näytettävät työtilaukset.</span><span class="sxs-lookup"><span data-stu-id="2f446-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="2f446-127">Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin**ja lisää työtilaukset, jotka haluat sisällyttää raporttiin.</span><span class="sxs-lookup"><span data-stu-id="2f446-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="2f446-128">Luo raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f446-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="2f446-129">Voit myös luoda [työtilausraportin](../work-orders/work-order-report.md), joka sisältää enemmän työtilaustietoja.</span><span class="sxs-lookup"><span data-stu-id="2f446-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>

