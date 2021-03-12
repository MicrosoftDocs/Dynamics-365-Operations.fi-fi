---
title: Määritä käsittelykoodit
description: Voit määrittää käsittelykoodit, jotka määrittävät, miten asiakkaan palauttamaa nimikettä käsitellään.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnDispositionCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 518b70223b2f6bf86809ccce77a2cf67c30e4168
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977535"
---
# <a name="set-up-disposition-codes"></a><span data-ttu-id="80278-103">Määritä käsittelykoodit</span><span class="sxs-lookup"><span data-stu-id="80278-103">Set up disposition codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="80278-104">Voit määrittää käsittelykoodit, jotka määrittävät, miten asiakkaan palauttamaa nimikettä käsitellään.</span><span class="sxs-lookup"><span data-stu-id="80278-104">You can set up disposition codes to specify how to process an item that is returned by a customer.</span></span> <span data-ttu-id="80278-105">Luo esimerkiksi käsittelykoodi nimeltä **Korjaa ja palauta**, kun haluat osoittaa, että palautettu nimike korjataan ja palautetaan asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="80278-105">For example, create a disposition code named **Repair and return** to indicate that the returned item will be repaired and then returned to the customer.</span></span> <span data-ttu-id="80278-106">Lisää esimerkkejä käsittelykoodeista, joita käytetään yleisesti asiakkaiden palauttamissa nimikkeissä, on kohdassa [Palautettujen nimikkeiden poistotavan määrittäminen](specify-how-to-dispose-of-returned-items.md).</span><span class="sxs-lookup"><span data-stu-id="80278-106">For more examples of disposition codes that are typically used for items that are returned by customers, see [Specify how to dispose of returned items](specify-how-to-dispose-of-returned-items.md).</span></span>

<span data-ttu-id="80278-107">Voit määrittää myös syykoodin, kun haluat kertoa nimikkeen palautuksen syyn.</span><span class="sxs-lookup"><span data-stu-id="80278-107">You can also set up a reason code to help explain why an item was returned.</span></span> <span data-ttu-id="80278-108">Lisätietoja syykoodeista on kohdassa [Palautusten syykoodien määrittäminen](set-up-return-reason-code.md).</span><span class="sxs-lookup"><span data-stu-id="80278-108">For more information about reason codes, see [Set up return reason codes](set-up-return-reason-code.md).</span></span>

1.  <span data-ttu-id="80278-109">Valitse **Myynti ja markkinointi** \> **Asetukset** \> **Myyntitilaukset** \> **Palautukset** \> **Käsittelykoodit**.</span><span class="sxs-lookup"><span data-stu-id="80278-109">Click **Sales and marketing** \> **Setup** \> **Sales orders** \> **Returns** \> **Disposition codes**.</span></span>

2.  <span data-ttu-id="80278-110">Luo uusi käsittelykoodi valitsemalla **Uusi** tai painamalla CTRL+N-näppäinyhdistelmää.</span><span class="sxs-lookup"><span data-stu-id="80278-110">Click **New** or press CTRL+N to create a new disposition code.</span></span>

3.  <span data-ttu-id="80278-111">Syötä yksilöivä kuvaava nimi, valitse toiminto ja syötä käsittelykoodille kuvaus.</span><span class="sxs-lookup"><span data-stu-id="80278-111">Enter a unique, descriptive name, select an action, and enter a description for the disposition code.</span></span>

4.  <span data-ttu-id="80278-112">Jos haluat liittää tähän käsittelykoodiin asiakasmaksuja, napsauta **Kulut**-painiketta avataksesi **Määritä kulut** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="80278-112">If you want to associate any customer charges with this disposition code, click the **Charges** button to open the **Set up charges** form.</span></span>

5.  <span data-ttu-id="80278-113">Jos haluat määrittää yrityksen omia käsittelykoodeja vastaavia ulkoisia koodeja, napsauta **Ulkoiset koodit** -painiketta avataksesi **Ulkoiset koodit** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="80278-113">If you want to define any external codes to match with the company's own disposition codes, click the **External codes** button to open the **External codes** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="80278-114">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="80278-114">See also</span></span>

[<span data-ttu-id="80278-115">Asiakaspalautusten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="80278-115">Customer returns overview</span></span>](disposition-and-return-reason-codes.md)

<span data-ttu-id="80278-116">[Käsittelykoodit (lomake)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="80278-116">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

<span data-ttu-id="80278-117">[Automaattiset kulut (lomake)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="80278-117">[Auto charges (form)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))</span></span>

<span data-ttu-id="80278-118">[Ulkoiset koodit (lomake)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="80278-118">[External codes (form)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))</span></span>

  


