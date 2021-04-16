---
title: Vähittäismyynnin toimintoprofiilin luominen
description: Tässä ohjeaiheessa käsitellään toimintoprofiilin luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b8d481597485775796290f61de19ef7682cb9f43
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791994"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="13454-103">Vähittäismyynnin toimintoprofiilin luominen</span><span class="sxs-lookup"><span data-stu-id="13454-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="13454-104">Tässä ohjeaiheessa käsitellään toimintoprofiilin luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="13454-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="13454-105">Commerce-toimintojen profiilissa on erilaisia online-kanavien asetuksia.</span><span class="sxs-lookup"><span data-stu-id="13454-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="13454-106">Kunkin kanavan on määritettävä toimintoprofiili.</span><span class="sxs-lookup"><span data-stu-id="13454-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="13454-107">Luo toimintoprofiili</span><span class="sxs-lookup"><span data-stu-id="13454-107">Create a functionality profile</span></span>

<span data-ttu-id="13454-108">Luo uusi toimintoprofiili seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="13454-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="13454-109">Siirry siirtymisruudussa kohtaan **Moduulit \> Kanavan määritys \> Myyntipisteprofiilit \> Toimintoprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="13454-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="13454-110">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="13454-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="13454-111">**Kirjoita profiili** -kenttään profiilin tunnus ("FN006" alla olevaan esimerkkikuvaan).</span><span class="sxs-lookup"><span data-stu-id="13454-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="13454-112">Kirjoita **Kuvaus**-kenttään arvo (Adventure Works -profiili alla olevaan esimerkkikuvaan).</span><span class="sxs-lookup"><span data-stu-id="13454-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="13454-113">Valitse **Yleiset**-osassa maa/alue **ISO**-kielelle.</span><span class="sxs-lookup"><span data-stu-id="13454-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="13454-114">Muokkaa **Yleiset**-osassa muita asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="13454-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="13454-115">Valitse **Yleiset**-osassa **Kuittiprofiilin tunnus** sähköpostin vastaanottajille.</span><span class="sxs-lookup"><span data-stu-id="13454-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="13454-116">Muokkaa **Toiminnot**-osassa asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="13454-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="13454-117">Muokkaa **Summa**-osassa asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="13454-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="13454-118">Muokkaa **Tietokoodit**-osassa asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="13454-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="13454-119">Muokkaa **Kuitin numerointi** -osassa muita asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="13454-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="13454-120">Seuraavassa kuvassa on esimerkki toimintoprofiilista.</span><span class="sxs-lookup"><span data-stu-id="13454-120">The following image shows an example functionality profile.</span></span>
  
![Toimintoprofiiliesimerkki](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="13454-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="13454-122">Additional resources</span></span>

[<span data-ttu-id="13454-123">Tietokoodit ja tietokoodiryhmät</span><span class="sxs-lookup"><span data-stu-id="13454-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="13454-124">Luo uusi osoitekirja</span><span class="sxs-lookup"><span data-stu-id="13454-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="13454-125">Näytön asettelun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="13454-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="13454-126">Retail Hardware Stationin määrittäminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="13454-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
