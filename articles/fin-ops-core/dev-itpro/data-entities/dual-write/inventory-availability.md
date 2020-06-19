---
title: Varaston käytettävyys kaksoiskirjoitusalueella
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426979"
---
# <a name="inventory-availability"></a><span data-ttu-id="682b6-103">Varaston käytettävyys</span><span class="sxs-lookup"><span data-stu-id="682b6-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="682b6-104">Varaston käytettävyyttä käyttämällä voit tarkistaa varastosi, ennen kuin lisäät tuotteen mallisovellusten **tarjouksiin**, **tilauksiin** tai **laskuihin** Dynamics 365 -järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="682b6-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="682b6-105">Esimerkiksi varaston tarkistaminen ja toteutuksen päättymispäivän määrittäminen ovat [prospektista käteiseksi](dual-write-prospect-to-cash.md) -prosessin avaintehtäviä.</span><span class="sxs-lookup"><span data-stu-id="682b6-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="682b6-106">Jos varastoa ei ole riittävästi, voit arvioida toimituspäivämäärän arvioitujen varastovastaanottojen ja varastostaottojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="682b6-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="682b6-107">Voit myös tarkistaa tuotteen luvattavissa oleva määrä (ATP) -tiedot, joiden ATP-määrä löytyy ennalta määritetystä aikaraja-arvotyypistä.</span><span class="sxs-lookup"><span data-stu-id="682b6-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="682b6-108">Käytettävissä oleva varasto</span><span class="sxs-lookup"><span data-stu-id="682b6-108">On-hand Inventory</span></span> 

<span data-ttu-id="682b6-109">Dynamics 365 Salesin **Tarjous**-, **Tilaus**- tai **Lasku** -lomakkeiden otsikossa on lisätty uusi **Käytettävissä oleva varasto** -painike.</span><span class="sxs-lookup"><span data-stu-id="682b6-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="682b6-110">Kun napsautat painiketta, näyttöön tulee valintaikkuna, jossa voit määrittää yrityksen ja tuotteen, jolle haluat tarkistaa käytettävissä olevan varaston.</span><span class="sxs-lookup"><span data-stu-id="682b6-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="682b6-111">Se palauttaa varastotiedot Dynamics 365 Supply Chain Management -lomakkeesta ja näyttää samat tiedot kuin kohteessa [käytettävissä oleva varasto](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="682b6-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="682b6-112">Tiedot sisältävät seuraavat määrät:</span><span class="sxs-lookup"><span data-stu-id="682b6-112">The information includes these quantities:</span></span>

- <span data-ttu-id="682b6-113">**Varastosaldo**</span><span class="sxs-lookup"><span data-stu-id="682b6-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="682b6-114">**Varattu varastosaldo**</span><span class="sxs-lookup"><span data-stu-id="682b6-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="682b6-115">**Saatavilla oleva varastosaldo**</span><span class="sxs-lookup"><span data-stu-id="682b6-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="682b6-116">**Tilattu määrä**</span><span class="sxs-lookup"><span data-stu-id="682b6-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="682b6-117">**Tilauksessa oleva määrä**</span><span class="sxs-lookup"><span data-stu-id="682b6-117">**On-order Quantity**</span></span>
- <span data-ttu-id="682b6-118">**Varattu tilattu määrä**</span><span class="sxs-lookup"><span data-stu-id="682b6-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="682b6-119">**Käytettävissä oleva kokonaismäärä**</span><span class="sxs-lookup"><span data-stu-id="682b6-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="682b6-120">ATP-tiedot</span><span class="sxs-lookup"><span data-stu-id="682b6-120">ATP information</span></span>

<span data-ttu-id="682b6-121">Dynamics 365 Salesin **Tarjous**-, **Tilaus**- tai **Lasku** -lomakkeiden rivinimikkeisiin on lisätty uusi **ATP-tiedot**-painike.</span><span class="sxs-lookup"><span data-stu-id="682b6-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="682b6-122">Kun napsautat painiketta, näyttöön tulee valintaikkuna, jossa voit määrittää yrityksen, tuotteen, varastopaikan, varastointivaraston ja tilausmäärän.</span><span class="sxs-lookup"><span data-stu-id="682b6-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="682b6-123">Se palauttaa **ATP-tiedot** Supply Chain Managementista ja näyttää asetukset [toimituksen lupaamisen](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) osalta.</span><span class="sxs-lookup"><span data-stu-id="682b6-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="682b6-124">Tietoihin sisältyvät **ATP-määrä**, **Vastaanottomäärä**, **Varasto-ottomäärä** ja **Käytettävissä oleva määrä**.</span><span class="sxs-lookup"><span data-stu-id="682b6-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
