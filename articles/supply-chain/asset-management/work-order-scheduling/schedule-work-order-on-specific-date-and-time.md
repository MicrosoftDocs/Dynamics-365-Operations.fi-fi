---
title: Työtilauksen ajoittaminen tiettyyn päivämäärään ja aikaan
description: Tässä ohjeaiheessa selitetään, kuinka voit ajoittaa työtilauksen tiettyyn päivämäärään ja kellonaikaan käyttöomaisuuden hallinnassa.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 827f4ca16341d29413f1b1d928965aa1919abf59
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822512"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a><span data-ttu-id="25bb1-103">Työtilauksen ajoittaminen tiettyyn päivämäärään ja aikaan</span><span class="sxs-lookup"><span data-stu-id="25bb1-103">Schedule work order on specific date and time</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="25bb1-104">Jos työtilaus pitää ajoittaa tiettynä päivämääränä *ja* kellonaikana, voit ohittaa vakioajoitusprosessin käyttöomaisuuden hallinnassa ja luoda työtilaukselle erityisen aikataulun.</span><span class="sxs-lookup"><span data-stu-id="25bb1-104">If a work order must be scheduled on a specific date *and* time, you can override the standard scheduling process in Asset Management and create a specific schedule for a work order.</span></span>

1. <span data-ttu-id="25bb1-105">Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="25bb1-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="25bb1-106">Napsauta työtilausluettelossa **Työtilaus**- sarakkeessa olevaa työtilauksen tunnusta.</span><span class="sxs-lookup"><span data-stu-id="25bb1-106">In the work order list, click on the Work order ID in the **Work order** column.</span></span>

3. <span data-ttu-id="25bb1-107">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="25bb1-107">Click **Edit**.</span></span>

4. <span data-ttu-id="25bb1-108">Lisää **Työtilauksen otsikko** -pikavälilehdellä alkamis- ja päättymispäivämäärät ja -ajat **Odotettu alkamispäivämäärä** -ja **Odotettu loppupäivämäärä** -kenttiin.</span><span class="sxs-lookup"><span data-stu-id="25bb1-108">On the **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields.</span></span>

    ![Kuva 1](media/05-work-order-scheduling.png)

5. <span data-ttu-id="25bb1-110">Valitse **Yleiset**-välilehdessä **Ajoitus**, jos haluat käyttää vakioajoitusprosessia, tai valitse **Resursoi**, jos aiot kohdentaa työtilauksen tietylle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="25bb1-110">On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Dispatch** if you want to assign the work order to a specific worker.</span></span>

6. <span data-ttu-id="25bb1-111">Jos haluat ohittaa kaikki olemassa olevat kapasiteettivaraukset ja varmistaa, että työtilaus ajoitetaan odotettuun ajanjaksoon, tee valinnat alla olevan kuvan mukaan **Ajoita työtilaus** -valintaikkunan **Rajallinen kapasiteetti** -osassa.</span><span class="sxs-lookup"><span data-stu-id="25bb1-111">In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, make the selections as shown in the figure below in the **Schedule work order** dialog > **Finite capacity** section.</span></span> <span data-ttu-id="25bb1-112">Tämä tarkoittaa, että ajoittaminen ohittaa olemassa olevat kapasiteettivaraukset, koska työtilauksen täytyy alkaa odotetusta alkamisajasta.</span><span class="sxs-lookup"><span data-stu-id="25bb1-112">This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time.</span></span>

    ![Kuva 2](media/06-work-order-scheduling.png)

7. <span data-ttu-id="25bb1-114">Aloita ajoitus valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="25bb1-114">Click **OK** to start scheduling.</span></span>

8. <span data-ttu-id="25bb1-115">Jos ajoittaminen aiheuttaa kaksinkertaisia varauksia, näytössä näkyy sanoma ja siihen liittyviä työtilauksia voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="25bb1-115">If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders.</span></span>

>[!NOTE]
><span data-ttu-id="25bb1-116">Jotta huoltotyöntekijä voidaan ajoittaa työtilauksen, kyseisen huoltotyöntekijän on oltava käytettävissä odotettuna alkamispäivänä ja aikana.</span><span class="sxs-lookup"><span data-stu-id="25bb1-116">In order to schedule a maintenance worker for the work order, that maintenance worker must be available at the expected start date and time.</span></span> <span data-ttu-id="25bb1-117">Työntekijän käytettävyys määritetään [Työntekijän kalenterissa](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span><span class="sxs-lookup"><span data-stu-id="25bb1-117">Worker availability is set up in the [worker calendar](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span></span> 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]