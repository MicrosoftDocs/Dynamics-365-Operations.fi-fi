---
title: Tilikauden lopetus
description: "Tässä aiheessa kuvataan kirjanpidon tilivuoden sulkemisprosessissa tarvittavat asetukset ja ohjeet."
author: kweekley
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bf9d0a6ab0fcf7d6f5a31813d68f0bd452ce1019
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="year-end-close"></a>Tilikauden lopetus

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan kirjanpidon tilivuoden sulkemisprosessissa tarvittavat asetukset ja ohjeet. 

Tilikauden lopussa sinun on suoritettava tilivuoden sulkemisprosessi siirtääksesi alkusaldot uudelle vuodelle. Useimmat organisaatiot suorittavat tilivuoden sulkemisprosessin useita kertoja. Ensimmäisellä kerralla saldot siirretään uudelle tilivuodelle. Sen jälkeen tilivuoden sulkemisen voi suorittaa uudelleen niin monta kertaa, kuin on tarve, jotta korjaustapahtumien saldot siirretään uudelle tilivuodelle. 

Tilivuoden sulkemisprosessissa voidaan luoda kahdenlaisia tapahtumia. Järjestelmä luo aina avaustapahtuman, jota käytetään uuden tilivuoden alkusaldojen luomiseen. Avaustapahtumassa näytetään kirjanpidon tasetilien saldot uudelle tilivuodelle sekä voitto- ja tappiokirjanpitotilien saldot kertyneiden tuottojen kirjanpitotileille uudelle tilivuodelle. Järjestelmä voi myös luoda sulkemistapahtuman, joka kirjaa voitto- ja tappiotilien saldot nollaan suljettavalle tilivuodelle.

## <a name="prepare-to-run-the-year-end-close"></a>Tilivuoden sulkemisen valmistelu
Vahvista seuraavat asetukset ennen tilivuoden sulkemisprosessin suorittamista: 

**Päätili**-sivulla:

-   Vahvista, että **Päätilin tyyppi** on määritetty oikein kullekin päätilille. Päätilin tyypillä määritetään, tuodaanko päätilin saldo edelleen alkusaldona, vai suljetaanko se kertyneihin tuottoihin avaustapahtumassa.
-   Päätilin saldon voi siirtää **Avaustili**-kentän avulla uudelle päätilille tilivuoden sulkemisprosessin aikana. Uusi päätili kirjataan **Avaustili**-kenttään. Tätä käytetään yleensä taseen päätileille, kun päätili on poistettu käytöstä ja uutta päätiliä käytetään uudella tilivuodella.

**Kirjanpidon parametrit** -sivun **Tilivuoden sulkeminen** -kohdassa:

-   **Poista päätöstapahtumat** -asetuksella määritetään, poistetaanko järjestelmän luoma edellisen tilivuoden päätöksen avaustapahtuma, kun tilivuoden päätös suoritetaan uudelleen. Jos tämä asetus on **Kyllä**, aiemmat avaustapahtumat poistetaan ja uusi avaustapahtuma luodaan nykyisten saldojen perusteella. Jos tämä asetus on **Ei**, edellinen avaustapahtuma säilytettään ja järjestelmä luo uuden avaustapahtuman, jolla saldot siirretään edelleen kirjatuista korjaustapahtumista edellisen tilivuoden sulkemisen jälkeen.
-   **Luo päätöstapahtumat siirron yhteydessä** -asetuksella luodaan sulkemistapahtumat suljettavalle tilivuodelle, jotta voitto- ja tappiotilien saldot voidaan asettaa nollaan. Jos tämä asetus on **Kyllä**, sekä avaus- että sulkemistapahtumat luodaan. Jos tämä asetus on **Ei**, vain avaustapahtuma luodaan tulevalle tilivuodelle saldojen siirtämiseksi. Voitto- ja tappiotilien saldot säilytetään tilikauden lopussa.
-   **Muuta tilikauden tilaksi pysyvästi suljettu** -asetuksella tilivuosi asetetaan pysyvästi suljettuun tilaan. Käytä tätä asetusta harkiten, sillä jaksoja, jotka ovat pysyvästi suljetussa tilassa ei voi avata uudelleen, eikä kyseisiin tilivuosiin voi tehdä korjauksia. On suositeltavinta asettaa arvoksi **Ei**.
-   **Tositenumero on täytettävä** -asetuksella määritetään, onko tositenumero pakollinen tilivuoden sulkemisprosessia suoritettaessa. Suositeltavinta on vaatia tositenumero, jotta avaustapahtuman tunnistaminen on mahdollisimman helppoa.

**Kirjanpidon vuosikalenteri** -sivulla:

-   Seuraava tilivuosi on luotava ennen tilivuoden sulkemisen suorittamista. Tuleva tilivuosi on pakollinen, jotta aloitusjakson alkusaldot voidaan luoda.

**Kirjanpitokalenteri** -sivulla:

-   Valinnainen: jokainen suljettavan tilivuoden tilikausi voidaan asettaa **pitoon**, jotta uusia tapahtumia ei voi kirjata. Kun oikaisutapahtumia tunnistetaan, pidossa olevat kaudet voidaan avata uudelleen oikaisutapahtumien kirjaamiseksi, vaikka tilivuoden sulkemisprosessi olisi jo suoritettu.

## <a name="define-year-end-close-templates"></a>Tilivuoden sulkemismallien määrittäminen
Kun järjestelmä on määritetty, tilivuoden sulkemisprosessin voi suorittaa. **Tilivuoden lopetus** -sivulla voidaan määrittää malli yritysryhmälle, joille tilivuoden lopetusprosessi suoritetaan. Mallia käytetään jokaisessa tilivuoden lopetuksessa, mutta se on muokattavissa organisaatiosi tarpeiden mukaan. 

Määritä ensimmäiseksi mallille **Ryhmän nimi** ja valitse kirjanpidon vuosikalenteri. Yritysryhmä tulisi voida tunnistaa ryhmän nimestä.  Mallit voi määrittää esimerkiksi maantieteellisen sijainnin perusteella erikseen pohjoisamerikkalaisille sekä EMEA- ja APAC-alueiden yrityksille. 

Yritykset voidaan seuraavaksi lisätä malliin. Yritykset voidaan lisätä joko valitsemalla ne tai valitsemalla organisaatiohierarkia. Jos valitset organisaatiohierarkian, ainoastaan hierarkian yritykset, jotka käyttävät valittua kirjanpidon vuosikalenteria lisätään malliin. Jos lisäät yritykset malliin yritysten perusteella, ainoastaan samaa kirjanpidon vuosikalenteria käyttävät yritykset voidaan lisätä. Sama kirjanpidon vuosikalenteri on vaatimus, koska tilivuoden lopetus suoritetaan valitsemalla tilivuosi, joka voi riippua vuosikalenterista. 

Kun yritykset on lisätty, määritä kertyneiden tuottojen päätilit kullekin yritykselle. **Edellisen tilikauden lopetuksen päivämäärä** -kenttä päivitetään joka kerta, kun yrityksen tilikausi lopetetaan. 

**Taloushallinnon dimensio** -välilehdellä määritetään taloushallinnon dimensiot, joita käytetään avaustapahtumassa. Huomaa, että määrittämäsi asetukset koskevat vain **Yritykset**-ruudukossa valittuja yrityksiä. Toista määritykset kaikille ruudukon yrityksille. 

**Siirrä tasedimensiot** -asetuksella määritetään, säilytetäänkö tasetileille kirjatut tapahtumien taloushallinnon dimensiot avaustapahtumassa. On suositeltavinta arvoksi **Kyllä**. **Siirrä tulosdimensiot** -asetuksella määritetään, mitkä voitto- ja tappiotileille kirjattujen tapahtumien taloushallinnon dimensiot siirretään kertyneiden tuottojen päätilille. Tunnista ensin valittua yritystä koskevat taloushallinnon dimensiot. Näihin sisältyvät kaikki vuodelle kirjatut taloushallinnon dimension, vaikka kyseiset dimensiot eivät olisikaan aktiivisen tilirakenteen osia. Määritä seuraavaksi kunkin dimension tyypiksi **Sulje yksittäinen** tai **Sulje kaikki**.  Oletusarvo on **Sulje kaikki**, joka ylläpitää kirjattujen tapahtumien alkuperäiset taloushallinnon dimensiot ja käyttää niitä alkusaldojen luomiseen kertyneiden tuottojen tilille. Erilliset kertyneiden tuottojen alkusaldot luodaan jokaiselle yksilölliselle taloushallinnon dimensioarvoyhdistelmälle. Jos valittuna on **Sulje yksittäinen**, kaikki kyseisellä taloushallinnon dimensiolla kirjatut tapahtumat tiivistetään kertyneiden tuottojen alkusaldoksi **Sulje yksittäinen** -kenttään annetulle dimensioarvolle. Oletetaan esimerkiksi, että kaikki tilivuoden tapahtumat on kirjattu Päätili - Osasto -tilirakenteella. Mallin Osasto- taloushallinnon dimensiossa on valittuna **Sulje yksittäinen** ja annettu arvo on 100. Jos kaikkien osastoille 200, 300 ja 400 kirjattujen tapahtumien arvo on $100 000, Kertynyt tuotto - 100 -tilille luodaan yksi avaussaldo. Jos valitset **Sulje yksittäinen** ja jätät taloushallinnon dimensioarmon tyhjäksi, kaikki tapahtumat kirjataan kertyneihin voittoihin tyhjällä dimensioarvolla. 

Tilivuoden päätösprosessi ei noudata tilirakenteita. Tämä johtuu siitä, että tilirakenteet voivat muuttua tilivuoden aikana, eikä asiaankuuluvaa tilirakennetta ei välttämättä voi tunnistaa näiden muutosten vuoksi.  Kun avaustapahtumat luodaan, saldot siirretään edelleen taloushallinnon dimensioiden kanssa tilivuoden lopetusmallin määrityksen mukaisesti. Alkusaldotapahtumat voivat sisältää taloushallinnon dimensioita, jotka eivät sisälly enää nykyiseen tilirakenne- ja segmenttiyhdistelmiin, jotka eivät ole enää kelvollisia nykyisessä tilirakenteessa. Jos organisaatiosi haluaa jättää taloushallinnon dimension pois kertyneiden voittojen alkusaldosta, aseta taloushallinnon dimension asetukseksi **Sulje yksittäinen** ja jätä dimensioarvo tyhjäksi.

## <a name="run-the-year-end-close-process"></a>Tilivuoden sulkemisprosessin suorittaminen
Kun tilivuoden sulkemismallit on luotu, sulkemisprosessi aloitetaan valitsemalla toimintoruudusta **Suorita tilivuosi**. Valitse kaikki mallin yritykset tai niiden osajoukko, joille tilikauden lopetus suoritetaan. Kun suoritat tilivuoden sulkemisen tilivuodelle ensimmäisen kerran, valitset luultavasti kaikki yritykset, jotta voit luoda kaikille yrityksille alkusaldot. Jos suoritat tilivuoden sulkemisprosessin uudelleen, voit suorittaa prosessin ainoastaan yrityksille, joille on kirjattu korjaustapahtumia. 

Valitse tilivuosi, jolle haluat suorittaa tilivuoden sulkemisprosessin. Jos tilivuoden viimeisellä kaudella on useampi sulkemisjakso, **Jakson nimi** -kentässä voi valita, mihin sulkemisjaksoon sulkemistapahtuma kirjataan, jos sulkemistapahtuman luominen on määritetty. 

Syötä tositenumero, joka on pakollinen riippuen kirjanpidon parametreissa määritetyistä asetuksista. Samaa tositenumeroa käytetään kaikille tilivuoden sulkemisprosessiin valituille yrityksille. Tositenumeron luomiseen ei käytetä numerosarjaa. On suositeltavinta syöttää tositenumero, vaikka se ei olisikaan pakollinen. Tositenumeron syöttäminen helpottaa avaustapahtuman löytämistä uudessa tilivuodessa. Jos tositenumeroa ei ole annettu, avaustapahtuman tosite on tyhjä. 

Jos haluat peruuttaa aiemman tilivuoden sulkemisen valitulle tilivuodelle, aseta **Kumoa edellinen sulkeminen** -arvoksi **Kyllä**. Tilivuoden sulkeminen peruutetaan, mutta prosessin voi suorittaa uudelleen milloin tahansa. Jos peruutat tilivuoden sulkemisen, **Edellisen tilikauden lopetuksen päivämäärä** -tieto ei ole saatavilla. 

Tilikauden lopetusprosessi ajetaan oletusarvoisesti eräajona. On suositeltavinta suorittaa prosessi eräajona, jotta käyttäjä voi palata muihin toimiin. **Edellisen tilikauden lopetuksen päivämäärä** -kenttään päivitetään istunnon päivämäärä joka kerta, kun tilivuoden sulkemisprosessi suoritetaan.

Lisätietoja on ohjeaiheissa [Kirjanpidon sulkeminen kauden lopussa](close-general-ledger-at-period-end.md) ja [Tilikauden sulkeminen](tasks/close-fiscal-year.md).




