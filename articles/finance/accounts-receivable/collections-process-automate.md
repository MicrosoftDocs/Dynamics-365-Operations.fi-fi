---
title: Perintäprosessin automatisointi
description: Tässä ohjeaiheessa kuvataan perintäprosessin strategiat. Ne määrittävät automaattisesti myyntilaskut, jotka edellyttävät sähköpostimuistutuksen, perintätoiminnon (kuten puhelu) tai maksukehotuksen lähettämisen asiakkaalle.
author: panolte
manager: AnnBe
ms.date: 08/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: a63058904df72a7fda5a67ed1e6a846eed393ce0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969698"
---
# <a name="collections-process-automation"></a>Perintäprosessin automatisointi

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan perintäprosessin strategiat. Ne määrittävät automaattisesti myyntilaskut, jotka edellyttävät sähköpostimuistutuksen, perintätoiminnon (kuten puhelu) tai maksukehotuksen lähettämisen asiakkaalle. 

Organisaatiot käyttävät paljon aikaa tutkiessaan vanhoja saldoraportteja, asiakastilejä ja avoimia laskuja. Näin organisaatioissa määritetään asiakkaat, joihin on oltava yhteydessä avoimen laskun tai tilisaldon vuoksi. Perintäasiamies kuluttaa paljon aikaa ollessaan yhteydessä asiakkaisiin ja periessään erääntyneitä maksuja tai ratkaistessaan laskuepäselvyyksiä. Perintäprosessin automatisoinnin avulla voit määrittää strategiaan perustuvan lähestymistavan perintäprosessille. Näin voit kohdistaa perintätoiminnot johdonmukaisesti mukautettujen sähköpostimuistutusten tai maksukehotusten lähettämisen suorittavan ohjelmoidun prosessin avulla. 

## <a name="collections-process-setup"></a>Perintäprosessin määrittäminen
Voit käyttää **Perintäprosessin määrittäminen** -sivua (**Luotonvalvonta > Määritys > Perintäprosessin määrittäminen**) jos haluat luoda automatisoituja perintäprosesseja. Niiden avulla voit ajoittaa toimintoja, lähettää sähköpostiviestejä ja luoda sekä lähettää asiakkaan maksukehotuksia. Prosessin vaiheet perustuvat johtavaan tai vanhimpaan avoimeen laskuun. Kukin vaihe käyttää tätä laskua määritettäessä, mitä viestintää käytetään ja mikä tehtävä suoritetaan kunkin asiakkaan kanssa.  

### <a name="process-hierarchy"></a>Prosessihierarkia
Kukin asiakaspooli voidaan liittää vain yhteen prosessihierarkiaan. Tämän vaiheen hierarkiajärjestys määrittää ensisijaisen prosessin, jos asiakas kuuluu useampaan kuin yhteen pooliin, johon on määritetty prosessihierarkia. Poolin tunnus määrittää, mitkä asiakkaat määritetään prosessiin. 

Hiljaiset päivät varmistavat, että automatisoitu prosessi ei ole asiakkaaseen yhteydessä liian usein.  Jos esimerkiksi hiljaisia päiviä on määritetty kaksi, automatisoitu prosessi ei ole yhteydessä asiakkaaseen vähintään kahteen päivään, vaikka alkuperäinen johtava lasku olisi maksettu kokonaan. 

Jos haluat sulkea asiakkaat pois prosessin automatisoinnista tilin saldon tai laskun saldon ollessa pienempi kuin määritetty arvo, määritä **Jätä pois prosessista** -kentän arvoksi **Kyllä** ja syötä summan arvo.

## <a name="process-details"></a>Prosessin tiedot
**Kuvauksen** avulla määritetään hierarkian vaiheen merkitys tai nimi.

**Toimintotyyppi** määrittää, luoko vaihe tehtävän, lähettääkö se sähköpostin vai luoko se maksukehotuksen.

**Liiketoiminta-asiakirja** määrittää toimintotyypin luomisessa käytettävän mallin.  Tämä voi olla tehtävämalli, sähköpostimalli tai maksukehotus asiakasta kohden. 

Toimintotyypit voidaan luoda joko ennen laskun eräpäivää tai sen jälkeen **Päivien määrä suhteessa laskun eräpäivään** -sarakkeen asetuksen perusteella.

Kun valitset sähköpostitoiminnon tyypin, vastaanottajaa käytetään määritettässä asiakas, myyntiryhmä tai perintäasiamiehen yhteyshenkilö- **Liiketoiminnan tarkoituksen yhteyshenkilö** -kenätn arvo määrittää, kenelle asiakkaan tilin yhteyshenkilölle viestintä lähetetään.

## <a name="business-document-details"></a>Liiketoiminta-asiakirjojen tiedot
Liiketoiminta-asiakirjan tiedot vaihtelevat prosessin tiedoissa valitun toimintotyypin perusteella.  Kun toimintotyyppi on tehtävä, tehtävämallin tiedot näytetään.  Näihin tietoihin sisältyvät tehtävämallin nimi, luotavan tehtävän tyyppi, tehtävän tarkoitus, tehtävän suorittamiseen ajoitettujen päivien määrä sekä tehtävän tiedot.  Tämä tehtävä linkittää sen jälkeen johtavan laskun, joka kertoo tehtävän suorittamiseen tarvittavan toiminnon vastaanottajalle.

Jos toimintotyyppi on sähköpostiviesti prosessin tiedoissa, tässä osassa on kaksi pikavälilehteä.  Ensimmäistä käytetään mallin tunnuksen, sähköpostin kuvauksen, oletuskielen, automaattisesti lähetettävien sähköpostiviestien vastaanottavan käyttäjätunnuksen ja liittyvän lähettäjän sähköpostiosoitteen määrittämisessä. Toisen avulla luodaan sähköpostin tekstiosa sen jälkeen, kun **Kieli**- ja **Aihe**-kentät on tallennettu valitsemalla **Muokkaa**.  Tämä avaa ikkunan, joka sallii HTML-sisällön lataamisen. Voit myös kirjoittaa manuaalisesti luodun viestin ikkunan vasemmassa alakulmassa olevaan ruutuun.  

> [!Note]
> Outlook-sähköposti voidaan tallentaa ilman haluttua tekstiosaa HTML-muodossa. Tämän jälkeen se voidaan ladata ja ottaa malli käyttöön. <br> <br> Jos maksukehotuksen toimintotyyppi on valittuna, asetuslomakkeessa ei ole liiketoiminta-asiakirjan tietojen osaa.


## <a name="fasttab-reference"></a>Pikavälilehden viite
Seuraavissa taulukoissa ovat sivut ja kentät, joiden avulla määritettyä pikavälilehteä voidaan käyttää, sekä välilehden tietojen kuvaus. 

### <a name="process-hierarchy"></a>Prosessihierarkia

|     Sivu                                                  |     Kenttä                         |     kuvaus                           |
| --------------------------------------------------------  |-------------------------------    |---------------------------------------    |
|     Perintäprosessin määrittäminen <br> Prosessien automatisointi       |                                   |     Luo ja hallitse perintä prosesseja, jotka perustuvat asiakaspoolin määrityksiin.                                                                                                                             |
|     Perintäprosessin määrittäminen <br> Prosessien automatisointi       |     Hierarkia                     |     Määrittää prosessin automatisoinnin prioriteetin. Se liitetään asiakkaalle, jos he kuuluvat useisiin pooleihin.                                                                                                   |
|     Perintäprosessin määrittäminen <br> Prosessien automatisointi       |     Ryhmän tunniste                       |     Kyselyt, jotka määrittävät asiakastietueryhmän.                                                                                                                                                        |
|     Perintäprosessin määrittäminen <br> Prosessien automatisointi       |     Hiljaiset päivät                    |     Määritä raja sille, miten usein prosessivaihe voidaan suorittaa. Jos esimerkiksi määritetään kaksi hiljaista päivää, seuraava prosessivaihe ei toteudu vähintään kahteen päivää, jos johtavaa laskua muutetaan.     |
|     Perintäprosessin määrittäminen <br> Prosessien automatisointi       |     Jätä pois prosessista        |     Jos valitset **Asiakkaan erääntymissaldo pienempi kuin** tai **Laskusumma pienempi kuin**, asiakas jätetään pois prosessin automatisoinnista, jos arvon ehtoja ei täytetä.                                   |

### <a name="process-details"></a>Prosessin tiedot
|     Sivu                                                  |     Kenttä                                         |      kuvaus                  |
|--------------------------------------------------------   |-----------------------------------------------    |----------------------------   |
|     Perintäprosessin määrittäminen <br> Prosessien automatisointi       |                                                   |     Määritä johtavan laskun perusteella toteutetut vaiheet.                                                                                                |
|                                                           |     kuvaus                                   |     Vapaamuotoisen tekstin kenttää käytetään vaiheen nimen ja/tai kuvauksen määrittämisessä.                                                                           |
|                                                           |     Toimenpidetyyppi                                   |     Tehtävä, sähköpostiviesti tai maksukehotus, joka luodaan prosessi vaiheen avulla.                                                                     |
|                                                           |     Liiketoiminta-asiakirja                           |     Määrittää tehtävän tai sähköpostiviestimallin, jota käytetään prosessivaiheen aikana.                                                                        |
|                                                           |     Milloin                                          |     Määrittää, tapahtuuko prosessivaihe ennen vai jälkeen johtavan laskun eräpäivän. Myös **Päivien määrä suhteessa laskun eräpäivään** -kentän arvo otetaan huomioon.        |
|                                                           |     Päivien määrä suhteessa laskun eräpäivään        |     Yhdessä **Kun**-kentän kanssa se määrittää prosessivaiheen ajoituksen.                                                                          |
|                                                           |     Vastaanottaja                                     |     Ilmaisee, lähetetäänkö sähköpostiviesti asiakkaalle, myyntiryhmälle vai perintäasiamiehen yhteyshenkilölle.                                                   |
|                                                           |     Liiketoiminnan tarkoituksen yhteyshenkilö                    |     Määrittää, mitä vastaanottajan sähköpostiosoitetta käytetään sähköpostiviestinnässä.                                                                                 |

### <a name="business-process-activity-template-details"></a>Liiketoimintaprosessin tehtävämallin tiedot 
|     Sivu                                                  |     Kenttä                     |      kuvaus                  |
|--------------------------------------------------------   |----------------------------   |-------------------------  |
|     Perintäprosessin määrittäminen <br> Prosessien automatisointi       |                               |     Määritysprosessin osa, jossa määritetään tehtävämallin tiedot.                                                                      |
|     Perintäprosessin määrittäminen <br> Prosessien automatisointi       |     Tehtävämalli       |     Määrittää tyypin, tarkoituksen, valmistumiseen kuluvien päivien määrän sekä sen tehtävän tiedot, joka luodaan tehtäväprosessivaiheen aikana.       |

### <a name="business-document-email-template-details"></a>Yritysasiakirjan sähköpostimallin tiedot 
|     Sivu                                                  |     Kenttä     |      kuvaus                  |
|--------------------------------------------------------   |-------------- |-----------------------------  |
|     Perintäprosessin määrittäminen <br> Prosessien automatisointi       |               |     Määrittää sähköpostiviestin kuvauksen, oletuskielen, lähettäjien nimen ja sähköpostiosoitteen, jotka luodaan sähköpostiviestin prosessivaiheessa.        |


### <a name="collections-history"></a>Perintähistoria 
|     Sivu                              |     Kenttä     |      kuvaus                                                          |
|------------------------------------   |-------------- |---------------------------------------------------------------------  |
|     Perintäprosessin määrittäminen       |               |     Näytä valitun prosessihierarkian uusin historia.     |

### <a name="collection-process-assignment"></a>Perintäprosessin määritys
|     Sivu                              |     Kenttä     |      kuvaus                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|     Perintäprosessin määrittäminen       |               |     Tarkastele perintäprosessiin liitettyjä asiakkaita.  
|     Manuaalinen määritys               |               |     Tarkastele asiakkaita, jotka on määritetty prosessiin manuaalisesti, tai valitse asiakkaat, jotka määritetään prosessiin. |
|     Esikatsele prosessin määritystä      |               |     Esikatsele asiakkaita, jotka liitetään strategiaan sen suorittamisen yhteydessä.   |
|     Esikatsele asiakasmääritystä     |               |     Näytä strategia, johon tietty asiakas on määritetty.    |
 
### <a name="parameters"></a>Parametrit
|     Sivu                                                                  |     Kenttä                                             |      kuvaus                              |
|-------------------------------------------------------------------------- |------------------------------------------------------ |-------------------------------------  |
|     Myyntireskontran parametrit > Perintäprosessin automatisointi     |     Asiakkaiden prosenttiosuus erätehtävää kohden          |     Asetus, joka määrittää erätehtävien määrän automaatioprosessia kohden.                                          |
|     Myyntireskontran parametrit > Perintäprosessin automatisointi     |     Lähetä maksukehotukset automaattisesti           |     Maksukehotuksen toimintotyypit lähettävät kehotuksen automatisoinnin aikana.                                      |
|     Myyntireskontran parametrit > Perintäprosessin automatisointi     |     Luo automatisoinnon tehtävät                |     Luo ja sulkee muiden kuin tehtävätoimintotyyppien tehtäviä kaikkien huomioon otettavien automatisoitujen vaiheiden tarkastelemista varten.        |
|     Myyntireskontran parametrit > Perintäprosessin automatisointi     |     Päivät, joiden ajan perintäprosessin automatisointi säilytetään     |     Määrittää, monenko päivän ajaksi perintähistoria tallennetaan.                                                       |
