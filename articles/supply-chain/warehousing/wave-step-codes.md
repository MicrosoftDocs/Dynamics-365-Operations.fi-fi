---
title: Aallon vaihekoodit
description: Tässä ohjeaiheessa on yleiskuvaus aallon vaihekoodeista ja niiden käytöstä.
author: josaw1
manager: tfehr
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 08b40c076e288592f6a4cd628b9acd8a2eaedb7e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998400"
---
# <a name="wave-step-codes"></a><span data-ttu-id="4b8c8-103">Aallon vaihekoodit</span><span class="sxs-lookup"><span data-stu-id="4b8c8-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b8c8-104">Aallon vaihekoodit ovat koodeja, joita käyttäjät voivat määrittää ja käyttää aaltomenetelmien tiettyjen esiintymien linkittämiseksi vastaavaan malliin.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="4b8c8-105">Mallit sisältävät malleja täydennykselle, konttijärjestelmälle, etikettien tulostamiselle, kuormituksen luonnille ja lajittelulle.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="4b8c8-106">Kun aallon vaihekoodeja ei käytetä, käyttäjien on kirjoitettava vapaamuotoista tekstiä viitatakseen aaltomenetelmän esiintymän tiettyyn malliin.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="4b8c8-107">Vapaamuotoinen teksti on altis virheille, koska käyttäjien on varmistettava, että heidän aaltomalliin tiettyä aallon vaihemenetelmää varten syöttämänsä aallon vaiheen teksti vastaa kohdemallissa olevaa aallon vaiheen tekstiä tarkalleen.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="4b8c8-108">Tietyn aallon vaihetyypin aallon vaihekoodit määritetään erillisellä sivulla.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="4b8c8-109">Aallon vaihekoodi on valittava avattavasta luettelosta jokaiselle aaltomallin aallon vaiheen menetelmän esiintymälle, joka edellyttää aallon vaihekoodia.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="4b8c8-110">Avattavasta luettelosta tehty valinta korvaa syötetyn vapaamuotoisen tekstin ja auttaa vähentämään inhimillisten virheiden riskiä ja vaikutusta.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="4b8c8-111">Asetuskoodeja käytetään aaltomallissa oleva aallon vaiheen menetelmän linkittämiseksi menetelmän kohdemalliin.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="4b8c8-112">Aallon vaihekoodien käyttö on valinnaista.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="4b8c8-113">Se on käytössä koko organisaation laajuisesti kaikille yrityksille.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="4b8c8-114">Asennuksen esittely</span><span class="sxs-lookup"><span data-stu-id="4b8c8-114">Setup demo</span></span> 

<span data-ttu-id="4b8c8-115">Esittelytietojen on oltava asennettuna tätä esittelyä varten, ja sinun on käytettävä esittelytietojen **USMF**-yritystä.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="4b8c8-116">Ota käyttöön aallon vaihekoodit</span><span class="sxs-lookup"><span data-stu-id="4b8c8-116">Enable wave step codes</span></span>

<span data-ttu-id="4b8c8-117">Noudata seuraavia ohjeita ottaaksesi aallon vaihekoodien ominaisuuden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="4b8c8-118">Mene **Toimintojen hallintaan**.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="4b8c8-119">Valitsemalla tämän voit ottaa käyttöön **Organisaation laajuisen Wave Step-koodin**.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="4b8c8-120">Kaikki olemassa olevat aallon vaiheiden vapaamuotoiset tekstit päivitetään uuteen rakenteeseen kaikissa yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="4b8c8-121">Kun tämä päivitys on valmis kaikille yrityksille, ominaisuus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="4b8c8-122">Jos toimintoa ei voi ottaa käyttöön yhdelle tai useammalle yritykselle, ominaisuus ei ole käytössä millekään yritykselle.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="4b8c8-123">Käyttöönoton aikana validoinnit tehdään tietojen päivityksen aikana.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="4b8c8-124">Jos päivitys epäonnistuu, näyttöön tulee virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="4b8c8-125">Päivitys saattaa epäonnistua seuraavien ristiriitojen takia:</span><span class="sxs-lookup"><span data-stu-id="4b8c8-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="4b8c8-126">Sinulla on identtisiä aallon vaiheiden vapaamuotoisia tekstejä.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="4b8c8-127">Sinulla on mukautuksia.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-127">Customizations exist.</span></span>
- <span data-ttu-id="4b8c8-128">Aallon vaiheen menetelmän esiintymään on liitetty aallon vaiheen vapaamuotoinen teksti, joka ei vastaa odotettua mallityyppiä.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="4b8c8-129">Kun olet ratkaissut vahvistusten aikana havaitut ristiriidat, voit yrittää ottaa ominaisuuden uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="4b8c8-130">Kun ominaisuus on otettu onnistuneesti käyttöön, **Aallon vaihekoodit** -sivu (**Varastonhallinta \> Asetukset \> Aallot \> Aallon vaihekoodit**) tulee saataville.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-130">When the feature has been enabled, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="4b8c8-131">Tällä sivulla on luettelo aallon vaihekoodeista, jotka päivitettiin, kun organisaationlaajuinen aallon vaihekoodi -ominaisuus otettiin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="4b8c8-132">Uusien aallon vaihekoodien luominen</span><span class="sxs-lookup"><span data-stu-id="4b8c8-132">Create new wave step codes</span></span>

<span data-ttu-id="4b8c8-133">Voit käyttää **Aallon vaihekoodit** -sivua luodaksesi ja poistaaksesi aallon vaihekoodeja.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="4b8c8-134">Jokaisen uuden aallon vaihekoodin ja siihen liittyvän tunnuksen on oltava yksilöllisiä kaikkien aallon vaihetyyppien keskuudessa, ja ne on määritettävä tietylle aallon vaihetyypille.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="4b8c8-135">Aallon vaihekoodien soveltaminen</span><span class="sxs-lookup"><span data-stu-id="4b8c8-135">Apply wave step codes</span></span>

<span data-ttu-id="4b8c8-136">Kun olet määrittänyt sopivat aallon vaihekoodit, niitä voidaan soveltaa aallon käsittelymenetelmille.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="4b8c8-137">Siirry asiaankuuluvaan kohdemalliin soveltaaksesi aallon vaihekoodeja.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="4b8c8-138">Alla on kohdemallit, joihin aallon vaihekoodit on määritetty osoittamaan:</span><span class="sxs-lookup"><span data-stu-id="4b8c8-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="4b8c8-139">**Täydennysmallit:** Varastonhallinta \> Asetukset \> Täydennys \> Täydennysmallit</span><span class="sxs-lookup"><span data-stu-id="4b8c8-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="4b8c8-140">**Kuormituksen luonnin mallipohjat:** Varastonhallinta \> Asetukset \> Kuormitus \> Kuormituksen luonnin mallipohjat</span><span class="sxs-lookup"><span data-stu-id="4b8c8-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="4b8c8-141">**Lajittelumallit:** Varastonhallinta \> Asetukset \> Pakkaus \> Lähtevät lajittelumallit</span><span class="sxs-lookup"><span data-stu-id="4b8c8-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="4b8c8-142">**Konttijärjestelmän mallit:** Varastonhallinta \> Asetukset \> Kontit \> Kontin rakennusmallit</span><span class="sxs-lookup"><span data-stu-id="4b8c8-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="4b8c8-143">**Etikettien tulostusmallit:** Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etikettimallit</span><span class="sxs-lookup"><span data-stu-id="4b8c8-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="4b8c8-144">Tässä luettelossa olevia malleja käytetään, kun niihin viitataan aaltomallissa valitusta aallon käsittelymenetelmästä.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="4b8c8-145">Kun aaltomallissa olevan aallon käsittelymenetelmän aallon vaihekoodi vastaa jossakin mallityypissä olevaa aallon vaihekoodia, mallia käytetään.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="4b8c8-146">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="4b8c8-146">Sample scenario</span></span>

<span data-ttu-id="4b8c8-147">Seuraava toimenpide auttaa varmistamaan, että luomasi täydennysmalli otetaan käyttöön aaltomallille.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="4b8c8-148">Siirry kohtaan **Varastonhallinta \> Asetukset \> Aallot \> Aallon vaihekoodit** ja luo aiheen vaihekoodi **Täydennys**-tyypille.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="4b8c8-149">Siirry kohtaan **Varastonhallinta \> Asetukset \> Täydennys \> Täydennysmallit** ja luo täydennysmalli.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="4b8c8-150">Valitse täydennysmallista aallon vaihekoodi, jonka loit **Täydennys**-tyypille.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="4b8c8-151">Siirry kohtaan **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit** ja valitse aaltomalli, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="4b8c8-152">Valitse mallin **Menetelmät**-pikavälilehdestä **Täydennys**-menetelmä.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="4b8c8-153">Valitse **Aallon vaihekoodi** -kentästä aallon vaihekoodi, jonka valitsit täydennysmallille.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="4b8c8-154">Nämä vaiheet suoritetaan kullekin yritykselle.</span><span class="sxs-lookup"><span data-stu-id="4b8c8-154">You perform these steps for each legal entity.</span></span>
