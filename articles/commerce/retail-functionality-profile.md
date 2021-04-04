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
ms.openlocfilehash: 14da5fd2b409790de2269036ccb941ffa6d3311c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478305"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="d2f41-103">Vähittäismyynnin toimintoprofiilin luominen</span><span class="sxs-lookup"><span data-stu-id="d2f41-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d2f41-104">Tässä ohjeaiheessa käsitellään toimintoprofiilin luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="d2f41-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d2f41-105">Commerce-toimintojen profiilissa on erilaisia online-kanavien asetuksia.</span><span class="sxs-lookup"><span data-stu-id="d2f41-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="d2f41-106">Kunkin kanavan on määritettävä toimintoprofiili.</span><span class="sxs-lookup"><span data-stu-id="d2f41-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="d2f41-107">Luo toimintoprofiili</span><span class="sxs-lookup"><span data-stu-id="d2f41-107">Create a functionality profile</span></span>

<span data-ttu-id="d2f41-108">Luo uusi toimintoprofiili seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="d2f41-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="d2f41-109">Siirry siirtymisruudussa kohtaan **Moduulit \> Kanavan määritys \> Myyntipisteprofiilit \> Toimintoprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="d2f41-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="d2f41-110">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d2f41-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d2f41-111">**Kirjoita profiili** -kenttään profiilin tunnus ("FN006" alla olevaan esimerkkikuvaan).</span><span class="sxs-lookup"><span data-stu-id="d2f41-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="d2f41-112">Kirjoita **Kuvaus**-kenttään arvo (Adventure Works -profiili alla olevaan esimerkkikuvaan).</span><span class="sxs-lookup"><span data-stu-id="d2f41-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="d2f41-113">Valitse **Yleiset**-osassa maa/alue **ISO**-kielelle.</span><span class="sxs-lookup"><span data-stu-id="d2f41-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="d2f41-114">Muokkaa **Yleiset**-osassa muita asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d2f41-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="d2f41-115">Valitse **Yleiset**-osassa **Kuittiprofiilin tunnus** sähköpostin vastaanottajille.</span><span class="sxs-lookup"><span data-stu-id="d2f41-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="d2f41-116">Muokkaa **Toiminnot**-osassa asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d2f41-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="d2f41-117">Muokkaa **Summa**-osassa asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d2f41-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="d2f41-118">Muokkaa **Tietokoodit**-osassa asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d2f41-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="d2f41-119">Muokkaa **Kuitin numerointi** -osassa muita asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d2f41-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="d2f41-120">Seuraavassa kuvassa on esimerkki toimintoprofiilista.</span><span class="sxs-lookup"><span data-stu-id="d2f41-120">The following image shows an example functionality profile.</span></span>
  
![Toimintoprofiiliesimerkki](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="d2f41-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d2f41-122">Additional resources</span></span>

[<span data-ttu-id="d2f41-123">Tietokoodit ja tietokoodiryhmät</span><span class="sxs-lookup"><span data-stu-id="d2f41-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="d2f41-124">Luo uusi osoitekirja</span><span class="sxs-lookup"><span data-stu-id="d2f41-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="d2f41-125">Näytön asettelun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d2f41-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="d2f41-126">Retail Hardware Stationin määrittäminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="d2f41-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
