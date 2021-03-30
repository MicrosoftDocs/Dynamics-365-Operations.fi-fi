---
title: Automaattisesti luodut huoltotilaukset
description: Voit luoda huoltosopimuksiin perustuvia huoltotilauksia huoltosopimuksen voimassaoloaikana.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c1244cedff23df0350598a3cc876d39d4400b8e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232131"
---
# <a name="automatically-create-service-orders"></a><span data-ttu-id="5eb19-103">Automaattisesti luodut huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="5eb19-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5eb19-104">Voit luoda huoltosopimuksiin perustuvia huoltotilauksia huoltosopimuksen voimassaoloaikana.</span><span class="sxs-lookup"><span data-stu-id="5eb19-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="5eb19-105">Huoltosopimuksista luotavat huoltotilaukset liitetään huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="5eb19-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="5eb19-106">Huoltotilaukset luodaan automaattisesti seuraavista asetuksista:</span><span class="sxs-lookup"><span data-stu-id="5eb19-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="5eb19-107">Huoltosopimuksen välin asetukset huoltosopimusriveillä.</span><span class="sxs-lookup"><span data-stu-id="5eb19-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="5eb19-108">Huoltosopimuksen väli ilmaisee huoltotilausrivien luomisen tiheyden.</span><span class="sxs-lookup"><span data-stu-id="5eb19-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="5eb19-109">Lisätietoja on kohdassa [Huoltovälit](service-intervals.md).</span><span class="sxs-lookup"><span data-stu-id="5eb19-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="5eb19-110">Huoltojakson määritys **Alkupäivämäärä**- ja **Loppupäivämäärä** -kentissä **Luo huoltotilauksia** -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="5eb19-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="5eb19-111">Lisätietoja on kohdassa [Luo huoltotilaukset automaattisesti](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="5eb19-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="5eb19-112">**Yhdistä huoltotilaukset** -vaihtoehto huoltosopimuksen otsikossa.</span><span class="sxs-lookup"><span data-stu-id="5eb19-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="5eb19-113">Tämä asetus määrittää, yhdistetäänkö huoltotilauksen rivit huoltosopimuksesta työntekijän, huoltotehtävän, huoltokohteen vai huoltosopimuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="5eb19-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="5eb19-114">Lisätietoja on kohdassa [Huoltotilausten yhdistäminen](combine-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="5eb19-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="5eb19-115">Huoltosopimusrivin **Aikaikkuna**-asetus.</span><span class="sxs-lookup"><span data-stu-id="5eb19-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="5eb19-116">Aikaikkuna määrittää, miten kauas huoltotilausrivi voi siirtyä suhteessa sen laskettuun päivämäärään.</span><span class="sxs-lookup"><span data-stu-id="5eb19-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="5eb19-117">Lisätietoja on kohdassa [Aikaikkunat](time-windows.md).</span><span class="sxs-lookup"><span data-stu-id="5eb19-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="5eb19-118">Jos huoltotilauksessa määritetty päivä ei ole avoin <STRONG>Huollon hallintaparametrit</STRONG> -lomakkeessa määritetyssä kalenterissa, järjestelmä ilmoittaa kalenteriristiriidasta.</span><span class="sxs-lookup"><span data-stu-id="5eb19-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="5eb19-119">Voit ohittaa sanoman, sillä huoltotilaus luodaan, vaikka päivä olisikin suljettu kalenterissa.</span><span class="sxs-lookup"><span data-stu-id="5eb19-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="5eb19-120">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="5eb19-120">Example 1</span></span>

<span data-ttu-id="5eb19-121">Huoltosopimus on voimassa 1. tammikuuta 2012 – 31. joulukuuta 2012.</span><span class="sxs-lookup"><span data-stu-id="5eb19-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="5eb19-122">Jos **Luo huoltotilauksia** -lomakkeessa määritetty huoltojakso on 1.11.2012 – 1.2.2013, huoltotilaukset luodaan ajalta 1.11.2012 – 31.12.2012.</span><span class="sxs-lookup"><span data-stu-id="5eb19-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="5eb19-123">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="5eb19-123">Example 2</span></span>

<span data-ttu-id="5eb19-124">Huoltosopimus on voimassa 1. tammikuuta 2012 – 31. joulukuuta 2012.</span><span class="sxs-lookup"><span data-stu-id="5eb19-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="5eb19-125">Huoltosopimukseen on liitetty kaksi huoltosopimusriviä.</span><span class="sxs-lookup"><span data-stu-id="5eb19-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="5eb19-126">Ensimmäisen huoltosopimusrivin alkamispäivä on 2.1.2012 ja päättymispäivä 1.3.2012.</span><span class="sxs-lookup"><span data-stu-id="5eb19-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="5eb19-127">Toisen huoltosopimusrivin alkamispäivä on 1.4.2012 ja päättymispäivä 31.12.2012.</span><span class="sxs-lookup"><span data-stu-id="5eb19-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="5eb19-128">Määrität **Luo huoltotilauksia** -lomakkeessa jaksoksi 1.10.2012–31.12.2012.</span><span class="sxs-lookup"><span data-stu-id="5eb19-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="5eb19-129">Tällöin huoltotilaukset luodaan vain toiselle huoltosopimusriville, sillä ensimmäisen sopimusrivin alkamis- ja päättymispäivä on ennen huoltotilaukselle määritettyä jaksoa.</span><span class="sxs-lookup"><span data-stu-id="5eb19-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]