---
title: Nimikkeet, joilla ei ole varastoa, voidaan kuitata ulos
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa siinä, kun asiakkaat voivat lisätä varastosta loppuneita nimikkeitä ostoskoriin ja jatkaa kassalle.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018455"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="98ec1-103">Nimikkeet, joilla ei ole varastoa, voidaan kuitata ulos</span><span class="sxs-lookup"><span data-stu-id="98ec1-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98ec1-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa siinä, kun asiakkaat voivat lisätä varastosta loppuneita nimikkeitä ostoskoriin ja jatkaa kassalle.</span><span class="sxs-lookup"><span data-stu-id="98ec1-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="98ec1-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="98ec1-105">Description</span></span>

<span data-ttu-id="98ec1-106">Käyttäjät voivat lisätä nimikkeen ostoskoriin, vaikka myymälässä ei olisikaan käytettävissä varastoa, ja jatkaa sitten kassasivulle.</span><span class="sxs-lookup"><span data-stu-id="98ec1-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="98ec1-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="98ec1-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="98ec1-108">Näytä loppu varastosta -virhe ominaisuuden ottaminen käyttöön Commercen sivuston luontiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="98ec1-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="98ec1-109">Ota **Näytä loppu varastosta -virhe** -ominaisuus käyttöön Commercen sivuston luontiohjelmassa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="98ec1-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="98ec1-110">Valitse sivusto, jota käsittelet.</span><span class="sxs-lookup"><span data-stu-id="98ec1-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="98ec1-111">Valitse vasemmanpuoleisessa siirtymisruudussa kohtaan **Sivut**.</span><span class="sxs-lookup"><span data-stu-id="98ec1-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="98ec1-112">Avaa **CartPage** valitsemalla.</span><span class="sxs-lookup"><span data-stu-id="98ec1-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="98ec1-113">Valitse **Cart 1** -paikka, valitse **Muokkaa** ja valitse sitten ominaisuusruudusta **Näytä loppu varastosta -virhe** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="98ec1-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="98ec1-114">Tallenna ja julkaise sivu.</span><span class="sxs-lookup"><span data-stu-id="98ec1-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98ec1-115">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="98ec1-115">Additional resources</span></span>

[<span data-ttu-id="98ec1-116">Varastoasetusten käyttäminen</span><span class="sxs-lookup"><span data-stu-id="98ec1-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="98ec1-117">Vähittäismyyntikanavien varaston käytettävyyden laskeminen</span><span class="sxs-lookup"><span data-stu-id="98ec1-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="98ec1-118">Varastopuskureiden ja varastotasojen konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="98ec1-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
