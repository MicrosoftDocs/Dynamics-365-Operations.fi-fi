---
title: Yhden tositteen kirjauskansioiden ja valuutan uudelleenarvostusten päivittäminen
description: Tässä aiheessa käsitellään yhden tositteen kirjauskansioiden ja valuutan uudelleenarvostusten päivittämistä.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3504c01a4ed1571866fd2a0cd83eef86a57d684a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127300"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="c9caf-103">Yhden tositteen kirjauskansioiden ja valuutan uudelleenarvostusten päivittäminen</span><span class="sxs-lookup"><span data-stu-id="c9caf-103">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9caf-104">Jotkin organisaatiot kirjaavat kirjauskansioita, jotka sisältävät yhden tositteen, jolla on useampi asiakas tai toimittaja, ja käyttävät myös myynti- tai ostoreskontran ulkomaanvaluutan uudelleenarvostusprosessia.</span><span class="sxs-lookup"><span data-stu-id="c9caf-104">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="c9caf-105">Tässä ohjeaiheessa kuvataan vaiheet, joita näiden organisaatioiden tulee seurata päivittäessään Microsoft Dynamics 365 for Operationsin versioon 1611.</span><span class="sxs-lookup"><span data-stu-id="c9caf-105">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="c9caf-106">Tee päivitys Microsoft Dynamics 365 for Operationsin versioon 1611 seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="c9caf-106">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="c9caf-107">Ennen kuin päivität Finance and Operationsiin, suorita ulkomaanvaluutan uudelleenarvostusprosessi myynti- ja ostoreskontralle.</span><span class="sxs-lookup"><span data-stu-id="c9caf-107">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="c9caf-108">Määritä **Tapa**-kentän arvoksi **Laskupäivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="c9caf-108">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="c9caf-109">Järjestelmä luo uudelleenarvostustapahtuman, joka kumoaa edellisen ulkomaanvaluutan uudelleenarvostuksen.</span><span class="sxs-lookup"><span data-stu-id="c9caf-109">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="c9caf-110">Siksi avoimet tapahtumat arvostetaan niiden alkuperäisessä kirjanpitovaluutassa.</span><span class="sxs-lookup"><span data-stu-id="c9caf-110">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="c9caf-111">Päivitä versioon 1611.</span><span class="sxs-lookup"><span data-stu-id="c9caf-111">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="c9caf-112">Aja ulkomaanvaluutan uudelleenarvostus uudelleen osto- ja myyntireskontrassa.</span><span class="sxs-lookup"><span data-stu-id="c9caf-112">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="c9caf-113">Aseta tällä kertaa **Tapa**-kentän arvoksi **Vakio**.</span><span class="sxs-lookup"><span data-stu-id="c9caf-113">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="c9caf-114">Järjestelmä luo uuden uudelleenarvostustapahtuman, joka perustuu nykyisiin vaihtokursseihin.</span><span class="sxs-lookup"><span data-stu-id="c9caf-114">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="c9caf-115">Tähän tapahtumaan tallennetaan toteutumaton voitto/tappio ja oikea reskontrakirjanpitotili.</span><span class="sxs-lookup"><span data-stu-id="c9caf-115">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>
