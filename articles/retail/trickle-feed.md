---
title: Vähittäismyyntitapahtumien syötteisiin perustuvien tilausten vähittäinen luominen
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Retail -sovelluksen vähittäismyyntitapahtumien syötteisiin perustuvien tilausten vähittäisestä luomisesta.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
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
ms.openlocfilehash: 80233a73dbffc7380503cf03703758b187824c2a
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622663"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a><span data-ttu-id="c4203-103">Vähittäismyyntitapahtumien syötteisiin perustuvien tilausten vähittäinen luominen (esikatselu)</span><span class="sxs-lookup"><span data-stu-id="c4203-103">Trickle feed-based order creation for retail store transactions (Public preview)</span></span>

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c4203-104">Dynamics 365 Retail -sovelluksen versiossa 10.0.4 ja vanhemmissa versioissa vähittäismyyntilaskelman kirjaaminen on päivän lopussa suoritettava toiminto, eli kaikki tapahtumat kirjataan päivän lopussa.</span><span class="sxs-lookup"><span data-stu-id="c4203-104">In Dynamics 365 Retail versions 10.0.4 and earlier, retail statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="c4203-105">Suuret tapahtumat on siis käsiteltävä rajoitetun ajan puitteissa. Joskus tämä aiheuttaa virheitä latauksessa, lukituksissa ja laskelmien kirjaamisessa.</span><span class="sxs-lookup"><span data-stu-id="c4203-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="c4203-106">Jälleenmyyjät eivät myöskään pysty kirjaamaan tuottoa ja maksuja kirjanpitoon päivän aikana.</span><span class="sxs-lookup"><span data-stu-id="c4203-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="c4203-107">Retail-sovelluksen versiossa 10.0.5 olevan syötteisiin perustuvien tilausten vähittäisen luomisen esikatselun avulla tapahtumat käsitellään päivän aikana. Vain maksuvälineiden taloushallinnon täsmäytyksen tapahtumat ja muut käteisvarojen hallintatapahtumat käsitellään päivän lopussa.</span><span class="sxs-lookup"><span data-stu-id="c4203-107">With the public preview of trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="c4203-108">Tämä toiminto jakaa myyntitilausten, laskujen ja maksujen luomisen päivän ajalle. Tämä mahdollistaa paremman suorituskyvyn ja tuoton ja maksujen kirjaamisen lähes reaaliaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="c4203-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="c4203-109">Syötteisiin perustuvien vähittäin suoritettavien kirjausten käyttäminen</span><span class="sxs-lookup"><span data-stu-id="c4203-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="c4203-110">Jos haluat ottaa vähittäismyyntitapahtumien syötteisiin perustuvien kirjausten vähittäisen suorittamisen käyttöön, siirry kohtaan **Järjestelmän hallinta > Asetukset > Käyttöoikeuden konfiguraatio** ja poista **Vähittäismyyntilaskelmat**-avain käytöstä.</span><span class="sxs-lookup"><span data-stu-id="c4203-110">To enable trickle feed-based posting of retail transactions, go to **System administration > Set up > License configuration** and disable the the **Retail statements** key.</span></span>

2. <span data-ttu-id="c4203-111">Ota samalla sivulla käyttöön **Vähittäismyyntilaskelmat (vähittäinen syöttö) – esikatselu** -käyttöoikeusavain.</span><span class="sxs-lookup"><span data-stu-id="c4203-111">On the same page, enable the **Retail statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="c4203-112">Varmista tämän avaimen käyttöönoton yhteydessä, että kirjausta odottavia laskelmia ei ole.</span><span class="sxs-lookup"><span data-stu-id="c4203-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

> [!Important]
> <span data-ttu-id="c4203-113">Varmista ennen **Vähittäismyyntilaskelmat (vähittäinen syöttö) – esikatselu** -käyttöoikeusavaimen käyttöönottoa, että kirjausta odottavia laskelmia ei ole.</span><span class="sxs-lookup"><span data-stu-id="c4203-113">Before you enable the **Retail statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="c4203-114">Nykyinen laskelma-asiakirja jaetaan kahteen eri tyyppiin, jotka ovat Tapahtumaraportti ja Raportti.</span><span class="sxs-lookup"><span data-stu-id="c4203-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="c4203-115">Tapahtumaraportti sisältää kaikki kirjaamattomat ja tarkistetut vähittäismyyntitapahtumat. Se luo myyntitilaukset, myyntilaskut, maksu- ja alennuskirjauskansiot sekä tulo- ja kulutapahtumat määritettyinä ajankohtina.</span><span class="sxs-lookup"><span data-stu-id="c4203-115">The transactional statement will pick up all unposted and validated retail transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="c4203-116">Määritä tämä prosessi suoritettavaksi usein. Tällöin asiakirjat luodaan, kun vähittäismyyntitapahtumat ladataan Retail Headquarters -sovellukseen P-työn kautta.</span><span class="sxs-lookup"><span data-stu-id="c4203-116">You should configure this process to run at a high frequency so that documents are created when the retail transactions are uploaded into Retail Headquarters through the P-job.</span></span> <span data-ttu-id="c4203-117">Koska tapahtumaraportti luo jo myyntitilaukset ja myyntilaskut, **Kirjaa varasto** -erätyötä ei tarvitse määrittää välttämättä.</span><span class="sxs-lookup"><span data-stu-id="c4203-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="c4203-118">Voit kuitenkin käyttää sitä, jos haluat varmistaa tiettyjen liiketoimintavaatimusten täyttymisen.</span><span class="sxs-lookup"><span data-stu-id="c4203-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="c4203-119">Raportti on määritetty niin, että se luodaan päivän lopuksi. Se tukee vain **Vuoro**-sulkemistapaa.</span><span class="sxs-lookup"><span data-stu-id="c4203-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="c4203-120">Laskelmaan kuuluu ainoastaan taloushallinnon täsmäytys ja se luo vain eri maksuvälineiden lasketun summan ja tapahtumasumman erotussummien kirjauskansiot sekä muut käteisvarojen hallintatapahtumien kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="c4203-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between           counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="c4203-121">Voit laskea tapahtumaraportin valitsemalla **Vähittäismyynti > Vähittäismyynnin IT > Myyntipistekirjaus > Laske tapahtumaraportit eräajona**.</span><span class="sxs-lookup"><span data-stu-id="c4203-121">To calculate the transactional statement, click **Retail > Retail IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="c4203-122">Voit kirjata tapahtumaraportin laskelmat eräajona valitsemalla **Vähittäismyynti > Vähittäismyynnin IT > Myyntipistekirjaus > Kirjaa tapahtumaraportit eräajona**.</span><span class="sxs-lookup"><span data-stu-id="c4203-122">To post the transactional statement statements in batch, click **Retail > Retail IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="c4203-123">Voit laskea raportin valitsemalla **Vähittäismyynti > Vähittäismyynnin IT > Myyntipistekirjaus > Laske raportit eräajona**.</span><span class="sxs-lookup"><span data-stu-id="c4203-123">To calculate the financial statement, click **Retail > Retail IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="c4203-124">Voit kirjata raportit eräajona valitsemalla **Vähittäismyynti > Vähittäismyynnin IT > Myyntipistekirjaus > Kirjaa raportit eräajona**.</span><span class="sxs-lookup"><span data-stu-id="c4203-124">To post the financial statements in batch, click **Retail > Retail IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="c4203-125">Valikon vaihtoehdot **Vähittäismyynti > Vähittäismyynnin IT > Myyntipistekirjaus > Laske laskelmat eräajona** ja **Vähittäismyynti > Vähittäismyynnin IT > Myyntipistekirjaus > Kirjaa laskelmat eräajona** eivät ole enää tässä toiminnossa.</span><span class="sxs-lookup"><span data-stu-id="c4203-125">The menu items **Retail > Retail IT > POS Posting > Calculate statements in batch** and **Retail > Retail IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="c4203-126">Tapahtumaraportti- ja Raportti-tyypit on kuitenkin mahdollista luoda manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="c4203-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="c4203-127">Siirry kohtaan **Vähittäismyynti > Kanavat > Vähittäismyymälät** ja valitse **Vähittäismyyntilaskelmat**.</span><span class="sxs-lookup"><span data-stu-id="c4203-127">Go to **Retail > Channels > Retail stores** and click **Retail statements**.</span></span> <span data-ttu-id="c4203-128">Valitse **Uusi** ja valitse sitten luotavan laskelman tyyppi.</span><span class="sxs-lookup"><span data-stu-id="c4203-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="c4203-129">**Vähittäismyyntilaskelmat**-sivun kentät ja sivun **Laskelmaryhmä**-kohdan toiminnot näyttävät tarvittavat tiedot ja toiminnot valitun laskelmatyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="c4203-129">Fields on the **Retail statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
