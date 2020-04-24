---
title: Ennusteen tarkkuuden seuranta
description: Tässä aiheessa kuvataan ennusteen tarkkuuden tyyppejä, joita Dynamics 365 Supply Chain Management laskee ja ilmoittaa, miten voit tarkastella näitä tarkkuusarvoja.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab74ba88ba9eb683107ef82bc105f5a3ed8fac08
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209809"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="040b0-103">Ennusteen tarkkuuden seuranta</span><span class="sxs-lookup"><span data-stu-id="040b0-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="040b0-104">Tässä aiheessa kuvataan ennusteen tarkkuuden tyyppejä, joita Microsoft Dynamics 365 Supply Chain Management laskee ja ilmoittaa, miten voit tarkastella näitä tarkkuusarvoja.</span><span class="sxs-lookup"><span data-stu-id="040b0-104">This topic describes the types of forecast accuracy that Microsoft Dynamics 365 Supply Chain Management calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="040b0-105">Supply Chain Management laskee seuraavia ennusteen tarkkuuden tyyppejä:</span><span class="sxs-lookup"><span data-stu-id="040b0-105">Supply Chain Management calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="040b0-106">Historiallinen ennusteen tarkkuus vertaamalla historiallista ennustetta, jota pääsuunnittelu käyttää historiallisen kysynnän kanssa.</span><span class="sxs-lookup"><span data-stu-id="040b0-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="040b0-107">Jos haluat tarkastella historiallisen tarkkuuden arvoja (sekä absoluuttisia että prosentuaalisia arvoja), valitse **Näytä tarkkuus** **Kysynnän ennusteen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="040b0-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="040b0-108">Ennustemallin arvioitua tarkkuutta käytetään ennusteiden luonnissa.</span><span class="sxs-lookup"><span data-stu-id="040b0-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="040b0-109">Voit tarkastella tarkkuusprosenttia kohdassa **Mallin tiedot - MAPE** **Kysynnän ennusteen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="040b0-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="040b0-110">Jos käytät kysynnän ennusteiden Microsoft Azuren automaattianalyysiä, sisäisen mallin tarkkuuden laskenta perustuu testitietojen joukkoon.</span><span class="sxs-lookup"><span data-stu-id="040b0-110">If you use the Demand forecasting Microsoft Azure Machine Learning, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="040b0-111">Voit määrittää testitietojoukon koon määrittämällä **TEST\_SET\_SIZE\_PERCENT** (Testijoukon koon prosenttiosuus) -parametrin **Kysynnän ennusteen parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="040b0-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="040b0-112">Jos esimerkiksi määrität arvoksi **20**, historiallisten tietojen viimeistä 20 prosenttia käytetään sisäisen mallin tarkkuuden laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="040b0-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="040b0-113">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="040b0-113">Additional resources</span></span>
--------

[<span data-ttu-id="040b0-114">Oikaistun ennusteen valtuuttaminen</span><span class="sxs-lookup"><span data-stu-id="040b0-114">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="040b0-115">Poista poikkeavat tiedot aiemmista tapahtumatiedoista laskettaessa ennustetarvetta</span><span class="sxs-lookup"><span data-stu-id="040b0-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)



