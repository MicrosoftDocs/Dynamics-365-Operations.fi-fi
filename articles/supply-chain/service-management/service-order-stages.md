---
title: Huoltotilauksen vaiheet
description: Huoltotilauksen vaiheet määrittämällä ja liittämällä ne työntekijöihin voit ohjata huoltotilauksen kulkua tehtävissä, joita eri henkilöt suorittavat huolto-organisaatiossa.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c46d4bb43c8f59a0ef55963ac9b453491a6112b0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817506"
---
# <a name="service-order-stages"></a><span data-ttu-id="f2b62-103">Huoltotilauksen vaiheet</span><span class="sxs-lookup"><span data-stu-id="f2b62-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f2b62-104">Voit määrittää huoltotilauksen tehtävät, jotka on suoritettava, niiden suoritusjärjestyksen ja työntekijät, jotka vastaavat niiden suorittamisesta.</span><span class="sxs-lookup"><span data-stu-id="f2b62-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="f2b62-105">Huoltotilauksen vaiheet määrittämällä ja liittämällä ne työntekijöihin voit ohjata huoltotilauksen kulkua tehtävissä, joita eri henkilöt suorittavat huolto-organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="f2b62-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="f2b62-106">Vaiheiden järjestyksen tulee sisältää alkuperäinen vaihe.</span><span class="sxs-lookup"><span data-stu-id="f2b62-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="f2b62-107">Voit myös määrittää toimenpiteet, jotka ovat sallittuja kussakin vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="f2b62-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="f2b62-108">Jos esimerkiksi poistat **Kirjaa**-valintaruudun valinnan muissa paitsi viimeisessä vaiheessa, huoltotilauksia ei voi kirjata, ennen kuin huoltotilaukset on käsitelty kaikkien vaiheiden läpi.</span><span class="sxs-lookup"><span data-stu-id="f2b62-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="f2b62-109">Haaroitus palvelutilauksen vaiheissa</span><span class="sxs-lookup"><span data-stu-id="f2b62-109">Branching in service order stages</span></span>

<span data-ttu-id="f2b62-110">Huollon vaiheen määrittäessäsi voit luoda useita vaihtoehtoja tai haaroja, joilla valitaan huoltotilauksen seuraava vaihe.</span><span class="sxs-lookup"><span data-stu-id="f2b62-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="f2b62-111">Kaikki luomasi sivuliikkeet ovat valittavissa, kun ensimmäinen vaihe on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="f2b62-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="f2b62-112">Voit esimerkiksi asettaa **Suunnittelun** aloitusvaiheeksi.</span><span class="sxs-lookup"><span data-stu-id="f2b62-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="f2b62-113">Luot kaksi vaihetta nimeltä **Käsittelyssä** ja **Peruuta** ja valitset sitten niiden ylätasoksi **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="f2b62-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="f2b62-114">Voit määrittää **suunnittelu**-vaiheen myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="f2b62-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="f2b62-115">Kun myyntitilauksen suunnitteluvaihe on valmis, voit valita **prosessivaiheessa**, onko myyntitilaus valmis käsiteltäväksi, tai voit valita **peruuta** vaihe, jos myyntitilaus peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="f2b62-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2b62-116">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="f2b62-116">See also</span></span>

[<span data-ttu-id="f2b62-117">Määritä huoltotilausvaiheet</span><span class="sxs-lookup"><span data-stu-id="f2b62-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="f2b62-118">Huoltotilauksen vaiheen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="f2b62-118">Change the service order stage</span></span>](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]