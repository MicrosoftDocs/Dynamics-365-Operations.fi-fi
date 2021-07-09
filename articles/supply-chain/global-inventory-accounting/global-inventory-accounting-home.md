---
title: Yleisen varastokirjanpidon aloitussivu
description: Tämä ohjeaihe on Microsoft Dynamics 365 Supply Chain Management yleisen varastokirjanpidon lisäosan aloitussivu.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f4434afb847104a18a2a2a2f07a7060cf01de816
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273147"
---
# <a name="global-inventory-accounting-home-page"></a><span data-ttu-id="cf9fa-103">Yleisen varastokirjanpidon aloitussivu</span><span class="sxs-lookup"><span data-stu-id="cf9fa-103">Global Inventory Accounting home page</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="cf9fa-104">Viranomaiset painostavat kansainvälisiä organisaatioita yhä enemmän noudattamaan paikallisia ja maailmanlaajuisia kirjanpitostandardeja.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-104">International organizations are under increasing pressure from authorities to comply with local and global accounting standards.</span></span> <span data-ttu-id="cf9fa-105">Varaston uudelleenarvostus on tärkeä rooli yhteensopivuuden varmistamisessa.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-105">The valuation of inventory plays a significant role in ensuring compliance.</span></span> <span data-ttu-id="cf9fa-106">Microsoft Dynamics 365 Supply Chain Managementin yleinen varastokirjanpitolisäosa tarjoaa kattavan ratkaisun, jonka avulla organisaatiot (erityisesti kansainväliset organisaatiot) voivat käyttää useita kustannuslaskennan kirjanpitoja varastokirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-106">The Global Inventory Accounting Add-in for Microsoft Dynamics 365 Supply Chain Management provides a comprehensive solution that enables organizations (especially international organizations) to use multiple costing ledgers to do inventory accounting.</span></span> <span data-ttu-id="cf9fa-107">Siksi organisaatiot voivat noudattaa useita kirjanpidon standardeja ja sisäisen hallinnan kirjanpitoa samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-107">Therefore, those organizations can comply with multiple accounting standards and internal management accounting at the same time.</span></span>

<span data-ttu-id="cf9fa-108">Yleinen varastolaskenta -toiminnolla voit ottaa varaston huomioon useissa esityksissä käyttämällä arvostusmenetelmää (standardikustannus, keskiarvo tai tietty tunnus) ja valitun kirjanpitovaluutan instanssia kohti.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-108">Global Inventory Accounting lets you account inventory in multiple representations by applying the appropriate valuation method (standard cost, average, or specific identification) and the selected accounting currency per instance.</span></span> <span data-ttu-id="cf9fa-109">Yleisen varastolaskennan avulla organisaatiot voivat raportoida varastotiliotteita ja alareskontran kirjanpidon arvoja (kutsutaan myös varastosaldoksi ja myytyjen tuotteiden kustannuksiksi), joita kutsutaan usein arvostusvaluutaksi ja/tai valuuttaksi.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-109">Global Inventory Accounting enables organizations to report inventory statements and subledger accounting values (also known as the inventory balance and the cost of goods sold) in what is often referred to as dual valuation and/or dual currency.</span></span>

<span data-ttu-id="cf9fa-110">Varastokirjanpito tehdään yksittäisissä kirjanpidoissa.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-110">Inventory accounting is done in individual ledgers.</span></span> <span data-ttu-id="cf9fa-111">Kullekin organisaation yritykselle voidaan tarvittaessa luoda useita yleisiä varastokirjanpitoja.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-111">Several Global Inventory Accounting ledgers can be created for each legal entity in an organization, as required.</span></span> <span data-ttu-id="cf9fa-112">Näin voidaan saada useita varastoesityksiä.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-112">Therefore, multiple inventory representations can be obtained.</span></span> <span data-ttu-id="cf9fa-113">Kaikki yritykselle kirjatut tiedostot (kuten ostotilaukset, myyntitilaukset ja siirtotilaukset) on tilitetty kaikissa tähän yritykseen liitetyissä kustannuslaskelmakirjanpidoissa.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-113">All documents that are posted in a legal entity (such as purchase orders, sales orders, and transfer orders) will be accounted in all the costing ledgers that are associated with that legal entity.</span></span>

<span data-ttu-id="cf9fa-114">Yleinen varastokirjanpito määritetään seuraavien elementtien yhdistelmällä:</span><span class="sxs-lookup"><span data-stu-id="cf9fa-114">A Global Inventory Accounting ledger is defined by a combination of the following elements:</span></span>

- <span data-ttu-id="cf9fa-115">Kalenteri</span><span class="sxs-lookup"><span data-stu-id="cf9fa-115">Calendar</span></span>
- <span data-ttu-id="cf9fa-116">Valuutta</span><span class="sxs-lookup"><span data-stu-id="cf9fa-116">Currency</span></span>
- <span data-ttu-id="cf9fa-117">Vaihtokurssin taulukko</span><span class="sxs-lookup"><span data-stu-id="cf9fa-117">Exchange rate table</span></span>
- <span data-ttu-id="cf9fa-118">Käytäntö</span><span class="sxs-lookup"><span data-stu-id="cf9fa-118">Convention</span></span>

<span data-ttu-id="cf9fa-119">Tämä käytäntö on kokoelma varastokirjanpitokäytäntöjä, jotka voidaan liittää yhteen tai useampiin kirjanpitoihin.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-119">A convention is a collection of inventory accounting policies that can be associated with one or more ledgers.</span></span> <span data-ttu-id="cf9fa-120">Käytäntöjen avulla voit jakaa organisaation yleiset käytännöt.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-120">Conventions let you share a common set of policies within your organization.</span></span>

## <a name="availability"></a><span data-ttu-id="cf9fa-121">Käytettävyys</span><span class="sxs-lookup"><span data-stu-id="cf9fa-121">Availability</span></span>

<span data-ttu-id="cf9fa-122">Yleinen varastokirjanpito on tällä hetkellä saatavilla seuraavilla Azuren maantieteellinen alueilla:</span><span class="sxs-lookup"><span data-stu-id="cf9fa-122">Global Inventory Accounting is currently available in the following Azure geographic regions:</span></span>

- <span data-ttu-id="cf9fa-123">Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="cf9fa-123">United States</span></span>
- <span data-ttu-id="cf9fa-124">Eurooppa</span><span class="sxs-lookup"><span data-stu-id="cf9fa-124">Europe</span></span>
- <span data-ttu-id="cf9fa-125">Iso-Britannia</span><span class="sxs-lookup"><span data-stu-id="cf9fa-125">United Kingdom</span></span>
- <span data-ttu-id="cf9fa-126">Australia</span><span class="sxs-lookup"><span data-stu-id="cf9fa-126">Australia</span></span>
- <span data-ttu-id="cf9fa-127">Kanada</span><span class="sxs-lookup"><span data-stu-id="cf9fa-127">Canada</span></span>

<span data-ttu-id="cf9fa-128">Jos yrität asentaa apuohjelman toiselta maantieteelliseltä alueelta, Microsoft Dynamics Lifecycle Services (LCS) näyttää sanoman, jonka mukaan maantieteellistä aluettasi ei tueta.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-128">If you try to install the add-in from another geographic region, Microsoft Dynamics Lifecycle Services (LCS) will show a message that your geographic region isn't supported.</span></span> <span data-ttu-id="cf9fa-129">Yleinen varastokirjanpito ei tue Supply Chain Managementin paikallista käyttöä.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-129">Global Inventory Accounting doesn't support on-premises deployments of Supply Chain Management.</span></span>

## <a name="licensing"></a><span data-ttu-id="cf9fa-130">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="cf9fa-130">Licensing</span></span>

<span data-ttu-id="cf9fa-131">Yleinen varastokirjanpito on lisensoitu yhdessä Supply Chain Managementin käytettävissä olevien kulujen hallinnan vakiotoimintojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-131">Global Inventory Accounting is licensed together with the standard cost management features available for Supply Chain Management.</span></span> <span data-ttu-id="cf9fa-132">Sinun ei tarvitse ostaa lisäkäyttöoikeutta, jotta voisit käyttää yleistä varastokirjanpitoa.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-132">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>
