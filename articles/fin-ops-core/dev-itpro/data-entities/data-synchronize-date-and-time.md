---
title: Tuontitöiden päivämäärän ja ajan synkronoiminen
description: Kun töitä tuodessa käytetään UTC-aikavyöhykkeitä aikavyöhykkeiden muunnot eivät aiheuta ongelmia.
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c0ec805a20a525989e0133e5dffb29ce3fed39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748666"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="469ab-103">Tuontitöiden päivämäärän ja ajan synkronoiminen</span><span class="sxs-lookup"><span data-stu-id="469ab-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="469ab-104">On tärkeää, että tuontityön aikavyöhykkeeksi määritetään koordinoitu yleisaika (UTC).</span><span class="sxs-lookup"><span data-stu-id="469ab-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="469ab-105">Tuoduissa tiedoissa voi näkyä odottamattomia päivämääriä ja aikoja, jos käytössä on jokin muu asetus.</span><span class="sxs-lookup"><span data-stu-id="469ab-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="469ab-106">Jos asetus ei ole oikea, tuontiprosessi muuntaa UTC-päivämäärän paikalliseen muotoon ja järjestelmäasetukset muuntavat sen sitten uudelleen.</span><span class="sxs-lookup"><span data-stu-id="469ab-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="469ab-107">Tämän kaksoismuunnon vuoksi päivämäärät muuttavat sovellusten välillä.</span><span class="sxs-lookup"><span data-stu-id="469ab-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="469ab-108">Kaksoismuunto voi aiheuttaa esimerkiksi sen, että työntekijällä on eri alkamispäivä Dynamics 365 Human Resourcesissa ja Dynamics 365 Financessa paikallisten aikavyöhykkeiden erojen vuoksi.</span><span class="sxs-lookup"><span data-stu-id="469ab-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="469ab-109">Tämä ongelma ratkaistaan määrittämällä tuontityöhön UTC-aika.</span><span class="sxs-lookup"><span data-stu-id="469ab-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="469ab-110">Valitse Dynamics 365 Finance and Operationsissa **Tiedonhallinta**.</span><span class="sxs-lookup"><span data-stu-id="469ab-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="469ab-111">Valitse ensin **Tuo projektit** ja sitten projekti.</span><span class="sxs-lookup"><span data-stu-id="469ab-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="469ab-112">Valitse **Lähteen päivämäärämuoto** kohdassa **CSV-Unicode**.</span><span class="sxs-lookup"><span data-stu-id="469ab-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="469ab-113">[![Lähteen päivämäärämuodon muuttaminen UTC-muotoon](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="469ab-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="469ab-114">Muuta **Aikavyöhyke**-asetukseksi **Koordinoitu yleisaika** ja muuta **Kieli**-asetukseksi **En-US**.</span><span class="sxs-lookup"><span data-stu-id="469ab-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]