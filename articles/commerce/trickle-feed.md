---
title: Vähittäismyyntitapahtumien syötteisiin perustuvien tilausten vähittäinen luominen
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commerce -sovelluksen tapahtumien syötteisiin perustuvien tilausten vähittäisestä luomisesta.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 79f99b9b401de3e3bcca6ec5a13a3b4f7bad6f8c
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766733"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="5a619-103">Vähittäismyyntitapahtumien syötteisiin perustuvien tilausten vähittäinen luominen</span><span class="sxs-lookup"><span data-stu-id="5a619-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5a619-104">Dynamics 365 Retail -sovelluksen versiossa 10.0.4 ja vanhemmissa versioissa laskelman kirjaaminen on päivän lopussa suoritettava toiminto, eli kaikki tapahtumat kirjataan päivän lopussa.</span><span class="sxs-lookup"><span data-stu-id="5a619-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="5a619-105">Suuret tapahtumat on siis käsiteltävä rajoitetun ajan puitteissa. Joskus tämä aiheuttaa virheitä latauksessa, lukituksissa ja laskelmien kirjaamisessa.</span><span class="sxs-lookup"><span data-stu-id="5a619-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="5a619-106">Jälleenmyyjät eivät myöskään pysty kirjaamaan tuottoa ja maksuja kirjanpitoon päivän aikana.</span><span class="sxs-lookup"><span data-stu-id="5a619-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="5a619-107">Retail-sovelluksen versiossa 10.0.5 olevan syötteisiin perustuvien tilausten vähittäisen luomisen avulla tapahtumat käsitellään päivän aikana. Vain maksuvälineiden taloushallinnon täsmäytyksen tapahtumat ja muut käteisvarojen hallintatapahtumat käsitellään päivän lopussa.</span><span class="sxs-lookup"><span data-stu-id="5a619-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="5a619-108">Tämä toiminto jakaa myyntitilausten, laskujen ja maksujen luomisen päivän ajalle. Tämä mahdollistaa paremman suorituskyvyn ja tuoton ja maksujen kirjaamisen lähes reaaliaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="5a619-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="5a619-109">Syötteisiin perustuvien vähittäin suoritettavien kirjausten käyttäminen</span><span class="sxs-lookup"><span data-stu-id="5a619-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="5a619-110">Jos haluat ottaa käyttöön vähittäiseen syöttöön perustuvan vähittäismyyntitapahtumien kirjaamisen, ota käyttöön **Vähittäismyyntilaskelmat – vähittäinen syöttö** -ominaisuus käyttämällä ominaisuuksien hallintaa.</span><span class="sxs-lookup"><span data-stu-id="5a619-110">To enable trickle feed-based posting of retail transactions, enable the feature named **Retail statements - Trickle feed** using Feature management.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="5a619-111">Varmista ennen ominaisuuden käyttöönottoa, ettei kirjausta odottavia laskelmia ei ole.</span><span class="sxs-lookup"><span data-stu-id="5a619-111">Before you enable the feature, make sure that no pending statements are waiting to be posted.</span></span>

2. <span data-ttu-id="5a619-112">Nykyinen laskelma-asiakirja jaetaan kahdeksi asiakirjatyypiksi: tapahtumaraportti ja raportti.</span><span class="sxs-lookup"><span data-stu-id="5a619-112">The current statement document will be split into two types: transactional statement and financial statement.</span></span>

      - <span data-ttu-id="5a619-113">Tapahtumaraportti sisältää kaikki kirjaamattomat ja tarkistetut tapahtumat. Se luo myyntitilaukset, myyntilaskut, maksu- ja alennuskirjauskansiot sekä tulo- ja kulutapahtumat määritettyinä ajankohtina.</span><span class="sxs-lookup"><span data-stu-id="5a619-113">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="5a619-114">Määritä tämä prosessi suoritettavaksi usein. Tällöin asiakirjat luodaan, kun tapahtumat ladataan Headquarters-sovellukseen P-työn kautta.</span><span class="sxs-lookup"><span data-stu-id="5a619-114">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="5a619-115">Koska tapahtumaraportti luo jo myyntitilaukset ja myyntilaskut, **Kirjaa varasto** -erätyötä ei tarvitse määrittää välttämättä.</span><span class="sxs-lookup"><span data-stu-id="5a619-115">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="5a619-116">Voit kuitenkin käyttää sitä, jos haluat varmistaa tiettyjen liiketoimintavaatimusten täyttymisen.</span><span class="sxs-lookup"><span data-stu-id="5a619-116">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="5a619-117">Raportti on määritetty niin, että se luodaan päivän lopuksi. Se tukee vain **Vuoro**-sulkemistapaa.</span><span class="sxs-lookup"><span data-stu-id="5a619-117">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="5a619-118">Laskelmaan kuuluu ainoastaan taloushallinnon täsmäytys ja se luo vain eri maksuvälineiden lasketun summan ja tapahtumasumman erotussummien kirjauskansiot sekä muut käteisvarojen hallintatapahtumien kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="5a619-118">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

3. <span data-ttu-id="5a619-119">Voit laskea tapahtumaraportin valitsemalla **Retail ja Commerce > Retailin ja Commercen IT > Myyntipistekirjaus > Laske tapahtumaraportit eräajona**.</span><span class="sxs-lookup"><span data-stu-id="5a619-119">To calculate the transactional statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="5a619-120">Voit kirjata tapahtumaraportit eräajona valitsemalla **Retail ja Commerce > Retailin ja Commercen IT > Myyntipistekirjaus > Kirjaa tapahtumaraportit eräajona**.</span><span class="sxs-lookup"><span data-stu-id="5a619-120">To post the transactional statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

4. <span data-ttu-id="5a619-121">Voit laskea raportin valitsemalla **Retail ja Commerce > Retailin ja Commercen IT > Myyntipistekirjaus > Laske raportit eräajona**.</span><span class="sxs-lookup"><span data-stu-id="5a619-121">To calculate the financial statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="5a619-122">Voit kirjata raportit eräajona valitsemalla **Retail ja Commerce > Retailin ja Commercen IT > Myyntipistekirjaus > Kirjaa raportit eräajona**.</span><span class="sxs-lookup"><span data-stu-id="5a619-122">To post the financial statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="5a619-123">Valikon vaihtoehdot **Retail ja Commerce > Retailin ja Commercen IT > Myyntipistekirjaus > Laske laskelmat eräajona** ja **Retail ja Commerce > Retailin ja Commercen IT > Myyntipistekirjaus > Kirjaa laskelmat eräajona** eivät ole enää tässä toiminnossa.</span><span class="sxs-lookup"><span data-stu-id="5a619-123">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="5a619-124">Tapahtumaraportti- ja Raportti-tyypit on kuitenkin mahdollista luoda manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="5a619-124">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="5a619-125">Siirry kohtaan **Retail ja Commerce > Kanavat > Myymälät** ja valitse **Laskelmat**.</span><span class="sxs-lookup"><span data-stu-id="5a619-125">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="5a619-126">Valitse **Uusi** ja valitse sitten luotavan laskelman tyyppi.</span><span class="sxs-lookup"><span data-stu-id="5a619-126">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="5a619-127">**Laskelmat**-sivun kentät ja sivun **Laskelmaryhmä**-kohdan toiminnot näyttävät tarvittavat tiedot ja toiminnot valitun laskelmatyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="5a619-127">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
