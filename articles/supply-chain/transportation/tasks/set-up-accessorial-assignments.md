---
title: Määritä lisämääritykset
description: Tässä menettelyssä kerrotaan, miten lisämaksun määritys määritetään.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAccessorialAssignment
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d7f48da374a0434130f2cf95bf77a126635cd63
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016905"
---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="3b69d-103">Määritä lisämääritykset</span><span class="sxs-lookup"><span data-stu-id="3b69d-103">Set up accessorial assignments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3b69d-104">Tässä menettelyssä kerrotaan, miten lisämaksun määritys määritetään.</span><span class="sxs-lookup"><span data-stu-id="3b69d-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="3b69d-105">Kuljetuskoordinaattori tekee tämän yleensä.</span><span class="sxs-lookup"><span data-stu-id="3b69d-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="3b69d-106">Määritä keskuksen lisämaksut ja lisämaksun päätiedot -ohjaus on suoritettava ennen tämän ohjauksen suorittamista</span><span class="sxs-lookup"><span data-stu-id="3b69d-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="3b69d-107">Lisämaksun määrityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3b69d-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="3b69d-108">Valitse Kuljetustenhallinta > Asetukset > Luokitus > Lisämaksun määritykset.</span><span class="sxs-lookup"><span data-stu-id="3b69d-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="3b69d-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3b69d-109">Click New.</span></span>
3. <span data-ttu-id="3b69d-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3b69d-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="3b69d-111">Ota käyttöön Tiedot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="3b69d-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="3b69d-112">Avaa haku valitsemalla Keskus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="3b69d-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3b69d-113">Valitse luettelosta keskus, joka luotiin lisämaksun tiedoissa Määritä keskuksen lisämaksut ja lisämaksun päätiedot -ohjauksen suorittamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="3b69d-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="3b69d-114">Avaa haku valitsemalla Keskuksen lisämaksun tunnus -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="3b69d-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="3b69d-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3b69d-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3b69d-116">Ota käyttöön Ehdot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="3b69d-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="3b69d-117">Ehdot-osassa voit valita tarkat ehdot kulun kohdistamiselle tässä tarjottujen erilaisten arvojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="3b69d-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="3b69d-118">Määritä Käytä aina -vaihtoehdon arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="3b69d-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="3b69d-119">Valitse asetus Lisämäärityksen taso -kentässä.</span><span class="sxs-lookup"><span data-stu-id="3b69d-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="3b69d-120">Ota käyttöön Laskenta-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="3b69d-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="3b69d-121">Valitse Lisämaksun tyyppi -kentässä Kiinteä.</span><span class="sxs-lookup"><span data-stu-id="3b69d-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="3b69d-122">Lisämaksun tyyppi määrittää, miten toteutunut kulu lasketaan.</span><span class="sxs-lookup"><span data-stu-id="3b69d-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="3b69d-123">Tässä esimerkissä kulu on kiinteä.</span><span class="sxs-lookup"><span data-stu-id="3b69d-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="3b69d-124">Syötä Lisämaksu-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="3b69d-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="3b69d-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3b69d-125">Click Save.</span></span>

