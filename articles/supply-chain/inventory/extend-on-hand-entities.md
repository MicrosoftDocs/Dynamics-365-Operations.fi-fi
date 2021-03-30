---
title: Varaston käytettävissä olevien tietoentiteettien laajentaminen
description: Tässä ohjeaiheessa on esimerkki siitä, miten laajennettuja kenttiä lisätään INVENTORSITEONHANDENTITY- ja INVENTWAREHOUSEONHANDENTITY-näkymään, jotta käytettävissä olevien varastoentiteettien ominaisuudet voivat toimia laajennusten kanssa.
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0f48e424a9ab3349d3c114ecbd01424005b9a9c6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219338"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="5e809-103">Varaston käytettävissä olevien tietoentiteettien laajentaminen</span><span class="sxs-lookup"><span data-stu-id="5e809-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e809-104">Microsoft Dynamics 365 Supply Chain Management tarjoaa [laajennettavuus](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md)-toimintoja, joiden avulla voit [lisätä kenttiä taulukoihin laajennuksen avulla](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span><span class="sxs-lookup"><span data-stu-id="5e809-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span></span> <span data-ttu-id="5e809-105">Tässä ohjeaiheessa on esimerkki siitä, miten laajennettuja kenttiä lisätään `INVENTORSITEONHANDENTITY`- ja `INVENTWAREHOUSEONHANDENTITY`-näkymään, jotta käytettävissä olevien varastoentiteettien ominaisuudet voivat toimia laajennusten kanssa.</span><span class="sxs-lookup"><span data-stu-id="5e809-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="5e809-106">Lisätietoja tietoentiteeteistä on kohdassa [Tietojen hallinnan yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="5e809-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="5e809-107">Seuraavassa on luettelo joistakin käytettävissä olevista tietoyksiköistä:</span><span class="sxs-lookup"><span data-stu-id="5e809-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="5e809-108">Käytettävissä oleva varasto toimipaikan mukaan.</span><span class="sxs-lookup"><span data-stu-id="5e809-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="5e809-109">Käytettävissä oleva varasto toimipaikan mukaan V2</span><span class="sxs-lookup"><span data-stu-id="5e809-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="5e809-110">Käytettävissä oleva varasto varaston mukaan</span><span class="sxs-lookup"><span data-stu-id="5e809-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="5e809-111">Käytettävissä oleva varasto varasto v2:n mukaan</span><span class="sxs-lookup"><span data-stu-id="5e809-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="5e809-112">Kun olet lisännyt kenttiä tauluihin, joita `inventSiteOnHandView`-näkymä käyttää, sinun on synkronoitava moduuli, jotta tunnisteet tunnistetaan oikein.</span><span class="sxs-lookup"><span data-stu-id="5e809-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="5e809-113">Laajenna `InventSiteOnHandView`-näkymää lisäämällä laajennuskenttä.</span><span class="sxs-lookup"><span data-stu-id="5e809-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="5e809-114">Laajenna `InventSiteOnHandAggregatedView`-näkymää laajennuskentillä.</span><span class="sxs-lookup"><span data-stu-id="5e809-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="5e809-115">Laajenna `InventSiteOnHandAggregatedViewBuilder` viewBuilder -luokkaa muokkaamalla `getExtensionFields()`-menetelmää.</span><span class="sxs-lookup"><span data-stu-id="5e809-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="5e809-116">Näin voit yhdistää vanhat näkymäkentät uusiin näkymäkenttiin, kun viewBuilder-synkronointi suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="5e809-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="5e809-117">Olet lisännyt esimerkiksi seuraavat neljä kenttää `InventTable`-tauluun laajennuksen avulla:</span><span class="sxs-lookup"><span data-stu-id="5e809-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="5e809-118">Mukautettu kenttä 1</span><span class="sxs-lookup"><span data-stu-id="5e809-118">Custom field 1</span></span>
- <span data-ttu-id="5e809-119">Mukautettu kenttä 2</span><span class="sxs-lookup"><span data-stu-id="5e809-119">Custom field 2</span></span>
- <span data-ttu-id="5e809-120">Mukautettu kenttä 3</span><span class="sxs-lookup"><span data-stu-id="5e809-120">Custom field 3</span></span>
- <span data-ttu-id="5e809-121">Mukautettu kenttä 4</span><span class="sxs-lookup"><span data-stu-id="5e809-121">Custom field 4</span></span>

<span data-ttu-id="5e809-122">Tässä tapauksessa `getExtensionFields()`-menetelmää on muokattava seuraavalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="5e809-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

<span data-ttu-id="5e809-123">Kun olet suorittanut nämä vaiheet, voit laajentaa käytettävissä olevan varaston toimipaikan mukaan sekä varastotiedot varaston tietoihin lisäämällä uudet kentät.</span><span class="sxs-lookup"><span data-stu-id="5e809-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="5e809-124">Näin varmistat, että laajennetut kentät tunnistetaan ja sisällytetään tietojen siirron aikana, joka käyttää kyseisiä tietokokonaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="5e809-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]