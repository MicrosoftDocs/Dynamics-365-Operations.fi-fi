---
title: Laadun ja määrityksistä poikkeamisen hallinnan yleiskuvaus
description: Tässä artikkelissa esitellään laadun ja määrityksistä poikkeamisen hallintatoiminnot Microsoft Dynamics 365 Supply Chain Managementissa ja kerrotaan, miten ne voivat parantaa toimitusketjun tuotteiden laatua.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11574"
- intro-internal
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 510dee78f6fed02e6511aedad00fcb1b15195470
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907490"
---
# <a name="quality-and-nonconformance-management-overview"></a>Laadun ja määrityksistä poikkeamisen hallinnan yleiskuvaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa esitellään laadun ja määrityksistä poikkeamisen hallintatoiminnot Microsoft Dynamics 365 Supply Chain Managementissa ja kerrotaan, miten ne voivat parantaa toimitusketjun tuotteiden laatua.

Laadunvarmistus käsittää määrityksistä poikkeavan materiaalin tuotetestausta ja hallintaa. Laadunhallintaprosessit auttavat varmistamaan toimitusketjun tuotteiden korkean tason. Nämä prosessit auttavat myös optimoimaan toimitusketjuprosesseja ja parantamaan asiakastyytyväisyyttä. Laadunhallinnan avulla voit hallita määrityksestä poikkeavien tuotteiden käsittelyaikaa kyseisten tuotteiden lähtöpisteestä riippumatta. Voit linkittää diagnostiikkatulokset korjauksen tehtäviin. Järjestelmä voi ajoittaa tehtäviä korjaamaan ongelmat ja estämään siten niiden toistumisen tulevaisuudessa. Voit seurata laadunhallinnan avulla myös ongelmia ongelmantyypin perusteella (myös sisäiset ongelmat) sekä tunnistaa lyhyt- tai pitkäaikaiset ratkaisut. Suorituskykyilmaisimia (KPI) koskevat tilastot antavat tietoja aiemmista määrityksistä poikkeamiseen liittyvistä ongelmista ja niiden korjaamiseen käytetyistä ratkaisuista. Voit tarkistaa historiallisten tietojen avulla, kuinka tehokkaita aiemmat laatutoimet ovat olleet, ja määrittää, mitkä toimet soveltuvat jatkossa käytettäviksi.

Laadunhallinnan avulla voit hallita määrityksestä poikkeavien tuotteiden käsittelyaikaa niiden lähtöpisteestä riippumatta. Koska vianmääritystyypit linkitetään korjausraportointiin, Supply Chain Management voi ajoittaa ongelmien korjaustehtävät ja estää ongelmien toistuminen.

Määrityksistä poikkeamisen hallintatoiminnon lisäksi laadunhallinta sisältää toiminnon ongelmien seuraamiseen ongelmantyypin perusteella (myös sisäiset ongelmat) sekä lyhyt- tai pitkäaikaisen ratkaisun tunnistamiseen. Suorituskykyilmaisimia (KPI) koskevat tilastot antavat tietoja aiemmista määrityksistä poikkeamiseen liittyvistä ongelmista ja niiden korjaamiseen käytetyistä ratkaisuista. Voit tarkistaa historiallisten tietojen avulla, kuinka tehokkaita aiemmat laatutoimet ovat olleet, ja määrittää, mitkä toimet soveltuvat jatkossa käytettäviksi.

Kun määrität laatuliitoksen, Supply Chain Management voi luoda liiketoiminnan eri prosesseille, tapahtumille ja ehdoille laatutilauksia. Laatuliitos voi koskea tiettyä nimikettä, tiettyä nimikeryhmää tai kaikkia nimikkeitä.

## <a name="examples-of-the-use-of-quality-management"></a>Esimerkkejä laadunhallinnan käytöstä

Laadunhallinta on joustavaa ja se voidaan toteuttaa eri tavoin vastaamaan toimitusketjun työvaiheiden tiettyjen tasojen vaatimuksia. Seuraavassa esimerkissä käsitellään näiden ominaisuuksien mahdollisia käyttötapoja:

- Laadunvalvontaprosessin käynnistäminen automaattisesti ennaltamääritettyjen ehtojen perusteella (esimerkiksi kun tietyn toimittajan ostotilaus rekisteröidään varastossa).
- Varaston esto tarkastuksen aikana, jotta varastoa, jota ei ole hyväksytty, ei käytetä (ostotilausmäärien täysi esto).
- Nimikeotannan käyttö laatuliitoksen osana määritettäessä tarkastettavan fyysisen varaston tämän hetkistä määrää. Otanta voi perustua kiinteisiin määriin, prosenttiosuuteen tai täyteen rekisterikilpeen.
- Luo laatutilaukset osittaisille vastaanotoille. Tilauksen mukana fyysisesti vastaanotettuun määrään perustuva laatutilaus luodaan valitsemalla **Päivitettyä määrää kohden** -valintaruutu **Nimikeotanta**-sivulla.
- Testin pienimmän, suurimman ja tavoiteltavan arvon sisältävien testityyppien luominen sekä sellaisen määrää ja laatua vertailevan testin suorittaminen, jolla on ennalta määritetyt tarkistustulokset.
- Hyväksyttävän laadun tason määrittäminen laadun mittaustoleranssien hallintaa varten.
- Tarkastustyövaiheiden edellyttämien resurssien, kuten testausalueen tai testin mittavälineiden, määrittäminen.

> [!NOTE]
> _Varastoprosessien laadunhallinta_ -ominaisuus laajentaa laadunhallinnan ominaisuuksia. Jos käytät tätä toimintoa, katso kohdasta [Varaston prosessien laadunhallinta](quality-management-for-warehouses-processes.md) esimerkkejä siitä, miten laadunhallinta toimii, kun se otetaan käyttöön.

## <a name="controlling-the-quality-management-process"></a>Laadunhallintaprosessin ohjaus

Voit ohjata laadunhallintaprosessia erimerkiksi seuraavin tavoin:

- Voit luoda käynnistyspisteisiin perustuvia laatutilauksia, kuten saapuvien työvaiheiden tuotteen vastaanotto tai lähtevien työvaiheiden tuotteen keräys.
- Voit dokumentoida testitulokset ja määrittää, vastaavatko tulokset määritettyjä testiehtoja ja hyväksyttävän laadun tasoa.
- Voit käyttää tuotteen tarkkojen teknisten tietojen ja käyttäjäkohtaisten huomautusten tiedostonhallintaa osana raportointia tarkastusprosessin aikana.
- Voit ylläpitää määrityksistä poikkeavia tuotteita ja yhdistää kyseiset tuotteet määrityksistä poikkeamisen lisätietoihin. Tällä tavoin voidaan jäljittää ongelman alkuperäinen syy.
- Voit dokumentoida määrityksistä poikkeamisen hallinnan kustannukset. Näitä kustannuksia voivat olla nimikkeet (kuten varaosat), muut kulut ja aikaraportin tunnit, jotka tarvitaan määrityksistä poikkeamisen korjaamiseen.
- Voit ajoittaa virheiden korjausprosessi käyttämällä laatutilaukseen linkitettyä korjauskäsittelyä.

[![Laadunhallintaprosess.i](media/quality-management-process-diagram.png)](media/quality-management-process-diagram.png)

## <a name="product-testing-and-quality-orders"></a>Tuotetestaus ja laatutilaukset

Tuotetestausta kutsutaan usein laadunvalvonnaksi, ja siinä käytetään laatutilauksia. Voit tehdä seuraavat toimet laadunvalvontatoiminnolla:

- Voit määrittää materiaalille suoritettavat testit. Näitä testejä ovat muun muassa laatumääritykset, mahdolliset testivälineet, testiä kuvaavat asiakirjat, otantasuunnitelma sekä hyväksyttävän laadun tasot.
- Voit luoda laatutilauksen, joka ilmaisee ostotilaukselle, tuotantotilaukselle tai muulle tilaukselle tai tietylle varaston määrälle suoritettavat testit. Voit luoda laatutilauksen manuaalisesti, tai laatutilaukset voidaan luoda automaattisesti laatuohjeiden mukaan.
- Voit määrittää kunkin osto-, karanteeni-, tuotanto- tai myyntitilaukseen liittyvän liiketoimintaprosessin laatuohjeet, joiden perusteella saapuvan ja lähtevän materiaalin testiedellytykset kuvaava laatutilaus voidaan luoda automaattisesti.
- Kirjaa laatutilauksen testitulokset, vahvista testitulosten ja hyväksyttävän laadun tason vastaavuus sekä tulosta testitulokset sisältävä analyysivarmenne.

## <a name="nonconformance"></a>Poikkeama

Määrityksistä poikkeaminen kuvaa nimikettä, jossa on laatuvirhe. Voit luoda määrityksistä poikkeamisprosessissa määrityksistä poikkeamisen tilauksen, joka kuvaa määrityksistä poikkeavaa materiaalia. Tilauksessa kuvataan ongelman lähde ja ongelman tyyppi. Lisäksi tilaus sisältää selitykset. Voit määrittää ongelmatyyppien luokat, mikä helpottaa määrityksistä poikkeavan materiaalin analysointia. Voit myös tulostaa määrityksistä poikkeamisen tunnisteen ja määrityksistä poikkeamisraportin ohjaamaan määrityksistä poikkeavan materiaalin käsittelyä. Tunniste ja raportti voivat esimerkiksi ilmaista tilan **Käyttökelvoton** tai **Rajoitettu käyttö**.

Seuraavassa taulussa on kuusi oletusarvoista määrityksistä poikkeamisen tyyppiä ja selitetään, mitkä tiedot on kirjattava kullekin tyypille.

| Määrityksistä poikkeamisen tyyppi: | Lähteen tiedot |
|---|---|
| Asiakas | Asiakkaan tilinumero, myyntitilausnumero ja myyntitilaustapahtuman eränumero. Määrityksistä poikkeaminen voi esimerkiksi liittyä tiettyyn myyntitilaustoimitukseen tai tuotteen laatua koskevaan asiakaspalautteeseen. |
| Palvelupyyntö | Asiakkaan tilinumero, myyntitilausnumero ja myyntitilaustapahtuman eränumero. Määrityksistä poikkeaminen voi esimerkiksi liittyä tiettyyn myyntitilaustoimitukseen tai asiakkaan valitukseen nimikkeen laadusta. |
| Toimittaja | Toimittajan tilinumero, ostotilausnumero ja ostotilaustapahtuman eränumero. Määrityksistä poikkeaminen voi esimerkiksi liittyä ostotilausten vastaanottoon tai toimittajan huoleen toimittamastaan osasta. |
| Tuotanto | Tuotantotilauksen numero tai tuotantotilaustapahtuman eränumero. Määrityksistä poikkeaminen voi esimerkiksi liittyä tiettyyn tuotettuun erään. |
| Sisäinen | Laatutilauksen numero tai laatutilaustapahtuman eränumero. Määrityksistä poikkeaminen voi esimerkiksi liittyä laatutilauksen osana tehtyihin testeihin tai työntekijän huoleen tuotteen laadusta. |
| Oheistuotteen tuotanto | Erätuotantotilauksiin liittyvä oheistuotteen tuotantotilauksen määrityksistä poikkeaminen. |

Määrityksistä poikkeamiset liitetään ongelmatyyppiin. Ongelmatyypit määritetään **Ongelmatyypit**-sivulla, jossa voit määrittää, mitkä ongelmatyypit voidaan liittää kuhunkin määrityksistä poikkeamisen tyyppiin. **Palvelupyyntö**-tyypin määrityksistä poikkeamisen ongelmatyypit voivat esimerkiksi vastata asiakasvalituksia, kun taas **Sisäinen**-tyypin tyyppi määrityksistä poikkeamisen ongelmatyypit voivat ilmaista vikakoodien luokittelun.

Valitset uuden määrityksistä poikkeamisen luonnin yhteydessä määrityksistä poikkeamisen tyypin ja ongelmatyypin. Alkuperäinen hyväksyntätila on **Uusi**, joka ilmaisee toimintopyynnön. Seuraavaksi hyväksyntäpyynnön tilaksi on vaihdettava **Hyväksytty** tai **Hylätty**, mikä ilmaisee toimitko vai et määrityksestä poikkeamisen suhteen. Voit myös sulkea määrityksistä poikkeamisen (valitsemalla toisen valintaruudun), mikä ilmaisee, että asia on kohdaltasi päättynyt. Voit myös avata määrityksistä poikkeamisen uudelleen ilmaisemaan, että lisäharkintaa tarvitaan.

Voit lisätä määrityksistä poikkeamiseen kommentteja liittämällä asiakirjan. Määrityksistä poikkeamisille kannattaa määrittää yksilöllinen asiakirjatyyppi **Asiakirjatyyppi**-sivulla. Voit sitten määrittää **Raportin asetukset** -sivulla, tulostetaanko tämän asiakirjatyypin kommentit määrityksistä poikkeamisraporttiin ja määrityksistä poikkeamisen tunnisteeseen. Määrityksistä poikkeamisraporttia ja -tunniste voivat auttaa materiaalin käsittelyssä. Voit muodostaa valikoivasti raportteja ja tunnisteita määrityksistä poikkeamiseen liitettyjen valintaehtojen perusteella. Näitä ehtoja ovat määrityksistä poikkeamisnumeron, nimike, asiakas, toimittaja ja tila.

Määrityksistä poikkeamisraportti sisältää määrityksistä poikkeamisen numeron, nimikkeen ja ongelmatyypin. Raportin asetuskäytännön mukaan raportissa voi olla myös määrityksistä poikkeamiseen liittyviä huomautuksia. Määrityksistä poikkeamisen tunnisteessa on vastaavia tietoja sekä karanteenivyöhyke ja määrityksistä poikkeamisille määritetty tyyppi (kuten **Rajoitettu käyttö** tai **Käyttökelvoton**), joka opastaa viallisen materiaalin käsittelyssä.

## <a name="approved-nonconformance"></a>Hyväksytty määrityksistä poikkeaminen

Voit vaihtoehtoisesti määrittää yhden tai useita liittyviä toimintoja hyväksyttyä määrityksistä poikkeamista varten. Liittyvässä työvaiheessa on suoritettavan työn kuvaus sekä luettelo määritetyistä laatutoiminnoista ja työn syyn kuvaus. Toiminnon määrittämisen jälkeen voit vaihtoehtoisesti määrittää muita maksuja, nimikkeitä ja aikaraportin työtunteja, jotka ovat edellytyksenä työn suorittamiselle. Näkyvissä on liittyvän toiminnon lasketut kustannukset ja määrityksistä poikkeamisten lasketut kokonaiskustannukset. Lasketut kustannukset ja pohjana olevat tiedot (nimikkeistä, työtunneista ja muista maksuista) edustavat viitetietoja, ja niitä käytetään vain laadunhallintatoiminnossa.

Voit vaihtoehtoisesti luoda laatutilauksen määrityksistä poikkeamisesta suorittamalla ensin kyselyn laatutilauksista ja luomalla sitten uuden laatutilauksen. Laatutilaus voi esimerkiksi ilmaista tarpeen testata tai uudelleentestata viallista materiaalia. Äskettäin luodussa laatutilauksessa on linkki alkuperäiseen määrityksistä poikkeamiseen.

Voit vaihtoehtoisesti linkittää yhden määrityksistä poikkeamisen toiseen ja luoda uuden määrityksistä poikkeamisen aiemmin luodusta. Linkki voi esimerkiksi ilmaista laatuongelmien välistä suhdetta.

## <a name="correction-handling"></a>Korjausten käsittely

Voit luoda **Korjaukset**-sivulla luettelon korjattavista määrityksistä poikkeamisista. Jokainen korjausnimike liitetään diagnostiikkatyypin, jolla ongelma havaittiin. **Korjaukset**-sivulla on myös tiedot siitä, kenen on suoritettava korjaustoiminto ja milloin se on suoritettava. Voit lisätä ongelman kuvauksen ja suoritettavan korjaustoiminnon liittämällä korjaukseen asiakirjan. Kun määrityksistä poikkeaminen on käsitelty tai korjattu, voit sulkea korjausnimikkeen valitsemalla **Valmis**. Voit myös ilmaista, että kyse oli lyhytaikaisesta ratkaisusta.

Korjauksille kannattaa määrittää yksilöllinen asiakirjatyyppi **Asiakirjatyyppi**-sivulla. Voit sitten määrittää **Raportin asetukset** -sivulla, tulostetaanko tämän asiakirjatyypin kommentit korjausraporttiin. Tulostetussa korjausraportissa on tietoja määrityksistä poikkeamisesta ja liittyvistä määrityksistä poikkeamisen huomautuksista. Raportissa on myös korjaustietoja, kuten diagnostiikkatyyppi, ja liittyvät korjaushuomaukset.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](enable-quality-management.md)
- [Varastoesto](inventory-blocking.md)
- [Karanteenitilaukset](quarantine-orders.md)
- [Tarkista tavaroiden laatu](tasks/inspect-quality-goods.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
