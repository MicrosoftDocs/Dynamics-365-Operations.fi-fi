---
title: Resurssien palvelutasot
description: Tässä ohjeaiheessa kerrotaan resurssien palvelutasoista resurssien hallinnassa.
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
ms.openlocfilehash: d1e2f8d2ac0c48d4f92b15ec345ffa650b71df0b
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571021"
---
# <a name="asset-service-levels"></a><span data-ttu-id="83b61-103">Resurssien palvelutasot</span><span class="sxs-lookup"><span data-stu-id="83b61-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="83b61-104">Tässä ohjeaiheessa kerrotaan resurssien palvelutasoista resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="83b61-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="83b61-105">Resurssien palvelutasot liittyvät varoihin, ja ne siirretään ylläpitopyyntöihin ja työtilauksiin.</span><span class="sxs-lookup"><span data-stu-id="83b61-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="83b61-106">Niitä käytetään työtilausten prioriteetin laskemiseen työtilausten ajoituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="83b61-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="83b61-107">Resurssien palvelutasoja voidaan muuttaa, jos muutoksia tarvitaan.</span><span class="sxs-lookup"><span data-stu-id="83b61-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="83b61-108">Lisätietoja asetuksista, jotka liittyvät työtilausten ajoituksen luokituspisteiden laskentaan, on kohdassa [Resurssien hallinnan parametrit.](../setup-for-objects/enterprise-asset-management-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="83b61-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="83b61-109">Vähintään yksi oletustietue on määritettävä resurssien palvelutasolle.</span><span class="sxs-lookup"><span data-stu-id="83b61-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="83b61-110">Tätä oletustietuetta käytetään, jos työtilauksen ajoituksen aikana ei löydy muuta vastaavuutta.</span><span class="sxs-lookup"><span data-stu-id="83b61-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="83b61-111">**Esimerkki 1:** oletuspalvelutaso, jota käytetään, jos muita vastaavuutta ei löydy.</span><span class="sxs-lookup"><span data-stu-id="83b61-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="83b61-112">Tässä tietueessa valitaan vain palvelutaso.</span><span class="sxs-lookup"><span data-stu-id="83b61-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="83b61-113">**Esimerkki 2:** korkea palvelutaso, jota käytetään töiden ajoittamiseen Volvo-rekan moottoreille.</span><span class="sxs-lookup"><span data-stu-id="83b61-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="83b61-114">Tässä tietueessa valitaan asiaankuuluva resurssityyppi (kuten **kuorma-auton moottori**), valmistaja (**Volvo**) ja palvelutaso.</span><span class="sxs-lookup"><span data-stu-id="83b61-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="83b61-115">Resurssien palvelutasojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="83b61-115">Set up asset service levels</span></span>

1. <span data-ttu-id="83b61-116">valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssien palvelutasot**.</span><span class="sxs-lookup"><span data-stu-id="83b61-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="83b61-117">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="83b61-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="83b61-118">Resurssien palveluasolle vaadittavien yksityiskohtien tasosta riippuen tee asiaankuuluvat valinnat kentissä **Toiminnallinen sijainti**, **Resurssin tyyppi**, **Valmistaja**, **Malli**, **Resurssi**, **Työtilauksen tyyppi** ja **Palvelutaso**.</span><span class="sxs-lookup"><span data-stu-id="83b61-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="83b61-119">Kun resurssien palvelutasoa käytetään kunnossapitopyyntöihin ja työtilauksiin, resurssien hallinta käy läpi kaikki resurssien palvelutasotietueet mahdollisen vastaavuuden tarkastamiseen.</span><span class="sxs-lookup"><span data-stu-id="83b61-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="83b61-120">Se tarkistaa aina kaikkein erikoisimman yhdistelmän ensin.</span><span class="sxs-lookup"><span data-stu-id="83b61-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="83b61-121">Toisin sanoen resurssien hallinta tarkistaa ensin **Työtilauksen tyyppi** -kentän vastaavuuden.</span><span class="sxs-lookup"><span data-stu-id="83b61-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="83b61-122">Jos vastaavuutta ei löydy, se tarkistaa **Resurssit** -kentän vastaavuuden ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="83b61-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="83b61-123">Kuten näet **resurssien palvelutasot** -sivun asettelussa, tämä tarkoittaa sitä, että jos haluat löytää erityisen yhdistelmän, resurssien hallinta tarkistaa kunkin tietueen oikealta vasemmalle, jotta se vastaa toisiaan.</span><span class="sxs-lookup"><span data-stu-id="83b61-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="83b61-124">Jos vastaavuutta ei löydy, käytetään oletustietuetta, jolla ei ole valintoja kyseisissä kentissä.</span><span class="sxs-lookup"><span data-stu-id="83b61-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="83b61-125">Valitse **Palvelutaso**-kentässä numero, joka ilmaisee palvelutason (prioriteetin).</span><span class="sxs-lookup"><span data-stu-id="83b61-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="83b61-126">Jos muutat resurssien palvelutasotietuetta **Resurssien palvelutasot** -sivulla sen jälkeen, kun olet jo käyttänyt sitä työtilauksessa, kunnossapitopyyntöjen ja työtilausten palvelutasoa ei päivitetä vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="83b61-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>
