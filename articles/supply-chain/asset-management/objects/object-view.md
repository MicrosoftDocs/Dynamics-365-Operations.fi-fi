---
title: Resurssinäkymä
description: Tässä aiheessa kuvataan resurssien hallinnan resurssinäkymää
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14dc2cd95a47931ae4941b87205f2104891af404
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208222"
---
# <a name="asset-view"></a><span data-ttu-id="b1180-103">Resurssinäkymä</span><span class="sxs-lookup"><span data-stu-id="b1180-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b1180-104">Tässä aiheessa kuvataan resurssien hallinnan resurssinäkymää</span><span class="sxs-lookup"><span data-stu-id="b1180-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="b1180-105">**Resurssinäkymä** -sivulla näkyvät aktiiviset resurssit ja toiminnalliset sijainnit puunäkymässä.</span><span class="sxs-lookup"><span data-stu-id="b1180-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="b1180-106">Tämän vuoksi voit helposti saada yhteenvedon resurssien suhteista toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="b1180-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="b1180-107">Lisäksi voit tarkastella yksityiskohtaisia tietoja toiminnallisista sijainneista, resursseista ja niihin liittyvistä tuoterakenteista.</span><span class="sxs-lookup"><span data-stu-id="b1180-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="b1180-108">Voit myös saada nopean yleiskatsauksen aktiivisiin ylläpitopyyntöihin ja työtilauksiin, jotka liittyvät resurssiin.</span><span class="sxs-lookup"><span data-stu-id="b1180-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="b1180-109">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Resurssinäkymä**.</span><span class="sxs-lookup"><span data-stu-id="b1180-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="b1180-110">Jos haluat muuttaa sivulla näkyviä näkymää, valitse uusi arvo **Näkymä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b1180-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b1180-111">Oletusnäkymä, joka näkyy avattaessa **resurssinäkymä** -sivu, määräytyy sen mukaan, mikä arvo on valittuna **Resurssien hallinnan parametrit** -sivun **resurssit**-välilehden **Näytä**-kentässä. (**Resurssienhallinta** \> **Asetukset** \> **Resurssien hallinnan parametrit**).</span><span class="sxs-lookup"><span data-stu-id="b1180-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="b1180-112">Pikavälilehti näyttää valitun näkymän tiedot sivun oikeassa reunassa.</span><span class="sxs-lookup"><span data-stu-id="b1180-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="b1180-113">Puunäkymän yläpuolella näkyvä navigointipolku näyttää nykyisen valinnan puunäkymässä.</span><span class="sxs-lookup"><span data-stu-id="b1180-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="b1180-114">Tämä navigointipolku käyttää seuraavaa muotoa:</span><span class="sxs-lookup"><span data-stu-id="b1180-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="b1180-115">Toiminnallisen siajinnin tunnus / Toiminnallisen siajinnin tunnus (jos on enemmän kuin yksi sijainti) \> Resurssien tunnus / Resurssien tunnus (jos on useampi kuin yksi resurssi) - nimikenumero.</span><span class="sxs-lookup"><span data-stu-id="b1180-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="b1180-116">Jos olet valinnut resurssin puunäkymässä, voit valita **aktiiviset pyynnöt** tai **aktiiviset työtilaukset**, jos haluat tarkastella resurssiin liittyviä ylläpito- tai työtilauksia.</span><span class="sxs-lookup"><span data-stu-id="b1180-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="b1180-117">Voit myös valita **avaa** \> **Toiminnallinen sijainti**, **Resurssit** tai **Resurssien tuoterakenne** avataksesi liittyvät näkymän.</span><span class="sxs-lookup"><span data-stu-id="b1180-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="b1180-118">**Resurssien toiminnalliset sijainnit** -vaihtoehto, jonka voit valita **Näytä**-kentässä, on käytettävissä myös missä tahansa resurssihaussa, jossa voit valita resurssin.</span><span class="sxs-lookup"><span data-stu-id="b1180-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="b1180-119">Puunäkymä näkyy **Resurssinäkymä**-välilehdessä, esimerkiksi silloin, kun [luot resurssin](../objects/create-an-object.md), luot ylläpitopyynnön tai luot työtilauksen.</span><span class="sxs-lookup"><span data-stu-id="b1180-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>
