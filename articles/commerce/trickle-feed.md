---
title: Vähittäismyyntitapahtumien syötteisiin perustuvien tilausten vähittäinen luominen
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commerce -sovelluksen tapahtumien syötteisiin perustuvien tilausten vähittäisestä luomisesta.
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
ms.openlocfilehash: 7d5812893edff24a60a0e2eb3607701ac47a8a78
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057148"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>Vähittäismyyntitapahtumien syötteisiin perustuvien tilausten vähittäinen luominen (esikatselu)

[!include [banner](includes/banner.md)]

Dynamics 365 Retail -sovelluksen versiossa 10.0.4 ja vanhemmissa versioissa laskelman kirjaaminen on päivän lopussa suoritettava toiminto, eli kaikki tapahtumat kirjataan päivän lopussa. Suuret tapahtumat on siis käsiteltävä rajoitetun ajan puitteissa. Joskus tämä aiheuttaa virheitä latauksessa, lukituksissa ja laskelmien kirjaamisessa. Jälleenmyyjät eivät myöskään pysty kirjaamaan tuottoa ja maksuja kirjanpitoon päivän aikana.

Retail-sovelluksen versiossa 10.0.5 olevan syötteisiin perustuvien tilausten vähittäisen luomisen esikatselun avulla tapahtumat käsitellään päivän aikana. Vain maksuvälineiden taloushallinnon täsmäytyksen tapahtumat ja muut käteisvarojen hallintatapahtumat käsitellään päivän lopussa. Tämä toiminto jakaa myyntitilausten, laskujen ja maksujen luomisen päivän ajalle. Tämä mahdollistaa paremman suorituskyvyn ja tuoton ja maksujen kirjaamisen lähes reaaliaikaisesti. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Syötteisiin perustuvien vähittäin suoritettavien kirjausten käyttäminen
  
1. Jos haluat ottaa tapahtumien syötteisiin perustuvien kirjausten vähittäisen suorittamisen käyttöön, siirry kohtaan **Järjestelmän hallinta > Asetukset > Käyttöoikeuden konfiguraatio** ja poista **Laskelmat**-avain käytöstä.

2. Ota samalla sivulla käyttöön **Laskelmat (vähittäinen syöttö) – esikatselu** -käyttöoikeusavain. Varmista tämän avaimen käyttöönoton yhteydessä, että kirjausta odottavia laskelmia ei ole. 

    > [!Important]
    > Varmista ennen **Laskelmat (vähittäinen syöttö) – esikatselu** -käyttöoikeusavaimen käyttöönottoa, että kirjausta odottavia laskelmia ei ole.

3. Nykyinen laskelma-asiakirja jaetaan kahteen eri tyyppiin, jotka ovat Tapahtumaraportti ja Raportti.

      - Tapahtumaraportti sisältää kaikki kirjaamattomat ja tarkistetut tapahtumat. Se luo myyntitilaukset, myyntilaskut, maksu- ja alennuskirjauskansiot sekä tulo- ja kulutapahtumat määritettyinä ajankohtina. Määritä tämä prosessi suoritettavaksi usein. Tällöin asiakirjat luodaan, kun tapahtumat ladataan Headquarters-sovellukseen P-työn kautta. Koska tapahtumaraportti luo jo myyntitilaukset ja myyntilaskut, **Kirjaa varasto** -erätyötä ei tarvitse määrittää välttämättä. Voit kuitenkin käyttää sitä, jos haluat varmistaa tiettyjen liiketoimintavaatimusten täyttymisen.  
      
     - Raportti on määritetty niin, että se luodaan päivän lopuksi. Se tukee vain **Vuoro**-sulkemistapaa. Laskelmaan kuuluu ainoastaan taloushallinnon täsmäytys ja se luo vain eri maksuvälineiden lasketun summan ja tapahtumasumman erotussummien kirjauskansiot sekä muut käteisvarojen hallintatapahtumien kirjauskansiot.   

4. Voit laskea tapahtumaraportin valitsemalla **Vähittäismyynti ja kauppa > Vähittäismyynnin ja kaupan IT > Myyntipistekirjaus > Laske tapahtumaraportit eräajona**. Voit kirjata tapahtumaraportin laskelmat eräajona valitsemalla **Vähittäismyynti ja kauppa > Vähittäismyynnin ja kaupan IT > Myyntipistekirjaus > Kirjaa tapahtumaraportit eräajona**.

5. Voit laskea raportin valitsemalla **Vähittäismyynti ja kauppa > Vähittäismyynnin ja kaupan IT > Myyntipistekirjaus > Laske raportit eräajona**. Voit kirjata raportit eräajona valitsemalla **Vähittäismyynti ja kauppa > Vähittäismyynnin ja kaupan IT > Myyntipistekirjaus > Kirjaa raportit eräajona**.

> [!NOTE]
> Valikon vaihtoehdot **Vähittäismyynti ja kauppa > Vähittäismyynnin ja kaupan IT > Myyntipistekirjaus > Laske laskelmat eräajona** ja **Vähittäismyynti ja kauppa > Vähittäismyynnin ja kaupan IT > Myyntipistekirjaus > Kirjaa laskelmat eräajona** eivät ole enää tässä toiminnossa.

Tapahtumaraportti- ja Raportti-tyypit on kuitenkin mahdollista luoda manuaalisesti. Siirry kohtaan **Vähittäismyynti ja kauppa > Kanavat > Myymälät** ja valitse **Laskelmat**. Valitse **Uusi** ja valitse sitten luotavan laskelman tyyppi. **Laskelmat**-sivun kentät ja sivun **Laskelmaryhmä**-kohdan toiminnot näyttävät tarvittavat tiedot ja toiminnot valitun laskelmatyypin mukaan.
