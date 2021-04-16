---
title: Tuoterakenneversion hajottaminen
description: Tässä artikkelissa kuvataan pääsuunnittelun skenaario, johon liittyy tuoterakenteen version hajotus.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 367b662a43b3c3255632f20aeb821b973b04d890
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833590"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="fde61-103">Tuoterakenneversion hajottaminen</span><span class="sxs-lookup"><span data-stu-id="fde61-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fde61-104">Tässä artikkelissa kuvataan pääsuunnittelun skenaario, johon liittyy tuoterakenteen version hajotus.</span><span class="sxs-lookup"><span data-stu-id="fde61-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="fde61-105">Tuoterakenneversion kysynnän hajotus luo kysynnän kullekin tuoterakennerivin nimikkeelle määritetyssä toimipaikassa ja mahdollisesti tietyssä varastossa.</span><span class="sxs-lookup"><span data-stu-id="fde61-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="fde61-106">Toimipaikkakohtaisen tuoterakenteen kullekin tuoterakenneriville voidaan määrittää tietty varasto.</span><span class="sxs-lookup"><span data-stu-id="fde61-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="fde61-107">Lisäksi kunkin tuoterakennerivin nimikkeen dimensioasetukset määrittävät, onko varasto tarpeen.</span><span class="sxs-lookup"><span data-stu-id="fde61-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="fde61-108">Kunkin tuoterakennerivin nimikkeen tuloksena syntyvä kysyntä muodostaa jatkossa aloituspisteen lisäkysynnän hajotukselle.</span><span class="sxs-lookup"><span data-stu-id="fde61-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="fde61-109">Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:</span><span class="sxs-lookup"><span data-stu-id="fde61-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="fde61-110">Toimipaikkadimensio on pakollinen ja se on määritettävä tarvetapahtumalle.</span><span class="sxs-lookup"><span data-stu-id="fde61-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="fde61-111">Toimipaikkadimensio on yhdenmukainen.</span><span class="sxs-lookup"><span data-stu-id="fde61-111">The site dimension is consistent.</span></span> <span data-ttu-id="fde61-112">Näin ollen alemman tason tarpeen toimipaikka on sama kuin alkuperäisen tarvetapahtuman toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="fde61-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="fde61-113">Seuraava kuva ilmaisee, miten pääsuunnittelun kysynnän hajotus etenee.</span><span class="sxs-lookup"><span data-stu-id="fde61-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Kysynnän hajottaminen tuoterakenneversion avulla](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="fde61-115">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fde61-115">Additional resources</span></span>
--------

[<span data-ttu-id="fde61-116">Tuoterakenneversion määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fde61-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="fde61-117">Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="fde61-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]