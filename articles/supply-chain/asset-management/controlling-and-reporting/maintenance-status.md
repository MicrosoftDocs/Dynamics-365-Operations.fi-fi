---
title: Ylläpidon tila
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpidon tila lasketaan resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918346"
---
# <a name="maintenance-status"></a><span data-ttu-id="900ba-103">Ylläpidon tila</span><span class="sxs-lookup"><span data-stu-id="900ba-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="900ba-104">Käyttöomaisuuden hallinnassa voit laskea yhteenvedon, jossa on tietoja uusista, aktiivisista ja valmiista huoltopyynnöistä, työtilauksista ja ylläpitoseisokeista tietyltä kaudelta.</span><span class="sxs-lookup"><span data-stu-id="900ba-104">In Asset Management, you can make a calculation to see an overview of new, active, and completed maintenance requests, work orders, and maintenance downtime activities for a specific period.</span></span> <span data-ttu-id="900ba-105">Voit tarkastella myös saman kauden suoritettujen kuntoarviointien määrää.</span><span class="sxs-lookup"><span data-stu-id="900ba-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="900ba-106">Tämän laskennan avulla saat yleiskuvan saapuvien ja suoritettujen kunnossapitopyyntöjen ja työtilausten kuormituksesta.</span><span class="sxs-lookup"><span data-stu-id="900ba-106">Use this calculation to get an overview of workload regarding incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="900ba-107">Ylläpidon tilan laskennan suorittaminen</span><span class="sxs-lookup"><span data-stu-id="900ba-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="900ba-108">Valitse **Resurssien hallinta** > **Kyselyt** > **Ylläpidon tila**.</span><span class="sxs-lookup"><span data-stu-id="900ba-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="900ba-109">Valitse **Laske tila** -valintaikkunassa kausi, jonka ajalta haluat tehdä laskennan (**Alkamispäivämäärä**- ja **Päättymispäivämäärä** -kentät).</span><span class="sxs-lookup"><span data-stu-id="900ba-109">In the **Calculate status** dialog, select the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="900ba-110">**Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia ylläpitoriveistä haluat liittyen toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="900ba-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> <span data-ttu-id="900ba-111">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoinen toiminnallinen sijaintirakenne, kaikki toimintosijainnin ylläpitorivit näkyvät ylimmällä tasolla, joten rivin tila voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="900ba-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="900ba-112">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki ylläpitorivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="900ba-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="900ba-113">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="900ba-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="900ba-114">Valitse toimintoruudun **Ryhmittely...** -ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason.</span><span class="sxs-lookup"><span data-stu-id="900ba-114">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="900ba-115">Valitut toimintoruudun painikkeet on korostettu.</span><span class="sxs-lookup"><span data-stu-id="900ba-115">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="900ba-116">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="900ba-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="900ba-117">Muista napsauttaa **Päivitä**-painiketta, jos haluat päivittää laskemisen aina, kun teet muutoksia aktivoimalla tai poistamalla käytöstä **Ryhmittely...**  -painikkeita tai tekemällä laskelmia uudelle kaudelle.</span><span class="sxs-lookup"><span data-stu-id="900ba-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by...** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="900ba-118">Valitse **Tila**, jos haluat luoda uuden ylläpitotilan laskemisen.</span><span class="sxs-lookup"><span data-stu-id="900ba-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="900ba-119">**Ylläpitotila**-kohdassa näkyvät tulokset koskevat vain huoltopyyntöjä ja työtilauksia, joilla on todellinen alkamispäivämäärä ja -aika.</span><span class="sxs-lookup"><span data-stu-id="900ba-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="900ba-120">Päättymispäivämäärä ja -aika voivat olla tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="900ba-120">End date and time may be blank.</span></span>

<span data-ttu-id="900ba-121">*Esimerkki 1:*</span><span class="sxs-lookup"><span data-stu-id="900ba-121">*Example 1:*</span></span>

<span data-ttu-id="900ba-122">Alla olevassa kuvassa **Vuosi**- ja **Kuukausi**-painikkeet on aktivoitu.</span><span class="sxs-lookup"><span data-stu-id="900ba-122">In the figure below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="900ba-123">Tässä saat yleiskuvan ylläpitopyyntöihin ja työtilauksiin liittyvästä kuormituksesta ja suoritusnopeudesta kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="900ba-123">Here, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Kuva 1](media/13-controlling-and-reporting.png)

<span data-ttu-id="900ba-125">*Esimerkki 2:*</span><span class="sxs-lookup"><span data-stu-id="900ba-125">*Example 2:*</span></span>

<span data-ttu-id="900ba-126">Alla olevassa kuvassa on lisätty tietoja toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="900ba-126">In the figure below, information about functional locations has been added.</span></span> <span data-ttu-id="900ba-127">Nyt on mahdollista vertailla työmäärää ja suorituskykyä eri toiminnallisissa sijainneissa, jotka voivat edustaa maantieteellisiä sijainteja, tehtaita tai työalueita.</span><span class="sxs-lookup"><span data-stu-id="900ba-127">Now, it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Kuva 2](media/14-controlling-and-reporting.png)

