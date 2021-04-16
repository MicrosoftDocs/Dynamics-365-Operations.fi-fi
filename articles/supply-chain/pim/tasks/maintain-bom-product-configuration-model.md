---
title: Ylläpidä tuotemääritysmallin tuoterakennetta
description: Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49aa17aa376f8536e9d2290292f877d314c2c078
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818010"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="a2799-103">Ylläpidä tuotemääritysmallin tuoterakennetta</span><span class="sxs-lookup"><span data-stu-id="a2799-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a2799-104">Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin.</span><span class="sxs-lookup"><span data-stu-id="a2799-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="a2799-105">Tämä menettely luodaan käyttämällä USMF-demoyrityksen Korkealaatuinen kaiutin -mallia.</span><span class="sxs-lookup"><span data-stu-id="a2799-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="a2799-106">Lisää tuoterakennerivi</span><span class="sxs-lookup"><span data-stu-id="a2799-106">Add a BOM line</span></span>
1. <span data-ttu-id="a2799-107">Valitse Tuotevarianttimallin määritys.</span><span class="sxs-lookup"><span data-stu-id="a2799-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="a2799-108">Valitse Tuotekonfiguraation mallit.</span><span class="sxs-lookup"><span data-stu-id="a2799-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="a2799-109">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a2799-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a2799-110">Valitse tähän menettelyyn korkealaatuinen kaiutin.</span><span class="sxs-lookup"><span data-stu-id="a2799-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="a2799-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a2799-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a2799-112">Laajenna Tuoterakennerivi-osa.</span><span class="sxs-lookup"><span data-stu-id="a2799-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="a2799-113">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="a2799-113">Click Add.</span></span>
7. <span data-ttu-id="a2799-114">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a2799-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="a2799-115">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a2799-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="a2799-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a2799-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="a2799-117">Lisää tuoterakennerivin tiedot</span><span class="sxs-lookup"><span data-stu-id="a2799-117">Add BOM line details</span></span>
1. <span data-ttu-id="a2799-118">Valitse Tuoterakennerivin tiedot.</span><span class="sxs-lookup"><span data-stu-id="a2799-118">Click BOM line details.</span></span>
2. <span data-ttu-id="a2799-119">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a2799-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a2799-120">Valitse esimerkiksi nimike M0055.</span><span class="sxs-lookup"><span data-stu-id="a2799-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="a2799-121">Voit valita kunkin tuoterakennerivin ominaisuuden kohdalla, annetaanko sille kiinteä arvo vai yhdistetäänkö se määritteeseen.</span><span class="sxs-lookup"><span data-stu-id="a2799-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="a2799-122">Valitse Määritä-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="a2799-122">Select the Set check box.</span></span>
4. <span data-ttu-id="a2799-123">Valitse Laskenta-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="a2799-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="a2799-124">Laskelma-ominaisuuden määrittäminen arvoksi Kyllä varmistaa, että tuoterakennerivi sisältyy kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="a2799-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="a2799-125">Valitse Asetukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a2799-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="a2799-126">Valitse Määritä-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="a2799-126">Select the Set check box.</span></span>
7. <span data-ttu-id="a2799-127">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a2799-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a2799-128">Määräkenttä määrittää, miten suuri osa nimikkeestä sisällytetään tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="a2799-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="a2799-129">Tämä voisi olla hyvä ehdokas määritteen yhdistämiselle.</span><span class="sxs-lookup"><span data-stu-id="a2799-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="a2799-130">Valitse Dimensio-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a2799-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="a2799-131">Tarkista, onko yksikään tuotedimensio aktiviinen ja onko sillä siksi oltava arvo tai määrite määritettynä.</span><span class="sxs-lookup"><span data-stu-id="a2799-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="a2799-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a2799-132">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]