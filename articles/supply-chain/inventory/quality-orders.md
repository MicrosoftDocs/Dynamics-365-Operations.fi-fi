---
title: Laatutilaukset
description: Tässä aiheessa kuvataan, kuinka laatutilauksia luodaan manuaalisesti tai automaattisesti ja miten niitä käsitellään tarkastusten tekemiseksi ja testitulosten kirjaamiseksi Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d06cd7766f4445a248e0394e75ae390314762cf211a2780da76b4f52aa5bccd4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739799"
---
# <a name="quality-orders"></a>Laatutilaukset

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka laatutilauksia luodaan manuaalisesti tai automaattisesti ja miten niitä käsitellään tarkastusten tekemiseksi ja testitulosten kirjaamiseksi Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="automatically-created-quality-orders"></a>Automaattisesti luodut laatutilaukset

Voit konfiguroida järjestelmän niin, että se luo nimikeotantasääntöjen perusteella laatutilaukset automaattisesti. Lisätietoja on kohdassa [Laadunhallinnan nimikeotanta](quality-item-sampling.md).

## <a name="manually-create-quality-orders"></a><a name="manual-quality-orders"></a>Laatutilausten manuaalinen luonti

Voit luoda laatutilauksen manuaalisesti seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**.
1. Valitse **Uusi**.
1. Valitse **Laatutilaukset**-valintaikkunan **Viitetyyppi**-kentästä varastoviite, johon laatutilaus liittyy. Lisätietoja valittavissa olevista viitetyypeistä on jäljempänä tämän ohjeaihee [Laatutilauksen viitetyypit](#ref-types) -osassa.

    > [!NOTE]
    > Valittuun viitteeseen liittyvän varaston on oltava käytettävissä. Jos valittavan viitetyypin, määrän ja varastodimension yhdistelmälle ei ole käytettävissä varastoa, näyttöön tulee virhesanoma.

1. Noudata yhtä näistä vaiheita sen arvon mukaan, jonka valitsit **Viitetyyppi**-kentässä:

    - Jos valitsit **Varasto**, lisäviitetietoja ei tarvita.
    - Jos valitsit **Myynti** tai **Osto**, määritä seuraavat tiedot:

        - **Tilin valinta** – Viittaa asiakkaan tai toimittajan numeroon.
        - **Viitenumero** – Viittaa myyntitilauksen tai ostotilauksen numeroon.
        - **Viite-erä** – Viittaa tiettyyn myyntitilausriviin tai ostotilausriviin.

    - Jos valitsit **Tuotanto**, **Karanteeni** tai **Oheistuotteen tuotanto** **Viitenumero**-kentässä, viittaa tuotantotilauksen, erätilauksen tai karanteenitilauksen numeroon.
    - Jos valitsit **Reitityksen työvaihe**, määritä seuraavat tiedot:

        - **Viitenumero** – Viittaa tuotantotilauksen tai erätilauksen numeroon.
        - **Työvaihenro** – Viittaa tiettyyn reitityksen työvaiheen numeroon.
        - **Työvaihe** – Viittaa tiettyyn reitityksen työvaiheen numeroon.
        - **Resurssi** – Viittaa tiettyyn resurssiin, jota on käytettävä reitityksen työvaiheen kanssa.

1. Valitse **Testiryhmä**-kentässä suoritettava testiryhmä.
1. Kirjoita **Määrä**-kenttään testattavien nimikkeiden määrä.
1. Syötä **Varastodimensiot**-osaan kaikki muut valittua nimikettä varten tarvittavat varastodimensiot.
1. Valitse **OK**.

Laatutilauksen luomisen jälkeen voit alkaa tarkistaa varastoa ja kirjata testitulokset. Lisätietoja testitulosten kirjaamisesta ja tarkistamisesta on kohdassa [Tarkista tavaroiden laatu](tasks/inspect-quality-goods.md).

## <a name="quality-order-reference-types"></a><a name="ref-types"></a>Laatutilauksen viitetyypit

Laatutilausten avulla seurataan tietoja oman varaston erityisvaraston tarkastuksista ja testituloksista. Laatutilauksen on sisällettävä viite, joka edustaa testattavan varaston lähdettä. Laatutilaukset voivat liittyä seuraaviin viitetyyppeihin:

- **Varasto** – Tämä viitetyyppi ilmaisee, että olet tarkistamassa käytettävissä olevan varaston. Tämän tyyppiset tarkastukset ovat yleensä satunnaisia tai suunnittelemattomia, ja ne tehdään, kun varastotyöntekijä havaitsee ongelman.
- **Myynti** – Tämä viitetyyppi ilmaisee, että tarkastetaan tiettyyn myyntitilaukseen liittyvää varastoa. Tämän tyyppiset tarkastukset koskevat yleensä asiakkaan määrityksiä tai analyysitodistuksen (CoA) luontia, joka on toimitettava asiakkaalle lähetyksen osana. (CoA:ta kutsutaan joskus myös yhteensopivuustodistukseksi \[CoC\].)
- **Osto** – Tämä viitetyyppi ilmaisee, että tarkastetaan tiettyyn ostotilaukseen liittyvää varastoa. Tämäntyyppisiä tarkastusmenetelmiä käytetään usein saapuvien tuotteiden tarkistamiseen, ennen kuin ne otetaan varastoon tai kulutetaan tuotantoprosesseissa.
- **Tuontanto** – Tämä viitetyyppi ilmaisee, että tarkastetaan tiettyyn tuotantotilaukseen liittyvää varastoa. Tämäntyyppisiä tarkastusmenetelmiä käytetään usein valmiiden tuotteiden tarkistamiseen, ennen kuin ne otetaan varastoon.
- **Karanteeni** – Tämä viitetyyppi ilmaisee, että tarkastetaan tiettyyn karanteenitilaukseen liittyvää varastoa. Karanteenitilaukset ovat erityistilauksia, joissa seurataan varastoa jaetussa varastossa tai varaston jaetulla alueella. Tämäntyyppisiä tarkastuksia käytetään usein asiakkaan palauttamien tai karanteeniin lisäanalyysiä varten asetettujen tuotteiden tarkistamiseen. Karanteenitilauksia voidaan luoda laatutilauksista. Vaihtoehtoisesti ne voidaan luoda muista lähteistä, ja sitten laatutilaukset voidaan määrittää karanteenitilauksiin.
- **Reitityksen työvaihe** – Tämä viitetyyppi ilmaisee, että tarkastetaan tiettyyn tuotantotilauksen reitityksen tiettyyn vaiheeseen liittyvää varastoa. Tämän tyyppisiä tarkastuksia käytetään yleensä tuotteen keskeneräisen työn (KET) analysointiin, ennen kuin se siirtyy tuotantoprosessin seuraavaan vaiheeseen.
- **Oheistuotteen tuotanto** – Tämä viitetyyppi ilmaisee, että tarkastetaan tietyn tuotantotilauksen oheistuotteeseen liittyvää varastoa. Tämän tyyppisiä tarkastuksia käytetään yleensä erätilauksen osatuotteen tarkistamiseen ennen kuin oheistuote lisätään varastoon.

## <a name="view-and-create-quality-orders-from-various-parts-of-the-system"></a>Laatutilausten tarkasteleminen ja luominen järjestelmän eri osista

Laatutilaukset voidaan luoda manuaalisesti. Vaihtoehtoisesti ne voidaan luoda automaattisesti määritettyjen laatuliitosten perusteella. Lisätietoja laatutilausten automaattisen luonnin luomisesta ja hallitsemisesta on kohdassa [Laatuliitokset](quality-associations.md).

Laatutilaussivun avulla voit luoda uuden laatutilauksen manuaalisesti tai tarkastella toiseen tietueeseen liittyvän laatutilauksen tilaa. Laatutilaussivua voi käyttää monella tavalla.

### <a name="from-the-quality-orders-page"></a>Laatutilaukset-sivulta

Jos haluat luoda laatutilauksen manuaalisesti ja tarkastella kaikkia luotuja laatutilauksia, siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**. Tämän ohjeaiheen muut osat antavat lisätietoja **Laatutilaukset**-sivun käyttämisestä.

### <a name="from-sales-orders"></a>Myyntitilauksista

Voit käyttää myyntitilauksiin liittyviä laatutilauksia valitsemalla **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset** ja noudattamalla sitten jotakin seuraavista vaiheista:

- Avaa myyntitilaus tai valitse se ruudukossa. Sitten toimintoruudun **Kerää ja pakkaa** -välilehdessä **Laadunhallinta**-ryhmässä valitse **Laatutilaukset** avataksesi **Laatutilaukset**-sivun. Siinä voit tarkastella, luoda ja päivittää myyntitilaukseen liittyviä laatutilauksia.
- Avaa myyntitilaus ja valitse sitten **Otsikko**-välilehdestä **Yleinen**-pikavälilehti. **Laatutilauksen tila** -kentässä näkyy kaikkien myyntitilaukseen liittyvien laatutilausten yleinen tila.
- Avaa myyntitilaus ja valitse sitten **Rivit**-välilehdestä **Myyntitilausrivit**-pikavälilehti. **Laatutilauksen tila** -sarakkeessa näkyy myyntitilauksen kunkin rivin tila.

### <a name="from-purchase-orders"></a>Ostotilauksista

Voit käyttää ostotilauksiin liittyviä laatutilauksia valitsemalla **Hankkiminen ja hankinta \> Ostotilaukset \> Kaikki ostotilaukset** ja noudattamalla sitten jotakin seuraavista vaiheista:

- Avaa ostotilaus tai valitse se ruudukossa. Sitten toimintoruudun **Vastaanota**-välilehdessä **Laadunhallinta**-ryhmässä valitse **Laatutilaukset** avataksesi **Laatutilaukset**-sivun. Siinä voit tarkastella, luoda ja päivittää ostotilaukseen liittyviä laatutilauksia.
- Avaa ostotilaus ja valitse sitten **Otsikko**-välilehdestä **Yleinen**-pikavälilehti. **Laatutilauksen tila** -kentässä näkyy kaikkien ostotilaukseen liittyvien laatutilausten yleinen tila.
- Avaa ostotilaus ja valitse sitten **Rivit**-välilehdestä **Ostotilausrivit**-pikavälilehti. **Laatutilauksen tila** -sarakkeessa näkyy ostotilauksen kunkin rivin tila.

### <a name="from-production-orders"></a>Tuotantotilauksista

Voit käyttää tuotantotilauksiin liittyviä laatutilauksia valitsemalla **Tuotannonhallinta \> Tuotantotilaukset \> Kaikki tuotantotilaukset** ja noudattamalla sitten jotakin seuraavista vaiheista:

- Avaa tuotantotilaus tai valitse se ruudukossa. Sitten toimintoruudun **Näytä**-välilehdessä **Laadunhallinta**-ryhmässä valitse **Laatutilaukset** avataksesi **Laatutilaukset**-sivun. Siinä voit tarkastella, luoda ja päivittää tuotantotilaukseen liittyviä laatutilauksia.
- Avaa tuotantotilaus tai valitse se ruudukossa. Sitten toimintoruudun **Tuotantotilaus**-välilehden **Tuotantotiedot**-ryhmässä valitse **Reitytys** avataksesi **Tuotantoreititys**-sivun. Voit tarkastella reitityksen työvaiheisiin liittyviä laatutilauksia seuraavasti:

    - Valitse ruudukosta kohteena oleva reitityksen työvaihe. Valitse sitten toimintoruudussa **Kyselyt \> Laatutilaukset**.
    - Valitse arvo kohdassa **Työvaiheen nro** kenttä kohteena olevan reitityksen työvaiheelle avataksesi **Tuotantoreititys**-tietosivun. **Yleinen**-pikavälilehden **Laatutilauksen tila** -kentässä näkyy reitityksen työvaiheisiin liittyvien laatutilausten tila.

- Avaa tuotantotilaus ja valitse **Yleinen**-pikavälilehti. **Laatutilauksen tila** -kentässä näkyy kaikkien tuotantotilaukseen liittyvien laatutilausten tila.

### <a name="from-quarantine-orders"></a>Karanteenitilauksista

Voit käyttää karanteenitilauksiin liittyviä laatutilauksia valitsemalla **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Karanteenitilaukset** ja noudattamalla sitten jotakin seuraavista vaiheista:

- Tarkasta arvoja **Laatutilauksen tila** -sarakkeessa. Näin saat tietää kaikkien ruudukon kuhunkin karanteenitilaukseen liittyvien laatutilausten yleisen tilan.
- Valitse karanteenitilaus ruudukosta ja valitse sitten toimintoruudusta **Laatutilaukset**, jos haluat tarkastella, luoda tai päivittää karanteenitilaukseen liittyviä laatutilauksia.

## <a name="advanced-actions-for-quality-orders"></a>Laatutilausten lisätoiminnot

Voit hallita tilaa, luoda tiedostoja ja tehdä lisäkyselyjä laatutilauksissa useilla toimenpiteillä.

### <a name="reopen-a-quality-order"></a>Avaa laatutilaus uudelleen

Oletusarvon mukaan laatutilausta ei voi enää muokata tai päivittää sen jälkeen, kun se on vahvistettu ja testit on läpäisty. Joissain tapauksissa laatutilaus on kuitenkin ehkä avattava uudelleen sen valmistumisen jälkeen.

Voit avata laatutilauksen uudelleen seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**.
1. Avaa vahvistettu laatutilaus tai valitse se ruudukossa.
1. Valitse toimintoruudussa **Avaa laatutilaus uudelleen**.

### <a name="create-a-certificate-of-analysis-for-a-quality-order"></a>Analyysitodistuksen luominen laatutilausta varten

Analyysitodistus (CoA) on organisaation laadunvarmistusryhmän luoma raportti. Se tarkistaa, että tuote täyttää tietyt säädökset tai vaatimukset. Asiakkaasi tai geopoliittisen sijaintisi sääntelyviranomaiset saattavat edellyttää analyysitodistuksia. Ne voivat olla myös pakollisia toimialasi sekä sellaisten tuotteiden mukaan, joita käsittelet, ostat, tuotat tai myyt.

Supply Chain Managementin avulla voit luoda analyysitodistuksen laatutilauksesta. Raportti sisältää laatutilauksen testien tulokset, jos **Analyysitodistusraportti**-asetuksena on *Kyllä*. Tämän vaihtoehdon voi määrittää oletusarvon mukaan **Testit**-sivulla määritettävän testin perusteella. Tietyille laatutilauksille tehtyjen tiettyjen testien asetus voidaan kuitenkin ohittaa.

Voit luoda analyysitodistuksen laatutilaukselle manuaalisesti seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**.
1. Valitse laatutilaus, jota varten haluat luoda analyysitodistuksen.
1. Valitse toimintoruudussa **Kyselyt \> Analyysitodistus**.
1. Valitse **Analyysitodistus**-sivulla toimintoruudussa **Uusi**.
1. Valinnainen: Valitse **Yhteyshenkilö**-kentästä yhteyshenkilö, jolle todistus osoitetaan.
1. Valitse toimintoruudussa **Tulosta**.
1. Määritä **Analyysitodistus**-valintaikkunassa raportin tulostustapa. Tulosta sitten raportti tulostimelle, näyttöön, tiedostoon tai sähköpostiin valitsemalla **OK**.
1. Sulje sivut.

### <a name="block-or-unblock-inventory-for-a-quality-order"></a>Laatutilauksen varaston eston estäminen tai eston poistaminen

Kun laatutilaus luodaan automaattisesti laatuliitoksesta, laatuliitokseen liitetty nimikeotanta voidaan konfiguroida niin, että se estää testattavan viitteen koko varastomäärän. Lisätietoja nimikenäytteistä on kohdassa [Laadunhallinnan nimikeotanta](quality-item-sampling.md).

Jos et käytä täyttä estoa tai jos luot laatutilauksen manuaalisesti, järjestelmä luo automaattisesti varastoestotietueen laatutilauksessa testattavalle nimikkeen määrälle. **Varastoesto**-sivulla luodussa tietueessa **Varastoeston tyyppi** -kentän arvona on *Laatutilaus*.

Voit tarkastella ja muokata **Varastoesto**-sivulla valitun laatutilauksen varastoestoa valitsemalla toimintoruudusta **Kyselyt \>Varastoesto**. Lisätietoja on kohdassa [Varastoesto](inventory-blocking.md).

### <a name="inquire-about-the-details-of-a-quality-order"></a>Kyselyjä laatutilauksen yksityiskohdista

Voit tarkastella lisätietoja laatutilauksesta tai siihen liittyen **Laatutilaukset**-sivun toimintoruudun seuraavien painikkeiden avulla:

- **Kyselyt \> Työn tiedot** – Avaa sivu, jolla voit tarkastella laatutilaukseen liittyvää varastotyötä.
- **Kyselyt \> Määrityksistä poikkeamiset** – Avaa sivu, jolla voit tarkastella laatutilaukseen liittyviä määrityksistä poikkeamisia.
- **Varasto** – Tämän valikon komennot ovat yleisiä kaikissa varastotapahtumissa. Niiden avulla voit tarkastella tai päivittää esimerkiksi tapahtumia, käytettävissä olevaa varastoa, varauksia ja merkintää.

### <a name="create-cases-related-to-quality-orders"></a>Laatutilauksiin liittyvien tapausten luominen

Voit luoda laatutilauksiin liittyviä tapauksia. Näin voit seurata ongelmatietoja ja etsiä ratkaisua. Tämän jälkeen voit käyttää tapausten hallinnan työnkulkuominaisuuksia, kun haluat reitittää tapauksen ennalta määritetyn liiketoimintaprosessin kautta. Tällöin saat lisähyväksyntää tai lisätietoja tietystä ongelmasta. Tietoartikkelit-ominaisuuden avulla voit myös luoda ratkaisujen tietokannan yleisiä ongelmia varten.

## <a name="case-management-examples-for-quality-management"></a>Tapaustenhallinnan esimerkkejä laadunhallinnalle

### <a name="example-1"></a>Esimerkki 1

Työskentelet valmistusyrityksessä, jonka on noudatettava tiukkaa lainsäädäntöä, joka liittyy säänneltyjen tuotteiden, kuten ruoan, tuotantoon. Laatutilauksia käytetään nimikkeiden laadun tietojen kirjaamiseen ja seuraamiseen tuotantoprosessin aikana. Jos laatutilaus epäonnistuu tietyissä testeissä, laitteistossa voi olla ongelma. Tapausten avulla seurataan liiketoimintaprosessia ja eskaloidaan ongelma oikeille insinöörille, jotta juurisyy voidaan määrittää. Jotta liiketoimintaprosesseja olisi helpompi seurata, yritys pitää tietokantaa yleisistä laatutilauksiin ja laitteisiin liittyvistä ongelmista.

### <a name="example-2"></a>Esimerkki 2

Työskentelet jakeluyrityksessä, joka toimittaa tuotteita, joita voidaan mukauttaa eri maiden ja alueiden mukaan. Joillakin asiakkailla on tiukat vaatimukset, joita on noudatettava. Muutoin maksuja ja palautuksia tai takaisinveloituksia voi aiheutua. Laatutilausten avulla voit seurata tietoja kustakin asiakkaan vaatimuksia vastaavasta testistä ja tuloksista. Tapausten avulla tarkistetaan ja hyväksytään analyysitodistuksen tiedot, ennen kuin asiakirja luodaan ja liitetään yhteen muiden lähetyspaperien kanssa.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallintaprosessit](quality-management-processes.md)
- [Laatutesti](quality-tests.md)
- [Laatutestiryhmät](quality-test-groups.md)
- [Laatuliitokset](quality-associations.md)
- [Laadunhallintaprosessit](quality-management-processes.md)
- [Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](enable-quality-management.md)
- [Laadunhallinta varastoprosesseja varten](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
