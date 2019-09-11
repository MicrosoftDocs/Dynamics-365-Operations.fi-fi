---
title: Määritä ensisijaiset ylläpitotyöntekijät
description: Tässä ohjeaiheessa kerrotaan, kuinka ensisijaiset ylläpitopitotyöntekijät määritetään resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887408"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="438c7-103">Ensisijaiset ylläpitotyöntekijät</span><span class="sxs-lookup"><span data-stu-id="438c7-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="438c7-104">Voit määrittää, mitkä kunnossapitotyöntekijät kohdistetaan ensisijaisesti työtilausten ajoituksessa.</span><span class="sxs-lookup"><span data-stu-id="438c7-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="438c7-105">Tämän toiminnon käyttäminen on valinnaista, mutta sen avulla voit tehdä valinnan pätevimman kunnossapitotyöntekijän kanssa työn suorittamiseksi työntekijöiden taitojen ja osaamisen perusteella.</span><span class="sxs-lookup"><span data-stu-id="438c7-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="438c7-106">Näin ollen **Ensisijaiset ylläpitotyöntekijät** -asetuksen avulla määritetään, onko työtilaukselle tarkoitus ajoittaa tietty kunnossapitotyöntekijä tai työntekijäryhmä työtilauksen ajoituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="438c7-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="438c7-107">Vain ajoitushetkellä käytettävissä olevat kunnossapitotyöntekijät ajoitetaan.</span><span class="sxs-lookup"><span data-stu-id="438c7-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="438c7-108">Jos ensisijaisen kunnossapitotyöntekijän asetus vastaa työtilausta ajoituksen aikana, mutta kunnossapitotyöntekijä kohdistetaan muihin töihin, työtilaus ajoitetaan toiselle, käytettävissä olevalle huoltotyöntekijälle.</span><span class="sxs-lookup"><span data-stu-id="438c7-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="438c7-109">Ennen kuin voit määrittää ensisijaisia kunnossapitotyöntekijöitä, sinun on ensin määritettävä ylläpitotyöntekijät ja kunnossapitotyöntekijäryhmät, joiden pitäisi olla valittavissa.</span><span class="sxs-lookup"><span data-stu-id="438c7-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="438c7-110">Lisätietoja työntekijöiden ja kunnossapitotyöntekijäryhmien määrittämisestä on kohdassa [huoltotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="438c7-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="438c7-111">Ensisijaisten ylläpitotyöntekijöiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="438c7-111">Set up preferred workers</span></span>

<span data-ttu-id="438c7-112">Ensisijainen kunnossapitotyöntekijä tai työntekijäryhmä voi liittyä tiettyyn</span><span class="sxs-lookup"><span data-stu-id="438c7-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="438c7-113">kauppa</span><span class="sxs-lookup"><span data-stu-id="438c7-113">trade</span></span>  
- <span data-ttu-id="438c7-114">ylläpitotyön tyypin muunnos</span><span class="sxs-lookup"><span data-stu-id="438c7-114">maintenance job type variant</span></span>  
- <span data-ttu-id="438c7-115">ylläpitotyön tyyppi</span><span class="sxs-lookup"><span data-stu-id="438c7-115">maintenance job type</span></span>  
- <span data-ttu-id="438c7-116">ylläpitotyön tyypin luokka</span><span class="sxs-lookup"><span data-stu-id="438c7-116">maintenance job type category</span></span>  
- <span data-ttu-id="438c7-117">käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="438c7-117">asset</span></span>  
- <span data-ttu-id="438c7-118">resurssin tyyppi</span><span class="sxs-lookup"><span data-stu-id="438c7-118">asset type</span></span>  

<span data-ttu-id="438c7-119">tai näiden valintojen yhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="438c7-119">or a combination of those selections.</span></span> <span data-ttu-id="438c7-120">Mitä enemmän valintoja teet samalle tietueelle, sitä tarkempia ovat määritykset.</span><span class="sxs-lookup"><span data-stu-id="438c7-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="438c7-121">Valitse **Resurssien hallinta** > **Asetukset** > **työntekijät** > **Ensisijaiset ylläpitotyöntekijät**.</span><span class="sxs-lookup"><span data-stu-id="438c7-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="438c7-122">Luo uusi tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="438c7-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="438c7-123">Aloita luomalla "oletusarvoisen" ylläpitotyöntekijän tai työntekijäyhmän asetukset, jolla ei ole valintoja edellä olevan luettelon kentissä.</span><span class="sxs-lookup"><span data-stu-id="438c7-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="438c7-124">Tämä tarkoittaa, että valitset vain haluamasi **Ensisijainen ylläpitotyöntekijäryhmä**- tai **Ensisijainen ylläpitotyöntekijä** -kentän.</span><span class="sxs-lookup"><span data-stu-id="438c7-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="438c7-125">Alla olevassa kuvassa on esimerkki ensimmäisestä tietueesta, jossa "Pyynnöt" valitaan ensisijaiseksi kunnossapitotyöntekijäryhmäksi.</span><span class="sxs-lookup"><span data-stu-id="438c7-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="438c7-126">Tätä oletusasetusta käytetään työtilauksen ajoituksen aikana, jos mikään muu, tarkemmin määritettävä yhdistelmä ei vastaa työtilauksen sisältöä työtilauksen ajoituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="438c7-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="438c7-127">Luo uusi tietue toistamalla vaihe 2.</span><span class="sxs-lookup"><span data-stu-id="438c7-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="438c7-128">Tee tarvittavat valinnat ensisijaisen työntekijän tai työntekijäryhmän tietojen yksityiskohtaisuuden tason mukaan.</span><span class="sxs-lookup"><span data-stu-id="438c7-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="438c7-129">*Esimerkki:* Alla olevassa kuvassa kuudennen tietueen kunnossapitotyöntekijä Shawn Richardson valitaan ensisijaiseksi työntekijäksi.</span><span class="sxs-lookup"><span data-stu-id="438c7-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="438c7-130">Hänet valitaan automaattisesti sellaisen työtilauksen ajoituksen yhteydessä, joka sisältää käyttöomaisuuden CH-BP1-03-02 ja ylläpitotyötyypin" Facility Assessment", jos hän on käytettävissä ajoitettuna ajankohtana.</span><span class="sxs-lookup"><span data-stu-id="438c7-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="438c7-131">Yleensä kun työtilauksen ajoituksessa valitaan ensisijainen kunnossapitotyöntekijä, käyttöomaisuuden hallinta käy läpi kaikki **Ensisijainen ylläpitotyöntekijä** -tietueet ja etsii mahdollisen vastaavuuden tarkistamalla aina tarkimman yhdistelmän ensin.</span><span class="sxs-lookup"><span data-stu-id="438c7-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="438c7-132">Jos vastinetta ei löydy, käytetään oletustietuetta, jonka valinta on joko **Ensisijainen ylläpitotyöntekijäryhmä** -kentässä tai **Ensisijainen ylläpitotyöntekijä** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="438c7-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![Kuva 1](media/02-work-order-scheduling.png)

<span data-ttu-id="438c7-134">Voit myös määrittää vastuulliset huoltotyöntekijät, jotka voidaan valita, kun kunnossapitopyyntö tai työtilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="438c7-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="438c7-135">Voit tarvittaessa muokata valintaa kohdassa **Kaikki työtilaukset** ja **Kaikki ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="438c7-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="438c7-136">Lisätietoja on kohdassa [Vastuulliset huoltotyöntekijät](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="438c7-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="438c7-137">Työtilausten ajoituksessa lasketaan eri pisteet, joiden perusteella määritetään, mitkä työn tekijät voivat suorittaa työtilaukseen liittyvät työt (nämä pisteet määritetään kohdassa **Resurssienhallinnan parametrit** > **Työtilausten ajoitus** -linkki).</span><span class="sxs-lookup"><span data-stu-id="438c7-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="438c7-138">Jos vähintään kaksi ensisijaista huoltotyöntekijää tai vastaavaa huolto työntekijä saavat samat pisteet työtilauksen ajoituksessa, toinen työntekijä valitaan satunnaisesti.</span><span class="sxs-lookup"><span data-stu-id="438c7-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="438c7-139">Muussa tapauksessa työtilauksen suorittaa aina työntekijä, jolla on korkein pistemäärä.</span><span class="sxs-lookup"><span data-stu-id="438c7-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

