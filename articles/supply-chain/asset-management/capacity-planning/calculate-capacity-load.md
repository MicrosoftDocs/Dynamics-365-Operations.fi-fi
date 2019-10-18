---
title: Laske kapasiteetin kuormitus
description: Tässä ohjeaiheessa kerrotaan, kuinka kapasiteettikuormitus lasketaan resurssien hallinnassa.
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
ms.openlocfilehash: 82f65293679591f278e0e3b79c112ba36debc3bb
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2277940"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="36309-103">Laske kapasiteetin kuormitus</span><span class="sxs-lookup"><span data-stu-id="36309-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="36309-104">Resurssien hallinnassa voit laskea kapasiteetin kuormituksen</span><span class="sxs-lookup"><span data-stu-id="36309-104">In Asset Management, you can calculate capacity load on</span></span>

- <span data-ttu-id="36309-105">ylläpitoaikataulun riveille</span><span class="sxs-lookup"><span data-stu-id="36309-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="36309-106">työtilauksille, joita ei ole vielä ajoitettu</span><span class="sxs-lookup"><span data-stu-id="36309-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="36309-107">ajoitetuille työtilauksille.</span><span class="sxs-lookup"><span data-stu-id="36309-107">scheduled work orders</span></span>

<span data-ttu-id="36309-108">Tästä on hyötyä, jos haluat saada yleiskuvan tietyn kauden odotetusta kapasiteetin kuormituksesta.</span><span class="sxs-lookup"><span data-stu-id="36309-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="36309-109">Kapasiteetin kuormituksen laskeminen voidaan tehdä kaikille käyttöomaisuuksille tai valituille käyttöomaisuuksille.</span><span class="sxs-lookup"><span data-stu-id="36309-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="36309-110">Voit myös tehdä laskelmia kunnossapitoseisokkien tai työtilauspoolien osalta.</span><span class="sxs-lookup"><span data-stu-id="36309-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="36309-111">Valitse **Resurssien hallinta** > **Kyselyt** > **Kapasiteetin kuormitus** tai **Resurssien hallinta** > **Yhteiset** > **Työtilauspoolit** > **Kaikki työtilauspoolit** / **Aktiiviset työtilauspoolit** > valitse työtilauspooli listasta > **Kapasiteetin kuormitus** -painike tai **Resurssien hallinta** > **Yhteiset** > **Ylläpidon käyttökatkojen toiminnot** > **Kaikki ylläpidon käyttökatkojen toiminnot** / **Aktiiviset ylläpidon käyttökatkojen toiminnot** > valitse ylläpidon toiminno listasta> **Kapasiteetin kuormitus** -painike.</span><span class="sxs-lookup"><span data-stu-id="36309-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="36309-112">Valitse **Laske kapasiteetin kuormitus** -valintaikkunassa laskennan kausi **Alkamispäivämäärä/-kellonaika**- ja **Päättymispäivämäärä/-kellonaika** -kentissä.</span><span class="sxs-lookup"><span data-stu-id="36309-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="36309-113">Valitse **Sisällytä ylläpitoaikataulu** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää ylläpitoaikataulurivit laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="36309-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="36309-114">Valitse **Sisällytä työtilaus** -vaihtopainikkeen arvoksi Kyllä, jos haluat sisällyttää työttilauksen työt laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="36309-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="36309-115">**Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia kapasiteetin kuormitusriveistä haluat liittyen toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="36309-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> <span data-ttu-id="36309-116">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin ylläpitoaikataulun rivit ja työtilaukset näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="36309-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="36309-117">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki kunnossapitoaikataulurivit ja kaikki työtilaukset kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="36309-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="36309-118">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="36309-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="36309-119">Valitse toimintoruudun **Ryhmittely...** -ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason.</span><span class="sxs-lookup"><span data-stu-id="36309-119">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="36309-120">Valitut toimintoruudun ryhmäpainikkeet on korostettu sinisellä.</span><span class="sxs-lookup"><span data-stu-id="36309-120">The selected action pane group buttons are highlighted in blue color.</span></span> <span data-ttu-id="36309-121">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="36309-121">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="36309-122">Alla oleva kuva näyttää esimerkin käyttöliittymästä.</span><span class="sxs-lookup"><span data-stu-id="36309-122">The figure below shows an example of the interface.</span></span>

![Kuva 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="36309-124">Jos haluat keskittyä vain ajoitettujen työtilausten kapasiteettisuunnitteluun, lisätietoja on kohdassa [Ajoitettujen työtilausten kapasiteetin kuormituksen laskeminen](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="36309-124">If you want to focus only on capacity planning regarding scheduled work orders, refer to [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

