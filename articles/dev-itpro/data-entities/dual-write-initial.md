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
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>Finance and Operationsin ja Common Data Servicen alkuperäisen sykronoinnin toteuttamisjärjestys

Ennen kuin käytät tietojen integrointia, sinun on luotava asiakkaille, toimittajille ja yhteyshenkilöille tarvittavat alkuperäiset tiedot. Jos haluat esimerkiksi luoda uuden **toimittajaryhmän** nimikkeen ja määrittää sen **maksuehdoksi** **Net30**-arvon, sinun on varmistettava ennen kuin yrität luoda **toimittajaryhmän** nimikettä, että **Net30** on olemassa sekä Finance and Operationsissa että Common Data Servicessa. (Tulevaisuudessa julkaisemme kaksoiskirjoitusalustan toiminnallisuuden nimeltä **Alkusynronointi**. Se tekee tietojen kertasynkronoinnin Finance and Operationsin ja Common Data Servicen välillä osana kaksoiskirjoituksen määritystä.)

Vinkkejä: Julkaisemme kaksoiskirjoituksen yhdistämismääritykset kaikille viitetiedoille, mukaan lukien **Maksuehdot** (maksuehdot). Jos sinulla on jo alkuperäiset tiedot yhdessä järjestelmässä, tietueen pieni päivitystoiminto voi laukaista kaksoiskirjoitustoiminnon kyseiseen tietueeseen. 

Sinun on noudatettava seuraavaa järjestystä ja varmistettava, että alkuperäiset tiedot ovat käytettävissä sekä Finance and Operationsissa että Common Data Servicessa.   

## <a name="vendor"></a>Toimittaja

Toimittajan suoritusjärjestys on:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>Asiakas (organisaatio)

Asiakkaan suoritusjärjestys on:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>Yhteyshenkilö (henkilö)

Yhteyshenkilön suoritusjärjestys on:

```
Customer
Vendor               
```
