---
title: Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi
description: Tässä ohjeaiheessa on tietoja suorituskykyongelmien vianmäärityksestä sähköisen raportoinnin (ER) suorituskyvyn jäljitystoiminnon avulla.
author: NickSelin
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6585e44701160bf31c107c07226f992b12cf035e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550645"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi

[!include[banner](../includes/banner.md)]

Osana sähköisten raportointikonfiguraatioiden suunnittelua sähköisten asiakirjojen luomista varten määritetään menetelmä, jonka avulla tiedot haetaan sovelluksesta ja syötetään luotavaan tuotokseen. ER Performance Trace -toiminto auttaa vähentämään huomattavasti aikaa ja kustannuksia, jotka liittyvät ER-muodon suorituksen yksityiskohtien keräämiseen ja niiden käyttämiseen suorituskykyongelmien vianmäärityksessä. Tässä opetusohjelmassa on ohjeita siitä, miten suorituskykyä voidaan seurata suoritettavissa ER-muodoissa ja miten suorituskykyä voidaan parantaa näiden jälkien tietojen avulla.

## <a name="prerequisites"></a>Edellytykset

Tämän opetusohjelman esimerkkien suorittaminen edellyttää seuraavia käyttöoikeuksia:

- Jonkin seuraavien roolien käyttöoikeus:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

- Käyttöoikeus Regulatory Configuration Services (RCS) -esiintymään, joka on valmisteltu samalle vuokralaiselle kuin sovellus, jollekin seuraavista rooleista:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

Seuraavat tiedostot täytyy myös ladata ja tallentaa paikallisesti.

| Tiedosto                                  | Sisältö                               |
|---------------------------------------|---------------------------------------|
| Suorituskyvyn jäljitysmalli.versio.1     | [Esimerkin ER-tietomallin konfigurointi](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| Suorituskyvyn jäljitysmetadata.versio.1  | [Esimerkin ER-metadatan konfigurointi](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| Suorituskyvyn jäljitysmapping.versio.1 | [Esimerkin ER-mallikartoituksen konfigurointi](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Suorituskyvyn jäljitysformat.versio.1  | [Esimerkin ER-format-konfigurointi](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a>Konfiguroi ER-parametrit

Jokainen sovelluksessa luotu ER-suorituskykyjäljitys tallennetaan suorituslokitietueen liitteenä. Näiden liitteiden hallinnassa käytetään tiedostojen hallinnan (DM) kehystä. Sinun on määritettävä ER-parametrit etukäteen ja määritettävä DM-tiedosto tyyppi, jota käytetään suorituskykyjälkien liittämiseen. Valitse **Sähköinen raportointi** -työtilasta **Sähköisen raportoinnin parametrit**. Valitse sitten **Sähköisen raportoinnin parametrit** -sivun **Liitteet**-välilehden **Muut**-kentästä suorituskyvyn jäljille käytettävä DM-tiedostotyyppi.

![Sähköisen raportoinnin parametrit -sivu](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

Jos haluat olla käytettävissä **Muut** -hakukentässä, DM-tiedostotyyppi on konfiguroitava seuraavalla tavalla **Asiakirjatyypit**-sivulla (**Organisaation hallinta \> Asiakirjan hallinta \> Asiakirjatyypit**):

- **Luokka:** Liitä tiedosto
- **Ryhmä:** Tiedosto

![Asiakirjatyypit-sivu](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> Valitun tiedostotyypin on oltava käytettävissä kaikissa nykyisen esiintymän yrityksissä, koska DM-liitteet ovat yrityskohtaisia.

### <a name="configure-rcs-parameters"></a>Konfiguroi RCS-parametrit

Luodut ER-suorituskykyjäljet tuodaan RCS:ään analysointia varten käyttämällä ER Format Designeria ja ER Mapping Designeria. Koska ER-suorituskykyjäljet tallennetaan ER-muotoon liittyvän suorituslokitietueen liitteinä, RCS-parametrit on määritettävä etukäteen, jotta voidaan määrittää DM-tiedostotyyppi, jota käytetään suorituskykyjälkien liittämiseen. Valitse yrityksellesi määritetyn RCS-esiintymän **Sähköisen raportoinnin** -työtilassa **Sähköiset raportointiparametrit**. Valitse sitten **Sähköisen raportoinnin parametrit** -sivun **Liitteet**-välilehden **Muut**-kentästä suorituskyvyn jäljille käytettävä DM-tiedostotyyppi.

![Sähköisen raportoinnin parametrit -sivu RCS:ssä](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

Jos haluat olla käytettävissä **Muut** -hakukentässä, DM-tiedostotyyppi on konfiguroitava seuraavalla tavalla **Asiakirjatyypit**-sivulla (**Organisaation hallinta \> Asiakirjan hallinta \> Asiakirjatyypit**):

- **Luokka:** Liitä tiedosto
- **Ryhmä:** Tiedosto

## <a name="design-an-er-solution"></a>Suunnittele ER-ratkaisu

Oletetaan, että olet aloittanut uuden ER-ratkaisun suunnittelun, joka luo toimittajatapahtumia esittelevän uuden raportin. Tällä hetkellä voit etsiä valitun toimittajan tapahtumat **Toimittajatapahtumat**-sivulta (Siirry **Ostoreskontra \> Toimittajat \> Kaikki toimittajat**, valitse toimittaja ja sitten toimintoruudun **Toimittaja**-välilehti kohdassa valitse **Tapahtumat**-ryhmästä **Tapahtumat**). Haluat kuitenkin saada kaikki toimittajatapahtumat samaan aikaan yhdessä sähköisessä asiakirjassa XML-muodossa. Tämä ratkaisu koostuu useista ER-konfiguraatioista, jotka sisältävät vaaditun tietomallin, metatiedot, mallien yhdistämismääritykset ja muotokomponentit.

1. Kirjaudu yrityksen RCS-esiintymään, joka on valmisteltu yrityksellesi.
2. Tässä opetusohjelmassa luodaan ja muokataan konfiguraatioita malliyritykselle **Litware, Inc.**. Varmista siksi, että tämä konfigurointipalvelu on lisätty RCS-järjestelmään ja valittu aktiiviseksi. Lisätietoja on kohdassa [Luo konfigurointipalvelut ja merkitse ne aktiivisiksi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) menettelyiksi.
3. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.
4. Tuo **Konfiguraatiot** -sivulla lataamasi ER-kokoonpanot RCS-edellytyksenä seuraavassa järjestyksessä: tietomalli, metatiedot, mallikartoitus, muoto. Luo kukin mukautus seuraavasti:

    1. Valitse toimintoruudusta **Vaihda \> Lataa XML-tiedostosta**.
    2. Valitse haluamasi ER-kokoonpanon tiedosto XML-muodossa valitsemalla **Selaa**.
    3. Valitse **OK**.

    ![Konfiguroinnit-sivu RCS:ssä](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>ER-ratkaisun suorittaminen jäljityksen suorittamista varten

Oletetaan, että olet suunnitellut ER-ratkaisun ensimmäisen version. Nyt haluat testata sitä esiintymässäsi ja analysoida suorituskykyä.

### <a id='import-configuration'></a>ER-konfiguraation tuominen RCI:sta Finance and Operationsiin

1. Kirjaudu sisään sovelluksen esiintymään.
2. Tämän opetusohjelman avulla voit tuoda konfiguraatiot RCS-esiintymästäsi (jossa suunnittelet ER-komponentteja) esiintymääsi (jossa testaat ja lopulta käytät niitä). Siksi on varmistettava, että kaikki vaaditut tiedot on valmisteltu. Ohjeita on kohdassa [Sähköisen raportoinnin konfiguraatioiden tuonti Regulatory Configuration Services (RCS) -palvelusta](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).
3. Seuraavien vaiheiden mukaisesti voit tuoda konfiguraatiot RCS:stä sovellukseen:

    1. Valitse **Sähköisen raportoinnin** työtilassa**Litware, Inc**-määrityspalveluruudussa **Arkistot**.
    2. Valitse **Konfiguraatiosäilö**-sivun ruudukossa oleva säilö, jonka tyyppi on **RCS** ja valitse sitten **Avaa**.
    3. Valitse **Konfiguraatiot**-pikavälilehdessä **Suorituskyvyn jäljitysmuodon** konfiguraatio.
    4. Valitse **Versiot**-pikavälilehdellä valitun konfiguraation versio **1.1** ja valitse sitten **Tuo**.

    ![Konfiguraatiosäilön sivu](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

Tietomallin ja mallin yhdistämismääritysten vastaavat versiot tuodaan automaattisesti valmiiksi tuodun ER-muodon konfiguroinnin edellytyksinä.

### <a name="turn-on-the-er-performance-trace"></a>ER-suorituskykyjäljityksen ottaminen käyttöön

1. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. Toimi **Käyttäjäparametrit**-valintaikkunan **Suorituksen jäljitys** -osassa seuraavasti:

    1. Valitse **Suorituksen jäljitys muoto** -kentässä **Korjaa jäljitystiedosto** -kentässä, joka alkaa keräämään tietoja ER-muodon suorittamisesta. Kun tämä arvo valitaan, suorituskyvyn jäljitys kerää seuraaviin toimiin kuluvaa aikaa koskevia tietoja:

        - Kunkin tietolähteen suorittamista mallikartoituksista, joita kutsutaan tietojen hakemiseksi
        - Kunkin muotoilunimikkeen käsitteleminen siten, että se syöttää tietoja luotavalle tulosteelle

        **Suorituksen jäljitysmuoto** -kentän avulla voit määrittää sen luodun suorituskykyjäljityksen muodon, johon suoritustiedot tallennetaan ER-ja Mapping-elementeissä. Kun valitset arvoksi **Virheen korjauksen jäljitysmuodon**, pystyt analysoimaan jäljityksen sisältöä ER Operation Designerissa ja näkemään ER-muodon tai määrityselementit, jotka mainitaan jäljityksessä.

    2. Määritä seuraavat asetukset: **Kyllä**, jos haluat kerätä tarkempia tietoja ER-mallin kartoituksesta ja ER-muotokomponenttien suorittamisesta.

        - **Kyselyn tilastotietojen kerääminen** – Kun tämä vaihtoehto on käytössä, suorituskyvyn jäljitys kerää seuraavat tiedot:

            - Tietolähteiden tekemien kutsujen määrä
            - Tietokantaan lisättyjen toistettujen kutsujen määrä
            - Tietokantakutsujen tekemiseen käytettävien SQL-lauseiden tiedot

        - **Jäljitysvälimuistin käyttäminen** – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja ER-mallikartoituksen välimuistin käytöstä.
        - **Jäljitystietojen käyttö** – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja siitä, kuinka monta käyntiä tietokantaan on tehty tietueluettelotyypin suoritettavissa tietolähteissä.
        - **Jäljitystietojen luettelointi** – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja siitä, kuinka monta käyntiä tietokantaan on tehty tietueluettelotyypin suoritettavissa tietolähteissä.

    > [!NOTE]
    > **Käyttäjäparametrit** -valintaikkunan parametrit koskevat käyttäjää ja nykyistä yritystä.

    ![Käyttäjän parametrit -valintaikkuna](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a>Suorita ER-muoto

1. Valitse **DEMF**-yritys.
2. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
3. Valitse **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn jäljitysmuodon** nimike.
4. Valitse toimintoruudussa **Suorita**.

Huomaa, että luotu tiedosto sisältää tietoja kuuden toimittajan 265-tapahtumista.

## <a name="review-the-execution-trace"></a>Suorituksen jäljityksen tarkasteleminen

### <a id='export-trace'></a>Vie luotu jäljitys sovelluksesta

Suorituskykyjäljet irrotetaan lähde-ER-muodosta, ja ne voidaan sarjoittaa ulkoiseen zip-tiedostoon.

1. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Määritysten virheenkorjauslokit**.
2. Valitse **Sähköisen raportoinnin ajon lokit** -sivun vasemmanpuoleisen ruudun **Konfiguration nimi** -kentässä **Suorituskyvyn jäljitysmuoto** jos haluat löytää lokitiedostot, jotka on luotu **Suoritus kyvyn jäljitysmuodon** konfiguraatiolle.
3. Valitse **Liitteet**-painikkeen sivun oikeassa yläkulmassa (paperiliitinsymboli) tai paina **Ctrl+Shift+A**.

    ![Liitteet-painike Sähköisen raportoinnin ajolokit -sivulla](./media/GER-PerfTrace-GER-DebugLog.png)

4. **Valitse sähköisen raportoinnin ajon lokit** -sivun toimintoruudussa **Avaa**, jos haluat saada suorituskyvyn jäljityksen zip-tiedostona ja tallentaa sen paikallisesti.

    ![Sähköisen raportoinnin ajolokien liitteet](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> Luotu jäljitys viittaa lähde-ER-raporttiin yksilöivän raporttitunnuksen avulla vain **GUID**-muodossa. Muodon versionumerointia ei oteta huomioon.

Huomaa, että suoritetun ER-muodon ja ER-mallikartoituksen muodostaman suorituskyvyn jäljittämisen välinen yhteys perustuu käytössä olevaan juurihakemistoon ja yhteiseen tietomalliin. Muodon versionumerointia ja mallin yhdistämistä ei oteta huomioon. Mallimerkinnän **oletusarvoa mallimerkintää varten** ei myöskään oteta huomioon.

### <a id='import-trace'></a>Tuo tuotettu jälki RCS:ään.

1. Valitse RCS:ssä **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.
2. Laajenna **Konfiguraatiot**-sivun konfiguraatiopuussa **Suorituskyvyn jäljitysmalli** -nimike ja valitse **Suorituskyvyn seurannan muoto** -nimike.
3. Valitse toimintoruudussa **Suunnittelija**.
4. Valitse **Muodon suunnittelija**-sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.
5. Valitse **Suorituskyvyn jäljitystulosten asetukset** -valintaikkunasta **Tuo suorituskyvyn jäljitys**.
6. Valitse **Selaa** valitaksesi aiemmin viemäsi zip-tiedoston.
7. Valitse **OK**.

    ![Suorituskyvyn jäljitystulosten asetukset -valintaikkuna RCS-kohteessa](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>Suorituskyvyn seurannan käyttäminen RCS – Format -suoritusanalyysissä

1. Laajenna kaikkien muotoilukohteiden sisältö valitsemalla **Laajenna/tiivistä**-vaihtoehto **Muodon suunnittelija**-sivulla.

    Huomaa, että joistakin nykyisen muodon kohteista näytetään lisätietoja:

    - Todellinen aika, joka käytettiin tietojen syöttämiseen luotuun tulosteeseen kohteen muotoilun avulla
    - Sama aika ilmaistaan prosentteina kokonaisajasta, joka käytettiin koko tuotoksen tuottamiseen.

    ![Muodon suunnittelutoiminto -sivu RCS:ssä](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. Sulje **Muodon suunnittelutoiminto** -sivu.

### <a id='use-trace'></a>Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys

1. Valitse RCS:ssä **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn jäljitysmääritys** -nimike.
2. Valitse toimintoruudussa **Suunnittelija**.
3. Valitse **Suunnittelu**.
4. Valitse **Mallin määrityssuunnittelija** -sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.
5. Valitse aiemmin tuotu jäljitys.
6. Valitse **OK**.

Huomaa, että joidenkin nykyisen mallimääritysten tietolähdenimikkeiden käytettävissä on uusia tietoja:

- Tietolähteen avulla tietoja haettaessa käytetty todellinen aika
- Sama aika ilmaistaan prosentteina kokonaisajasta, joka käytettiin koko mallin määrityksen suorittamiseen.

Huomaa, että ER ilmoittaa, että nykyisen mallin yhdistämismääritys kopioi tietokantapyynnöt, kun VendTable/\<Relations/VendTrans\_. VendTable AccountNum-tietolähde suoritetaan. Tämä päällekkäisyys johtuu siitä, että toimittajatapahtumien luetteloa kutsutaan kaksi kertaa kutakin iteroitua toimittajatietuetta varten:

- Yksi kutsu tehdään tietomallin kunkin tapahtuman tietojen syöttämiseen määritettyjen sidosten perusteella.
- Yksi kutsu tehdään, kun toimittaja määrittää lasketun määrän tapahtumia toimittajakohtaisesti tietomallissa.

![Virheilmoitus tietokantapyyntöjen kopioista RCS-mallin malli kartoituksen suunnittelusivulla](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

Arvo **\[Q:530\]** ilmaisee, että VendTrans-taulua kutsuttiin 530 kertaa palauttamaan kyseisessä taulussa oleva tietue VendTable/\<Relations/VendTrans. VendTable\_AccountNum-tieto lähteeseen. Arvo **\[530\]** ilmaisee, että VendTable/\<Relations/VendTrans. VendTable\_AccountNum-tietolähdettä kutsuttiin 530 kertaa palaamaan, jolloin tietue palautetaan kyseiseen tietolähteeseen ja sen tiedot syötetään tietomalliin.

Suosittelemme, että käytät VendTable/\<Relations/VendTrans. VendTable\_AccountNum-tietolähteen välimuistia, jotta voit vähentää 265-tapahtumien tietojen saamiseksi tehtyjen kutsujen määrää ja parantaa mallimäärityksen suorituskykyä.

Voi myös olla hyödyllistä vähentää LedgerTransTypeList-tietolähteeseen tehtyjen kutsujen määrää. Tätä tietolähdettä käytetään liittämään kaikki **lLedgerTransType**-luetteloinnin arvot sen otsikkoon. Käyttämällä tätä tietolähdettä voit löytää asianmukaisen tunnisteen ja syöttää sen kunkin toimittajatapahtuman tietomalliin. Tähän tietolähteeseen soitettujen kutsujen määrä (9 027) on melko suuri 265-tapahtumissa.

![Mallin määrityksen suunnittelijasivu RCS:ssä näyttää 9 027 puhelua tietolähteeseen](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Paranna mallin määritystä suorituksen jälkeisten tietojen perusteella

### <a name="modify-the-logic-of-the-model-mapping"></a>Mallin määrityksen logiikan muokkaaminen

1. Seuraavia ohjeita noudattamalla voit käyttää välimuistia, joka estää kaksoissoittoja tietokantaan:

    1. Valitse RCS:ssä **Mallin määrityksen suunnittelu** -sivun **Tietolähteet**-ruudusta **VendTable**-nimike.
    2. Valitse **Välimuisti**.
    3. Laajenna **VendTable**-nimike, laajenna VendTable-tietolähde ( **\<Suhde**-nimike), yksi-moneen-suhteiden luettelo ja valitse **VendTrans.VendTable\_AccountNum**-nimike
    4. Valitse **Välimuisti**.

    ![Asetusten tallentaminen välimuistiin, jotta kaksinkertaiset kutsut voidaan estää](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. Siirrä LedgerTransTypeList-tietolähde VendTable-tietolähteen käyttöalueeseen seuraavasti:

    1. Laajenna **Tietolähdetyypit**-ruudussa **Funktiot**-nimike ja valitse **Laskettu kenttä** -nimike.
    2. Valitse **Tietolähteet**-ruudusta **VendTable**-nimike.
    3. Valitse **Lisää**.
    4. Kirjoita **Nimi**-kenttään **\$TransType**.
    5. Valitse **Muokkaa kaavaa**.
    6. Kirjoita **Kaava**-kenttään **LedgerTransTypeList**.
    7. Valitse **Tallenna**.
    8. Sulje **Kaavaeditori**-sivu.
    9. Valitse **OK**.

3. Suorita **\$TransType**-kentän tallentaminen välimuistiin seuraavien vaiheiden mukaisesti:

    1. Valitse **LedgerTransTypeList**-nimike.
    2. Valitse **Välimuisti**.
    3. Valitse **VendTable.\$TransType**-nimike.
    4. Valitse **Välimuisti**.

    ![$TransType-kentän asetusten tallentaminen välimuistiin](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. Näiden vaiheiden avulla voit muuttaa **\$TransTypeRecord**-kenttää siten, että se alkaa käyttää välimuistissa olevaa **\$TransType**-kenttää:

    1. Laajenna **Tietolähteet**-ruudussa **VendTable**-nimike, laajenna **\<Suhteet**-nimike, laajenna **VendTrans.VendTable\_AccountNum**-nimike ja valitse **VendTable. VendTrans. VendTable\_AccountNum.\$Transtyperecord** -nimike.
    2. Valitse **Muokkaa**.
    3. Valitse **Muokkaa kaavaa**.
    4. Etsi **Kaava**-kentästä seuraava lauseke:

        FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. Syötä **Kaava**-kenttään seuraava lauseke:

        FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).

    6. Valitse **Tallenna**.
    7. Sulje **Kaavaeditori**-sivu.
    8. Valitse **OK**.

5. Valitse **Tallenna**.
6. Sulje **Mallimäärityksen sunnittelun** sivu.
7. Sulje **Mallimääritykset**-sivu.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>ER-mallin yhdistämismäärityksen muokatun version täydentäminen

1. Valitse RCS-järjestelmän **Konfiguraatiot**-sivun **Versiot**-pikavälilehdessä **Suorituskyvyn jäljityksen** määrityksen versio **1.2**.
2. Valitse **Muutoksen tila**.
3. Valitse **Valmis**.

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a>Tuo muokattu ER-mallin yhdistämismääritys RCS:stä sovellukseen

Toista tämän aiheen [Tuo ER-konfiguraatio RCS:stä Finance and Operationsiin](#import-configuration) -osiossa kuvatut vaiheet tuodaksesi **Suorituskyvyn jäljityskartoitus** -konfiguraation version 1.2.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Muokatun ER-ratkaisun suorittaminen jäljityksen suorittamista varten

### <a name="run-the-er-format"></a>Suorita ER-muoto

Luo uusi suoritusjälki [Suorita ER-muoto](#run-format) toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.

## <a name="review-the-execution-trace"></a>Suorituksen jäljityksen tarkasteleminen

### <a name="export-the-generated-trace-from-the-application"></a>Vie luotu jäljitys sovelluksesta

Toista tämän aiheen [Vie luotu jäljitys sovelluksesta](#export-trace) -osiossa kuvatut vaiheet tallentaaksesi uuden suorituskyvyn jäljityksen paikallisesti.

### <a name="import-the-generated-trace-into-rcs"></a>Tuo tuotettu jälki RCS:ään.

Toista tässä osassa aiemmin kerrotut vaiheet [Tuo luodut jäljet RCS](#import-trace) tuodaksesi uudet suorituskykyjäljet RCS:ään.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys

Suorita aiemmin tämän ohjeaiheen [Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys](#use-trace) -osassa kuvatut suorituskyvyn jäljitys -kohdan vaiheet, kun haluat analysoida viimeisimmän suorituskyvyn jäljityksen.

Huomaa, että mallimääritykseen tehdyt oikaisut ovat poistaneet tietokannasta päällekkäisiä kyselyitä. Tämän mallimäärityksen tietokantataulukoihin ja tietolähteisiin tehtyjen kutsujen määrä on myös vähennetty. Näin ollen koko ER-ratkaisun suorituskyky on parantunut.

![Jäljitä tietoja VendTable-tietolähteestä RCS-mallin mallinmäärityssuunnittelija-sivulta](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

Jäljitystiedoissa VendTable-tietolähteen arvo **\[12\]** ilmaisee, että tätä tietolähdettä kutsuttiin 12 kertaa. Arvo **\[Q:6\]** ilmaisee, että tietokantakutsuille on käännetty kuusi kutsua VendTable-tauluun. Arvo **\[C:6\]** ilmaisee, että tietokannasta noudetut tiedot tallennettiin välimuistiin ja kuusi muuta kutsua käsiteltiin välimuistin avulla.

Huomaa, että LedgerTransTypeList-tietolähteeseen soitettujen kutsujen määrä on vähentynyt 9 027:sta 240:een.

![Jäljitä tietoja LedgerTransTypeList-tietolähteestä RCS-mallin mallinmäärityssuunnittelija-sivulta](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a>Tarkasta suorituksen jäljitys sovelluksessa

RCS:n lisäksi jotkin versiot voivat tarjota ER-kehyssuunnittelijakokemuksen ominaisuuksia. Näissä versioissa on **Ota käyttöön suunnittelutila** -vaihtoehto, joka voidaan ottaa käyttöön. Tämä vaihtoehto löytyy **Sähköisen raportoinnin parametrit** -sivun **Yleiset**-välilehdestä, jonka voit avata **Sähköisen raportoinnin** työtilassa.

![Ota käyttöön suunnittelutila -vaihtoehto Sähköisen raportoinnin parametrit- sivulla](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

Jos käytät jotakin näistä versioista, voit analysoida luotuja suorituskyvyn jäljityksiä suoraan sovelluksessa. Sinun ei tarvitse viedä niitä sovelluksesta ja tuoda niitä RCS:ään.

## <a name="review-the-execution-trace-by-using-external-tools"></a>Suorituksen jäljityksen tarkasteleminen ulkoisten työkalujen avulla

### <a name="configure-user-parameters"></a>Konfiguroi käyttäjäparametrit

1. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. Valitse **Käyttäjäparametrit** -valintaikkunan **Suorituksen jäljitys** -osan **Suorituksen jäljitys muoto-osan** -kentässä **PerfView XML**.

### <a name="run-the-er-format"></a>Suorita ER-muoto

Luo uusi suoritusjälki [Suorita ER-muoto](#run-format) toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.

Huomaa, että Internet-selain tarjoaa zip-tiedoston ladattavaksi. Tämä tiedosto sisältää suorituskyvyn jäljityksen PerfView-muodossa. Tämän jälkeen voit analysoida ER Format Execution -toiminnon tietoja Perxview-suorituskyvyn analysointityökalun avulla.

![Suoritetun ER-muodon jäljitystiedot PerfView-muodossa](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a>Tietokantakyselyjä sisältävän suorituksen jäljityksen tarkastelemisen arviointi ulkoisilla työkaluilla

ER-kehykseen tehtyjen parannusten ansiosta PerfView-muodossa luotu suorituskyvyn jäljitys sisältää nyt enemmän tietoja ER-muodon suorittamisesta. Microsoft Dynamics 365 for Finance and Operations -versiossa 10.0.4 (heinäkuu 2019) tämä jäljitys voi sisältää myös tietoja suoritetuista sovellustietokannan SQL-kyselyistä.

### <a name="configure-user-parameters"></a>Konfiguroi käyttäjäparametrit

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. Määritä seuraavat parametrit **Käyttäjäparametrit**-valintaikkunan **Suorituksen jäljitys** -osassa:

    - Valitse **Suorituksen jäljitysmuoto** -kentässä **PerfView XML**.
    - Määritä **Kerää kyselytilastot** -asetukseksi **Kyllä**.
    - Määritä **Jäljitä kysely** -asetukseksi **Kyllä**.

    ![Käyttäjän parametrit -valintaikkuna](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a>Suorita ER-muoto

Luo uusi suoritusjälki [Suorita ER-muoto](#run-format) toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.

Huomaa, että Internet-selain tarjoaa zip-tiedoston ladattavaksi. Tämä tiedosto sisältää suorituskyvyn jäljityksen PerfView-muodossa. Tämän jälkeen voit analysoida ER Format Execution -toiminnon tietoja Perxview-suorituskyvyn analysointityökalun avulla. Tämä jäljitys sisältää nyt tiedot SQL-tietokannan käytöstä ER-muodon suorittamisen aikana.

![Suoritetun ER-muodon jäljitystiedot PerfView-muodossa](./media/GER-PerfTrace2-PerfViewTrace2.PNG)
