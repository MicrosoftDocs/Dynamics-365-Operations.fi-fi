---
title: Indeksikorkojen määrittäminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää indeksikorot. Indeksikorot ovat pakollisia, jos organisaatio liittää maksusummat indeksikorkojoukkoon.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6424248e8d01d04720ad65e80aaa543b42abccc6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823020"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="ba49c-104">Indeksikorkojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ba49c-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba49c-105">Jos vuokramaksut riippuvat indeksistä, järjestelmään voidaan lisätä indeksikorkotyypit ja niitä voi ylläpitää siellä.</span><span class="sxs-lookup"><span data-stu-id="ba49c-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="ba49c-106">Voit arvostaa vuokrat uudelleen **Indeksikorkotyyppi**-sivulla, jos indeksikoron uudelleenarvostusprosessi käyttää uusinta indeksikorkoa uudelleenarvostuksen päivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="ba49c-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="ba49c-107">Voit lisätä indeksikorkotyyppejä ja indeksikorkoja seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="ba49c-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="ba49c-108">Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Indeksikorkotyyppi**.</span><span class="sxs-lookup"><span data-stu-id="ba49c-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="ba49c-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ba49c-109">Select **New**.</span></span>
3. <span data-ttu-id="ba49c-110">Syötä asianmukaisiin kenttiin korkotyyppi ja indeksikoron nimi.</span><span class="sxs-lookup"><span data-stu-id="ba49c-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="ba49c-111">Jos haluat lisätä uuden indeksikoron arvon, valitse indeksikorkotyyppi ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="ba49c-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="ba49c-112">Valitse koron voimassaolon alkamispäivämäärä ja valitse koron arvo.</span><span class="sxs-lookup"><span data-stu-id="ba49c-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="ba49c-113">Sinun on valittava **Indeksikoron arvojen ero**- tai **Indeksikoron arvo** indeksikoron menetelmäksi.</span><span class="sxs-lookup"><span data-stu-id="ba49c-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="ba49c-114">Valitse **Indeksikoron arvojen ero** -menetelmä, jos haluat laskea uuden vuokran indeksikoron eron perusteella alkupäivämäärän ja uusimman indeksikoron välillä.</span><span class="sxs-lookup"><span data-stu-id="ba49c-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="ba49c-115">Indeksikorko määritetään **Indeksikorko (%)** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="ba49c-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="ba49c-116">Valitse **Indeksikoron arvo** -menetelmä, jos haluat laskea maksun käyttämällä **Indeksikorko (%)** -kentässä määritettyä prosenttilukua.</span><span class="sxs-lookup"><span data-stu-id="ba49c-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]