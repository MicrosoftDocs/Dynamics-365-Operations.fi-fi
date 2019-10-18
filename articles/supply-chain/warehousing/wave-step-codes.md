---
title: Aallon vaihekoodit
description: Tässä ohjeaiheessa on yleiskuvaus aallon vaihekoodeista ja niiden käytöstä.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
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
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992354"
---
# <a name="wave-step-codes"></a><span data-ttu-id="58271-103">Aallon vaihekoodit</span><span class="sxs-lookup"><span data-stu-id="58271-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="58271-104">Tietoja aallon vaihekoodeista</span><span class="sxs-lookup"><span data-stu-id="58271-104">About wave step codes</span></span>

<span data-ttu-id="58271-105">Aallon vaihekoodit ovat koodeja, joita käyttäjät voivat määrittää ja käyttää aaltomenetelmien tiettyjen esiintymien linkittämiseksi vastaavaan malliin.</span><span class="sxs-lookup"><span data-stu-id="58271-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="58271-106">Mallit sisältävät malleja täydennykselle, konttijärjestelmälle, etikettien tulostamiselle, kuormituksen luonnille ja lajittelulle.</span><span class="sxs-lookup"><span data-stu-id="58271-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="58271-107">Kun aallon vaihekoodeja ei käytetä, käyttäjien on kirjoitettava vapaamuotoista tekstiä viitatakseen aaltomenetelmän esiintymän tiettyyn malliin.</span><span class="sxs-lookup"><span data-stu-id="58271-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="58271-108">Vapaamuotoinen teksti on altis virheille, koska käyttäjien on varmistettava, että heidän aaltomalliin tiettyä aallon vaihemenetelmää varten syöttämänsä aallon vaiheen teksti vastaa kohdemallissa olevaa aallon vaiheen tekstiä tarkalleen.</span><span class="sxs-lookup"><span data-stu-id="58271-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="58271-109">Tietyn aallon vaihetyypin aallon vaihekoodit määritetään erillisellä sivulla.</span><span class="sxs-lookup"><span data-stu-id="58271-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="58271-110">Aallon vaihekoodi on valittava avattavasta luettelosta jokaiselle aaltomallin aallon vaiheen menetelmän esiintymälle, joka edellyttää aallon vaihekoodia.</span><span class="sxs-lookup"><span data-stu-id="58271-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="58271-111">Avattavasta luettelosta tehty valinta korvaa syötetyn vapaamuotoisen tekstin ja auttaa vähentämään inhimillisten virheiden riskiä ja vaikutusta.</span><span class="sxs-lookup"><span data-stu-id="58271-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="58271-112">Asetuskoodeja käytetään aaltomallissa oleva aallon vaiheen menetelmän linkittämiseksi menetelmän kohdemalliin.</span><span class="sxs-lookup"><span data-stu-id="58271-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="58271-113">Aallon vaihekoodien ominaisuuden käyttäminen on valinnaista, ja käyttö tapahtuu yrityskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="58271-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="58271-114">Jos siis tietty yritys käyttää tätä ominaisuutta, kaikki kyseisen yrityksen olemassa olevat aallon vaihekoodit päivitetään uuteen rakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="58271-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="58271-115">Asennuksen esittely</span><span class="sxs-lookup"><span data-stu-id="58271-115">Setup demo</span></span> 

<span data-ttu-id="58271-116">Esittelytietojen on oltava asennettuna tätä esittelyä varten, ja sinun on käytettävä esittelytietojen **USMF**-yritystä.</span><span class="sxs-lookup"><span data-stu-id="58271-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="58271-117">Ota käyttöön aallon vaihekoodit</span><span class="sxs-lookup"><span data-stu-id="58271-117">Enable wave step codes</span></span>

<span data-ttu-id="58271-118">Noudata seuraavia ohjeita ottaaksesi aallon vaihekoodien ominaisuuden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="58271-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="58271-119">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="58271-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="58271-120">Määritä **Yleinen**-välilehden **Aallon käsittely** -pikavälilehdessä **Ota käyttöön aallon vaihekoodit** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="58271-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="58271-121">Kaikki olemassa olevat aallon vaiheiden vapaamuotoiset tekstit päivitetään uuteen rakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="58271-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="58271-122">Kun tämä päivitys on suoritettu yritykselle, **Ota käyttöön aallon vaihekoodit** -asetus ei ole enää käytettävissä **Varastonhallinnan parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="58271-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="58271-123">Vahvistukset tehdään päivityksen aikana, ja jos päivitys epäonnistuu, näet virhesanoman.</span><span class="sxs-lookup"><span data-stu-id="58271-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="58271-124">Päivitys saattaa epäonnistua seuraavien ristiriitojen takia:</span><span class="sxs-lookup"><span data-stu-id="58271-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="58271-125">Sinulla on identtisiä aallon vaiheiden vapaamuotoisia tekstejä.</span><span class="sxs-lookup"><span data-stu-id="58271-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="58271-126">Sinulla on mukautuksia.</span><span class="sxs-lookup"><span data-stu-id="58271-126">Customizations exist.</span></span>
- <span data-ttu-id="58271-127">Aallon vaiheen menetelmän esiintymään on liitetty aallon vaiheen vapaamuotoinen teksti, joka ei vastaa odotettua mallityyppiä.</span><span class="sxs-lookup"><span data-stu-id="58271-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="58271-128">Kun olet ratkaissut vahvistusten aikana havaitut ristiriidat, voit suorittaa päivitysprosessin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="58271-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="58271-129">Kun päivitys on suoritettu onnistuneesti, **Aallon vaihekoodit** -sivu (**Varastonhallinta \> Asetukset \> Aallot \> Aallon vaihekoodit**) tulee saataville.</span><span class="sxs-lookup"><span data-stu-id="58271-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="58271-130">Tällä sivulla on luettelo aallon vaihekoodeista, jotka päivitettiin, kun aallon vaiheenkoodien ominaisuus otettiin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="58271-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="58271-131">Uusien aallon vaihekoodien luominen</span><span class="sxs-lookup"><span data-stu-id="58271-131">Create new wave step codes</span></span>

<span data-ttu-id="58271-132">Voit käyttää **Aallon vaihekoodit** -sivua luodaksesi ja poistaaksesi aallon vaihekoodeja.</span><span class="sxs-lookup"><span data-stu-id="58271-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="58271-133">Jokaisen uuden aallon vaihekoodin ja siihen liittyvän tunnuksen on oltava yksilöllisiä kaikkien aallon vaihetyyppien keskuudessa, ja ne on määritettävä tietylle aallon vaihetyypille.</span><span class="sxs-lookup"><span data-stu-id="58271-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="58271-134">Aallon vaihekoodien soveltaminen</span><span class="sxs-lookup"><span data-stu-id="58271-134">Apply wave step codes</span></span>

<span data-ttu-id="58271-135">Kun olet määrittänyt sopivat aallon vaihekoodit, niitä voidaan soveltaa aallon käsittelymenetelmille.</span><span class="sxs-lookup"><span data-stu-id="58271-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="58271-136">Siirry asiaankuuluvaan kohdemalliin soveltaaksesi aallon vaihekoodeja.</span><span class="sxs-lookup"><span data-stu-id="58271-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="58271-137">Alla on kohdemallit, joihin aallon vaihekoodit on määritetty osoittamaan:</span><span class="sxs-lookup"><span data-stu-id="58271-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="58271-138">**Täydennysmallit:** Varastonhallinta \> Asetukset \> Täydennys \> Täydennysmallit</span><span class="sxs-lookup"><span data-stu-id="58271-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="58271-139">**Kuormituksen luonnin mallipohjat:** Varastonhallinta \> Asetukset \> Kuormitus \> Kuormituksen luonnin mallipohjat</span><span class="sxs-lookup"><span data-stu-id="58271-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="58271-140">**Lajittelumallit:** Varastonhallinta \> Asetukset \> Pakkaus \> Lähtevät lajittelumallit</span><span class="sxs-lookup"><span data-stu-id="58271-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="58271-141">**Konttijärjestelmän mallit:** Varastonhallinta \> Asetukset \> Kontit \> Kontin rakennusmallit</span><span class="sxs-lookup"><span data-stu-id="58271-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="58271-142">**Etikettien tulostusmallit:** Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etikettimallit</span><span class="sxs-lookup"><span data-stu-id="58271-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="58271-143">Tässä luettelossa olevia malleja käytetään, kun niihin viitataan aaltomallissa valitusta aallon käsittelymenetelmästä.</span><span class="sxs-lookup"><span data-stu-id="58271-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="58271-144">Kun aaltomallissa olevan aallon käsittelymenetelmän aallon vaihekoodi vastaa jossakin mallityypissä olevaa aallon vaihekoodia, mallia käytetään.</span><span class="sxs-lookup"><span data-stu-id="58271-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="58271-145">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="58271-145">Sample scenario</span></span>

<span data-ttu-id="58271-146">Seuraava toimenpide auttaa varmistamaan, että luomasi täydennysmalli otetaan käyttöön aaltomallille.</span><span class="sxs-lookup"><span data-stu-id="58271-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="58271-147">Siirry kohtaan **Varastonhallinta \> Asetukset \> Aallot \> Aallon vaihekoodit** ja luo aiheen vaihekoodi **Täydennys**-tyypille.</span><span class="sxs-lookup"><span data-stu-id="58271-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="58271-148">Siirry kohtaan **Varastonhallinta \> Asetukset \> Täydennys \> Täydennysmallit** ja luo täydennysmalli.</span><span class="sxs-lookup"><span data-stu-id="58271-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="58271-149">Valitse täydennysmallista aallon vaihekoodi, jonka loit **Täydennys**-tyypille.</span><span class="sxs-lookup"><span data-stu-id="58271-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="58271-150">Siirry kohtaan **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit** ja valitse aaltomalli, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="58271-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="58271-151">Valitse mallin **Menetelmät**-pikavälilehdestä **Täydennys**-menetelmä.</span><span class="sxs-lookup"><span data-stu-id="58271-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="58271-152">Valitse **Aallon vaihekoodi** -kentästä aallon vaihekoodi, jonka valitsit täydennysmallille.</span><span class="sxs-lookup"><span data-stu-id="58271-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>
