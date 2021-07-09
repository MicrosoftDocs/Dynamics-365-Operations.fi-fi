---
title: Tuote on pidossa tapahtumia varten
description: Kun olet vahvistanut suunnittelutilaukset, saat virhesanoman, jossa todetaan, että nimike on tapahtumien osalta pidossa.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301276"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="b28f8-103">Tuote on pidossa tapahtumia varten</span><span class="sxs-lookup"><span data-stu-id="b28f8-103">Product is on hold for transactions</span></span>

<span data-ttu-id="b28f8-104">Virhekoodi: SYS13295</span><span class="sxs-lookup"><span data-stu-id="b28f8-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="b28f8-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="b28f8-105">Symptoms</span></span>

<span data-ttu-id="b28f8-106">Kun yrität vahvistaa suunnitellut tilaukset, näyttöön tulee seuraava virhesanoma:</span><span class="sxs-lookup"><span data-stu-id="b28f8-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="b28f8-107">Tapahtumat on estetty nimikkeen %1 osalta kohteessa %2.</span><span class="sxs-lookup"><span data-stu-id="b28f8-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="b28f8-108">Syy</span><span class="sxs-lookup"><span data-stu-id="b28f8-108">Cause</span></span>

<span data-ttu-id="b28f8-109">Kun järjestelmä kuvailee estettyjä nimikkeitä, se käyttää *estetyn*, *pysäytetyn* ja *estossa olevien* ehtojen vaihtoa.</span><span class="sxs-lookup"><span data-stu-id="b28f8-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="b28f8-110">Tämä virhe tarkoittaa, että nimike on määritetty tilauksen oletusasetuksissa **Pysäytetty**-tilaksi.</span><span class="sxs-lookup"><span data-stu-id="b28f8-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="b28f8-111">Jos nimike on estetty ja lisäät sen ostotilaukseen tai myyntitilausriviin, näyttöön tulee varoitussanoma.</span><span class="sxs-lookup"><span data-stu-id="b28f8-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="b28f8-112">Kun nimike on estetty, osto- tai myyntitilausriviin liittyviä varastotapahtumia ei voi muokata (esimerkiksi pakkausluetteloa tai laskua kirjattaessa).</span><span class="sxs-lookup"><span data-stu-id="b28f8-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="b28f8-113">Voit estää ostetun nimikkeen ja samanaikaisesti myydä nimikkeen.</span><span class="sxs-lookup"><span data-stu-id="b28f8-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="b28f8-114">Tässä tapauksessa **Pysäytetty**-kenttä on valittu ostotilauksessa, mutta sitä ei ole estetty varastossa tai myyntitilauksessa.</span><span class="sxs-lookup"><span data-stu-id="b28f8-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="b28f8-115">Jotkin ehdoista voivat estää nimiketunnuksen myynnissä:</span><span class="sxs-lookup"><span data-stu-id="b28f8-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="b28f8-116">Nimike on vielä kehitys- tai valmistusvaiheessa.</span><span class="sxs-lookup"><span data-stu-id="b28f8-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="b28f8-117">Et siis halua, että sitä myydään tai varataan.</span><span class="sxs-lookup"><span data-stu-id="b28f8-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="b28f8-118">Olet vastaanottanut useita viallisia nimikkeitä, ja viat on korjattava, ennen kuin nimikettä voi myydä.</span><span class="sxs-lookup"><span data-stu-id="b28f8-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="b28f8-119">Tämän tyyppisissä tapauksissa nimikkeen myynti voidaan estää ongelman ratkaisuun asti.</span><span class="sxs-lookup"><span data-stu-id="b28f8-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="b28f8-120">JOs nimike on estetty ja luot palautustilausrivin, saat sanoman.</span><span class="sxs-lookup"><span data-stu-id="b28f8-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="b28f8-121">Et voi estää nimikesarjaa tai -erää.</span><span class="sxs-lookup"><span data-stu-id="b28f8-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="b28f8-122">Jos nimikkeen osia tulee estää, tämä voidaan tehdä varastosiirroilla tai estämällä koko nimikevarasto tarvittavaksi ajaksi.</span><span class="sxs-lookup"><span data-stu-id="b28f8-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="b28f8-123">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="b28f8-123">Resolution</span></span>

- <span data-ttu-id="b28f8-124">Avaa nimikkeen **oletustilausasetukset** -sivu ja tyhjennä **Pysäytetty**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b28f8-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
