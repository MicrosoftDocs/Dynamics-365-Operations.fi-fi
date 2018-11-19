---
title: "Vähittäismyyntikanavan kirjanpidon integrointi"
description: "Tässä ohjeaiheessa on yleiskuvaus Retail POS:n kirjanpidon integroinnista."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: fi-fi
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a>Vähittäismyyntikanavan kirjanpidon integrointi

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 for Retailin kirjanpidon integrointitoiminnosta. Kirjanpidon integrointitoiminto on kehikko, joka on suunniteltu tukemaan paikallista kirjanpitolainsäädäntöä. Sen avulla on tarkoitus estää petoksia vähittäismyyntialalla. Kirjanpidon integraatiota käyttäviä tyypillisiä skenaarioita ovat esimerkiksi seuraavat:

- Verokuitin tulostaminen ja sen antaminen asiakkaalle.
- Myyntipisteessä suoritettuun myyntiin ja palautuksiin liittyvien tietojen lähettämisen turvaaminen viranomaisen ilmoittamaan ulkoiseen palveluun.
- Tietojen suojaaminen käyttämällä viranomaisen hyväksymää digitaalista allekirjoitusta.

Tässä ohjeaiheessa on ohjeet kirjanpidon integraation määrittämiseen siten, että käyttäjät voivat suorittaa seuraavat tehtävät. 

- Määritä kirjanpidon yhdistimet, jotka ovat laskentavälineitä tai -palveluja. Niitä käytetään kirjanpidon rekisteröinnissä, kuten kirjanpitotietojen tallentaminen, digitaalinen allekirjoittaminen ja turvallinen lähettäminen.
- Määritä asiakirjan toimittaja, joka määrittää tulostusmenetelmän ja kirjanpitoasiakirjan muodostusalgoritmin.
- Määritä kirjanpidon rekisteröintiprosessi, joka määrittää vaiheiden järjestyksen ja kussakin vaiheessa käytetyn yhdistinryhmän.
- Määritä kirjanpidon rekisteröintiprosessin myyntipisteen toimintaprofiileihin.
- Määrittää yhdistimen tekniset profiilit joko laitteistoprofiileihin (paikallisille kirjanpidon yhdistimille) tai myyntipisteen toimintaprofiileihin (muille kirjanpidon yhdistintyypeille).

## <a name="fiscal-integration-execution-flow"></a>Kirjanpidon integroinnin suorittamisen työnkulku
Seuraavassa skenaariossa esitellään yleinen kirjanpidon integroinnin suorittamisen työnkulku.

1. Kirjanpidon rekisteröintiprosessin alustaminen.
  
   Sen jälkeen kun on suoritettu joitakin toimintoja, joissa tarvitaan kirjanpidon rekisteröintiä, kuten vähittäismyyntitapahtuman päättämisen jälkeen, kirjanpidon rekisteröintiprosessi liitetään nykyiseen myyntipisteen toimintoprofiiliin.

1. Kirjanpidon yhdistimen haku.
   
   Järjestelmä vertaa kirjanpidon yhdistinluetteloa jokaiseen kirjanpidon rekisteröintiprosessiin sisältyvään kirjanpidon rekisteröintivaiheeseen. Näillä yhdistimillä on toimintaprofiili, joka sisältyy määritettyyn yhdistinryhmään sekä yhdistinluettelo, joiden tekninen profiili on liitetty nykyiseen laitteistoprofiiliin (kun yhdistintyyppi on sama kuin vain **Paikallinen**) tai nykyiseen myyntipisteen toimintoprofiiliin (muille yhdistintyypeille).
   
1. Kirjanpidon integroinnin suorittaminen.

   Järjestelmä suorittaa kaikki tarvittavat löydettyyn yhdistimeen linkitetyn kokoonpanon määrittämät toiminnot. Se tehdään kyseisen yhdistimen edellisessä vaiheessa löydetyn toimintaprofiilin ja teknisen profiilin asetusten mukaisesti.

## <a name="setup-needed-before-using-fiscal-integration"></a>Kirjanpidon integroinnin käyttöä edeltävät asetukset
Määritä seuraavat asetukset ennen kirjanpidon integrointitoiminnon käyttämistä:

- Määritä kirjanpidon toimintaprofiilin numeron numerosarjan **Vähittäismyynnin parametrit** -sivulla.
  
- Määritä seuraavien viitteiden numerosarjat **Vähittäismyynnin yhteiset parametrit** -sivulla:
  
  - Kirjanpidon teknisen profiilin numero
  - Kirjanpidon yhdistinryhmän numero
  - Rekisteröintiprosessin numero

- Luo **kirjanpidon yhdistin** jokaiselle laitteelle tai palvelulle, jota aiot käyttää kirjanpidon integroinnissa, valitsemalla **Vähittäismyynti > Kanavan asetukset > Kirjanpidon integrointi > Kirjanpidon yhdistimet**.

-  Luo **Kirjainpitoasiakirjan toimittajat** kaikille kirjanpidon yhdistimille valitsemalla **Vähittäismyynti > Kanavan asetukset > Kirjanpidon integrointi > Kirjainpitoasiakirjan toimittajat**. Tietojen yhdistämisen katsotaan olevan osa kirjainpitoasiakirjan toimittajaa. Jos haluat määrittää samalle yhdistimelle erilaisia tietojen yhdistämisiä (kuten osavaltiokohtaisia säädöksiä), sinun on luotava erillisiä kirjainpitoasiakirjan toimittajia.

- Luo **Yhdistimen toiminnallinen profiili** kullekin kirjanpitoasiakirjan toimittajalle valitsemalla **Vähittäismyynti > Kanavan asetukset > Kirjanpidon integrointi >Yhdistimen toiminnallinen profiili**.
  - Valitse yhdistimen nimi.
  - Valitse asiakirjan toimittaja.
  - Määritä ALV-prosenttiasetukset **Palvelun asetukset** -välilehdessä.
  - Määritä ALV-koodien yhdistäminen ja maksuvälinetyyppien yhdistäminen **Tietojen yhdistäminen** -välilehdessä.

  #### <a name="examples"></a>Esimerkkejä 

  |  | Muoto | Esimerkki | 
  |--------|--------|--------|
  | ALV-prosenttiasetukset | arvo: VATrate | 1 : 2000, 2 : 1800 |
  | ALV-koodien yhdistäminen | VATcode : arvo | vat20 : 1, vat18 : 2 |
  | Maksuvälinetyyppien yhdistäminen | TenderTyp : arvo | Käteinen : 1, Kortti : 2 |

- Luo **Kirjanpidon yhdistinryhmät** valitsemalla **Vähittäismyynti > Kanavan asetukset > Kirjanpidon integrointi > Kirjanpidon yhdistinryhmät**. Yhdistinryhmä on niiden toiminnallisten profiilien alajoukko, joka on linkitetty samoja toimintoja suorittaviin kirjanpidon yhdistimiin ja joita käytetään samassa kirjanpidon rekisteröintiprosessin vaiheessa.

   - Lisää toiminnalliset profiilit yhdistinryhmään. Valitse ensin **Lisää** **Toiminnalliset profiilit** -sivulla ja sitten profiilin numero.
   - Jos haluat keskeyttää toiminnallisen profiilin käytön, valitse **Poista käytöstä** -asetukseksi **Kyllä**. 
   
     Muutos koskee vain nykyistä yhdistinryhmää. Voit jatkaa saman toiminnallisen profiilin käyttöä muissa yhdistinryhmissä.

     >[!NOTE]
     > Kullakin kirjanpidon yhdistimellä voi olla yhdistinryhmässä vain yksi toiminnallinen profiili.

- Luo **Yhdistimen tekninen profiili** kullekin kirjanpidon yhdistimelle valitsemalla **Vähittäismyynti > Kanavan asetukset > Kirjanpidon integrointi >Yhdistimen tekninen profiili**.
  - Valitse yhdistimen nimi.
  - Valitse yhdistimen tyyppi: 
      - **Paikallinen** – määritä tämä tyyppi paikalliseen koneeseen asennetuille fyysisille laitteille tai sovelluksille.
      - **Sisäinen** – määritä tämä tyyppi Retail Serveriin yhdistetyille kirjanpidon laitteille ja palveluille.
      - **Ulkoinen** – ulkoisille kirjanpidon palveluille, kuten veroviranomaisten verkkoportaalille.
    
  - Määritä asetukset **Yhteys**-välilehdessä.

      
 >[!NOTE]
 > Aiemmin ladatun määrityksen päivitetty versio ladataan sekä toiminnalliselle että tekniselle profiilille. Jos soveltuva yhdistin asiakirjan toimittaja on jo käytössä, saat siitä ilmoituksen. Oletusarvoisesti kaikki toiminnalliseen ja tekniseen profiiliin manuaalisesti tehdyt muutokset tallennetaan. Voit korvata nämä profiilit määrityksen oletusparametrijoukolla valitsemalla **Päivitä** **Yhdistimen toiminnalliset profiilit** -sivulla ja **Yhdistimen tekniset profiilit** -sivulla.
 
- Luo **Kirjanpidon rekisteröintiprosessi** kirjanpidon integroinnin jokaiselle yksilölliselle prosessille valitsemalla **Vähittäismyynti > Kanavan asetukset > Kirjanpidon integrointi > Kirjanpidon rekisteröintiprosessi**. Rekisteröintivaiheiden järjestys ja kussakin vaiheessa käytetty yhdistinryhmä määrittävät rekisteröintiprosessin. 
  
  - Lisää rekisteröintivaiheet prosessiin:
      - Valitse **Lisää**.
      - Valitse yhdistimen tyyppi.
      
      >[!NOTE]
      > Tämä kenttä määrittää, mistä järjestelmä etsii yhdistintä teknisessä profiilissa. Jos yhdistimen tyyppi on **Paikallinen**, haku tehdään laitteistoprofiileissa, kun taas muita kirjanpidon yhdistintyyppejä haetaan myyntipisteen toiminnallisista profiileista.
      
   - Valitse yhdistinryhmä.
   
     >[!NOTE]
     > Tarkista rekisteröintiprosessin rakenteen yhtenäisyys valitsemalla **Vahvista**. Tarkistusten suorittamista suositellaan seuraavissa tapauksissa:
       >- Uudessa rekisteröintiprosessissa sen jälkeen, kun kaikki asetukset ovat valmiita. Tämä koskee myös sidontaa myyntipisteen toiminnallisiin profiileihin ja laitteistoprofiileihin.
       >- Aiemmin luodun rekisteröintiprosessin päivittämisen jälkeen.

-  Sido kirjanpidon rekisteröintiprosessit myyntipisteen toiminnallisiin profiileihin valitsemalla **Vähittäismyynti > Kanavan asetukset > POS-asetukset > POS-profiilit > Toiminnalliset profiilit**.
   - Valitse ensin **Muokkaa** ja sitten **Prosessin numero** **Kirjanpidon rekisteröintiprosessi** -välilehdessä.
- Sido yhdistimen tekniset profiilit laiteprofiileihin valitsemalla **Vähittäismyynti > Kanavan asetukset > POS-asetukset > POS-profiilit > Laiteprofiilit**.
   - Valitse ensin **Muokkaa** ja sitten **Uusi** **Kirjanpidon tekninen profiili** -välilehdessä.
   - Valitse yhdistimen tekninen profiili **Profiilin numero** -kentässä.
   
     >[!NOTE]
     > Voit lisätä useita teknisiä profiileja laiteprofiiliin. Tätä ei kuitenkaan tueta, jos laiteprofiilissa on useampi kuin yksi leikkauskohta jonkin yhdistinryhmän kanssa. Voit estää virheelliset asetukset, jos tarkistat rekisteröintiprosessin suositusten mukaisesti kaikkien laiteprofiilien päivittämisen jälkeen.

