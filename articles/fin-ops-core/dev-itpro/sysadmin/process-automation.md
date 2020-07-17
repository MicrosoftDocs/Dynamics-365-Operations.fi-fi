---
title: Prosessien automatisointi
description: Tässä ohjeaiheessa on tietoja siitä, miten prosessien automatisointi mahdollistaa eräpalvelimen käyttämien prosessien yksinkertaisen aikatauluttamisen.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508182"
---
# <a name="process-automation"></a><span data-ttu-id="449bc-103">Prosessien automatisointi</span><span class="sxs-lookup"><span data-stu-id="449bc-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="449bc-104">Prosessien automatisointi mahdollistaa eräpalvelimen käyttämien prosessien yksinkertaisen aikatauluttamisen.</span><span class="sxs-lookup"><span data-stu-id="449bc-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="449bc-105">Ajoitetun työmäärän päivitetyn kalenterinäkymän avulla peruskäyttäjät voivat tarkastella ajoitettuja ja valmiita töitä sekä tehdä niihin liittyviä toimia.</span><span class="sxs-lookup"><span data-stu-id="449bc-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="449bc-106">Hallinto</span><span class="sxs-lookup"><span data-stu-id="449bc-106">Administration</span></span>

<span data-ttu-id="449bc-107">Kaikkien prosessien automatisointien keskitetty hallintasivu löytyy **Asetukset**-valikon Järjestelmänhallinta-moduulista.</span><span class="sxs-lookup"><span data-stu-id="449bc-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="449bc-108">Tällä sivulla luetellaan kaikki järjestelmään määritetyt automaattiset prosessit (sarjat).</span><span class="sxs-lookup"><span data-stu-id="449bc-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="449bc-109">Sen avulla voit myös lisätä uusia prosessiautomaatioita suoraan tältä sivulta.</span><span class="sxs-lookup"><span data-stu-id="449bc-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="449bc-110">Kun sarja on määritetty, voit hallita kutakin sarjaa tästä luettelosta.</span><span class="sxs-lookup"><span data-stu-id="449bc-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="449bc-111">Voit halutessasi muokata koko sarjaa, poistaa sen, tarkastella kaikkia luettelonäkymän esiintymiä tai poistaa sarjan käytöstä, jos haluat keskeyttää ajoitetun työn tietyn ajanjakson ajaksi.</span><span class="sxs-lookup"><span data-stu-id="449bc-111">You can chose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a period of time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="449bc-112">Kalenterinäkymä</span><span class="sxs-lookup"><span data-stu-id="449bc-112">Calendar view</span></span> 
<span data-ttu-id="449bc-113">Yksi prosessin automaation tärkeimmistä eduista on mahdollisuus tarkastella ajoitettua työtä yksinkertaisessa kalenterinäkymässä.</span><span class="sxs-lookup"><span data-stu-id="449bc-113">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="449bc-114">Tämän näkymän avulla voit tarkastella töitä viikon kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="449bc-114">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="449bc-115">Tämä näkymä näkyy **Prosessin automatisointi** -sivun oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="449bc-115">You will see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="449bc-116">Valitun sarjan ajoitettu työmäärä täytetään.</span><span class="sxs-lookup"><span data-stu-id="449bc-116">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="449bc-117">[![Prosessin automatisointikalenteri](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="449bc-117">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="449bc-118">Esiintymän muutokset</span><span class="sxs-lookup"><span data-stu-id="449bc-118">Occurrence changes</span></span>
<span data-ttu-id="449bc-119">Kutakin esiintymää voi muokata muuttamatta niiden sarjojen määrittämiä esiintymiä, jotka ovat peräisin niistä.</span><span class="sxs-lookup"><span data-stu-id="449bc-119">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="449bc-120">Ajoitettujen töiden esiintymiä voi muokata kalenterinäkymästä valitsemalla **Näytä/Muokkaa**-painike ja valitsemalla sitten **Esiintymä**.</span><span class="sxs-lookup"><span data-stu-id="449bc-120">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="449bc-121">Näin voit käyttää kaikkia asetuksia, jotka on alun perin määritetty ohjatussa sarjan asennuksessa, ja antaa mahdollisuuden tehdä kertaluonteinen muutos valitulle esiintymälle.</span><span class="sxs-lookup"><span data-stu-id="449bc-121">This allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="449bc-122">Ajoitettujen töiden esiintyminen voidaan poistaa käytöstä myös valitsemalla **Poista käytöstä** -painike kalenterinäkymästä.</span><span class="sxs-lookup"><span data-stu-id="449bc-122">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span> 

## <a name="developer-documentation"></a><span data-ttu-id="449bc-123">Kehitysdokumentaatio</span><span class="sxs-lookup"><span data-stu-id="449bc-123">Developer documentation</span></span> 
<span data-ttu-id="449bc-124">Kehittäjien ohjeita kirjoitetaan parhaillaan, jotta kehittäjät voivat laajentaa prosessin automaatiokehystä.</span><span class="sxs-lookup"><span data-stu-id="449bc-124">Developer documentation is currently being written to allow developers to extend the process automation framework.</span></span> <span data-ttu-id="449bc-125">Näissä ohjeissa on tietoja siitä, miten voit luoda mukautettuja prosesseja, joita eräpalvelin suorittaa ajoitettuna ohjatun prosessin automatisoinnin avulla, ja tuoda ne näkyviin kalenterinäkymään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="449bc-125">This documentation will provide information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>
