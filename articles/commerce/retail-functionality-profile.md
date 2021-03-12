---
title: Vähittäismyynnin toimintoprofiilin luominen
description: Tässä ohjeaiheessa käsitellään toimintoprofiilin luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a53fc77a7d457534428929bd431175be7cf450f7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979644"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="d4d4f-103">Vähittäismyynnin toimintoprofiilin luominen</span><span class="sxs-lookup"><span data-stu-id="d4d4f-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d4d4f-104">Tässä ohjeaiheessa käsitellään toimintoprofiilin luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d4d4f-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d4d4f-105">Overview</span></span>

<span data-ttu-id="d4d4f-106">Commerce-toimintojen profiilissa on erilaisia online-kanavien asetuksia.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-106">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="d4d4f-107">Kunkin kanavan on määritettävä toimintoprofiili.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-107">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="d4d4f-108">Luo toimintoprofiili</span><span class="sxs-lookup"><span data-stu-id="d4d4f-108">Create a functionality profile</span></span>

<span data-ttu-id="d4d4f-109">Luo uusi toimintoprofiili seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="d4d4f-109">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="d4d4f-110">Siirry siirtymisruudussa kohtaan **Moduulit \> Kanavan määritys \> Myyntipisteprofiilit \> Toimintoprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="d4d4f-111">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d4d4f-112">**Kirjoita profiili** -kenttään profiilin tunnus ("FN006" alla olevaan esimerkkikuvaan).</span><span class="sxs-lookup"><span data-stu-id="d4d4f-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="d4d4f-113">Kirjoita **Kuvaus**-kenttään arvo (Adventure Works -profiili alla olevaan esimerkkikuvaan).</span><span class="sxs-lookup"><span data-stu-id="d4d4f-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="d4d4f-114">Valitse **Yleiset**-osassa maa/alue **ISO**-kielelle.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="d4d4f-115">Muokkaa **Yleiset**-osassa muita asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="d4d4f-116">Valitse **Yleiset**-osassa **Kuittiprofiilin tunnus** sähköpostin vastaanottajille.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="d4d4f-117">Muokkaa **Toiminnot**-osassa asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="d4d4f-118">Muokkaa **Summa**-osassa asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="d4d4f-119">Muokkaa **Tietokoodit**-osassa asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="d4d4f-120">Muokkaa **Kuitin numerointi** -osassa muita asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="d4d4f-121">Seuraavassa kuvassa on esimerkki toimintoprofiilista.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-121">The following image shows an example functionality profile.</span></span>
  
![Toimintoprofiiliesimerkki](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="d4d4f-123">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d4d4f-123">Additional resources</span></span>

[<span data-ttu-id="d4d4f-124">Tietokoodit ja tietokoodiryhmät</span><span class="sxs-lookup"><span data-stu-id="d4d4f-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="d4d4f-125">Luo uusi osoitekirja</span><span class="sxs-lookup"><span data-stu-id="d4d4f-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="d4d4f-126">Näytön asettelun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d4d4f-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="d4d4f-127">Retail Hardware Stationin määrittäminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="d4d4f-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
