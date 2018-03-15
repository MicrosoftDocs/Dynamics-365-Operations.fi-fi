---
title: "Huoltokohderyhmät"
description: "Kohderyhmät ovat hyödyllisiä raporttien ja tilastojen tietojen lajittelussa ja suodatuksessa."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
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
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: fa503ac82286099a0eafc7034d169e165b538e2c
ms.contentlocale: fi-fi
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="b60ed-103">Huoltokohderyhmät</span><span class="sxs-lookup"><span data-stu-id="b60ed-103">Service object groups</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b60ed-104">Kohderyhmät ovat hyödyllisiä raporttien ja tilastojen tietojen lajittelussa ja suodatuksessa.</span><span class="sxs-lookup"><span data-stu-id="b60ed-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="b60ed-105">Voit ryhmittää kohteita esimerkiksi maantieteellisen sijainnin tai tyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="b60ed-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="b60ed-106">Ryhmittely maantieteellisen sijainnin mukaan</span><span class="sxs-lookup"><span data-stu-id="b60ed-106">Group by geographical location</span></span>

<span data-ttu-id="b60ed-107">Voit käyttää tätä ryhmittelymenetelmää näyttämään, missä yrityksen huoltamat eri kohteet sijaitsevat.</span><span class="sxs-lookup"><span data-stu-id="b60ed-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="b60ed-108">Kohteiden ryhmittely maantieteellisen sijainnin mukaan on hyödyllistä myös esimerkiksi silloin, kun sinun on määritettävä tietyn maan/alueen kohteet, joita yritys jo huoltaa.</span><span class="sxs-lookup"><span data-stu-id="b60ed-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="b60ed-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="b60ed-109">Example</span></span>

<span data-ttu-id="b60ed-110">Belgialainen asiakas soittaa palvelukeskukseen ja haluaa tehdä huoltosopimuksen kohteesta ABC.</span><span class="sxs-lookup"><span data-stu-id="b60ed-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="b60ed-111">Olet liittänyt kaikkiin Belgiassa huollettaviin kohteisiin maantieteellisen sijainnin kohderyhmän Belgia.</span><span class="sxs-lookup"><span data-stu-id="b60ed-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="b60ed-112">Kun käytät ryhmää suodattimena, voit hakea nopeasti, onko ABC jo tietueena ohjelmassa vai onko sinun määritettävä uusi kohde.</span><span class="sxs-lookup"><span data-stu-id="b60ed-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="b60ed-113">Ryhmittely tyypin mukaan</span><span class="sxs-lookup"><span data-stu-id="b60ed-113">Group by type</span></span>

<span data-ttu-id="b60ed-114">Voit näyttää yrityksesi huoltamien kohteiden tyypit käyttämällä tätä ryhmittelymenetelmää.</span><span class="sxs-lookup"><span data-stu-id="b60ed-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="b60ed-115">Kohteiden ryhmittely tyypin mukaan voi olla hyödyllinen toiminto myös esimerkiksi silloin, kun haluat luoda uuden objektin ohjelmaan aiemmin luotujen kohteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="b60ed-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="b60ed-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="b60ed-116">Example</span></span>

<span data-ttu-id="b60ed-117">Asiakas soittaa ja haluaa tehdä ilmastointilaitteelle HIJ huoltosopimuksen.</span><span class="sxs-lookup"><span data-stu-id="b60ed-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="b60ed-118">Tälle laitteelle ei ole vielä tietuetta.</span><span class="sxs-lookup"><span data-stu-id="b60ed-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="b60ed-119">Olet kuitenkin aiemmin määrittänyt kohderyhmän nimeltä Ilmastointilaitteet ja liittänyt tämän ryhmän kaikkiin ilmastointilaitekohteisiin.</span><span class="sxs-lookup"><span data-stu-id="b60ed-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="b60ed-120">Niinpä voitkin nopeasti etsiä ja määrittää muut ilmastointilaitteet ja käyttää näiden kohteiden mallitietoja HIJ:n huoltosopimusrivejä luotaessa.</span><span class="sxs-lookup"><span data-stu-id="b60ed-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="b60ed-121">Käyttämällä kohderyhmiä tällä tavalla voit määrittää uudet kohteet nopeasti. Voit määrittää myös niissä tehtävät huoltotehtävät.</span><span class="sxs-lookup"><span data-stu-id="b60ed-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 



