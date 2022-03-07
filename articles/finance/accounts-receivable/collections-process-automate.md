---
title: Perintäprosessin automatisointi
description: Tässä ohjeaiheessa kuvataan perintäprosessin strategiat. Ne määrittävät automaattisesti myyntilaskut, jotka edellyttävät sähköpostimuistutuksen, perintätoiminnon tai maksukehotuksen lähettämisen asiakkaalle.
author: JodiChristiansen
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 59db852024faf457db7ac145b67619b31555aaf2
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/10/2021
ms.locfileid: "7486866"
---
# <a name="collections-process-automation"></a>Perintäprosessin automatisointi

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan perintäprosessin strategiat. Ne määrittävät automaattisesti myyntilaskut, jotka edellyttävät sähköpostimuistutuksen, perintätoiminnon (kuten puhelu) tai maksukehotuksen lähettämisen asiakkaalle. 

Organisaatiot käyttävät usein paljon aikaa tutkiessaan vanhoja saldoraportteja, asiakastilejä ja avoimia laskuja. Näin organisaatioissa määritetään asiakkaat, joihin on oltava yhteydessä avoimen laskun tai tilisaldon vuoksi. Perintäasiamies kuluttaa paljon aikaa ollessaan yhteydessä asiakkaisiin ja periessään erääntyneitä maksuja tai ratkaistessaan laskuepäselvyyksiä. Perintäprosessin automatisoinnin avulla voit määrittää strategiaan perustuvan lähestymistavan perintäprosessille. Näin voit kohdistaa perintätoiminnot johdonmukaisesti mukautettujen sähköpostimuistutusten tai maksukehotusten lähettämisen suorittavan ohjelmoidun prosessin avulla. 

## <a name="collections-process-setup"></a>Perintäprosessin määrittäminen
Voit käyttää **Perintäprosessin määrittäminen** -sivua (**Luotonvalvonta > Määritys > Perintäprosessin määrittäminen**) jos haluat luoda automatisoituja perintäprosesseja. Niiden avulla voit ajoittaa toimintoja, lähettää sähköpostiviestejä ja luoda sekä lähettää asiakkaan maksukehotuksia. Prosessin vaiheet perustuvat johtavaan tai vanhimpaan avoimeen laskuun. Kukin vaihe käyttää tätä laskua määritettäessä, mitä viestintää käytetään ja mikä tehtävä suoritetaan kunkin asiakkaan kanssa.  

Perintäryhmät lähettävät tavallisesti etuajassa ilmoituksen, joka liittyy kuhunkin avoimeen laskuun, jotta asiakkaalle ilmoitetaan ennen laskun erääntymistä. **Ennen perintää** -valinta voidaan määrittää sallimaan jokaisessa prosessihierarkiassa yksi vaihe jokaista laskua kohti, joka toteutetaan, kun laskun ajoitus saavuttaa tämän vaiheen.

### <a name="process-hierarchy"></a>Prosessihierarkia
Kukin asiakaspooli voidaan liittää vain yhteen prosessihierarkiaan. Tämän vaiheen hierarkiajärjestys määrittää ensisijaisen prosessin, jos asiakas kuuluu useampaan kuin yhteen pooliin, johon on määritetty prosessihierarkia. Poolin tunnus määrittää, mitkä asiakkaat määritetään prosessiin. Kunkin määritettävän hierarkian voi delegoida vain yhdelle prosessiautomaatiolle.

Hiljaiset päivät varmistavat, että automatisoitu prosessi ei ole asiakkaaseen yhteydessä liian usein. Jos esimerkiksi hiljaisia päiviä on määritetty kaksi, automatisoitu prosessi ei ole yhteydessä asiakkaaseen vähintään kahteen päivään, vaikka alkuperäinen johtava lasku olisi maksettu kokonaan. 

Jos haluat jättää asiakkaita pois prosessiautomaatiosta, jos asiakkaan erääntymissaldo tai laskun summa on vähemmän kuin määritetty arvo, valitse **Asiakkaan erääntymissaldo vähemmän kuin** tai **Laskun summa vähemmän kuin** kentässä **Jätä pois prosessista** ja syötä summan arvo.

Merkitse **Käytä ennusteita** luodaksesi perintäaktiviteetteja käyttäen asiakkaan maksuennusteita. Luodut aktiviteetit käyttävät aktiviteettimallia **Maksuennusteet**-kohdasta **Myyntireskontran parametrit** -sivulla **Kokoelmaprosessin automaatio** -välilehdessä. 

### <a name="process-details"></a>Prosessin tiedot
Napsauta **Uusi** lisätäksesi uudet prosessitiedot hierarkiaan. **Kuvauksen** avulla määritetään hierarkian vaiheen merkitys tai nimi. Valitse **Toimintotyyppi** määrittääksesi, mikä vaihe luo tehtävän, lähettää sähköpostin tai luo maksukehotuksen. 

- **Liiketoiminta-asiakirja** määrittää toimintotyypin luomisessa käytettävän mallin. Tämä asiakirja voi olla tehtävämalli, sähköpostimalli tai maksukehotus, joka lähetetään jokaiselle asiakkaalle. Perintäprosessin automatisointi luo vain maksukehotuksia asiakasta kohti riippumatta siitä, miten muut perintäparametrit on määritetty.
- **Ajankohta** määrittää prosessin vaiheen, joka tapahtuu ennen johtavan (vanhimman) laskun erääntymispäivää tai sen jälkeen, ja jota käytetään yhdessä **Laskun erääntymispäivään liittyvät päivät** -sarakkeessa näytettävän lukumäärän kanssa. 
- Merkitse **Esikehotus**-vaihtoehto luodaksesi toiminnon jokaiselle laskulle yhdessä vaiheessa prosessihierarkiassa. Esikehotukset ovat tavallisesti etuajassa lähetettäviä ilmoituksia, jotka liittyvät avoimeen laskuun, jotta asiakkaalle voidaan ilmoittaa ennen laskun erääntymistä. Esikehotus voidaan merkitä vain yhdelle aktiviteetille hierarkiaa kohden. Kun valitset sähköpostitoiminnon tyypin, vastaanottajaa käytetään määrittämään, lähetetäänkö sähköpostiviesti asiakkaalle, myyntiryhmälle vai perimisasiamiehen yhteyshenkilölle. 
- **Liiketoiminnan tarkoituksen yhteyshenkilö** -kenätn arvo määrittää, kenelle asiakkaan tilin yhteyshenkilölle viestintä lähetetään.

### <a name="business-document-details"></a>Liiketoiminta-asiakirjojen tiedot
Liiketoiminta-asiakirjan tiedot vaihtelevat prosessin tiedoissa valitun toimintotyypin perusteella. Kun toimintotyyppi on tehtävä, tehtävämallin tiedot näytetään. Näihin tietoihin sisältyvät tehtävämallin nimi, luotavan tehtävän tyyppi, tehtävän tarkoitus, tehtävän suorittamiseen ajoitettujen päivien määrä sekä tehtävän tiedot. Tämä tehtävä linkittää sen jälkeen johtavan laskun, joka kertoo tehtävän suorittamiseen tarvittavan toiminnon vastaanottajalle.

Jos toimintotyyppi on sähköpostiviesti prosessin tiedoissa, tässä osassa on kaksi pikavälilehteä. Ensimmäistä käytetään mallin tunnuksen, sähköpostin kuvauksen, oletuskielen, automaattisesti lähetettävien sähköpostiviestien vastaanottavan käyttäjätunnuksen ja liittyvän lähettäjän sähköpostiosoitteen määrittämisessä. Toisen avulla luodaan sähköpostin tekstiosa sen jälkeen, kun **Kieli**- ja **Aihe**-kentät on tallennettu valitsemalla **Muokkaa**. Tämä avaa ikkunan, joka sallii HTML-sisällön lataamisen. 

> [!Note]
> Voit tallentaa Outlook-sähköpostiviestin, joka sisältää leipätekstin HTML-muodossa. Tämän jälkeen voit ottaa mallin käyttöön lataamalla viestin sisällön. <br> <br> Jos maksukehotuksen toimintotyyppi on valittuna, asetussivulla ei ole liiketoiminta-asiakirjan tietojen osaa.

Käytä **Perintäprosessin historia** -painiketta tarkastellaksesi valitun prosessihierarkian viimeaikaista historiaa. 

Napsauta **Perintäprosessin määritys** -toimintoa tarkastellaksesi asiakkaita, jotka on liitetty perintäprosessiin. Käytä **Asiakkaan määrityksen esikatselua** tarkastellaksesi hierarkiaa, joka on määritetty tietylle asiakkaalle. Käytä **Prosessin määrityksen esikatselua** esikatsellaksesi asiakkaita, jotka määritetään hierarkiaan sen suorittamisen yhteydessä. Napsauta **Manuaalinen määritys** tarkastellaksesi asiakkaita, jotka on määritetty prosessiin manuaalisesti, tai valitse asiakkaat, joille määritetään prosessi.

Napsauta **Prosessin simulaatio** -toiminto esikatsellaksesi toimenpiteet, jotka luodaan, jos valittu prosessien automaatio suoritetaan tällä kertaa. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
