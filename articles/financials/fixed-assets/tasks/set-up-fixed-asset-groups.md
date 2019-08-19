---
title: Määritä käyttöomaisuusryhmät
description: Tässä menettelyssä näytetään, miten uusi käyttöomaisuusryhmä luodaan.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: e8f52b73c07aad1047d6e6e7caf80daecc9c26e7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839782"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="8fa9a-103">Määritä käyttöomaisuusryhmät</span><span class="sxs-lookup"><span data-stu-id="8fa9a-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8fa9a-104">Tässä menettelyssä näytetään, miten uusi käyttöomaisuusryhmä luodaan.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="8fa9a-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="8fa9a-106">Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuusryhmät.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="8fa9a-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-107">Click New.</span></span>
3. <span data-ttu-id="8fa9a-108">Kirjoita arvo Käyttöomaisuusryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="8fa9a-109">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="8fa9a-110">Käyttöomaisuuserien automaattinen numerointi ja käyttöomaisuuserien automaattinen numerointi korvaavat käyttöomaisuusparametrien asetukset.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="8fa9a-111">Voit muuttaa asetusta tässä, jos tämän käyttöomaisuusryhmän käyttöomaisuuserillä on eri numerointi kuin muilla ryhmillä.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="8fa9a-112">Valitse Kirjat.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-112">Click Books.</span></span>
6. <span data-ttu-id="8fa9a-113">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="8fa9a-114">Jos Laske poisto -kentän arvoksi on määritetty Kyllä, käyttöomaisuuskirja sisällytetään poistoehdotuksiin.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="8fa9a-115">Jos Laske poisto -kentän arvoksi on määritetty Ei, käyttöomaisuudelle ei tehdä automaattisesti poistoa.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="8fa9a-116">Määritä käyttöomaisuuserän käyttöikä vuosina.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="8fa9a-117">Ota huomioon, että Poistokaudet-kentän arvo lasketaan käyttöiän määrittämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="8fa9a-118">Valitse vaihtoehto Poistomenetelmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="8fa9a-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8fa9a-119">Close the page.</span></span>

