---
title: Luo vähittäismyynnin toimintoprofiili
description: Tässä ohjeaiheessa käsitellään vähittäismyynnin toimintoprofiilin luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9fb0fd63b11e55f2b153fc9c135f148a6e343057
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002840"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="47904-103">Luo vähittäismyynnin toimintoprofiili</span><span class="sxs-lookup"><span data-stu-id="47904-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="47904-104">Tässä ohjeaiheessa käsitellään vähittäismyynnin toimintoprofiilin luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="47904-104">This topic describes how to create a retail functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="47904-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="47904-105">Overview</span></span>

<span data-ttu-id="47904-106">Vähittäismyynnin toimintojen profiilissa on erilaisia online-kanavien asetuksia.</span><span class="sxs-lookup"><span data-stu-id="47904-106">The retail functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="47904-107">Kunkin vähittäismyyntikanavan on määritettävä vähittäismyyntitoimintoprofiili.</span><span class="sxs-lookup"><span data-stu-id="47904-107">Each retail channel must specify a retail functionality profile.</span></span>

## <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="47904-108">Luo vähittäismyynnin toimintoprofiili</span><span class="sxs-lookup"><span data-stu-id="47904-108">Create a retail functionality profile</span></span>

<span data-ttu-id="47904-109">Luo uusi vähittäismyynnin toimintoprofiili seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="47904-109">To create a retail functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="47904-110">Siirry siirtymisruudussa kohtaan **Moduulit \> Kanavan määritys \> Myyntipisteprofiilit \> Toimintoprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="47904-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="47904-111">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="47904-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="47904-112">**Kirjoita profiili** -kenttään profiilin tunnus ("FN006" alla olevaan esimerkkikuvaan).</span><span class="sxs-lookup"><span data-stu-id="47904-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="47904-113">Kirjoita **Kuvaus**-kenttään arvo (Adventure Works -profiili alla olevaan esimerkkikuvaan).</span><span class="sxs-lookup"><span data-stu-id="47904-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="47904-114">Valitse **Yleiset**-osassa maa **ISO**-kielelle.</span><span class="sxs-lookup"><span data-stu-id="47904-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="47904-115">Muokkaa **Yleiset**-osassa muita asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="47904-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="47904-116">Valitse **Yleiset**-osassa **Kuittiprofiilin tunnus** sähköpostin vastaanottajille.</span><span class="sxs-lookup"><span data-stu-id="47904-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="47904-117">Muokkaa **Toiminnot**-osassa asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="47904-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="47904-118">Muokkaa **Summa**-osassa asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="47904-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="47904-119">Muokkaa **Tietokoodit**-osassa asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="47904-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="47904-120">Muokkaa **Kuitin numerointi** -osassa muita asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="47904-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="47904-121">Seuraavassa kuvassa on esimerkki vähittäiskaupan toimintoprofiilista.</span><span class="sxs-lookup"><span data-stu-id="47904-121">The following image shows an example retail functionality profile.</span></span>
  
![Vähittäiskaupan toimintoprofiiliesimerkki](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="47904-123">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="47904-123">Additional resources</span></span>

[<span data-ttu-id="47904-124">Tietokoodit ja tietokoodiryhmät</span><span class="sxs-lookup"><span data-stu-id="47904-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="47904-125">Luo uusi osoitekirja</span><span class="sxs-lookup"><span data-stu-id="47904-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="47904-126">Näytön asettelun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="47904-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="47904-127">Retail Hardware Stationin määrittäminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="47904-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
