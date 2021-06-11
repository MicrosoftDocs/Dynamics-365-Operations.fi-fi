---
title: Kaksoiskirjoituksen asetukset Lifecycle Servicesistä
description: Tässä aiheessa käsitellään kaksoiskirjoitusyhteyden määrittämistä Microsoft Dynamics Lifecycle Servicesistä (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103566"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="0ed3e-103">Kaksoiskirjoituksen asetukset Lifecycle Servicesistä</span><span class="sxs-lookup"><span data-stu-id="0ed3e-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0ed3e-104">Tässä aiheessa käsitellään kaksoiskirjoitusyhteyden käyttöön ottamista Microsoft Dynamics Lifecycle Servicesistä (LCS).</span><span class="sxs-lookup"><span data-stu-id="0ed3e-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0ed3e-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="0ed3e-105">Prerequisites</span></span>

<span data-ttu-id="0ed3e-106">Power Platform -integrointi on suoritettava seuraavien ohjeaiheiden mukaan:</span><span class="sxs-lookup"><span data-stu-id="0ed3e-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="0ed3e-107">Power Platform -integrointi - Ota käyttöön ympäristön käyttöönoton aikana</span><span class="sxs-lookup"><span data-stu-id="0ed3e-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="0ed3e-108">Power Platform -integrointi - Määritä ympäristön käyttöönoton jälkeen</span><span class="sxs-lookup"><span data-stu-id="0ed3e-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="0ed3e-109">Määritä kaksoiskirjoitus uusille Dataverse-ympäristöille</span><span class="sxs-lookup"><span data-stu-id="0ed3e-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="0ed3e-110">Noudattamalla näitä ohjeita voit määrittää kaksoiskirjoituksen LCS-**ympäristön tiedot** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="0ed3e-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="0ed3e-111">Laajenna **Power Platform -integrointi** -osa **Ympäristön tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="0ed3e-112">Valitse **Kaksoiskirjoitussovellus**-näppäin.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-112">Select the **Dual-write application** button.</span></span>

    ![Power Platform -integrointi](media/powerplat_integration_step2.png)

3. <span data-ttu-id="0ed3e-114">Lue ehdot ja valitse valintaruutu ja valitse sitten **Määritä**.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="0ed3e-115">Jatka valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="0ed3e-116">Voit seurata etenemistä päivittämällä säännöllisesti ympäristön tietosivun.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="0ed3e-117">Asetusten määritys kestää yleensä 30 minuuttia tai vähemmän.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="0ed3e-118">Kun asetukset on tehty, näyttöön tulee sanoma, jossa näkyy, onko prosessi onnistunut tai onko siinä ollut virhe.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="0ed3e-119">Jos asennus epäonnistui, näyttöön tulee liittyvä virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="0ed3e-120">Virheet on korjattava ennen seuraavaan vaiheeseen siirtymistä.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="0ed3e-121">Luo linkki Dataversen ja nykyisen ympäristön tietokantojen välille valitsemalla **Yhdistä Power Platform -ympäristöön**.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="0ed3e-122">Tämä kestää yleensä alle 5 minuuttia.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Yhdistä Power Platform -ympäristöön":::

8. <span data-ttu-id="0ed3e-124">Kun yhdistäminen on valmis, hyperlinkki tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="0ed3e-125">Linkin avulla voit kirjautua sisään kaksoiskirjoitusalueelle Finance and Operations -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="0ed3e-126">Siellä voit tehdä entiteettien yhdistämismäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="0ed3e-127">Määritä kaksoiskirjoitus olemassa olevalle Dataverse-ympäristölle</span><span class="sxs-lookup"><span data-stu-id="0ed3e-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="0ed3e-128">Määrittääksesi kaksoiskirjoituksen aiemmin luotuun Dataverse-ympäristöön, sinun tulee luoda Microsoft [tukipyyntö](../../lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="0ed3e-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="0ed3e-129">Pyynnössä on oltava seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="0ed3e-129">The ticket must include:</span></span>

+ <span data-ttu-id="0ed3e-130">Finance and Operations -ympäristösi tunnus.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="0ed3e-131">Lifecycle Services -ympäristösi nimi.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="0ed3e-132">Dataverse-organisaatiotunnus tai Power Platform -ympäristötunnus Power Platform -hallintakeskuksesta.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="0ed3e-133">Pyydä tukipyynnössäsi, että esiintymän tunnusta voi käyttää Power Platform -integroinnissa.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="0ed3e-134">Et voi poistaa ympäristöjen välistä linkitystä LCS-sovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="0ed3e-135">Jos haluat poistaa linkityksen, avaa **Tietojen integrointi** -työtila Finance and Operations -ympäristössä ja valitse sitten **Poista linkitys**.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
