---
title: RCS-parannettu suodatus RCS:ssä/yleisessä tietovarastossa
description: Tässä ohjeaiheessa kuvataan parannetut suodatusominaisuudet RSC:n yleiselle tietovarastolle. Ominaisuuksia on parannettu niin, että ne sisältävät lisäsuodattimia.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1913b661c46af5e34da1a2939cb2a5d5b4e46411
ms.sourcegitcommit: 7df49a85de484d013518217ba8ada6c61da4b6e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/24/2020
ms.locfileid: "3287936"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="bdbd6-103">RCS-parannetut suodatusvaihtoehdot konfiguraatioiden löytämiseksi RCS:stä/yleisestä tietovarastosta</span><span class="sxs-lookup"><span data-stu-id="bdbd6-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bdbd6-104">Tässä ohjeaiheessa kuvataan parannetut suodatusominaisuudet RSC:n (Regulatory Configuration Services) yleiselle tietovarastolle. Ominaisuuksia on parannettu niin, että ne sisältävät kyvyn suodattaa seuraavilla kriteereillä:</span><span class="sxs-lookup"><span data-stu-id="bdbd6-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="bdbd6-105">**Maa/alue** - Perustuu ISO-maakoodeihin</span><span class="sxs-lookup"><span data-stu-id="bdbd6-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="bdbd6-106">**Tunnisteet** tyypit:</span><span class="sxs-lookup"><span data-stu-id="bdbd6-106">**Tags** types for:</span></span>
  - <span data-ttu-id="bdbd6-107">Toiminnallinen alue</span><span class="sxs-lookup"><span data-stu-id="bdbd6-107">Functional area</span></span>
  - <span data-ttu-id="bdbd6-108">Ominaisuusalue</span><span class="sxs-lookup"><span data-stu-id="bdbd6-108">Feature area</span></span>
  - <span data-ttu-id="bdbd6-109">Toimiala</span><span class="sxs-lookup"><span data-stu-id="bdbd6-109">Industry</span></span> 
  - <span data-ttu-id="bdbd6-110">Liiketoiminta-asiakirja</span><span class="sxs-lookup"><span data-stu-id="bdbd6-110">Business document</span></span> 

<span data-ttu-id="bdbd6-111">Tehdäksesi helpommaksi löytää tiettyjä tai toisiinsa liittyviä konfiguraatioita, voit käyttää suodattimia joko yksitellen tai ryhminä.</span><span class="sxs-lookup"><span data-stu-id="bdbd6-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="bdbd6-112">Jos esimerkiksi haluat löytää yhden tyyppisiä konfiguroitavissa olevia liiketoiminta-asiakirjoja, jotka liittyvät toimittajalaskuihin, voit käyttää **Liiketoiminta-asiakirjatyyppi**-suodatinta kyseisen asiakirjatyypin etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="bdbd6-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="bdbd6-113">[![Yleisen tietovaraston suodatusosa](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="bdbd6-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="bdbd6-114">Voit tarkentaa hakua valitsemalla tiedostotyypin, esimerkiksi toimittajan lasku ja valitsemalla sitten **Käytä suodatinta**.</span><span class="sxs-lookup"><span data-stu-id="bdbd6-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="bdbd6-115">Seuraavassa esimerkissä ovat tulokset, kun suodatetaan **Liiketoiminta-asiakirjan tyyppi**, kun asiakirjatyyppi on lisätty.</span><span class="sxs-lookup"><span data-stu-id="bdbd6-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="bdbd6-116">[![Kohdistettu suodatin ja liiketoiminta-asiakirjan tyypin tuonti](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="bdbd6-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="bdbd6-117">Suodatetut tulokset voidaan tuoda käyttäjien RCS-arkistoon tai Dynamics 365 Finance -ympäristöön joko yksittäin tai osana.</span><span class="sxs-lookup"><span data-stu-id="bdbd6-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="bdbd6-118">Voit tehdä tämän valitsemalla konfiguraatioryhmän ja valitsemalla **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="bdbd6-118">To do this, select the group of configurations, and click **Import**.</span></span>
