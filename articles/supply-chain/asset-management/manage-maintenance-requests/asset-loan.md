---
title: Lainatut resurssit
description: Tässä ohjeaiheessa kerrotaan, miten lainatut resurssit rekisteröidään resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a365fb5b1e0126b9de56bcc84a14f2352208d4f
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571711"
---
# <a name="asset-loans"></a><span data-ttu-id="bb234-103">Lainatut resurssit</span><span class="sxs-lookup"><span data-stu-id="bb234-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="bb234-104">Jos yrityksesi saa resursseja korjaus-tai huoltotöihin joko sisäisistä sijainneista tai asiakkailta ja jos olet tilapäisesti lainannut resursseja kyseisille sijainteille tai asiakkaille, resurssien hallinta voi seurata resurssilainoja.</span><span class="sxs-lookup"><span data-stu-id="bb234-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="bb234-105">Rekisteröi kunnossapitopyynnön resurssilainat</span><span class="sxs-lookup"><span data-stu-id="bb234-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="bb234-106">Valitse **Resurssien hallinta** \> **yhteiset** \> **Ylläpitopyynnöt** \> **Kaikki ylläpitopyynnöt** ta **Aktiiviset ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="bb234-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="bb234-107">Valitse ylläpitopyyntö, johon resurssilaina rekisteröidään, ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="bb234-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="bb234-108">Valitse **Pyyntö**-sivulla **Lähetä lainaresurssi**.</span><span class="sxs-lookup"><span data-stu-id="bb234-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="bb234-109">Valitse resurssi ja syötä odotettu palautuspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="bb234-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="bb234-110">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb234-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="bb234-111">Voit lähettää lainaresurssin vain, jos saman resurssityypin resurssi on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="bb234-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="bb234-112">Lainatulla resurssilla on oltava resurssien elinkaaritila, jonka avulla sitä voidaan käyttää lainaresurssina, kuten **InStorage**.</span><span class="sxs-lookup"><span data-stu-id="bb234-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="bb234-113">Kun resurssilaina on rekisteröity, resurssin elinkaaren tila päivitetään automaattisesti esimerkiksi tilaan **onLoan**.</span><span class="sxs-lookup"><span data-stu-id="bb234-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="bb234-114">Voit tarkastella luettelosa kaikista resursseista, jotka olet lainannut muihin siajinetihin tai asiakkaille valitsemalla **Resurssien hallinta** \> **Yhteiset** \> **Resurssin laina** \> **Kaikki resurssilainat**.</span><span class="sxs-lookup"><span data-stu-id="bb234-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="bb234-115">Jos **Päättynyt** -valintaruutu on valittuna resurssille, resurssi on rekisteröity palautetuksi yritykseesi.</span><span class="sxs-lookup"><span data-stu-id="bb234-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Ylläpitopyyntöjen hallinta](media/06-manage-maintenance-requests.png)

<span data-ttu-id="bb234-117">**Aktiiviset resurssilainat** -sivulla voit tarkastella luetteloa kaikista lainavaroista, joita ei ole vielä palautettu yrityksellesi.</span><span class="sxs-lookup"><span data-stu-id="bb234-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="bb234-118">Rekisteröi lainaresurssit palautetuksi</span><span class="sxs-lookup"><span data-stu-id="bb234-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="bb234-119">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssin laina** \> **Aktiiviset resurssilainat**.</span><span class="sxs-lookup"><span data-stu-id="bb234-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="bb234-120">Valitse resurssilaina, jonka haluat rekisteröidä palautetuksi, ja valitse sitten **Palauta resurssilaina**.</span><span class="sxs-lookup"><span data-stu-id="bb234-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="bb234-121">Määritä päivämäärä ja kellonaika **Palautettu**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="bb234-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="bb234-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb234-122">Select **OK**.</span></span>
5. <span data-ttu-id="bb234-123">Päivitä **Aktiiviset resurssilainat** -luetteloivu ja huomaa, että resurssilaina ei enää näy luettelossa.</span><span class="sxs-lookup"><span data-stu-id="bb234-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
