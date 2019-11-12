---
title: Liiketoiminta-asiakirjojen hallinta – yleiskatsaus
description: Tässä ohjeaiheessa on tietoja ER-kehyksen liiketoiminnan asiakirjojen hallintatoiminnon käyttämisestä.
author: NickSelin
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 05dee1efc4e817795824e3fa1c41093d48a97d78
ms.sourcegitcommit: 219a73371638a9a4c6076d4c88b95fb2ebe95b00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/23/2019
ms.locfileid: "2652614"
---
# <a name="business-document-management-overview"></a>Liiketoiminta-asiakirjojen hallinta – yleiskatsaus

Yrityskäyttäjät käyttävät [sähköisen raportoinnin (ER) kehystä](general-electronic-reporting.md) määrittääkseen lähtevien sähköisten asiakirjojen muodot eri maiden ja alueiden lakisääteisten vaatimusten mukaisiksi. Käyttäjät voivat myös määrittää tietovirran määrittääkseen, mitkä sovellustiedot sijoitetaan luotuihin tiedostoihin. ER-kehys luo lähteviä tiedostoja Microsoft Office -muodoissa (Excel-työkirjoissa tai Word-asiakirjoissa) ennalta määritettyjen mallien avulla. Mallit täytetään tarvittavilla tiedoilla määritetyn tietovirran mukaisesti, kun vaadittavat tiedostot luodaan. Kukin konfiguroitu muoto voidaan julkaista osana ER-ratkaisua tiettyjen lähtevien tiedostojen luomista varten. Tätä kuvaa ER-muotoonfiguraatio, joka voi sisältää malleja, joiden avulla voit luoda erilaisia lähteviä asiakirjoja. Yrityskäyttäjät voivat hallita tarvittavia liikeasiakirjoja tämän kehyksen avulla.

**Liiketoiminta-asiakirjojen hallinta** perustuu ER-kehykseen, ja sen avulla yrityskäyttäjät voivat muokata liiketoiminta-asiakirjamalleja Microsoft Office 365 -palvelun tai asianmukaisen Microsoft Office -työpöytäsovelluksen avulla. Asiakirjoihin tehdyt muokkaukset voivat olla liiketoiminnan asiakirjamallien muuttamista ja lisätietojen paikkamerkkien lisäämistä ilman lähdekoodin muutoksia ja uusia käyttöönottoja. Yritysasiakirjojen mallien päivittämiseksi ei tarvita tietoja ER-kehyksestä.

> [!NOTE]
> Huomaa, että yritystiedostojen hallinnan avulla voit muokata malleja, joita käytetään liiketoiminnan asiakirjojen, kuten tilausten, laskujen jne. tuottamiseen. Kun mallia on muokattu ja sen uusi versio on julkaistu, tätä versiota käytetään tarvittavien liikeasiakirjojen luomiseen. Yritysasiakirjan hallintaa ei voi käyttää aiemmin luotujen liikeasiakirjojen muokkaamiseen.

## <a name="supported-deployments"></a>Tuetut käyttöönotot

Tällä hetkellä yritysasiakirjan hallintatoiminto on käytössä vain pilvikäyttöönotoissa. Jos tämä toiminto on kriittinen paikallisen käyttöönoton kannalta, kerro siitä meille antamalla palautetta [Ideat](https://experience.dynamics.com/ideas/)-sivustossa.

## <a name="supported-microsoft-office-applications"></a>Tuetut Microsoft Office -sovellukset

Yritystiedostojen hallinnan käyttäminen mallien muokkaamiseen Excel- tai Word-muodoissa Microsoft Office -työpöytäsovellusten avulla edellyttää, että asennettuna on Microsoft Office 2010 tai uudempi. Tätä tuetaan sekä pilvi- että paikallisissa käyttöönotoissa.

## <a name="business-document-availability"></a>Yritysasiakirjojen käytettävyys

Seuraavat Excel-pohjaisten mallien raportit ovat käytettävissä julkisen esikatselun julkaisemisen yhteydessä:

**Myyntireskontra** (elokuu 2019)

- Myynnin ennakkomaksun lasku
- Myyntitilauksen pakkausluettelo

**Ostoreskontra** (elokuu 2019)

- Oston ennakkomaksun lasku
- Ostotilaus
- Ostotilauksen pakkausluettelo

Lisää raportteja tulee saataville. Lisäraporttien erityisilmoitukset lähetetään erikseen. 

Täydellinen luettelo kaikista suunnitelluista raporteista lokakuun 2019 julkaisussa löytyy kohdasta [Määritettävien liikeasiakirjaraportointi Wordissa ja Excelissä](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).

# <a name="example-enable-configure-and-use-business-document-management"></a>Esimerkki: yritysasiakirjan hallinnan ottaminen käyttöön, määrittäminen ja käyttäminen

Saat lisätietoja tästä toiminnosta suorittamalla tämän ohjeaiheen seuraavan esimerkin.

## <a name="configure-er-parameters"></a>Konfiguroi ER-parametrit

Koska yritysasiakirjan hallinta perustuu ER-kehykseen, on määritettävä ER-parametrit, jotta yritystiedostojen hallinta voidaan aloittaa. Jotta voisit tehdä tämän, sinun on määritettävä ER-parametrit kohdassa [Määritä ER-kehys](electronic-reporting-er-configure-parameters.md) kuvatulla tavalla. Lisää myös uusi konfigurointipalvelu, joka on kuvattu kohdassa [Luo konfigurointipalvelut ja merkitse ne aktiivisiksi](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![ER-työtila](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>Tuo ER-ratkaisut

Sinun on tuotava yritysasiakirjojen malleja sisältäviä ER-konfiguraatioita nykyiseen esiintymään. Suorita nämä toimet lataamalla ja ja tallentamalla paikallisesti seuraavat tiedostot.

**Esimerkki ER-asiakaslaskutusratkaisusta**

| **Tiedosto**                                  | **Sisältö**                                |
|-------------------------------------------|--------------------------------------------|
| Customer invoicing model.version.2.xml    | [ER-tietomallin konfigurointi](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Customer FTI report (GER).version.2.3.xml | [Vapaatekstilaskun ER-muodon määritys](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Esimerkki ER-maksutarkastusratkaisusta**

| **Tiedosto**                                  | **Sisältö**                                |
|-------------------------------------------|--------------------------------------------|
| Model for cheques.version.10.xml          | [ER-tietomallin konfigurointi](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Cheques printing format.version.10.9.xml  | [Maksusekin ER-muodon konfigurointi](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Esimerkki ER-ulkomaankaupparatkaisusta**

| **Tiedosto**                                  | **Sisältö**                                |
|-------------------------------------------|--------------------------------------------|
| Intrastat model.version.1.xml             | [ER-tietomallin konfigurointi](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Intrastat report.version.1.9.xml          | [Intrastat-valvontaraportin ER-muodon konfigurointi](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Tuo kukin tiedosto noudattamalla seuraavia ohjeita. Tuo kunkin ER-ratkaisun ER-*tietomallin* konfiguraatio yllä oleviin tauluihin ennen kuin tuot vastaavan ER *-muodon* konfiguraation.

1. Avaa **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot** -sivu.
2. Valitse sivun yläosassa **Vaihda**.
3. Valitse **Lataa XML-tiedostosta**.
4. Lataa tarvittava XML-tiedosto valitsemalla **Selaa**.
5. Vahvista konfiguroinnin tuonti valitsemalla **OK**.

![Sähköisen raportoinnin konfiguroinnit -sivu](./media/BDM-Overview-ERSolutions.png)

Lisätietoja ER-määritysten tuomisesta on kohdassa [ER-konfiguraation elinkaaren hallinta](general-electronic-reporting-manage-configuration-lifecycle.md).

## <a name="enable-business-document-management"></a>Ota liiketoiminta-asiakirjojen hallinta käyttöön

Jos haluat käynnistää yritystiedostojen hallinnan, sinun on avattava **Ominaisuuksien hallinta** -työtila ja otettava käyttöön **Liiketoiminta-asiakirjojen hallinta** -ominaisuus.

Seuraavia ohjeita noudattamalla voit ottaa käyttöön yritystiedostojen hallinnan toiminnot kaikille yrityksille.

1. Avaa **Ominaisuuksien hallinta** -työtila.
2. Valitse **Uusi**-välilehdestä **Liiketoiminta-asiakirjojen hallinta** -ominaisuus luettelosta.
3. Ota valittu toiminto käyttöön valitsemalla **Ota käyttöön nyt**.
4. Voit avata uuden toiminnon päivittämällä sivun.

![Ominaisuushallinnan työtila](./media/BDM-Overview-FMEnabling.png)

Lisätietoja uusien ominaisuuksien aktivoinnista on kohdassa [ominaisuuksien hallinnan yleiskuvaus](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

## <a name="configure-parameters"></a>Konfiguroi parametrit

Seuraavien osien tietojen avulla voit määrittää liiketoiminnan tiedostojen hallinnan perusparametrit.

### <a name="prerequisites-for-parameter-setup"></a>Parametrien asetusten edellytykset
Ennen kuin voit määrittää liiketoiminnan asiakirjan hallinnan, sinun on määritettävä asiakirjan hallinnan kehys. Tämän tiedostotyypin avulla voit määrittää Office-muodoissa (Excel ja Word) olevien tiedostojen väliaikaisen tallennuksen, jota käytetään ER-raporttien malleina. Väliaikaista tallennusmallia voi muokata Office-työpöytäsovellusten avulla.

Tämän tiedosto tyypin osalta on valittava seuraavat määritearvot.

| **Määritteen nimi**  | **Määritteen arvo**   |
|---------------------|-----------------------|
| Luokka               | Liitä tiedosto           |
| Ryhmä               | Tiedosto                  |
| Toimipaikka            | SharePoint            |

Lisätietoja tarvittavien tiedoston hallintaparametrien ja tiedostotyyppien määrittämisestä on kohdassa [tiedostojen hallinnan määrittäminen](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management).

![Määritä asiakirjojen hallinnan tiedostotyyppi](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a>Parametrien määrittäminen

Liiketoiminnan asiakirjojen hallinnan perusparametrit voidaan määrittää **Liiketoiminta-asiakirjan parametrit** -sivulla. Vain tietyt käyttäjät voivat käyttää sivua. Näihin sisältyvät:

- **Järjestelmänvalvoja**-rooliin määritetyt käyttäjät.
- Käyttäjät, jotka on määritetty rooliin, joka pystyy suorittamaan toiminnon **Ylläpidä liiketoiminta-asiakirjan hallinnan parametreja** (AOT-nimi **ERBDMaintainParameters**).

Seuraavien ohjeiden avulla voit määrittää perusparametrit kaikille yrityksille.

1. Kirjaudu sisään käyttäjänä, jolla on **Liiketoiminta-asiakirjan parametrit** -sivun käyttöoikeus.
2. Siirry kohtaan **Organisaation hallinto** \> **Sähköinen raportointi** \> **Liiketoiminta-asiakirjojen hallinta**\> **Liiketoiminta-asiakirjan parametrit**.
3.  Määritä **Liiketoiminta-asiakirjan parametrit**-sivun **Liitteet**-välilehden **SharePoint-tiedostotyyppi** -kentässä asiakirjatyyppi, jota käytetään, kun malleja tallennetaan väliaikaisesti Office-muodoissa, kun niitä muokataan Office-työpöytäsovellusten avulla. 

> [!NOTE]
> Tätä parametria varten on käytettävissä vain tiedostotyyppejä , jotka on konfiguroitu käyttämällä SharePoint-sijaintia.

![Liiketoiminta-asiakirjan parametrien määrittäminen](./media/BDM-Overview-BDMSetting.png)

Valittu tiedostotyyppi on yrityskohtainen, ja sitä käytetään, kun käyttäjä käyttää liiketoiminnan tiedostojen hallintaa yrityksessä, jolle valittu tiedostotyyppi on määritetty. Kun käyttäjä käyttää liiketoiminnan tiedostojen hallintaa toisessa yrityksessä, käytetään samaa valittua tiedostotyyppiä, jos sellaista ei ole määritetty tälle yritykselle. Kun tiedostotyyppi on konfiguroitu, sitä käytetään **SharePoint-tiedostotyyppi** -kentässä valitun asemesta.

## <a name="configure-access-permissions"></a>Käyttöoikeuksien määrittäminen

Jos yrityksen tiedostojen hallinnan käyttöoikeuksia ei ole otettu käyttöön, kaikki yrityksen asiakirjahallinnan työtilan käyttäjät näkevät oletusarvoisesti kaikki ER-ratkaisumallit, jotka ovat käytettävissä. Liiketoiminnan asiakirjan hallinnan työtilassa näkyvät vain ne mallit, jotka sijaitsevat ER-muotomäärityksissä ja jotka on merkitty **Liiketoiminta-asiakirjatyyppi** -tunnisteella.

![Sähköisen raportoinnin konfiguroinnit -sivu](./media/BDM-Overview-ERFormatTags.png)

Yritysasiakirjan hallinnan työtilassa käytettävissä olevien mallien luetteloa voi rajoittaa määrittämällä käyttöoikeudet. Tämä voi olla tärkeää, kun eri malleja käytetään liiketoiminnan asiakirjojen tuottamiseen eri toimialueilla (toiminnalliset alueet), ja haluat sallia tietyille käyttäjille eri mallien käytön yritysasiakirjan hallinnan työtilassa muokkaamista varten.

Yritysasiakirjan hallinnan käyttöoikeudet voidaan määrittää kohdassa **Käyttöoikeuksien määritys**. Vain seuraavat käyttäjät voivat käyttää sivua:

- **Järjestelmänvalvoja**-rooliin määritetyt käyttäjät.
- Käyttäjät, jotka on liitetty mihin tahansa rooliin, joka on määritetty suorittamaan tehtävä **Aseta käyttöoikeuksia käyttääksesi liiketoiminta-asiakirjamallien muokkausta** (AOT-nimi **ERBDTemplatesSecurity**).

Seuraavia ohjeita noudattamalla voit määrittää yritystiedostojen hallinnan käyttöoikeudet kaikille yrityksille.

1. Kirjaudu sisään käyttäjänä, jolla on **Käyttöoikeuksien määritys** -sivun käyttöoikeus.
2. Siirry kohtaan **Organisaation hallinto** \> **Sähköinen raportointi** \> **Liiketoiminta-asiakirjojen hallinta**\> **Käyttöoikeuksien hallinta**.

Kiinnitä huomiota ilmoitukseen, jossa kerrotaan, että liiketoimintatiedostojen hallinnan käyttöoikeuksien käyttöä ei ole otettu käyttöön tällä hetkellä.

![Yritysasiakirjan hallinnan käyttöoikeuskonfiguraattorin sivu](./media/BDM-Overview-TemplatesAccess1.png)

Kun tämä asetus on käytössä, kaikki sellaiseen käyttöoikeusrooliin määritetyt käyttäjät, jotka on määritetty suorittamaan tehtävä **Liiketoiminta-asiakirjamallien hallinta** (AOT-nimi **ERBDManageTemplates**), voivat avata yritysasiakirjan hallinnan työtilan ja muokata mitä tahansa käytettävissä olevaa mallia.

Seuraavassa kuvassa näkyy, mitä yritysasiakirjan hallinnan työtilassa on käytettävissä **Myyntireskontranhoitaja**-rooliin määritetyille käyttäjille. Nykyisten käyttöoikeuksien asetuksen avulla käyttäjä voi muokata eri toimintoalueista peräisin olevia liiketoiminta-asiakirjamalleja, kuten laskutusta, viranomaisraportointia ja maksuja.

![Liiketoiminta-asiakirjojen hallinnan työtilan sivu](./media/BDM-Overview-TemplatesForAlice1.png)

3. Valitse **Käyttöoikeuksien määritys** -sivulla **Käyttöoikeuksien asetukset**.
4. Ota **Mallien muokkauksen käyttöoikeuksien asetukset** -valintaikkunassa käyttöön **Ota määritetyt käyttöoikeudet käyttöön** -vaihtoehto.
5. Vahvista , että yritysasiakirjan hallinnan käyttöoikeudet on otettu käyttöön valitsemalla **OK**.

![Yritysasiakirjan hallinnan käyttöoikeuksien määritysten sivu](./media/BDM-Overview-TemplatesAccess2.png)

6. Valitse **Lisää**, jos haluat määrittää uuden liiketoimintaroolin, jonka käyttöoikeuksia yritysasiakirjan hallinnan malleihin on määritettävä.
7. Valitse **Käyttöoikeusroolit** -valintaikkunassa **Myyntireskontranhoitaja**-rooli ja vahvista roolin valinta valitsemalla **OK**.
8. Valitse **Määritystunnistekohtaiset käyttöoikeudet** -välilehdessä **Uusi**.
9. Valitse **Tunnisteen tyyppi** -kentässä **Toiminnallinen alue** ja valitse **Tunnus**-kentästä **Laskutus**.
10. Valitse **Tallenna**, jos haluat tallentaa valitun roolin määritetyt käyttöoikeudet.

  Nykyiset asetukset tarkoittavat sitä, että kaikille käyttäjille, jotka on liitetty **Myyntireskontranhoitaja**-rooliin ja jotka suorittavat tehtävän **Liiketoiminta-asiakirjamallien hallinta** (AOT-nimi **ERBDManageTemplates**), ER-muotokonfigurointimallit, joiden **Toiminnallinen alue** -tunnisteen arvo on **Laskutus**, ovat käytettävissä muokattavaksi yritysasiakirjan hallinnan työtilassa.

11. Vaihda **Aiheeseen liittyviä tietoja** -ruutu nykyisen sivun oikeasta reunasta. **Aiheeseen liittyviä tietoja** -ruudussa näkyy, miten konfiguroituja käyttöoikeuksia käytetään, mukaan lukien se, mitä ER-konfigurointimalleja **Myyntireskontranhoitaja**-rooliin määritetyt käyttäjät voivat käyttää.

![Yritysasiakirjan hallinnan käyttöoikeuksien määritysten sivu](./media/BDM-Overview-TemplatesAccess3.png)

12. Valitse **Määrityskohtaiset käyttöoikeudet** -välilehdessä **Lisää**.
13. Merkitse **Valitse määritys** -valintaikkunassa ER-muotokonfiguraatio **Intrastat-raportti**.
14. Vahvista valittujen konfiguraatioiden määritys valitsemalla **OK** ja tallenna valitun roolin määritetyt käyttöoikeudet valitsemalla **Tallenna**.

Nykyiset asetukset tarkoittavat sitä, että kaikille käyttäjille, jotka on liitetty **Myyntireskontranhoitaja**-rooliin ja jotka suorittavat tehtävän **Liiketoiminta-asiakirjamallien hallinta** (AOT-nimi **ERBDManageTemplates**), seuraavat mallit ovat käytettävissä muokattavaksi yritysasiakirjan hallinnan työtilassa:

- Mallit, joiden **Toiminnallinen alue** -tunnisteen arvo on **Laskutus**.
- Mallit ER-muotokonfiguraatioista, jotka on lueteltu **Määrityskohtaiset käyttöoikeudet** -välilehdessä (mallit **Intrastat-raportti** -muotokokoonpanosta **Lakisääteinen raportointi** -toimialueella tässä esimerkissä).

![Yritysasiakirjan hallinnan käyttöoikeuksien määritysten sivu](./media/BDM-Overview-TemplatesAccess4.png)

Seuraavassa kuvassa näkyy, mitä yritysasiakirjan hallinnan työtilassa on saatavilla **Myyntireskontranhoitaja**-rooliin määritetyille käyttäjille. Nykyisen yritysasiakirjan hallinnan käyttöoikeuksien asetuksen avulla käyttäjä voi muokata liiketoiminta-asiakirjamalleja **Laskutus**-toimialueelta ja **Intrastat-raportti** -muotokonfiguraatiosta. **Maksu**-toimialueen mallit eivät ole käytettävissä **Myyntireskontranhoitaja**-roolille.

![Liiketoiminta-asiakirjojen hallinnan työtilan sivu](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> **Määrityskohtaiset käyttöoikeudet** -säännöt tallennetaan käyttämällä ER-muotokonfiguraation yksilöivää tunnusta. Tämä tarkoittaa, että näitä sääntöjä ei poisteta, kun niihin viittaava ER-konfiguraatio poistetaan. Kun tuot poistetut konfiguraatiot takaisin tähän esiintymään, nämä säännöt viittaavat niihin uudelleen. Sääntöjä ei tarvitse määrittää uudelleen poistettujen konfiguraatioiden tuomisen jälkeen.

## <a name="use-business-document-management-to-edit-templates"></a>Mallien muokkaaminen yritystiedostojen hallinnan avulla

Yrityskäyttäjät voivat käyttää yrityksen asiakirjamalleja muokkausta varten liiketoiminnan asiakirjanhallinnan työtilassa. Vain seuraavat käyttäjät voivat käyttää liiketoiminta-asiakirjan hallinnan työtilaa:

- **Järjestelmänvalvoja**-rooliin määritetyt käyttäjät.
- Käyttäjät, jotka on määritetty rooliin, joka pystyy suorittamaan toiminnon **Liiketoiminta-asiakirjamallien hallinta** (AOT-nimi **ERBDManageTemplates**).

Seuraavia ohjeita noudattamalla voit muokata vapaatekstilaskun malleja yritysasiakirjanhallinnan työtilassa. Ennen kuin suoritat nämä toimet, tämän ohje aiheen kaikki edellä mainitut toimenpiteet on suoritettava loppuun.

1. Kirjaudu sisään käyttäjänä, jolla on Liiketoiminta-asiakirjan hallintatyötilan käyttöoikeus.
2. Avaa liiketoiminta-asiakirjojen hallinnan työtila.

![Liiketoiminta-asiakirjojen hallinnan työtilan sivu](./media/BDM-Overview-EditingTemplate1.png)

**Malli** -välilehdessä näkyy valitun mallin sisältö. Valitse **Tiedot**-välilehti, jossa voit tarkastella valitun mallin tietoja sekä sen ER-muotokonfiguraation tietoja, jossa tämä malli sijaitsee. Huomaa, että kaikkien mallien tila on **Julkaistu**, eivätkä ne sisällä tietoja **Tarkistusversio**-sarakkeessa. Tämä tarkoittaa, että näitä malleja ei tällä hetkellä muokata.

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Konfigurointipalvelun omistamien mallien muokkauksen aloittaminen

1. Valitse yritysasiakirjan hallinnan työtilassa **Sekkien tulostusmuoto** -malli luettelosta.
2. Valitse **Tiedot**-välilehti.

![Liiketoiminta-asiakirjojen hallinnan työtilan sivu](./media/BDM-Overview-EditingTemplate2.png)

**Muokkaa mallia-** vaihtoehto on käytettävissä valitulle mallille. Tämä vaihtoehto on aina käytettävissä mallissa, joka on ER-muotokokoonpanossa, jonka omistaa aktiivinen ER-konfiguraatiopalvelun toimittaja (tässä esimerkissä **Litware, Inc**). Kun **Muokkaa mallia** on valittuna, aiemmin luodun ER-muotokonfiguraation luonnosversion mallia voi muokata.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Muiden palveluiden omistamien mallien muokkauksen aloittaminen

1. Valitse yritysasiakirjan hallinnan työtilassa **Asiakkaan FTI-raportti (GER)** -malli luettelosta.
2. Valitse **Tiedot**-välilehti.

![Liiketoiminta-asiakirjojen hallinnan työtilan sivu](./media/BDM-Overview-EditingTemplate3.png)

**Uusi asiakirja** -vaihtoehto on käytettävissä valitulle mallille. Tämä vaihtoehto on aina käytettävissä mallissa, joka on ER-muotokokoonpanossa, jonka tarjoaa toinen toimittaja (tässä esimerkissä **Microsoft**). Kun **Uusi asiakirja** valitaan, uusi malli on muokattavissa. Muokattu malli tallennetaan sen jälkeen uuteen ER-muotokonfiguraatioon, joka luodaan automaattisesti.

### <a name="start-editing-a-template"></a>Aloita mallin muokkaus

1. Valitse valitusta mallista **Uusi asiakirja**.
2. Muuta tarvittaessa muokattavan mallin otsikkoa **Otsikko**-kentässä. Tekstin avulla voit nimetä automaattisesti luotavan ER-muodon konfiguraation. Huomaa, että tämän konfiguraation luonnos (**Asiakkaan FTI-raportti (GER) Copy**), joka sisältää muokatun mallin, merkitään automaattisesti suorittamaan tämä ER-muoto nykyiselle käyttäjälle. Samaan aikaan ER-perusmuotomäärityksen ei-muokattua alkuperäistä mallia käytetään tämän ER-muodon suorittamiseen toiselle käyttäjälle.
3. Vaihda **Nimi** -kenttään automaattisesti luotavan muokattavan mallin ensimmäisen version nimi.
4. Vaihda **Kommentti**-kenttään automaattisesti luotavan muokattavan mallin huomautus.

![Liiketoiminta-asiakirjojen hallinnan työtilan sivu](./media/BDM-Overview-EditingTemplate4.png)

5. Vahvista muokkausprosessin aloittaminen valitsemalla **OK**.

**BDM-mallieditori**-sivu avautuu. Valittu malli on käytettävissä online-muokkausta varten käyttämällä Office 365:tä.

![Liiketoiminta-asiakirjojen hallinnan työtilan sivu](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-office-365"></a>Mallin muokkaaminen Office 365:ssä

Muokkaa mallia käyttämällä Office 365 -toiminnallisuutta. Esimerkiksi Office Onlinessa voit muuttaa mallin otsikossa olevien kenttä kehotteiden fonttia arvosta **Normaali** arvoon **Lihavoitu**. Nämä muutokset tallentuvat automaattisesti muokattavaan malliin, joka on tallennettu ER-kehikolle määritettyyn ensisijaisen perusmallin tallennustilaan (oletusarvona on Azuren blob-säilö).

![Yritystiedostojen hallinnan mallin muokkauseditori](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a>Mallin muokkaaminen Office-työpöytäsovelluksessa

1. Valitse **Avaa työpöytäsovelluksessa** -vaihtoehto, jos haluat muokata mallia Office-työpöytäsovelluksen toimintojen avulla (tässä esimerkissä Excel). Muokattava malli kopioidaan pysyvästä tallennuspaikasta yrityksen tiedostojen hallinnan parametreissa määritettyyn väliaikaiseen varastoon SharePoint-kansiona.
2. Vahvista, että haluat avata mallin väliaikaisesta tiedostovarastoinnista Officen Excel -työpöytäsovelluksessa.

![Liiketoiminta-asiakirjojen hallinnan työtilan sivu](./media/BDM-Overview-EditingLayout3.png)

3. Muokkaa mallia. Esimerkiksi voit muuttaa mallin otsikossa olevien kenttäkehotteiden fonttia päivittämällä värin arvosta **Musta** arvoon **Sininen**.

![Yritystiedostojen hallinnan mallin muokkauseditori](./media/BDM-Overview-EditingLayout4.png)

4. Tallenna mallin muutokset väliaikaiseen varastoon valitsemalla Excel-työpöytäsovelluksessa **Tallenna**.

![Yritystiedostojen hallinnan mallin muokkauseditori](./media/BDM-Overview-EditingLayout5.png)

5. Sulje Excel-työpöytäsovellus.
6. Synkronoi väliaikainen mallisäilö pysyvään mallivarastoon valitsemalla **Synkronoi tallennettu kopio**.

> [!NOTE]
> Väliaikaisen tiedostovaraston muokattavan mallin kopio säilytetään vain nykyisessä mallinmuokkausistunnossa. Kun lopetat tämän istunnon sulkemalla **BDM-mallieditorin** sivun, tämä kopio poistetaan. Jos olet säätänyt mallin väliaikaisessa tiedostotallennuksessa etkä valinnut **Synkronoi tallennettu kopio** -vaihtoehtoa, kun yrität sulkea **BDM-mallieditori** -sivun, näyttöön tulee sanoma, jossa kysytään, haluatko tallentaa tehdyt muutokset. Valitse **kyllä**, jos haluat tallentaa malliin tekemäsi muutokset pysyvään tiedostosijaintiin.

### <a name="validate-a-template"></a>Tarkista malli

1. Valitse **BDM-mallieditorin** sivulla **Tarkista ongelmat** vahvitaaksesi muokatun mallin suhteessa pohjana olevaan ER-muotokonfiguraatioon. Noudata suosituksia (jos sellaisia on), jos haluat yhtenäistää mallin ER-perusmuotokonfiguraation muodon rakenteen kanssa.
2. Valitse **Näytä muoto**, jos haluat tarkastella muodon nykyistä rakennetta ER-perusmuotomäärityksistä, joka on yhdenmukaistettava muokattavan mallin kanssa. 
3. Voit sulkea ruudun valitsemalla **Piilota muoto**.

![BDM-mallieditorin sivu](./media/BDM-Overview-EditingTemplate6.png)

4. Sulje **BDM-mallieditorin** sivu.

Päivitetty malli näkyy **Malli**-välilehdessä. Huomaa, että muokatun mallin tila on nyt **Luonnos** eikä nykyinen versio ole enää tyhjä. Tämä tarkoittaa, että tämän mallin muokkauksen prosessi on aloitettu.

![Liiketoiminta-asiakirjojen hallinnan työtilan sivu](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Muokatun mallin testaaminen 

1. Vaihda sovelluksessa yritykseen **USMF**.
2. Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.
3. Valitse **FTI-00000002** -lasku ja valitse sitten **Tulostuksenhallinta**.
4. Valitse **Moduuli - Myyntireskontra** \> **Tiedostot** \> **Vapaatekstilasku** \> **Alkuperäinen tiedosto** -taso määrittääksesi käsiteltävien laskujen vaikutusalueen.
5. Valitse **Raportin muoto** -kentästä **Asiakkaan FTI-raportti (GER) Copy** -ER-muoto määritetylle tiedostotasolle.

![Tulostuksenhallinnan asetukset -sivu](./media/BDM-Overview-TestRun1.png)

6. Voit sulkea nykyisen sivun painamalla **ESC-näppäintä**.
7. Valitse **Tulosta** ja valitse **Valittu**.
8. Lataa tiedosto ja avaa se käyttämällä Excel-työpöytäsovellusta.

![Vapaatekstilaskut-sivu](./media/BDM-Overview-TestRun2.png)

Muokatun mallin avulla luodaan valitulle nimikkeelle vapaatekstilaskun raportti. Jos haluat analysoida, miten malliin tekemäsi muutokset vaikuttavat tähän raporttiin, voit suorittaa tämän raportin yhdessä sovellusistunnossa suoraan sen jälkeen, kun olet muokannut mallia toisessa sovellusistunnossa.

### <a name="create-an-alternative-template-revision"></a>Vaihtoehtoisen malliversion luominen

1. Avaa **BDM-mallieditorib** sivu ja valitse **Asiakkaan FTI-raportti (GER) Copy** -malli.
2. Valitse **Versiot**-välilehdestä **Uusi**.
3. Muuta tarvittaessa toisen version nimeä **Nimi** -kentässä ja perusta se tällä hetkellä aktiiviselle ensimmäiselle versiolle.
4. Vaihda **Kommentti**-kenttään automaattisesti luotavan muokattavan mallin huomautus tarvittaessa.

![Liiketoiminta-asiakirjojen hallinnan työtilan sivu](./media/BDM-Overview-AddRevision.png)

Loit uuden mallin version, joka on tallennettu pysyvän mallin varastoon. Voit jatkaa nyt aktiiviseksi valitun toisen version mallin muokkaamista.

5. Valitse ensimmäinen versio ja valitse sitten **Määritä aktiivinen**. Voit valita toisen version aktiiviseksi, jos haluat palata kyseiseen mallin versioon.
6. Valitse toinen versio ja valitse sitten **Poista**.
7. Valitse **OK**, kun haluat poistaa valitun version. Voit poistaa kaikki ei-aktiiviset versiot, kun niitä ei enää tarvita.

### <a name="delete-a-modified-template"></a>Muokatun mallin poistaminen

1. Valitse **Malli**-välilehti **BDM mallieditorin** sivulla.
2. Valitse **Poista**.
3. Jos valitset **OK** poiston vahvistamiseksi, **Asiakkaan FTI-raportti (GER) Copy** -ER-muoto poistetaan muokatun mallin kanssa. Voit tutkia muita vaihtoehtoja valitsemalla **Peruuta**.

### <a name="revoke-changes-of-template"></a>Peruuta mallin muutokset

Kun muokkaat mallia nykyisen aktiivisen palveluntarjoajan omistamasta ER-muodosta, sinulle tarjotaan mahdollisuus peruuttaa malliin tehdyt muutokset.

![Liiketoiminta-asiakirjojen hallinnan työtilan sivu](./media/BDM-Overview-RevokeChanges.png)

1. Valitse **Malli**-välilehti **BDM mallieditorin** sivulla.
2. Valitse **Kumoa**.
3. Jos valitset **OK** peruuttaaksesi malliin tehdyt muutokset, muokattu malli korvataan alkuperäisellä mallilla ja kaikki muutokset poistetaan. Kun peruutat malliin tehdyt muutokset, voit poistaa mallin. Voit tutkia muita vaihtoehtoja valitsemalla **Peruuta**.

### <a name="publish-a-modified-template"></a>Muokatun mallin julkaiseminen
1. Valitse **BDM mallieditorin** sivun **Malli**-välilehdessä **Julkaise**.
2. Jos valitset **OK** julkaisun vahvistamiseksi, muutetun mallin sisältävä **Asiakkaan FTI-raportti (GER) Copy** -ER-muodon johdettu luonnos merkitään valmiiksi. Muokattu malli tulee muiden käyttäjien saataville. Tämän ER-muodon valmiit versiot säilyttävät vain mallin viimeisimmän aktiivisen version. Muut versiot poistetaan. Voit tutkia muita vaihtoehtoja valitsemalla **Peruuta**.

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

#### <a name="i-selected-new-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-office-365-web-page"></a>Valitsin **Uusi asiakirja**, mutta sen sijaan, että avautuisi **BDM-mallieditorin** sivu Finance and Operationsissa, minut on siirretty Office 365 -verkkosivulle.
Tämä on tunnettu Office 365:n uudelleenohjauksen ongelma. Näin tapahtuu, kun kirjaudut Office 365:een ensimmäisen kerran. Voit välttää tämän ongelman valitsemalla selaimesi **Takaisin**-painikkeen ja siirtymällä takaisin.

#### <a name="i-understand-how-to-edit-a-template-by-using-office-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-adjusting-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-do-this-using-the-office-desktop-application"></a>Ymmärrän, miten voit muokata mallia käyttämällä Office 365:tä ensimmäisessä sovellusistunnossa ja miten mallia käytetään toisessa sovellusistunnossa mallin säätämiseen, jotta näen, miten muutokset vaikuttavat luotuun liiketoimintaasiakirjaan. Voinko tehdä tämän Office-työpöytäsovelluksen avulla?
Kyllä voit. Valitse ensimmäisessä sovellusistunnossa **Avaa työpöytäsovelluksessa**. Malli tallennetaan väliaikaiseen tiedostovarastoon ja avataan Office-työpöytäsovelluksessa. Tee seuraavaksi seuraavat vaiheet, kun haluat esikatsella mallin muutoksia luodussa yritysasiakirjassa:

1. Tee muutoksia malliin käyttämällä Office-työpöytäsovellusta.
2. Valitse Office-työpöytäsovelluksessa **Tallenna**.
3. Valitse ensimmäisen sovellusistunnon **BDM-mallieditorin**sivulla **Synkronoi tallennettu kopio**.
4. Suorita tämä mallin ER-muoto toisessa sovellusistunnossa.

#### <a name="i-get-the-error-value-cannot-be-null-parameter-name-externalid-when-i-select-open-in-desktop-app-how-do-i-work-around-this"></a>Näyttöön tulee virhe "Arvo ei voi olla nolla. Parametrin nimi: : externalId’, kun valitsen **Avaa työpöytäsovelluksessa**. Kuinka voin välttää tämän? 
Kirjauduit todennäköisesti Azure AD -toimialueen nykyisen sovelluksen esiintymään, joka ei ole sama kuin esiintymän käyttöönotossa käytetty Azure AD -toimialue. Koska SharePoint-palvelu, johon tallennetaan malleja, joiden avulla niitä voidaan muokata Office-työpöytäsovelluksella, kuuluu samaan toimialueeseen, meillä ei ole SharePoint-palvelun käyttöoikeuksia. Voit ratkaista tämän ongelman kirjautumalla nykyiseen esiintymään käyttämällä oikean Azure AD -toimialueen käyttäjän tunnistetietoja.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Suunnittele kokoonpano, jolla raportit voi luoda OPENXML-muodossa](tasks/er-design-reports-openxml-2016-11.md)

[Suunnittele ER-konfiguraatiot voidaksesi luoda raportteja Word-muodossa](tasks/er-design-configuration-word-2016-11.md)

[Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md)

[Sähköisen raportoinnin määrittäminen hakemaan tiedot Power BI:hin](general-electronic-reporting-report-configuration-get-data-powerbi.md)
