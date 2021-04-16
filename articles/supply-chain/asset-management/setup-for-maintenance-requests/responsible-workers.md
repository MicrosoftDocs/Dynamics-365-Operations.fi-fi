---
title: Vastuulliset ylläpitotyöntekijät
description: Tässä ohjeaiheessa kerrotaan, kuinka vastuulliset ylläpitopitotyöntekijät määritetään resurssien hallinnassa.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1330aa04a57809ff34dcca9791f8fb0a93c8d71
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808445"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="6172f-103">Vastuulliset ylläpitotyöntekijät</span><span class="sxs-lookup"><span data-stu-id="6172f-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6172f-104">Vastuulliset huoltotyöntekijät voivat liittyä resurssityyppeihin, resursseihin, toiminnallisiin sijainteihin, kunnossapitotöiden tyyppiluokkiin, kunnossapidon työtyyppeihin, kunnossapidon työn tyypin variantteihin ja toimialoihin.</span><span class="sxs-lookup"><span data-stu-id="6172f-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="6172f-105">Niitä voidaan käyttää työtilauksiin ja ylläpitopyyntöihin, jotka ilmaisevat ensisijaisuuden työtilauksesta vastuussa oleville huoltotyöntekijöille.</span><span class="sxs-lookup"><span data-stu-id="6172f-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="6172f-106">(Nämä kunnossapitotyöntekijät eivät kuitenkaan välttämättä ole samoja työntekijöitä, jotka on ajoitettu suorittamaan työtilauksen.) Tämän toiminnon käyttö on valinnaista.</span><span class="sxs-lookup"><span data-stu-id="6172f-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="6172f-107">Sen avulla voidaan esimerkiksi valita vastuulliset työntekijät tai työntekijäryhmät tietyille työtyypeille tai työalueille.</span><span class="sxs-lookup"><span data-stu-id="6172f-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="6172f-108">Työtilauksen elinkaaren tai huoltopyynnön elinkaaren aikana vastuullisia kunnossapitotyöntekijöitä voidaan muuttaa tai päivittää.</span><span class="sxs-lookup"><span data-stu-id="6172f-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="6172f-109">Tämä muutos tai päivitys voi liittyä esimerkiksi huoltopyynnön elinkaaren tilan muutokseen tai työtilauksen elinkaaren tilaan.</span><span class="sxs-lookup"><span data-stu-id="6172f-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="6172f-110">**Vastuulliset ylläpitotyöntekijät** -sivun asetuksia *ei* käytetä työtilauksen ajoituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="6172f-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="6172f-111">Resurssien hallinnassa voit myös määrittää *ensisijaiset* kunnossapitotyöntekijät, jotka voidaan kohdistaa työtilauksiin työtilauksen ajoituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="6172f-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="6172f-112">Ennen kuin voit määrittää vastuullisia kunnossapitotyöntekijöitä, sinun on määritettävä työntekijät ja kunnossapitotyöntekijäryhmät, joiden pitäisi olla valittavissa.</span><span class="sxs-lookup"><span data-stu-id="6172f-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="6172f-113">Lisätietoja työntekijöiden ja kunnossapitotyöntekijäryhmien määrittämisestä on kohdassa [huoltotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="6172f-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="6172f-114">Määritä vastuulliset ylläpitotyöntekijät</span><span class="sxs-lookup"><span data-stu-id="6172f-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="6172f-115">Valitse **Resurssien hallinta** \> **Asetukset** \> **Työntekijät** \> **Vastuulliset ylläpitotyöntekijät**.</span><span class="sxs-lookup"><span data-stu-id="6172f-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="6172f-116">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6172f-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="6172f-117">Luo ensin oletusarvoisen vastuullisen huoltotyöntekijän tai vastuullisen ylläpitotyöntekijäryhmän määritys, jossa määrität vain **Vastuullinen ylläpitotyöntekijäryhmä** -kentän ja/tai **Vastuullinen työntekijä** -kentän.</span><span class="sxs-lookup"><span data-stu-id="6172f-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="6172f-118">Jätä muut kentät tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="6172f-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="6172f-119">Tätä oletusasetusta käytetään työtilauksen ajoituksen aikana, jos mikään muu, tarkemmin määritettävä yhdistelmä ei vastaa työtilauksen sisältöä.</span><span class="sxs-lookup"><span data-stu-id="6172f-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6172f-120">Huoltopyynnön luomisen aikana, kun vastuullinen huoltotyöntekijä tai vastuullinen kunnossapitotyöntekijäryhmä on valittavissa **Kaikki ylläpitopyynnöt** -sivulla, resurssien hallinta käy läpi kaikki vastuulliset kunnossapitotyöntekijätietueet tarkistaen mahdollisen vastaavuuden.</span><span class="sxs-lookup"><span data-stu-id="6172f-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="6172f-121">Se tarkistaa aina kaikkein erikoisimman yhdistelmän ensin.</span><span class="sxs-lookup"><span data-stu-id="6172f-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="6172f-122">Toisin sanoen resurssien hallinta tarkistaa ensin **Kauppa**-kentän vastaavuuden.</span><span class="sxs-lookup"><span data-stu-id="6172f-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="6172f-123">Jos vastaavuutta ei löydy, se tarkistaa **Ylläpitotyön tyypin variantti** -kentän vastaavuuden.</span><span class="sxs-lookup"><span data-stu-id="6172f-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="6172f-124">Jos vastaavuutta ei löydy, se tarkistaa **Ylläpitotyön tyyppi** -kentän vastaavuuden ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="6172f-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="6172f-125">Kuten näet sivun asettelussa, tämä tarkoittaa, että löytääksesi täsmällisimman yhdistelmän, resurssien hallinta tarkistaa kunkin tietueen oikealta vasemmalle, jotta osuvuus (ensin **Kauppa**, sitten **Ylläpitotyön tyypin variantti**, sitten **Ylläpitotyön tyyppi**, sitten **Ylläpitotyön tyypin luokka**, sitten **Toiminnallinen sijainti**, sitten **Resurssi** ja lopuksi **Resurssin tyyppi**).</span><span class="sxs-lookup"><span data-stu-id="6172f-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="6172f-126">Jos vastaavuutta ei löydy, käytetään oletustietuetta, jolla ei ole valintoja kyseisissä seitsemässä kentässä.</span><span class="sxs-lookup"><span data-stu-id="6172f-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="6172f-127">Seuraavassa kuvassa on esimerkki **Vastuulliset ylläpitotyöntekijät** -sivusta.</span><span class="sxs-lookup"><span data-stu-id="6172f-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![Vastaavien ylläpitotyöntekijöiden sivu](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]