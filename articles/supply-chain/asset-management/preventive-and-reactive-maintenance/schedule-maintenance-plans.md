---
title: Ajoita ylläpitosuunnitelmat
description: Tässä ohjeaiheessa kerrotaan ylläpitosuunnitelmien ajoittamisesta resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b6e5bde83474fe8971e482af518f7cee23a2220
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875626"
---
# <a name="schedule-maintenance-plans"></a><span data-ttu-id="5ad82-103">Ajoita ylläpitosuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="5ad82-103">Schedule maintenance plans</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="5ad82-104">Ennaltaehkäisevän kunnossapidon ajoituksessa luodaan käyttöomaisuuksien kalenterimerkinnät käyttöomaisuudelle määritettyjen ylläpitosuunnitelmien perusteella.</span><span class="sxs-lookup"><span data-stu-id="5ad82-104">Preventive maintenance scheduling generates calendar entries on assets, based on the maintenance plans set up on the assets.</span></span> <span data-ttu-id="5ad82-105">Voit ajoittaa kalenterimerkintöjä valittujen ylläpitosuunnitelmien, käyttöomaisuustyyppien ja resurssien mukaan.</span><span class="sxs-lookup"><span data-stu-id="5ad82-105">You can schedule calendar entries based on selected maintenance plans, asset types, and assets.</span></span>

1. <span data-ttu-id="5ad82-106">Valitse **Resurssien hallinta** > **Kausittainen** > **Ennalta ehkäisevä ylläpito** > **Ajoita ylläpitosuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="5ad82-106">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance plans**.</span></span>

2. <span data-ttu-id="5ad82-107">Voit valita aikavälin **Jakso**- ja **Jakson frekvenssi** -kentistä.</span><span class="sxs-lookup"><span data-stu-id="5ad82-107">You can select a time interval in the **Period** and **Period frequency** fields.</span></span>

>[!NOTE]
><span data-ttu-id="5ad82-108">**Jakso**- ja **Jakson frekvenssi** -kentät ilmaisevat, kuinka kauas eteenpäin haluat, että huoltoaikataulu rivit luodaan luomiesi ylläpitosuunnitelmien (aikapohjainen tai laskuripohjainen) perusteella.</span><span class="sxs-lookup"><span data-stu-id="5ad82-108">The **Period** and **Period frequencey** fields indicate how far ahead in time you want maintenance schedule lines to be created, based on the maintenance plans you have created (time-based or counter-based).</span></span> <span data-ttu-id="5ad82-109">Alla olevassa kuvassa ylläpitoaikataulurivit (= työtilausehdotukset) luodaan nykyisestä päivästä kolme kuukautta eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="5ad82-109">In the figure below, maintenance schedule lines (= work order proposals) are created from the current date and three months onwards.</span></span>

3. <span data-ttu-id="5ad82-110">Valitse "kyllä" **Luo automaattisesti, jos on määritetty rivillä** -vaihtopainikkeessa, jos työtilaukset luodaan automaattisesti huoltosuunnitelmarivin mukaan.</span><span class="sxs-lookup"><span data-stu-id="5ad82-110">Select "Yes" on the **Auto create if specified in the line** toggle button if work orders should automatically be created according to the maintenance plan line.</span></span>

>[!NOTE]
><span data-ttu-id="5ad82-111">Jos tämän vaihtopainikkeen arvoksi on määritetty "kyllä" *ja* **Luo automaattisesti** -valintaruutu on valittuna **Ylläpitosuunnitelmat** -kohdan ylläpitoriveillä, työtilaukset luodaan huoltosuunnitelmarivien perusteella ja myös ylläpitosuunnitelmarivit, joiden tila on "Työtilaus luotu", luodaan.</span><span class="sxs-lookup"><span data-stu-id="5ad82-111">If this toggle button is set to "Yes", *and* the **Auto create** check box is also selected on maintenance plan lines in **Maintenance plans**, work orders are created based on the maintenance plan lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="5ad82-112">Jos valittuna on vain yksi vaihtoehto (**Luo automaattisesti, jos määritetty rivillä** -vaihtopainike tai **Luo automaattisesti** -valintaruutu **Ylläpitosuunnitelmat** -lomakkeessa), vain huoltoaikataulurivit luodaan tilassa "Luotu".</span><span class="sxs-lookup"><span data-stu-id="5ad82-112">If only one option is selected (**Auto create if specified in the line** toggle button in this dialog or **Auto create** check box in **Maintenance plans** form), only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="5ad82-113">Tässä tapauksessa työtilauksia ei luoda.</span><span class="sxs-lookup"><span data-stu-id="5ad82-113">In that case, no work orders are created.</span></span>

4. <span data-ttu-id="5ad82-114">On mahdollista luoda kalenterimerkintöjä, jotka perustuvat ylläpitosuunnitelmiin (aika tai laskuri), käyttöomaisuuseriin, resurssityyppeihin, toiminnallisiin sijainteihin ja toiminnallisiin sijaintityyppeihin.</span><span class="sxs-lookup"><span data-stu-id="5ad82-114">It is possible to generate calendar entries based on maintenance plans (time or counter), assets, asset types, functional locations, and functional location types.</span></span> <span data-ttu-id="5ad82-115">Napsauta **Suodata**-painiketta ja tee valintasi tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="5ad82-115">Click the **Filter** button and make your selections, if required.</span></span>

- <span data-ttu-id="5ad82-116">Toiminnallisten sijaintien ylläpitosuunnitelmien ajoittamiseen liittyen: Jos päivität resurssin tyyppien, valmistajien ja mallien asetukset ylläpitosuunnitelmille **Kaikki toiminnalliset sijainnit** >  **Ylläpitosuunnitelmat** -pikavälilehdessä ja olet suunnitellut kunnossapitosuunnitelmat, aiemmin luodut kyseiseen toiminnalliseen sijaintiin liittyvät kunnossapitoaikataulun merkinnät poistetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="5ad82-116">Regarding scheduling of maintenance plans on functional locations: If you update the setup of asset types, manufacturers, and models on maintenance plans in **All functional locations** > **Maintenance plans** FastTab after you have scheduled maintenance plans, existing maintenance schedule entries related to that functional location are automatically deleted.</span></span> <span data-ttu-id="5ad82-117">Jotta voit luoda uusia kalenterimerkintöjä, jotka vastaavat toiminnallisen sijainnin päivitettyjä ylläpitosuunnitelman asetuksia, sinun on suoritettava kyseiselle toiminnalliselle sijainnille uusi ylläpitosuunnitelman aikataulu.</span><span class="sxs-lookup"><span data-stu-id="5ad82-117">In order to create new calendar entries, which correspond with the updated maintenance plan setup on the functional location, you must run a new maintenance plan schedule for that functional location.</span></span> <span data-ttu-id="5ad82-118">Lisätietoja käyttöomaisuuden tyyppien, valmistajien ja mallien määrittämisestä toiminnallisissa sijainneissa on kohdassa [Luo toiminnalliset sijainnit](../functional-locations/create-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="5ad82-118">Read more about the setup of asset types, manufacturers, and models on functional locations in [Create functional locations](../functional-locations/create-functional-locations.md).</span></span>

><span data-ttu-id="5ad82-119">*Esimerkki:* Haluat luoda huoltosuunnitelman tiettyä toiminnallista sijaintia varten, jolloin kaikki kyseiseen toimintapaikkaan määritetyt käyttökohteet sisällytetään valittuna aikana, kun ajoitat huoltosuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="5ad82-119">*Example:* You want to create a maintenance plan for a specific functional location, meaning all assets set up on that functional location at any given time will be included when you schedule the maintenance plan.</span></span> <span data-ttu-id="5ad82-120">Tässä tapauksessa luot huoltosuunnitelman ja valitset tietyn toimintosijainnin, mutta ET lisää huoltosuunnitelmaan mitään objekteja.</span><span class="sxs-lookup"><span data-stu-id="5ad82-120">In that case, you create a maintenance plan and select the specific functional location, but you do NOT add any objects in the maintenance plan.</span></span> <span data-ttu-id="5ad82-121">Tuloksena on, että kun ajoitat kyseisen ylläpitosuunnitelman, kunnossapitoaikataulurivit luodaan kaikille kyseiseen toimintapaikkaan liittyville resursseille.</span><span class="sxs-lookup"><span data-stu-id="5ad82-121">The result is that when you schedule that maintenance plan, maintenance schedule lines will be created for all the assets related to the functional location at that time.</span></span>

- <span data-ttu-id="5ad82-122">Jos teet muutoksia käyttöomaisuuden tyyppeihin, valmistajiin tai malleihin kohdassa **Resurssityypit**, muutokset vaikuttavat vain uusiin käyttöomaisuuseriin, jotka käyttävät päivitettyä käyttöomaisuuslajia.</span><span class="sxs-lookup"><span data-stu-id="5ad82-122">If you make changes to asset types, manufacturers and models in **Asset types**, those changes only affect new assets that use the updated asset type.</span></span> <span data-ttu-id="5ad82-123">Lue lisää käyttöomaisuustyyppien määrityksestä kohdassa [Resurssityypit](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="5ad82-123">Read more about asset type setup in [Asset types](../setup-for-objects/object-types.md).</span></span>  

5. <span data-ttu-id="5ad82-124">Aloita käyttöomaisuuksien ylläpitoaikataulumerkintöjen luominen valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ad82-124">Click **OK** to start the generation of maintenance schedule entries on assets.</span></span> <span data-ttu-id="5ad82-125">Luodut merkinnät näkyvät **Kaikki ylläpitoaikataulut** -luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="5ad82-125">The generated entries will be shown in the **All maintenance schedule** list page.</span></span>

![Kuva 1](media/09-preventive-maintenance.png)

- <span data-ttu-id="5ad82-127">**Ajoita ylläpitosuunnitelmat** -valintaikkunassa voit määrittää erätyöt **Suorita taustalla** -pikavälilehdessä, jolloin kalenterimerkinnät luodaan automaattisesti säännöllisin väliajoin.</span><span class="sxs-lookup"><span data-stu-id="5ad82-127">In the **Schedule maintenance plans** dialog, you can set up batch jobs on the **Run in the background** FastTab to automatically generate calendar entries at regular intervals.</span></span>  
- <span data-ttu-id="5ad82-128">Kun ajoitat ennaltaehkäisevän huollon, ylläpitoaikataulurivejä, joiden alkamispäivämäärä ja -aika ovat aikaisempia kuin järjestelmän päivämäärä ja kellonaika, ei luoda.</span><span class="sxs-lookup"><span data-stu-id="5ad82-128">When you schedule preventive maintenance, maintenance schedule lines with expected start date and time earlier than the system date and time will not be created.</span></span>  

<span data-ttu-id="5ad82-129">Alla olevassa kuvassa on graafinen esimerkki aikapohjaisesta ylläpitosuunnitelman laskennasta.</span><span class="sxs-lookup"><span data-stu-id="5ad82-129">The figure below provides a graphic illustration of a time-based maintenance plan calculation.</span></span>  

![Kuva 2](media/10-preventive-maintenance.jpg)

<span data-ttu-id="5ad82-131">Laskuripohjaisiin ylläpitosuunnitelmiin liittyen: Alla olevissa kuvissa näytetään kaksi eri laskurin rekisteröinnin jaksoa.</span><span class="sxs-lookup"><span data-stu-id="5ad82-131">Regarding counter-based maintenance plans: In the figures below, two different counter registration cycles are shown.</span></span> <span data-ttu-id="5ad82-132">Ne perustuvat ylläpitosuunnitelmaan, joka on määritetty käyttöomaisuuserälle "V0001", ja odottaa, että käyttöomaisuuserää (autoa) ajetaan noin 2 000 km joka kuukausi.</span><span class="sxs-lookup"><span data-stu-id="5ad82-132">They are based on a maintenance plan set up for asset "V0001", expecting the asset (a car) to run approx. 2,000 km every month.</span></span>

<span data-ttu-id="5ad82-133">Ensimmäisessä esimerkissä odotettua 2 000 km:ä ei saavuteta kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="5ad82-133">In the first example, the expected 2,000 km are not reached every month.</span></span> <span data-ttu-id="5ad82-134">Laskuripohjaisen ylläpitosuunnitelman mukaan kynnysarvo on 2 000 km, eli kun huoltosuunnitelman ajoitus suoritetaan, huoltoaikataulurivi luodaan aina, kun 2 000 kilometrin raja saavutetaan.</span><span class="sxs-lookup"><span data-stu-id="5ad82-134">According to the counter-based maintenance plan, the threshold is 2,000 km, meaning when you run a maintenance plan scheduling, a maintenance schedule line should be created each time the 2,000-kilometer threshold is reached.</span></span> <span data-ttu-id="5ad82-135">Esimerkissä 1 on neljä rekisteröitymisriviä, mutta 2 000 kilometrin raja saavutetaan vain kerran.</span><span class="sxs-lookup"><span data-stu-id="5ad82-135">In example 1, there are 4 registration lines, but the 2,000-kilometer threshold is only reached once.</span></span> <span data-ttu-id="5ad82-136">Tämä tarkoittaa sitä, että kun suoritat ylläpitosuunnitelmat tälle käyttöomaisuuserälle (esimerkiksi kolmen kuukauden jaksona) luodaan vain yksi huoltoaikataulurivi.</span><span class="sxs-lookup"><span data-stu-id="5ad82-136">This means that when you run schedule maintenance plans this asset, for example for a 3-month period, only one maintenance schedule line will be created.</span></span>

<span data-ttu-id="5ad82-137">Seuraavassa kuvassa 2 000 km tai enemmän kirjataan kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="5ad82-137">In the next figure, 2,000 km or more are registered every month.</span></span> <span data-ttu-id="5ad82-138">Tämän vuoksi luodaan kolme kunnossapitoriviä, jos tämän käyttöomaisuuserän huoltosuunnitelmat ajoitetaan kolmen kuukauden ajaksi.</span><span class="sxs-lookup"><span data-stu-id="5ad82-138">Therefore, three maintenance lines would be created if you schedule maintenance plans for this asset for a 3-month period.</span></span> 

<span data-ttu-id="5ad82-139">Tässä kuvatut esimerkit osoittavat, että kaikki käyttöomaisuuserään tehdyt laskurikirjaukset näyttävät trendin, joka kuvaa käyttöomaisuuserän kulumista.</span><span class="sxs-lookup"><span data-stu-id="5ad82-139">The examples described here show that all counter registrations made on an asset show a trend describing wear and tear on the asset.</span></span> <span data-ttu-id="5ad82-140">Tätä trendiä käytetään laskuperusteena ylläpitosuunnitelman ajoituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="5ad82-140">That trend is used as calculation basis at the time of maintenance plan scheduling.</span></span>

![Kuva 3](media/11-preventive-maintenance.png)

![Kuva 4](media/12-preventive-maintenance.png)
