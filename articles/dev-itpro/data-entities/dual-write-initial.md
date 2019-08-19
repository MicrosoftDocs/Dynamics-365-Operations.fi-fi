---
title: Finance and Operationsin ja Common Data Servicen alkuperäisen sykronoinnin toteuttamisjärjestys
description: Tässä ohjeaiheessa määritetään synkronoinnin järjestys, jota on noudatettava alkuperäisten tietojen luomiseen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797295"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="29fc7-103">Finance and Operationsin ja Common Data Servicen alkuperäisen sykronoinnin toteuttamisjärjestys</span><span class="sxs-lookup"><span data-stu-id="29fc7-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="29fc7-104">Ennen kuin käytät tietojen integrointia, sinun on luotava asiakkaille, toimittajille ja yhteyshenkilöille tarvittavat alkuperäiset tiedot.</span><span class="sxs-lookup"><span data-stu-id="29fc7-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="29fc7-105">Jos haluat esimerkiksi luoda uuden **toimittajaryhmän** nimikkeen ja määrittää sen **maksuehdoksi** **Net30**-arvon, sinun on varmistettava ennen kuin yrität luoda **toimittajaryhmän** nimikettä, että **Net30** on olemassa sekä Finance and Operationsissa että Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="29fc7-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="29fc7-106">(Tulevaisuudessa julkaisemme kaksoiskirjoitusalustan toiminnallisuuden nimeltä **Alkusynronointi**. Se tekee tietojen kertasynkronoinnin Finance and Operationsin ja Common Data Servicen välillä osana kaksoiskirjoituksen määritystä.)</span><span class="sxs-lookup"><span data-stu-id="29fc7-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="29fc7-107">Vinkkejä: Julkaisemme kaksoiskirjoituksen yhdistämismääritykset kaikille viitetiedoille, mukaan lukien **Maksuehdot** (maksuehdot).</span><span class="sxs-lookup"><span data-stu-id="29fc7-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="29fc7-108">Jos sinulla on jo alkuperäiset tiedot yhdessä järjestelmässä, tietueen pieni päivitystoiminto voi laukaista kaksoiskirjoitustoiminnon kyseiseen tietueeseen.</span><span class="sxs-lookup"><span data-stu-id="29fc7-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="29fc7-109">Sinun on noudatettava seuraavaa järjestystä ja varmistettava, että alkuperäiset tiedot ovat käytettävissä sekä Finance and Operationsissa että Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="29fc7-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="29fc7-110">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="29fc7-110">Vendor</span></span>

<span data-ttu-id="29fc7-111">Toimittajan suoritusjärjestys on:</span><span class="sxs-lookup"><span data-stu-id="29fc7-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="29fc7-112">Asiakas (organisaatio)</span><span class="sxs-lookup"><span data-stu-id="29fc7-112">Customer (Organization)</span></span>

<span data-ttu-id="29fc7-113">Asiakkaan suoritusjärjestys on:</span><span class="sxs-lookup"><span data-stu-id="29fc7-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="29fc7-114">Yhteyshenkilö (henkilö)</span><span class="sxs-lookup"><span data-stu-id="29fc7-114">Contact (Person)</span></span>

<span data-ttu-id="29fc7-115">Yhteyshenkilön suoritusjärjestys on:</span><span class="sxs-lookup"><span data-stu-id="29fc7-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
