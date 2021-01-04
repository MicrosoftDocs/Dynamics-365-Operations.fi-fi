---
title: Vuokrasopimuksen parametrien määrittäminen (esiversio)
description: Tässä ohjeaiheessa kuvataan resurssin vuokrauksen asetukset. Niitä ovat esimerkiksi suojauksen tiedot ja kirjanpidon asetukset.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f71006570cd8f2bdc0385388eae0800cd29d3ec8
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442970"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="939a0-103">Vuokrasopimuksen parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="939a0-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="939a0-104">Useat määritysasetukset vaikuttavat siihen, miten resurssin vuokraus toimii.</span><span class="sxs-lookup"><span data-stu-id="939a0-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="939a0-105">Näitä asetuksia ovat esimerkiksi kirjauskansioiden nimet, yleiset parametrit ja kirjausprofiilin asetukset.</span><span class="sxs-lookup"><span data-stu-id="939a0-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="939a0-106">Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Resurssin vuokrausparametrit**.</span><span class="sxs-lookup"><span data-stu-id="939a0-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="939a0-107">Valitse **Vuokrasopimukset**-välilehdessä **Yleistiedot**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="939a0-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="939a0-108">**Salli manuaalisen luokituksen ohitus** -parametri määrittää, voidaanko vuokrauksen luokitus ohittaa, ennen kuin maksuaikataulu on vahvistettu.</span><span class="sxs-lookup"><span data-stu-id="939a0-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="939a0-109">**Yksiköiden välinen erä** -parametri määrittää, voitko kirjata muita yrityksiä nykyisestä yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="939a0-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="939a0-110">Jos tämä parametri on käytössä, voit luoda sille yritykselle kirjauskansiovientejä, jonka käyttöoikeus sinulla on.</span><span class="sxs-lookup"><span data-stu-id="939a0-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="939a0-111">Määritä **Salli vahvistettujen vuokrasopimusten poistaminen** -vaihtoehdon arvoksi **Kyllä**, jos haluat sallia vahvistetut maksuaikataulut omaavien vuokrasopimusten poistamisen.</span><span class="sxs-lookup"><span data-stu-id="939a0-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="939a0-112">Vuokrasopimuksia ei voi poistaa, jos niihin liittyy kirjattuja tai kirjaamattomia tapahtumia tämän asetuksen määrityksestä huolimatta.</span><span class="sxs-lookup"><span data-stu-id="939a0-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="939a0-113">Et voi palauttaa vuokrasopimuksen tietuetta sen poistamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="939a0-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="939a0-114">Jos lataat kaikki poistetun vuokrasopimuksen tietueet joko manuaalisesti tai tietoentiteettien kautta, ladattuja tietoja käsitellään uusina, ei aiemmin luodun vuokrasopimuksen päivityksinä.</span><span class="sxs-lookup"><span data-stu-id="939a0-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="939a0-115">Jos määrität tämän asetuksen arvoksi **Kyllä** ja kirjan siirtymätyyppi on **Kumulatiivinen päivitysvaihto A tai B**, järjestelmä määrittää **Inkrementaalinen lainakorko** -kentän arvoksi **Inkrementaalinen lainakorko siirtymässä** -kentän arvon **Kirjan asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="939a0-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="939a0-116">Jos tämän asetuksen arvoksi on määritetty **Ei**, päävuokrasopimuksen määräksi annetaan **Inkrementaalinen lainakorko** -kentän arvo **Kirjan tiedot** -sivulla riippumatta kirjan siirtymätyypistä.</span><span class="sxs-lookup"><span data-stu-id="939a0-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="939a0-117">Määritä **Salli poistojen peruutukset suljetun kirjan versiossa** -vaihtoehdon arvoksi **Kyllä**, jos poistokulutapahtumia voi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="939a0-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="939a0-118">Kulutapahtumat voidaan peruuttaa myös kirjan version sulkemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="939a0-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="939a0-119">On suositeltavaa säilyttää tämän asetuksen arvona **Ei**.</span><span class="sxs-lookup"><span data-stu-id="939a0-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="939a0-120">Tämän asetuksen määritystä käytetään tarkistuksessa ja ohjausobjektissa, jotta suljettua kirjan versiota ei poisteta vahingossa.</span><span class="sxs-lookup"><span data-stu-id="939a0-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="939a0-121">Jos säilytät asetuksen arvona **Ei**, voit säilyttää nettokirjanpitoarvon ja tulevien poistojen laskelmat ajantasalla.</span><span class="sxs-lookup"><span data-stu-id="939a0-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>
