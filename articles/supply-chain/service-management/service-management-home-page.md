---
title: Huoltohallinta
description: "Huoltohallinta-toimintoa käytetään tekemään huoltosopimuksia ja huollon ylläpitosopimuksia, käsittelemään huoltotilauksia ja asiakaskyselyitä, sekä hallinnoimaan ja analysoimaan huoltotoimituksia asiakkaille."
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
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
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: fi-fi
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="6ed7a-103">Huoltohallinta</span><span class="sxs-lookup"><span data-stu-id="6ed7a-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6ed7a-104">**Huoltohallinta**-toimintoa käytetään tekemään huoltosopimuksia ja huollon ylläpitosopimuksia, käsittelemään huoltotilauksia ja asiakaskyselyitä, sekä hallinnoimaan ja analysoimaan huoltotoimituksia asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="6ed7a-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="6ed7a-105">Voit käyttää palvelusopimuksia määrittämään tavallisessa palveluluettelossa käytettäviä resursseja.</span><span class="sxs-lookup"><span data-stu-id="6ed7a-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="6ed7a-106">Huoltosopimusten avulla voit tarkastella, miten nämä resurssit laskutetaan asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="6ed7a-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="6ed7a-107">Huoltosopimus voidaan myös sisällyttää palvelutasosopimukseen, jossa määritetään normaali vasteaika ja tarjotaan työkalut todellisen ajan kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="6ed7a-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="6ed7a-108">Voit luoda huoltotilauksia hallitsemaan tietoja ajoitetuista ja ajoittamattomista käynneistä, jotka huoltoteknikko tekee asiakkaan toimipaikassa.</span><span class="sxs-lookup"><span data-stu-id="6ed7a-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="6ed7a-109">Huoltotilauksiin kuuluu tietoja, kuten:</span><span class="sxs-lookup"><span data-stu-id="6ed7a-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="6ed7a-110">Työtunnit, jotka huoltoteknikko suorittaa</span><span class="sxs-lookup"><span data-stu-id="6ed7a-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="6ed7a-111">Palvelun tai korjauksen tyyppi</span><span class="sxs-lookup"><span data-stu-id="6ed7a-111">The type of service or repair</span></span>

3.  <span data-ttu-id="6ed7a-112">Korjattava nimike, mukaan lukien tiedot oireista ja diagnoosi</span><span class="sxs-lookup"><span data-stu-id="6ed7a-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="6ed7a-113">Kaikki kulut ja maksut, jotka liittyvät palveluun tai huoltoon</span><span class="sxs-lookup"><span data-stu-id="6ed7a-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="6ed7a-114">Asiakkaat voivat lähettää palvelupyyntöjä Internetin kautta käyttämällä yritysportaalia.</span><span class="sxs-lookup"><span data-stu-id="6ed7a-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="6ed7a-115">Voit vastaanottaa käsitellä ja resursoida näitä pyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="6ed7a-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="6ed7a-116">Kun olet luonut huoltotilauksen, voit valvoa edistymistä huoltovaiheiden avulla sekä määrittää sääntöjä, jotka ohjaavat kussakin vaiheessa käytössä olevia toimintoja.</span><span class="sxs-lookup"><span data-stu-id="6ed7a-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="6ed7a-117">Kun huoltotilaus on valmis, voit hyväksyä tilauksen vahvistaaksesi, että se on valmis ja kirjata sitten tilauksen laskutusprosessin käynnistämiseksi.</span><span class="sxs-lookup"><span data-stu-id="6ed7a-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="6ed7a-118">Käytä raportointityökaluja huoltotilausten marginaalien ja ylläpitosopimustapahtumien valvontaan sekä työmääräinten ja työn vastaanottokuittausten tulostamiseen.</span><span class="sxs-lookup"><span data-stu-id="6ed7a-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="6ed7a-119">Liiketoimintaprosessit</span><span class="sxs-lookup"><span data-stu-id="6ed7a-119">Business processes</span></span>

<span data-ttu-id="6ed7a-120">Seuraavassa kaaviossa on kuvattu korkean tason liiketoimintaprosessit **Huoltohallinta**-toimintoa varten. Kaavio näyttää myös, missä huoltoprosessit integroituvat muiden Microsoft Dynamics 365 for Finance and Operations -moduulien kanssa.</span><span class="sxs-lookup"><span data-stu-id="6ed7a-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="6ed7a-121">[![Huoltohallinta-moduulin liiketoimintaprosessikaavio](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="6ed7a-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="6ed7a-122">Palveluhallinnan esittely</span><span class="sxs-lookup"><span data-stu-id="6ed7a-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ed7a-123">Tärkeät tehtävät</span><span class="sxs-lookup"><span data-stu-id="6ed7a-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="6ed7a-124">Ensisijaiset lomakkeet</span><span class="sxs-lookup"><span data-stu-id="6ed7a-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="6ed7a-125">Suositut raportit</span><span class="sxs-lookup"><span data-stu-id="6ed7a-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ed7a-126">Huoltosopimusten täyttäminen</span><span class="sxs-lookup"><span data-stu-id="6ed7a-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="6ed7a-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Palvelusopimukset (lomake)</a></span><span class="sxs-lookup"><span data-stu-id="6ed7a-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="6ed7a-128"><strong>Huoltotilauksen marginaali</strong></span><span class="sxs-lookup"><span data-stu-id="6ed7a-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ed7a-129">Käsittele asiakkaan kyselyt</span><span class="sxs-lookup"><span data-stu-id="6ed7a-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="6ed7a-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Palvelutilaukset (lomake)</a></span><span class="sxs-lookup"><span data-stu-id="6ed7a-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="6ed7a-131"><strong>Työmääräin</strong></span><span class="sxs-lookup"><span data-stu-id="6ed7a-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6ed7a-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Resursointitaulu (lomake)</a></span><span class="sxs-lookup"><span data-stu-id="6ed7a-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="6ed7a-133"><strong>Tapahtuma - ylläpitosopimus</strong></span><span class="sxs-lookup"><span data-stu-id="6ed7a-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6ed7a-134"><strong>Ylläpitosopimusmaksutapahtumat</strong></span><span class="sxs-lookup"><span data-stu-id="6ed7a-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="6ed7a-135">Palvelun hallinnan integrointi</span><span class="sxs-lookup"><span data-stu-id="6ed7a-135">Integration of Service management</span></span>

<span data-ttu-id="6ed7a-136">Huoltohallinta voidaan integroida seuraaviin Microsoft Dynamics 365 for Finance and Operations -moduuleihin:</span><span class="sxs-lookup"><span data-stu-id="6ed7a-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="6ed7a-137">Myynti ja markkinointi</span><span class="sxs-lookup"><span data-stu-id="6ed7a-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="6ed7a-138">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="6ed7a-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


