---
title: Kausittaiset luotonhallinnan tehtävät
description: Tässä ohjeaiheessa käsitellään kausittaisia tehtäviä, jotka ovat välttämätön osa asiakkaiden luottorajojen hallintaprosessia.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5e5d1ad7b0b151d67bd96513e9ce0c82c172a601
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835289"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="1b66b-103">Säännölliset luotonhallintatehtävät</span><span class="sxs-lookup"><span data-stu-id="1b66b-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b66b-104">Tässä ohjeaiheessa käsitellään kausittaisia tehtäviä, jotka ovat välttämätön osa asiakkaiden luottorajojen hallintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="1b66b-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="1b66b-105">Päivitä riskipisteet</span><span class="sxs-lookup"><span data-stu-id="1b66b-105">Update risk scores</span></span>

<span data-ttu-id="1b66b-106">Kun yritykset kehittyvät ja olosuhteet muuttuvat, myös tietyn asiakkaan luottoriskit voivat muuttua.</span><span class="sxs-lookup"><span data-stu-id="1b66b-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="1b66b-107">Asiakkaiden asianmukaisten luottorajojen ylläpitäminen edellyttää, että kunkin riskipisteytyksen kriteerit tarkistetaan kausittain ja että kunkin asiakkaan pistemäärät päivitetään.</span><span class="sxs-lookup"><span data-stu-id="1b66b-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="1b66b-108">Voit päivittää seuraavat pistemäärät **Päivitä riskipisteet** -sivulla (**Luotonvalvonta \> Kausittaiset tehtävät \> Luotonhallinta \> Päivitä riskipisteet**).</span><span class="sxs-lookup"><span data-stu-id="1b66b-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="1b66b-109">Myös kaikki käyttäjän määrittämät laskelmat käsitellään.</span><span class="sxs-lookup"><span data-stu-id="1b66b-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="1b66b-110">**Maksupäiviä keskimäärin** – tämä pistemäärä on se päivien määrä keskimäärin, joka asiakkaalta menee laskujen maksamiseen.</span><span class="sxs-lookup"><span data-stu-id="1b66b-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="1b66b-111">**Asiakas lähtien** – tämä pistemäärä on aika vuosina, jonka asiakas on ollut organisaation asiakkaana.</span><span class="sxs-lookup"><span data-stu-id="1b66b-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="1b66b-112">**Toiminut vuodesta** – Tämä pistemäärä ilmaisee vuosina, kuinka kauan asiakkaan yritystoiminta on kestänyt.</span><span class="sxs-lookup"><span data-stu-id="1b66b-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="1b66b-113">Se käyttää **Asiakkaat**-sivun **Yritystoiminta alkoi** -kentän arvoa.</span><span class="sxs-lookup"><span data-stu-id="1b66b-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="1b66b-114">**Selvittämätön päivämyynti** – tämä pistemäärä perustuu myyntireskontran saldoon, myyntituottoon ja päivien määrää kuluneen 12 kuukauden kaudelta.</span><span class="sxs-lookup"><span data-stu-id="1b66b-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="1b66b-115">**Keskimääräinen saldo** – tämä pistemäärä perustuu kuluneen 12 kuukauden kauden myyntireskontran saldoon.</span><span class="sxs-lookup"><span data-stu-id="1b66b-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="1b66b-116">**Luotonhallintaryhmä**, **Tilin tila** ja **Maa** – nämä pistemäärät käyttävät asiakkaalta saatuja tietoja.</span><span class="sxs-lookup"><span data-stu-id="1b66b-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="1b66b-117">Asiakkaan saldotilastojen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="1b66b-117">Update customer balance statistics</span></span>

<span data-ttu-id="1b66b-118">Voit suorittaa **Päivitä asiakkaan saldotilastot** -prosessin, joka päivittää **Saldotilastokysely**-sivulla näkyvän saldotilastolaskelman.</span><span class="sxs-lookup"><span data-stu-id="1b66b-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="1b66b-119">Näitä tietoja käytetään riskipisteiden laskemiseen, ja nämä arvot näkyvät **Asiakas**-sivun luottotilastojen tietoruuduissa.</span><span class="sxs-lookup"><span data-stu-id="1b66b-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="1b66b-120">Kun prosessi suoritetaan, se päivittää yhden asiakkaan saldotilaston.</span><span class="sxs-lookup"><span data-stu-id="1b66b-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="1b66b-121">Jos haluat määrittää erätyön suorittamaan prosessin useiden asiakkaiden osalta, voit käyttää **Laske saldotilastot** -sivua (**Luotonhallinta \> Kausittaiset tehtävät \> Laske saldotilastot**).</span><span class="sxs-lookup"><span data-stu-id="1b66b-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]