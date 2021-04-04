---
title: Nimikkeet, joilla ei ole varastoa, voidaan kuitata ulos
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa siinä, kun asiakkaat voivat lisätä varastosta loppuneita nimikkeitä ostoskoriin ja jatkaa kassalle.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6df9c77248c7f4e16765b98327fe5838f0fce7e4
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585301"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="f56fd-103">Nimikkeet, joilla ei ole varastoa, voidaan kuitata ulos</span><span class="sxs-lookup"><span data-stu-id="f56fd-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f56fd-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa siinä, kun asiakkaat voivat lisätä varastosta loppuneita nimikkeitä ostoskoriin ja jatkaa kassalle.</span><span class="sxs-lookup"><span data-stu-id="f56fd-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="f56fd-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="f56fd-105">Description</span></span>

<span data-ttu-id="f56fd-106">Käyttäjät voivat lisätä nimikkeen ostoskoriin, vaikka myymälässä ei olisikaan käytettävissä varastoa, ja jatkaa sitten kassasivulle.</span><span class="sxs-lookup"><span data-stu-id="f56fd-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="f56fd-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f56fd-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="f56fd-108">Näytä loppu varastosta -virhe ominaisuuden ottaminen käyttöön Commercen sivuston luontiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="f56fd-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="f56fd-109">Ota **Näytä loppu varastosta -virhe** -ominaisuus käyttöön Commercen sivuston luontiohjelmassa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f56fd-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f56fd-110">Valitse sivusto, jota käsittelet.</span><span class="sxs-lookup"><span data-stu-id="f56fd-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="f56fd-111">Valitse vasemmanpuoleisessa siirtymisruudussa kohtaan **Sivut**.</span><span class="sxs-lookup"><span data-stu-id="f56fd-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="f56fd-112">Avaa **CartPage** valitsemalla.</span><span class="sxs-lookup"><span data-stu-id="f56fd-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="f56fd-113">Valitse **Cart 1** -paikka, valitse **Muokkaa** ja valitse sitten ominaisuusruudusta **Näytä loppu varastosta -virhe** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f56fd-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="f56fd-114">Tallenna ja julkaise sivu.</span><span class="sxs-lookup"><span data-stu-id="f56fd-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f56fd-115">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f56fd-115">Additional resources</span></span>

[<span data-ttu-id="f56fd-116">Varastoasetusten käyttäminen</span><span class="sxs-lookup"><span data-stu-id="f56fd-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="f56fd-117">Vähittäismyyntikanavien varaston käytettävyyden laskeminen</span><span class="sxs-lookup"><span data-stu-id="f56fd-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="f56fd-118">Varastopuskureiden ja varastotasojen konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="f56fd-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
