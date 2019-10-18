---
title: Työtilaukset ja käyttöomaisuuserät
description: Tässä ohjeaiheessa selitetään, miten työtilaukset ja käyttöomaisuuserät ajoitetaan käyttöomaisuuden hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250826"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="15b27-103">Työtilaukset ja käyttöomaisuuserät</span><span class="sxs-lookup"><span data-stu-id="15b27-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="15b27-104">Resurssien hallinnassa resurssit voivat liittyä käyttöomaisuuseriin, ja voit luoda työtilauksia kyseisille resursseille.</span><span class="sxs-lookup"><span data-stu-id="15b27-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="15b27-105">Jos käytät tätä toimintoa, voit saada kattavan yleiskuvan käyttöomaisuuksista, niihin liittyvistä investointiprojekteista sekä **Projektinhallinta ja kirjanpito** -moduulin ja **Käyttöomaisuuserät**-moduulin investointiprojekteihin rekisteröidyistä kustannuksista.</span><span class="sxs-lookup"><span data-stu-id="15b27-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module.</span></span>

>[!NOTE]
><span data-ttu-id="15b27-106">**Käyttöomaisuus erän numero** -kenttä täytetään työtilauksen työprojektissa vain, jos työtilauksen työprojektin projektityypiksi on valittu "investointi".</span><span class="sxs-lookup"><span data-stu-id="15b27-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![Kuva 1](media/24-work-orders.png)

<span data-ttu-id="15b27-108">Seuraavassa menettelyssä kuvataan resurssien, työtilausten, työtilausten työprojektien ja käyttöomaisuuserien välinen suhde.</span><span class="sxs-lookup"><span data-stu-id="15b27-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="15b27-109">Luot käyttöomaisuuserään liittyvän resurssin alla olevan kuvan osoittamalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="15b27-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![Kuva 2](media/25-work-orders.png)

2. <span data-ttu-id="15b27-111">Kun määrität työtilaustyypit (**Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Työtilaustyypit**), luot työtilaustyypin, jolla käsitellään investointeja.</span><span class="sxs-lookup"><span data-stu-id="15b27-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="15b27-112">Katso myös [Työtilaustyypit ](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="15b27-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Kuva 3](media/26-work-orders.png)

3. <span data-ttu-id="15b27-114">Kun määrität työtilausten projektiryhmät (**Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Projektiasetukset** > **Projektiryhmä**-linkki), luot suhteen investointeihin käytettävän työtilaustyypin ja investoinneille **Projektinhallinta ja kirjanpito** -moduulissa (**Projektinhallinta ja kirjanpito** > **Asetukset** > **Kirjaus** > **Projektiryhmät**) luodun projektiryhmän välillä.</span><span class="sxs-lookup"><span data-stu-id="15b27-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Kuva 4](media/27-work-orders.png)

4. <span data-ttu-id="15b27-116">Kun luot käyttöomaisuusobjektiin liittyvän työtilauksen, valitset sijoitusten käsittelyyn käytettävän työtilaustyypin, esimerkiksi "investointi".</span><span class="sxs-lookup"><span data-stu-id="15b27-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="15b27-117">Kun työtilaus luodaan, siihen liittyvä työtilaustyyppi näkyy kohdassa **Kaikki työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="15b27-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![Kuva 5](media/28-work-orders.png)

6. <span data-ttu-id="15b27-119">Kun työtilaus luodaan, työtilaukseen liittyvä projekti luodaan kohdassa **Projektinhallinta ja kirjanpito** > **Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="15b27-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="15b27-120">Voit tarkastella projektiin liittyviä tietoja napsauttamalla työtilauksen **Projektitunnus**-linkkiä (**Resurssien hallinta**, avaa työtilaus Tiedot-näkymässä > **Rivin tiedot** -pikavälilehti > **Yleiset** -välilehti > **Projektitunnus**-kenttä).</span><span class="sxs-lookup"><span data-stu-id="15b27-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![Kuva 6](media/29-work-orders.png)

7. <span data-ttu-id="15b27-122">**Käyttöomaisuuserät**-kohdassa näkyy yhteenveto käyttöomaisuuserään liittyvistä projekteista (**Käyttöomaisuuserät** > **Käyttöomaisuuserät** > **Käyttöomaisuuserät** > valitse **Käyttöomaisuuserän numero** -kentässä erä ja> tarkastele **Aiheeseen liittyvät tiedot**-ruudun sisällössä kohtaa **Liittyvät projektit**).</span><span class="sxs-lookup"><span data-stu-id="15b27-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

