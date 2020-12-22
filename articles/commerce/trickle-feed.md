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
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458945"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Vähittäismyyntitapahtumien syötteisiin perustuvien tilausten vähittäinen luominen

[!include [banner](includes/banner.md)]

Dynamics 365 Retail -sovelluksen versiossa 10.0.4 ja vanhemmissa versioissa laskelman kirjaaminen on päivän lopussa suoritettava toiminto, eli kaikki tapahtumat kirjataan päivän lopussa. Suuret tapahtumat on siis käsiteltävä rajoitetun ajan puitteissa. Joskus tämä aiheuttaa virheitä latauksessa, lukituksissa ja laskelmien kirjaamisessa. Jälleenmyyjät eivät myöskään pysty kirjaamaan tuottoa ja maksuja kirjanpitoon päivän aikana.

Retail-sovelluksen versiossa 10.0.5 olevan syötteisiin perustuvien tilausten vähittäisen luomisen avulla tapahtumat käsitellään päivän aikana. Vain maksuvälineiden taloushallinnon täsmäytyksen tapahtumat ja muut käteisvarojen hallintatapahtumat käsitellään päivän lopussa. Tämä toiminto jakaa myyntitilausten, laskujen ja maksujen luomisen päivän ajalle. Tämä mahdollistaa paremman suorituskyvyn ja tuoton ja maksujen kirjaamisen lähes reaaliaikaisesti. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Syötteisiin perustuvien vähittäin suoritettavien kirjausten käyttäminen
  
1. Jos haluat ottaa käyttöön vähittäiseen syöttöön perustuvan vähittäismyyntitapahtumien kirjaamisen, ota käyttöön **Vähittäismyyntilaskelmat – vähittäinen syöttö** -ominaisuus käyttämällä ominaisuuksien hallintaa.

    > [!IMPORTANT]
    > Varmista ennen ominaisuuden käyttöönottoa, ettei kirjausta odottavia laskelmia ei ole.

2. Nykyinen laskelma-asiakirja jaetaan kahdeksi asiakirjatyypiksi: tapahtumaraportti ja raportti.

      - Tapahtumaraportti sisältää kaikki kirjaamattomat ja tarkistetut tapahtumat. Se luo myyntitilaukset, myyntilaskut, maksu- ja alennuskirjauskansiot sekä tulo- ja kulutapahtumat määritettyinä ajankohtina. Määritä tämä prosessi suoritettavaksi usein. Tällöin asiakirjat luodaan, kun tapahtumat ladataan Headquarters-sovellukseen P-työn kautta. Koska tapahtumaraportti luo jo myyntitilaukset ja myyntilaskut, **Kirjaa varasto** -erätyötä ei tarvitse määrittää välttämättä. Voit kuitenkin käyttää sitä, jos haluat varmistaa tiettyjen liiketoimintavaatimusten täyttymisen.  
      
     - Raportti on määritetty niin, että se luodaan päivän lopuksi. Se tukee vain **Vuoro**-sulkemistapaa. Laskelmaan kuuluu ainoastaan taloushallinnon täsmäytys ja se luo vain eri maksuvälineiden lasketun summan ja tapahtumasumman erotussummien kirjauskansiot sekä muut käteisvarojen hallintatapahtumien kirjauskansiot.   

3. Voit laskea tapahtumaraportin valitsemalla **Retail ja Commerce > Retailin ja Commercen IT > Myyntipistekirjaus > Laske tapahtumaraportit eräajona**. Voit kirjata tapahtumaraportit eräajona valitsemalla **Retail ja Commerce > Retailin ja Commercen IT > Myyntipistekirjaus > Kirjaa tapahtumaraportit eräajona**.

4. Voit laskea raportin valitsemalla **Retail ja Commerce > Retailin ja Commercen IT > Myyntipistekirjaus > Laske raportit eräajona**. Voit kirjata raportit eräajona valitsemalla **Retail ja Commerce > Retailin ja Commercen IT > Myyntipistekirjaus > Kirjaa raportit eräajona**.

> [!NOTE]
> Valikon vaihtoehdot **Retail ja Commerce > Retailin ja Commercen IT > Myyntipistekirjaus > Laske laskelmat eräajona** ja **Retail ja Commerce > Retailin ja Commercen IT > Myyntipistekirjaus > Kirjaa laskelmat eräajona** eivät ole enää tässä toiminnossa.

Tapahtumaraportti- ja Raportti-tyypit on kuitenkin mahdollista luoda manuaalisesti. Siirry kohtaan **Retail ja Commerce > Kanavat > Myymälät** ja valitse **Laskelmat**. Valitse **Uusi** ja valitse sitten luotavan laskelman tyyppi. **Laskelmat**-sivun kentät ja sivun **Laskelmaryhmä**-kohdan toiminnot näyttävät tarvittavat tiedot ja toiminnot valitun laskelmatyypin mukaan.
