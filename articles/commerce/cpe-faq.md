---
title: Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset
description: Tässä aiheessa on vastauksia Microsoft Dynamics 365 Commercen arviointiympäristön usein kysyttyihin kysymyksiin.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 241853c12c5b6a7fdbd1cf7353b4274f4dd99cc1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213887"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="50784-103">Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="50784-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="50784-104">Tässä aiheessa on vastauksia Microsoft Dynamics 365 Commercen arviointiympäristön usein kysyttyihin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="50784-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="50784-105">**Voiko Commercen arviointiympäristöä käyttää sähköisen kaupankäynnin kaupassa asiakkaille, jotka tällä hetkellä käyttävät Retailia?**</span><span class="sxs-lookup"><span data-stu-id="50784-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="50784-106">Nro</span><span class="sxs-lookup"><span data-stu-id="50784-106">No.</span></span> <span data-ttu-id="50784-107">Commercen arviointiympäristö on tarkoitettu vain arviointiin.</span><span class="sxs-lookup"><span data-stu-id="50784-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="50784-108">Jos tarvitset ympäristöä asiakkaalle, joka toteuttaa vähittäismyynnin, ota yhteyttä Microsoftiin.</span><span class="sxs-lookup"><span data-stu-id="50784-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="50784-109">**Voiko Commercen arviointiympäristöä käyttää sähköisen kaupankäynnin ominaisuuksien valmisteluun nykyisen Retailin toteutuksessa käytetyn sovelluksen tai ympäristön ohella?**</span><span class="sxs-lookup"><span data-stu-id="50784-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="50784-110">Ei (yleensä).</span><span class="sxs-lookup"><span data-stu-id="50784-110">No (mostly).</span></span> <span data-ttu-id="50784-111">Commercen arviointiosat ovat saatavana vain ympäristöissä, jotka vastaavat edellytyksissä ja valmisteluoppaassa mainittuja määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="50784-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="50784-112">Lisäksi vaadittuja perusesittelytietoja ei ole ympäristöissä, jotka otettiin käyttöön alkuperäisessä julkaisussa, joka on aikaisempi kuin versio 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="50784-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="50784-113">**Mitä kustannuksia liittyy Commercen arviointiympäristön käyttöönottoon Microsoft Azuressa Microsoft Dynamics Lifecycle Servicesin (LCS) kautta?**</span><span class="sxs-lookup"><span data-stu-id="50784-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="50784-114">Perinteistä Dynamics 365 Financen, Dynamics 365 Supply Chain Managementin ja Dynamics 365 Commercen pääkonttorin esittely-ympäristöä (virtuaalikone \[VM\]) isännöidään Azure-tilauksessa.</span><span class="sxs-lookup"><span data-stu-id="50784-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="50784-115">Voit käyttää [Azure hinnoittelulaskuria](https://azure.microsoft.com/pricing/calculator/) tämän kustannuksen arvioimiseen.</span><span class="sxs-lookup"><span data-stu-id="50784-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="50784-116">Muut osat, kuten Commerce Scale Unit, Commercen sivustonmuodostin ja sähköinen kaupankäyntisivusto, ovat saatavana Microsoftin isännöimänä ohjelmisto palveluna (SaaS) -vaihtoehtona.</span><span class="sxs-lookup"><span data-stu-id="50784-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="50784-117">**Mitkä Azure-maita tuetaan tällä hetkellä Commercen arviointiympäristössä?**</span><span class="sxs-lookup"><span data-stu-id="50784-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="50784-118">Commercen arviointiympäristö voidaan ottaa käyttöön vain Pohjois-Amerikan maantieteellisellä alueella.</span><span class="sxs-lookup"><span data-stu-id="50784-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="50784-119">**Onko olemassa ladattava virtuaalinen kovalevy (VHD), jolla on täydellinen OneBox Virtual Machinen (VM) vaihtoehto?**</span><span class="sxs-lookup"><span data-stu-id="50784-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="50784-120">Dynamics 365 Commerce ja Commerce Scale Unit ovat saatavana pilvessä käytettävänä ohjelmisto palveluna (SaaS) -versiona.</span><span class="sxs-lookup"><span data-stu-id="50784-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="50784-121">**Kuinka kauan Commerce arviointiympäristöä voi käyttää?**</span><span class="sxs-lookup"><span data-stu-id="50784-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="50784-122">Commerce arviointiympäristöllä on 30 päivän aikaraja siitä päivästä, jolloin SaaS-osat, kuten Commerce Scale Unit, Commercen sivustonmuodostin ja oma sähköinen kaupankäyntisivusto, on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="50784-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="50784-123">**Voinko pidentää Commercen arviointiympäristön aikarajaa?**</span><span class="sxs-lookup"><span data-stu-id="50784-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="50784-124">Aikarajan pidennys on poikkeus, jota harkitaan tapauskohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="50784-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="50784-125">Ota tässä tapauksessa yhteys Microsoft-kumppaniin.</span><span class="sxs-lookup"><span data-stu-id="50784-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="50784-126">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="50784-126">Additional resources</span></span>

[<span data-ttu-id="50784-127">Dynamics 365 Commerce -arviointiympäristön yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="50784-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="50784-128">Dynamics 365 Commerce -arviointiympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="50784-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="50784-129">Dynamics 365 Commerce -arviointiympäristön määritykset</span><span class="sxs-lookup"><span data-stu-id="50784-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="50784-130">BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä</span><span class="sxs-lookup"><span data-stu-id="50784-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="50784-131">Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset</span><span class="sxs-lookup"><span data-stu-id="50784-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]