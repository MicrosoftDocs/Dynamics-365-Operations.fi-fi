---
title: Konsernin sisäisten tilausten suodattaminen tilausten ja tilausrivien synkronoinnin välttämiseksi
description: Tässä artikkelissa käsitellään konsernin sisäisten tilausten suodattamista niin, ettei Tilaukset- ja Tilausrivit-yksiköitä synkronoida.
author: negudava
ms.date: 11/09/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: negudava
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f5b7831e103aaa219394099b79537bf0842d9be8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289277"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>Konsernin sisäisten tilausten suodattaminen tilausten ja tilausrivien synkronoinnin välttämiseksi

[!include [banner](../../includes/banner.md)]

Konsernin sisäiset tilaukset voidaan suodattaa siten, ettei **Tilaukset** ja **Tilausrivit**-tauluja synkronoida. Joissakin skenaarioissa konsernin sisäisiä tilaustietoja ei tarvita asiakkaan aktivointisovelluksessa.

Kutakin Dataverse-vakiotaulua laajennetaan viittauksilla **IntercompanyOrder**-sarakkeisiin, ja kaksoiskirjoitusmäärityksiä muokataan siten, että ne viittaavat suodattimien lisäsarakkeisiin. Tämän vuoksi konsernin sisäisiä tilauksia ei enää synkronoida. Tämä prosessi auttaa estämään tarpeettomat tiedot asiakkaiden aktivointisovelluksessa.

1. **CDS myyntitilauksen otsikot** -taulu voidaan laajentaa lisäämällä viittaus **IntercompanyOrder**-sarakkeeseen. Tämä sarake täytetään vain konsernin sisäisissä tilauksissa. **IntercompanyOrder**-sarake on käytettävissä **SalesTable**-taulussa.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="CDS-myyntitilauksen otsikoiden Yhdistä väliaikainen alue kohteeseen -sivu.":::

2. Kun **CDS-myyntitilauksen otsikot** on laajennettu, **IntercompanyOrder**-sarake on käytettävissä yhdistämismäärityksessä. Käytä suodatinta, jossa on `INTERCOMPANYORDER == ""` kyselymerkkijonona.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="CDS-myyntitilauksen otsikoiden Muokkaa kyselyä -valintaikkuna.":::

3. **CDS-myyntitilausrivit**-taulua voidaan laajentaa lisäämällä viittaus **IntercompanyInventTransId**-sarakkeeseen. Tämä sarake täytetään vain konsernin sisäisissä tilauksissa. **InterCompanyInventTransId**-sarake on käytettävissä **SalesLine**-taulussa.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="CDS-myyntitilausrivin Yhdistä väliaikainen alue kohteeseen -sivu.":::

4. Kun **CDS-myyntitilausrivit** on laajennettu, **IntercompanyInventTransId**-sarake on käytettävissä yhdistämismäärityksessä. Käytä suodatinta, jossa on `INTERCOMPANYINVENTTRANSID == ""` kyselymerkkijonona.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="CDS-myyntitilausrivien Muokkaa kyselyä -valintaikkuna.":::

5. Laajenna **Myyntilaskun otsikko V2** -taulu ja lisää suodatinkysely toistamalla vaiheet 1 ja 2. Käytä tässä tapauksessa suodatinta, jossa `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` on kyselymerkkijonona.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Myyntilaskun otsikko V2:n Yhdistä väliaikainen alue kohteeseen -sivu.":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Myyntilaskun otsikko V2:n Muokkaa kyselyä -valintaikkuna.":::

6. Laajenna **Myyntilaskurivit V2** -taulu ja lisää suodatinkysely toistamalla vaiheet 3 ja 4. Käytä tässä tapauksessa suodatinta, jossa `INTERCOMPANYINVENTTRANSID == ""` on kyselymerkkijonona.

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Myyntilaskun rivit V2:n Muokkaa kyselyä -valintaikkuna.":::

7. **Tarjoukset**-taulussa ei ole yritysten välistä suhdetta. Jos joku luo tarjouksen jollekin konsernin sisäiselle asiakkaalle, kaikki kyseiset asiakkaat voidaan sijoittaa yhteen asiakasryhmään käyttämällä **CustGroup**-saraketta. Otsikkoa ja rivejä voidaan laajentaa lisäämällä **CustGroup**-sarake ja tekemällä sitten suodatuksen, joka ei sisällä kyseistä ryhmää.

    :::image type="content" source="media/filter-cust-group.png" alt-text="CDS-myyntitarjouksen otsikon Yhdistä väliaikainen alue kohteeseen -sivu.":::

8. Kun **Tarjoukset** on laajennettu, käytä suodatinta, jossa on `CUSTGROUP != "<company>"` kyselymerkkijonona.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="CDS-myyntitarjouksen otsikon Muokkaa kyselyä -valintaikkuna.":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
