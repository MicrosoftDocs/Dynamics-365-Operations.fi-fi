---
title: Sivujen näyttäminen rinnakkain Avaa uudessa ikkunassa -toiminnon avulla
description: Tässä artikkelissa kerrotaan, miten sivut voidaan näyttää rinnakkain.
author: aneesmsft
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7144f26c0977fbc420b804728151262b2f166bc0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180688"
---
# <a name="show-pages-side-by-side-by-using-the-open-in-new-window-feature"></a><span data-ttu-id="a46d6-103">Sivujen näyttäminen rinnakkain Avaa uudessa ikkunassa -toiminnon avulla</span><span class="sxs-lookup"><span data-stu-id="a46d6-103">Show pages side by side by using the Open in new window feature</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a46d6-104">Tässä artikkelissa kerrotaan, miten sivut voidaan näyttää rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="a46d6-104">This article explains how to display pages side-by-side.</span></span>

<span data-ttu-id="a46d6-105">Joskus tehtäviä halutaan suorittaa nopeasti ja tarkastella useita sivuja rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="a46d6-105">You may want to view multiple pages side-by-side to complete tasks quickly.</span></span> <span data-ttu-id="a46d6-106">Voit esimerkiksi haluta tarkistaa usean kirjauskansion rivejä tai syöttää niitä useaan kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="a46d6-106">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="a46d6-107">Yleensä tämä vaatii palaamisen kirjauskansioluettelon sisältävälle sivulle ja takaisin tietyn kirjauskansion sisältävälle sivulle.</span><span class="sxs-lookup"><span data-stu-id="a46d6-107">Typically, to do this you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="a46d6-108">**Avaa uudessa ikkunassa** -toiminnon avulla voit kuitenkin näyttää nämä sivut rinnakkain, jolloin tehtävien suorittaminen nopeutuu.</span><span class="sxs-lookup"><span data-stu-id="a46d6-108">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span>

<span data-ttu-id="a46d6-109">Kun haluat tarkastella rivejä, voit valita **Avaa uudessa ikkunassa** -kuvakkeen.</span><span class="sxs-lookup"><span data-stu-id="a46d6-109">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span>

<span data-ttu-id="a46d6-110">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="a46d6-110">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span>

<span data-ttu-id="a46d6-111">Kun **Avaa uudessa ikkunassa** -kuvake valitaan, rivien sivu avataan uudessa selainikkunassa ponnahdusikkunana. Tämän jälkeen siirrytään takaisin alkuperäisen selaimen aiemmalle sivulle, joka on kirjauskansioluettelon sisältävä sivu.</span><span class="sxs-lookup"><span data-stu-id="a46d6-111">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="a46d6-112">Tämän jälkeen sivut voidaan näyttää rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="a46d6-112">You can then display both pages side-by-side.</span></span> <span data-ttu-id="a46d6-113">Kun kirjauskansion tarkasteleminen on tehty, voit muuttaa kirjauskansiovalinnan kirjauskansioluettelosivulla. Tällöin ponnahdusikkunan rivien sivulla näytetään automaattisesti juuri valitun kirjauskansion rivit.</span><span class="sxs-lookup"><span data-stu-id="a46d6-113">When you are done viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span>

<span data-ttu-id="a46d6-114">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="a46d6-114">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span>

<span data-ttu-id="a46d6-115">Dynaaminen linkitys ja päivittäminen tapahtuu näiden sivujen taustalla olevien tietojen suhteiden vuoksi.</span><span class="sxs-lookup"><span data-stu-id="a46d6-115">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="a46d6-116">Jos järjestelmä ei ota huomioon tietojen välisiä suhteita, ponnahdusikkunaa ei päivitetä automaattisesti alkuperäisessä ikkunassa tehtävien muutosten perusteella.</span><span class="sxs-lookup"><span data-stu-id="a46d6-116">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span>

<span data-ttu-id="a46d6-117">Joillakin sivuilla on useita näkymiä, kuten ruudukko-, otsikko- ja tietonäkymä.</span><span class="sxs-lookup"><span data-stu-id="a46d6-117">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="a46d6-118">**Avaa uudessa ikkunassa** -kuvake avaa koko sivun uudessa selainikkunassa.</span><span class="sxs-lookup"><span data-stu-id="a46d6-118">The **Open in new window** icon causes the entire page to be opened in the new browser window.</span></span> <span data-ttu-id="a46d6-119">Tämän vuoksi **Avaa uudessa ikkunassa** -toiminnon avulla samaa sivua ei voi näyttää rinnakkain.</span><span class="sxs-lookup"><span data-stu-id="a46d6-119">Therefore, you cannot keep two views of the same page side-by-side using the **Open in new window** feature.</span></span> <span data-ttu-id="a46d6-120">Melkein kaikilla tällaisilla sivuilla on kuitenkin siirtymisluettelo, jonka avulla tietueiden välillä voi siirtyä. Tällöin käyttökokemus on samanlainen.</span><span class="sxs-lookup"><span data-stu-id="a46d6-120">However, almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span>

<span data-ttu-id="a46d6-121">Määritä selaimen ponnahdusikkunoiden estotoiminto sallimaan ponnahdusikkunat sivuston URL-osoitteesta, ennen kuin käytät **Avaa uudessa ikkunassa** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="a46d6-121">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the site.</span></span> <span data-ttu-id="a46d6-122">Ponnahdusikkunat voidaan sallia esimerkiksi osoitteesta \*.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="a46d6-122">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span>

<span data-ttu-id="a46d6-123">**Avaa uudessa ikkunassa** -toiminto on käytettävissä vain, kun ikkunassa on avoinna useita sivuja.</span><span class="sxs-lookup"><span data-stu-id="a46d6-123">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="a46d6-124">Ponnahdusikkunan suljetaan automaattisesti, kun sivuja ei ole enää avoinna (eli sitten, kun ikkunan viimeinen sivu suljetaan).</span><span class="sxs-lookup"><span data-stu-id="a46d6-124">Also, the pop-up window automatically closes when there are no more pages open (that is, when the last page in that window is closed).</span></span> <span data-ttu-id="a46d6-125">Järjestelmä sulkee sivut myös silloin, kun siirryt sovelluksen toiselle alueelle.</span><span class="sxs-lookup"><span data-stu-id="a46d6-125">The system also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="a46d6-126">Jos ponnahdusikkunoita siis on avoinna silloin, kun siirryt sovelluksen toiselle alueelle, ponnahdusikkunat suljetaan automaattisesti, koska järjestelmä sulkee ikkunoissa olevat sivut.</span><span class="sxs-lookup"><span data-stu-id="a46d6-126">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows are automatically closed because the pages in those windows were closed by the system.</span></span>

<span data-ttu-id="a46d6-127">Ponnahdusikkunoiden yläpalkeissa on tietoja yrityksestä, jolle sivu on avattu. Tiedot ovat vain luku -muodossa.</span><span class="sxs-lookup"><span data-stu-id="a46d6-127">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="a46d6-128">Ponnahdusikkunat ovat riippuvaisia myös selainikkunasta.</span><span class="sxs-lookup"><span data-stu-id="a46d6-128">The pop-up windows also rely on the main browser window.</span></span> <span data-ttu-id="a46d6-129">Jos pääikkuna suljetaan tai päivitetään, kaikki avoimet ponnahdusikkunat siirtyvät vain luku -tilaan.</span><span class="sxs-lookup"><span data-stu-id="a46d6-129">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="a46d6-130">Tällöin voit yhä tarkastella ikkunoiden tietoja, mutta et voi käsitellä niitä.</span><span class="sxs-lookup"><span data-stu-id="a46d6-130">This means that you can still view the information in these windows, but you will not be able to interact with it.</span></span>
