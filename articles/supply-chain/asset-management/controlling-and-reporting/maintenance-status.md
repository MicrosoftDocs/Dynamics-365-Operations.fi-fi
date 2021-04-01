---
title: Ylläpidon tila
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpidon tila lasketaan resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f65bfc7b5ef9651853a12bab2ed83dbb8562ba6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253731"
---
# <a name="maintenance-status"></a><span data-ttu-id="b2a97-103">Ylläpitotila</span><span class="sxs-lookup"><span data-stu-id="b2a97-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b2a97-104">Resurssienhallinnassa voit laskea yhteenvedon, jossa on tietoja uusista, aktiivisista ja valmiista ylläpitopyynnöistä, työtilauksista ja ylläpidon käyttökatkoista tietyltä kaudelta.</span><span class="sxs-lookup"><span data-stu-id="b2a97-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="b2a97-105">Voit tarkastella myös saman kauden suoritettujen kuntoarviointien määrää.</span><span class="sxs-lookup"><span data-stu-id="b2a97-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="b2a97-106">Tämän laskennan avulla saat yleiskuvan saapuvien ja suoritettujen kunnossapitopyyntöjen ja työtilausten kuormituksesta.</span><span class="sxs-lookup"><span data-stu-id="b2a97-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="b2a97-107">Ylläpidon tilan laskennan suorittaminen</span><span class="sxs-lookup"><span data-stu-id="b2a97-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="b2a97-108">Valitse **Resurssien hallinta** > **Kyselyt** > **Ylläpidon tila**.</span><span class="sxs-lookup"><span data-stu-id="b2a97-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="b2a97-109">Valitse **Laske tila** -valintaikkunassa aikaväli, jonka ajalta haluat tehdä laskennan (**Alkamispäivämäärä**- ja **Päättymispäivämäärä** -kentät).</span><span class="sxs-lookup"><span data-stu-id="b2a97-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="b2a97-110">**Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia ylläpitoriveistä haluat liittyen toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="b2a97-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="b2a97-111">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoinen toiminnallinen sijaintirakenne, kaikki toimintosijainnin ylläpitorivit näkyvät ylimmällä tasolla, joten rivin tila voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="b2a97-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="b2a97-112">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki ylläpitorivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="b2a97-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="b2a97-113">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2a97-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="b2a97-114">Valitse **Ryhmittely...**-painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason.</span><span class="sxs-lookup"><span data-stu-id="b2a97-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="b2a97-115">Valitut **Ryhmittely...**-painikkeet on korostettu.</span><span class="sxs-lookup"><span data-stu-id="b2a97-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="b2a97-116">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="b2a97-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="b2a97-117">Muista napsauttaa **Päivitä**-painiketta, jos haluat päivittää laskemisen aina, kun teet muutoksia aktivoimalla tai poistamalla käytöstä **Ryhmittely...**-painikkeita tai tekemällä laskelmia uudelle kaudelle.</span><span class="sxs-lookup"><span data-stu-id="b2a97-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="b2a97-118">Valitse **Tila**, jos haluat luoda uuden ylläpitotilan laskemisen.</span><span class="sxs-lookup"><span data-stu-id="b2a97-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="b2a97-119">**Ylläpitotila**-kohdassa näkyvät tulokset koskevat vain huoltopyyntöjä ja työtilauksia, joilla on todellinen alkamispäivämäärä ja -aika.</span><span class="sxs-lookup"><span data-stu-id="b2a97-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="b2a97-120">Päättymispäivämäärä ja -aika voivat olla tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="b2a97-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="b2a97-121">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="b2a97-121">Example 1</span></span>

<span data-ttu-id="b2a97-122">Alla olevassa näyttökuvassa **Vuosi**- ja **Kuukausi**-painikkeet on aktivoitu.</span><span class="sxs-lookup"><span data-stu-id="b2a97-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="b2a97-123">Kun nämä **Ryhmittely...**-asetukset on valittu, saat yleiskuvan ylläpitopyyntöihin ja työtilauksiin liittyvästä kuormituksesta ja suoritusnopeudesta kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="b2a97-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Esimerkki kuukausittaisesta kuormituksesta](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="b2a97-125">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="b2a97-125">Example 2</span></span>

<span data-ttu-id="b2a97-126">Alla olevassa näyttökuvassa on lisätty tietoja toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="b2a97-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="b2a97-127">Nyt on mahdollista vertailla työmäärää ja suorituskykyä eri toiminnallisissa sijainneissa, jotka voivat edustaa maantieteellisiä sijainteja, tehtaita tai työalueita.</span><span class="sxs-lookup"><span data-stu-id="b2a97-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Esimerkki kuukausittaisesta kuormituksesta ja toiminnallisista sijainneista](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]