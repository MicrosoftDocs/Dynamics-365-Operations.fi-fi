---
title: Vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistaja
description: Tässä aiheessa kuvataan vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistajan toiminnot ohjelmassa Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "302231"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="de294-103">Vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistaja</span><span class="sxs-lookup"><span data-stu-id="de294-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="de294-104">Tässä aiheessa kuvataan vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistajan, joka on käytössä versiosta 8.1.3. alkaen, toiminnot ohjelmassa Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="de294-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="de294-105">Yhdenmukaisuuden tarkistaja tunnistaa ja osoittaa yhtäpitämättömät tapahtumat, ennen kuin laskelmien kirjaamisprosessi ottaa ne käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="de294-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="de294-106">Kun laskelma kirjataan Retailissa, kirjaus saattaa epäonnistua vähittäismyynnin tauluissa olevien yhtäpitämättömien tietojen johdosta.</span><span class="sxs-lookup"><span data-stu-id="de294-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="de294-107">Ongelma tiedoissa saattaa johtua odottamattomista ongelmista myyntipistesovelluksessa, tai siitä, että tapahtumat on tuotu virheellisesti kolmannen osapuolen myyntipistejärjestelmistä.</span><span class="sxs-lookup"><span data-stu-id="de294-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="de294-108">Nämä ristiriidat voivat näyttää esimerkiksi seuraavanlaisilta:</span><span class="sxs-lookup"><span data-stu-id="de294-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="de294-109">Tapahtuman kokonaissumma otsikkotaulussa ei vastaa riveillä olevaa tapahtuman kokonaissummaa.</span><span class="sxs-lookup"><span data-stu-id="de294-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="de294-110">Otsikkotaulun rivimäärä ei vastaa transaktiotaulun rivimäärää.</span><span class="sxs-lookup"><span data-stu-id="de294-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="de294-111">Otsikkotaulussa olevat verot eivät vastaa riveillä olevaa veron määrää.</span><span class="sxs-lookup"><span data-stu-id="de294-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="de294-112">Kun laskelmien kirjausprosessi havaitsee epäyhtenäisiä tapahtumia, luodaan yhteensopimattomia myyntilaskuja ja maksutietoja, ja koko laskelmien kirjausprosessi epäonnistuu tämän seurauksena.</span><span class="sxs-lookup"><span data-stu-id="de294-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="de294-113">Laskelmien palauttaminen sellaisesta tilasta vaatii monimutkaisia tietojen korjauksia moneen transaktiotauluun.</span><span class="sxs-lookup"><span data-stu-id="de294-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="de294-114">Vähittäismyynnin tapahtumien yhdenmukaisuuden tarkistaja estää tällaiset ongelmat.</span><span class="sxs-lookup"><span data-stu-id="de294-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="de294-115">Seuraavassa kaaviossa havainnollistetaan kirjausprosessi, jossa tapahtumien yhdenmukaisuuden tarkistaja on käytössä.</span><span class="sxs-lookup"><span data-stu-id="de294-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="de294-116">![Laskelman kirjausprosessi, jossa tapahtumien yhdenmukaisuuden tarkistaja on käytössä](./media/validchecker.png "Laskelman kirjausprosessi, jossa tapahtumien yhdenmukaisuuden tarkistaja on käytössä")</span><span class="sxs-lookup"><span data-stu-id="de294-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transsaction consistency checker")</span></span>

<span data-ttu-id="de294-117">**Vahvista myymälän tapahtumat** -eräajoprosessi tarkistaa seuraavien seikkojen yhdenmukaisuuden vähittäismyynnin transaktiotauluista.</span><span class="sxs-lookup"><span data-stu-id="de294-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="de294-118">Asiakkaan tili - Tarkistaa, että vähittäismyynnin transaktiotauluissa oleva asiakastili on olemassa asiakkaan alkuperäisissä tiedoissa pääkonttorissa.</span><span class="sxs-lookup"><span data-stu-id="de294-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="de294-119">Rivien määrä - Tarkistaa, että rivien määrä transaktioiden otsikkotaulussa vastaa myynnin transaktiotauluissa olevien rivien määrää.</span><span class="sxs-lookup"><span data-stu-id="de294-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="de294-120">Määritä yhdenmukaisuuden tarkistaja</span><span class="sxs-lookup"><span data-stu-id="de294-120">Set up the consistency checker</span></span>
<span data-ttu-id="de294-121">Määritä "Vahvista myymälän tapahtumat" -eräajoprosessi tapahtumaan säännöllisesti paikassa **Vähittäismyynti \> Vähittäismyynti IT \> Myyntipisteen laskenta**.</span><span class="sxs-lookup"><span data-stu-id="de294-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="de294-122">Eräajoprosessi voidaan aikatauluttaa myymälän organisaatiohierarkian perusteella samaan tapaan kuin "Laskelman laskeminen erässä" - ja "Laskelman kirjaaminen erässä" -prosessit on määritetty.</span><span class="sxs-lookup"><span data-stu-id="de294-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="de294-123">Suosittelemme määrittelemään tämän eräajoprosessin käynnistymään useita kertoja päivässä ja aikatauluttamaan sen siten, että se käynnistyy jokaisen P-tehtävän suorituskerran lopuksi.</span><span class="sxs-lookup"><span data-stu-id="de294-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="de294-124">Tarkistusprosessin tulokset</span><span class="sxs-lookup"><span data-stu-id="de294-124">Results of validation process</span></span>
<span data-ttu-id="de294-125">Eräajoprosessin suorittaman tarkistuksen tulokset yhdistetään asianmukaiseen vähittäismyynnin tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="de294-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="de294-126">**Vahvistuksen tila** -kenttä vähittäismyynnin tapahtumatietueessa on joko **Onnistui** tai **Virhe**, ja edellisen tarkistusajon päivämäärä näkyy **Edellisen tarkistuksen aika** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="de294-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="de294-127">Katso kuvaavampi tarkistuksen epäonnistumiseen liittyvä virheteksti valitsemalla asiaankuuluva vähittäismyymälän transaktiotietue ja napauttamalla **Oikeellisuustarkistusvirheet**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="de294-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="de294-128">Tapahtumia, jotka eivät läpäise tarkistusta, ja tapahtumia, joita ei ole vielä tarkistettu, ei tuoda laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="de294-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="de294-129">”Laske laskelma” -prosessin aikana käyttäjille lähetetään ilmoitus, jos on tapahtumia, jotka olisi voitu sisällyttää laskelmaan mutta joita ei ole siihen sisällytetty.</span><span class="sxs-lookup"><span data-stu-id="de294-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="de294-130">Jos löydetään tarkistusvirhe, ainoa tapa sen korjaamiseksi on ottaa yhteyttä Microsoftin tukeen.</span><span class="sxs-lookup"><span data-stu-id="de294-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="de294-131">Tulevissa versioissa ohjelmaan lisätään toiminto, jonka avulla käyttäjät voivat korjata käyttöliittymän kautta ne tietueet, jotka aiheuttivat virheen.</span><span class="sxs-lookup"><span data-stu-id="de294-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="de294-132">Tapahtumaloki- ja auditointiominaisuudet tulevat myös saataville muutoshistorian seurantaa varten.</span><span class="sxs-lookup"><span data-stu-id="de294-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="de294-133">Tarkistussääntöjä useamman mahdollisen tilanteen kattamiseksi lisätään tulevissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="de294-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>
