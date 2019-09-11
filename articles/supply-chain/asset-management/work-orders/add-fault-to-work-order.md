---
title: Vian lisääminen työtilaukseen
description: Tässä aiheessa kuvataan, miten vikamerkinnät lisätään työtilauksiin käyttöomaisuuden hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875635"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="54e1e-103">Vian lisääminen työtilaukseen</span><span class="sxs-lookup"><span data-stu-id="54e1e-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="54e1e-104">Voit lisätä vikasuunnittelijassa vikamäärityksiä työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="54e1e-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="54e1e-105">Työtilauksessa valitulla käyttöomaisuuserällä on oltava käyttöomaisuustyypit, joihin on liitetty yksi tai useita vikatietueita.</span><span class="sxs-lookup"><span data-stu-id="54e1e-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="54e1e-106">Lisätietoja määrityksestä on kohdassa [Vikojen hallinta](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="54e1e-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="54e1e-107">Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="54e1e-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="54e1e-108">Valitse luettelosta työtilaus, johon haluat tehdä vikamerkinnän, ja valitse **Resurssin vika**.</span><span class="sxs-lookup"><span data-stu-id="54e1e-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="54e1e-109">Valitse **Oireet** -pikavälilehdessä **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="54e1e-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="54e1e-110">**Vika**-kenttään syötetään automaattisesti vian järjestysnumero.</span><span class="sxs-lookup"><span data-stu-id="54e1e-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="54e1e-111">Valitse asiaankuuluva oire **vian oire** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="54e1e-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="54e1e-112">Valitse **Vika-alue** ja **Vikatyyppi**.</span><span class="sxs-lookup"><span data-stu-id="54e1e-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="54e1e-113">**Vian päivämäärä** -kenttään valitaan automaattisesti nykyinen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="54e1e-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="54e1e-114">Voit muuttaa päivämäärää tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="54e1e-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="54e1e-115">Lisää **Valitun oireen syyt** -pikavälilehdessä rivi, joka kuvaa ongelman syytä.</span><span class="sxs-lookup"><span data-stu-id="54e1e-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="54e1e-116">Lisää **Valitun oireen korjaukset** -pikavälilehdessä rivi, joka kuvaa ongelman mahdollista ratkaisua.</span><span class="sxs-lookup"><span data-stu-id="54e1e-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="54e1e-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="54e1e-117">Click **Save**.</span></span>

![Kuva 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="54e1e-119">Näytä resurssin viat</span><span class="sxs-lookup"><span data-stu-id="54e1e-119">View asset faults</span></span>

<span data-ttu-id="54e1e-120">**Resurssin viat** -luettelossa voit saada yleiskuvan kaikista omaisuuteen rekisteröidyistä virheistä.</span><span class="sxs-lookup"><span data-stu-id="54e1e-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="54e1e-121">Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssin viat** avatksesi listan.</span><span class="sxs-lookup"><span data-stu-id="54e1e-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="54e1e-122">Tulosta resurssin vikaraportti</span><span class="sxs-lookup"><span data-stu-id="54e1e-122">Print asset fault report</span></span>

<span data-ttu-id="54e1e-123">**Kaikki resurssit** luettelosivulla voit tulostaa omaisuusvikaraportin, jossa näkyvät kaikki vikamerkinnät sekä graafisen yhteenvedon vikatilastoista.</span><span class="sxs-lookup"><span data-stu-id="54e1e-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="54e1e-124">Valitse **Resurssien hallinta**  >  **Yhteiset**  >  **Resurssit**  >  **Kaikki resurssit**.</span><span class="sxs-lookup"><span data-stu-id="54e1e-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="54e1e-125">Valitse **Resurssit**-luettelosta resurssi, jolle haluat tulostaa vikaraportin.</span><span class="sxs-lookup"><span data-stu-id="54e1e-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="54e1e-126">Valitse **Yleiset**-välilehden **Raportit**-osassa **Resurssin vika**.</span><span class="sxs-lookup"><span data-stu-id="54e1e-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="54e1e-127">Lisää tietty kausi tai valitse vikatyyppi.</span><span class="sxs-lookup"><span data-stu-id="54e1e-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="54e1e-128">Tulosta raportti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="54e1e-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="54e1e-129">Voit myös tulostaa useiden resurssien tai resurssityyppien vikaraportin valitsemalla **Resurssien hallinta** > **Raportit** > **Resurssit** > **Resurssin vika**.</span><span class="sxs-lookup"><span data-stu-id="54e1e-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

