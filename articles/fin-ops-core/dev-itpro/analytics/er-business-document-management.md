---
title: Liiketoiminta-asiakirjojen hallinta – yleiskatsaus
description: Tässä ohjeaiheessa on tietoja ER-kehyksen liiketoiminnan asiakirjojen hallintatoiminnon käyttämisestä.
author: NickSelin
ms.date: 04/23/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: faea9d4d9b3fc8f3f1474b6bb2a8dc31cdc22511
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986248"
---
# <a name="business-document-management-overview"></a>Liiketoiminta-asiakirjojen hallinta – yleiskatsaus

[!include [banner](../includes/banner.md)]

Yrityskäyttäjät käyttävät [sähköisen raportoinnin (ER)](general-electronic-reporting.md) kehystä määrittääkseen lähtevien sähköisten asiakirjojen muodot eri maiden ja alueiden lakisääteisten vaatimusten mukaisiksi. Käyttäjät voivat myös määrittää tietovirran määrittääkseen, mitkä sovellustiedot sijoitetaan luotuihin tiedostoihin. ER-kehys luo lähteviä tiedostoja Microsoft Office -muodoissa (Excel-työkirjoissa tai Word-asiakirjoissa) ennalta määritettyjen mallien avulla. Mallit täytetään tarvittavilla tiedoilla määritetyn tietovirran mukaisesti, kun vaadittavat tiedostot luodaan. Kukin konfiguroitu muoto voidaan julkaista osana ER-ratkaisua tiettyjen lähtevien tiedostojen luomista varten. Tätä kuvaa ER-muotoonfiguraatio, joka voi sisältää malleja, joiden avulla voit luoda erilaisia lähteviä asiakirjoja. Yrityskäyttäjät voivat hallita tarvittavia liikeasiakirjoja tämän kehyksen avulla.

**Liiketoiminta-asiakirjojen hallinta** perustuu ER-kehykseen, ja sen avulla yrityskäyttäjät voivat muokata liiketoiminta-asiakirjamalleja Microsoft 365 -palvelun tai asianmukaisen Microsoft Office -työpöytäsovelluksen avulla. Asiakirjoihin tehdyt muokkaukset voivat olla liiketoiminnan asiakirjamallien muuttamista ja lisätietojen paikkamerkkien lisäämistä ilman lähdekoodin muutoksia ja uusia käyttöönottoja. Yritysasiakirjojen mallien päivittämiseksi ei tarvita tietoja ER-kehyksestä.

> [!NOTE]
> Huomaa, että yritystiedostojen hallinnan avulla voit muokata malleja, joita käytetään liiketoiminnan asiakirjojen, kuten tilausten, laskujen jne. tuottamiseen. Kun mallia on muokattu ja sen uusi versio on julkaistu, tätä versiota käytetään tarvittavien liikeasiakirjojen luomiseen. Yritysasiakirjan hallintaa ei voi käyttää aiemmin luotujen liikeasiakirjojen muokkaamiseen.

## <a name="supported-deployments"></a>Tuetut käyttöönotot

Tällä hetkellä yritysasiakirjan hallintatoiminto on käytössä vain pilvikäyttöönotoissa. Jos tämä toiminto on kriittinen paikallisen käyttöönoton kannalta, kerro siitä meille antamalla palautetta [Ideat](https://experience.dynamics.com/ideas/)-sivustossa.

## <a name="supported-microsoft-office-applications"></a>Tuetut Microsoft Office -sovellukset

Yritystiedostojen hallinnan käyttäminen mallien muokkaamiseen Excel- tai Word-muodoissa Microsoft Office -työpöytäsovellusten avulla edellyttää, että asennettuna on Microsoft Office 2010 tai uudempi. Tätä tuetaan sekä pilvi- että paikallisissa käyttöönotoissa.

Yritystiedostojen hallinnan käyttäminen mallien muokkaamiseen Excel- tai Word-muodoissa Microsoft 365 -sovellusten avulla edellyttää, että asennettuna on Microsoft 365 Office verkkotilausta varten. Tätä tuetaan pilvikäyttöönotossa.

## <a name="business-document-availability"></a>Yritysasiakirjojen käytettävyys

Täydellinen luettelo kaikista lokakuun 2019 julkaisun suunnitelluista raporteista on kohdassa [Määritettävien liiketoiminta-asiakirjaraportointi Wordissa ja Excelissä](/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).

Täydellinen luettelo kaikista lokakuun 2020 julkaisun suunnitelluista raporteista on kohdassa [Määritettävät liiketoiminta-asiakirjat – Word-mallit](/dynamics365-release-plan/2020wave1/dynamics365-finance/configurable-business-documents-word-templates).

Lisää raportteja tulee saataville tulevissa julkaisuissa. Lisäraporttien erityisilmoitukset lähetetään erikseen. Lisätietoja tällä hetkellä saatavilla olevien raporttien luettelon tarkistamisesta on jäljempänä kohdassa [Luettelo Financessa julkaistuista määritettäviä liiketoiminta-asiakirjoja tukevista ER-määrityksistä](#list-of-configurations-cbd).

Saat lisätietoja tästä toiminnosta suorittamalla tämän ohjeaiheen seuraavan esimerkin.

## <a name="configure-er-parameters"></a>Konfiguroi ER-parametrit

Koska yritysasiakirjan hallinta perustuu ER-kehykseen, on määritettävä ER-parametrit, jotta yritystiedostojen hallinta voidaan aloittaa. Jotta voisit tehdä tämän, sinun on määritettävä ER-parametrit kohdassa [Sähköisen raportoinnin (ER) kehyksen määrittäminen](electronic-reporting-er-configure-parameters.md) kuvatulla tavalla. Lisää myös uusi konfigurointipalvelu, joka on kuvattu kohdassa [Luo konfigurointipalvelut ja merkitse ne aktiivisiksi](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![ER-työtila.](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>Tuo ER-ratkaisut

Tämän menettelyn esimerkeissä käytetään ER-näytemäärityksiä. Nykyiseen Dynamics 365 Finance -esiintymään on tuotava ER-määrityksiä, joiden sisältämiä liiketoiminta-asiakirjamalleja voidaan muokata liiketoiminta-asiakirjojen hallinnalla. Suorita nämä toimet lataamalla ja tallentamalla paikallisesti seuraavat tiedostot.

**Esimerkki ER-asiakaslaskutusratkaisusta**

| Tiedosto                                      | Sisältö |
|-------------------------------------------|---------|
| Customer invoicing model.version.2.xml    | [ER-tietomallin konfigurointi](https://download.microsoft.com/download/b/f/a/bfa5cb52-e6e2-42bc-a4c0-77014a4c54e6/Customerinvoicingmodel.version.2.xml) |
| Customer FTI report (GER).version.2.3.xml | [Vapaatekstilaskun ER-muodon määritys](https://download.microsoft.com/download/3/c/2/3c2e58f2-6e56-43d9-85ea-4c97252a108d/CustomerFTIreportGER.version.2.3.xml) |

**Esimerkki ER-maksutarkastusratkaisusta**

| Tiedosto                                     | Sisältö |
|------------------------------------------|---------|
| Model for cheques.version.10.xml         | [ER-tietomallin konfigurointi](https://download.microsoft.com/download/3/7/6/376cb0f6-181a-4895-a432-390ffca64162/Modelforcheques.version.10.xml) |
| Cheques printing format.version.10.9.xml | [Maksusekin ER-muodon konfigurointi](https://download.microsoft.com/download/6/d/6/6d61bfff-3d89-4377-9e34-2e3ee6d6df91/Chequesprintingformat.version.10.9.xml) |

**Esimerkki ER-ulkomaankaupparatkaisusta**

| Tiedosto                             | Sisältö |
|----------------------------------|---------|
| Intrastat model.version.1.xml    | [ER-tietomallin konfigurointi](https://download.microsoft.com/download/2/0/0/200d6ed1-eff8-48ec-ab75-175a4acf9714/Intrastatmodel.version.1.xml) |
| Intrastat report.version.1.9.xml | [Intrastat-valvontaraportin ER-muodon konfigurointi](https://download.microsoft.com/download/7/a/2/7a2a27c3-a8a5-42a1-9d04-f0a8e1ec1707/Intrastatreport.version.1.9.xml) |

Tuo kukin tiedosto noudattamalla seuraavia ohjeita. Tuo kunkin ER-ratkaisun ER-*tietomallin* konfiguraatio yllä oleviin tauluihin ennen kuin tuot vastaavan ER *-muodon* konfiguraation.

1. Avaa **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot** -sivu.
2. Valitse sivun yläosassa **Vaihda**.
3. Valitse **Lataa XML-tiedostosta**.
4. Lataa tarvittava XML-tiedosto valitsemalla **Selaa**.
5. Vahvista konfiguroinnin tuonti valitsemalla **OK**.

![Määrityksen tuonnin vahvistava ER-määritysten sivu.](./media/BDM-Overview-ERSolutions.png)

Vaihtoehtoisesti voit tuoda virallisesti julkaistut ER-muotomääritykset Microsoft Dynamics Lifecycle Servicestä (LCS). Tämän menettelyn viimeistelyä voit esimerkiksi tuoda **Vapaatekstilasku (Excel)** -ER-muotomäärityksen uusimman version. Vastaavat ER-tietomalli ja ER-mallin yhdistämismääritykset tuodaan automaattisesti.

![LCS:n jaetun resurssikirjaston sisältösivu.](./media/BDM-Overview-SharedAssetLibrary.png)

Lisätietoja ER-määritysten tuomisesta on kohdassa [ER-konfiguraation elinkaaren hallinta](general-electronic-reporting-manage-configuration-lifecycle.md).

## <a name="enable-business-document-management"></a>Ota liiketoiminta-asiakirjojen hallinta käyttöön

Jos haluat käynnistää yritystiedostojen hallinnan, sinun on avattava **Ominaisuuksien hallinta** -työtila ja otettava käyttöön **Liiketoiminta-asiakirjojen hallinta** -ominaisuus.

Seuraavia ohjeita noudattamalla voit ottaa käyttöön yritystiedostojen hallinnan toiminnot kaikille yrityksille.

1. Avaa **Ominaisuuksien hallinta** -työtila.
2. Valitse **Uusi**-välilehdestä **Liiketoiminta-asiakirjojen hallinta** -ominaisuus luettelosta.
3. Ota valittu toiminto käyttöön valitsemalla **Ota käyttöön nyt**.
4. Voit avata uuden toiminnon päivittämällä sivun.

> [!NOTE]
> Lisätietoja uuden asiakirjan käyttöliittymän käyttämisestä liiketoiminta-asiakirjojen hallinnassa on kohdassa [Uusi asiakirjojen käyttöliittymä liiketoiminta-asiakirjojen hallinnassa](er-business-document-management-new-template-ui.md).

![Ominaisuuksien hallinta -työtila.](./media/BDM-Overview-FMEnabling.png)

Lisätietoja uusien ominaisuuksien aktivoinnista on kohdassa [ominaisuuksien hallinnan yleiskuvaus](../../fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-parameters"></a>Konfiguroi parametrit

Seuraavien osien tietojen avulla voit määrittää liiketoiminnan tiedostojen hallinnan perusparametrit.

### <a name="prerequisites-for-parameter-setup"></a>Parametrien asetusten edellytykset

Ennen kuin voit määrittää liiketoiminnan asiakirjan hallinnan, sinun on määritettävä asiakirjan hallinnan kehys. Tämän tiedostotyypin avulla voit määrittää Office-muodoissa (Excel ja Word) olevien tiedostojen väliaikaisen tallennuksen, jota käytetään ER-raporttien malleina. Väliaikaista tallennusmallia voi muokata Office-työpöytäsovellusten avulla.

Tämän tiedosto tyypin osalta on valittava seuraavat määritearvot.

| Määritteen nimi | Määritteen arvo |
|----------------|-----------------|
| Luokka          | Liitä tiedosto     |
| Ryhmä          | Tiedosto            |
| Toimipaikka       | SharePoint      |

Lisätietoja tarvittavien tiedoston hallintaparametrien ja tiedostotyyppien määrittämisestä on kohdassa [tiedostojen hallinnan määrittäminen](../../fin-ops/organization-administration/configure-document-management.md).

![Määritä asiakirjojen hallinnan tiedostotyyppi.](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a><a name="SetupBdmParameters"></a>Parametrien määrittäminen

Liiketoiminnan asiakirjojen hallinnan perusparametrit voidaan määrittää **Liiketoiminta-asiakirjan parametrit** -sivulla. Vain tietyt käyttäjät voivat käyttää sivua. Näihin sisältyvät:

- **Järjestelmänvalvoja**-rooliin määritetyt käyttäjät.
- Käyttäjät, jotka on määritetty rooliin, joka pystyy suorittamaan toiminnon **Ylläpidä liiketoiminta-asiakirjan hallinnan parametreja** (AOT-nimi **ERBDMaintainParameters**).

Seuraavien ohjeiden avulla voit määrittää perusparametrit kaikille yrityksille.

1. Kirjaudu sisään käyttäjänä, jolla on **Liiketoiminta-asiakirjan parametrit** -sivun käyttöoikeus.
2. Siirry kohtaan **Organisaation hallinto** \> **Sähköinen raportointi** \> **Liiketoiminta-asiakirjojen hallinta**\> **Liiketoiminta-asiakirjan parametrit**.
3. Määritä **Liiketoiminta-asiakirjan parametrit**-sivun **Liitteet**-välilehden **SharePoint-tiedostotyyppi** -kentässä asiakirjatyyppi, jota käytetään, kun malleja tallennetaan väliaikaisesti Office-muodoissa, kun niitä muokataan Office-työpöytäsovellusten avulla. 

> [!NOTE]
> Tätä parametria varten on käytettävissä vain tiedostotyyppejä , jotka on konfiguroitu käyttämällä SharePoint-sijaintia.

![Liiketoiminta-asiakirjan parametrien määrittäminen.](./media/BDM-Overview-BDMSetting.png)

Valittu tiedostotyyppi on yrityskohtainen, ja sitä käytetään, kun käyttäjä käyttää liiketoiminnan tiedostojen hallintaa yrityksessä, jolle valittu tiedostotyyppi on määritetty. Kun käyttäjä käyttää liiketoiminnan tiedostojen hallintaa toisessa yrityksessä, käytetään samaa valittua tiedostotyyppiä, jos sellaista ei ole määritetty tälle yritykselle. Kun tiedostotyyppi on konfiguroitu, sitä käytetään **SharePoint-tiedostotyyppi** -kentässä valitun asemesta.

> [!NOTE]
> **SharePoint -asiakirjatyyppi** -parametri määrittä SharePoint -kansion väliaikaiseksi tallennuspaikaksi malleille, joita voidaan muokata Microsoft Excelillä tai Wordilla. Tämä parametri on määritettävä, jos aiot käyttää näitä Office-työpöytäsovelluksia mallien muokkaamiseen. Lisätietoja on kohdassa [Mallin muokkaaminen Office-työpöytäsovelluksessa](#EditInOfficeDesktopApp). Voit pitää tämän parametrin tyhjänä, jos aiot muokata mallia vain käyttämällä toimintoa Microsoft 365:ssä. Lisätietoja on kohdassa [Mallin muokkaaminen Microsoft 365:ssä](#EditInOffice365).

## <a name="configure-access-permissions"></a>Käyttöoikeuksien määrittäminen

Jos yrityksen tiedostojen hallinnan käyttöoikeuksia ei ole otettu käyttöön, kaikki yrityksen asiakirjahallinnan työtilan käyttäjät näkevät oletusarvoisesti kaikki ER-ratkaisumallit, jotka ovat käytettävissä. Liiketoiminnan asiakirjan hallinnan työtilassa näkyvät vain ne mallit, jotka sijaitsevat ER-muotomäärityksissä ja jotka on merkitty **Liiketoiminta-asiakirjatyyppi** -tunnisteella.

![ER-määrityssivu ja liiketoiminta-asiakirjatyypin tunniste.](./media/BDM-Overview-ERFormatTags.png)

Yritysasiakirjan hallinnan työtilassa käytettävissä olevien mallien luetteloa voi rajoittaa määrittämällä käyttöoikeudet. Tämä voi olla tärkeää, kun eri malleja käytetään liiketoiminnan asiakirjojen tuottamiseen eri toimialueilla (toiminnalliset alueet), ja haluat sallia tietyille käyttäjille eri mallien käytön yritysasiakirjan hallinnan työtilassa muokkaamista varten.

Yritysasiakirjan hallinnan käyttöoikeudet voidaan määrittää kohdassa **Käyttöoikeuksien määritys**. Vain seuraavat käyttäjät voivat käyttää sivua:

- **Järjestelmänvalvoja**-rooliin määritetyt käyttäjät.
- Käyttäjät, jotka on liitetty mihin tahansa rooliin, joka on määritetty suorittamaan tehtävä **Aseta käyttöoikeuksia käyttääksesi liiketoiminta-asiakirjamallien muokkausta** (AOT-nimi **ERBDTemplatesSecurity**).

Seuraavia ohjeita noudattamalla voit määrittää yritystiedostojen hallinnan käyttöoikeudet kaikille yrityksille.

1. Kirjaudu sisään käyttäjänä, jolla on **Käyttöoikeuksien määritys** -sivun käyttöoikeus.
2. Siirry kohtaan **Organisaation hallinto** \> **Sähköinen raportointi** \> **Liiketoiminta-asiakirjojen hallinta**\> **Käyttöoikeuksien hallinta**.

    Kiinnitä huomiota ilmoitukseen, jossa kerrotaan, että liiketoimintatiedostojen hallinnan käyttöoikeuksien käyttöä ei ole otettu käyttöön tällä hetkellä.

    ![Liiketoiminta-asiakirjojen hallinnan käyttöoikeuksien määrityssivu.](./media/BDM-Overview-TemplatesAccess1.png)

    Kun tämä asetus on käytössä, kaikki sellaiseen käyttöoikeusrooliin määritetyt käyttäjät, jotka on määritetty suorittamaan tehtävä **Liiketoiminta-asiakirjamallien hallinta** (AOT-nimi **ERBDManageTemplates**), voivat avata yritysasiakirjan hallinnan työtilan ja muokata mitä tahansa käytettävissä olevaa mallia.

    Seuraavassa kuvassa näkyy, mitä yritysasiakirjan hallinnan työtilassa on käytettävissä **Myyntireskontranhoitaja**-rooliin määritetyille käyttäjille. Nykyisten käyttöoikeuksien asetuksen avulla käyttäjä voi muokata eri toimintoalueista peräisin olevia liiketoiminta-asiakirjamalleja, kuten laskutusta, viranomaisraportointia ja maksuja.

    ![Myyntireskontran käsittelijän liiketoiminta-asiakirjojen hallinnan työtilan sivu.](./media/BDM-Overview-TemplatesForAlice1.png)

3. Valitse **Käyttöoikeuksien määritys** -sivulla **Käyttöoikeuksien asetukset**.
4. Ota **Mallien muokkauksen käyttöoikeuksien asetukset** -valintaikkunassa käyttöön **Ota määritetyt käyttöoikeudet käyttöön** -vaihtoehto.
5. Vahvista , että yritysasiakirjan hallinnan käyttöoikeudet on otettu käyttöön valitsemalla **OK**.

    ![Liiketoiminta-asiakirjojen hallinnan käyttöoikeuksien vahvistaminen.](./media/BDM-Overview-TemplatesAccess2.png)

6. Valitse **Lisää**, jos haluat määrittää uuden liiketoimintaroolin, jonka käyttöoikeuksia yritysasiakirjan hallinnan malleihin on määritettävä.
7. Valitse **Käyttöoikeusroolit** -valintaikkunassa **Myyntireskontranhoitaja**-rooli ja vahvista roolin valinta valitsemalla **OK**.
8. Valitse **Määritystunnistekohtaiset käyttöoikeudet** -välilehdessä **Uusi**.
9. Valitse **Tunnisteen tyyppi** -kentässä **Toiminnallinen alue** ja valitse **Tunnus**-kentästä **Laskutus**.
10. Valitse **Tallenna**, jos haluat tallentaa valitun roolin määritetyt käyttöoikeudet.

    Nykyiset asetukset tarkoittavat sitä, että kaikille käyttäjille, jotka on liitetty **Myyntireskontranhoitaja**-rooliin ja jotka suorittavat tehtävän **Liiketoiminta-asiakirjamallien hallinta** (AOT-nimi **ERBDManageTemplates**), ER-muotokonfigurointimallit, joiden **Toiminnallinen alue** -tunnisteen arvo on **Laskutus**, ovat käytettävissä muokattavaksi yritysasiakirjan hallinnan työtilassa.

11. Vaihda **Aiheeseen liittyviä tietoja** -ruutu nykyisen sivun oikeasta reunasta. **Aiheeseen liittyviä tietoja** -ruudussa näkyy, miten konfiguroituja käyttöoikeuksia käytetään, mukaan lukien se, mitä ER-konfigurointimalleja **Myyntireskontranhoitaja**-rooliin määritetyt käyttäjät voivat käyttää.

    ![Käyttöoikeuksien määrityssivun liittyvien tietojen ruutu.](./media/BDM-Overview-TemplatesAccess3.png)

12. Valitse **Määrityskohtaiset käyttöoikeudet** -välilehdessä **Lisää**.
13. Merkitse **Valitse määritys** -valintaikkunassa ER-muotokonfiguraatio **Intrastat-raportti**.
14. Vahvista valittujen konfiguraatioiden määritys valitsemalla **OK** ja tallenna valitun roolin määritetyt käyttöoikeudet valitsemalla **Tallenna**.

Nykyiset asetukset tarkoittavat sitä, että kaikille käyttäjille, jotka on liitetty **Myyntireskontranhoitaja**-rooliin ja jotka suorittavat tehtävän **Liiketoiminta-asiakirjamallien hallinta** (AOT-nimi **ERBDManageTemplates**), seuraavat mallit ovat käytettävissä muokattavaksi yritysasiakirjan hallinnan työtilassa:

- Mallit, joiden **Toiminnallinen alue** -tunnisteen arvo on **Laskutus**.
- Mallit ER-muotokonfiguraatioista, jotka on lueteltu **Määrityskohtaiset käyttöoikeudet** -välilehdessä (mallit **Intrastat-raportti** -muotokokoonpanosta **Lakisääteinen raportointi** -toimialueella tässä esimerkissä).

![Käyttöoikeuksien pikavälilehdet käyttöoikeuksien määrityssivulla.](./media/BDM-Overview-TemplatesAccess4.png)

Seuraavassa kuvassa näkyy, mitä yritysasiakirjan hallinnan työtilassa on saatavilla **Myyntireskontranhoitaja**-rooliin määritetyille käyttäjille. Nykyisen yritysasiakirjan hallinnan käyttöoikeuksien asetuksen avulla käyttäjä voi muokata liiketoiminta-asiakirjamalleja **Laskutus**-toimialueelta ja **Intrastat-raportti** -muotokonfiguraatiosta. **Maksu**-toimialueen mallit eivät ole käytettävissä **Myyntireskontranhoitaja**-roolille.

![Liiketoiminta-asiakirjamallien muokkaaminen Liiketoiminta-asiakirjojen hallinnan työtila -sivulla.](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> **Määrityskohtaiset käyttöoikeudet** -säännöt tallennetaan käyttämällä ER-muotokonfiguraation yksilöivää tunnusta. Tämä tarkoittaa, että näitä sääntöjä ei poisteta, kun niihin viittaava ER-konfiguraatio poistetaan. Kun tuot poistetut konfiguraatiot takaisin tähän esiintymään, nämä säännöt viittaavat niihin uudelleen. Sääntöjä ei tarvitse määrittää uudelleen poistettujen konfiguraatioiden tuomisen jälkeen.

## <a name="use-business-document-management-to-edit-templates"></a>Mallien muokkaaminen yritystiedostojen hallinnan avulla

Yrityskäyttäjät voivat käyttää yrityksen asiakirjamalleja muokkausta varten liiketoiminnan asiakirjanhallinnan työtilassa. Vain seuraavat käyttäjät voivat käyttää liiketoiminta-asiakirjan hallinnan työtilaa:

- **Järjestelmänvalvoja**-rooliin määritetyt käyttäjät.
- Käyttäjät, jotka on määritetty rooliin, joka pystyy suorittamaan toiminnon **Liiketoiminta-asiakirjamallien hallinta** (AOT-nimi **ERBDManageTemplates**).

Seuraavia ohjeita noudattamalla voit muokata vapaatekstilaskun malleja yritysasiakirjanhallinnan työtilassa. Ennen kuin suoritat nämä toimet, tämän ohje aiheen kaikki edellä mainitut toimenpiteet on suoritettava loppuun.

1. Kirjaudu sisään käyttäjänä, jolla on Liiketoiminta-asiakirjan hallintatyötilan käyttöoikeus.
2. Avaa liiketoiminta-asiakirjojen hallinnan työtila.

Kun työasiakirjan hallintatoiminnon **Yrityksen asiakirjanhallinnan Officen kaltainen käyttökokemus** on poistettu käytöstä **Ominaisuuksien hallinta** -työtilassa, **Yrityksen asiakirjanhallinnan** työtilan pääruudukkona näkyvät seuraavat mallit:

- Mallit, joiden omistaja on ER-määrityksen toimittaja (eli toimittaja, joka on tällä hetkellä merkitty aktiiviseksi **Sähköinen raportointi** -työtilassa). Kun olet valinnut jonkin näistä malleista, voit aloittaa tai jatkaa muokkaamista valitsemalla **Muokkaa mallia**.
- Muiden ER-määritysten toimittajien omistamat mallit. Kun olet valinnut jonkin näistä malleista, voit valita **Uuden tiedoston** ja luoda siitä kopion, jonka omistaa ER-määrityspalvelu, ja aloittaa sitten kopion muokkaamisen.

![Malliluettelo Liiketoiminta-asiakirjojen hallinnan työtila -sivulla.](./media/BDM-Overview-EditingTemplate1.png)

**Malli** -välilehdessä näkyy valitun mallin sisältö. Valitse **Tiedot**-välilehti, jossa voit tarkastella valitun mallin tietoja sekä sen ER-muotokonfiguraation tietoja, jossa tämä malli sijaitsee. Huomaa, että kaikkien mallien tila on **Julkaistu**, eivätkä ne sisällä tietoja **Tarkistusversio**-sarakkeessa. Tämä tarkoittaa, että näitä malleja ei tällä hetkellä muokata.

Kun **Työasiakirjan hallinta -toiminnon toimiston kaltainen käyttöliittymä** on otettu käyttöön **Ominaisuuksien hallinta** -työtilassa, **yrityksen asiakirjanhallinnan** työtilan pääruudukko näyttää ne mallit, jotka ovat ER-määrityksen toimittajan omistamia (eli palvelu, joka on tällä hetkellä merkitty aktiiviseksi **sähköisen raportoinnin** työtilassa). Kun olet valinnut jonkin näistä malleista, voit aloittaa tai jatkaa muokkaamista valitsemalla **Muokkaa mallia**.

Jos haluat käsitellä muiden ER-määrityksen toimittajien omistamia malleja, valitse **Uusi asiakirja** luodaksesi kopion ER-toimittajan omistamasta mallista. Voit sitten aloittaa kopion muokkaamisen. Katso lisätietoja kohdasta [Uuden asiakirjan käyttöliittymä liiketoiminta-asiakirjan hallinnassa](er-business-document-management-new-template-ui.md).

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Konfigurointipalvelun omistamien mallien muokkauksen aloittaminen

1. Valitse yritysasiakirjan hallinnan työtilassa **Sekkien tulostusmuoto** -malli luettelosta.
2. Valitse **Tiedot**-välilehti.

![Liiketoiminta-asiakirjojen hallinnan työtila -sivun Tiedot-välilehti.](./media/BDM-Overview-EditingTemplate2.png)

**Muokkaa mallia-** vaihtoehto on käytettävissä valitulle mallille. Tämä vaihtoehto on aina käytettävissä mallissa, joka on ER-muotokokoonpanossa, jonka omistaa aktiivinen ER-konfiguraatiopalvelun toimittaja (tässä esimerkissä **Litware, Inc**). Kun **Muokkaa mallia** on valittuna, aiemmin luodun ER-muotokonfiguraation luonnosversion mallia voi muokata.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Muiden palveluiden omistamien mallien muokkauksen aloittaminen

1. Valitse liiketoiminta-asiakirjojen hallinnan työtilassa asiakirja, jota haluat käyttää mallina.

    ![Asiakirjan valitseminen Liiketoiminta-asiakirjojen hallinnan työtila -sivu.](./media/BDM-Overview-EditingTemplate3.png)

2. Valitse **Uusi asiakirja** ja muuta tarvittaessa muokattavan mallin otsikkoa **Otsikko**-kentässä. Tekstin avulla voit nimetä automaattisesti luotavan ER-muodon konfiguraation. Huomaa, että tämän konfiguraation luonnos (**Asiakkaan FTI-raportti (GER) Copy**), joka sisältää muokatun mallin, merkitään automaattisesti suorittamaan tämä ER-muoto nykyiselle käyttäjälle. Samaan aikaan ER-perusmuotomäärityksen ei-muokattua alkuperäistä mallia käytetään tämän ER-muodon suorittamiseen toiselle käyttäjälle.
3. Vaihda **Nimi** -kenttään automaattisesti luotavan muokattavan mallin ensimmäisen version nimi.
4. Vaihda **Kommentti**-kenttään automaattisesti luotavan muokattavan mallin kommentti.
5. Vahvista muokkausprosessin aloittaminen valitsemalla **OK**.

![Uuden mallin luominen vahvistamalla muokkausprosessin alkaminen.](./media/BDM-Overview-EditingTemplate4.png)

Jos palveluntarjoajaa ei ole, sen luomista tarjotaan. Jos aktiivista toimittajaa ei ole, se voidaan valita aktivoitavaksi.

Jos haluat luoda tarjoajan, muuta tarjoajan nimi **Nimi**-kentässä, päivitä uuden tarjoajan **Internet-osoite** kenttään ja vahvista valitsemalla **OK**.

   ![Uuden tarjoajan luominen BDM:ssä.](./media/bdm_create_provider.png)

Voit aktivoida aiemmin luodun tarjoajan valitsemalla **Konfigurointipalvelu**-kentästä tarjoajan nimen ja valitsemalla **OK**, jos haluat määrittää tarjoajan aktiiviseksi.

   ![Tarjoajan aktivoiminen BDM:ssä.](./media/bdm_choose_provider.png)

> [!NOTE]
> Kunkin BDM-malli viittaa palveluntarjoajaan kokoonpanon tekijänä. Siksi mallissa tarvitaan aktiivista toimittajaa.


**Uusi tiedosto** -vaihtoehto on aina käytettävissä siinä ER-muotomäärityksen mallissa, jolla ei ole uutta versiota ja jonka toimittaa kulloinenkin ja toinen palvelu (tässä esimerkissä Microsoft). Muokattu malli tallennetaan sen jälkeen uuteen ER-muotokonfiguraatioon, joka luodaan automaattisesti.



### <a name="start-editing-a-template"></a>Aloita mallin muokkaus

1. Valitse valitusta mallista **Muokkaa tiedostoa**.
2. Vaihda **Nimi** -kenttään automaattisesti luotavan muokattavan mallin ensimmäisen version nimi.
3. Vaihda **Kommentti**-kenttään automaattisesti luotavan muokattavan mallin huomautus.

    ![Mallin muokkaaminen Liiketoiminta-asiakirjojen hallinnan työtila -sivulla.](./media/BDM-Overview-EditingTemplate5.png)

4. Vahvista muokkausprosessin aloittaminen valitsemalla **OK**.

**BDM-mallieditori**-sivu avautuu. Valittu malli on käytettävissä online-muokkausta varten käyttämällä Microsoft 365:tä.

![Liiketoiminta-asiakirjojen hallinnan mallieditori -sivu.](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-microsoft-365"></a><a name="EditInOffice365"></a>Mallin muokkaaminen Microsoft 365:ssä

Voit muokkaa mallia Microsoft 365:ssä. Esimerkiksi Office Onlinessa voit muuttaa mallin otsikossa olevien kenttä kehotteiden fonttia arvosta **Normaali** arvoon **Lihavoitu**. Nämä muutokset tallentuvat automaattisesti muokattavaan malliin, joka on tallennettu ensisijaisen perusmallin tallennustilaan (oletusarvona on Azuren blob-säilö). Tämä on määritetty ER-kehykselle.

![Mallin otsikon fontin muuttaminen lihavoiduksi Liiketoiminta-asiakirjojen hallinnan mallieditori -sivulla.](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a><a name="EditInOfficeDesktopApp"></a>Mallin muokkaaminen Office-työpöytäsovelluksessa

> [!NOTE]
> Tämä toiminto on käytettävissä vain, kun **SharePoint -asiakirjatyyppi** -parametri on määritetty oikein. Lisätietoja on kohdassa [Parametrien määrittäminen](#SetupBdmParameters).

1. Valitse **Avaa työpöytäsovelluksessa** -vaihtoehto, jos haluat muokata mallia Office-työpöytäsovelluksen toimintojen avulla (tässä esimerkissä Excel). Muokattava malli kopioidaan pysyvästä tallennuspaikasta yrityksen tiedostojen hallinnan parametreissa määritettyyn väliaikaiseen varastoon SharePoint-kansiona.
2. Vahvista, että haluat avata mallin väliaikaisesta tiedostovarastoinnista Officen Excel -työpöytäsovelluksessa.

    ![Excel-työpöytäsovelluksessa avattu malli.](./media/BDM-Overview-EditingLayout3.png)

3. Muokkaa mallia. Esimerkiksi voit muuttaa mallin otsikossa olevien kenttäkehotteiden fonttia päivittämällä värin arvosta **Musta** arvoon **Sininen**.

    ![Mallin otsikon fontin värin muokkaaminen Excel-työpöytäsovelluksessa.](./media/BDM-Overview-EditingLayout4.png)

4. Tallenna mallin muutokset väliaikaiseen varastoon valitsemalla Excel-työpöytäsovelluksessa **Tallenna**.

    ![Muutosten tallentaminen Liiketoiminta-asiakirjojen hallinnan mallieditori -sivulla Excel-työpöytäsovelluksessa.](./media/BDM-Overview-EditingLayout5.png)

5. Sulje Excel-työpöytäsovellus.
6. Synkronoi väliaikainen mallisäilö pysyvään mallivarastoon valitsemalla **Synkronoi tallennettu kopio**.

> [!NOTE]
> Väliaikaisen tiedostovaraston muokattavan mallin kopio säilytetään vain nykyisessä mallinmuokkausistunnossa. Kun lopetat tämän istunnon sulkemalla **BDM-mallieditorin** sivun, tämä kopio poistetaan. Jos olet säätänyt mallin väliaikaisessa tiedostotallennuksessa etkä valinnut **Synkronoi tallennettu kopio** -vaihtoehtoa, kun yrität sulkea **BDM-mallieditori** -sivun, näyttöön tulee sanoma, jossa kysytään, haluatko tallentaa tehdyt muutokset. Valitse **kyllä**, jos haluat tallentaa malliin tekemäsi muutokset pysyvään tiedostosijaintiin.

### <a name="validate-a-template"></a>Tarkista malli

1. Valitse **BDM-mallieditorin** sivulla **Tarkista ongelmat** vahvitaaksesi muokatun mallin suhteessa pohjana olevaan ER-muotokonfiguraatioon. Noudata suosituksia (jos sellaisia on), jos haluat yhtenäistää mallin ER-perusmuotokonfiguraation muodon rakenteen kanssa.
2. Valitse **Näytä muoto**, jos haluat tarkastella muodon nykyistä rakennetta ER-perusmuotomäärityksistä, joka on yhdenmukaistettava muokattavan mallin kanssa. 
3. Voit sulkea ruudun valitsemalla **Piilota muoto**.

    ![BDM-mallieditorin sivu.](./media/BDM-Overview-EditingTemplate6.png)

4. Sulje **BDM-mallieditorin** sivu.

Päivitetty malli näkyy **Malli**-välilehdessä. Huomaa, että muokatun mallin tila on nyt **Luonnos** eikä nykyinen versio ole enää tyhjä. Tämä tarkoittaa, että tämän mallin muokkauksen prosessi on aloitettu.

![Päivitetyn mallin näyttäminen Liiketoiminta-asiakirjojen hallinnan työtila -sivulla.](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Muokatun mallin testaaminen 

1. Vaihda sovelluksessa yritykseen **USMF**.
2. Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.
3. Valitse **FTI-00000002** -lasku ja valitse sitten **Tulostuksenhallinta**.
4. Valitse **Moduuli - Myyntireskontra** \> **Tiedostot** \> **Vapaatekstilasku** \> **Alkuperäinen tiedosto** -taso määrittääksesi käsiteltävien laskujen vaikutusalueen.
5. Valitse **Raportin muoto** -kentästä **Asiakkaan FTI-raportti (GER) Copy** -ER-muoto määritetylle tiedostotasolle.

    ![Tulostuksenhallinnan asetukset -sivu.](./media/BDM-Overview-TestRun1.png)

6. Voit sulkea nykyisen sivun painamalla **ESC-näppäintä**.
7. Valitse ensin **Tulosta** ja sitten **Valittu**.
8. Lataa tiedosto ja avaa se käyttämällä Excel-työpöytäsovellusta.

![Vapaatekstilaskut-sivu.](./media/BDM-Overview-TestRun2.png)

Muokatun mallin avulla luodaan valitulle nimikkeelle vapaatekstilaskun raportti. Jos haluat analysoida, miten malliin tekemäsi muutokset vaikuttavat tähän raporttiin, voit suorittaa tämän raportin yhdessä sovellusistunnossa suoraan sen jälkeen, kun olet muokannut mallia toisessa sovellusistunnossa.

### <a name="create-an-alternative-template-revision"></a>Vaihtoehtoisen malliversion luominen

1. Avaa **BDM-mallieditorib** sivu ja valitse **Asiakkaan FTI-raportti (GER) Copy** -malli.
2. Valitse **Versiot**-välilehdestä **Uusi**.
3. Muuta tarvittaessa toisen version nimeä **Nimi** -kentässä ja perusta se tällä hetkellä aktiiviselle ensimmäiselle versiolle.
4. Vaihda **Kommentti**-kenttään automaattisesti luotavan muokattavan mallin huomautus tarvittaessa.

    ![Mallin versioiden luominen Liiketoiminta-asiakirjojen hallinnan työtila -sivulla.](./media/BDM-Overview-AddRevision.png)

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

![Mallin muutosten hylkääminen Liiketoiminta-asiakirjojen hallinnan työtila -sivulla.](./media/BDM-Overview-RevokeChanges.png)

1. Valitse **Malli**-välilehti **BDM mallieditorin** sivulla.
2. Valitse **Kumoa**.
3. Jos valitset **OK** peruuttaaksesi malliin tehdyt muutokset, muokattu malli korvataan alkuperäisellä mallilla ja kaikki muutokset poistetaan. Kun peruutat malliin tehdyt muutokset, voit poistaa mallin. Voit tutkia muita vaihtoehtoja valitsemalla **Peruuta**.

### <a name="publish-a-modified-template"></a>Muokatun mallin julkaiseminen

1. Valitse **BDM mallieditorin** sivun **Malli**-välilehdessä **Julkaise**.
2. Jos valitset **OK** julkaisun vahvistamiseksi, muutetun mallin sisältävä **Asiakkaan FTI-raportti (GER) Copy** -ER-muodon johdettu luonnos merkitään valmiiksi. Muokattu malli tulee muiden käyttäjien saataville. Tämän ER-muodon valmiit versiot säilyttävät vain mallin viimeisimmän aktiivisen version. Muut versiot poistetaan. Voit tutkia muita vaihtoehtoja valitsemalla **Peruuta**.

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

### <a name="i-selected-edit-document-but-instead-of-going-to-the-bdm-template-editor-page-in-finance-i-was-sent-to-the-microsoft-365-webpage"></a>Valitsin Muokkaa tiedostoa, mutta sen sijaan että BDM-mallieditorisivu avautuisi Financessa, siirryin Microsoft 365 -verkkosivulle.

Tämä on tunnettu Microsoft 365:n uudelleenohjauksen ongelma. Näin tapahtuu, kun Microsoft 365:een kirjaudutaan ensimmäisen kerran. Tämän ongelman voi korjata palaamalla edelliselle sivulle valitsemalla selaimessa **Edellinen**.

### <a name="i-understand-how-to-edit-a-template-by-using-microsoft-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-and-adjust-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-use-the-office-desktop-application-in-the-same-way"></a>Ymmärrän, miten voit muokata mallia käyttämällä Microsoft 365:tä ensimmäisessä sovellusistunnossa ja miten mallia käytetään toisessa sovellusistunnossa ja mallin säätämiseen, jotta näen, miten muutokset vaikuttavat luotuun liiketoiminta-asiakirjaan. Voiko Office-työpöytäsovellusta käyttää samalla tavalla?

Kyllä voit. Valitse ensimmäisessä sovellusistunnossa **Avaa työpöytäsovelluksessa**. Malli tallennetaan väliaikaiseen tiedostovarastoon ja avataan Office-työpöytäsovelluksessa. Tee seuraavaksi seuraavat vaiheet, kun haluat esikatsella mallin muutoksia luodussa yritysasiakirjassa:

1. Tee muutoksia malliin käyttämällä Office-työpöytäsovellusta.
2. Valitse Office-työpöytäsovelluksessa **Tallenna**.
3. Valitse ensimmäisen sovellusistunnon **BDM-mallieditorin** sivulla **Synkronoi tallennettu kopio**.
4. Suorita tämä mallin ER-muoto toisessa sovellusistunnossa.

### <a name="when-i-select-open-in-desktop-app-i-receive-the-following-error-message-value-cannot-be-null-parameter-name-externalid-how-do-i-work-around-this-issue"></a>Sen jälkeen kun Avaa työpöytäsovelluksessa on valittu, seuraava virhesanoma avautuu: Arvo ei voi olla tyhjäarvo. Parametrin nimi: externalId. Miten tämä ongelma ratkaistaan?

Kirjauduit todennäköisesti Azure AD -toimialueen nykyisen sovelluksen esiintymään, joka ei ole sama kuin esiintymän käyttöönotossa käytetty Azure AD -toimialue. Koska SharePoint-palvelu, johon tallennetaan malleja, joiden avulla niitä voidaan muokata Office-työpöytäsovelluksella, kuuluu samaan toimialueeseen, meillä ei ole SharePoint-palvelun käyttöoikeuksia. Voit ratkaista tämän ongelman kirjautumalla nykyiseen esiintymään käyttämällä oikean Azure AD -toimialueen käyttäjän tunnistetietoja.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)

[ER OPENXML-muodossa luotavien raporttien määritysten suunnittelu (marraskuu 2016)](tasks/er-design-reports-openxml-2016-11.md)

[Suunnittele ER-konfiguraatiot voidaksesi luoda raportteja Word-muodossa](tasks/er-design-configuration-word-2016-11.md)

[Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md)

[Sähköisen raportoinnin (ER) määrittäminen hakemaan tiedot Power BI:hin](general-electronic-reporting-report-configuration-get-data-powerbi.md)

## <a name="list-of-er-configurations-that-have-been-released-in-finance-to-support-configurable-business-documents"></a><a name="list-of-configurations-cbd"></a>Luettelo Financessa julkaistuista määritettäviä liiketoiminta-asiakirjoja tukevista ER-määrityksistä

Financen ER-määritysten [luetteloa](general-electronic-reporting.md#list-of-configurations) päivitetään jatkuvasti. Tällä hetkellä tuettujen ER-määritysten luetteloa voi tarkastella avaamalla [yleisen tietovaraston](er-download-configurations-global-repo.md). Yleinen tietovarasto voidaan [suodattaa](../../../finance/localizations/enhanced-filtering-global-repo.md) näyttämään luettelo määritettäviä liiketoiminta-asiakirjoja tukevista ER-määrityksistä.

![Yleisen tietovaraston sisällön suodattaminen Konfiguraatiosäilö-sivulla.](./media/bdm-overview-filterglobalrepo.gif)

Seuraavassa taulukossa on luettelo ER-määrityksistä, jotka tukevat määritettäviä liiketoiminta-asiakirjoja ja jotka on julkaistu Financessa joulukuuhun 2020 mennessä.

| Tietomallimääritys    | Muotomääritykset                           |
|-----------------------------|-------------------------------------------------|
| Rahtikirjamalli        | Rahtikirja (Excel)                          |
|                             | Rahtikirja (Word)                           |
| Alkuperätodistusmalli | Alkuperätodistus (Excel)                   |
|                             | Alkuperätodistus (Word)                    |
| Laskumalli               | Asiakkaan veloitus- ja hyvityslasku (Excel)          |
|                             | Asiakkaan veloitus- ja hyvityslasku (Word)           |
|                             | Vapaatekstilasku (Excel)                       |
|                             | Vapaatekstilasku (Excel) (BH)                  |
|                             | Vapaatekstilasku (FR) (Excel)                  |
|                             | Vapaatekstilasku (LT) (Excel)                  |
|                             | Vapaatekstilasku (LV) (Excel)                  |
|                             | Vapaatekstilasku (PL) (Excel)                  |
|                             | Vapaatekstilasku (CZ) (Excel)                  |
|                             | Vapaatekstilasku (EE) (Excel)                  |
|                             | Vapaatekstilasku (HU) (Excel)                  |
|                             | Vapaatekstilasku (TH) (Excel)                  |
|                             | Vapaatekstilasku (Word)                        |
|                             | Projektisopimuksen rivinimikkeet (Excel)             |
|                             | Projektisopimuksen rivinimikkeet (CZ) (Excel)        |
|                             | Projektisopimuksen rivinimikkeet (Excel) (BH)        |
|                             | Projektisopimuksen rivinimikkeet (HU) (Excel)        |
|                             | Projektisopimuksen rivinimikkeet (LT) (Excel)        |
|                             | Projektisopimuksen rivinimikkeet (PL) (Excel)        |
|                             | Projektisopimuksen rivinimikkeet (Word)              |
|                             | Projektiasiakkaan pidätyksen vapautus (Excel)      |
|                             | Projektiasiakkaan pidätyksen vapautus (CZ) (Excel) |
|                             | Projektiasiakkaan pidätyksen vapautus (HU) (Excel) |
|                             | Projektiasiakkaan pidätyksen vapautus (LT) (Excel) |
|                             | Projektiasiakkaan pidätyksen vapautus (PL) (Excel) |
|                             | Projektiasiakkaan pidätyksen vapautus (TH) (Excel) |
|                             | Projektiasiakkaan pidätyksen vapautus (Word)       |
|                             | Projektilasku (Excel)                         |
|                             | Projektilasku (Word)                          |
|                             | Projektilasku (AE) (Excel)                    |
|                             | Projektilasku (CZ) (Excel)                    |
|                             | Projektilasku (Excel) (BH)                    |
|                             | Projektilasku (HU) (Excel)                    |
|                             | Projektilasku (JP) (Excel)                    |
|                             | Projektilasku (LT) (Excel)                    |
|                             | Projektilasku (PL) (Excel)                    |
|                             | Projektilasku (TH) (Excel)                    |
|                             | Täydellinen projektilasku (OMA) (Excel)               |
|                             | Yksinkertainen projektilasku (OMA) (Excel)             |
|                             | Projektinhallintalasku (LT) (Excel)                  |
|                             | Projektinhallintalasku (CZ) (Excel)             |
|                             | Projektinhallintalasku (Excel) (BH)             |
|                             | Projektinhallintalasku (HU) (Excel)             |
|                             | Projektinhallintalasku (JP) (Excel)             |
|                             | Projektinhallintalasku (LT) (Excel)             |
|                             | Projektinhallintalasku (PL) (Excel)             |
|                             | Projektinhallintalasku (Word)                   |
|                             | Oston ennakkomaksun lasku (Excel)                |
|                             | Oston ennakkomaksun lasku (Word)                 |
|                             | Myynnin ennakkomaksun lasku (Excel)                   |
|                             | Myynnin ennakkomaksun lasku (Word)                    |
|                             | Myynnin ennakkomaksun lasku (PL) (Excel)              |
|                             | Myyntilasku (Excel)                           |
|                             | Myyntilasku (Excel) (BH)                      |
|                             | Myyntilasku (Excel) (CZ)                      |
|                             | Myyntilasku (Excel) (EE)                      |
|                             | Myyntilasku (Excel) (FR)                      |
|                             | Myyntilasku (Excel) (HU)                      |
|                             | Myyntilasku (Excel) (IN)                      |
|                             | Myyntilasku (Excel) (LT)                      |
|                             | Myyntilasku (Excel) (LV)                      |
|                             | Myyntilasku (Excel) (PL)                      |
|                             | Myyntilasku (Excel) (TH)                      |
|                             | Myyntilasku (Word)                            |
|                             | TMS-kauppalasku (Excel)                  |
|                             | TMS-kauppalasku (Word)                   |
|                             | Toimittajan laskuasiakirja (Excel)                 |
|                             | Toimittajan laskuasiakirja (CZ) (Excel)            |
|                             | Toimittajan laskuasiakirja (HU) (Excel)            |
|                             | Toimittajan laskuasiakirja (IN) (Excel)            |
|                             | Toimittajan laskuasiakirja (LT) (Excel)            |
|                             | Toimittajan laskuasiakirja (LV) (Excel)            |
|                             | Toimittajan laskuasiakirja (OMA) (Excel)            |
|                             | Toimittajan laskuasiakirja (Word)                  |
| Tilausmalli                 | Sopimuksen vahvistus (Excel)                  |
|                             | Sopimuksen vahvistus (Word)                   |
|                             | Ostosopimuksen vahvistus (Excel)         |
|                             | Ostosopimuksen vahvistus (Word)          |
|                             | Ostotilaus (Excel)                          |
|                             | Ostotilaus (CZ) (Excel)                     |
|                             | Ostotilauskysely (CZ) (Excel)             |
|                             | Ostotilaus (HU) (Excel)                     |
|                             | Ostotilauskysely (HU) (Excel)             |
|                             | Ostotilaus (Word)                           |
|                             | Ostotilauskysely (Excel)                  |
|                             | Ostotilauskysely (Word)                   |
|                             | Myyntitilauksen vahvistus (Excel)                |
|                             | Myyntitilauksen vahvistus (CZ) (Excel)           |
|                             | Myyntitilauksen vahvistus (HU) (Excel)           |
|                             | Myyntitilauksen vahvistus (Word)                 |
| Pakkausluettelomalli          | Säilön sisältö (Excel)                      |
|                             | Säilön sisältö (Word)                       |
|                             | Kuormaluettelo (Excel)                               |
|                             | Kuormaluettelo (Word)                                |
|                             | Keräysluettelo (Excel)                            |
|                             | Keräysluettelo (CZ) (Excel)                       |
|                             | Keräysluettelo (Word)                             |
|                             | Tuotannon keräysluettelo (Excel)                    |
|                             | Tuotannon keräysluettelo (Word)                     |
|                             | Lähetyksen keräysluettelo kuormaa varten (Excel)             |
|                             | Lähetyksen keräysluettelo kuormaa varten (Word)              |
|                             | Lähetyksen keräysluettelo lähetystä varten (Excel)         |
|                             | Lähetyksen keräysluettelo lähetystä varten (Word)          |
|                             | Lähetyksen keräysluettelo aaltoa varten (Excel)             |
|                             | Lähetyksen keräysluettelo aaltoa varten (Word)              |
| Maksumalli               | Asiakkaan maksuehdotus (Excel)                 |
|                             | Asiakkaan maksuehdotus (Word)                  |
|                             | Toimittajan maksuehdotus (Excel)                   |
|                             | Toimittajan maksuehdotus (Word)                    |
| Tarjousmalli             | Projektitarjous (Excel)                       |
|                             | Projektitarjous (Word)                        |
|                             | Tarjouspyyntö (Excel)                   |
|                             | Tarjouspyyntö (hyväksyntä) (Excel)          |
|                             | Tarjouspyyntö (hyväksyntä) (Word)           |
|                             | Tarjouspyyntö (hylkäys) (Excel)          |
|                             | Tarjouspyyntö (hylkäys) (Word)           |
|                             | Tarjouspyyntö (palautus) (Excel)          |
|                             | Tarjouspyyntö (palautus) (Word)           |
|                             | Tarjouspyyntö (Word)                    |
|                             | Myyntitarjous (Excel)                         |
|                             | Myyntitarjous (CZ) (Excel)                    |
|                             | Myyntitarjous (HU) (Excel)                    |
|                             | Myyntitarjous (Word)                          |
|                             | Myyntitarjouksen vahvistus (Excel)            |
|                             | Myyntitarjouksen vahvistus (Word)             |
| Täsmäytysmalli        | Asiakkaan tiliote, ulkoinen (Excel)             |
|                             | Asiakkaan tiliote, ulkoinen (CN) (Excel)        |
|                             | Asiakkaan tiliote, ulkoinen (Word)              |
|                             | Asiakkaan tiliote, Ranska (Excel)          |
| Muistutusmalli              | Maksukehotus (Excel)                  |
|                             | Maksukehotus (CN) (Excel)             |
|                             | Maksukehotus (Word)                   |
|                             | Asiakkaan korkolasku (Excel)                  |
|                             | Asiakkaan korkolasku (Word)                   |
| Kuormakirjamalli               | Kuorman maksuväline (Excel)                             |
|                             | Kuorman maksuväline (Word)                              |
|                             | Ostotilauksen pakkausluettelo (Excel)             |
|                             | Ostotilauksen pakkausluettelo (CZ) (Excel)        |
|                             | Ostotilauksen pakkausluettelo (Word)              |
|                             | Reititys (Excel)                                   |
|                             | Reititys (Word)                                    |
|                             | Myyntitilauksen pakkausluettelo (Excel)                |
|                             | Myyntitilauksen pakkausluettelo (CZ) (Excel)           |
|                             | Myyntitilauksen pakkausluettelo (LT) (Excel)           |
|                             | Myyntitilauksen pakkausluettelo (PL) (Excel)           |
|                             | Myyntitilauksen pakkausluettelo (Word)                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
