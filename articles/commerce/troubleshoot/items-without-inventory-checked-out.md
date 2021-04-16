---
title: Nimikkeet, joilla ei ole varastoa, voidaan kuitata ulos
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa siinä, kun asiakkaat voivat lisätä varastosta loppuneita nimikkeitä ostoskoriin ja jatkaa kassalle.
author: Reza-Assadi
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
ms.openlocfilehash: af44def901d3aa7d4b24ab6abfac60d066a8d1a3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801744"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="03240-103">Nimikkeet, joilla ei ole varastoa, voidaan kuitata ulos</span><span class="sxs-lookup"><span data-stu-id="03240-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="03240-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa siinä, kun asiakkaat voivat lisätä varastosta loppuneita nimikkeitä ostoskoriin ja jatkaa kassalle.</span><span class="sxs-lookup"><span data-stu-id="03240-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="03240-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="03240-105">Description</span></span>

<span data-ttu-id="03240-106">Käyttäjät voivat lisätä nimikkeen ostoskoriin, vaikka myymälässä ei olisikaan käytettävissä varastoa, ja jatkaa sitten kassasivulle.</span><span class="sxs-lookup"><span data-stu-id="03240-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="03240-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="03240-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="03240-108">Näytä loppu varastosta -virhe ominaisuuden ottaminen käyttöön Commercen sivuston luontiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="03240-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="03240-109">Ota **Näytä loppu varastosta -virhe** -ominaisuus käyttöön Commercen sivuston luontiohjelmassa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="03240-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="03240-110">Valitse sivusto, jota käsittelet.</span><span class="sxs-lookup"><span data-stu-id="03240-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="03240-111">Valitse vasemmanpuoleisessa siirtymisruudussa kohtaan **Sivut**.</span><span class="sxs-lookup"><span data-stu-id="03240-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="03240-112">Avaa **CartPage** valitsemalla.</span><span class="sxs-lookup"><span data-stu-id="03240-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="03240-113">Valitse **Cart 1** -paikka, valitse **Muokkaa** ja valitse sitten ominaisuusruudusta **Näytä loppu varastosta -virhe** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="03240-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="03240-114">Tallenna ja julkaise sivu.</span><span class="sxs-lookup"><span data-stu-id="03240-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03240-115">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="03240-115">Additional resources</span></span>

[<span data-ttu-id="03240-116">Varastoasetusten käyttäminen</span><span class="sxs-lookup"><span data-stu-id="03240-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="03240-117">Vähittäismyyntikanavien varaston käytettävyyden laskeminen</span><span class="sxs-lookup"><span data-stu-id="03240-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="03240-118">Varastopuskureiden ja varastotasojen konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="03240-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
