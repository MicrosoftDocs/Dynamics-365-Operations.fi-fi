---
title: Valmiiksi ilmoittamisen peruuttaminen luo odottamattoman avoimen tapahtuman
description: Valmiiksi ilmoittamisen peruutus, jossa on merkintä, luo avoimen tapahtuman, jossa peruutetulla määrällä on samat varastodimensiot kuin peruutetulla tapahtumalla.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026485"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="1dec0-103">Valmiiksi ilmoittamisen peruuttaminen luo odottamattoman avoimen tapahtuman</span><span class="sxs-lookup"><span data-stu-id="1dec0-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="1dec0-104">Tietopankin numero: 4612469</span><span class="sxs-lookup"><span data-stu-id="1dec0-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="1dec0-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="1dec0-105">Symptoms</span></span>

<span data-ttu-id="1dec0-106">Jos peruutat valmiiksi ilmoittamisen, jossa on merkintä, järjestelmä luo avoimen tapahtuman, jossa peruutetulla määrällä on samat varastodimensiot kuin peruutetulla tapahtumalla.</span><span class="sxs-lookup"><span data-stu-id="1dec0-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="1dec0-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="1dec0-107">Resolution</span></span>

<span data-ttu-id="1dec0-108">Kun peruutat valmiiksi ilmoittamistoiminnon, varastodimensio alustetaan tuotantokirjauskansiosta.</span><span class="sxs-lookup"><span data-stu-id="1dec0-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="1dec0-109">Näin ollen se saa eränumeron.</span><span class="sxs-lookup"><span data-stu-id="1dec0-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="1dec0-110">Merkinnän vuoksi myyntitilaustapahtumat perivät eränumeron.</span><span class="sxs-lookup"><span data-stu-id="1dec0-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="1dec0-111">Dimension voi nollata, kun valmiiksi ilmoittaminen kirjataan.</span><span class="sxs-lookup"><span data-stu-id="1dec0-111">The dimension can be reset when the reporting as finished is posted.</span></span>
