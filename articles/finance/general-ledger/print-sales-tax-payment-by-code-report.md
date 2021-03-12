---
title: Arvonlisäveromaksun tulostaminen koodeittain -raportti
description: Tässä ohjeaiheessa on tietoja asetuksista ja toiminnoista, joita tarvitaan, jotta arvonlisäveromaksun koodiraportti voidaan tulostaa kirjanpidon tai verokoodin valuuttana.
author: anasyash
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: dd490663e66d1eda0eb0ea052e5b54fb867f81df
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990289"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="d2afd-103">Arvonlisäveromaksun tulostaminen koodeittain -raportti</span><span class="sxs-lookup"><span data-stu-id="d2afd-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2afd-104">Jos haluat tulostaa **Arvonlisäveromaksun koodin perusteella** -raportin, siirry kohtaan **Vero** \> **Tiedustelut ja raportit** \> **Arvonlisäveroraportit** \> **Arvon lisäveromaksu koodin mukaan**.</span><span class="sxs-lookup"><span data-stu-id="d2afd-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="d2afd-105">Oletusarvon mukaan raportin summat luodaan yrityksen kirjanpitovaluuttana kaikille raportointikoodeille, jotka on määritetty **Arvonlisäveroilmoituksen koodit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d2afd-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="d2afd-106">Voit myös luoda tämän raportin niin, että se näyttää arvonlisäveromaksun summat arvonlisäverokoodien valuuttoina kaikkien niiden raportointikoodien osalta, jotka on liitetty **Arvonlisäverokoodit** -sivun ALV-koodeihin.</span><span class="sxs-lookup"><span data-stu-id="d2afd-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="d2afd-107">Toiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="d2afd-107">Turn on the feature</span></span>

<span data-ttu-id="d2afd-108">Ota **Ominaisuuden hallinta** -työtilassa käyttöön seuraava ominaisuus: **Luo arvonlisäveromaksu koodin mukaan -raportti arvonlisäverokoodin valuuttana**.</span><span class="sxs-lookup"><span data-stu-id="d2afd-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="d2afd-109">Raportin suorittaminen</span><span class="sxs-lookup"><span data-stu-id="d2afd-109">Run the report</span></span>

1. <span data-ttu-id="d2afd-110">Siirry kohtaan **Vero** \> **Kyselyt ja raportit** \> **Arvonlisäveroraportit** \> **Arvonlisäveron maksu koodin mukaan**.</span><span class="sxs-lookup"><span data-stu-id="d2afd-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="d2afd-111">Valitse **Raportin valuutta** -kentästä jokin seuraavista arvoista:</span><span class="sxs-lookup"><span data-stu-id="d2afd-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="d2afd-112">**Kirjanpito valuutta** : Tulosta raportin summat kirjanpitovaluuttana.</span><span class="sxs-lookup"><span data-stu-id="d2afd-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="d2afd-113">**Arvonlisäverokoodin valuutta** – Tulosta raportin summat arvonlisäverokoodien valuuttoina.</span><span class="sxs-lookup"><span data-stu-id="d2afd-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Arvonlisäveromaksu koodeittain -valintaikkuna](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="d2afd-115">Seuraavassa kuvassa näkyy esimerkki luotavasta raportista.</span><span class="sxs-lookup"><span data-stu-id="d2afd-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="d2afd-116">Raportti osoittaa, että raportointikoodilla **101** on **EUR**-valuutta, jos **Arvonlisäveron valuutta** -kentän arvoksi on määritetty **EUR** sen arvonlisäverokoodin osalta, johon raportointikoodi on liitetty.</span><span class="sxs-lookup"><span data-stu-id="d2afd-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![Esimerkki arvonlisäveromaksu koodin mukaan -raportista](media/Sales-tax-payment-by-code-2.png)
