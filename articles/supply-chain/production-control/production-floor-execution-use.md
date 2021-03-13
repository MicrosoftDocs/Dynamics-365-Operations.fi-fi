---
title: Tuotannon käyttöliittymän käytön ohjeet työntekijöille
description: Tässä ohjeaiheessa käsitellään tuotannon käyttöliittymää työntekijän näkökulmasta.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4b89e911f3c6eb8ffa0cfe049ef9bfc2ed306021
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077628"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Tuotannon käyttöliittymän käytön ohjeet työntekijöille

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tuotannon käyttöliittymä on optimoitu kosketuskäyttöön. Siihen suunniteltu visuaalinen kontrasti vastaa tuotantoympäristön helppokäyttöisyysvaatimuksia. Siinä on kaikki samat toiminnalliset ominaisuudet kuin työkorttilaitteessa. Siinä voidaan kuitenkin aloittaa myös rinnakkain useita töitä työluettelosta. (Tätä ominaisuutta kutsutaan myös *töiden niputukseksi*.) Työntekijät voivat avata työluettelosta myös Microsoft Dynamics 365 Guidesissa luodun oppaan. He saavat tällä tavoin visuaalisia ohjeita HoloLensissa.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Kirjautuminen tuotannon käyttöliittymään työntekijänä

Ennen kuin työntekijät voivat aloittaa laitteen käytön, työnjohtajan tai teknisen henkilökunnan on valmisteltava se ja avattava oikea sivu Dynamics 365 Supply Chain Managementissa. Lisätietoja laitteen määrittämisestä on kohdassa [Laitteen määrittäminen käyttämään tuotannon käyttöliittymää](production-floor-execution-setup.md).

Kun laite on valmisteltu, kirjautumissivu avautuu. Tällä sivulla on tietoja paikallisen työsolun töiden tilasta. Nämä tiedot päivitetään säännöllisesti. Työntekijät kirjautuvat sivulla käyttämällä nimilappunsa tunnusta. Vaikka työntekijöillä ei tarvitse olla Supply Chain Managementin käyttäjätiliä, heillä on oltava *aikarekisteröidyn työntekijän* tili, jolla he kirjautuvat sisään.

![Tuotannon käyttöliittymän kirjautumissivu](media/pfei-sign-in-page.png "Tuotannon käyttöliittymän kirjautumissivu")

Tämän ohjeaiheen muissa osissa käsitellään tapoja, joilla työntekijät käyttävät liittymää.

## <a name="all-jobs-tab"></a>Kaikki työt -välilehti

**Kaikki työt** -välilehdessä on työluettelo. Tässä luettelossa on kaikki ne tuotantotyöt, joiden tila on *Ei aloitettu*, *Pysäytetty* tai *Aloitettu*. (Tätä välilehden nimiä voi mukauttaa, joten sillä voi olla eri nimi omassa järjestelmässä.)

![Kaikki työt -välilehti](media/pfei-all-jobs-tab.png "Kaikki työt -välilehti")

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

![Aktiiviset työt -välilehti](media/pfei-active-jobs-tab.png "Aktiiviset työt -välilehti")

Aktiivisten töiden luettelossa on seuraavat sarakkeet:

- **Valintasarake** – Vasemmassa sarakkeessa käytetään valintamerkkejä ilmaisemaan työt, jotka työntekijä on valinnut. Työntekijät voivat valita luettelossa useita töitä samanaikaisesti. Kaikki työt voidaan valita valitsemalla valintamerkki sarakkeen otsikossa. Jos töitä valitaan yksi, kyseisen työn tiedot näytetään sivun alareunassa.
- **Tilaus** – tämä sarake näyttää työn tuotantotilauksen numeron.
- **Kuvaus** – tämä sarake näyttää sen toiminnon kuvauksen, jonka osa työ on.
- **Pyydetty** – tämä sarake näyttää määrän, joka työn on tarkoitus valmistaa.
- **Aloitettu** – tämä sarake näyttää määrän, joka on työlle jo aloitettu.
- **Valmis** – tämä sarake näyttää määrän, joka työstä on jo valmistunut.
- **Hävikki** – tämä sarake näyttää määrän, joka on työstä jo hävikkiä.
- **Jäljellä** – tämä sarake näyttää määrän, joka työstä on vielä valmistumatta.

## <a name="my-machine-tab"></a>Oma kone -välilehti

**Oma kone** -välilehdessä työntekijät voivat valita resurssin, joka on liitetty koneresurssiin **Kaikki työt** -välilehdessä määritetyssä suodattimessa. Työntekijät voi sitten tarkastella valitun resurssin tilaa ja kuntoa lukemalla enintään neljän valitun laskurin arvot sekä viimeaikaisten ylläpitopyyntöjen ja rekisteröityjen seisokkien luetteloita. Työntekijät voi myös pyytää valitun resurssin ylläpitoa sekä rekisteröidä ja muokata koneen seisokkeja. (Tätä välilehden nimiä voi mukauttaa, joten sillä voi olla eri nimi omassa järjestelmässä.)
 
![Oma kone -välilehti](media/pfei-my-machine-tab.png "Oma kone -välilehti")

**Oma kone** -välilehdessä on seuraavat sarakkeet. Numerot vastaavat edellisessä kuvassa käytettyjä numeroita.

1. **Koneresurssi** – Valitse seurattava koneresurssi. Aloita nimen kirjoittaminen ja tee valinta kirjoitusta vastaavien resurssien luettelosta. Vaihtoehtoisesti voit valita suurennuslasikuvakkeen ja tehdä valinnan luettelossa, jossa on kaikki työluettelon suodattimessa oleviin resursseihin liitetyt resurssit.

    > [!NOTE]
    > Supply Chain Managementin käyttäjät voivat määrittää tarpeen mukaan kullekin resurssille resurssin **Kaikki resurssit** -sivulla (**Käyttöomaisuus**-välilehden avattavassa **Resurssi**-luettelossa). Lisätietoja on kohdassa [Resurssin luominen](../asset-management/objects/create-an-object.md).

1. **Asetukset** – Valitse rataskuvake ja avaa valintaikkuna, jossa voidaan valita, mitä valitun koneresurssin laskureita tarkastellaan. Näiden laskureiden arvot näytetään **Resurssien hallinta** -välilehden yläosassa. (Seuraavassa näyttökuvassa olevassa) **Asetukset**-valikossa voi ottaa käyttöön enintään neljä laskuria. Valitse kukin käyttöönotettava laskuri käyttämällä ruudun yläosassa olevaa hakukenttää. Hakukentässä on luettelo kaikista valittuun resurssiin liitetyistä laskurista. Resurssi valittiin **Resurssien hallinta** -sivun yläosassa. Määritä kukin laskuri seuraamaan joko **Koottu**-arvoa ja laskurin uusinta **Toteutunut**-arvoa. Jos määritetty laskuri esimerkiksi seuraa, kuinka monta tuntia kone on ollut käytössä, määrityksenä on oltava **Koottu**. Jos laskuri määritetään seuraamaan viimeksi päivitettyä lämpötilaa tai painetta, määrityksenä on oltava **Toteutunut**. Valitse **OK** tallentaaksesi asetukset ja sulje valintaikkuna.

    ![Oma kone -välilehti](media/pfei-my-machine-tab-settings.png "Oma kone -välilehti")

1. **Yläpitopyyntö** – Tämän painikkeen valinta avaa valintaikkunan, jossa voidaan luoda ylläpitopyyntö. Pyynnölle voi antaa kuvauksen ja lisätä huomautuksen. Pyyntö tulee Supply Chain Management -käyttäjän näkyville, ja tämä käyttäjä voi sitten muuntaa ylläpitopyynnön ylläpidon työtilaukseksi.
1. **Rekisteröi seisokki** – Tämän painikkeen valinta avaa valintaikkunan, jossa voi rekisteröidä koneen seisokin. Seisokille voidaan valita syykoodi ja antaa seisokin ajankohta ja kesto. Koneen seisokkirekisteröinnin avulla lasketaan koneresurssin tehokkuus.
1. **Näytä tai muokkaa** – tämän painikkeen valinta avaa valintaikkunan, jossa voi muokata tai tarkastella aiemmin luotuja seisokkitietueita.


## <a name="starting-and-completing-production-jobs"></a>Tuotantotöiden aloittaminen ja valmistuminen

Työntekijä aloittaa tuotantotyön valitsemalla työn **Kaikki työt** -välilehdessä ja avaamalla **Aloita työ** -valintaikkunan sitten valitsemalla **Aloita työ**.

![Aloita työ -valintaikkuna](media/pfei-start-job-dialog.png "Aloita työ -valintaikkuna")

Työntekijät vahvistavat **Aloita työ** -valintaikkunassa tuotannon määrän ja aloittavat sitten työn. Työntekijät voivat säätää määrää valitsemalla **Määrä**-kentän ja käyttämällä avautuvaa numeronäppäimistöä. Työntekijät aloittavat sitten työn tekemisen valitsemalla **Aloita**. **Aloita työ** -valintaikkuna suljetaan ja työ lisätään **Aktiiviset työt** -välilehteen.

Työntekijät voivat aloittaa työn riippumatta siitä, mikä sen tila on. Jos työntekijä aloittaa työn, jonka tila on *Ei aloitettu*, **Aloita työ** -valintaikkunan **Määrä**-kentässä on aluksi koko määrä. Jos työntekijä aloittaa työn, jonka tila on *Aloitettu* tai *Pysäytetty*, **Määrä**-kentässä on aluksi jäljellä oleva määrä.

## <a name="reporting-good-quantities"></a>Hyväksyttyjen määrän ilmoittaminen

Kun työntekijä tekee työn kokonaan tai osittain valmiiksi, hän voi raportoida tuotetut hyväksyttävät määrät valitsemalla työn **Aktiiviset työt** -välilehden ja valitsemalla sitten **Raportointi on meneillään**. Tämän jälkeen työntekijä antaa **Raportointi on meneillään** -valintaikkunassa hyväksyttyjen määrän numeronäppäimistössä. Määrä on oletusarvoisesti tyhjä. Työntekijä voi määrän antamisen jälkeen päivittää työn tilaksi *Käsittelyssä*, *Pysäytetty* tai *Valmis*.

![Raportointi on meneillään -valintaikkuna](media/pfei-report-progress-dialog.png "Raportointi on meneillään -valintaikkuna")

## <a name="reporting-scrap"></a>Hävikin raportointi

Kun työntekijä tekee työn kokonaan tai osittain valmiiksi, hän voi raportoida hävikin valitsemalla työn **Aktiiviset työt** -välilehden ja valitsemalla sitten **Hävikin raportointi**. Tämän jälkeen työntekijä antaa **Hävikin raportointi** -valintaikkunassa hävikin määrän numeronäppäimistöllä. Työntekijä valitsee myös syyn (*Ei yhtään*, *Kone*, *Käyttäjä* tai *Materiaali*).

![Hävikin raportointi -valintaikkuna](media/pfei-report-scrap-dialog.png "Hävikin raportointi -valintaikkuna")

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

Epäsuorat tehtävät ovat tehtäviä, jotka eivät liity suoraan tuotantotilaukseen. Epäsuorat tehtävät voidaan määrittää joustavasti, mistä on lisätietoja kohdassa [Työajan seurannan epäsuorien tehtävien määrittäminen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

Shannon, joka on Contoson tuotannon työntekijä, haluaa esimerkiksi osallistua yrityksen kokoukseen, ja kokouksia pidetään epäsuorina tehtävinä. Jompikumpi seuraavista skenaarioista on käytössä:

- **Shannon tekee vähintään yhtä aktiivista työtä.** Shannon valitsee **Tehtävä**-kohdan, määrittää tehtävän (kokous) ja vahvistaa valinnan. Avautuva sanoma ilmoittaa, että hänellä on keskeneräisiä töitä. Shannon voi valita sanomassa tekemiensä töiden päättämisen tai pysäyttämisen ennen kokoukseen lähtemistä.
- **Shannonilla ei ole aktiivisia töitä.** Shannon valitsee **Tehtävä**-kohdan, määrittää tehtävän (kokous) ja vahvistaa valinnan. Hänet on kirjattu kokouksessa olevaksi.

Kun Shannon on vahvistanut valintansa kummassakin skenaariossa, hän siirtyy joko kirjautumissivulle tai sivulle, joka odottaa hänen vahvistavan paluun epäsuorasta tehtävästä. Avautuva sivu määräytyy tuotannon käyttöliittymän määritysten mukaan. (Lisätietoja on kohdassa [Tuotannon käyttöliittymän määrittäminen](production-floor-execution-configure.md).)

## <a name="registering-breaks"></a>Rekisteröidyt tauot

Työntekijät voivat kirjata taukoja. Tauot voidaan määrittää joustavasti, kuten on kuvattu kohdassa [Rekisteröinteihin perustuva palkka](pay-based-on-registrations.md).

Työntekijä kirjaa tauon valitsemalla **Tauko**-vaihtoehdon ja valitsemalla sitten tauon tyyppiä vastaavan kortin (kuten lounaan). Kun työntekijä on vahvistanut valinnan, laitteeseen avautuu joko kirjautumissivu tai sivu, joka odottaa työntekijän vahvistavan tauolta palaamisen. Avautuva sivu määräytyy tuotannon käyttöliittymän määritysten mukaan. (Lisätietoja on kohdassa [Tuotannon käyttöliittymän määrittäminen](production-floor-execution-configure.md).)

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
