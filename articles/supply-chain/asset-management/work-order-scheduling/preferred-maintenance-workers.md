---
title: Määritä ensisijaiset ylläpitotyöntekijät
description: Tässä ohjeaiheessa kerrotaan, kuinka ensisijaiset ylläpitopitotyöntekijät määritetään resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 327cda12a05ad54b310e472a652f1c822ad97142
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215329"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="0ffa5-103">Määritä ensisijaiset ylläpitotyöntekijät</span><span class="sxs-lookup"><span data-stu-id="0ffa5-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0ffa5-104">Työtilausten ajoittamisen yhteydessä voit määrittää, mikä ylläpitotyöntekijä tai työntekijäryhmä kohdennetaan ensisijaisesti työtilauksen suorittamiselle.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="0ffa5-105">Tämän toiminnon käyttäminen on valinnaista, mutta sen avulla voit tehdä valinnan pätevimman kunnossapitotyöntekijän kanssa työn suorittamiseksi työntekijöiden taitojen ja osaamisen perusteella.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="0ffa5-106">Vain ajoitushetkellä käytettävissä olevat kunnossapitotyöntekijät ajoitetaan.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="0ffa5-107">Jos ensisijaisen ylläpitotyöntekijän asetus vastaa työtilausta ajoituksen aikana, mutta ylläpitotyöntekijä kohdistetaan muihin töihin, työtilaus ajoitetaan toiselle, käytettävissä olevalle ylläpitotyöntekijälle.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="0ffa5-108">Ennen kuin voit määrittää ensisijaisia ylläpitotyöntekijöitä, sinun on ensin määritettävä ylläpitotyöntekijöitä ja työntekijäryhmiä.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="0ffa5-109">Kuvaus ylläpitotyöntekijöiden ja työntekijäryhmien määrityksestä esitetään kohdassa [Ylläpitotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="0ffa5-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="0ffa5-110">Ensisijaisten ylläpitotyöntekijöiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0ffa5-110">Set up preferred workers</span></span>

<span data-ttu-id="0ffa5-111">Ensisijainen ylläpitotyöntekijä tai työntekijäryhmä voi liittyä yhteen tai useampaan seuraavista:</span><span class="sxs-lookup"><span data-stu-id="0ffa5-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="0ffa5-112">kauppa</span><span class="sxs-lookup"><span data-stu-id="0ffa5-112">trade</span></span>  
- <span data-ttu-id="0ffa5-113">ylläpitotyön tyypin muunnos</span><span class="sxs-lookup"><span data-stu-id="0ffa5-113">maintenance job type variant</span></span>  
- <span data-ttu-id="0ffa5-114">ylläpitotyön tyyppi</span><span class="sxs-lookup"><span data-stu-id="0ffa5-114">maintenance job type</span></span>  
- <span data-ttu-id="0ffa5-115">ylläpitotyön tyypin luokka</span><span class="sxs-lookup"><span data-stu-id="0ffa5-115">maintenance job type category</span></span>  
- <span data-ttu-id="0ffa5-116">käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="0ffa5-116">asset</span></span>  
- <span data-ttu-id="0ffa5-117">resurssin tyyppi</span><span class="sxs-lookup"><span data-stu-id="0ffa5-117">asset type</span></span>  

<span data-ttu-id="0ffa5-118">Mitä enemmän valintoja teet samalle tietueelle, sitä tarkempia ovat määritykset.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="0ffa5-119">Valitse **Resurssien hallinta** > **Asetukset** > **työntekijät** > **Ensisijaiset ylläpitotyöntekijät**.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="0ffa5-120">Luo uusi tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="0ffa5-121">Aloita luomalla "oletusarvoinen" ylläpitotyöntekijä tai työntekijäryhmä.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="0ffa5-122">Tämä tarkoittaa, että valitset vain haluamasi **Ensisijainen ylläpitotyöntekijäryhmä**- tai **Ensisijainen ylläpitotyöntekijä** -kentän.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="0ffa5-123">Alla olevassa näyttökuvassa on esimerkki ensimmäisestä tietueesta, jossa kentän **Ensisijainen ylläpitotyöntekijäryhmä** -kentän arvoksi valitaan "Pyynnöt".</span><span class="sxs-lookup"><span data-stu-id="0ffa5-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="0ffa5-124">Tätä oletusasetusta käytetään työtilauksen ajoituksen aikana, jos mikään muu, tarkemmin määritettävä yhdistelmä ei vastaa työtilauksen sisältöä.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="0ffa5-125">Luo uusi tietue toistamalla vaihe 2.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="0ffa5-126">Tee tarvittavat valinnat ensisijaisen työntekijän tai työntekijäryhmän tietojen yksityiskohtaisuuden tason mukaan.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="0ffa5-127">*Esimerkki:* Alla olevassa näyttökuvassa kuudennen tietueen ylläpitotyöntekijä Shawn Richardson valitaan ensisijaiseksi työntekijäksi.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="0ffa5-128">Hänet valitaan automaattisesti sellaisen työtilauksen ajoituksen yhteydessä, joka sisältää resurssin CH-BP1-03-02 ja ylläpitotyötyypin "Facility Assessment", jos hän on käytettävissä ajoitettuna ajankohtana.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="0ffa5-129">Yleensä kun työtilauksen ajoituksessa valitaan ensisijainen kunnossapitotyöntekijä, käyttöomaisuuden hallinta käy läpi kaikki **Ensisijainen ylläpitotyöntekijä** -tietueet ja etsii mahdollisen vastaavuuden tarkistamalla aina tarkimman yhdistelmän ensin.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="0ffa5-130">Jos vastinetta ei löydy, käytetään oletustietuetta, jonka valinta on joko **Ensisijainen ylläpitotyöntekijäryhmä** -kentässä tai **Ensisijainen ylläpitotyöntekijä** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![Kuva 1](media/02-work-order-scheduling.png)

<span data-ttu-id="0ffa5-132">Voit myös määrittää *Vastaavat ylläpitotyöntekijät*, jotka voidaan valita, kun ylläpitopyyntö tai työtilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="0ffa5-133">Voit tarvittaessa muokata valintaa kohdassa **Kaikki työtilaukset** ja **Kaikki ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="0ffa5-134">Lisätietoja on kohdassa [Vastaavat ylläpitotyöntekijät](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="0ffa5-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="0ffa5-135">Työtilausten ajoituksessa lasketaan eri pisteet, joiden perusteella määritetään, mitkä työn tekijät voivat suorittaa työtilaukseen liittyvät työt (nämä pisteet määritetään kohdassa **Resurssienhallinnan parametrit** > **Työtilausten ajoitus** -linkki).</span><span class="sxs-lookup"><span data-stu-id="0ffa5-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="0ffa5-136">Jos vähintään kaksi ensisijaista huoltotyöntekijää tai vastaavaa huolto työntekijä saavat samat pisteet työtilauksen ajoituksessa, toinen työntekijä valitaan satunnaisesti.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="0ffa5-137">Muussa tapauksessa työtilauksen suorittaa aina työntekijä, jolla on korkein pistemäärä.</span><span class="sxs-lookup"><span data-stu-id="0ffa5-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

