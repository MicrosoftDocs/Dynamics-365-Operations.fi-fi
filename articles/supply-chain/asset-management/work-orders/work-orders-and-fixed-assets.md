---
title: Työtilaukset ja käyttöomaisuuserät
description: Tässä ohjeaiheessa selitetään, miten työtilaukset ja käyttöomaisuuserät ajoitetaan käyttöomaisuuden hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 678bfae5d0b4ea469a91fc89306be40c39cb082d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223431"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="88f08-103">Työtilaukset ja käyttöomaisuuserät</span><span class="sxs-lookup"><span data-stu-id="88f08-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="88f08-104">Resurssien hallinnassa resurssit voivat liittyä käyttöomaisuuseriin, ja voit luoda työtilauksia kyseisille resursseille.</span><span class="sxs-lookup"><span data-stu-id="88f08-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="88f08-105">Jos käytät tätä toimintoa, voit saada kattavan yleiskuvan käyttöomaisuudesta, siihen liittyvistä investointiprojekteista sekä investointiprojekteihin rekisteröidyistä kustannuksista moduuleissa **Projektinhallinta ja kirjanpito** ja **Käyttöomaisuuserät** Microsoft Dynamics 365 for Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="88f08-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="88f08-106">**Käyttöomaisuuden numero** -kenttä määritetään työtilauksen työprojektissa vain, jos työtilauksen työprojektin projektityypiksi on valittu **Investointi**.</span><span class="sxs-lookup"><span data-stu-id="88f08-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="88f08-107">Alla olevassa kuvassa näkyy **Projektinhallinta ja kirjanpito** -moduulissa olevan investointiprojektin ja työtilaustehtäväprojektin välinen suhde.</span><span class="sxs-lookup"><span data-stu-id="88f08-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![Kuva 1](media/24-work-orders.png)

<span data-ttu-id="88f08-109">Seuraavassa menettelyssä kuvataan resurssien, työtilausten, työtilausten työprojektien ja käyttöomaisuuserien välinen suhde.</span><span class="sxs-lookup"><span data-stu-id="88f08-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="88f08-110">Luot resurssin, jonka liität käyttöomaisuuteen.</span><span class="sxs-lookup"><span data-stu-id="88f08-110">You create an asset that you relate to a fixed asset.</span></span>

![Kuva 2](media/25-work-orders.png)

2. <span data-ttu-id="88f08-112">Kun määrität työtilaustyypit **Työtilaustyypit**-sivulla (**Resurssienhallinta** > **Asetukset** > **Työtilaukset** > **Työtilaustyypit**), luot työtilaustyypin, jolla käsitellään investointeja.</span><span class="sxs-lookup"><span data-stu-id="88f08-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="88f08-113">Katso myös [Työtilaustyypit ](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="88f08-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Kuva 3](media/26-work-orders.png)

3. <span data-ttu-id="88f08-115">Kun määrität työtilausten projektiryhmiä **Työtilauksen projektiasetukset**-sivun **Projektiryhmä**-välilehdessä (**Resurssienhallinta** > **Asetukset** > **Työtilaukset** > **Projektimääritykset**), luot suhteen investointeihin käytettävän työtilaustyypin ja investoinneille **Projektinhallinta ja kirjanpito** -moduulin **Projektiryhmät**-sivulla (**Projektinhallinta ja kirjanpito** > **Asetukset** > **Kirjaus** > **Projektiryhmät**) luodun projektiryhmän välillä.</span><span class="sxs-lookup"><span data-stu-id="88f08-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Kuva 4](media/27-work-orders.png)

4. <span data-ttu-id="88f08-117">Kun luot käyttöomaisuuteen liittyvän työtilauksen, valitset investointien käsittelyyn käytettävän työtilaustyypin (kuten **Investointi**).</span><span class="sxs-lookup"><span data-stu-id="88f08-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="88f08-118">Kun työtilaus luodaan, siihen liittyvä työtilaustyyppi näkyy sivulla **Kaikki työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="88f08-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![Kuva 5](media/28-work-orders.png)

6. <span data-ttu-id="88f08-120">Kun työtilaus luodaan, työtilaukseen liittyvä projekti luodaan **Kaikki projektit** -sivulla **Projektinhallinta ja kirjanpito** -moduulissa (**Projektinhallinta ja kirjanpito** > **Projektit** > **Kaikki projektit**).</span><span class="sxs-lookup"><span data-stu-id="88f08-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="88f08-121">Jos haluat tarkastella projektiin liittyviä tietoja, valitse linkki **Projektitunnus**-kentässä **Yleistä**-välilehdessä **Rivitiedot**-pikavälilehdessä **Kaikki työtilaukset** -sivun tietonäkymässä **Resurssienhallinta** -moduulissa (**Resurssienhallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset**).</span><span class="sxs-lookup"><span data-stu-id="88f08-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![Kuva 6](media/29-work-orders.png)

7. <span data-ttu-id="88f08-123">Jos haluat nähdä yhteenvedon käyttöomaisuuteen liittyvistä projekteista, valitse **Käyttöomaisuuserät** > **Käyttöomaisuuserät** > **Käyttöomaisuuserät** ja sitten **Käyttöomaisuuserän numero** -kentässä linkki käyttöomaisuudelle, joka avataan tietonäkymässä.</span><span class="sxs-lookup"><span data-stu-id="88f08-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="88f08-124">Laajenna **Aiheeseen liittyviä tietoja** -ruutu sivun oikeassa reunassa ja valitse **Liittyvät projektit** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="88f08-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]