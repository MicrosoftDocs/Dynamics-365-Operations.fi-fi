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
ms.openlocfilehash: 6dad0cb480f69eac84df5ea9a67f2adb94e2f52c
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811800"
---
# <a name="asset-service-levels"></a><span data-ttu-id="5f7e9-103">Resurssien palvelutasot</span><span class="sxs-lookup"><span data-stu-id="5f7e9-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5f7e9-104">Tässä ohjeaiheessa kerrotaan resurssien palvelutasoista resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="5f7e9-105">Resurssien palvelutasot liittyvät varoihin, ja ne siirretään ylläpitopyyntöihin ja työtilauksiin.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="5f7e9-106">Niitä käytetään työtilausten prioriteetin laskemiseen työtilausten ajoituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="5f7e9-107">Resurssien palvelutasoja voidaan muuttaa, jos muutoksia tarvitaan.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="5f7e9-108">Lisätietoja asetuksista, jotka liittyvät työtilausten ajoituksen luokituspisteiden laskentaan, on kohdassa [Resurssien hallinnan parametrit.](../setup-for-objects/enterprise-asset-management-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="5f7e9-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="5f7e9-109">Vähintään yksi oletustietue on määritettävä resurssien palvelutasolle.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="5f7e9-110">Tätä oletustietuetta käytetään, jos työtilauksen ajoituksen aikana ei löydy muuta vastaavuutta.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="5f7e9-111">**Esimerkki 1:** oletuspalvelutaso, jota käytetään, jos muita vastaavuutta ei löydy.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="5f7e9-112">Tässä tietueessa valitaan vain palvelutaso.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="5f7e9-113">**Esimerkki 2:** korkea palvelutaso, jota käytetään töiden ajoittamiseen Volvo-rekan moottoreille.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="5f7e9-114">Tässä tietueessa valitaan asiaankuuluva resurssityyppi (kuten **kuorma-auton moottori**), valmistaja (**Volvo**) ja palvelutaso.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="5f7e9-115">Resurssien palvelutasojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5f7e9-115">Set up asset service levels</span></span>

1. <span data-ttu-id="5f7e9-116">valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssien palvelutasot**.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="5f7e9-117">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="5f7e9-118">Resurssien palveluasolle vaadittavien yksityiskohtien tasosta riippuen tee asiaankuuluvat valinnat kentissä **Toiminnallinen sijainti**, **Resurssin tyyppi**, **Valmistaja**, **Malli**, **Resurssi**, **Työtilauksen tyyppi** ja **Palvelutaso**.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5f7e9-119">Kun resurssien palvelutasoa käytetään kunnossapitopyyntöihin ja työtilauksiin, resurssien hallinta käy läpi kaikki resurssien palvelutasotietueet mahdollisen vastaavuuden tarkastamiseen.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="5f7e9-120">Se tarkistaa aina kaikkein erikoisimman yhdistelmän ensin.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="5f7e9-121">Toisin sanoen resurssien hallinta tarkistaa ensin **Työtilauksen tyyppi** -kentän vastaavuuden.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="5f7e9-122">Jos vastaavuutta ei löydy, se tarkistaa **Resurssit** -kentän vastaavuuden ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="5f7e9-123">Kuten näet **resurssien palvelutasot** -sivun asettelussa, tämä tarkoittaa sitä, että jos haluat löytää erityisen yhdistelmän, resurssien hallinta tarkistaa kunkin tietueen oikealta vasemmalle, jotta se vastaa toisiaan.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="5f7e9-124">Jos vastaavuutta ei löydy, käytetään oletustietuetta, jolla ei ole valintoja kyseisissä kentissä.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="5f7e9-125">Valitse **Palvelutaso**-kentässä numero, joka ilmaisee palvelutason (prioriteetin).</span><span class="sxs-lookup"><span data-stu-id="5f7e9-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="5f7e9-126">Jos muutat resurssien palvelutasotietuetta **Resurssien palvelutasot** -sivulla sen jälkeen, kun olet jo käyttänyt sitä työtilauksessa, kunnossapitopyyntöjen ja työtilausten palvelutasoa ei päivitetä vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>
