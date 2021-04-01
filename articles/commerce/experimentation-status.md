---
title: Kokeen tilan tarkistaminen
description: Tässä ohjeaiheessa käsitellään kokeen tilaa kokeilun elinkaaren aikana Dynamics 365 Commercessa.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ae459ddaf947db6c3de2602a706390edab49efa1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250855"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="5ca19-103">Kokeen tilan tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="5ca19-103">Review the status of an experiment</span></span>
<span data-ttu-id="5ca19-104">Kokeen määrittäminen ja suorittaminen Dynamics 365 Commercessa on monivaiheinen prosessi.</span><span class="sxs-lookup"><span data-stu-id="5ca19-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="5ca19-105">Lisätietoja kokeilun elinkaaresta on kohdassa [Kokeilut Dynamics 365 Commercessa](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5ca19-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="5ca19-106">Kokeen elinkaaren vaiheen voi tarkistaa Commercen sivustonmuodostimen vasemman siirtymisruudun **Kokeet**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="5ca19-106">To learn where an experiment is in the lifecycle, in Commerce site builder select **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="5ca19-107">Näkyvissä on koeluettelo sekä kunkin kokeen tila sekä Commercessa että siinä kolmannen osapuolen palvelussa, jossa kokeet luodaan, variaatiot määritetään ja tiedot analysoidaan.</span><span class="sxs-lookup"><span data-stu-id="5ca19-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="5ca19-108">**Commerce-tila**-sarakkeessa on jokin seuraavista arvoista:</span><span class="sxs-lookup"><span data-stu-id="5ca19-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="5ca19-109">**Luonnos** – koe on yhdistetty sivuun tai osaan Commercessa ja sitä muokataan.</span><span class="sxs-lookup"><span data-stu-id="5ca19-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="5ca19-110">**Julkaistu** – Kokeen variaatiot ovat valmiita näytettäviksi sivustossa.</span><span class="sxs-lookup"><span data-stu-id="5ca19-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="5ca19-111">Jos koe suoritetaan kolmannen osapuolen palvelussa, sivuston käyttäjät näkevät kolmannen osapuolen palvelun valitseman sivu- tai osavariaation.</span><span class="sxs-lookup"><span data-stu-id="5ca19-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="5ca19-112">**Julkaisu peruutettu** – Koe ei ole enää käytettävissä sivustossa.</span><span class="sxs-lookup"><span data-stu-id="5ca19-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="5ca19-113">Sivuston käyttäjät näkevät vain sivun tai osan oletusversion, vaikka suoritus olisi käynnissä kolmannen osapuolen palvelussa.</span><span class="sxs-lookup"><span data-stu-id="5ca19-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="5ca19-114">**Valmis** – koe on päättynyt ja variaatio on korotettu live-sivustoon kaikkien sivuston käyttäjien käyttöön.</span><span class="sxs-lookup"><span data-stu-id="5ca19-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="5ca19-115">Vastaavasti **kolmannen osapuolen tilasarakkeessa** seuraavat arvot ilmaisevat, mikä on kolmannen osapuolen palvelussa olevien kokeiden tila.</span><span class="sxs-lookup"><span data-stu-id="5ca19-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="5ca19-116">**Luonnos** – koe on määritetty kolmannen osapuolen palvelussa, mutta sitä ei ole vielä aloitettu.</span><span class="sxs-lookup"><span data-stu-id="5ca19-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="5ca19-117">**Suoritetaan** – koe on aloitettu kolmannen osapuolen palvelussa ja kerää tietoja.</span><span class="sxs-lookup"><span data-stu-id="5ca19-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="5ca19-118">**Keskeytetty** – Koe on keskeytetty eikä kerää tietoja.</span><span class="sxs-lookup"><span data-stu-id="5ca19-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="5ca19-119">Koetta on jatkettava, jotta tietoja voidaan taas kerätä.</span><span class="sxs-lookup"><span data-stu-id="5ca19-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="5ca19-120">**Arkistoitu** – koe on suoritettu loppuun ja se on luetteloitu kolmannen osapuolen palvelussa tulevaa käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="5ca19-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="5ca19-121">Molemmat tilajoukot ja niiden keskinäinen suhde näkyy seuraavassa kaaviossa.</span><span class="sxs-lookup"><span data-stu-id="5ca19-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="5ca19-122">[ ![Kokeilun tilat](./media/experimentation_statuses.svg)](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="5ca19-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]