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
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997889"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="1f2c0-103">Varaston käytettävyys kaksoiskirjoituksessa</span><span class="sxs-lookup"><span data-stu-id="1f2c0-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1f2c0-104">Varaston käytettävyyttä käyttämällä voi tarkistaa varaston, ennen kuin tuote lisätään Microsoft Dynamics 365 Salesin **Tarjoukset** -, **Tilaukset** - tai **Laskut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="1f2c0-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations** , **Orders** , or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="1f2c0-105">Esimerkiksi varaston tarkistaminen ja täyttämispäivän määrittäminen ovat yksi [prospektista käteiseksi](dual-write-prospect-to-cash.md) -prosessin avaintehtävistä.</span><span class="sxs-lookup"><span data-stu-id="1f2c0-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="1f2c0-106">Jos varastoa ei ole riittävästi, voit arvioida toimituspäivämäärän arvioitujen varastovastaanottojen ja varastostaottojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="1f2c0-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="1f2c0-107">Voit myös tarkistaa tuotteen luvattavissa oleva määrä (ATP) -tiedot, joiden ATP-määrä löytyy ennalta määritetystä aikaraja-arvotyypistä.</span><span class="sxs-lookup"><span data-stu-id="1f2c0-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="1f2c0-108">Käytettävissä oleva varasto</span><span class="sxs-lookup"><span data-stu-id="1f2c0-108">On-hand inventory</span></span>

<span data-ttu-id="1f2c0-109">Dynamics 365 Salesin **Tarjous** -, **Tilaus** - ja **Lasku** -sivujen otsikkoon on lisätty uusi **Käytettävissä oleva varasto** -painike.</span><span class="sxs-lookup"><span data-stu-id="1f2c0-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes** , **Orders** , and **Invoices** pages.</span></span> <span data-ttu-id="1f2c0-110">Kun valitset tämän painikkeen, näyttöön avautuu valintaikkuna, jossa voit määrittää yrityksen ja tuotteen, jonka käytettävissä olevan varaston haluat tarkistaa.</span><span class="sxs-lookup"><span data-stu-id="1f2c0-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="1f2c0-111">Tässä valintaikkunassa on samat tiedot kuin [käytettävissä olevassa varastossa](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="1f2c0-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="1f2c0-112">Valintaikkuna palauttaa varastotiedot Dynamics 365 Supply Chain Managementista.</span><span class="sxs-lookup"><span data-stu-id="1f2c0-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1f2c0-113">Nämä tiedot sisältävät seuraavat määrät:</span><span class="sxs-lookup"><span data-stu-id="1f2c0-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="1f2c0-114">Varastosaldo</span><span class="sxs-lookup"><span data-stu-id="1f2c0-114">On-hand quantity</span></span>
- <span data-ttu-id="1f2c0-115">Varattu varastosaldo</span><span class="sxs-lookup"><span data-stu-id="1f2c0-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="1f2c0-116">Käytettävissä oleva varastosaldo</span><span class="sxs-lookup"><span data-stu-id="1f2c0-116">Available on-hand quantity</span></span>
- <span data-ttu-id="1f2c0-117">Tilattu määrä</span><span class="sxs-lookup"><span data-stu-id="1f2c0-117">Ordered quantity</span></span>
- <span data-ttu-id="1f2c0-118">Tilauksessa oleva määrä</span><span class="sxs-lookup"><span data-stu-id="1f2c0-118">On-order quantity</span></span>
- <span data-ttu-id="1f2c0-119">Varattu tilattu määrä</span><span class="sxs-lookup"><span data-stu-id="1f2c0-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="1f2c0-120">Käytettävissä oleva kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="1f2c0-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="1f2c0-121">ATP-tiedot</span><span class="sxs-lookup"><span data-stu-id="1f2c0-121">ATP information</span></span>

<span data-ttu-id="1f2c0-122">Salesissa on lisätty uusi **ATP-tiedot** -painike **Tarjoukset** -, **Tilaukset** - ja **Laskut** -sivujen rivinimikkeisiin.</span><span class="sxs-lookup"><span data-stu-id="1f2c0-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes** , **Orders** , and **Invoices** pages.</span></span> <span data-ttu-id="1f2c0-123">Kun tämä painike valitaan, avautuvassa valintaikkunassa voi määrittää yrityksen, tuotteen, varastopaikan, varastointivaraston ja tilausmäärän.</span><span class="sxs-lookup"><span data-stu-id="1f2c0-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="1f2c0-124">Tässä valintaikkunassa on samat asetukset, jotka kuvattiin kohdassa [Luvatut tilaukset](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="1f2c0-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="1f2c0-125">Valintaikkuna palauttaa ATP-tiedot Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="1f2c0-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="1f2c0-126">Nämä tiedot sisältävät seuraavat määrät:</span><span class="sxs-lookup"><span data-stu-id="1f2c0-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="1f2c0-127">ATP-määrä</span><span class="sxs-lookup"><span data-stu-id="1f2c0-127">ATP quantity</span></span>
- <span data-ttu-id="1f2c0-128">Vastaanoton määrä</span><span class="sxs-lookup"><span data-stu-id="1f2c0-128">Receipt quantity</span></span>
- <span data-ttu-id="1f2c0-129">Varasto-oton määrä</span><span class="sxs-lookup"><span data-stu-id="1f2c0-129">Issue quantity</span></span>
- <span data-ttu-id="1f2c0-130">Varastosaldo</span><span class="sxs-lookup"><span data-stu-id="1f2c0-130">On-hand quantity</span></span>
