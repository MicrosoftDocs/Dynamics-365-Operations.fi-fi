---
title: Prosessien automatisointi
description: Tässä ohjeaiheessa on tietoja siitä, miten prosessien automatisointi mahdollistaa eräpalvelimen käyttämien prosessien yksinkertaisen aikatauluttamisen.
author: RyanCCarlson2
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 509decec3c3d3b598a2457cddba4896730480ec6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745922"
---
# <a name="process-automation"></a><span data-ttu-id="30bdb-103">Prosessien automatisointi</span><span class="sxs-lookup"><span data-stu-id="30bdb-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="30bdb-104">Prosessien automatisointi mahdollistaa eräpalvelimen käyttämien prosessien yksinkertaisen aikatauluttamisen.</span><span class="sxs-lookup"><span data-stu-id="30bdb-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="30bdb-105">Ajoitetun työmäärän päivitetyn kalenterinäkymän avulla peruskäyttäjät voivat tarkastella ajoitettuja ja valmiita töitä sekä tehdä niihin liittyviä toimia.</span><span class="sxs-lookup"><span data-stu-id="30bdb-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="30bdb-106">Hallinto</span><span class="sxs-lookup"><span data-stu-id="30bdb-106">Administration</span></span>

<span data-ttu-id="30bdb-107">Kaikkien prosessien automatisointien keskitetty hallintasivu löytyy **Asetukset**-valikon Järjestelmänhallinta-moduulista.</span><span class="sxs-lookup"><span data-stu-id="30bdb-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="30bdb-108">Tällä sivulla luetellaan kaikki järjestelmään määritetyt automaattiset prosessit (sarjat).</span><span class="sxs-lookup"><span data-stu-id="30bdb-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="30bdb-109">Sen avulla voit myös lisätä uusia prosessiautomaatioita suoraan tältä sivulta.</span><span class="sxs-lookup"><span data-stu-id="30bdb-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="30bdb-110">Kun sarja on määritetty, voit hallita kutakin sarjaa tästä luettelosta.</span><span class="sxs-lookup"><span data-stu-id="30bdb-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="30bdb-111">Voit halutessasi muokata koko sarjaa, poistaa sen, tarkastella kaikkia luettelonäkymän esiintymiä tai poistaa sarjan käytöstä, jos haluat keskeyttää ajoitetun työn tietyksi aikaa.</span><span class="sxs-lookup"><span data-stu-id="30bdb-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="30bdb-112">Kaikki ominaisuuksien hallinnassa käytöstä poistetut prosessit eivät näy, kun toiminto on poistettu käytöstä.</span><span class="sxs-lookup"><span data-stu-id="30bdb-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="30bdb-113">Lisäksi prosessiautomaation ajoitusmoduuli ei ajoita esiintymiä tai taustaprosesseja käytöstä poistetun ominaisuuden osalta.</span><span class="sxs-lookup"><span data-stu-id="30bdb-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="30bdb-114">Kun ominaisuus otetaan uudelleen käyttöön, kaikki ajoitetut esiintymät tai taustaprosessit suoritetaan heti.</span><span class="sxs-lookup"><span data-stu-id="30bdb-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span>

## <a name="calendar-view"></a><span data-ttu-id="30bdb-115">Kalenterinäkymä</span><span class="sxs-lookup"><span data-stu-id="30bdb-115">Calendar view</span></span>

<span data-ttu-id="30bdb-116">Yksi prosessin automaation tärkeimmistä eduista on mahdollisuus tarkastella ajoitettua työtä yksinkertaisessa kalenterinäkymässä.</span><span class="sxs-lookup"><span data-stu-id="30bdb-116">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="30bdb-117">Tämän näkymän avulla voit tarkastella töitä viikon kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="30bdb-117">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="30bdb-118">Tämä näkymä näkyy **Prosessin automatisointi** -sivun oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="30bdb-118">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="30bdb-119">Valitun sarjan ajoitettu työmäärä täytetään.</span><span class="sxs-lookup"><span data-stu-id="30bdb-119">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="30bdb-120">[![Prosessin automatisointikalenteri](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="30bdb-120">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="30bdb-121">Esiintymän muutokset</span><span class="sxs-lookup"><span data-stu-id="30bdb-121">Occurrence changes</span></span>

<span data-ttu-id="30bdb-122">Kutakin esiintymää voi muokata muuttamatta niiden sarjojen määrittämiä esiintymiä, jotka ovat peräisin niistä.</span><span class="sxs-lookup"><span data-stu-id="30bdb-122">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="30bdb-123">Ajoitettujen töiden esiintymiä voi muokata kalenterinäkymästä valitsemalla **Näytä/Muokkaa**-painike ja valitsemalla sitten **Esiintymä**.</span><span class="sxs-lookup"><span data-stu-id="30bdb-123">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="30bdb-124">Tämän sivun avulla voit käyttää kaikkia asetuksia, jotka on alun perin määritetty ohjatussa sarjan asennuksessa, ja antaa mahdollisuuden tehdä kertaluonteinen muutos valitulle esiintymälle.</span><span class="sxs-lookup"><span data-stu-id="30bdb-124">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="30bdb-125">Ajoitettujen töiden esiintyminen voidaan poistaa käytöstä myös valitsemalla **Poista käytöstä** -painike kalenterinäkymästä.</span><span class="sxs-lookup"><span data-stu-id="30bdb-125">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="30bdb-126">Kehitysdokumentaatio</span><span class="sxs-lookup"><span data-stu-id="30bdb-126">Developer documentation</span></span>

<span data-ttu-id="30bdb-127">Prosessin automaatiokehyksen avulla kehittäjät voivat laajentaa prosessin automaatiokehystä.</span><span class="sxs-lookup"><span data-stu-id="30bdb-127">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="30bdb-128">[Prosessin automaatiokehys](../process-automation/process-automation-framework.md) -dokumentaatio sisältää tietoja siitä, miten voit luoda mukautettuja prosesseja, joita eräpalvelin suorittaa ajoitettuna ohjatun prosessin automatisoinnin avulla, ja tuoda ne näkyviin kalenterinäkymään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="30bdb-128">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]