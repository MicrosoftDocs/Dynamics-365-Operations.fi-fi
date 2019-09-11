---
title: Määritä käyttöomaisuusryhmät
description: Tässä aiheessa kerrotaan, miten uusi käyttöomaisuusryhmä luodaan.
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 246502f66c0cfcd4b4ed3c4b9f2ae616e71a1c50
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867532"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="5b6a6-103">Määritä käyttöomaisuusryhmät</span><span class="sxs-lookup"><span data-stu-id="5b6a6-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b6a6-104">Tässä aiheessa kerrotaan, miten uusi käyttöomaisuusryhmä luodaan.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="5b6a6-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="5b6a6-106">Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Asetukset > Käyttöomaisuusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="5b6a6-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-107">Select **New**.</span></span>
3. <span data-ttu-id="5b6a6-108">Kirjoita arvo **Käyttöomaisuusryhmä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="5b6a6-109">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="5b6a6-110">**Käyttöomaisuusryhmän** numerojärjestyskoodi ja käyttöomaisuuserien automaattinen numerointi korvaavat käyttöomaisuusparametrien asetukset.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="5b6a6-111">Voit muuttaa asetusta tässä, jos tämän käyttöomaisuusryhmän käyttöomaisuuserillä on eri numerointi kuin muilla ryhmillä.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="5b6a6-112">Valitse **Kirjat**.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-112">Select **Books**.</span></span>
6. <span data-ttu-id="5b6a6-113">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="5b6a6-114">Jos **Laske poisto** -kentän arvoksi on määritetty **Kyllä**, käyttöomaisuuskirja sisällytetään poistoehdotuksiin.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="5b6a6-115">Jos **Laske poisto** -kentän arvoksi on määritetty **Ei**, käyttöomaisuudelle ei tehdä automaattisesti poistoa.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="5b6a6-116">Määritä käyttöomaisuuserän käyttöikä vuosina.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="5b6a6-117">Ota huomioon, että **Poistokaudet**-kentän arvo lasketaan käyttöiän määrittämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="5b6a6-118">Valitse vaihtoehto **Poistomenetelmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="5b6a6-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-119">Close the page.</span></span>

