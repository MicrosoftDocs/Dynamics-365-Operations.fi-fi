---
title: Käyttöomaisuuden lisäyksen määrittäminen
description: Tässä menettelyssä kerrotaan, miten aiemmin määritettyyn käyttöomaisuuserään lisätään lisäys.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35e447ff9652861de4f7f310f68e8180a69589b4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209995"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="99ae6-103">Käyttöomaisuuden lisäyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="99ae6-103">Enter an addition to a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99ae6-104">Tässä menettelyssä kerrotaan, miten aiemmin määritettyyn käyttöomaisuuserään lisätään lisäys.</span><span class="sxs-lookup"><span data-stu-id="99ae6-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="99ae6-105">Käyttöomaisuuden lisäysten tarkoitus on seurata käyttöomaisuuserän nimikelisäyksiä, huoltoa tai parannuksia. Tämä kohta on tarkoitettu vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="99ae6-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="99ae6-106">Kaikki käyttöomaisuuden arvon tai käyttöiän muutokset on tehtävä erikseen.</span><span class="sxs-lookup"><span data-stu-id="99ae6-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   

<span data-ttu-id="99ae6-107">Menettelyssä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="99ae6-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="99ae6-108">Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Käyttöomaisuuserät > Käyttöomaisuuserät**.</span><span class="sxs-lookup"><span data-stu-id="99ae6-108">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="99ae6-109">Etsi ja valitse luettelosta käyttöomaisuus lisäystä varten.</span><span class="sxs-lookup"><span data-stu-id="99ae6-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="99ae6-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="99ae6-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="99ae6-111">Valitse toimintoruudussa **Käyttöomaisuus**.</span><span class="sxs-lookup"><span data-stu-id="99ae6-111">On the Action Pane, click **Fixed asset**.</span></span>
5. <span data-ttu-id="99ae6-112">Valitse **Käyttöomaisuuden lisäykset**.</span><span class="sxs-lookup"><span data-stu-id="99ae6-112">Click **Fixed asset additions**.</span></span>
6. <span data-ttu-id="99ae6-113">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="99ae6-113">Click **New**.</span></span>
7. <span data-ttu-id="99ae6-114">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="99ae6-114">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="99ae6-115">Määritä **Hankintapäivä**-kentässä oston tai palvelun lisäämisen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="99ae6-115">In the **Acquisition date** field, set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="99ae6-116">Syötä resurssin nimikkeen, huollon tai muun parannuksen kustannus **Yksikkökustannus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="99ae6-116">In the **Unit cost** field, enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="99ae6-117">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="99ae6-117">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="99ae6-118">Kokonaiskustannuksilla ei ole vaikutusta käyttöomaisuuserän arvoon. Se on tarkoitettu vain seuranta- ja tiedotustarkoitukseen.</span><span class="sxs-lookup"><span data-stu-id="99ae6-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="99ae6-119">Jos kustannukset aktivoidaan, kirjanpitoarvon korotustapahtuma on kirjattava erikseen.</span><span class="sxs-lookup"><span data-stu-id="99ae6-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="99ae6-120">Valitse **Yleiset**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="99ae6-120">Click the **General** tab.</span></span>

    * <span data-ttu-id="99ae6-121">Määritä **Pidentää käyttöikää** -kohdan arvoksi **Kyllä**, jos lisäys pidentää resurssin käyttöikää.</span><span class="sxs-lookup"><span data-stu-id="99ae6-121">Set **Increases service life** to **Yes** if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="99ae6-122">Tämä kenttä on vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="99ae6-122">This field is informational only.</span></span> <span data-ttu-id="99ae6-123">Voit lisätä käyttöikää muokkaamalla käyttöomaisuuserän arvomallien ja/tai poistokirjojen käyttöikää.</span><span class="sxs-lookup"><span data-stu-id="99ae6-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]