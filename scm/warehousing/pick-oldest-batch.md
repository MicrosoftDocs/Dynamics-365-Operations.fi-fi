---
title: "Mobiililaitteen vanhimman erän kerääminen"
description: "Tässä ohjeaiheessa kerrotaan mobiililaitteen vanhimman erän keräysvaihtoehdon määrittämisestä ja käyttämisestä."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 25056886b1a18dbaef12c8732a1fd0bd92a6d04b
ms.contentlocale: fi-fi
ms.lasthandoff: 07/18/2017

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="bfd14-103">Mobiililaitteen vanhimman erän kerääminen</span><span class="sxs-lookup"><span data-stu-id="bfd14-103">Pick oldest batch on a mobile device</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bfd14-104">Voit käyttää **Valitse vanhin erä** -määritystä mobiililaitteen valikosta. Voit pakottaa sen avulla varastotyöntekijät keräämään vanhimman erän nykyisestä sijainnista tai varoittaa heitä siitä.</span><span class="sxs-lookup"><span data-stu-id="bfd14-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="bfd14-105">Käyttö</span><span class="sxs-lookup"><span data-stu-id="bfd14-105">Where it applies</span></span>
<span data-ttu-id="bfd14-106">Vanhimman erän valinta on määritetty mobiililaitteen valikkovaihtoehdoissa ja se vaikuttaa erän alempien nimikkeiden keräilyyn.</span><span class="sxs-lookup"><span data-stu-id="bfd14-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="bfd14-107">Vanhimman erän valinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bfd14-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="bfd14-108">Aiemmin luotua työtä käyttämään määritetyillä nimikkeillä **Valitse vanhin erä** -asetukseksi voidaan valita **Ei mitään**, **Varoita** tai **Pakota** mobiililaitteen valikossa.</span><span class="sxs-lookup"><span data-stu-id="bfd14-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="bfd14-109">**Ei mitään**: työntekijät eivät saa mitään ilmoituksia ja he saavat kerätä minkä tahansa erä omassa sijainnissaan.</span><span class="sxs-lookup"><span data-stu-id="bfd14-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="bfd14-110">**Varoita** ja **Pakota**: luettelo eristä, joilla on vanhimmat vanhentumispäivät, näytetään erähallinnan yläpuolella, kun työntekijä valitsee erän.</span><span class="sxs-lookup"><span data-stu-id="bfd14-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="bfd14-111">Jos rekisterikilven sijainti on ohjattu, rekisterikilpiluettelo, jossa on vanhin erä, näkyy rekisterikilven ohjausobjektin yläpuolella.</span><span class="sxs-lookup"><span data-stu-id="bfd14-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="bfd14-112">**Varoita**: jos työntekijä valitsee rekisterikilven tai erän, joka ei näy luettelossa, ohjausobjekti on tyhjennetty ja varoitus ilmoittaa, että valittavana on vanhempi erä.</span><span class="sxs-lookup"><span data-stu-id="bfd14-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="bfd14-113">Työn jatkaminen on edellyttää, että työntekijä valitsee uudelleen saman rekisterikilven tai erän.</span><span class="sxs-lookup"><span data-stu-id="bfd14-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="bfd14-114">**Pakota**: työntekijä saa edelleen ilmoituksia, että valittavana vanhempi erä.</span><span class="sxs-lookup"><span data-stu-id="bfd14-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>

