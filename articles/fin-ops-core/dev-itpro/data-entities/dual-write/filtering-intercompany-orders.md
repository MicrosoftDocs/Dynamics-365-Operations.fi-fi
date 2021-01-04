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
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="54bec-103">Yritysten välisten tilausten suodattaminen Tilausten ja Tilausrivien synkronoinnin välttämiseksi</span><span class="sxs-lookup"><span data-stu-id="54bec-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54bec-104">Voit suodattaa yritysten välisiä tilauksia **Tilausten** ja **Tilausrivien** entiteettien synkronoinnin välttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="54bec-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="54bec-105">Joissakin tapauksissa yritysten väliset tilaustiedot eivät ole tarpeen Customer Engagement -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="54bec-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="54bec-106">Kutakin vakiomuotoista Common Data Service -entiteettiä laajennetaan viittauksella **IntercompanyOrder** -kenttään, ja kaksoiskirjoituskarttoja muokataan niin, että ne viittaavat suodattimien lisäkenttiin.</span><span class="sxs-lookup"><span data-stu-id="54bec-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="54bec-107">Tuloksena on, että yritysten välisiä tilauksia ei enää synkronoida.</span><span class="sxs-lookup"><span data-stu-id="54bec-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="54bec-108">Tämä prosessi välttää tarpeettomat tiedot Customer engagement -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="54bec-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="54bec-109">Lisää viittaus kohteeseen **IntercompanyOrder** kohteeseen **CDS Sales Order Headers**.</span><span class="sxs-lookup"><span data-stu-id="54bec-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="54bec-110">Se täytetään vain yritysten välisille tilauksille.</span><span class="sxs-lookup"><span data-stu-id="54bec-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="54bec-111">Kenttä **IntercompanyOrder** on käytettävissä taulussa **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="54bec-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Yhdistä välivarastointi kohteeseen, SalesOrderHeader":::
    
2. <span data-ttu-id="54bec-113">Kun **CDS Sales Order Headers** on laajennettu, **IntercompanyOrder**-kenttä on käytettävissä yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="54bec-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="54bec-114">Käytä suodatinta `INTERCOMPANYORDER == ""` kyselymerkkijonona.</span><span class="sxs-lookup"><span data-stu-id="54bec-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Myyntitilausten otsikot, muokkaa kyselyä":::

3. <span data-ttu-id="54bec-116">Lisää viittaus **IntercompanyInventTransId** kohteeseen **CDS Sales Order Lines**.</span><span class="sxs-lookup"><span data-stu-id="54bec-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="54bec-117">Se täytetään vain yritysten välisille tilauksille.</span><span class="sxs-lookup"><span data-stu-id="54bec-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="54bec-118">Kenttä **InterCompanyInventTransID** on käytettävissä kohteessa **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="54bec-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Yhdistä välivarastointi kohteeseen, SalesOrderLine":::

4. <span data-ttu-id="54bec-120">Kun **CDS Sales Order Lines** on laajennettu, **IntercompanyInventTransId**-kenttä on käytettävissä yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="54bec-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="54bec-121">Käytä suodatinta `INTERCOMPANYINVENTTRANSID == ""` kyselymerkkijonona.</span><span class="sxs-lookup"><span data-stu-id="54bec-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Myyntitilauksen rivit, muokkaa kyselyä":::

5. <span data-ttu-id="54bec-123">Laajenna **Sales Invoice Header V2** ja **Sales Invoice Lines V2** samalla tavalla kuin laajensit Common Data Service -entiteetit vaiheissa 1 ja 2.</span><span class="sxs-lookup"><span data-stu-id="54bec-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="54bec-124">Lisää sitten suodatinkyselyt.</span><span class="sxs-lookup"><span data-stu-id="54bec-124">Then add the filter queries.</span></span> <span data-ttu-id="54bec-125">Suodatinmerkkijono kohteelle **Sales Invoice Header V2** on `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span><span class="sxs-lookup"><span data-stu-id="54bec-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="54bec-126">Suodatinmerkkijono kohteelle **Sales Invoice Lines V2** on `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="54bec-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Yhdistä välivarastointi kohteeseen, Myyntilaskun otsikot":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Myyntilaskun otsikot, muokkaa kyselyä":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Myyntilaskun rivit, muokkaa kyselyä":::

6. <span data-ttu-id="54bec-130">**Tarjoukset**-entiteetillä ei ole yritysten välistä suhdetta.</span><span class="sxs-lookup"><span data-stu-id="54bec-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="54bec-131">Jos joku luo tarjouksen jollekin yritysten väliselle asiakkaallesi, voit sijoittaa kaikki nämä asiakkaat yhteen asiakasryhmään käyttämällä **CustGroup**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="54bec-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="54bec-132">Otsikkoa ja rivejä voidaan laajentaa lisäämällä **CustGroup**-kenttä ja valitsemalla sitten suodata, jotta tätä ryhmää ei oteta mukaan.</span><span class="sxs-lookup"><span data-stu-id="54bec-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Yhdistä välivarastointi kohteeseen, Myyntitarjouksen otsikko":::

7. <span data-ttu-id="54bec-134">Kun olet laajentanut **Tarjoukset**-entiteettiä, suodata käyttämällä kyselymerkkijonona merkkijonoa `CUSTGROUP !=  "<company>"` .</span><span class="sxs-lookup"><span data-stu-id="54bec-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Myynt tarjouksen otsikko, muokkaa kyselyä":::
