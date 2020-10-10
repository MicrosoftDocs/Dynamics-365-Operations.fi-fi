---
title: Työtilauksen resursointi
description: Tässä ohjeaiheessa selitetään, miten työtilaus resursoidaan käyttöomaisuuden hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d46beb04923d06aa8ccec05355731aa1b3f27c5b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889286"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="cd380-103">Työtilauksen resursointi</span><span class="sxs-lookup"><span data-stu-id="cd380-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="cd380-104">Voit ajoittaa yhden työtilauksen tai työtilauksen työt yhdelle työntekijälle **Resursoi**-toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="cd380-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="cd380-105">Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="cd380-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="cd380-106">Valitse työtilaus luettelosta.</span><span class="sxs-lookup"><span data-stu-id="cd380-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="cd380-107">Valitse **Yleiset**-välilehdestä **Resursoi**.</span><span class="sxs-lookup"><span data-stu-id="cd380-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="cd380-108">Valitse **Ajoita työtilaus** -valintaikkunassa työntekijä **Työntekijä**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="cd380-108">In the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="cd380-109">**Ajoita tunnit** -kenttään voit lisätä odotettuja työtunteja, jos odotettavissa oleva työaika poikkeaa ennustetunneista.</span><span class="sxs-lookup"><span data-stu-id="cd380-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="cd380-110">**Ajoitettu aloitus** -kenttään voit tarvittaessa muokata aloituspäivämäärää ja aikaa.</span><span class="sxs-lookup"><span data-stu-id="cd380-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="cd380-111">Jos ajoitusprosessissa on huomioitava muiden töiden jo ajoitettujen resurssien kapasiteettirajoitukset, varmista, että **Resurssi**, **Työkalu** ja **Työntekijä**-vaihtopainikkeiden arvoksi on määritetty **Kyllä.**</span><span class="sxs-lookup"><span data-stu-id="cd380-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to **Yes**.</span></span> <span data-ttu-id="cd380-112">Jos haluat nähdä yksityiskohtaisia tietoja aikataulutuksesta, valitse **Kyllä** **Yksityiskohtainen**-vaihtopainikkeessa.</span><span class="sxs-lookup"><span data-stu-id="cd380-112">If you want to see detailed information about the scheduling process, select **Yes** on the **Verbose** toggle button.</span></span> <span data-ttu-id="cd380-113">Tämä tarkoittaa, että työtilauksen laskettujen pisteiden tiedot näytetään infolokissa.</span><span class="sxs-lookup"><span data-stu-id="cd380-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="cd380-114">Valitse **Kyllä** **Ohita aikataulu** -vaihtopainikkeessa, jos haluat ohittaa kalenterin suljetut päivät (koskee käyttöomaisuus erää, työntekijää ja työkaluja).</span><span class="sxs-lookup"><span data-stu-id="cd380-114">Select **Yes** on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="cd380-115">Valitse **Kyllä** **Ohita ajoitettu suoritus** -vaihtopainikkeessa, jos haluat ohittaa rajoitukset, jotka on mahdollisesti valittu työtilaukselle ajoituksen osalta.</span><span class="sxs-lookup"><span data-stu-id="cd380-115">Select **Yes** on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> 

    <span data-ttu-id="cd380-116">Ajoitetun suorituksen määrityksestä on lisätietoja osassa [Ajoitettu suoritus](../setup-for-work-orders/scheduled-execution.md).</span><span class="sxs-lookup"><span data-stu-id="cd380-116">For information on the setup of scheduled execution, see the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section.</span></span>

9. <span data-ttu-id="cd380-117">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd380-117">Click **OK**.</span></span> <span data-ttu-id="cd380-118">Työtilauksen elinkaaren tila päivittyy automaattisesti **Ajoitettu**-elinkaaritilaan, joka on määritetty kohdassa **Resurssienhallinta** > **Asetukset** > **Työtilaukset** > **Elinkaarimallit**.</span><span class="sxs-lookup"><span data-stu-id="cd380-118">The work order lifecycle state is automatically updated to the **Scheduled** lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="cd380-119">Alla olevassa kuvassa näkyy esimerkki resursointivalinnoista **Ajoita työtilaus** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="cd380-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![Kuva 1](media/04-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="cd380-121">Jos haluat poistaa aikataulun työtilauksesta, valitse työtilaus kohdassa **Kaikki työtilaukset** ja valitsemalla **Yleiset**-välilehdestä **Poista ajoitus**. Muista päivittää työtilauksen elinkaaritila manuaalisesti, jos poistat aikataulun.</span><span class="sxs-lookup"><span data-stu-id="cd380-121">If you want to delete the schedule on a work order, select the work order in **All work orders**, and then click **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

