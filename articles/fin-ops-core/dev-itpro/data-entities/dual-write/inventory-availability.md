---
title: Varaston käytettävyys kaksoiskirjoituksessa
description: Tässä ohjeaiheessa on tietoja varaston käytettävyyden tarkistamisesta kaksoiskirjoituksella.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: a7bfe998d2d787203a507a831c171fc43b03fedc
ms.sourcegitcommit: cc9921295f26804259cc9ec5137788ec9f2a4c6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839546"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="4819f-103">Varaston käytettävyys kaksoiskirjoituksessa</span><span class="sxs-lookup"><span data-stu-id="4819f-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4819f-104">Varaston käytettävyyttä käyttämällä voi tarkistaa varaston, ennen kuin tuote lisätään Microsoft Dynamics 365 Salesin **Tarjoukset**-, **Tilaukset**- tai **Laskut**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="4819f-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="4819f-105">Esimerkiksi varaston tarkistaminen ja täyttämispäivän määrittäminen ovat yksi [prospektista käteiseksi](dual-write-prospect-to-cash.md) -prosessin avaintehtävistä.</span><span class="sxs-lookup"><span data-stu-id="4819f-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="4819f-106">Jos varastoa ei ole riittävästi, voit arvioida toimituspäivämäärän arvioitujen varastovastaanottojen ja varastostaottojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="4819f-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="4819f-107">Voit myös tarkistaa tuotteen luvattavissa oleva määrä (ATP) -tiedot, joiden ATP-määrä löytyy ennalta määritetystä aikaraja-arvotyypistä.</span><span class="sxs-lookup"><span data-stu-id="4819f-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="4819f-108">Käytettävissä oleva varasto</span><span class="sxs-lookup"><span data-stu-id="4819f-108">On-hand inventory</span></span>

<span data-ttu-id="4819f-109">Dynamics 365 Salesin **Tarjous**-, **Tilaus**- ja **Lasku** -sivujen otsikkoon on lisätty uusi **Käytettävissä oleva varasto** -painike.</span><span class="sxs-lookup"><span data-stu-id="4819f-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="4819f-110">Kun valitset tämän painikkeen, näyttöön avautuu valintaikkuna, jossa voit määrittää yrityksen ja tuotteen, jonka käytettävissä olevan varaston haluat tarkistaa.</span><span class="sxs-lookup"><span data-stu-id="4819f-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="4819f-111">Tässä valintaikkunassa on samat tiedot kuin [käytettävissä olevassa varastossa](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="4819f-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="4819f-112">Valintaikkuna palauttaa varastotiedot Dynamics 365 Supply Chain Managementista.</span><span class="sxs-lookup"><span data-stu-id="4819f-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="4819f-113">Nämä tiedot sisältävät seuraavat määrät:</span><span class="sxs-lookup"><span data-stu-id="4819f-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="4819f-114">Varastosaldo</span><span class="sxs-lookup"><span data-stu-id="4819f-114">On-hand quantity</span></span>
- <span data-ttu-id="4819f-115">Varattu varastosaldo</span><span class="sxs-lookup"><span data-stu-id="4819f-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="4819f-116">Käytettävissä oleva varastosaldo</span><span class="sxs-lookup"><span data-stu-id="4819f-116">Available on-hand quantity</span></span>
- <span data-ttu-id="4819f-117">Tilattu määrä</span><span class="sxs-lookup"><span data-stu-id="4819f-117">Ordered quantity</span></span>
- <span data-ttu-id="4819f-118">Tilauksessa oleva määrä</span><span class="sxs-lookup"><span data-stu-id="4819f-118">On-order quantity</span></span>
- <span data-ttu-id="4819f-119">Varattu tilattu määrä</span><span class="sxs-lookup"><span data-stu-id="4819f-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="4819f-120">Käytettävissä oleva kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="4819f-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="4819f-121">ATP-tiedot</span><span class="sxs-lookup"><span data-stu-id="4819f-121">ATP information</span></span>

<span data-ttu-id="4819f-122">Salesissa on lisätty uusi **ATP-tiedot**-painike **Tarjoukset**-, **Tilaukset**- ja **Laskut**-sivujen rivinimikkeisiin.</span><span class="sxs-lookup"><span data-stu-id="4819f-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="4819f-123">Kun tämä painike valitaan, avautuvassa valintaikkunassa voi määrittää yrityksen, tuotteen, varastopaikan, varastointivaraston ja tilausmäärän.</span><span class="sxs-lookup"><span data-stu-id="4819f-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="4819f-124">Tässä valintaikkunassa on samat asetukset, jotka kuvattiin kohdassa [Luvatut tilaukset](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="4819f-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="4819f-125">Valintaikkuna palauttaa ATP-tiedot Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="4819f-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="4819f-126">Nämä tiedot sisältävät seuraavat määrät:</span><span class="sxs-lookup"><span data-stu-id="4819f-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="4819f-127">ATP-määrä</span><span class="sxs-lookup"><span data-stu-id="4819f-127">ATP quantity</span></span>
- <span data-ttu-id="4819f-128">Vastaanoton määrä</span><span class="sxs-lookup"><span data-stu-id="4819f-128">Receipt quantity</span></span>
- <span data-ttu-id="4819f-129">Varasto-oton määrä</span><span class="sxs-lookup"><span data-stu-id="4819f-129">Issue quantity</span></span>
- <span data-ttu-id="4819f-130">Varastosaldo</span><span class="sxs-lookup"><span data-stu-id="4819f-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="4819f-131">Näin se toimii</span><span class="sxs-lookup"><span data-stu-id="4819f-131">How it works</span></span>

<span data-ttu-id="4819f-132">Kun **Käytettävissä oleva varasto** -painike valitaan **Tarjoukset**-, **Tilaukset**- tai **Laskut**-sivulla, reaaliaikainen kaksoiskirjoituskutsu tehdään **Käytettävissä oleva varasto** -ohjelmistorajapinnassa.</span><span class="sxs-lookup"><span data-stu-id="4819f-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="4819f-133">Ohjelmointirajapinta laskee annetun tuotteen käytettävissä olevan varaston.</span><span class="sxs-lookup"><span data-stu-id="4819f-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="4819f-134">Tulos tallennetaan **InventCDSInventoryOnHandRequestEntity**- ja **InventCDSInventoryOnHandEntryEntity**-taulukoihin ja kirjoitettaan sitten kaksoiskirjoituksella Dataverseen.</span><span class="sxs-lookup"><span data-stu-id="4819f-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="4819f-135">Tämän toiminnon käyttämistä varten on suoritettava seuraavat kaksoiskirjoituksen määritykset.</span><span class="sxs-lookup"><span data-stu-id="4819f-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="4819f-136">Ohita ensimmäinen synkronointi määrityksiä suoritettaessa.</span><span class="sxs-lookup"><span data-stu-id="4819f-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="4819f-137">CDS:n käytettävissä olevan varaston viennit (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="4819f-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="4819f-138">CDS:n käytettävissä olevan varaston pyynnöt (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="4819f-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="4819f-139">Mallit</span><span class="sxs-lookup"><span data-stu-id="4819f-139">Templates</span></span>
<span data-ttu-id="4819f-140">Seuraavat mallit ovat käytettävissä käytettävissä olevan varaston tietojen tuominen nähtäville</span><span class="sxs-lookup"><span data-stu-id="4819f-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="4819f-141">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="4819f-141">Finance and Operations apps</span></span> | <span data-ttu-id="4819f-142">Asiakkaiden aktivointisovellus</span><span class="sxs-lookup"><span data-stu-id="4819f-142">Customer engagement app</span></span> | <span data-ttu-id="4819f-143">kuvaus</span><span class="sxs-lookup"><span data-stu-id="4819f-143">Description</span></span> 
---|---|---
[<span data-ttu-id="4819f-144">CDS:n käytettävissä olevan varaston merkinnät</span><span class="sxs-lookup"><span data-stu-id="4819f-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="4819f-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="4819f-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="4819f-146">CDS:n käytettävissä olevan varaston pyynnöt</span><span class="sxs-lookup"><span data-stu-id="4819f-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="4819f-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="4819f-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="4819f-148">CDS:n käytettävissä olevan varaston viennit (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="4819f-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="4819f-149">Tämä malli synkronoi tiedot Finance and Operations -sovellusten ja Dataversen välillä.</span><span class="sxs-lookup"><span data-stu-id="4819f-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="4819f-150">Finance and Operations -kenttä</span><span class="sxs-lookup"><span data-stu-id="4819f-150">Finance and Operations field</span></span> | <span data-ttu-id="4819f-151">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="4819f-151">Map type</span></span> | <span data-ttu-id="4819f-152">Asiakkaiden aktivointi -kenttä</span><span class="sxs-lookup"><span data-stu-id="4819f-152">Customer engagement field</span></span> | <span data-ttu-id="4819f-153">Oletusarvo</span><span class="sxs-lookup"><span data-stu-id="4819f-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="4819f-154">CDS:n käytettävissä olevan varaston pyynnöt (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="4819f-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="4819f-155">Tämä malli synkronoi tiedot Finance and Operations -sovellusten ja Dataversen välillä.</span><span class="sxs-lookup"><span data-stu-id="4819f-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="4819f-156">Finance and Operations -kenttä</span><span class="sxs-lookup"><span data-stu-id="4819f-156">Finance and Operations field</span></span> | <span data-ttu-id="4819f-157">Määritystyyppi</span><span class="sxs-lookup"><span data-stu-id="4819f-157">Map type</span></span> | <span data-ttu-id="4819f-158">Asiakkaiden aktivointi -kenttä</span><span class="sxs-lookup"><span data-stu-id="4819f-158">Customer engagement field</span></span> | <span data-ttu-id="4819f-159">Oletusarvo</span><span class="sxs-lookup"><span data-stu-id="4819f-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |




