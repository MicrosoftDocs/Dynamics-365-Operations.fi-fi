---
title: Huoltokohderyhmät
description: Kohderyhmät ovat hyödyllisiä raporttien ja tilastojen tietojen lajittelussa ja suodatuksessa.
author: ShylaThompson
manager: AnnBe
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc5b1bf93deaf60a3c6384671ad575c73871eb35
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543327"
---
# <a name="service-object-groups"></a><span data-ttu-id="be84d-103">Huoltokohderyhmät</span><span class="sxs-lookup"><span data-stu-id="be84d-103">Service object groups</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be84d-104">Kohderyhmät ovat hyödyllisiä raporttien ja tilastojen tietojen lajittelussa ja suodatuksessa.</span><span class="sxs-lookup"><span data-stu-id="be84d-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="be84d-105">Voit ryhmittää kohteita esimerkiksi maantieteellisen sijainnin tai tyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="be84d-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="be84d-106">Ryhmittely maantieteellisen sijainnin mukaan</span><span class="sxs-lookup"><span data-stu-id="be84d-106">Group by geographical location</span></span>

<span data-ttu-id="be84d-107">Voit käyttää tätä ryhmittelymenetelmää näyttämään, missä yrityksen huoltamat eri kohteet sijaitsevat.</span><span class="sxs-lookup"><span data-stu-id="be84d-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="be84d-108">Kohteiden ryhmittely maantieteellisen sijainnin mukaan on hyödyllistä myös esimerkiksi silloin, kun sinun on määritettävä tietyn maan/alueen kohteet, joita yritys jo huoltaa.</span><span class="sxs-lookup"><span data-stu-id="be84d-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="be84d-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="be84d-109">Example</span></span>

<span data-ttu-id="be84d-110">Belgialainen asiakas soittaa palvelukeskukseen ja haluaa tehdä huoltosopimuksen kohteesta ABC.</span><span class="sxs-lookup"><span data-stu-id="be84d-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="be84d-111">Olet liittänyt kaikkiin Belgiassa huollettaviin kohteisiin maantieteellisen sijainnin kohderyhmän Belgia.</span><span class="sxs-lookup"><span data-stu-id="be84d-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="be84d-112">Kun käytät ryhmää suodattimena, voit hakea nopeasti, onko ABC jo tietueena ohjelmassa vai onko sinun määritettävä uusi kohde.</span><span class="sxs-lookup"><span data-stu-id="be84d-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="be84d-113">Ryhmittely tyypin mukaan</span><span class="sxs-lookup"><span data-stu-id="be84d-113">Group by type</span></span>

<span data-ttu-id="be84d-114">Voit näyttää yrityksesi huoltamien kohteiden tyypit käyttämällä tätä ryhmittelymenetelmää.</span><span class="sxs-lookup"><span data-stu-id="be84d-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="be84d-115">Kohteiden ryhmittely tyypin mukaan voi olla hyödyllinen toiminto myös esimerkiksi silloin, kun haluat luoda uuden objektin ohjelmaan aiemmin luotujen kohteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="be84d-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="be84d-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="be84d-116">Example</span></span>

<span data-ttu-id="be84d-117">Asiakas soittaa ja haluaa tehdä ilmastointilaitteelle HIJ huoltosopimuksen.</span><span class="sxs-lookup"><span data-stu-id="be84d-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="be84d-118">Tälle laitteelle ei ole vielä tietuetta.</span><span class="sxs-lookup"><span data-stu-id="be84d-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="be84d-119">Olet kuitenkin aiemmin määrittänyt kohderyhmän nimeltä Ilmastointilaitteet ja liittänyt tämän ryhmän kaikkiin ilmastointilaitekohteisiin.</span><span class="sxs-lookup"><span data-stu-id="be84d-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="be84d-120">Niinpä voitkin nopeasti etsiä ja määrittää muut ilmastointilaitteet ja käyttää näiden kohteiden mallitietoja HIJ:n huoltosopimusrivejä luotaessa.</span><span class="sxs-lookup"><span data-stu-id="be84d-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="be84d-121">Käyttämällä kohderyhmiä tällä tavalla voit määrittää uudet kohteet nopeasti. Voit määrittää myös niissä tehtävät huoltotehtävät.</span><span class="sxs-lookup"><span data-stu-id="be84d-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 

## <a name="create-service-object-groups"></a><span data-ttu-id="be84d-122">Huoltokohderyhmien luominen</span><span class="sxs-lookup"><span data-stu-id="be84d-122">Create service object groups</span></span>

<span data-ttu-id="be84d-123">Voit luoda ryhmiä, joihin voit määrittää huoltokohteet.</span><span class="sxs-lookup"><span data-stu-id="be84d-123">Create groups that you can assign service objects to.</span></span> <span data-ttu-id="be84d-124">Huoltokohteet ovat varastonimikkeitä ja muita tuotteita, jonka palvelut suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="be84d-124">Service objects are inventory items and other products for which services are performed.</span></span> <span data-ttu-id="be84d-125">Ryhmittämällä palveluobjekteja voit luoda raportteja vastaaville ja liittyville palveluobjekteille.</span><span class="sxs-lookup"><span data-stu-id="be84d-125">By grouping service objects, you can create reports for similar and related service objects.</span></span> <span data-ttu-id="be84d-126">Huoltokohderyhmä voi koostua esimerkiksi kahdesta huoltokohteesta: yksi huoltokohde on sarja ja toinen huoltokohde on huolto, jonka avulla sarja asennetaan.</span><span class="sxs-lookup"><span data-stu-id="be84d-126">For example, a service object group might consist of two service objects: One service object is a kit, and the second service object is the service to install the kit.</span></span>

<span data-ttu-id="be84d-127">Luo huolto kohderyhmiä noudattamalla seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="be84d-127">To create service object groups, follow these steps:</span></span>

1. <span data-ttu-id="be84d-128">Valitse **Huoltohallinta > Asetukset > Huoltokohteet > Huoltokohderyhmät**.</span><span class="sxs-lookup"><span data-stu-id="be84d-128">Click **Service management > Setup > Service objects > Service object groups**.</span></span>

2. <span data-ttu-id="be84d-129">Luo uusi huoltokohderyhmä valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="be84d-129">Click **New** to create a new service object group.</span></span>

3. <span data-ttu-id="be84d-130">Kirjoita palveluobjektiryhmälle yksilöivä nimi ja halutessasi kuvaus.</span><span class="sxs-lookup"><span data-stu-id="be84d-130">Enter a unique name for the service object group and, optionally, a description.</span></span>

<span data-ttu-id="be84d-131">Voit määrittää huoltokohteet ryhmään **Huoltokohteet**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="be84d-131">You can assign service objects to the group by using the **Service objects** form.</span></span> 

## <a name="see-also"></a><span data-ttu-id="be84d-132">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="be84d-132">See also</span></span>

[<span data-ttu-id="be84d-133">Huoltokohteiden luominen</span><span class="sxs-lookup"><span data-stu-id="be84d-133">Create service objects</span></span>](create-service-objects.md)


