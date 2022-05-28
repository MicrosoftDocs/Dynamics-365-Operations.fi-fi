---
title: Tilikauden lopetus
description: Tässä aiheessa kuvataan kirjanpidon tilivuoden sulkemisprosessissa tarvittavat asetukset ja ohjeet.
author: kweekley
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: kfend
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 247c3286124da946937c8afd248a275e5a745044
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725230"
---
# <a name="year-end-close"></a>Tilikauden lopetus

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan kirjanpidon tilivuoden sulkemisprosessissa tarvittavat asetukset ja ohjeet.

Tilikauden lopussa sinun on suoritettava tilivuoden sulkemisprosessi siirtääksesi alkusaldot uudelle vuodelle. Useimmat organisaatiot suorittavat tilivuoden sulkemisprosessin useita kertoja. Ensimmäinen suoritus siirtää saldot uuteen tilivuoteen. Prosessi voidaan sen jälkeen suorittaa niin monta kertaa kuin on tarpeen saldojen siirtämiseksi korjaustapahtumista uuteen tilivuoteen.

Tilivuoden sulkemisprosessissa voidaan luoda kahdenlaisia tapahtumia. Järjestelmä luo aina avaustapahtuman, jota käytetään uuden tilivuoden alkusaldojen luomiseen. Avaustapahtumassa näytetään kirjanpidon tasetilien saldot uudelle tilivuodelle sekä voitto- ja tappiokirjanpitotilien saldot kertyneiden tuottojen kirjanpitotileille uudelle tilivuodelle. Järjestelmä voi myös luoda sulkemistapahtuman, joka kirjaa voitto- ja tappiotilien saldot nollaan suljettavalle tilivuodelle.

## <a name="prepare-to-run-the-year-end-close"></a>Tilivuoden sulkemisen valmistelu

Vahvista seuraavat asetukset ennen tilivuoden sulkemisprosessin suorittamista:

**Päätili**-sivulla:

- Tarkista, että **Päätilityyppi**-kenttä on määritetty oikein jokaiselle päätilille. Päätilin tyyppi määrittää, tuodaanko päätilin saldo alkusaldona, vai suljetaanko se kertyneisiin tuottoihin avaustapahtumassa.
- Päätilin saldo voidaan siirtää uuteen päätiliin tilivuoden sulkemisprosessin aikana. Syötä uusi päätili **Avaustili**-kenttään. Tätä kenttää käytetään yleensä taseen päätileille, kun päätili on poistettu käytöstä ja uutta päätiliä käytetään uudella tilivuodella.

**Kirjanpidon parametrit** -sivun **Tilivuoden sulkeminen** -kohdassa:

- **Poista tilivuoden päätöksen tapahtumat kun tilivuosi suljetaan** -asetuksella määritetään, poistetaanko järjestelmän luoma edellisen tilivuoden päätöksen avaustapahtuma, kun tilivuoden päätös suoritetaan uudelleen. Jos tämä asetus on **Kyllä**, aiemmat avaustapahtumat ja valinnaiset sulkutapahtumat poistetaan ja uusi avaus- tai sulkutapahtuma luodaan nykyisten saldojen perusteella. Jos tämä asetus on **Ei**, edelliset avaus- ja valinnaiset sulkutapahtumat säilytetään ja järjestelmä luo uuden avaus- tai sulku tapahtuman, jolla saldot siirretään edelleen edellisen tilivuoden sulkemisen jälkeen kirjatuista korjaustapahtumista.
- **Luo päätöstapahtumat siirron yhteydessä** -asetuksella luodaan sulkemistapahtumat suljettavalle tilivuodelle, jotta kaikkien päätilien saldot voidaan asettaa nollaan (0). Jos tämä asetus on **Kyllä**, sekä avaus- että sulkemistapahtumat luodaan. Jos tämä asetus on **Ei**, vain avaustapahtuma luodaan tulevalle tilivuodelle saldojen siirtämiseksi. Päätilien saldot säilytetään tilikauden lopussa.
- **Muuta tilikauden tilaksi pysyvästi suljettu** -asetuksella tilivuosi asetetaan pysyvästi suljettuun tilaan. Käytä tätä vaihtoehtoa huolellisesti, koska kausia, joiden tila on pysyvästi suljettu, ei voi avata uudelleen. Sen vuoksi oikaisuja ei voi kirjata tilivuoteen. On suositeltavinta asettaa arvoksi **Ei**.
- **Tositenumero on täytettävä** -vaihtoehto on poistettu. Tosite on nyt pakollinen, kun vuoden lopun sulkemisprosessi suoritetaan. Tositenumero syötetään silloin manuaalisesti.

**Kirjanpidon vuosikalenteri** -sivulla:

- Seuraava tilivuosi on luotava ennen tilivuoden sulkemisen suorittamista. Muuten alkusaldoja ei voi luoda avauskaudella.

**Kirjanpitokalenteri** -sivulla:

- Valinnainen: jokainen suljettavan tilivuoden tilikausi voidaan asettaa **Pitoon**, jotta uusia tapahtumia ei voi kirjata. Kun oikaisutapahtumia tunnistetaan, pidossa olevat kaudet voidaan avata uudelleen oikaisutapahtumien kirjaamisen mahdollistamiseksi, vaikka tilivuoden sulkemisprosessi olisi jo suoritettu.

**Vuoden lopun sulkemismallin asetukset** -sivulla:

- **Kun pääkirjanpidon vuoden lopun parannukset** -ominaisuus on käytössä, vuoden lopun sulkemismallin määrittäminen on erillään vuoden lopun sulkemisprosessista. Malli voidaan määrittää **Vuoden lopun sulkemismallin asetukset** -sivulla (**Pääkirjanpito \> Kirjanpidon asetukset \> Vuoden lopun sulkemismallin asetukset**) tai sitä voidaan käyttää vuoden lopun sulkemisprosessista.

## <a name="define-year-end-close-templates"></a>Tilivuoden sulkemismallien määrittäminen

Kun järjestelmä on määritetty, tilivuoden sulkemisprosessin voi suorittaa. **Tilivuoden sulkemismallin asetukset** -sivulla voidaan määrittää malli yritysryhmälle, joille tilivuoden sulkemisprosessi suoritetaan. Mallia käytetään jokaisessa tilivuoden lopetuksessa, mutta se on muokattavissa organisaatiosi tarpeiden mukaan.

Määritä ensimmäiseksi mallille **Ryhmän nimi** ja valitse kirjanpidon vuosikalenteri. Sisällytettävä yritysryhmä tulisi voida tunnistaa ryhmän nimestä. Kun määrität yritysryhmiä, muista, että yritykset voidaan sisällyttää samaan ryhmään vain, jos niille on valittu sama kirjanpidon kalenteri. Mallit voi määrittää esimerkiksi maantieteellisen sijainnin perusteella erikseen pohjoisamerikkalaisille, Euroopan, Lähi-Idän ja Afrikan (EMEA) -alueen yrityksille sekä Aasian ja Tyynenmeren (APAC) alueen yrityksille.

Yritykset voidaan seuraavaksi lisätä malliin. Yritykset voidaan lisätä joko valitsemalla ne tai valitsemalla organisaatiohierarkia. Jos valitset organisaatiohierarkian, ainoastaan hierarkian yritykset, jotka käyttävät valittua kirjanpidon vuosikalenteria lisätään malliin. Jos lisäät yritykset malliin yritysten perusteella, ainoastaan samaa kirjanpidon vuosikalenteria käyttävät yritykset voidaan lisätä. Sama kirjanpidon vuosikalenteri on vaatimus, koska tilivuoden lopetus suoritetaan valitsemalla tilivuosi, joka voi riippua vuosikalenterista.

Kun yritykset on lisätty, määritä kertyneiden tuottojen päätilit kullekin yritykselle.

**Taloushallinnon dimensio** -välilehdellä määritetään taloushallinnon dimensiot, joita käytetään avaustapahtumassa. Huomaa, että tällä välilehdellä määritetyt asetukset koskevat vain **Yritykset**-ruudukossa valittua yritystä. Määritykset on toistettava kullekin ruudukon yritykselle.

**Siirrä tasedimensiot** -asetuksella määritetään, säilytetäänkö tasetileille kirjatut tapahtumien taloushallinnon dimensiot avaustapahtumassa. On suositeltavinta asettaa tämän asetuksen arvoksi **Kyllä**. Tasedimensioiden asetus ei vaikuta kertyneiden tuottojen kirjanpitotilien olemassa oleviin saldoihin. Nämä saldot määräytyvät seuraavassa osassa määritettyjen tulosdimensioiden mukaan. Esimerkiksi tilivuosi 2019 oli ensimmäinen suljettu vuosi, ja **Sulje kaikki**-valintaa käytettiin sulkemisessa **Osasto**- ja **Kustannuspaikka**-dimensioiden valitsemista varten. Tässä tapauksessa kullekin osaston ja kustannuspaikan yhdistelmälle luotiin erillinen kertynyt tuottotili. Kun tilivuoden sulkeminen suoritetaan tilivuodelle 2020, edellisen vuoden kertyneet tulot säilyvät täsmälleen samanlaisina kuin ne on kirjattu, vaikka **Siirrä tasedimensiot** -asetuksen arvoksi olisi määritetty **Ei**. Edellisen tilivuoden sulkemisista kirjatut kertyneet tuotot eivät koskaan muutu.

**Siirrä tulosdimensiot** -osassa määritetään, mitkä voitto- ja tappiotileille kirjattujen tapahtumien taloushallinnon dimensiot siirretään kertyneiden tuottojen päätilille. Tunnista ensin valittua yritystä koskevat taloushallinnon dimensiot. Näihin taloushallinnon dimensioihin sisältyvät kaikki vuodelle kirjatut taloushallinnon dimensiot, vaikka kyseiset dimensiot eivät olisikaan aktiivisen tilirakenteen osia. Määritä seuraavaksi kunkin dimension tyypiksi **Sulje yksittäinen** tai **Sulje kaikki**. Oletusarvo on **Sulje kaikki**. Tämä valinta säilyttää alkuperäisen taloushallinnon dimension arvot kirjatuista tapahtumista, ja käyttää niitä avaussaldojen luomiseen säilytettyjen tuottojen tilille. Erilliset kertyneiden tuottojen alkusaldot luodaan jokaiselle yksilölliselle taloushallinnon dimensioarvoyhdistelmälle. Jos valittuna on **Sulje yksittäinen**, kaikki kyseiselle taloushallinnon dimensiolle kirjatut tapahtumat tiivistetään kertyneiden tuottojen alkusaldoksi **Sulje yksittäinen** -kentän jälkeen näkyvään kenttään syötetylle dimensioarvolle. Oletetaan esimerkiksi, että kaikki tilivuoden tapahtumat on kirjattu **Päätili - Osasto** -tilirakenteella. Mallin taloushallinnon dimensiolle **Osasto** on valittu **Sulje yksittäinen** ja dimension arvoksi on syötetty **100**. Jos kaikkien osastoille 200, 300 ja 400 kirjattujen tapahtumien kokonaisarvo on $100 000, **Kertynyt tuotto - 100** -tilille luodaan yksi avaussaldo. Jos valitset **Sulje yksittäinen**, mutta jätät taloushallinnon dimensioarvon tyhjäksi, kaikki tapahtumat kirjataan kertyneihin tuottoihin ja dimension arvo on tyhjä.

## <a name="run-the-year-end-close-process"></a>Tilivuoden sulkemisprosessin suorittaminen

Kun tilivuoden lopun sulkemismallit on luotu, voit käynnistää vuoden lopun sulkemisprosessin **Vuoden sulkeminen** -sivulla (**Pääkirjanpito \> Kauden sulkeminen \> Tilivuoden sulkeminen**). Ennen vuoden lopun sulkemista voit lisätä uusia vuoden lopun sulkemismalleja tai muokata aiemmin luotuja malleja valitsemalla **Vuoden sulkemismallin asetukset,** jotta voit avata mallien asetussivun.

Valitse vuoden lopun sulkemismalli ja valitse sitten toimintoruudusta **Suorita tilivuoden lopun sulkeminen**. Valitse kaikki mallin yritykset tai niiden osajoukko, joille tilikauden lopetus suoritetaan. Kun suoritat tilivuoden sulkemisen tilivuodelle ensimmäisen kerran, valitset luultavasti kaikki yritykset, jotta voit luoda niille kaikille alkusaldot. Jos tilivuoden sulkemisprosessi on jo suoritettu aiemmin, voit suorittaa prosessin ainoastaan yrityksille, joille on kirjattu korjaustapahtumia.

Valitse seuraavaksi tilivuosi, jolle haluat suorittaa tilivuoden sulkemisprosessin. Jos tilivuoden viimeisellä kaudella on useita sulkemiskausia, **Kauden nimi** -kenttä tulee käyttöön. Tämän jälkeen voit valita sulkemiskauden, johon sulkemistapahtuma kirjataan, jos asetukset on määritetty luomaan sulkemistapahtuma.

Kirjoita seuraavaksi tositenumero. Samaa tositenumeroa käytetään kaikille tilivuoden sulkemisprosessiin valituille yrityksille. Tositenumeron luomiseen ei käytetä numerosarjaa.

Tilikauden lopetusprosessi suoritetaan oletusarvoisesti eränä. Alustamisen jälkeen voit siis palata muihin toimiin.

Koska tilirakenteet voivat muuttua koko tilivuoden ajan, tilirakennetta ei aina voida tunnistaa. Siksi tilivuoden päätösprosessi ei noudata tilirakenteita. Kun avaustapahtumat luodaan, saldot siirretään edelleen taloushallinnon dimensioiden kanssa tilivuoden lopetusmallin määrityksen mukaisesti. Alkusaldotapahtumat voivat sisältää taloushallinnon dimensioita, jotka eivät sisälly enää nykyisiin tilirakenne- ja segmenttiyhdistelmiin, jotka eivät ole enää kelvollisia nykyisessä tilirakenteessa. Jos organisaatiosi haluaa jättää taloushallinnon dimension pois kertyneiden voittojen alkusaldosta, aseta taloushallinnon dimension asetukseksi **Sulje yksittäinen** ja jätä dimensioarvo tyhjäksi.

Kun prosessi on valmis, kullekin yrityksen ja tilivuoden yhdistelmälle luodaan tietue. Vain niiden yritysten tietuee näkyvät, joihin sinulla on käyttöoikeudet. Kukin tietue sisältää järjestelmän päivämäärän ja ajan, jolloin prosessi suoritettiin ja suoran linkin tilivuoden lopun sulkemista varten luotuihin tositteisiin.

[![Vuoden lopun sulkemisen Vuoden lopun sulkemishistoria -pikavälilehdellä luodut tietueet](./media/run-yr-end-close.png)](./media/run-yr-end-close.png)

Jos suoritat vuoden lopun sulkemisen uudelleen, näet yhden tietueen tai useita tietueita kutakin yrityksen ja tilivuoden yhdistelmää varten sen mukaan, mitö asetusta on käytetty **Poista aiemmin luodut tilivuoden lopun tapahtumat, kun tilivuosi suljetaan uudelleen** -valinnassa **Pääkirjanpidon parametrit** -sivulla:

- Jos asetukseksi on valittu **Kyllä**, edellisen tilivuoden sulkemisen tosite poistetaan. Tietue merkitään **Peruutetuksi** ja siihen merkitään päivämäärä ja aika, jolloin peruutus tehtiin. Lisäksi linkki tositenumeroon poistetaan. Kun tilivuoden sulkeminen on valmis, uudelle luotavalle tositteelle luodaan uusi tietue.
- Jos asetuksena on **Ei**, edellisen vuoden lopun sulkemistietue ja tositteen linkki säilyvät. Aina, kun vuoden tilivuoden sulkeminen suoritetaan uudelleen, luodaan uusi tietue sekä linkki uusiin tositteisiin.

## <a name="reverse-the-year-end-close-process"></a>Tilivuoden sulkemisprosessin peruuttaminen

**Tiliuoden sulkeminen** -sivulla voit peruuttaa tilivuoden sulkemisen. Valitse yrityksen ja peruutettavan tilikauden yhdistelmän tietue ja valitse sitten **Peruuta tilivuoden sulkeminen**. Peruutusprosessi poistaa kaikki tilivuodelle luodut avaus- ja sulkemistositteet. Tietue merkitään **Peruutetuksi** ja siihen merkitään päivämäärä ja aika, jolloin peruutus tehtiin. Lisäksi linkki tositenumeroon poistetaan. Peruuttamisprosessi suoritetaan eränä kuten tilivuoden sulkeminenkin.

Ruudukon yllä käytettävissä olevan **Näytä peruutettu** -valintaruudun avulla voit piilottaa tai näyttää peruutun vuoden lopun sulkemisprosessien tietueet. Kun olet suorittanut prosessin **Peruuta tilivuoden sulkeminen**, sinun on ehkä valittava **Näytä peruutettu** -valintaruutu, jos haluat nähdä tietueen. Voit määrittää muita tietoja varten lisäsuodatusta.

[![Näytä peruutettu -valintaruudun avulla voit tarkastella palautettujen vuoden lopun sulkemisprosessien tietueita Vuoden sulkeminen -sivulla](./media/rvrs-yr-end-close.png)](./media/rvrs-yr-end-close.png)

Lisätietoja on ohjeaiheissa [Kirjanpidon sulkeminen kauden lopussa](close-general-ledger-at-period-end.md) ja [Tilikauden sulkeminen](tasks/close-fiscal-year.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
