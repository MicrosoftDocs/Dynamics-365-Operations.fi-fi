---
title: Dynamics 365 Supply Chain Managementin esiversio 10.0.25 (huhtikuu 2022)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin version 10.0.25 uusia tai muuttuneita ominaisuuksia.
author: kamaybac
ms.date: 02/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 0ce9bc4685542cf691d862c0fec76f3f7b40c6b6
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087317"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10025-april-2022"></a>Dynamics 365 Supply Chain Managementin esiversio 10.0.25 (huhtikuu 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin esiversion 10.0.25 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.1149. Se on käytettävissä seuraavasti:

- **Julkaisun esiversio:** helmikuu 2022
- **Julkaisun yleinen saatavuus (oma päivitys):** maaliskuu 2022
- **Julkaisun yleinen saatavuus (automaattinen päivitys):** huhtikuu 2022

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. Tämän aiheen päivitys saattaa sisältää ominaisuuksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ominaisuusalue | Ominaisuus | Lisätietoja | Käyttöönottaja:   |
|---|---|---|---|
| Varasto&nbsp;ja&nbsp;logistiikka | Vaarallisten materiaalien parannukset | Nämä parannukset pohjautuvat olemassa oleviin vaarallisten materiaalien toimintoihin, joiden avulla yritykset voivat paremmin noudattaa paikallisia määräyksiä kuljettaessaan vaarallista materiaalia eri maantieteellisten alueiden välillä. <!-- KFM: Update to 2022w1 link when published -->| Toimintojen hallinta:<br>*Vaarallisten materiaalien parannukset* |
| Varasto&nbsp;ja&nbsp;logistiikka | Pakkausasemien pakkaustyö | Tämä ominaisuus parantaa merkittävästi pakkaus- ja lähetystoimintojen joustavuutta ja ketteryyttä. Pakkausprosessin aikana varastotyöntekijät voivat nyt pakata ja lähettää yksittäisiä samaan lähetykseen ja kuormaan liittyviä pakkauksia. Samaan lähetykseen kuuluvia tilausrivejä ei välttämättä tarvitse lähettää yhdessä, jos osa nimikkeistä on valmiina lähetettäväksi heti. Yksittäinen tilaus voidaan pakata ja lähettää useaksi pakkauksiksi eri toimitusajoille, mikä vähentää odotusaikoja ja lisää ketteryyttä.<!-- KFM: Update to 2022w1 link when published --> | Toimintojen hallinta:<br>*Pakkausasemien pakkaustyö* |
| Varasto&nbsp;ja&nbsp;logistiikka | [Skannaa varaston viivakoodit GS1-muotostandardien avulla](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) <!-- KFM: Update to 2022w1 link when published --> | [GS1-viivakoodit ja QR-koodit](../warehousing/gs1-barcodes.md) | Toimintojen hallinta:<br>*Skannaa GS1-viivakoodit* |
| Valmistus | [Materiaalin kulutus ja varaukset tuotannon käyttöliittymässä](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Tuotannon käyttöliittymän käytön ohjeet työntekijöille](../production-control/production-floor-execution-use.md) | Toimintojen hallinta:<br>*(Esiversio) Rekisteröi materiaalikulutus tuotannon käyttöliittymässä (käytössä WMS:ssä)* |
| Valmistus | [Rekisteröi materiaalikulutus skaalausyksiköissä](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [Valmistuksen suorituksen kuormitukset pilven ja reunan asteikon yksiköitä varten](../cloud-edge/cloud-edge-workload-manufacturing.md) | Toimintojen hallinta:<br>*Rekisteröi materiaalikulutus skaalausyksikön mobiilisovelluksessa* |
| Suunnittelu | [Optimointiehdotusten suunnittelu aiemmin luodun toimituksen optimointia varten](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Toimintosanomat](../master-planning/action-messages.md) | Oletusarvoisesti käytössä |
| Suunnittelu | Yksinkertaiset suunnitellut tilaukset | [Yksinkertaiset suunnitellut tilaukset](../master-planning/planning-optimization/planned-orders-simplified.md ) | Toimintojen hallinta:<br>*Yksinkertaiset suunnitellut tilaukset* |

## <a name="feature-enhancements-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnon parannukset

Seuraavassa taulukossa on tämän julkaisun sisältämät ominaisuuksien parannukset. Jokainen näistä parannuksista parantaa aiemmin luotua toimintoa lisäysten avulla. Koska ne ovat vain parannuksia, niitä ei ole lueteltu [vapautussuunnitelmassa](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Jos kuitenkin haluat varmistaa, että nämä parannukset eivät ole ristiriidassa aiemmin luotujen mukautuksiesi tai asetuksesi kanssa, kaikki muutokset ovat oletusarvon mukaan pois käytöstä (ellei toisin ilmoiteta).

Jos haluat ottaa jonkin näistä ominaisuuksista käyttöön tai poistaa ne käytöstä, sinun on tehtävä se [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moduuli | Ominaisuuden nimi ominaisuuksienhallinnassa | Lisätietoja |
|---|---|---|
| Varastonhallinta | (Puola) Salli useiden SAD-laskujen linkitys yhden SAD:n yhteen ostotilausriviin | Tämän ominaisuuden avulla voit jakaa ostotilausrivejä ja linkittää ne yhteen valvonta-asiakirjaan (SAD), kun nämä ostotilausrivit on kirjattu useassa eri laskussa (esimerkiksi eri lähetyksille). |
| Hankinta | Konsolidoi useat ostoehdotukset yhdeksi ostotilaukseksi kirjauspäivän mukaan | Tämän ominaisuuden avulla useita ostoehdotuksia voidaan konsolidoida yhdeksi ostotilaukseksi, jos eri ostoehdotuksilla on eri kirjanpitopäivät. Ostotilausten luomisen ja kysynnän konsolidoinnin ostokäytännön säännöt voidaan määrittää automatisoimaan päätös, joka koskee ehdotusrivien ryhmittelyä kirjanpitopäivän mukaan ostotilaustasolla. Ostotilausten konsolidointia kirjanpitopäivämäärän mukaan ei tueta, jos budjetin hallinta on käytössä, koska kirjanpidon päivämäärää käytetään budjettivarauksissa ja varauksissa. Siksi se on säilytettävä siirryttäessä ostoehdotuksesta ostotilaukseen. |
| Hankinta | Poista ostoehdotuksen jakelun palautuspainike käytöstä | Tämä ominaisuus poistaa **Kirjanpidollinen jako** -sivun **Nollaa**-painikkeen käytöstä tarkistettaville ostoehdotuksille. |
| Hankinta | Näytä vanhat tarjouspyynnön oletusvastauskenttäasetukset | Tämä ominaisuus palauttaa vanhat tarjouspyynnön oletusvastauskentän asetukset, jotka on aiemmin poistettu käyttöliittymästä. Nämä asetukset eivät toimita mitään toimintoja valmiina, mutta niitä voi mukauttaa toimittamaan niitä tarvittaessa. Ota tämä toiminto käyttöön, jos organisaatiosi on jo lisännyt toimintoja tarjouspyynnön oletusvastauskentän asetuksiin tai aikoo käyttää lisätä niitä. Kun tämä ominaisuus on käytössä, voit käyttää asetuksia **hankintaparametrien** sivulla,avaamalla **Tarjouspyyntö**-välilehden ja valitsemalla **tarjouksen oletusvastauskentät**. |
| Hankinta | Yhdistä sen toimittajan taloushallinnon dimensiot, jolla on aktiivisen dimension linkin taloushallinnon dimensio ostotilauksessa | Tämän ominaisuuden avulla voit yhdistää toimittajien taloushallinnon dimensiot aktiivisen dimension kanssa. Linkitä taloushallinnon dimensiot ostoehdotuksen hyväksymisen jälkeen, jos määrität linkin taloushallinnon dimension ja toimipaikan varastodimension välille. Ostotilauksen luomisen ja kysynnän konsolidoinnin oston käytäntösäännöt voidaan määrittää edistämään päätöstä taloushallinnon dimensioiden yhdistämisestä toimittajilta aktiivisen dimension kanssa. Linkitä taloushallinnon dimensio ostotilauksen otsikon tasolla. |
| Tuotannonhallinta | (Venäjä) Ota käyttöön tuotannon kaavan / tuoterakenteen ja automaattisen GTD-varauksen/-kulutuksen oletussijainnin määritys tuotannossa | Tämä ominaisuus ottaa käyttöön lisäasetuksia tuotantoon tuoduista raaka-aineista (vain Venäjän lokalisointi).<ul><li>Automaattisen oletussijainnin määrittäminen tuotantokaavoille ja tuoterakenteelle sekä resurssiryhmissä että varastoissa.</li><li>Raaka-aineiden automaattinen varaus *GTD-numero*-dimension mukaan WMS-aktivoidussa varastoissa ei-WMS-varausalgoritmin mukaan. Tämä pätee, kun *raaka-aineiden keräilyä* koskeva työkäytäntö on käytössä ja **työn luontimenetelmänä** on *Ei koskaan* ja varasto, sijainti ja nimiketunnus vastaavat tuotanto(erä)tilauksen varastotapahtumia.</li><li>Automaattinen raaka-aineiden kulutus *GTD-numero*-dimension mukaan keräysluettelon kirjaamisen yhteydessä aiemmin kuvatun hankitun varauksen mukaisesti.</li></ul> |
| Varastonhallinta   | Poista odotettujen vastaanottojen käyttö laatutilauksissa, joihin varastot ovat estotilassa | Tämä ominaisuus estää järjestelmää luomasta odotettuja vastaanottotapahtumia laatutilauksille, jotka ottava näytteitä varastosta, joka on estotilassa. Koska estetty varasto ei ole käytettävissä, tämä toiminto poistaa odotetut vastaanotot. Näin voidaan varmistaa, että varasto ei päädy useisiin estotiloihin, mikä voi aiheuttaa tietojen eheysongelmia. |
| Varastonhallinta   | (Esiversio) Saapuvien ja lähtevien varastotilausten skaalausyksikön tuki | Tämän toiminnon avulla järjestelmä luo lähtevät varastotilaukset vapautus varastoon -prosessin aikana sekä luo saapuvia varastotilauksia, kun siirtotilaukset kirjataan toimitetuiksi. Järjestelmä synkronoi sitten kunkin saapuvan tai lähtevän varastotilauksen toimituksesta tai vastaanottamisesta vastaavalle skaalausyksikölle. Huomaa, että kun tämä ominaisuus on otettu käyttöön, varaston suorituksen kuormitukset on päivitettävä. Lisätietoja on kohdassa [Varaston hallinnan kuormitukset pilven ja reunan asteikon yksiköitä varten](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>Tämä ominaisuus vaatii *Erota hyllytys lähetysilmoituksista (ASN)* -toiminnon, ja se mahdollistaa siirtotilausten vastaanottamisen Warehouse Management -mobiilisovelluksessa rekisterikilpeä käyttäen. |

## <a name="feature-state-changes-in-this-release"></a>Tämän julkaisun toiminnon tilan muutokset

Seuraavassa taulukossa luetellaan ominaisuudet, jotka tulivat pakollisiksi tai oletusarvoisesti käyttöön versiossa 10.0.25. Kaikki nämä toiminnot tulevat automaattisesti käyttöön järjestelmässä heti, kun päivität versioksi 10.0.25. Pakollisia ominaisuuksia ei voi poistaa käytöstä, mutta oletusarvoisesti käytössä olevia ominaisuuksia voi silti poistaa käytöstä käyttämällä [ominaisuuksien hallintaa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Taulukossa luetellaan myös aiemmat julkisen esiversion ominaisuudet, mutta jotka ovat muuttuneet yleisesti käytettäviksi versiossa 10.0.25, mikä tarkoittaa sitä, että niitä suositellaan käytettäviksi tuotantoympäristöissä. Nämä toiminnot ovat oletusarvon mukaan pois käytöstä, ellei toisin ilmoiteta, joten ne on otettava käyttöön käyttämällä [ominaisuuksien hallintaa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), jos haluat käyttää niitä.

| Moduuli | Toiminnon nimi | Ominaisuuden tila |
| --- | --- | --- |
| Resurssien hallinta | Käytä sääntöjä työtilausten ryhmittelyyn ylläpitosuunnitelman ollessa käynnissä | Yleisesti saatavilla |
| Resurssien hallinta | Vastaperusteiset ylläpitoparannukset | Yleisesti saatavilla |
| Kustannushintojen hallinta | Kustannuslaskentataso | Yleisesti saatavilla |
| Kustannushintojen hallinta | Ota käyttöön käyttäjän määrittämät eränumeroasetukset varaston käänteistä sulkutoimenpidettä varten | Yleisesti saatavilla |
| Kustannushintojen hallinta | Varaston sulkemisen edistymistiedot | Yleisesti saatavilla |
| Kustannushintojen hallinta | Varastokustannuksen uudelleenarvostuksen taloushallinnon dimensioiden oletusasetukset | Yleisesti saatavilla |
| Kustannushintojen hallinta | Varaston arvon raportin tietojen puhdistus | Käytössä oletusarvoisesti |
| Kustannushintojen hallinta | Varastoarvoraporttien säiliö | Käytössä oletusarvoisesti |
| Kustannushintojen hallinta | Näytä varaston sulkemisen loki ruudukossa | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | Aiemmin luotujen tuotteiden muutostenhallinnan ottaminen käyttöön | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | Suunnittelun muutosten hallinta | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | Suunnittelun ilmoitukset tuotannolle | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | Parannettu suunnittelun muutostenhallinnan määritteiden periytyvyys | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | Hallitse kaavojen ja niiden ainesosien muutoksia | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | Tuotteen valmiustarkistukset | Käytössä oletusarvoisesti |
| Suunnittelun muutosten hallinta | Muuttujien luominen suunnittelun tuotteille | Käytössä oletusarvoisesti |
| Varastonhallinta | Siirtyminen tuoterakenneriveiltä tuoterakenneversioon. | Pakollinen |
| Pääsuunnittelu | Suunniteltujen suur- ja pakkauserätilausten eräkelpoinen vahvistaminen ja konsolidointi | Yleisesti saatavilla |
| Pääsuunnittelu | Resurssien suunnittelu ja ylläpito | Yleisesti saatavilla |
| Pääsuunnittelu | Ota käyttöön pääsuunnitelman asetusten ohjatun toiminnon ominaisuudet | Pakollinen |
| Pääsuunnittelu | Ennustemallinvalinta kysynnän ennusteen tiedoissa | Pakollinen |
| Pääsuunnittelu | Pääsuunnittelun edistymisen visualisointi | Pakollinen |
| Pääsuunnittelu | Suunniteltujen tilausten rinnakkainen vahvistaminen | Pakollinen |
| Pääsuunnittelu | Suunnitellun tilauksen vahvistaminen suodatuksen kanssa | Käytössä oletusarvoisesti |
| Pääsuunnittelu | Suunniteltujen tilausten tallennetut näkymät | Käytössä oletusarvoisesti |
| Hankinta | Poista ostoehdotuksen jakelun palautuspainike käytöstä | Yleisesti saatavilla |
| Hankinta | Ota käyttöön hankintaan liittyvien työnkulkujen nollaus | Yleisesti saatavilla |
| Hankinta | Mahdollisuus vahvistaa hyväksytyt ostotilaukset toimittajayhteistyöstä erässä | Pakollinen |
| Hankinta | Ostosopimuksen Suljettu-tila | Pakollinen |
| Hankinta | Lisää rivejä ostosopimukseen liittyviin ostotilauslaskuihin | Käytössä oletusarvoisesti |
| Hankinta | Lisää Tilattu määrä -kenttä Tuotteen vastaanoton kirjaus -sivulle | Käytössä oletusarvoisesti |
| Hankinta | Salli toimittajien käyttää hankintaluokkia toimittajayhteistyön avulla | Käytössä oletusarvoisesti |
| Hankinta | Ostotilausten veloitusten lähde- ja kohdesummat | Käytössä oletusarvoisesti |
| Hankinta | Veloitusten määritys toimipaikan ja varaston mukaan | Käytössä oletusarvoisesti |
| Hankinta | Ota käyttöön ostoveron laskeminen vuosittaisen tariffin perusteella | Käytössä oletusarvoisesti |
| Hankinta | Ostosopimuksen vastuullinen osapuoli | Käytössä oletusarvoisesti |
| Hankinta | Ostotilausten tallennetut näkymät | Käytössä oletusarvoisesti |
| Tuotetietojen hallinta | Oletustilausmäärien tarkka vahvistus | Pakollinen |
| Tuotetietojen hallinta | Tuoterakenteen raportin esikäsittely aikakatkaisun välttämiseksi | Käytössä oletusarvoisesti |
| Tuotetietojen hallinta | Taloushallinnon oletusdimensiot erikseen, kun käytetään nimikemalleja | Käytössä oletusarvoisesti |
| Tuotetietojen hallinta | Ota tuotedimensioryhmät käyttöön nimikemalleille | Käytössä oletusarvoisesti |
| Tuotetietojen hallinta | Luo tuotevarianttien nimet uudelleen nimikkeistön perusteella | Käytössä oletusarvoisesti |
| Tuotetietojen hallinta | Muuttujaehdotukset-sivun parannukset | Käytössä oletusarvoisesti |
| Tuotannonhallinta | Parantunut tuotannon todellisen painon määrän keräily | Yleisesti saatavilla |
| Tuotannonhallinta | Työkorttipääte-sivulle on lisätty uusi Lopeta tauko -painike | Pakollinen |
| Tuotannonhallinta | Ota käyttöön rekisterikilven numeron automaattinen luonti, kun työkorttilaitteessa raportoidaan valmiiksi | Pakollinen |
| Tuotannonhallinta | Ota käyttöön alihankintana hankittujen nimikkeiden osittainen vastaanotto ja korjaa Toimittaja-tyypin tuoterakennerivien hävikkilaskennan ongelma | Pakollinen |
| Tuotannonhallinta | Ominaisuus, jolla voi lukita työkorttilaitteen ja työkorttipäätteen desinfiointia varten | Pakollinen |
| Tuotannonhallinta | Töiden hyväksynnän ja siirron valintaikkunoiden parannukset | Pakollinen |
| Tuotannonhallinta | Rekisterikilpi valmiiksi raportointia varten on lisätty työkorttilaitteeseen | Pakollinen |
| Tuotannonhallinta | Tulosta etiketti työkorttilaitteesta | Pakollinen |
| Tuotannonhallinta | Tuotannon suoritus | Pakollinen |
| Tuotannonhallinta | Tuotannonohjausliittymän käyttöomaisuuden hallintatoiminto | Käytössä oletusarvoisesti |
| Tuotannonhallinta | Töiden haku tuotannon työnohjausliittymälle | Käytössä oletusarvoisesti |
| Tuotannonhallinta | Ohita oletustuotantovaraus | Käytössä oletusarvoisesti |
| Tuotannonhallinta | Näytä täydet sarja-, erä- ja rekisterinumerot tuotannon käyttöliittymässä | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | Myyntitilauksen tietojen suorituskykyparannus | Yleisesti saatavilla |
| Myynti ja markkinointi | Myyntitarjouksen tietojen suorituskykyparannus | Yleisesti saatavilla |
| Myynti ja markkinointi | Myyntitilauksen viitattujen tietojen vientikäytäntö | Pakollinen |
| Myynti ja markkinointi | Myyntitilauksesta ostotilausrivin poistokäytäntöön | Pakollinen |
| Myynti ja markkinointi | Myyntitarjouksen viitattujen tietojen vientikäytäntö | Pakollinen |
| Myynti ja markkinointi | Yhteyshenkilön tietoyksikön viennin optimointi | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | Ota käyttöön myyntitarjousasiakirjan esittely ja asiakirjojen loppulausekentät | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | Paranna 100 parasta -asiakasraportin suorituskykyä | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | Laske arvioitu asiakkaan saldo uudelleen | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | Myyntipalautustilauksen rivin rekisteröinti desimaalitarkkuudella sekä todellisen painon kanssa että ilman todellista painoa | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | Myynnin ja markkinoinnin tallennetut näkymät | Käytössä oletusarvoisesti |
| Myynti ja markkinointi | Myyntitilauksen vahvistus yhdellä napsautuksella | Käytössä oletusarvoisesti |
| Varastonhallinta   | Cross docking -mallit ja sijaintidirektiivit | Yleisesti saatavilla |
| Varastonhallinta   | Poista odotettujen vastaanottojen käyttö laatutilauksissa, joihin varastot ovat estotilassa | Yleisesti saatavilla |
| Varastonhallinta   | Rekisterikilven vastaanottohistoria | Yleisesti saatavilla |
| Varastonhallinta   | Pyöristä määrät alaspäin lähimpään myyntiyksikköön varastoon vapautuksen yhteydessä | Yleisesti saatavilla |
| Varastonhallinta   | Varastosovelluksen työluetteloiden yksikkötuki | Yleisesti saatavilla |
| Varastonhallinta   | Lähetysaallon etikettien tiedot | Yleisesti saatavilla |
| Varastonhallinta   | Käytä nopeampaa ohjelmointirajapintaa konttien sulkemiseen/uudelleenavaamiseen pakkausasemalla | Yleisesti saatavilla |
| Varastonhallinta   | Tarkista täydennystöitä varten valitut mallit | Yleisesti saatavilla |
| Varastonhallinta   | Salli täydennysmallin käyttää olemassa olevaa välitöntä täydennystyötä (yksiköiden välillä) | Pakollinen |
| Varastonhallinta   | Automaattinen GUID-tunnusten määrittäminen WHS-käyttäjän luonnissa | Pakollinen |
| Varastonhallinta   | Tallenna tuotevariantit ja seurantadimensiot varastointisovelluksessa kuormanimikkeen vastaanoton aikana | Pakollinen |
| Varastonhallinta   | Muuta seurantadimensioilla hallittujen nimikkeiden varastotilaa | Pakollinen |
| Varastonhallinta   | Työpoolin vaihtaminen työssä | Pakollinen |
| Varastonhallinta   | Klusterisijainti täynnä | Pakollinen |
| Varastonhallinta   | Klusterin hyllytysominaisuus | Pakollinen |
| Varastonhallinta   | Vahvistus ja siirtäminen | Pakollinen |
| Varastonhallinta   | Vahvista lähtevät lähetykset erätöistä | Pakollinen |
| Varastonhallinta   | Määritä, näytetäänkö vastaanoton yhteenvetosivu mobiililaitteissa | Pakollinen |
| Varastonhallinta   | Manuaalisen varastosiirtotoiminnon lykätty käsittely | Pakollinen |
| Varastonhallinta   | Älä salli sellaisten kuormien luomista, jotka eivät täytä aallon kuormanrakennusmallin vaatimuksia | Pakollinen |
| Varastonhallinta   | Laajennetut rekisterikilpien etikettien asettelut | Pakollinen |
| Varastonhallinta   | Arvioi kaikki useiden varastointiyksiköiden sijaintidirektiivien toiminnot | Pakollinen |
| Varastonhallinta   | Piilota Kokonaisarvo-kenttä Kaikki kuormat- ja Kuorman tiedot -sivuilla | Pakollinen |
| Varastonhallinta   | Rekisterikilven etiketin koontiversiomääritys | Pakollinen |
| Varastonhallinta   | Kuormarivin manuaalinen korjaus järjestelmänvalvojille tai vastaaville luotettaville käyttäjille | Pakollinen |
| Varastonhallinta   | Toimipaikan rekisterikilpien paikannus | Pakollinen |
| Varastonhallinta   | Tuotedimensioiden yhdistäminen sijainnissa | Pakollinen |
| Varastonhallinta   | Tee mobiililaitteen varastosiirron varaston tilan kentästä muokattava | Pakollinen |
| Varastonhallinta   | Manuaalinen myyntirivin keräyspalvelu järjestelmänvalvojalle tai vastaaville luotettaville käyttäjille | Pakollinen |
| Varastonhallinta   | Estä siirtotilauksen lähetettyjen rekisterikilpien käyttäminen muissa varastoissa kuin kohdevarastossa. | Pakollinen |
| Varastonhallinta   | Moniselitteisten sijainnin ja rekisterikilven nimien ratkaisukehote | Pakollinen |
| Varastonhallinta   | Laaduntarkistus | Pakollinen |
| Varastonhallinta   | Uuden varastosovelluksen käyttäjäasetukset, kuvakkeet ja vaiheotsikot | Pakollinen |
| Varastonhallinta   | Sijainnin lisävyöhyke | Käytössä oletusarvoisesti |
| Varastonhallinta   | Luo ja käsittele siirtotilauksia varastosovelluksesta | Käytössä oletusarvoisesti |
| Varastonhallinta   | Ota käyttöön varaston mobiililaitteiden nopea oikeellisuustarkistus | Käytössä oletusarvoisesti |
| Varastonhallinta   | Nimikkeen konsolidointisijainnin käyttöaste | Käytössä oletusarvoisesti |
| Varastonhallinta   | Varastonhallinnan käytettävissä olevan varaston merkintöjen siivoustyön enimmäissuoritusaika | Käytössä oletusarvoisesti |
| Varastonhallinta   | Lähtevän kuormituksen visualisointi | Käytössä oletusarvoisesti |
| Varastonhallinta   | Käsittele varastosovelluksen tapahtumat | Käytössä oletusarvoisesti |
| Varastonhallinta   | Tallennettu näkymä kuormasuunnittelun työtilaa varten | Käytössä oletusarvoisesti |
| Varastonhallinta   | Työn tietosivun tallennettu näkymä | Käytössä oletusarvoisesti |
| Varastonhallinta   | Tallennettu näkymä aallon käsittelyä varten | Käytössä oletusarvoisesti |
| Varastonhallinta   | Tallennetut näkymät kuorman käsittelyä varten | Käytössä oletusarvoisesti |
| Varastonhallinta   | Tallennetut näkymät lähetyksen käsittelyä varten | Käytössä oletusarvoisesti |
| Varastonhallinta   | Aallon erätyön tiedot | Käytössä oletusarvoisesti |
| Varastonhallinta   | Aallon suoritusilmoitukset | Käytössä oletusarvoisesti |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Taloushallinnon ja toimintojen sovellusten ympäristöpäivitykset

Microsoft Dynamics 365 Supply Chain Management 10.0.25 sisältää Platform updateja. Lisätietoja on kohdassa [taloushallinnon ja toimintojen sovellusten (huhtikuu 2022) käyttöympäristön päivitysversio 10.0.25.](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.25 virheenkorjauksista päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja tarkastelemalla [Knowledge Base -artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 1 -suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Katso [Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 1 -suunnitelma](/dynamics365-release-plan/2022wave1/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Poistetut ja vanhentuneet Supply Chain Management -toiminnot

[Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa kerrotaan toiminnoista, jotka on ajoitettu poistettaviksi tai vanhentuviksi tai jotka on poistettu Supply Chain Managementissa.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentunisilmoitus [Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -ohjeaiheessa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
