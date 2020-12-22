---
title: Tuottokirjausten yleiskatsaus
description: Tässä ohjeaiheessa on tietoja tuottokirjausominaisuudesta. Tämä ominaisuus tarjoaa joustavan kehyksen, jonka avulla voit määrittää yrityskohtaiset säännöt, joiden avulla voidaan tunnistaa moniosaisten tilausten tuottohinta ja tuottoaikataulu.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 92af567499c1a8a23cd4d51e5bab48eaab2d8422
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2020
ms.locfileid: "4458957"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="8aa78-104">Tuottokirjausten yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8aa78-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="8aa78-105">Tuoton kirjaustoimintoa ei voi ottaa käyttöön ominaisuuksien hallinnan avulla.</span><span class="sxs-lookup"><span data-stu-id="8aa78-105">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="8aa78-106">Tällä hetkellä se on otettava käyttöön konfigurointiavainten avulla.</span><span class="sxs-lookup"><span data-stu-id="8aa78-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="8aa78-107">Useita elementtejä myyvien yritysten, kuten tuotteiden, palveluiden ja tilausten, on pystyttävä purkamaan moniosaiset tilaukset, jotta tuotto voidaan kirjata yrityskohtaisia ja toimialakohtaisia ohjeita noudattaen.</span><span class="sxs-lookup"><span data-stu-id="8aa78-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="8aa78-108">Yleensä tuoton kirjausprosessia voidaan käyttää seuraavien tehtävien suorittamiseen:</span><span class="sxs-lookup"><span data-stu-id="8aa78-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="8aa78-109">Kohdista tuotto sen takaamiseksi, että asianmukainen tuottohinta tunnistetaan moniosaisten tilausten komponenttien arvon perusteella.</span><span class="sxs-lookup"><span data-stu-id="8aa78-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="8aa78-110">Siirrä tuottoa käyttäen tuottoaikataulua, joka edustaa sopimuksen voimassaoloaikaa sekä prosenttiosuuksia tuoton kirjaamiselle ajan kuluessa.</span><span class="sxs-lookup"><span data-stu-id="8aa78-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="8aa78-111">[Tuoton tunnistaminenDynamics 365 Financessa](https://youtu.be/v3amIsiqvoo) -video (yllä) kuuluu [Finance and Operations -soittolistaan](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) YouTubessa.</span><span class="sxs-lookup"><span data-stu-id="8aa78-111">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="8aa78-112">Tuoton kirjausominaisuus tarjoaa joustavan kehyksen, jonka avulla voit määrittää yrityskohtaiset säännöt, joiden avulla voidaan tunnistaa tuottohinta ja tuottoaikataulu.</span><span class="sxs-lookup"><span data-stu-id="8aa78-112">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="8aa78-113">Vapautettuja tuotteita käytetään myyntitilausasiakirjojen tuottojen kirjaamisen tukemiseen.</span><span class="sxs-lookup"><span data-stu-id="8aa78-113">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="8aa78-114">Vapautetut tuotteet sisältävät asetukset, joita tarvitaan tuottohinnan ja tuottoaikataulun määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="8aa78-114">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="8aa78-115">Myyntitilaus voi olla peräisin aika- ja materiaaliprojektista.</span><span class="sxs-lookup"><span data-stu-id="8aa78-115">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="8aa78-116">Yritykset voivat käyttää tuottoajoitustoimintoa käyttämättä tuottohintatoimintoa.</span><span class="sxs-lookup"><span data-stu-id="8aa78-116">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="8aa78-117">Tämän vuoksi myyntitilausrivien hintaa käytetään joko tuottona tai lykättynä tuottona.</span><span class="sxs-lookup"><span data-stu-id="8aa78-117">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="8aa78-118">Jos myyntitilausrivillä on tuottoaikataulu, myyntitilausrivin hintaa lykätään.</span><span class="sxs-lookup"><span data-stu-id="8aa78-118">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="8aa78-119">Jos myyntitilausrivillä ei ole tuottoaikataulua, myyntitilausrivin hinta kirjataan tuottotilille laskutettaessa.</span><span class="sxs-lookup"><span data-stu-id="8aa78-119">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="8aa78-120">Tuottohinta lasketaan joko silloin, kun myyntitilaus vahvistetaan tai laskun kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="8aa78-120">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="8aa78-121">Jos haluat esikatsella tuottohintaa ennen laskun kirjaamista, sinun on vahvistettava myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="8aa78-121">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="8aa78-122">Kun myyntitilaus on vahvistettu, myös odotettu tuottoaikataulu luodaan, jos jollakin myyntitilausrivillä on tuottoaikataulu.</span><span class="sxs-lookup"><span data-stu-id="8aa78-122">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="8aa78-123">Kun myyntitilaus laskutetaan, odotettu tuottoaikataulu poistetaan ja odotettu tuottoaikataulu korvataan todellisella tuoton kirjausaikataululla.</span><span class="sxs-lookup"><span data-stu-id="8aa78-123">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="8aa78-124">Myynnin tuottoaikataulun tiedot säilyvät kunkin myyntitilausrivin osalta.</span><span class="sxs-lookup"><span data-stu-id="8aa78-124">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="8aa78-125">Tämän vuoksi tuottokirjauksen hallinta voi tarkastella tietoja ja vapauttaa rivit tuottoihin, kun sopimusvelvoite on täytetty.</span><span class="sxs-lookup"><span data-stu-id="8aa78-125">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="8aa78-126">Kunkin kauden lopussa tuottokirjauksen hallinta voi luoda tuottokirjauskansion, joka vapauttaa määritettynä päivänä tai ennen sitä erääntyvät aikataulun rivit.</span><span class="sxs-lookup"><span data-stu-id="8aa78-126">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="8aa78-127">Tätä tuottokirjauskansiota ei kirjata heti.</span><span class="sxs-lookup"><span data-stu-id="8aa78-127">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="8aa78-128">Tämän vuoksi tuottokirjauksen hallinta voi tarkistaa, että oikeat summat vapautetaan laskennallisista tuloista todellisiin tuloihin.</span><span class="sxs-lookup"><span data-stu-id="8aa78-128">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="8aa78-129">Jos sopimukseen perustuva muutos aiheuttaa uuden myyntitilausrivin lisäämisen joko olemassa olevaan myyntitilaukseen tai uuteen myyntitilaukseen, uudelleenkohdistamista voidaan käyttää korjaamaan myyntitilausten kaikkien rivien tuottohinta.</span><span class="sxs-lookup"><span data-stu-id="8aa78-129">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
