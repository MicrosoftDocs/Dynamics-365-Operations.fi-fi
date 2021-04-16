---
title: Konsernin sisäisten tilausten suodattaminen tilausten ja tilausrivien synkronoinnin välttämiseksi
description: Tässä aiheessa käsitellään konsernin sisäisten tilausten suodattamista niin, ettei Tilaukset- ja Tilausrivit-yksiköitä synkronoida.
author: negudava
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 123427db61782490d348489c23e0eaf5f8b513c9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748638"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="cef58-103">Konsernin sisäisten tilausten suodattaminen tilausten ja tilausrivien synkronoinnin välttämiseksi</span><span class="sxs-lookup"><span data-stu-id="cef58-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cef58-104">Konsernin sisäiset tilaukset voidaan suodattaa siten, ettei **Tilaukset** ja **Tilausrivit**-tauluja synkronoida.</span><span class="sxs-lookup"><span data-stu-id="cef58-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="cef58-105">Joissakin skenaarioissa konsernin sisäisiä tilaustietoja ei tarvita asiakkaan aktivointisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="cef58-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="cef58-106">Kutakin Dataverse-vakiotaulua laajennetaan viittauksilla **IntercompanyOrder**-sarakkeisiin, ja kaksoiskirjoitusmäärityksiä muokataan siten, että ne viittaavat suodattimien lisäsarakkeisiin.</span><span class="sxs-lookup"><span data-stu-id="cef58-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="cef58-107">Tämän vuoksi konsernin sisäisiä tilauksia ei enää synkronoida.</span><span class="sxs-lookup"><span data-stu-id="cef58-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="cef58-108">Tämä prosessi auttaa estämään tarpeettomat tiedot asiakkaiden aktivointisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="cef58-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="cef58-109">**CDS myyntitilauksen otsikot** -taulu voidaan laajentaa lisäämällä viittaus **IntercompanyOrder**-sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="cef58-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="cef58-110">Tämä sarake täytetään vain konsernin sisäisissä tilauksissa.</span><span class="sxs-lookup"><span data-stu-id="cef58-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="cef58-111">**IntercompanyOrder**-sarake on käytettävissä **SalesTable**-taulussa.</span><span class="sxs-lookup"><span data-stu-id="cef58-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="CDS-myyntitilauksen otsikoiden Yhdistä väliaikainen alue kohteeseen -sivu":::

2. <span data-ttu-id="cef58-113">Kun **CDS-myyntitilauksen otsikot** on laajennettu, **IntercompanyOrder**-sarake on käytettävissä yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="cef58-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="cef58-114">Käytä suodatinta, jossa on `INTERCOMPANYORDER == ""` kyselymerkkijonona.</span><span class="sxs-lookup"><span data-stu-id="cef58-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="CDS-myyntitilauksen otsikoiden Muokkaa kyselyä -valintaikkuna":::

3. <span data-ttu-id="cef58-116">**CDS-myyntitilausrivit**-taulua voidaan laajentaa lisäämällä viittaus **IntercompanyInventTransId**-sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="cef58-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="cef58-117">Tämä sarake täytetään vain konsernin sisäisissä tilauksissa.</span><span class="sxs-lookup"><span data-stu-id="cef58-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="cef58-118">**InterCompanyInventTransId**-sarake on käytettävissä **SalesLine**-taulussa.</span><span class="sxs-lookup"><span data-stu-id="cef58-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="CDS-myyntitilausrivin Yhdistä väliaikainen alue kohteeseen -sivu":::

4. <span data-ttu-id="cef58-120">Kun **CDS-myyntitilausrivit** on laajennettu, **IntercompanyInventTransId**-sarake on käytettävissä yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="cef58-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="cef58-121">Käytä suodatinta, jossa on `INTERCOMPANYINVENTTRANSID == ""` kyselymerkkijonona.</span><span class="sxs-lookup"><span data-stu-id="cef58-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="CDS-myyntitilausrivien Muokkaa kyselyä -valintaikkuna":::

5. <span data-ttu-id="cef58-123">Laajenna **Myyntilaskun otsikko V2** -taulu ja lisää suodatinkysely toistamalla vaiheet 1 ja 2.</span><span class="sxs-lookup"><span data-stu-id="cef58-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="cef58-124">Käytä tässä tapauksessa suodatinta, jossa `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` on kyselymerkkijonona.</span><span class="sxs-lookup"><span data-stu-id="cef58-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Myyntilaskun otsikko V2:n Yhdistä väliaikainen alue kohteeseen -sivu":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Myyntilaskun otsikko V2:n Muokkaa kyselyä -valintaikkuna":::

6. <span data-ttu-id="cef58-127">Laajenna **Myyntilaskurivit V2** -taulu ja lisää suodatinkysely toistamalla vaiheet 3 ja 4.</span><span class="sxs-lookup"><span data-stu-id="cef58-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="cef58-128">Käytä tässä tapauksessa suodatinta, jossa `INTERCOMPANYINVENTTRANSID == ""` on kyselymerkkijonona.</span><span class="sxs-lookup"><span data-stu-id="cef58-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Myyntilaskun rivit V2:n Muokkaa kyselyä -valintaikkuna":::

7. <span data-ttu-id="cef58-130">**Tarjoukset**-taulussa ei ole yritysten välistä suhdetta.</span><span class="sxs-lookup"><span data-stu-id="cef58-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="cef58-131">Jos joku luo tarjouksen jollekin konsernin sisäiselle asiakkaalle, kaikki kyseiset asiakkaat voidaan sijoittaa yhteen asiakasryhmään käyttämällä **CustGroup**-saraketta.</span><span class="sxs-lookup"><span data-stu-id="cef58-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="cef58-132">Otsikkoa ja rivejä voidaan laajentaa lisäämällä **CustGroup**-sarake ja tekemällä sitten suodatuksen, joka ei sisällä kyseistä ryhmää.</span><span class="sxs-lookup"><span data-stu-id="cef58-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="CDS-myyntitarjouksen otsikon Yhdistä väliaikainen alue kohteeseen -sivu":::

8. <span data-ttu-id="cef58-134">Kun **Tarjoukset** on laajennettu, käytä suodatinta, jossa on `CUSTGROUP != "<company>"` kyselymerkkijonona.</span><span class="sxs-lookup"><span data-stu-id="cef58-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="CDS-myyntitarjouksen otsikon Muokkaa kyselyä -valintaikkuna":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]