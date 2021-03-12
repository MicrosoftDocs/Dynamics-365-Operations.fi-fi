---
title: Tuontitöiden päivämäärän ja ajan synkronoiminen
description: Kun töitä tuodessa käytetään UTC-aikavyöhykkeitä aikavyöhykkeiden muunnot eivät aiheuta ongelmia.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae04b09a68e64d6d70c0329e689ab08c3903fca0
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798716"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="fcd24-103">Tuontitöiden päivämäärän ja ajan synkronoiminen</span><span class="sxs-lookup"><span data-stu-id="fcd24-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fcd24-104">On tärkeää, että tuontityön aikavyöhykkeeksi määritetään koordinoitu yleisaika (UTC).</span><span class="sxs-lookup"><span data-stu-id="fcd24-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="fcd24-105">Tuoduissa tiedoissa voi näkyä odottamattomia päivämääriä ja aikoja, jos käytössä on jokin muu asetus.</span><span class="sxs-lookup"><span data-stu-id="fcd24-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="fcd24-106">Jos asetus ei ole oikea, tuontiprosessi muuntaa UTC-päivämäärän paikalliseen muotoon ja järjestelmäasetukset muuntavat sen sitten uudelleen.</span><span class="sxs-lookup"><span data-stu-id="fcd24-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="fcd24-107">Tämän kaksoismuunnon vuoksi päivämäärät muuttavat sovellusten välillä.</span><span class="sxs-lookup"><span data-stu-id="fcd24-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="fcd24-108">Kaksoismuunto voi aiheuttaa esimerkiksi sen, että työntekijällä on eri alkamispäivä Dynamics 365 Human Resourcesissa ja Dynamics 365 Financessa paikallisten aikavyöhykkeiden erojen vuoksi.</span><span class="sxs-lookup"><span data-stu-id="fcd24-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="fcd24-109">Tämä ongelma ratkaistaan määrittämällä tuontityöhön UTC-aika.</span><span class="sxs-lookup"><span data-stu-id="fcd24-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="fcd24-110">Valitse Dynamics 365 Finance and Operationsissa **Tiedonhallinta**.</span><span class="sxs-lookup"><span data-stu-id="fcd24-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="fcd24-111">Valitse ensin **Tuo projektit** ja sitten projekti.</span><span class="sxs-lookup"><span data-stu-id="fcd24-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="fcd24-112">Valitse **Lähteen päivämäärämuoto** kohdassa **CSV-Unicode**.</span><span class="sxs-lookup"><span data-stu-id="fcd24-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="fcd24-113">[![Lähteen päivämäärämuodon muuttaminen UTC-muotoon](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="fcd24-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="fcd24-114">Muuta **Aikavyöhyke**-asetukseksi **Koordinoitu yleisaika** ja muuta **Kieli**-asetukseksi **En-US**.</span><span class="sxs-lookup"><span data-stu-id="fcd24-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>


