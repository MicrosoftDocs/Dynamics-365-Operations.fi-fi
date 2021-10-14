---
title: Varaston käytettävissä olevien tietoentiteettien laajentaminen
description: Tässä ohjeaiheessa on esimerkki siitä, miten laajennettuja kenttiä lisätään INVENTORSITEONHANDENTITY- ja INVENTWAREHOUSEONHANDENTITY-näkymään, jotta käytettävissä olevien varastoentiteettien ominaisuudet voivat toimia laajennusten kanssa.
author: yufeihuang
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8161d951c3296b63476c4e7b527efca163a4f4b3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577693"
---
# <a name="extend-inventory-on-hand-data-entities"></a>Varaston käytettävissä olevien tietoentiteettien laajentaminen

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management tarjoaa [laajennettavuus](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md)-toimintoja, joiden avulla voit [lisätä kenttiä taulukoihin laajennuksen avulla](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md). Tässä ohjeaiheessa on esimerkki siitä, miten laajennettuja kenttiä lisätään `INVENTORSITEONHANDENTITY`- ja `INVENTWAREHOUSEONHANDENTITY`-näkymään, jotta käytettävissä olevien varastoentiteettien ominaisuudet voivat toimia laajennusten kanssa. Lisätietoja tietoentiteeteistä on kohdassa [Tietojen hallinnan yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

> [!NOTE]
> Seuraavassa on luettelo joistakin käytettävissä olevista tietoyksiköistä:
>
> - Käytettävissä oleva varasto toimipaikan mukaan.
> - Käytettävissä oleva varasto toimipaikan mukaan V2
> - Käytettävissä oleva varasto varaston mukaan
> - Käytettävissä oleva varasto varasto v2:n mukaan

Kun olet lisännyt kenttiä tauluihin, joita `inventSiteOnHandView`-näkymä käyttää, sinun on synkronoitava moduuli, jotta tunnisteet tunnistetaan oikein.

1. Laajenna `InventSiteOnHandView`-näkymää lisäämällä laajennuskenttä.
1. Laajenna `InventSiteOnHandAggregatedView`-näkymää laajennuskentillä.
1. Laajenna `InventSiteOnHandAggregatedViewBuilder` viewBuilder -luokkaa muokkaamalla `getExtensionFields()`-menetelmää. Näin voit yhdistää vanhat näkymäkentät uusiin näkymäkenttiin, kun viewBuilder-synkronointi suoritetaan.

Olet lisännyt esimerkiksi seuraavat neljä kenttää `InventTable`-tauluun laajennuksen avulla:

- Mukautettu kenttä 1
- Mukautettu kenttä 2
- Mukautettu kenttä 3
- Mukautettu kenttä 4

Tässä tapauksessa `getExtensionFields()`-menetelmää on muokattava seuraavalla tavalla.

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

Kun olet suorittanut nämä vaiheet, voit laajentaa käytettävissä olevan varaston toimipaikan mukaan sekä varastotiedot varaston tietoihin lisäämällä uudet kentät. Näin varmistat, että laajennetut kentät tunnistetaan ja sisällytetään tietojen siirron aikana, joka käyttää kyseisiä tietokokonaisuuksia.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]