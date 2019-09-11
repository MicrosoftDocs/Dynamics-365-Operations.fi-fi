---
title: Laske nimikkeen ennuste
description: Tässä ohjeaiheessa kerrotaan, kuinka nimike-ennuste lasketaan resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9091ff7a394cd08b68e78c8f668d7cd962003e6d
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886767"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="31dd7-103">Laske nimikkeen ennuste</span><span class="sxs-lookup"><span data-stu-id="31dd7-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="31dd7-104">Samalla tavalla kuin voit suorittaa edellisessä osassa kuvatut kapasiteetin kuormituksen laskennat, voit myös tehdä nimikkeen ennustelaskelmia</span><span class="sxs-lookup"><span data-stu-id="31dd7-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on</span></span>

- <span data-ttu-id="31dd7-105">Ylläpitoaikataulun rivit</span><span class="sxs-lookup"><span data-stu-id="31dd7-105">Maintenance schedule lines</span></span>  
- <span data-ttu-id="31dd7-106">työtilauksille, joita ei ole vielä ajoitettu</span><span class="sxs-lookup"><span data-stu-id="31dd7-106">Work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="31dd7-107">Ajoitetut työtilaukset</span><span class="sxs-lookup"><span data-stu-id="31dd7-107">Scheduled work orders</span></span>

<span data-ttu-id="31dd7-108">Tästä on hyötyä, jos haluat saada yleiskuvan odotetusta nimikkeen kulutuksesta (varaosat sekä muut työtilausten täyttämisessä tarvittavat nimikkeet) tietyltä kaudelta.</span><span class="sxs-lookup"><span data-stu-id="31dd7-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="31dd7-109">Nimike-ennusteen laskeminen voidaan tehdä kaikille käyttöomaisuuksille tai valituille käyttöomaisuuksille.</span><span class="sxs-lookup"><span data-stu-id="31dd7-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="31dd7-110">Voit myös tehdä laskelmia ylläpidon käyttökatkon tehtäville (**Kaikki ylläpidon käyttökatkojen toiminnot** tai **Aktiiviset ylläpidon käyttökatkojen toiminnot**) tai työtilauspooleille (**Kaikki työtilauspoolit** tai **Aktiiviset työtilauspoolit**).</span><span class="sxs-lookup"><span data-stu-id="31dd7-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="31dd7-111">Valitse **Resurssien hallinta** > **Kyselyt** > **Nimike-ennuste** tai **Resurssien hallinta** > **Yhteiset** > **Työtilauspoolit** > **Kaikki työtilauspoolit** / **Aktiiviset työtilauspoolit** > valitse työtilauspooli listasta > **Nimike-ennuste** -painike tai **Resurssien hallinta** > **Yhteiset** > **Ylläpidon käyttökatkojen toiminnot** > **Kaikki ylläpidon käyttökatkojen toiminnot** / **Aktiiviset ylläpidon käyttökatkojen toiminnot** > valitse ylläpitokatkon toiminto listasta> **Nimike-ennuste** -painike.</span><span class="sxs-lookup"><span data-stu-id="31dd7-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="31dd7-112">Valitse **Laske nimike-ennuste** -valintaikkunassa laskennan kausi **Alkamispäivämäärä/-kellonaika**- ja **Päättymispäivämäärä/-kellonaika** -kentissä.</span><span class="sxs-lookup"><span data-stu-id="31dd7-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="31dd7-113">Valitse **Sisällytä ylläpitoaikataulu** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää ylläpitoaikataulurivit ennustelaskelmiin.</span><span class="sxs-lookup"><span data-stu-id="31dd7-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="31dd7-114">Valitse **Sisällytä työtilaus** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää työttilauksen työt ennustelaskelmiin.</span><span class="sxs-lookup"><span data-stu-id="31dd7-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="31dd7-115">**Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia nimike-ennusteen riveistä haluat liittyen toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="31dd7-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> <span data-ttu-id="31dd7-116">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin ylläpitoaikataulun rivit ja työtilaukset näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="31dd7-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="31dd7-117">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki kunnossapitoaikataulurivit ja kaikki työtilaukset kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="31dd7-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="31dd7-118">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="31dd7-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="31dd7-119">Valitse toimintoruudun **Ryhmittely...** -ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason.</span><span class="sxs-lookup"><span data-stu-id="31dd7-119">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="31dd7-120">Valitut toimintoruudun ryhmäpainikkeet on korostettu sinisellä.</span><span class="sxs-lookup"><span data-stu-id="31dd7-120">The selected action pane group buttons are highlighted in blue color.</span></span> <span data-ttu-id="31dd7-121">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="31dd7-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="31dd7-122">Valitse **Näytä dimensiot** -painike, jos haluat nähdä nimikkeisiin liittyvät tuote-, varastointi- tai seurantadimensiot.</span><span class="sxs-lookup"><span data-stu-id="31dd7-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="31dd7-123">Valitse asiaankuuluvat valintaruudut ja napsauta sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="31dd7-123">Select the relevant check boxes, and click **OK**.</span></span>

<span data-ttu-id="31dd7-124">Alla oleva kuva näyttää näyttökuvan käyttöliittymästä.</span><span class="sxs-lookup"><span data-stu-id="31dd7-124">The figure below shows a screenshot of the interface.</span></span>

![Kuva 1](media/02-capacity-planning.png)
