---
title: Resurssin vuokrauksen raportit
description: Tässä ohjeaiheessa luetellaan ja kuvataan lyhyesti resurssin vuokrauksen käytettävissä olevat raportit.
author: moaamer
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-27
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 085027c5cc823beec99779791ff471dceb4ec8fe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814101"
---
# <a name="asset-leasing-reports"></a>Resurssin vuokrauksen raportit

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa luetellaan ja kuvataan lyhyesti resurssin vuokrauksen käytettävissä olevat raportit. Useimmat raportit näkyvät sen jälkeen kun tämä vaihe tai nämä vaiheet on suoritettu. Vaiheet ovat keskenään hyvin samankaltaisia. 

- Voit tarkastella useimpia resurssin vuokrauksen raportteja siirtymällä kohtaan **Resurssin vuokrauksen > Kyselyt ja raportit > Vuokrasopimuksen raportit** ja valitsemalla sitten raportin tarkastelua varten. Jos raportti vaatii erilaisen valintapolun, sen avaamiseen vaadittavat vaiheet löytyvät raportin kuvauksesta. 
- Kun valitset tulostettavan raportin, näyttöön tulee parametrien sivu. Sen avulla voit suodattaa raporttiin sisältyviä tietoja. Anna suodatusehdot ja luo raportti valitsemalla **OK**. Luodussa raportissa näkyvät määritettyjen suodattimien mukaiset tiedot.

## <a name="asset-movement"></a>Resurssien liikkeet
Käyttöomaisuuserien siirron raportti toimii eteenpäinsiirron raporttina kunkin vuokrasopimuksen käyttöoikeusomaisuuserän saldoille. Tämän raportin avulla voit tarkastella vuokrasopimuksen resurssitapahtumia tiettynä kautena. Raportti sisältää seuraavat kentät. 

|     Raportin kentät                  |     kuvaus                                                                |
|------------------------------------|--------------------------------------------------------------------------------|
|     Aloituspäivämäärä              |     Vuokrasopimuksen aikaisimman version alkamispäivä.                     |   
|     Vuokra-aika                     |     Vuokrasopimuksen aikaisimman version vuokra-aika.                            |
|     Lyhytaikainen vuokrasopimus               |     Jos vuokrasopimus luokitellaan lyhytaikaiseksi, näkyvissä on **Kyllä**.         |
|     Arvoltaan vähäinen vuokrasopimus                |     Jos vuokrasopimus luokitellaan arvoltaan vähäiseksi, näkyvissä on **Kyllä**.          |
|     Alkuperäinen käyttöoikeusomaisuuserä     |     Käyttöoikeusomaisuuserän alkuperäinen arvo alkuperäisestä tuloutuksen kirjauskansioviennistä.      |
|     Alkusaldo              |     käyttöoikeusomaisuuserän nettokirjanpitoarvo **alkamispäivästä** lähtien.                         |
|     Kauden poistokustannus    |     Raportissa määritetyn päivämäärävälin poistokulujen summa.        |
|     Kertynyt poisto       |     Kumulatiivisten poistojen summa **alkamispäivästä** lähtien.                               |
|     Arvonalennus                     |     Niiden resurssien summa, joiden arvoa on alennettu raportissa määritetyn päivämäärävälin aikana.               |
|     Muokkaukset                  |     Käyttöoikeusomaisuuserän oikaisujen summa päivämääräparametrien välillä.                            |
|     Nettokirjanpitoarvo                 |     Käyttöoikeusomaisuuserän loppunettokirjanpitoarvo, joka on kumuloitu nettopoisto **alkamispäivästä** lähtien.    |

## <a name="differences-report"></a>Raportin eroavuudet
Eroraportissa näkyvät vuokrauksen tuonnin kehykseen ladattujen tietojen ja järjestelmässä tällä hetkellä olevien tietojen erot. Tämän avulla voit vertailla vuokrauksen tuonnin kehyksen kautta oikaistuja, päivitettyjä tai lisättyjä tietoja.  

Raportin arvot vaihtelevat valitun vuokrasopimuksen mukaan. Raportissa näkyvät vain ne kentät, jotka poikkeavat järjestelmässä olevista ja väliaikaisen taulukon kentistä. Vanha arvo on se, joka on joko järjestelmässä tai joka oli järjestelmässä aiemmin sen mukaan, onko tuontiprosessi suoritettu vai ei. Uusi arvo näyttää väliaikaisen taulukon arvon. Se korvaa vanhan arvon.

## <a name="five-years-undiscounted-payment-forecast"></a>Viiden vuoden diskonttaamaton maksuennuste
Viide vuoden diskonttaamaton maksuennusteraportti näyttää arvioidut diskonttaamattomat vuokrat, jotka maksetaan seuraavien viiden vuoden aikana raporttiparametreissa määritetystä päivämäärästä alkaen. Raportti sisältää seuraavat kentät. 

|     Raportin kentät         |     kuvaus                                                                                       |
|-------------------------- |---------------------------------------------------------------------------------------------------    |
|     Vuokran kuvaus     |     Vuokran kuvaus vuokran otsikosta.                                                      |
|     Vuokratunnus              |     Vuokran yksilöivä tunnus.                                                                              |
|     Kirja                  |     Kirjan tunnukseen liitetty vuokrasopimuskirja.                                                         |
|     Luokittelu        |     Vuokrasopimuksen luokittelu.                                                                  |
|     Kirjanpitotaso         |     Taso, johon tämä vuokrasopimus kirjataan.                                                         |
|     Valuutta              |     Vuokrasopimuksen valuutta.                                                                        |
|     Valittu               |     Kaikkien maksettavien vuokrien summa seuraavien 12 kuukauden aikana raportointipäivämäärästä alkaen.          |
|     13–24 kuukautta          |     Kaikkien maksettavien vuokrien summa 13–24 kuukauden välillä raportointipäivämäärästä alkaen.           |
|     25–36 kuukautta          |     Kaikkien maksettavien vuokrien summa 25–36 kuukauden välillä raportointipäivämäärästä alkaen.           |
|     37–48 kuukautta          |     Kaikkien maksettavien vuokrien summa 37–48 kuukauden välillä raportointipäivämäärästä alkaen.           |
|     49–60 kuukautta          |     Kaikkien maksettavien vuokrien summa 49–60 kuukauden välillä raportointipäivämäärästä alkaen.           |
|     Sen jälkeinen            |     Kaikkien maksettavien vuokrien summa 61 kuukauden aikana tai sen jälkeen raportointipäivämäärästä alkaen.              |

## <a name="gaap-cash-flows-report"></a>GAAP-kassavirtojen raportti
GAAP:n ilmoitusten raportti täyttää Yhdysvaltojen GAAP:n ilmoitusten vaatimukset, jotka on määritetty kohteessa 842-20-50-4(g)(1). Voit tarkastella tätä raporttia siirtymällä kohtaan **Resurssin vuokraus > Kyselyt ja raportit > Ilmoitukset > GAAP – kassavirrat**. 

|     Raportin kentät                                 |     kuvaus                                                                                                                                               |
|------------------------------------------------   |-----------------------------------------------------------------------------  |
|     Päivämäärästä <br> Päivämäärään                        |     Määrittää päivämäärävälin, jota käytetään raportin tietojen rajoittamisessa.      |
|     Yritys                                  |     Vuokrasopimuksiin liittyvä yritys.                                      |
|     Vuokran tyyppi                                    |     Vuokrasopimuksen luokittelu rahoitus- tai käyttöleasingsopimukseksi.           |
|     Vuokratunnus                                      |     Vuokran yksilöivä tunnus.                                                      |
|     Vuokran kuvaus                             |     Vuokran kuvaus vuokran otsikosta.                              |
|     Vuokrasopimuskirja                                    |     Vuokrasopimuskirja, johon tämä rivi viittaa.                        |
|     Kirjanpitotaso                                 |     Kullekin käyttöomaisuuteen liitetylle kirjalle on määritetty tietty kirjanpitotaso, jolla on yleinen poistotavoite.                          |
|     Vuokraryhmä                                   |     Ryhmä, johon vuokrasopimus on liitetty.                                     |
|     Valuutta                                      |     Käytetyn tapahtumavaluutan lyhenne. Kaikki raportit muuntavat tapahtumavaluutan raportointivaluutaksi.                      |
|     Rahoitusleasingsopimukset – käyttöleasingin kassavirrat         |     Kaikkien kirjattujen muuttuvien maksujen ja kuoletusaikataulusta kirjattujen kaikkien korkomaksujen summa päivämääräparametrien välillä.        |
|     Rahoitusleasingsopimukset – rahoitusleasingin kassavirrat           |     Kaikkien pääomamaksujen summa kuoletusaikataulusta päivämääräparametrien välillä.       |
|     Käyttöleasingsopimukset– käyttöleasingin kassavirrat       |     Kaikkien kirjattujen vuokrien ja kirjattujen muuttuvien maksujen summa päivämääräparametrien välillä.            |

## <a name="lease-balances-forecast"></a>Vuokranmaksuennuste
Vuokrasaldojen ennuste sisältää tiedot suoraan velan kuoletusaikataulusta ja resurssin poistoaikataulusta. Raportissa ovat ennustetun vuokrasopimusvelan ennustesummat ja käyttöoikeusomaisuuserät ajanjaksolta, mukaan lukien näiden vuokrasopimusten kaikki ennustetut kulut. Raportti sisältää seuraavat kentät.

|     Raportin kentät                 |     kuvaus                                                                                                                                                                               |
|---------------------------------  |--------------------------------------------------------------------------------------------------------------------   |
|     Alkusaldo             |     Vuokran kuoletusaikataulun aloitussaldo raportin alkupäivämäärän sisältävällä kaudella.            |
|     Alkuperäinen tunnustaminen           |     Jos vuokrasopimuksen alkamispäivä on raportille määritettynä päivämäärävälinä, tässä sarakkeessa näkyy alkuperäisen tuloutuksen kirjauskansioviennin velkatilin arvo.      |
|     Maksut                      |     Vuokrasopimuksen niiden maksujen summa, jotka kuuluvat raportille määritettyyn päivämääräväliin.                               |
|     Kiinnostuksen kohteet                      |     Vuokrasopimuksen niiden korkokulujen summa jotka kuuluvat raportille määritettyyn päivämääräväliin.                    |
|     Loppusaldo                |     Vuokrasopimuksen velkasaldo **loppupäivämäärästä** lähtien.                                                             |
|     Lyhytaikainen velka          |     Lyhytaikaisen velan summa vuokrasopimuksen kuoletussuunnitelmassa **loppupäivämäärästä** lähtien.                           |
|     Pitkäaikainen velka           |     Pitkäaikaisen velan summa vuokrasopimuksen kuoletussuunnitelmassa **loppupäivämäärästä** lähtien.                            |
|     Alkunettokirjanpitoarvo      |     Vuokran kuoletusaikataulun alkunettokirjanpitoarvo raportin alkupäivämäärän sisältävällä kaudella      |
|     Alkuperäinen tunnustaminen           |     Jos vuokrasopimuksen alkamispäivä on raportin päivämääräparametrien välissä, tässä sarakkeessa näkyy alkuperäisen tuloutuksen kirjauskansioviennin resurssin tilin arvo.            |
|     Poistokulu          |     Vuokrasopimuksen niiden poistokulujen summa, jotka kuuluvat raportille määritettyyn päivämääräväliin.                  |
|     Loppusaldo                |     Vuokrasopimuksen resurssin saldo **loppupäivämäärästä** lähtien.                                                              |
|     Oman pääoman korjaus             |     Alkusaldo vähennettynä alkunettokirjanpitoarvolla.                                                             |

## <a name="lease-commencements-report"></a>Vuokrasopimuksen alkamisten raportti
Vuokrasopimuksen alkamisten raportti näyttää kaikki vuokrasopimukset, jotka ovat alkaneet määritettynä päivämäärävälinä, mukaan lukien alkuperäisen velan ja .käyttöoikeusomaisuuserän saldot. Raportti sisältää seuraavat kentät. 

|     Raportin kentät                 |     kuvaus                                                                                       |
|---------------------------------  |---------------------------------------------------------------------------------------------------    |
|     Aloituspäivämäärä             |     Alkuperäisen tälle vuokrasopimuksen versiolle kirjatun tuloutuksen kirjauskansioviennin päivämäärä.         |
|     Aloitusvaiheen velkamäärä      |     Alkuperäisen tuloutuksen kirjauskansioviennin velkasumma.                                  |
|     Alkuperäinen resurssin summa          |     Alkuperäisen tuloutuksen kirjauskansioviennin resurssin summa.                                      |

## <a name="lease-modification-report"></a>Vuokrasopimuksen muokkauksen raportti
Vuokrasopimuksen muokkauksen raportti sisältää kaikki vuokrasopimukset, joita on muokattu määritettynä päivämäärävälinä. Raportissa näkyy myös vuokrasopimusta muokannut käyttäjä ja oikaistun velan kokonaissumma. Raportti sisältää seuraavat kentät. 

|     Raportin kentät                 |     kuvaus           |
|---------------------------------  |-------------------------  |
|     Oikaissut                   |     Vuokrasopimusta muokanneen henkilön käyttäjänimi.                                |
|     Oikaisupäivämäärä               |     Oikaisukirjauskansioviennin kirjauspäivämäärä.                        |
|     Oikaisut                   |     Kaikkien vuokrasopimuksen velkatilille päivämääräparametrien välillä kirjattujen oikaisukirjauskansiovientien summa. Hyvitykset näkyvät positiivisina ja veloitukset negatiivisina.       |
|     Voittosumma (tai tappiosumma)            |     Kaikkien vuokrasopimuksen voitto-/tappiotilille päivämääräparametrien välillä kirjattujen oikaisukirjauskansiovientien summa. Hyvitykset näkyvät positiivisina ja veloitukset negatiivisina.       |
|     Jakamaton voitto             |     Kaikkien vuokrasopimuksen kertyneiden tuottojen tilille päivämääräparametrien välillä kirjattujen oikaisukirjauskansiovientien summa.      |
|     Sopimusvelan loppusaldo      |     Tuloksena saatava velkasaldo vuokrasopimuksen oikaisupäivämääränä.           |

## <a name="lease-movement-report"></a>Vuokrasopimuksen siirtoraportti
Vuokrasopimuksen siirron raportti toimii eteenpäinsiirron raporttina kunkin vuokrasopimuksen velkasaldoille. Tämän raportin avulla käyttäjä voi tarkastella vuokrasopimuksen velkatapahtumia tiettynä kautena.

|     Raportin kentät             |     kuvaus                                               |
|----------------------------   |-------------------------------------------------------------- |
|     Aloituspäivämäärä         |     Vuokrasopimuksen aikaisimman version alkamispäivä.    |
|     Vuokra-aika                |     Vuokrasopimuksen aikaisimman version vuokra-aika.           |
|     Maksuja jäljellä        |     Niiden maksujen määrä, joita ei vielä ole kirjattu vuokrasopimukselle.                       |
|     Alkusaldo         |     Niiden tapahtumien summa, jotka vaikuttavat ennen raportin alkupäivämäärää tapahtuneeseen vuokrasopimusvelkaan.             |
|     Alkuperäinen tunnustaminen       |     Ennen raportille määritettyä päivämääräväliä kirjatun vuokrasopimuksen minkä tahansa alkuperäisen kirjaamistapahtuman summa.     |
|     Maksut                  |     Raportille määritettynä päivämäärävälinä kirjattujen vuokrasopimuksen maksutapahtumien summa. Tämän sarakkeen arvot näkyvät negatiivisina summina, koska maksut pienentävät vuokrasopimuksen velkasaldoa.  |
|     Kiinnostuksen kohteet                  |     Raportille määritettynä päivämäärävälinä vuokrasopimukselle kirjattujen korkokertymien summa.            |
|     Oikaisut               |     Vuokrasopimuksen niiden kirjattujen oikaisutapahtumien summa, jotka kuuluvat raportille määritettyyn päivämääräväliin.                               |
|     Loppusaldo            |     Vuokrasopimuksen kaikkien velkatapahtumien saldo on kirjattu raporttiin **loppupäivämäärän** jälkeen.                  |

## <a name="lease-transactions-report"></a>Vuokratapahtumien raportti
Vuokratapahtumien kysely näyttää kaikki kirjauskansioviennit, jotka resurssin vuokrauksen on luonut. Kukin kirjauskansiovienti on linkitetty sen kirjan tunnukseen, josta se on peräisin. Tämän avulla voit liittää kirjauskansioviennin helposti vastaavaan vuokraan. Vuokratapahtumien kysely toimii samalla tavalla kuin kirjanpidon **Tositetapahtumat**-sivu.

## <a name="weighted-average-discount-rate-report"></a>Painotetun keskimääräisen diskonttauskoron raportti
Painotetun keskimääräisen diskonttauskoron raportti täyttää Yhdysvaltojen GAAP-ilmoituksen vaatimukset, jotka määritetään kohteessa ASC 842-20-50-4(g)(4) painotetulle keskimääräiselle diskonttauskorolle. Voit tarkastella tätä raporttia siirtymällä kohtaan **Resurssin vuokraus > Kyselyt ja raportit > Ilmoitukset > Painotettu keskimääräinen diskonttauskorko**. Raportti sisältää seuraavat kentät. 

|     Raportin kentät                     |     kuvaus                                                           |
|------------------------------------   |------------------------------------------------------------------------   |
|     Alkupäivämäärä                        |     Tämä raportti sisältää kaikki vuokrasopimukset, jotka on aloitettu **alkupäivämäärän** parametrin mukaisena päivänä tai ennen sitä. Tämä raportti on suoritettava sen kauden viimeisenä päivänä, joka ilmoitetaan.      |
|     Oikeushenkilö                      |     Vuokrasopimukseen liittyvä yritys.                           |
|     Vuokratunnus                          |     Vuokran yksilöivä tunnus.                                                  |
|     Vuokran kuvaus                 |     Vuokran kuvaus vuokran otsikosta.                          |
|     Kirja                              |     Näytetyn vuokrasopimuksen tietty kirjatyyppi.                                                                                                                                            |
|     Kirjanpitotaso                     |     Kullekin käyttöomaisuuteen liitetylle kirjalle on määritetty tietty kirjanpitotaso, jolla on yleinen poistotavoite.      |
|     Vuokraryhmä                       |     Ryhmä, johon vuokrasopimus kuuluu.                                 |
|     Diskonttauskorko                     |     Vuokrien diskonttauksessa käytettävä korko.                             |
|     Valuutta                          |     Käytetyn tapahtumavaluutan lyhenne. Kaikki raportit muuntavat tapahtumavaluutan raportointivaluutaksi.  |
|     Vuokria jäljellä          |     Maksamattomien vuokrien kokonaissumma, joka on jäljellä maksuaikataulusta **alkupäivämäärästä** lähtien.            |
|     Painotettuja maksuja jäljellä       |     Jäljellä olevat vuokramaksut kerrottuna käytetyllä diskonttauskorolla.   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]