---
title: Huoltokohteet
description: "Huoltokohteet ovat asiakkaan käyttöomaisuuseriä ja tuotteita, joille voidaan suorittaa huoltoja."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 29d63357b11d6222646102e53d83f68ae75cb5bb
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="service-objects"></a><span data-ttu-id="70d44-103">Huoltokohteet</span><span class="sxs-lookup"><span data-stu-id="70d44-103">Service objects</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70d44-104">Huoltokohteet ovat asiakkaan käyttöomaisuuseriä ja tuotteita, joille voidaan suorittaa huoltoja.</span><span class="sxs-lookup"><span data-stu-id="70d44-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="70d44-105">Objektit voivat olla tarjoamasi huollon mukaan aineellisia tai aineettomia:</span><span class="sxs-lookup"><span data-stu-id="70d44-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="70d44-106">Aineellisia objekteja ovat kohteet, joille voidaan tehdä fyysinen huoltotehtävä. Näitä objekteja ovat mm. kone tai rakennus.</span><span class="sxs-lookup"><span data-stu-id="70d44-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="70d44-107">Aineellinen huolto-objekti voi myös olla varastonimike, joka luodaan Vapautetun tuotteen tiedot -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="70d44-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="70d44-108">Riippuen varaston dimensioryhmästä, johon liität nimikkeen, voit luoda palveluobjektin sellaisella yksityiskohtien tasolla, joka sisältää nimikkeen sarjanumeron.</span><span class="sxs-lookup"><span data-stu-id="70d44-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="70d44-109">Se on hyödyllistä silloin, kun sinun on jäljitettävä huolto-objektin edustama tarkka nimike.</span><span class="sxs-lookup"><span data-stu-id="70d44-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="70d44-110">Aineellinen huolto-objekti voi kuitenkin olla myös nimike, joka ei suoraan liity yrityksen suoraan tuotanto- tai toimitusketjuun.</span><span class="sxs-lookup"><span data-stu-id="70d44-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="70d44-111">Esimerkiksi huoltotilauksen korjauksissa käytettävä työkalusarja voi olla huoltokohde, jota ei sisällytetä varastoon.</span><span class="sxs-lookup"><span data-stu-id="70d44-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="70d44-112">Tässä tapauksessa et rekisteröi sitä varastonimikkeenä.</span><span class="sxs-lookup"><span data-stu-id="70d44-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="70d44-113">Aineettomia objekteja ovat ei-fyysiset asiat, kuten tilijoukko tai lakisääteinen tosite, jolle palvelutehtäviä suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="70d44-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="70d44-114">Esimerkki aineettomasta huolto-objektista</span><span class="sxs-lookup"><span data-stu-id="70d44-114">Example of an intangible service object</span></span>

<span data-ttu-id="70d44-115">Yritys A ylläpitää useiden pienten yritysten kirjanpitotietueita.</span><span class="sxs-lookup"><span data-stu-id="70d44-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="70d44-116">Yksi yritys A:n asiakkaista on paikallinen jalkapalloseura, jonka viikoittaista kirjanpitoa ja vuosittaista tarkistusta yritys A hoitaa.</span><span class="sxs-lookup"><span data-stu-id="70d44-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="70d44-117">Klubin tilit määritetään Huoltokohteet-lomakkeella ja määritetään kohteiksi huoltosopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="70d44-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="70d44-118">Objektille on kaksi palvelusopimusriviä.</span><span class="sxs-lookup"><span data-stu-id="70d44-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="70d44-119">Rivi 1 on viikoittainen kirjanpito, joka sisältää riviin määritetyn viikoittaisen aikavälin, ja rivi 2 on vuosittainen tarkistus, johon on määritetty vuosittainen aikaväli.</span><span class="sxs-lookup"><span data-stu-id="70d44-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70d44-120">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="70d44-120">Related topics</span></span>

[<span data-ttu-id="70d44-121">Huoltokohteiden luominen</span><span class="sxs-lookup"><span data-stu-id="70d44-121">Create service objects</span></span>](create-service-objects.md)


