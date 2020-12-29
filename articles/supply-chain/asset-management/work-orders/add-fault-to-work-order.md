---
title: Vian lisääminen työtilaukseen
description: Tässä aiheessa kuvataan, miten vikamerkinnät lisätään työtilauksiin käyttöomaisuuden hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e82026f1d73e7368d93109bc0b895b7368ac84d4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427102"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="cd564-103">Vian lisääminen työtilaukseen</span><span class="sxs-lookup"><span data-stu-id="cd564-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="cd564-104">Voit lisätä vikasuunnittelijassa määritettyjä vikamäärityksiä työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="cd564-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="cd564-105">Vähintään yhden vikatietueen on liityttävä työtilauksessa valitussa resurssissa käytettyihin resurssityyppeihin.</span><span class="sxs-lookup"><span data-stu-id="cd564-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="cd564-106">Lisätietoja määrityksestä esitetään kohdassa [Vikojen hallinta](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="cd564-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="cd564-107">Valitse **Resurssienhallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="cd564-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="cd564-108">Valitse työtilaus, jolle vikarekisteröinti tehdään ja valitse sitten **Resurssin vika** **Resurssi**-ryhmän **Työtilaus**-välilehden toimintoruudussa.</span><span class="sxs-lookup"><span data-stu-id="cd564-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="cd564-109">Valitse **Oireet**-pikavälilehdessä **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="cd564-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="cd564-110">**Vika**-kenttään syötetään automaattisesti vian järjestysnumero.</span><span class="sxs-lookup"><span data-stu-id="cd564-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="cd564-111">Valitse asiaankuuluva oire **Vian oire** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="cd564-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="cd564-112">Valitse asianmukaiset arvot kentissä **Vika-alue** ja **Vikatyyppi**.</span><span class="sxs-lookup"><span data-stu-id="cd564-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="cd564-113">**Vian päivämäärä** -kenttään valitaan automaattisesti nykyinen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="cd564-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="cd564-114">Voit valita tarpeen mukaan eri päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="cd564-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="cd564-115">Lisää **Valitun oireen syyt** -pikavälilehdessä rivi kuvaamaan ongelman syytä.</span><span class="sxs-lookup"><span data-stu-id="cd564-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="cd564-116">Lisää **Valitun oireen korjaukset** -pikavälilehdessä rivi kuvaamaan mahdollista ratkaisua ongelmaan.</span><span class="sxs-lookup"><span data-stu-id="cd564-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="cd564-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="cd564-117">Select **Save**.</span></span>

<span data-ttu-id="cd564-118">Alla olevassa kuvassa näkyy esimerkki vikarekisteröinnistä.</span><span class="sxs-lookup"><span data-stu-id="cd564-118">The illustration below shows an example of a fault registration.</span></span>

![Kuva 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="cd564-120">Näytä resurssin viat</span><span class="sxs-lookup"><span data-stu-id="cd564-120">View asset faults</span></span>

<span data-ttu-id="cd564-121">**Resurssin viat** -luettelossa voit saada yleiskuvan kaikista omaisuuteen rekisteröidyistä virheistä.</span><span class="sxs-lookup"><span data-stu-id="cd564-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="cd564-122">**Resurssin viat** -luettelosivulla voit saada yleiskuvan kaikista resursseihin rekisteröidyistä virheistä.</span><span class="sxs-lookup"><span data-stu-id="cd564-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="cd564-123">Avaa sivu valitsemalla **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssin viat**.</span><span class="sxs-lookup"><span data-stu-id="cd564-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="cd564-124">Tulosta resurssin vikaraportti</span><span class="sxs-lookup"><span data-stu-id="cd564-124">Print asset fault report</span></span>

<span data-ttu-id="cd564-125">**Kaikki resurssit** luettelosivulla voit tulostaa omaisuusvikaraportin, jossa näkyvät kaikki vikarekisteröinnit sekä graafisen yhteenveto vikatilastoista.</span><span class="sxs-lookup"><span data-stu-id="cd564-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="cd564-126">Valitse **Resurssienhallinta** > **Yhteiset** > **Resurssit** > **Kaikki resurssit**.</span><span class="sxs-lookup"><span data-stu-id="cd564-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="cd564-127">Valitse resurssi, jolle tulostetaan vikaraportti.</span><span class="sxs-lookup"><span data-stu-id="cd564-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="cd564-128">Valitse toimintoruudun **Yleinen**-välilehden **Raportit**-ryhmässä **Resurssin vika**.</span><span class="sxs-lookup"><span data-stu-id="cd564-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="cd564-129">Syötä tietty kausi tai valitse vikatyyppi.</span><span class="sxs-lookup"><span data-stu-id="cd564-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="cd564-130">Tulosta raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd564-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="cd564-131">Voit tulostaa useiden resurssien tai resurssityyppien vikaraportin valitsemalla **Resurssien hallinta** > **Raportit** > **Resurssit** > **Resurssin vika**.</span><span class="sxs-lookup"><span data-stu-id="cd564-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

