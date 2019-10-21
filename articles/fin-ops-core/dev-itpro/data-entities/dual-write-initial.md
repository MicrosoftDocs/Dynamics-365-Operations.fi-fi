---
title: Finance and Operations -sovellusten ja Common Data Servicen alkuperäisen synkronoinnin toteuttamisjärjestys
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
ms.openlocfilehash: 3110cb809558d168e9d97f640701b249caf73f6c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184505"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a>Finance and Operations -sovellusten ja Common Data Servicen alkuperäisen synkronoinnin toteuttamisjärjestys

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Ennen kuin käytät tietojen integrointia, sinun on luotava asiakkaille, toimittajille ja yhteyshenkilöille tarvittavat alkuperäiset tiedot. Haluat esimerkiksi luoda uuden **Toimittajaryhmä**-nimikkeen ja määrittää sen **Maksuehdot**-arvoksi **Net30**. Varmista tässä tapauksessa ennen **Toimittajaryhmä**-nimikkeen luomisen yrittämistä, että **Net30** on sekä sovelluksessa että Common Data Servicessä. (Microsoft julkaisee tulevaisuudessa kaksoiskirjoitusalustan toiminnallisuuden nimeltä Alkusynkronointi. Tämä toiminto synkronoi tiedot kerran sovelluksen ja Common Data Servicen välillä osana kaksoiskirjoituksen määritystä.)

> [!TIP]
> Microsoft julkaisee kaksoiskirjoituksen yhdistämismääritykset kaikille viitetiedoille, mukaan lukien **Maksuehdot** (maksuehdot). Jos sinulla on jo alkuperäiset tiedot yhdessä järjestelmässä, tietueen pieni päivitystoiminto voi laukaista kaksoiskirjoitustoiminnon kyseiseen tietueeseen.

Sinun on noudatettava seuraavaa järjestystä ja varmistettava, että alkuperäiset tiedot ovat käytettävissä sekä sovelluksessa että Common Data Servicessä.

## <a name="vendor"></a>Toimittaja

Tässä on **Toimittaja**-kohteen suoritusjärjestys:

1. Toimittajaryhmä

    1. Maksuehto

        1. Maksupäivä ja -rivit
        2. Maksusuunnitelma

2. Toimittajan maksutapa

## <a name="customer-organization"></a>Asiakas (organisaatio)

Tässä on **Asiakas**-kohteen suoritusjärjestys:

1. Asiakasryhmä

    1. Maksuehto

        1. Maksupäivä ja -rivit
        2. Maksu 

2. Asiakkaan maksutapa

## <a name="contact-person"></a>Yhteyshenkilö (henkilö)

Tässä on **Yhteyshenkilö**-kohteen suoritusjärjestys:

1. Asiakas
2. Toimittaja
