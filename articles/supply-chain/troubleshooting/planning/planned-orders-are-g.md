---
title: Pääsuunnittelu luo suunniteltuja tilauksia haamutuotteita varten
description: Suunnitellut tilaukset luodaan haamutuotteita varten pääsuunnittelun suorittamisen jälkeen.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026480"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="40fb0-103">Pääsuunnittelu luo suunniteltuja tilauksia haamutuotteita varten</span><span class="sxs-lookup"><span data-stu-id="40fb0-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="40fb0-104">Tietopankin numero: 4614729</span><span class="sxs-lookup"><span data-stu-id="40fb0-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="40fb0-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="40fb0-105">Symptoms</span></span>

<span data-ttu-id="40fb0-106">Suunnitellut tilaukset luodaan haamutuotteita varten pääsuunnittelun suorittamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="40fb0-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="40fb0-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="40fb0-107">Resolution</span></span>

<span data-ttu-id="40fb0-108">Vapautettujen tuotteiden **Haamu**-vaihtoehdon asetus määrittää tuoterakenteen oletusrivityypin.</span><span class="sxs-lookup"><span data-stu-id="40fb0-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="40fb0-109">Kun **Haamu**-asetuksena on *Kyllä*, järjestelmä luo nimikkeelle edelleen suunnitellut tilaukset, mutta kunkin suunnitellun tilauksen **Suoraan johdettava tarve** -asetuksena on *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="40fb0-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="40fb0-110">Siksi suunniteltua tuotantotilausta ei voi vahvistaa erillään.</span><span class="sxs-lookup"><span data-stu-id="40fb0-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="40fb0-111">Sen sijaan se sisällytetään aina automaattisesti, kun päätuotantotilaus on vahvistettu.</span><span class="sxs-lookup"><span data-stu-id="40fb0-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="40fb0-112">Lisäksi suunnitellun haamutilauksen tuoterakennerivit sisällytetään päätuotantotilauksen tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="40fb0-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
