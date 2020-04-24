---
title: Laske nimikkeen ennuste
description: Tässä ohjeaiheessa kerrotaan, kuinka nimike-ennuste lasketaan resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 20f969b68e4e9a9936f377000191ba9db202447f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216456"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="d690f-103">Laske nimikkeen ennuste</span><span class="sxs-lookup"><span data-stu-id="d690f-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d690f-104">Samalla tavalla kuin voit suorittaa edellisessä osassa kuvatut kapasiteetin kuormituksen laskennat, voit myös tehdä nimikkeen ennustelaskelmia:</span><span class="sxs-lookup"><span data-stu-id="d690f-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="d690f-105">ylläpitoaikataulun riveille</span><span class="sxs-lookup"><span data-stu-id="d690f-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="d690f-106">työtilauksille, joita ei ole vielä ajoitettu</span><span class="sxs-lookup"><span data-stu-id="d690f-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="d690f-107">ajoitetuille työtilauksille.</span><span class="sxs-lookup"><span data-stu-id="d690f-107">scheduled work orders</span></span>

<span data-ttu-id="d690f-108">Tästä on hyötyä, jos haluat saada yleiskuvan odotetusta nimikkeen kulutuksesta (varaosat sekä muut työtilausten täyttämisessä tarvittavat nimikkeet) tietyltä kaudelta.</span><span class="sxs-lookup"><span data-stu-id="d690f-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="d690f-109">Nimike-ennusteen laskeminen voidaan tehdä kaikille käyttöomaisuuksille tai valituille käyttöomaisuuksille.</span><span class="sxs-lookup"><span data-stu-id="d690f-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="d690f-110">Voit myös tehdä laskelmia ylläpidon käyttökatkon tehtäville (**Kaikki ylläpidon käyttökatkojen toiminnot** tai **Aktiiviset ylläpidon käyttökatkojen toiminnot**) tai työtilauspooleille (**Kaikki työtilauspoolit** tai **Aktiiviset työtilauspoolit**).</span><span class="sxs-lookup"><span data-stu-id="d690f-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="d690f-111">Valitse **Resurssien hallinta** > **Kyselyt** > **Nimike-ennuste** tai **Resurssien hallinta** > **Yhteiset** > **Työtilauspoolit** > **Kaikki työtilauspoolit** / **Aktiiviset työtilauspoolit** > valitse työtilauspooli listasta > **Nimike-ennuste** -painike tai **Resurssien hallinta** > **Yhteiset** > **Ylläpidon käyttökatkojen toiminnot** > **Kaikki ylläpidon käyttökatkojen toiminnot** / **Aktiiviset ylläpidon käyttökatkojen toiminnot** > valitse ylläpitokatkon toiminto listasta> **Nimike-ennuste** -painike.</span><span class="sxs-lookup"><span data-stu-id="d690f-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="d690f-112">Valitse **Laske nimike-ennuste** -valintaikkunassa laskennan kausi **Alkamispäivämäärä/-kellonaika**- ja **Päättymispäivämäärä/-kellonaika** -kentissä.</span><span class="sxs-lookup"><span data-stu-id="d690f-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="d690f-113">Valitse **Sisällytä ylläpitoaikataulu** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää ylläpitoaikataulurivit ennustelaskelmiin.</span><span class="sxs-lookup"><span data-stu-id="d690f-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="d690f-114">Valitse **Sisällytä työtilaus** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää työttilauksen työt ennustelaskelmiin.</span><span class="sxs-lookup"><span data-stu-id="d690f-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="d690f-115">**Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia nimike-ennusteen riveistä haluat liittyen toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="d690f-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="d690f-116">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin ylläpitoaikataulun rivit ja työtilaukset näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="d690f-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="d690f-117">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki kunnossapitoaikataulurivit ja kaikki työtilaukset kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="d690f-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="d690f-118">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="d690f-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="d690f-119">Valitse **Ryhmittely...**-ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason.</span><span class="sxs-lookup"><span data-stu-id="d690f-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="d690f-120">Alla olevassa näyttökuvassa valitut **Ryhmittele...**-painikkeet on korostettu sinisellä.</span><span class="sxs-lookup"><span data-stu-id="d690f-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="d690f-121">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="d690f-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="d690f-122">Valitse **Näytä dimensiot** -painike, jos haluat nähdä nimikkeisiin liittyvät tuote-, varastointi- tai seurantadimensiot.</span><span class="sxs-lookup"><span data-stu-id="d690f-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="d690f-123">Valitse asiaankuuluvat valintaruudut ja napsauta sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d690f-123">Select the relevant check boxes, and click **OK**.</span></span>

![Kuva 1](media/02-capacity-planning.png)
