---
title: Resurssin mittarit
description: Tässä ohjeaiheessa kerrotaan, kuinka resurssin mittarityypit luodaan resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: adadb1df7b41488fad496f937ecbc24e0761e42d
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889766"
---
# <a name="counters"></a><span data-ttu-id="2f24c-103">Laskurit</span><span class="sxs-lookup"><span data-stu-id="2f24c-103">Counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2f24c-104">Tässä ohjeaiheessa kerrotaan, kuinka resurssienhallinnassa luodaan laskurityyppejä.</span><span class="sxs-lookup"><span data-stu-id="2f24c-104">The topic explains how to create counter types in Asset Management.</span></span> <span data-ttu-id="2f24c-105">Laskurityyppejä käytetään resurssien laskurirekisteröintien tekemiseen esimerkiksi tuotantotuntien määrän tai resurssin tuottaman määrän osalta.</span><span class="sxs-lookup"><span data-stu-id="2f24c-105">Counter types are used to make counter registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="2f24c-106">Resurssityypit liittyvät laskurityyppeihin.</span><span class="sxs-lookup"><span data-stu-id="2f24c-106">Asset types are related to the counter types.</span></span> <span data-ttu-id="2f24c-107">Tämä tarkoittaa sitä, että laskuria voidaan käyttää resurssin vain, jos laskuri on määritetty resurssiin käytetylle resurssityypille.</span><span class="sxs-lookup"><span data-stu-id="2f24c-107">This means that a counter can only be used on an asset if the counter is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="2f24c-108">Ennen kuin voit tehdä laskurirekisteröintejä resursseille, luo ensin ne laskurityypit, joita haluat käyttää **Laskurit**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="2f24c-108">Before you can make counter registrations on assets, you first create the counter types you want to use in **Counters**.</span></span> <span data-ttu-id="2f24c-109">Seuraavaksi voit luoda laskurirekisteröintejä kohdassa **Laskurit**.</span><span class="sxs-lookup"><span data-stu-id="2f24c-109">Next, you can create counter registrations on assets in **Counters**.</span></span> 

<span data-ttu-id="2f24c-110">Laskureita voidaan käyttää ylläpitosuunnitelmissa.</span><span class="sxs-lookup"><span data-stu-id="2f24c-110">Counters can be used on maintenance plans.</span></span> <span data-ttu-id="2f24c-111">Huoltosuunnitelman rivin tyyppi voi olla esimerkiksi Laskuri, joka liittyy esim. tuotantotuntien määrään tai tuotettuun määrään.</span><span class="sxs-lookup"><span data-stu-id="2f24c-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="2f24c-112">Laskurirekisteröinti voidaan päivittää manuaalisesti tai automaattisesti tuotantotuntien tai tuotetun määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="2f24c-112">A counter registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="2f24c-113">Laskuri voidaan määrittää käyttämään yhtä kolmesta päivitysmenetelmästä (valitaan **Laskurit**-kohdan **Päivitys**-kentässä):</span><span class="sxs-lookup"><span data-stu-id="2f24c-113">A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="2f24c-114">Manuaalinen – Laskuriarvot on rekisteröitävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="2f24c-114">Manual - you must manually register counter values.</span></span>  
- <span data-ttu-id="2f24c-115">Tuotantotunnit – laskuri päivitetään automaattisesti tuotantotuntien määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="2f24c-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="2f24c-116">Tuotantomäärä – laskuri päivitetään automaattisesti tuotetun määrän perusteella.</span><span class="sxs-lookup"><span data-stu-id="2f24c-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="2f24c-117">Jos käytetään tuotettua määrää, *kaikki* rekisteröidyt nimikkeet sisällytetään laskurirekisteröintiin, sekä hyvä määrä että virhemäärä.</span><span class="sxs-lookup"><span data-stu-id="2f24c-117">If quantity produced is used, *all* registered items are included in the counter registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="2f24c-118">On aina mahdollista tehdä manuaalisia laskurirekisteröintejä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="2f24c-118">It is always possible to make manual counter registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="2f24c-119">Luo resurssilaskurien rekisteröintien laskurityypit</span><span class="sxs-lookup"><span data-stu-id="2f24c-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="2f24c-120">Valitse **Resurssien hallinta** > **Asetukset** > **Resurssityypit** > **Laskurit**.</span><span class="sxs-lookup"><span data-stu-id="2f24c-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="2f24c-121">Luo uusi laskurityyppi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2f24c-121">Select **New** to create a new counter type.</span></span>
3. <span data-ttu-id="2f24c-122">Lisää tunnus **Laskuri**-kenttään ja laskurin nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2f24c-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="2f24c-123">Valitse laskuriyksikkö **Yleiset**-pikavälilehden **Yksikkö**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="2f24c-123">On the **General** FastTab, select a counter unit in the **Unit** field.</span></span>
5. <span data-ttu-id="2f24c-124">Valitse **Päivitys**-kentässä laskurissa käytettävä päivitystapa.</span><span class="sxs-lookup"><span data-stu-id="2f24c-124">In the **Update** field, select the update method to be used for the counter.</span></span>
6. <span data-ttu-id="2f24c-125">Valitse **Peri laskurin arvot** vaihtopainikkeessa Kyllä, jos resurssirakenteen alatason resurssien tulisi periä automaattisesti pääresurssiin tehdyt laskurirekisteröinnit.</span><span class="sxs-lookup"><span data-stu-id="2f24c-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit counter registrations made on the parent asset.</span></span>
7. <span data-ttu-id="2f24c-126">Valitse **Yhteenlaskettu summa**-kentässä se summausmenetelmä, jota käytetään laskurissa tätä laskurityyppiä käyttäen.</span><span class="sxs-lookup"><span data-stu-id="2f24c-126">In the **Total aggregate** field, select the summation method to be used for a counter using this counter type.</span></span> <span data-ttu-id="2f24c-127">"Summa" on vakio valinta, jota käytetään kirjattujen arvojen jatkuvaan lisäämiseen kokonaisarvoon.</span><span class="sxs-lookup"><span data-stu-id="2f24c-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="2f24c-128">"Keskiarvo"-arvoa voidaan käyttää, jos laskuri on määritetty valvomaan esimerkiksi resurssin lämpötilaa, tärinää tai kulumista.</span><span class="sxs-lookup"><span data-stu-id="2f24c-128">"Average" can be used if a counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="2f24c-129">Aseta **Poikkeama yli** -kentässä ylempi taso prosentteina, jonka avulla tarkistetaan, jos manuaaliset laskurirekisteröinnit ovat odotetun alueen sisällä.</span><span class="sxs-lookup"><span data-stu-id="2f24c-129">In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="2f24c-130">Tarkistus perustuu olemassa olevien laskurirekisteröintien lineaariseen kasvuun.</span><span class="sxs-lookup"><span data-stu-id="2f24c-130">The validation is based on a linear increase in existing counter registrations.</span></span>
9. <span data-ttu-id="2f24c-131">Aseta **Poikkeama ali** -kentässä alempi taso prosentteina, jonka avulla tarkistetaan, jos manuaaliset laskurirekisteröinnit ovat odotetun alueen sisällä.</span><span class="sxs-lookup"><span data-stu-id="2f24c-131">In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="2f24c-132">Tarkistus perustuu olemassa olevien laskurirekisteröintien lineaariseen pienenemiseen.</span><span class="sxs-lookup"><span data-stu-id="2f24c-132">The validation is based on a linear decrease in existing counter registrations.</span></span>
10. <span data-ttu-id="2f24c-133">Valitse **Tyyppi**-kentässä sanomatyyppi (ilmoitus, varoitus, virhe), joka näytetään, jos määritetyn alueen ulkopuoliset poikkeamat toteutuvat, kun teet manuaalisia laskurirekisteröintejä.</span><span class="sxs-lookup"><span data-stu-id="2f24c-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.</span></span>
11. <span data-ttu-id="2f24c-134">Lisää **Resurssityypit**-pikavälilehdessä resurssityypit, joiden tulisi voida käyttää laskuria.</span><span class="sxs-lookup"><span data-stu-id="2f24c-134">On the **Asset types** FastTab, add the asset types that should be able to use the counter.</span></span>
12. <span data-ttu-id="2f24c-135">Lisää **Liittyvät resurssilaskurit** -pikavälilehdessä laskuri, jota haluat päivittää automaattisesti, kun tämä laskuri päivitetään.</span><span class="sxs-lookup"><span data-stu-id="2f24c-135">On the **Related asset counters** FastTab, add the counter that you want to be automatically updated when this counter is updated.</span></span>


>[!NOTE]
><span data-ttu-id="2f24c-136">Liittyvä laskuri päivitetään automaattisesti vain, jos liittyvällä laskurilla on resurssityyppi, johon se liittyy, laskurin määrityksissä.</span><span class="sxs-lookup"><span data-stu-id="2f24c-136">A related counter is automatically updated only if the related counter has the asset type, to which it is related, in the counter setup.</span></span> <span data-ttu-id="2f24c-137">Esimerkki: Voit määrittää laskurin Tuotantotunnit ja lisätä resurssityypin Kuorma-auton moottori.</span><span class="sxs-lookup"><span data-stu-id="2f24c-137">For example: You set up a counter for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="2f24c-138">Kun tämä laskuri päivitetään, liittyvään laskuriin "Öljy" päivitetään myös samat laskuriarvot.</span><span class="sxs-lookup"><span data-stu-id="2f24c-138">When that counter is updated, a related counter "Oil" is also updated with the same counter values.</span></span> <span data-ttu-id="2f24c-139">**Laskurit**-asetuksissa on Tunnit-määritys.</span><span class="sxs-lookup"><span data-stu-id="2f24c-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="2f24c-140">Myös laskurille "Öljy" resurssityyppi "Kuorma-auton moottori" pitää lisätä **Resurssityypit**-pikavälilehteen , jotta laskurisuhde voidaan varmistaa.</span><span class="sxs-lookup"><span data-stu-id="2f24c-140">Also, on the "Oil" counter, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the counter relation.</span></span> <span data-ttu-id="2f24c-141">Alla olevissa näyttökuvissa on esimerkki laskureiden Tunti ja Öljy määrityksistä.</span><span class="sxs-lookup"><span data-stu-id="2f24c-141">See the screenshots below for an example of the setup on the Hours and Oil counters.</span></span>

<span data-ttu-id="2f24c-142">Kun resurssityypit lisätään laskurityyppiin kohdassa **Laskurit**, kyseinen laskuri lisätään automaattisesti **Laskurit**-pikavälilehden resurssityyppeihin kohdassa [Resurssitypit](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="2f24c-142">When asset types are added to a counter type in **Counters**, that counter is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Kuva 1](media/071-setup-for-objects.png)

