---
title: Resurssin mittarit
description: Tässä ohjeaiheessa kerrotaan, kuinka resurssin mittarityypit luodaan resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783245"
---
# <a name="asset-measures"></a><span data-ttu-id="1fd36-103">Resurssin mittarit</span><span class="sxs-lookup"><span data-stu-id="1fd36-103">Asset measures</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="1fd36-104">Tässä ohjeaiheessa kerrotaan, kuinka resurssin mittarityypit luodaan resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="1fd36-104">The topic explains how to create asset measure types in Asset Management.</span></span> <span data-ttu-id="1fd36-105">Resurssien mittatyyppejä käytetään resurssien mittausrekisteröintien tekemiseen esimerkiksi tuotantotuntien määrän tai resurssin tuottaman määrän osalta.</span><span class="sxs-lookup"><span data-stu-id="1fd36-105">Asset measure types are used to make measurement registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="1fd36-106">Resurssityypit liittyvät resurssien mitta tyyppeihin.</span><span class="sxs-lookup"><span data-stu-id="1fd36-106">Asset types are related to the asset measure types.</span></span> <span data-ttu-id="1fd36-107">Tämä tarkoittaa sitä, että resurssi mittaa voidaan käyttää vain, jos resurssin mitta on määritetty resurssiin käytetylle resurssityypille.</span><span class="sxs-lookup"><span data-stu-id="1fd36-107">This means that an asset measure can only be used on an asset if the asset measure is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="1fd36-108">Ennen kuin voit tehdä mittauksen rekisteröinnit resursseille, luo ensin ne resurssin mittatyypit, joita haluat käyttää **Laskurit**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="1fd36-108">Before you can make measurement registrations on assets, you first create the asset measure types you want to use in **Counters**.</span></span> <span data-ttu-id="1fd36-109">Seuraavaksi voit luoda resurssien mittausrekisteröinnit kohdassa **Resurssin mittarit**.</span><span class="sxs-lookup"><span data-stu-id="1fd36-109">Next, you can create measurement registrations on assets in **Asset measures**.</span></span> 

<span data-ttu-id="1fd36-110">Resurssin mittareita voidaan käyttää huoltosuunnitelmissa.</span><span class="sxs-lookup"><span data-stu-id="1fd36-110">Asset measures can be used on maintenance plans.</span></span> <span data-ttu-id="1fd36-111">Huoltosuunnitelman rivin tyyppi voi olla esimerkiksi Laskuri, joka liittyy esim. tuotantotuntien määrään tai tuotettuun määrään.</span><span class="sxs-lookup"><span data-stu-id="1fd36-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="1fd36-112">Resurssin mittarirekisteröinti voidaan päivittää manuaalisesti tai automaattisesti tuotantotuntien tai tuotetun määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="1fd36-112">An asset measurement registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="1fd36-113">Resurssin mittari voidaan määrittää käyttämään yhtä kolmesta päivitysmenetelmästä (valitaan**Laskurit**-kohdan **Päivitys**-kentässä):</span><span class="sxs-lookup"><span data-stu-id="1fd36-113">An asset measure can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="1fd36-114">Manuaalinen – Resurssin mittariarvot on rekisteröitävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="1fd36-114">Manual - you must manually register asset measurement values.</span></span>  
- <span data-ttu-id="1fd36-115">Tuotantotunnit – laskuri päivitetään automaattisesti tuotantotuntien määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="1fd36-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="1fd36-116">Tuotantomäärä – laskuri päivitetään automaattisesti tuotetun määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="1fd36-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="1fd36-117">Jos käytetään tuotettua määrää, *kaikki* rekisteröidyt nimikkeet sisällytetään mittausrekisteröintiin, sekä hyvä määrä että virhemäärä.</span><span class="sxs-lookup"><span data-stu-id="1fd36-117">If quantity produced is used, *all* registered items are included in the measurement registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="1fd36-118">On aina mahdollista tehdä manuaalisia resurssin mittarirekisteröintejä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="1fd36-118">It is always possible to make manual asset measurement registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="1fd36-119">Luo resurssilaskurien rekisteröintien laskurityypit</span><span class="sxs-lookup"><span data-stu-id="1fd36-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="1fd36-120">Valitse **Resurssien hallinta** > **Asetukset** > **Resurssityypit** > **Laskurit**.</span><span class="sxs-lookup"><span data-stu-id="1fd36-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="1fd36-121">Luo uusi resurssin mittarityyppi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="1fd36-121">Select **New** to create a new asset measure type.</span></span>
3. <span data-ttu-id="1fd36-122">Lisää tunnus **Laskuri**-kenttään ja laskurin nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1fd36-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="1fd36-123">Valitse mittayksikkö **Yleiset**-pikavälilehden **Yksikkö**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1fd36-123">On the **General** FastTab, select a measurement unit in the **Unit** field.</span></span>
5. <span data-ttu-id="1fd36-124">Valitse **Päivitys**-kentässä resurssin mittarissa käytettävä päivitystapa.</span><span class="sxs-lookup"><span data-stu-id="1fd36-124">In the **Update** field, select the update method to be used for the asset measure.</span></span>
6. <span data-ttu-id="1fd36-125">Valitse **Peri laskurin arvot** vaihtopainikkeessa Kyllä, jos resurssirakenteen alatason resurssien tulisi periä automaattisesti pääresurssiin tehdyt rekisteröinnit.</span><span class="sxs-lookup"><span data-stu-id="1fd36-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit asset measure registrations made on the parent asset.</span></span>
7. <span data-ttu-id="1fd36-126">Valitse **Yhteenlaskettu summa**-kentässä se summausmenetelmä, jota käytetään resurssin mitassa tätä resurssin mittatyyppiä käyttäen.</span><span class="sxs-lookup"><span data-stu-id="1fd36-126">In the **Total aggregate** field, select the summation method to be used for an asset measure using this asset measure type.</span></span> <span data-ttu-id="1fd36-127">"Summa" on vakio valinta, jota käytetään kirjattujen arvojen jatkuvaan lisäämiseen kokonaisarvoon.</span><span class="sxs-lookup"><span data-stu-id="1fd36-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="1fd36-128">"Keskiarvo"-arvoa voidaan käyttää, jos resurssin mitta on määritetty valvomaan esimerkiksi resurssin lämpötilaa, tärinää tai kulumista.</span><span class="sxs-lookup"><span data-stu-id="1fd36-128">"Average" can be used if an asset measure is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="1fd36-129">Aseta **Poikkeama yli** -kentässä ylempi taso prosentteina, jonka avulla tarkistetaan, jos manuaaliset resurssin rekisteröinnit ovat odotetun alueen sisällä.</span><span class="sxs-lookup"><span data-stu-id="1fd36-129">In the **Deviation over** field, insert the upper level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="1fd36-130">Tarkistus perustuu olemassa olevien resurssin rekisteröintien lineaariseen kasvuun.</span><span class="sxs-lookup"><span data-stu-id="1fd36-130">The validation is based on a linear increase in existing asset measure registrations.</span></span>
9. <span data-ttu-id="1fd36-131">Aseta **Poikkeama alle** -kentässä alempi taso prosentteina, jonka avulla tarkistetaan, jos manuaaliset resurssin rekisteröinnit ovat odotetun alueen sisällä.</span><span class="sxs-lookup"><span data-stu-id="1fd36-131">In the **Deviation under** field, insert the lower level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="1fd36-132">Tarkistus perustuu olemassa olevien resurssin rekisteröintien lineaariseen vähenemiseen.</span><span class="sxs-lookup"><span data-stu-id="1fd36-132">The validation is based on a linear decrease in existing asset measure registrations.</span></span>
10. <span data-ttu-id="1fd36-133">Valitse **Tyyppi**-kentässä sanomatyyppi (ilmoitus, varoitus, virhe), joka näytetään, jos määritetyn alueen ulkopuoliset poikkeamat toteutuvat, kun teet manuaalisia resurssin mittauksen rekisteröintejä.</span><span class="sxs-lookup"><span data-stu-id="1fd36-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual asset measure registrations.</span></span>
11. <span data-ttu-id="1fd36-134">Lisää **Resurssityypit**-pikavälilehdessä resurssityypit, joiden tulisi voida käyttää resurssin mittaria.</span><span class="sxs-lookup"><span data-stu-id="1fd36-134">On the **Asset types** FastTab, add the asset types that should be able to use the asset measure.</span></span>
12. <span data-ttu-id="1fd36-135">Lisää **Liittyvät resurssin mittarit** -pikavälilehdessä resurssin mitat, jotka haluat päivittää automaattisesti, kun tämä resurssin mitta päivitetään.</span><span class="sxs-lookup"><span data-stu-id="1fd36-135">On the **Related asset measures** FastTab, add the asset measures that you want to be automatically updated when this asset measure is updated.</span></span>


>[!NOTE]
><span data-ttu-id="1fd36-136">Liittyvä resurssin mittari päivitetään automaattisesti vain, jos liittyvällä resurssin mittarilla on resurssityyppi, johon se liittyy, resurssin mittauksen määrityksissä.</span><span class="sxs-lookup"><span data-stu-id="1fd36-136">A related asset measure is automatically updated only if the related asset measure has the asset type, to which it is related, in the asset measure setup.</span></span> <span data-ttu-id="1fd36-137">Esimerkki: Voit määrittää resurssin mittarin Tuotantotunnit ja lisätä resurssityypin Kuorma-auton moottori.</span><span class="sxs-lookup"><span data-stu-id="1fd36-137">For example: You set up an asset measure for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="1fd36-138">Kun tämä resurssin mittari päivitetään, liittyvään laskuriin "Öljy" päivitetään myös samat mittarin arvot.</span><span class="sxs-lookup"><span data-stu-id="1fd36-138">When that asset measure is updated, a related counter "Oil" is also updated with the same asset measure values.</span></span> <span data-ttu-id="1fd36-139">**Laskurit**-asetuksissa on Tunnit-määritys.</span><span class="sxs-lookup"><span data-stu-id="1fd36-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="1fd36-140">Myös resurssin mittarille "Öljy" resurssityyppi "Kuorma-auton moottori" pitää lisätä **Resurssityypit**-pikavälilehteen , jotta resurssin mittarin suhde voidaan varmistaa.</span><span class="sxs-lookup"><span data-stu-id="1fd36-140">Also, on the "Oil" asset measure, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the asset measure relation.</span></span> <span data-ttu-id="1fd36-141">Alla olevissa näyttökuvissa on esimerkki resurssin mittarien Tunti ja Öljy määrityksistä.</span><span class="sxs-lookup"><span data-stu-id="1fd36-141">See the screenshots below for an example of the setup on the Hours and Oil asset measures.</span></span>

<span data-ttu-id="1fd36-142">Kun resurssityyppit lisätään resurssin mittarityyppiin kohdassa **Laskurit**, kyseinen resurssin mittari lisätään automaattisesti **Laskurit**-pikavälilehden resurssityyppeihin kohdassa [Resurssitypit](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="1fd36-142">When asset types are added to an asset measure type in **Counters**, that asset measure is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Kuva 1](media/071-setup-for-objects.png)


