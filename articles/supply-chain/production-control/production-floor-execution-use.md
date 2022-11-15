---
title: Kuinka työntekijät käyttävät tuotannon käyttöliittymää
description: Tässä artikkelissa käsitellään tuotannon käyttöliittymää työntekijän näkökulmasta.
author: johanhoffmann
ms.date: 01/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 876ee36c75a31ca89a9351d0ee1484e66076b6aa
ms.sourcegitcommit: 4abf9b375fed6885ea11a425c524958fea29c3b9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748710"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Tuotannon käyttöliittymän käytön ohjeet työntekijöille

[!include [banner](../includes/banner.md)]

Tuotannon käyttöliittymä on optimoitu kosketuskäyttöön. Siihen suunniteltu visuaalinen kontrasti vastaa tuotantoympäristön helppokäyttöisyysvaatimuksia. Siinä on kaikki samat toiminnalliset ominaisuudet kuin työkorttilaitteessa. Siinä voidaan kuitenkin aloittaa myös rinnakkain useita töitä työluettelosta. (Tätä ominaisuutta kutsutaan myös *töiden niputukseksi*.) Työntekijät voivat avata työluettelosta myös Microsoft Dynamics 365 Guidesissa luodun oppaan. He saavat tällä tavoin visuaalisia ohjeita HoloLensissa.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Kirjautuminen tuotannon käyttöliittymään työntekijänä

Ennen kuin työntekijät voivat aloittaa laitteen käytön, työnjohtajan tai teknisen henkilökunnan on valmisteltava se ja avattava oikea sivu Dynamics 365 Supply Chain Managementissa. Lisätietoja laitteen määrittämisestä on kohdassa [Laitteen määrittäminen käyttämään tuotannon käyttöliittymää](production-floor-execution-setup.md).

Kun laite on valmisteltu, kirjautumissivu avautuu. Tällä sivulla on tietoja paikallisen työsolun töiden tilasta. Nämä tiedot päivitetään säännöllisesti. Työntekijät kirjautuvat sivulla käyttämällä nimilappunsa tunnusta. Vaikka työntekijöillä ei tarvitse olla Supply Chain Managementin käyttäjätiliä, heillä on oltava *aikarekisteröidyn työntekijän* tili, jolla he kirjautuvat sisään.

![Tuotannon käyttöliittymän kirjautumissivu.](media/pfei-sign-in-page.png "Tuotannon käyttöliittymän kirjautumissivu")

Tämän artikkelin muissa osissa käsitellään tapoja, joilla työntekijät käyttävät liittymää.

## <a name="all-jobs-tab"></a>Kaikki työt -välilehti

**Kaikki työt** -välilehdessä on työluettelo. Tässä luettelossa on kaikki ne tuotantotyöt, joiden tila on *Ei aloitettu*, *Pysäytetty* tai *Aloitettu*. (Tätä välilehden nimiä voi mukauttaa, joten sillä voi olla eri nimi omassa järjestelmässä.)

![Kaikki työt -välilehti.](media/pfei-all-jobs-tab.png "Kaikki työt -välilehti")

Työluettelossa on seuraavat sarakkeet. Numerot vastaavat edellisessä kuvassa käytettyjä numeroita.

1. **Valintasarake** – Vasemmassa sarakkeessa käytetään valintamerkkejä ilmaisemaan työt, jotka työntekijä on valinnut. Työntekijät voivat valita luettelossa useita töitä samanaikaisesti. Kaikki työt voidaan valita valitsemalla valintamerkki sarakkeen otsikossa. Jos töitä valitaan yksi, kyseisen työn tiedot näytetään sivun alareunassa.
1. **Työn tilasarake** – Tämä sarake ilmaisee symboleilla kunkin työn tilan. Jos työllä ei ole tässä sarakkeessa symbolia, sen tila on *Ei aloitettu*. Vihreä kolmio ilmaisee työn, jonka tila on *Aloitettu*. Kaksi keltaista pystysuoraa viivaa ilmaisevat työn, jonka tila on *Pysäytetty*.
1. **Korkea prioriteetin sarake** – tämä sarake ilmaisee huutomerkillä työn, jolla on korkea prioriteetti.
1. **Tilaus** – tämä sarake näyttää työn tuotantotilauksen numeron.
1. **Kuvaus** – tämä sarake näyttää sen toiminnon kuvauksen, jonka osa työ on.
1. **Pyydetty** – tämä sarake näyttää määrän, joka työn on tarkoitus valmistaa.
1. **Aloitettu** – tämä sarake näyttää määrän, joka on työlle jo aloitettu.
1. **Valmis** – tämä sarake näyttää määrän, joka työstä on jo valmistunut.
1. **Hävikki** – tämä sarake näyttää määrän, joka on työstä jo hävikkiä.
1. **Jäljellä** – tämä sarake näyttää määrän, joka työstä on vielä valmistumatta.

## <a name="active-jobs-tab"></a>Aktiiviset työt -välilehti

**Aktiiviset työt** -välilehdissä on luettelo kaikista töistä, jotka kirjautunut työntekijä on jo aloittanut. (Tätä välilehden nimiä voi mukauttaa, joten sillä voi olla eri nimi omassa järjestelmässä.)

![Aktiiviset työt -välilehti.](media/pfei-active-jobs-tab.png "Aktiiviset työt -välilehti")

Aktiivisten töiden luettelossa on seuraavat sarakkeet:

- **Valintasarake** – Vasemmassa sarakkeessa käytetään valintamerkkejä ilmaisemaan työt, jotka työntekijä on valinnut. Työntekijät voivat valita luettelossa useita töitä samanaikaisesti. Kaikki työt voidaan valita valitsemalla valintamerkki sarakkeen otsikossa. Jos töitä valitaan yksi, kyseisen työn tiedot näytetään sivun alareunassa.
- **Tilaus** – tämä sarake näyttää työn tuotantotilauksen numeron.
- **Kuvaus** – tämä sarake näyttää sen toiminnon kuvauksen, jonka osa työ on.
- **Pyydetty** – tämä sarake näyttää määrän, joka työn on tarkoitus valmistaa.
- **Aloitettu** – tämä sarake näyttää määrän, joka on työlle jo aloitettu.
- **Valmis** – tämä sarake näyttää määrän, joka työstä on jo valmistunut.
- **Hävikki** – tämä sarake näyttää määrän, joka on työstä jo hävikkiä.
- **Jäljellä** – tämä sarake näyttää määrän, joka työstä on vielä valmistumatta.

## <a name="my-jobs-tab"></a>Omat työt -välilehti

**Omat työt** -välilehden avulla työntekijät voivat helposti tarkastella kaikkia heille määritettyjä keskeneräisiä töitä. Tämä ominaisuus on hyödyllinen yrityksille, jotka joskus tai aina määrittävät työt tietyille työntekijöille (henkilöstöresursseille) muiden resurssityyppien (kuten koneiden) sijaan.

Ajoitusjärjestelmä määrittää kunkin tuotantotyön automaattisesti tietylle resurssitietueelle, ja kullakin resurssitietueella on tyyppi (esimerkiksi kone tai henkilö). Kun määrität työntekijän tuotantotyöntekijäksi, voit liittää työntekijätilin yksilöivään henkilöstöresurssitietueeseen.

Kaikki sisäänkirjautuneen työntekijän henkilöstötietueeseen määritetyt aloittamattomat ja keskeneräiset työt näkyvät **Omat työt** -välilehdessä, jos työntekijä on kirjautunut sisään. Siinä ei kuitenkaan ole luetteloa koneelle tai muulle resurssityypille määritetyistä töistä, vaikka sisäänkirjautunut työntekijä olisi alkanut työstää tällaisia töitä.

Voit tarkastella kaikkia sisäänkirjautuneen työntekijän aloittamia töitä riippumatta siitä, mihin resurssityyppiin kukin työ on liitetty, käyttämällä **Aktiiviset työt** -välilehteä. Voit nähdä kaikki keskeneräiset työt, jotka vastaavat paikallista työn suodatuskonfiguraatiota työntekijästä tai aloitustilasta riippumatta, käyttämällä **Kaikki työt** -välilehteä.

![Omat työt -välilehti.](media/pfei-my-jobs-tab.png "Omat työt -välilehti")

## <a name="my-machine-tab"></a>Oma kone -välilehti

**Oma kone** -välilehdessä työntekijät voivat valita resurssin, joka on liitetty koneresurssiin **Kaikki työt** -välilehdessä määritetyssä suodattimessa. Työntekijät voi sitten tarkastella valitun resurssin tilaa ja kuntoa lukemalla enintään neljän valitun laskurin arvot sekä viimeaikaisten ylläpitopyyntöjen ja rekisteröityjen seisokkien luetteloita. Työntekijät voi myös pyytää valitun resurssin ylläpitoa sekä rekisteröidä ja muokata koneen seisokkeja. (Tätä välilehden nimiä voi mukauttaa, joten sillä voi olla eri nimi omassa järjestelmässä.)

![Oma kone -välilehti.](media/pfei-my-machine-tab.png "Oma kone -välilehti")

**Oma kone** -välilehdessä on seuraavat sarakkeet. Numerot vastaavat edellisessä kuvassa käytettyjä numeroita.

1. **Koneresurssi** – Valitse seurattava koneresurssi. Aloita nimen kirjoittaminen ja tee valinta kirjoitusta vastaavien resurssien luettelosta. Vaihtoehtoisesti voit valita suurennuslasikuvakkeen ja tehdä valinnan luettelossa, jossa on kaikki työluettelon suodattimessa oleviin resursseihin liitetyt resurssit.

    > [!NOTE]
    > Supply Chain Managementin käyttäjät voivat määrittää tarpeen mukaan kullekin resurssille resurssin **Kaikki resurssit** -sivulla (**Käyttöomaisuus**-välilehden avattavassa **Resurssi**-luettelossa). Lisätietoja on kohdassa [Resurssin luominen](../asset-management/objects/create-an-object.md).

1. **Asetukset** – Valitse rataskuvake ja avaa valintaikkuna, jossa voidaan valita, mitä valitun koneresurssin laskureita tarkastellaan. Näiden laskureiden arvot näytetään **Resurssien hallinta** -välilehden yläosassa. (Seuraavassa näyttökuvassa olevassa) **Asetukset**-valikossa voi ottaa käyttöön enintään neljä laskuria. Valitse kukin käyttöönotettava laskuri käyttämällä ruudun yläosassa olevaa hakukenttää. Hakukentässä on luettelo kaikista valittuun resurssiin liitetyistä laskurista. Resurssi valittiin **Resurssien hallinta** -sivun yläosassa. Määritä kukin laskuri seuraamaan joko **Koottu**-arvoa ja laskurin uusinta **Toteutunut**-arvoa. Jos määritetty laskuri esimerkiksi seuraa, kuinka monta tuntia kone on ollut käytössä, määrityksenä on oltava **Koottu**. Jos laskuri määritetään seuraamaan viimeksi päivitettyä lämpötilaa tai painetta, määrityksenä on oltava **Toteutunut**. Valitse **OK** tallentaaksesi asetukset ja sulje valintaikkuna.

    ![Oma kone -välilehden asetukset.](media/pfei-my-machine-tab-settings.png "Oma kone -välilehden asetukset")

1. **Yläpitopyyntö** – Tämän painikkeen valinta avaa valintaikkunan, jossa voidaan luoda ylläpitopyyntö. Pyynnölle voi antaa kuvauksen ja lisätä huomautuksen. Pyyntö tulee Supply Chain Management -käyttäjän näkyville, ja tämä käyttäjä voi sitten muuntaa ylläpitopyynnön ylläpidon työtilaukseksi.
1. **Rekisteröi seisokki** – Tämän painikkeen valinta avaa valintaikkunan, jossa voi rekisteröidä koneen seisokin. Seisokille voidaan valita syykoodi ja antaa seisokin ajankohta ja kesto. Koneen seisokkirekisteröinnin avulla lasketaan koneresurssin tehokkuus.
1. **Näytä tai muokkaa** – tämän painikkeen valinta avaa valintaikkunan, jossa voi muokata tai tarkastella aiemmin luotuja seisokkitietueita.

## <a name="starting-and-completing-production-jobs"></a>Tuotantotöiden aloittaminen ja valmistuminen

Työntekijä aloittaa tuotantotyön valitsemalla työn **Kaikki työt** -välilehdessä ja avaamalla **Aloita työ** -valintaikkunan sitten valitsemalla **Aloita työ**.

![Aloita työ -valintaikkuna.](media/pfei-start-job-dialog.png "Aloita työ -valintaikkuna")

Työntekijät vahvistavat **Aloita työ** -valintaikkunassa tuotannon määrän ja aloittavat sitten työn. Työntekijät voivat säätää määrää valitsemalla **Määrä**-kentän ja käyttämällä avautuvaa numeronäppäimistöä. Työntekijät aloittavat sitten työn tekemisen valitsemalla **Aloita**. **Aloita työ** -valintaikkuna suljetaan ja työ lisätään **Aktiiviset työt** -välilehteen.

Työntekijät voivat aloittaa työn riippumatta siitä, mikä sen tila on. Jos työntekijä aloittaa työn, jonka tila on *Ei aloitettu*, **Aloita työ** -valintaikkunan **Määrä**-kentässä on aluksi koko määrä. Jos työntekijä aloittaa työn, jonka tila on *Aloitettu* tai *Pysäytetty*, **Määrä**-kentässä on aluksi jäljellä oleva määrä.

## <a name="reporting-good-quantities"></a>Hyväksyttyjen määrän ilmoittaminen

Kun työntekijä tekee työn kokonaan tai osittain valmiiksi, hän voi raportoida tuotetut hyväksyttävät määrät valitsemalla työn **Aktiiviset työt** -välilehden ja valitsemalla sitten **Raportointi on meneillään**. Tämän jälkeen työntekijä antaa **Raportointi on meneillään** -valintaikkunassa hyväksyttyjen määrän numeronäppäimistössä. Määrä on oletusarvoisesti tyhjä. Työntekijä voi määrän antamisen jälkeen päivittää työn tilaksi *Käsittelyssä*, *Pysäytetty* tai *Valmis*.

![Raportointi on meneillään -valintaikkuna.](media/pfei-report-progress-dialog.png "Raportointi on meneillään -valintaikkuna")

## <a name="reporting-good-quantities-on-batch-orders-that-have-co-products-and-by-products"></a>Tuotemäärien raportointi sellaisten erätilausten osalta, joilla on oheis- ja sivutuotteita

Työntekijät voivat käyttää tuotannon suoritusliittymää erätilausten edistymisen raportointiin. Tähän raportointiin kuuluu oheis- ja sivutuotteita koskeva raportointi.

Jotkut valmistajat erityisesti prosessitoimialoilla käyttävät erätilauksia tuotantoprosessiensa hallintaan. Erätilaukset luodaan kaavojen perusteella, ja nämä kaavat voidaan määritellä siten, että niiden tuloksena on oheis- ja sivutuotteita. Kun palautetta näistä erätilauksista raportoidaan, tulosten määrä on rekisteröitävä reseptinimikkeeseen sekä oheis- ja sivutuotteisiin.

Kun työntekijä saa erätilaukseen liittyvän tehtävän valmiiksi tai osittain valmiiksi, hän voi raportoida kullekin tilauksen tulokseksi määritetylle tuotteelle tuote- tai hävikkimääriä. Erätilauksen tulokseksi määritetyt tuotteet voivat olla tyyppiä *Kaava*, *Oheistuote* tai *Sivutuote*.

Tuotteiden tuotemäärien raportointia varten työntekijä valitsee tehtävän **Aktiiviset tehtävät** -välilehdestä ja valitsee sitten **Raportoi edistyminen**.

Sitten työntekijä voi valita **Raportoi edistyminen** -valintaruudussa raportoitavan tuotteen niiden tuotteiden joukosta, jotka on määritetty erätyön tuloksiksi. Työntekijä voi valita jonkin luettelon useista tuotteista ja valita sitten **Raportoi edistyminen**. Kunkin tuotteen osalta määrä on oletusarvoisesti tyhjä, ja työntekijä voi syöttää määrän numeronäppäimistöllä. Työntekijä voi siirtyä valittujen tuotteiden välillä painikkeiden **Edellinen** ja **Seuraava** avula. Työntekijä voi kunkin tuotteen määrän antamisen jälkeen päivittää työn tilaksi *Käsittelyssä*, *Pysäytetty* tai *Valmis*.

![Oheis- ja sivutuotteiden raportointi.](media/report-co-by-products.png "Oheis- ja sivutuotteiden raportointi")

### <a name="reporting-on-batch-orders-for-planning-items"></a>Suunnittelunimikkeiden erätilauksia koskeva raportointi

Kun työntekijä saa suunnittelunimikkeen erätilauksen tehtävän valmiiksi, hän raportoi määrät vain oheis- ja sivutuotteiden osalta, koska suunnittelunimikkeet eivät sisällä *Kaava*-tyypin nimikettä.

### <a name="reporting-co-product-variation"></a>Oheistuotteiden vaihtelua koskeva raportointi

Jos erätilaus luodaan kaavaversiosta, jossa **Oheistuotteen variaatiot** -asetuksen arvoksi on määritetty *Kyllä*, työntekijä voi raportoida oheistuotteista, jotka eivät kuulu erätuotteiden määritelmään. Tätä toimintoa käytetään skenaarioissa, joissa tuotantoprosessissa voi esiintyä odottamaton tuotetulos.

Tällöin työntekijä voi määrittää raportoitavan oheistuotteen ja määrän valitsemalla **Oheistuotteiden variaatiot** raportin edistymisen valintaikkunassa. Sitten työntekijä voi valita kaikista julkaistuista tuotteista, jotka on määritetty oheistuotteiksi.

### <a name="reporting-catch-weight-items"></a>Todellisen painon nimikkeiden raportointi

Työntekijät voivat käyttää tuotannon suoritusliittymää todellisen painon nimikkeille luotujen erätilausten edistymisen raportointiin. Erätilaukset luodaan kaavojen perusteella, ja nämä kaavat voidaan määritellä siten, että niissä on todellisen painon nimikkeet kaavanimikkeinä, oheistuotteina ja sivutuotteina. Kaavan voi määrittää myös, jos kaavarivit on määritetty todellisen painon ainesosille. Todellisen painon nimikkeissä käytetään kahta mittayksikköä varaston seuraamiseksi: todellisen painon määrä ja varastomäärä. Esimerkiksi elintarviketeollisuudessa laatikollinen lihaa voidaan määrittää todellisen painon nimikkeeksi, jossa todellisen painon määrää käytetään laatikoiden määrän seuraamiseen, ja varastomäärää käytetään laatikoiden painon seuraamiseen.

## <a name="reporting-scrap"></a>Hävikin raportointi

Kun työntekijä tekee työn kokonaan tai osittain valmiiksi, hän voi raportoida hävikin valitsemalla työn **Aktiiviset työt** -välilehden ja valitsemalla sitten **Hävikin raportointi**. Tämän jälkeen työntekijä antaa **Hävikin raportointi** -valintaikkunassa hävikin määrän numeronäppäimistöllä. Työntekijä valitsee myös syyn (*Ei yhtään*, *Kone*, *Käyttäjä* tai *Materiaali*).

![Hävikin raportointi -valintaikkuna.](media/pfei-report-scrap-dialog.png "Hävikin raportointi -valintaikkuna")

## <a name="adjust-material-consumption-and-make-material-reservations"></a>Materiaalikulutuksen oikaiseminen ja materiaalivarausten tekeminen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Työntekijät voivat säätää kunkin tuotantotyön materiaalikulutusta. Tätä toimintoa käytetään tilanteissa, joissa tuotantotyössä kulutetun materiaalien todellinen määrä on suurempi tai pienempi kuin suunniteltu määrä. Siksi varastotasot on muutettava niin, että ne ovat ajan tasalla.

Työntekijät voivat myös tehdä varauksia materiaalien erä- ja sarjanumeroista. Tätä toimintoa käytetään tilanteissa, joissa työntekijän on määritettävä manuaalisesti, mitä materiaalin erä- tai sarjanumeroita kulutettiin, täyttääkseen materiaaliin liittyvät jäljitysvaatimukset.

Työntekijät voivat määrittää oikaistavat määrän valitsemalla **Oikaise materiaali**. Tämä painike on käytettävissä seuraavissa sijainneissa:

- **Hävikin raportointi** -valintaikkunassa
- **Edistymisen raportointi** -valintaikkunassa
- Oikealla työkalurivissä

### <a name="adjust-material-consumption-from-the-report-scrap-and-report-progress-dialog-boxes"></a>Materiaalikulutuksen oikaiseminen Hävikin raportointi- ja Raportointi on meneillään -valintaikkunoissa

Kun työntekijä on syöttänyt määrän raporttiin **Edistymisen raportointi**- tai **Hävikin raportointi** -valintaikkunassa, **Materiaalin oikaiseminen** -painike on käytettävissä. Kun käyttäjä valitsee tämän painikkeen, näyttöön tulee **Materiaalin oikaiseminen** -valintaikkuna. Tässä valintaikkunassa luetellaan nimikkeet, jotka on suunniteltu kulutettavaksi, kun työn hyvä määrä tai hävikkimäärä raportoidaan.

Valintaikkunan luettelossa on seuraavat tiedot:

- **Tuotenumero** – Päätuote ja tuotevariantti.
- **Tuotteen nimi** – Tuotteen nimi.
- **Ehdotus** – Arvioitu materiaalimäärä, joka kulutetaan, kun työn määritetyn määrän edistyminen tai hävikki ilmoitetaan.
- **Kulutus** – Todellinen materiaalimäärä, joka kulutetaan, kun työn määritetyn määrän edistyminen tai hävikki ilmoitetaan.
- **Varattu** – Materiaalimäärä, joka on fyysisesti varattu varastossa.
- **Yksikkö** – Tuoterakenteen (BOM) yksikkö.

Valintaikkunan oikeassa reunassa näkyy seuraavat tiedot:

- **Tuotenumero** – Päätuote ja tuotevariantti.
- **Arvioitu** – Arvioitu kulutettava määrä.
- **Aloitettu** – Tuotantotyön aloitettu määrä.
- **Jäljelle jäävä määrä** – Arvioidusta määrästä se määrä, joka on vielä kulutettava.
- **Vapautettu määrä** – Määrä, joka on kulutettu.

Voidaan tehdä seuraavia toimenpiteitä:

- Työntekijä voi määrittää materiaalin oikaistavat määrän valitsemalla **Oikaise kulutus**. Kun määrä on vahvistettu, **Kulutus**-sarakkeen määrä päivitetään oikaistulla määrällä.
- Kun työntekijä valitsee **Materiaalin oikaiseminen**, tuotannon keräysluettelon kirjauskansio luodaan. Tämä kirjauskansio sisältää samat nimikkeet ja määrät kuin **Oikaise materiaali** -luettelo.
- Kun työntekijä muuttaa määrää **Oikaise materiaali** -valintaikkunassa, vastaavan kirjauskansiorivin **Ehdotus**-kenttään päivitetään sama määrä. Jos työntekijä valitsee **Oikaise materiaali** -valintaikkunassa **Peruuta**, keräysluettelo poistetaan.
- Jos työntekijä valitsee **OK**, keräysluetteloa ei poisteta. Se kirjataan, kun työ raportoidaan **Hävikin raportointi**- tai **Edistymisen raportointi**-valintaikkunassa.
- Jos työntekijä valitsee **Edistymisen raportointi**- tai **Hävikin raportointi** -valintaikkunassa **Peruuta**, keräysluettelo poistetaan.

### <a name="adjust-material-from-the-primary-or-secondary-toolbar"></a>Materiaalin säätäminen ensisijaisella tai toissijaisella työkalurivillä

**Materiaalin säätäminen** -painike voidaan konfiguroida niin, että se näkyy ensisijaisella tai toissijaisella työkalurivillä. (Lisätietoja on kohdassa [Suunnittele tuotantotilan suorituksen liittymä](production-floor-execution-tabs.md).) Työntekijä voi valita käynnissä olevaa tuotantotyötä varten **materiaalin oikaisemisen**. Tässä tapauksessa näyttöön tulee **Materiaalin oikaiseminen** -valintaikkuna, jossa työntekijä voi tehdä haluamansa muutokset. Kun valintaikkuna avataan, tuotantotilausta varten luodaan oikaistuja määriä sisältävien rivien tuotannon keräysluettelo. Jos työntekijä valitsee **Kirjaa nyt**, oikaisu vahvistetaan ja keräysluettelo kirjataan. Jos työntekijä valitsee **Peruuta**, keräysluettelo poistetaan eikä oikaisua tehdä.

### <a name="adjust-material-consumption-for-catch-weight-items"></a>Todellisen painon nimikkeiden materiaalikulutuksen oikaiseminen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Työntekijät voivat oikaista todellisen painon nimikkeiden materiaalikulutuksen. Tätä toimintoa käytetään tilanteissa, joissa tuotantotyössä kulutetun todellisen painon materiaalien todellinen määrä on suurempi tai pienempi kuin suunniteltu määrä. Siksi varastotasot on muutettava niin, että ne ovat ajan tasalla. Kun työntekijä oikaisee todellisen painon nimikkeen kulutuksen, hän voi muokata sekä todellisen painon määrää että varastomäärää. Jos tuotantotyö on suunniteltu esimerkiksi kuluttamaan viisi laatikkoa, joiden arvioitu paino on 2 kilogrammaa laatikolta, työntekijä voi säätää sekä kulutettavien laatikoiden määrää että laatikoiden painoa. Järjestelmä vahvistaa, että määritetty laatikoiden paino on vapautettavassa tuotteessa määritetyn vähimmäis- ja enimmäisrajan sisällä.

### <a name="reserve-materials"></a>Varaa materiaalit

**Materiaalien oikaiseminen** -valintaikkunassa työntekijä voi tehdä ja oikaista materiaalivarauksia valitsemalla **Varaa materiaali**. Näyttöön tulevassa **Varaa materiaali** -valintaikkunassa näkyy nimikkeen fyysisesti saatavilla oleva varasto kutakin varasto- ja seurantadimensiota varten.

Jos materiaali on otettu käyttöön varastonhallintaprosesseissa (WMS), luettelossa näkyy vain tuotannon syötteen materiaalin sijainnin fyysisesti käytettävissä oleva varasto. Tuotannon syötteen sijainti määritetään resurssissa, jossa tuotantotyö suunnitellaan. Jos nimiketunnusta ohjataan erä- tai sarjanumerolla, näkyvissä on fyysisesti käytettävissä olevien erä- ja sarjanumeroiden luettelo. Jos haluat määrittää varattavan määrän, työntekijä voi valita **Varaa materiaali**. Jos haluat poistaa aiemmin luodun varauksen, työntekijä voi valita **Poista varaus**.

Lisätietoja tuotannon syötesijainnin määrittämisestä on seuraavassa blogikirjoituksessa: [Tuotannon syötesijainnin määrittäminen](/archive/blogs/axmfg/deliver-picked-materials-to-the-locations-where-the-materials-are-consumed-by-operations-in-production).

> [!NOTE]
> Työntekijän **Varaa materiaali** -valintaikkunassa varaukset säilyvät, kun työntekijä valitsee **Edistymisen raportointi**- tai **Hävikin raportointi** -valintaikkunassa **Peruuta**.
>
> Todellisen painon nimikkeiden varauksia ei voi oikaista.

## <a name="completing-a-job-and-starting-a-new-job"></a>Työn valmistuminen ja uuden työn aloittaminen

Työntekijät päättävät työn yleensä valitsemalla ainakin yhden meneillään olevan työn **Aktiiviset työt** välilehdessä ja valitsemalla sitten **Raportointi on meneillään**. Seuraavaksi he antavat tuotetun määrän (hyväksyttyjen määrä) ja määrittävät tilaksi *Valmis*. Jos valittuna oli useita töitä, työntekijä siirtyy sitten työstä toiseen **Edellinen**- ja **Seuraava**-painikkeilla. Työntekijä aloittaa uuden työn valitsemalla ensin **Kaikki työt** -välilehden ja sitten **Aloita työ**.

Työntekijä voi aloittaa uuden työn, vaikka edellinen työ olisi edelleen avoinna. Työntekijä valitsee taas uuden työn **Kaikki työt** -välilehdessä ja valitsee sitten **Aloita työ**. Tässä tapauksessa **Aloita työ** -valintaikkuna kuitenkin ilmaisee työntekijälle, että he tekevät jo työtä ja että heidän on sen vuoksi joko pysäytettävä tai päätettävä kyseinen työ ennen uuden työn aloittamista.

## <a name="working-on-multiple-jobs-in-parallel"></a>Useiden töiden tekeminen rinnakkain

Yksi työntekijä voi tehdä useita töitä samanaikaisesti (eli rinnakkain). Tässä tapauksessa työntekijän tekemää töiden kokoelmaa kutsutaan *töiden niputukseksi*. Työntekijä voi lisätä uusia töitä nippuun tai päättää yhden työn tai useita töitä nipussa. Seuraavat kaksi skenaariota osoittavat, miten työntekijä voi tehdä töitä rinnakkain.

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>Skenaario 1: työntekijä, jolla ei ole yhtään aktiivista työtä, haluaa aloittaa kaksi työtä ja tehdä niitä rinnakkain

Työntekijä valitsee kaksi työtä **Kaikki työt** -välilehdessä ja valitsee sitten **Aloita työ**. Molemmat valitut työt näkyvät **Aloita työ** -valintaikkunassa, ja työntekijä voi muuttaa kummankin työ määrää. Työntekijä vahvistaa sitten valintaikkunan ja voi aloittaa molemmat työt.

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>Skenaario 2: työntekijä, jolla on kaksi keskeneräistä aktiivista työtä, haluaa aloittaa kolmannen työn ja tehdä sitä rinnakkain kahden muun työn kanssa

Työntekijä valitsee kolmannen työn **Kaikki työt** -välilehdessä ja valitsee sitten **Nippu**. Työntekijä voi aloittaa muuttamalla määrää **Nippu**-valintaikkunassa. Työntekijä vahvistaa sitten valintaikkunan valitsemalla **Nippu**.

## <a name="working-on-indirect-activities"></a>Epäsuorien tehtävien tekeminen

Epäsuorat tehtävät ovat tehtäviä, jotka eivät liity suoraan tuotantotilaukseen. Epäsuorat tehtävät voidaan määrittää joustavasti, mistä on lisätietoja kohdassa [Työajan seurannan epäsuorien tehtävien määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

Shannon, joka on Contoson tuotannon työntekijä, haluaa esimerkiksi osallistua yrityksen kokoukseen, ja kokouksia pidetään epäsuorina tehtävinä. Jompikumpi seuraavista skenaarioista on käytössä:

- **Shannon tekee vähintään yhtä aktiivista työtä.** Shannon valitsee **Tehtävä**-kohdan, määrittää tehtävän (kokous) ja vahvistaa valinnan. Avautuva sanoma ilmoittaa, että hänellä on keskeneräisiä töitä. Shannon voi valita sanomassa tekemiensä töiden päättämisen tai pysäyttämisen ennen kokoukseen lähtemistä.
- **Shannonilla ei ole aktiivisia töitä.** Shannon valitsee **Tehtävä**-kohdan, määrittää tehtävän (kokous) ja vahvistaa valinnan. Hänet on kirjattu kokouksessa olevaksi.

Kun Shannon on vahvistanut valintansa kummassakin skenaariossa, hän siirtyy joko kirjautumissivulle tai sivulle, joka odottaa hänen vahvistavan paluun epäsuorasta tehtävästä. Avautuva sivu määräytyy tuotannon käyttöliittymän määritysten mukaan. (Lisätietoja on kohdassa [Tuotannon käyttöliittymän määrittäminen](production-floor-execution-configure.md).)

## <a name="registering-breaks"></a>Rekisteröidyt tauot

Työntekijät voivat kirjata taukoja. Tauot voidaan määrittää joustavasti, kuten on kuvattu kohdassa [Rekisteröinteihin perustuva palkka](pay-based-on-registrations.md).

Työntekijä kirjaa tauon valitsemalla **Tauko**-vaihtoehdon ja valitsemalla sitten tauon tyyppiä vastaavan kortin (kuten lounaan). Kun työntekijä on vahvistanut valinnan, laitteeseen avautuu joko kirjautumissivu tai sivu, joka odottaa työntekijän vahvistavan tauolta palaamisen. Avautuva sivu määräytyy tuotannon käyttöliittymän määritysten mukaan. (Lisätietoja on kohdassa [Tuotannon käyttöliittymän määrittäminen](production-floor-execution-configure.md).)

## <a name="view-the-my-day-dialog"></a>Näytä Päivän tehtävät -valintaikkuna

**Päivän tehtävät** -valintaikkunassa on työntekijöille rekisteröintien ja saldojen yhteenveto. Valintaikkuna on jaettu seuraaviin kolmeen osaan:

- Pääosa sisältää nykyisen työntekijän valittuna päivänä tekemät rekisteröinnit. Se avautuu, ja siinä näkyvät kuluvan päivän rekisteröinnit. Siinä näkyy päivämäärän valitsin, jonka avulla työntekijä voi tarkastella muita päiviä.
- **Viimeisin laskettu päivän saldo** -osassa näkyvät työntekijän maksetun ajan, maksetun ylityöajan, poissaolon ja maksetun poissaolon saldot. Nämä arvot perustuvat rekisteröinteihin, jotka on laskettu hyväksyntäprosessin aikana.
- **Saldot**-osassa on yleiskatsaus saldoista määritetyllä kaudella valituille rekisteröintiluokille (kuten loma, vakioaika ja ylityö). Nämä saldot perustuvat siihen, miten tilastosaldot määritetään **Aika ja läsnäolo** -moduulissa. Lisätietoja tämän määrittämisestä on kohdassa [Näytä lomasaldot tuotannon käyttöliittymässä](production-floor-execution-payroll-stats.md).

Järjestelmänvalvojat voivat lisätä tämän ominaisuuden käyttöliittymäin asettamalla **Päivän tehtävät**-painikkeen kunkin asiaankuuluvan välilehden työkaluriviin, kuten on kuvattu kohdassa [Tuotannon käyttöliittymän suunnitteleminen](production-floor-execution-tabs.md).

## <a name="working-in-teams"></a>Työskentely ryhmissä

Kun samaan tuotantotyöhön on liitetty useita työntekijöitä, he voivat muodostaa ryhmän. Tiimi voi nimetä yhden työntekijän vetäjäksi. Jäljellä olevista työntekijöistä tulee tämän jälkeen automaattisesti tämän vetäjän avustajia. Tuloksena olevassa ryhmässä vain vetäjän on rekisteröitävä työn tila. Aikatietueita käytetään kaikille ryhmän jäsenille.

### <a name="prerequisites"></a>Edellytykset

Jotta ryhmiä voi käyttää, järjestelmänvalvojan on otettava **Avustaja**-toiminto käyttöön tuotannon käyttöliittymän **Kaikki työt** -välilehden ensisijaisessa työkalurivissä. Lisätietoja on kohdassa [Tuotannon käyttöliittymän suunnitteleminen](production-floor-execution-tabs.md).

### <a name="form-a-new-team-that-has-a-pilot-and-an-assistant"></a>Uuden ryhmän muodostaminen, jossa on vetäjä ja avustaja

Työntekijä voi rekisteröityä avustajaksi valitsemalla **Avustaja** **Kaikki työt** -välilehdestä. Tämän jälkeen työntekijä voi valita **Valitse avustettava työntekijä** -ikkunassa vetäjän työntekijöistä, jotka työskentelevät aktiivisesti työn parissa. Kun työntekijä on vahvistanut valintansa, hän muuttuu valitun työntekijän avustajaksi, josta tulee uuden ryhmän vetäjä.

### <a name="assign-a-new-pilot-to-an-existing-team"></a>Uuden vetäjän määrittäminen olemassa olevaan ryhmään

Kun ryhmä haluaa valita uuden vetäjän, nykyisen vetäjän on nimettävä toinen työntekijä ryhmän uudeksi vetäjäksi. Uuden vetäjän valitsemiseksi nykyinen vetäjä valitsee **Avustaja** **Kaikki työt** -välilehdestä. Tämän jälkeen näyttöön tulevassa **Vaihda vetäjää** -valintaikkunassa vetäjä voi valita uuden vetäjän ryhmään jo kuuluvien työntekijöiden luettelosta. Kun nykyinen vetäjä on vahvistanut valintansa, heidät poistetaan ryhmästä kokonaan. He voivat kuitenkin liittyä ryhmään uudelleen tarpeen mukaan.

### <a name="assistant-clocks-out"></a>Avustaja leimaa ulos

Kun avustajana työskentelevä työntekijä leimaa ulos, hän poistuu ryhmästä. Jos **Pysyvät ryhmät**- ja **Uudelleen aloitus saapumisen yhteydessä** -asetukset ovat *Kyllä*, työntekijä, joka leimaa ulos automaattisesti, tulee ryhmään uudelleen, kun hän leimaa seuraavan kerran sisään. Nämä vaihtoehdot ovat **Aika ja läsnäolo - parametrit** -sivun **Yleiset**-välilehdessä.

## <a name="opening-instructions"></a>Ohjeiden avaaminen

Työntekijät voivat avata työhön liitetyn asiakirjan valitsemalla **Ohjeet**. **Ohjeet**-painike on käytettävissä vain, jos asiakirja on liitetty työhän päätiedoissa. Työntekijät voivat avata tuotteeseen esimerkiksi Supply Chain Managementin **Vapautetut tuotteet** -sivulla liitetyn asiakirjan tuotannon käyttöliittymässä.

## <a name="opening-mixed-reality-guides-for-hololens"></a>HoloLensin yhdistetyn todellisuuden oppaiden avaaminen

[Dynamics 365 Guidesin](https://dynamics.microsoft.com/mixed-reality/guides/) avulla työntekijöille voidaan antaa yhdistettyä todellisuutta käyttävää käytännönläheistä opastusta. Voit määrittää standardoidut prosessit vaiheittaisilla ohjeilla, jotka opastavat työntekijöitä valitsemaan tarvittavat työkalut ja osat. Lisäksi nämä oppaat näyttävät, miten kyseisiä työkaluja käytetään todellisissa työtilanteissa. Prosessin yhteenveto:

1. Aina kun työntekijä avaa työluettelon tuotannon käyttöliittymässä, liittymä etsii kaikki näkyvissä olevia töitä koskevat oppaat.
1. Työntekijä voi tarkastella opasluetteloa valitsemalla **Oppaat**.
1. Työntekijä valitsee sopivan oppaan luettelosta.
1. Tuotannon käyttöliittymä näyttää valitun oppaan QR-koodin.
1. Työntekijä ottaa HoloLensin käyttöön ja käynnistää oppaan kohdistamalla katseen QR-koodiin.
1. Työntekijä opettelee tehtävän toimimalla oppaan mukaisesti.

Lisätietoja HoloLens-oppaiden luonnista, määrittämisestä ja käyttämisestä on kohdassa [Yhdistetyn todellisuuden oppaiden tuottaminen tuotannon työntekijöille](instruction-guides-in-production-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
