---
title: TaxTrans-kentän arvo on virheellinen
description: Tässä aiheessa on tietoja virheellisten kenttien arvojen vianmäärityksestä TaxTrans-kentässä.
author: bijian
manager: beya
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 97f9bb24d32180f2fccb69c5a13e2aa0349c1ee4
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947630"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="b4c92-103">TaxTrans-kentän arvo on virheellinen</span><span class="sxs-lookup"><span data-stu-id="b4c92-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4c92-104">Jos **TaxTrans**-kentän arvo on virheellinen, voit yrittää ratkaista ongelman tämän ohjeaiheen tietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="b4c92-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="b4c92-105">Arvojen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b4c92-105">Overview of values</span></span>
<span data-ttu-id="b4c92-106">Seuraavassa luettelossa näkyy, että **TaxTrans**, **TaxUncommitted** ja **TmpTaxWorkTrans** ovat samanlaisia tietojoukkoja, mutta toimivat eri tavoin.</span><span class="sxs-lookup"><span data-stu-id="b4c92-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="b4c92-107">**TaxTrans** on viimeinen kirjattu verotapahtuman tulos, joka säilyy tietokannassa.</span><span class="sxs-lookup"><span data-stu-id="b4c92-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="b4c92-108">**TaxUncommitted** on väliaikainen laskettu verotulos, joka säilyy tietokannassa (jos käytettävissä), jota käytetään myöhemmin kirjauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b4c92-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="b4c92-109">**TmpTaxWorkTrans** on väliaikainen laskettu verotulos muistissa olevassa taulukossa (taulutyyppi = InMemory).</span><span class="sxs-lookup"><span data-stu-id="b4c92-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="b4c92-110">Jos virheellisen **TaxTrans**-sarakkeen juurisyy löytyy, olet myös löytänyt virheellisen **TaxUncommitted**- tai **TmpTaxWorkTrans**-sarakkeen juurisyyn.</span><span class="sxs-lookup"><span data-stu-id="b4c92-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="b4c92-111">Tämä johtuu siitä, että nämä kolme saraketta kopioidaan toisistaan.</span><span class="sxs-lookup"><span data-stu-id="b4c92-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="b4c92-112">Yleensä verolaskennan aikana luodaan **TmpTaxWorkTrans** ja sitten, jos käytettävissä, luodaan **TaxUncommitted**.</span><span class="sxs-lookup"><span data-stu-id="b4c92-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="b4c92-113">Verojen kirjaamisen aikana luodaan **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="b4c92-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="b4c92-114">Keskeytyskohtien lisääminen</span><span class="sxs-lookup"><span data-stu-id="b4c92-114">Add breakpoints</span></span>
<span data-ttu-id="b4c92-115">Lisää keskeytyskohtia seuraavien ohjeiden mukaan:</span><span class="sxs-lookup"><span data-stu-id="b4c92-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="b4c92-116">Lisää laajennuksia ja keskeytyskohtia *lisää()*- ja *päivitä()*-kohdissa laajennuksiin alla esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="b4c92-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="b4c92-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="b4c92-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="b4c92-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="b4c92-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="b4c92-119">**TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="b4c92-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="b4c92-120">Voit myös lisätä keskeytyskohtia suoraan, kun **TaxUncommitted** ei sisälly.</span><span class="sxs-lookup"><span data-stu-id="b4c92-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="b4c92-121">*TaxTrans.insert()*, *TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="b4c92-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="b4c92-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="b4c92-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="b4c92-123">Toistaminen ja virheenkorjaus</span><span class="sxs-lookup"><span data-stu-id="b4c92-123">Reproduce and debug</span></span>

<span data-ttu-id="b4c92-124">Kun keskeytyskohdat on määritetty, kaikki tietojen säilymisen muutokset näkyvät virheenkorjauksen aikana.</span><span class="sxs-lookup"><span data-stu-id="b4c92-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="b4c92-125">Voit etsiä juurisyyn virheelliselle sarakkeelle **TaxTrans**, **TaxUncommitted** tai **TmpTaxWorkTrans** tarkistamalla ja huomioimalla seuraavat nimikkeet:</span><span class="sxs-lookup"><span data-stu-id="b4c92-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="b4c92-126">Viimeinen keskeytyskohta, jossa sarake on oikea.</span><span class="sxs-lookup"><span data-stu-id="b4c92-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="b4c92-127">Ensimmäinen keskeytyskohta, jossa sarake on väärä.</span><span class="sxs-lookup"><span data-stu-id="b4c92-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="b4c92-128">Mitä näiden kahden pisteen välillä tapahtuu.</span><span class="sxs-lookup"><span data-stu-id="b4c92-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="b4c92-129">Määritä, onko mukautus olemassa</span><span class="sxs-lookup"><span data-stu-id="b4c92-129">Determine whether customization exists</span></span>
<span data-ttu-id="b4c92-130">Jos olet suorittanut edellisten osien vaiheet, mutta et voi ratkaista ongelmaa, selvitä, onko mukautus olemassa.</span><span class="sxs-lookup"><span data-stu-id="b4c92-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="b4c92-131">Jos mukautusta ei ole, ota yhteyttä Microsoftin tukeen.</span><span class="sxs-lookup"><span data-stu-id="b4c92-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

