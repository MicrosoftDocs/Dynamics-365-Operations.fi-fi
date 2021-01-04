---
title: Yritysten välisten tilausten suodattaminen Tilausten ja Tilausrivien synkronoinnin välttämiseksi
description: Tässä aiheessa kerrotaan, kuinka yritysten välisiä tilauksia suodatetaan Tilausten ja Tilausrivien synkronoinnin välttämiseksi.
author: negudava
manager: tfehr
ms.date: 11/09/2020
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
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701030"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>Yritysten välisten tilausten suodattaminen Tilausten ja Tilausrivien synkronoinnin välttämiseksi

[!include [banner](../../includes/banner.md)]

Voit suodattaa yritysten välisiä tilauksia **Tilausten** ja **Tilausrivien** entiteettien synkronoinnin välttämiseksi. Joissakin tapauksissa yritysten väliset tilaustiedot eivät ole tarpeen Customer Engagement -sovelluksessa.

Kutakin vakiomuotoista Common Data Service -entiteettiä laajennetaan viittauksella **IntercompanyOrder** -kenttään, ja kaksoiskirjoituskarttoja muokataan niin, että ne viittaavat suodattimien lisäkenttiin. Tuloksena on, että yritysten välisiä tilauksia ei enää synkronoida. Tämä prosessi välttää tarpeettomat tiedot Customer engagement -sovelluksessa.

1. Lisää viittaus kohteeseen **IntercompanyOrder** kohteeseen **CDS Sales Order Headers**. Se täytetään vain yritysten välisille tilauksille. Kenttä **IntercompanyOrder** on käytettävissä taulussa **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Yhdistä välivarastointi kohteeseen, SalesOrderHeader":::
    
2. Kun **CDS Sales Order Headers** on laajennettu, **IntercompanyOrder**-kenttä on käytettävissä yhdistämismäärityksessä. Käytä suodatinta `INTERCOMPANYORDER == ""` kyselymerkkijonona.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Myyntitilausten otsikot, muokkaa kyselyä":::

3. Lisää viittaus **IntercompanyInventTransId** kohteeseen **CDS Sales Order Lines**.  Se täytetään vain yritysten välisille tilauksille. Kenttä **InterCompanyInventTransID** on käytettävissä kohteessa **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Yhdistä välivarastointi kohteeseen, SalesOrderLine":::

4. Kun **CDS Sales Order Lines** on laajennettu, **IntercompanyInventTransId**-kenttä on käytettävissä yhdistämismäärityksessä. Käytä suodatinta `INTERCOMPANYINVENTTRANSID == ""` kyselymerkkijonona.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Myyntitilauksen rivit, muokkaa kyselyä":::

5. Laajenna **Sales Invoice Header V2** ja **Sales Invoice Lines V2** samalla tavalla kuin laajensit Common Data Service -entiteetit vaiheissa 1 ja 2. Lisää sitten suodatinkyselyt. Suodatinmerkkijono kohteelle **Sales Invoice Header V2** on `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`. Suodatinmerkkijono kohteelle **Sales Invoice Lines V2** on `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Yhdistä välivarastointi kohteeseen, Myyntilaskun otsikot":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Myyntilaskun otsikot, muokkaa kyselyä":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Myyntilaskun rivit, muokkaa kyselyä":::

6. **Tarjoukset**-entiteetillä ei ole yritysten välistä suhdetta. Jos joku luo tarjouksen jollekin yritysten väliselle asiakkaallesi, voit sijoittaa kaikki nämä asiakkaat yhteen asiakasryhmään käyttämällä **CustGroup**-kenttää.  Otsikkoa ja rivejä voidaan laajentaa lisäämällä **CustGroup**-kenttä ja valitsemalla sitten suodata, jotta tätä ryhmää ei oteta mukaan.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Yhdistä välivarastointi kohteeseen, Myyntitarjouksen otsikko":::

7. Kun olet laajentanut **Tarjoukset**-entiteettiä, suodata käyttämällä kyselymerkkijonona merkkijonoa `CUSTGROUP !=  "<company>"` .

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Myynt tarjouksen otsikko, muokkaa kyselyä":::
