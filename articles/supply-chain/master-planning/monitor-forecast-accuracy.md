---
title: Ennusteen tarkkuuden valvonta
description: "Tässä artikkelissa käsitellään ennusteen tarkkuuden tyyppejä, joita Microsoft Dynamics 365 for Finance and Operations laskee, ja kerrotaan, miten voit tarkastella näitä tarkkuusarvoja."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c2f9482a9906ad6c607d275769ac06b29b22c25d
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="c0783-103">Ennusteen tarkkuuden valvonta</span><span class="sxs-lookup"><span data-stu-id="c0783-103">Monitor forecast accuracy</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c0783-104">Tässä artikkelissa käsitellään ennusteen tarkkuuden tyyppejä, joita Microsoft Dynamics 365 for Finance and Operations laskee, ja kerrotaan, miten voit tarkastella näitä tarkkuusarvoja.</span><span class="sxs-lookup"><span data-stu-id="c0783-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="c0783-105">Finance and Operations laskee seuraavia ennusteen tarkkuuden tyyppejä:</span><span class="sxs-lookup"><span data-stu-id="c0783-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="c0783-106">Historiallinen ennusteen tarkkuus vertaamalla historiallista ennustetta, jota pääsuunnittelu käyttää historiallisen kysynnän kanssa.</span><span class="sxs-lookup"><span data-stu-id="c0783-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="c0783-107">Jos haluat tarkastella historiallisen tarkkuuden arvoja (sekä absoluuttisia että prosentuaalisia arvoja), valitse **Näytä tarkkuus****Kysynnän ennusteen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c0783-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="c0783-108">Ennustemallin arvioitua tarkkuutta käytetään ennusteiden luonnissa.</span><span class="sxs-lookup"><span data-stu-id="c0783-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="c0783-109">Voit tarkastella tarkkuusprosenttia kohdassa **Mallin tiedot - MAPE** **Kysynnän ennusteen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c0783-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="c0783-110">**Huomautus:** Jos käytät Finance and Operationsin kysynnän ennusteiden Microsoft Azuren automaattianalyysipalvelua, sisäisen mallin tarkkuuden laskenta perustuu testitietojen joukkoon.</span><span class="sxs-lookup"><span data-stu-id="c0783-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="c0783-111">Voit määrittää testitietojoukon koon määrittämällä **TEST\_SET\_SIZE\_PERCENT** (Testijoukon koon prosenttiosuus) -parametrin **Kysynnän ennusteen parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c0783-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="c0783-112">Jos esimerkiksi määrität arvoksi **20**, historiallisten tietojen viimeistä 20 prosenttia käytetään sisäisen mallin tarkkuuden laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="c0783-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="see-also"></a><span data-ttu-id="c0783-113">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="c0783-113">See also</span></span>
--------

[<span data-ttu-id="c0783-114">Oikaistun kysynnän ennusteen valtuuttaminen</span><span class="sxs-lookup"><span data-stu-id="c0783-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="c0783-115">Poista poikkeavat tiedot aiemmista tapahtumatiedoista laskettaessa ennustetarvetta</span><span class="sxs-lookup"><span data-stu-id="c0783-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)




