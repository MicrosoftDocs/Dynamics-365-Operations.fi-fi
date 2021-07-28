---
title: Paranna sähköisen raportoinnin ratkaisujen suorituskykyä lisäämällä parametrisoidut LASKETTU KENTTÄ -tietolähteet.
description: Tässä ohjeaiheessa kerrotaan, miten sähköisen raportoinnin ratkaisujen suorituskykyä voi parantaa lisäämällä parametrisoidut LASKETTU KENTTÄ -tietolähteet.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e3dc83b71300387c8123f5533522c5ead7d86333
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349181"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>Paranna sähköisen raportoinnin ratkaisujen suorituskykyä lisäämällä parametrisoidut LASKETTU KENTTÄ -tietolähteet.

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten voit [jäljittää suorituskykyä](trace-execution-er-troubleshoot-perf.md) suoritetuissa [sähköisen raportoinnin](general-electronic-reporting.md) muodoissa ja käyttää sitten näitä jäljitystietoja suorituskyvyn parantamisessa määrittämällä parametrisoitu **Laskettu kenttä** -tietolähde.

Osana sähköisen raportoinnin konfiguraation suunnittelua yritysasiakirjojen luomista varten määritetään menetelmä, jonka avulla tiedot haetaan sovelluksesta ja syötetään luotavaan tuotokseen. Kun parametrisoidun sähköisen raportoinnin **Laskettu kenttä** -tyyppinen tietolähde on suunniteltu, voit vähentää tietokantakutsujen määrää sekä vähentää merkittävästi aikaa, joka kuluu sähköisen raportoinnin muodon suorituksen tietojen keräämiseen kuluvaa aikaa ja käytettyjä kustannuksia.

## <a name="prerequisites"></a>Edellytykset

- Tässä ohjeaiheessa olevien esimerkkien suorittaminen edellyttää käyttöoikeutta johonkin seuraavaan [rooliin](../sysadmin/tasks/assign-users-security-roles.md):

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

- Yritykselle on asetettava **DEMF**.
- Tämän ohjeaiheen [lisäyksen 1](#appendix1) vaiheiden mukaisesti voit ladata tämän ohjeaiheen esimerkkien suorittamisessa tarvittavien Microsoftin sähköisen raportoinnin näyteratkaisun komponentit.
- Määritä tämän ohjeaiheen [lisäyksen 2](#appendix2) ohjeiden avulla sähköisen raportoinnin parametrien vähimmäismäärä, joka vaaditaan sähköisen raportoinnin kehystä varten Microsoftin sähköisen raportoinnin näyteratkaisin suorituskyvyn parantamiseksi.

## <a name="import-the-sample-er-solution"></a>Sähköisen raportoinnin näyteratkaisun tuominen

Oletetaan, että sinun on suunniteltava uusi sähköisen raportoinnin ratkaisu, jonka avulla luodaan toimittajatapahtumat näyttävä uusi raportti. Tällä hetkellä voit etsiä valitun toimittajan tapahtumat **Toimittajatapahtumat**-sivulta (Siirry **Ostoreskontra** \> **Toimittajat** \> **Kaikki toimittajat**, valitse toimittaja ja sitten toimintoruudun **Toimittaja**-välilehti kohdassa valitse **Tapahtumat**-ryhmästä **Tapahtumat**). Haluat kuitenkin saada kaikki toimittajatapahtumat yhdessä sähköisessä asiakirjassa XML-muodossa. Tämä ratkaisu koostuu useista sähköisen raportoinnin konfiguraatioista, jotka sisältävät vaaditun tietomallin, mallien yhdistämismääritykset ja muotokomponentit.

Ensimmäinen vaihe on sähköisen raportoinnin näyteratkaisun tuominen toimittajatapahtumien luomista varten.

1. Kirjaudu Microsoft Dynamics 365 Financen esiintymään, joka on valmisteltu yrityksellesi.
2. Tässä aiheessa luodaan ja muokataan konfiguraatioita malliyritykselle **Litware, Inc.**. Varmista, että tämä konfiguraation tarjoaja on lisätty Finance-esiintymään ja merkitty aktiiviseksi. Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.
4. Tuo **Konfiguraatiot** -sivulla lataamasi ER-kokoonpanot Financen edellytyksenä seuraavassa järjestyksessä: tietomalli, metatiedot, mallikartoitus, muoto. Luo kukin mukautus seuraavasti:

    1. Valitse toimintoruudussa **Vaihda** \> **Lataa XML-tiedostosta**.
    2. Valitse soveltuva sähköisen raportoinnin konfiguraation tiedosto XML-muodossa valitsemalla **Selaa**.
    3. Valitse **OK**.

![Konfiguraatiot-sivun tuodut konfiguraatiot.](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>Sähköisen raportoinnin näyteratkaisun tarkistaminen

### <a name="review-the-model-mapping"></a>Mallin määrityksen tarkastelu

1. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu, laajenna **Suorituskyvyn parantamisen malli** ja valitse sitten **Suorituskyvyn parantamisen yhdistämismääritys**.
2. Valitse toimintoruudussa **Suunnittelija**.
3. Valitse **Malli tietolähteen yhdistämismääritystä varten** -sivun toimintoruudussa **Suunnittelija**.

    Tämä sähköisen raportoinnin mallin yhdistämismääritys on suunniteltu seuraavia toimintoja varten:

    - Hae VendTrans-tauluun (**Trans**-tietolähde) tallennettujen toimittajatapahtumien luettelo.
    - Hae jokaiselle tapahtumalle VendTable-taulusta toimittajatietue, johon tapahtuma on kirjattu (**\#Vend**-tietolähde).

    > [!NOTE]
    > **\#Vend**-tietolähde on määritetty hakemaan vastaava toimittajatietue käyttämällä olemassa olevaa monta yhteen -suhdetta **\@.'\>Relations'.VendTable\_AccountNum**.

    Tässä kokoonpanossa mallin yhdistäminen käyttää tälle mallille luotujen ja Financessa suoritettujen sähköisen raportoinnin muotojen perustietomallia. Tämän vuoksi **Trans**-tietolähteen sisältö näkyy sähköisen raportoinnin muodoissa, esimerkiksi abstrakteina **mallitietolähteinä**.

    ![Mallin yhdistämismäärityksen suunnitteluohjelman sivun Trans-tietolähde.](media/er-calculated-field-ds-performance-mapping-1.png)

4. Sulje **Mallimäärityksen sunnittelun** sivu.
5. Sulje **Malli tietolähteen yhdistämismääritystä varten** -sivu.

### <a name="review-format"></a>Muodon tarkastelu

1. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu, laajenna **Suorituskyvyn parantamisen malli** ja valitse sitten **Suorituskyvyn parantamisen muoto**.
2. Valitse toimintoruudussa **Suunnittelija**.
3. Valitse **Muodon suunnittelu** -sivun **Yhdistämismääritys**-välilehdessä **Laajenna/kutista**.
4. Laajenna **Malli**-, **Tiedot**- ja **Tapahtuma**-kohteet.

    Tämä sähköisen raportoinnin muoto on suunniteltu toimittajatapahtumien raportin luomiseksi XML-muodossa.

    ![Muodon tietolähteet ja määritetyt muotoelementtien sidokset Muodon suunnittelutoiminto -sivulla.](media/er-calculated-field-ds-performance-format.png)

5. Sulje **Muodon suunnittelija** -sivu.

## <a name="run-the-sample-er-solution-to-trace-execution"></a>Sähköisen raportoinnin näyteratkaisun suorittaminen jäljityksen suorittamista varten

Ajatellaan, että olet suunnitellut sähköisen raportoinnin ratkaisun ensimmäisen version. Haluat nyt testata ratkaisun Finance-esiintymässä ja analysoida suorituskyvyn.

### <a name="turn-on-the-er-performance-trace"></a>ER-suorituskykyjäljityksen ottaminen käyttöön

1. Valitse **DEMF**-yritys.
2. Seuraa [ER-suorituskykyjäljityksen ottaminen käyttöön](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) -kohdan ohjeita ja luo suorituskykyjäljitys sähköisen raportoinnin muotoilun suorituksen aikana.

    ![Käyttäjän parametrit -valintaikkuna.](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>Suorita ER-muoto

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn parantamisen muoto**.
3. Valitse toimintoruudussa **Suorita**.

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>Suorituskykyjäljityksen käyttäminen mallin yhdistämismäärityksen suorituskyvyn analysoimisessa

1. Valitse **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn parantamisen yhdistämismääritys**.
2. Valitse toimintoruudussa **Suunnittelija**.
3. Valitse **Mallin yhdistämismääritykset** -sivun toimintoruudussa **Suunnittelija**.
4. Valitse **Mallin määrityssuunnittelija** -sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.
5. Valitse uusin jäljitys ja valitse sitten **OK**.

Joidenkin nykyisen mallin yhdistämismääritysten tietolähdenimikkeiden käytettävissä on nyt uusia tietoja:

- Tietolähteen avulla tietoja haettaessa käytetty todellinen aika
- Sama aika ilmaistaan prosentteina kokonaisajasta, joka käytettiin koko mallin määrityksen suorittamiseen.

![Mallin yhdistämismäärityksen suunnittelu -sivun suoritusajan tiedot.](./media/er-calculated-field-ds-performance-mapping-2.png)

**Suorituskyvyn tilastotiedot** -ruudukossa on tieto, että **Trans**-tietolähde kutsuu VendTrans-taulua kerran. Arvo **\[265\]\[Q:265\]** **Trans**-tietolähteessä osoittaa, että 265 toimittajatapahtumaa on noudettu sovelluksen taulusta ja palautettu tietomallille.

**Suorituskyvyn tilastotiedot** -ruudukossa on myös nykyisen mallin yhdistämismäärityksen kaksoiskappaleiden tietokantapyynnöt, kun **\#Vend**-tietolähdettä suoritetaan. Kaksoiskappaleita tulee seuraavista syistä:

- Toimittajan taulua kutsutaan kaksi kertaa jokaista 265 iteroitua toimittajatapahtumaa kohden. Yhteensä kutsuja on 530:

    - Yksi kutsu tehdään toimittajan tilinumeron syöttämistä varten.
    - Yksi kutsu tehdään toimittajan nimen syöttämistä varten.

- Toimittajan taulua kutsutaan jokaista iteroitua toimittajatapahtumaa kohden, vaikka noudetut tapahtumat on kirjattu vain viidelle toimittajalle. 530 kutsusta 525 on kaksoiskappaleita. Seuraavassa kuvassa näkyy sanoma, joka ilmaisee, että kutsut ovat päällekkäisiä kutsuja (tietokantapyyntöjä).

![Virheilmoitus tietokantapyyntöjen kaksoiskappaleista mallin yhdistämismäärityksen suunnittelusivulla.](./media/er-calculated-field-ds-performance-mapping-2a.png)

Ota huomioon, että yli 80 prosenttia (noin kuusi sekuntia) mallin yhdistämismäärityksen kokonaissuoritusajasta on kulunut VendTable-sovellustaulun arvojen hakemiseen. Tämä prosenttiosuus on liian suuri viiden toimittajan kahdelle määritteelle verrattuna VendTrans-sovellustaulun tietojen määrään.

Voit vähentää kunkin tapahtuman toimittajan tietojen haussa käytettävien kutsujen määrää ja parantaa mallin yhdistämismäärityksne suorituskykyä käyttämällä **\#Vend**-tietolähteen välimuistiin tallentamista.

> [!NOTE]
> **Trans\\\#Vend**-tietolähde tallennetaan välimuistiin nykyiselle **Trans**-tietolähteelle suorituksen aikana.

Kun **\#Vend**-tietolähde tallennetaan välimuistiin, kutsujen kaksoiskappaleiden määrä vähenee 525 kutsusta 260 kutsuun. Kaksoiskappaleita kuitenkin on yhä. Voit poistaa kaksoiskappaleet kokonaan määrittämällä uuden parametrisoidun tietolähteen, jonka tyyppi on **Laskettu kenttä**.

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Paranna mallin määritystä suorituksen jälkeisten tietojen perusteella

### <a name="change-the-logic-of-the-model-mapping"></a>Mallin yhdistämismäärityksen logiikan muuttaminen

Näiden ohjeiden avulla voit käyttää **Laskettu kenttä** -tyyppistä tietolähdettä. Se auttaa estämään tietokannan kutsujen kaksoiskappaleita.

1. Valitse **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn parantamisen yhdistämismääritys**.
2. Valitse toimintoruudussa **Suunnittelija**.
3. Valitse **Mallin yhdistämismääritykset** -sivun toimintoruudussa **Suunnittelija**.
4. Lisää **Mallin yhdistämismäärityksen suunnittelija** -sivulla **Taulun tietueet** -tyyppinen tietolähde VendTable-sovellustauluun seuraavasti:

    1. Laajenna **Tietolähdetyypit** -ruudussa **Dynamics 365 for Operations** ja valitse **Taulun tietueet**.
    2. Valitse **Lisää pääkansio**.
    3. Anna valintaikkunan **Nimi**-kenttään **Vend**-arvo.
    4. Anna **Taulu**-kenttään **VendTable**-arvo.
    5. Valitse **OK**.

5. Voit parametrisoida **Laskettu kenttä** -tyyppisten tietolähteiden kutsut vain, jos nämä tietolähteet ovat säilössä. Noudata tämän vuoksi näitä ohjeita, jos haluat lisätä **Tyhjä säilö** -tyyppisen tietolähteen uuden **Laskettu kenttä** -tyyppisen parametrisoidun tietolähteen tallennuspaikaksi.

    1. Laajenna **Tietolähdetyypit** -ruudussa **Yleistä** ja valitse **Tyhjä säilö**.
    2. Valitse **Lisää pääkansio**.
    3. Anna valintaikkunan **Nimi**-kenttään **Box**-arvo.
    3. Valitse **OK**.

    ![Mallin yhdistämismäärityksen suunnitteluohjelman sivun Box-tietolähde.](./media/er-calculated-field-ds-performance-mapping-3.png)

6. Lisää **Laskettu kenttä** -tyyppinen parametrisoitu tietolähde seuraavasti:

    1. Valitse **Tietolähteet**-ruudussa **Box**.
    2. Laajenna **Tietolähdetyypit**-ruudussa **Funktiot** ja valitse **Laskettu kenttä**.
    3. Valitse **Lisää**.
    4. Anna valintaikkunan **Nimi**-kenttään **Vend**-arvo.
    5. Valitse **Muokkaa kaavaa**.
    6. Valitse **Kaavan suunnittelutoiminto** -sivulla **Parametrit** ja määritä, mitkä parametrit on annettava tietolähteen kutsumisen yhteydessä.
    7. Valitse **Parametrit**-valintaruudussa **Uusi**.
    8. Anna **Nimi**-kenttään **parmVendAccNumber**-arvo.
    9. Kirjoita **Tyyppi**-kenttään **Merkkijono**.
    10. Valitse **OK**.
    11. Syötä **Kaava**-kenttään **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.
    12. Valitse **Tallenna** ja sulje **Kaavan suunnittelutoiminto** -sivu.
    13. Lisää uusi tietolähde valitsemalla **OK**.

7. Merkitse lisätty tietolähde välimuistiin tallennetuksi suorituksen aikana seuraavasti:

    1. Valitse **Tietolähteet**-ruudussa **Box\\Vend**.
    2. Valitse **Välimuisti**.

    > [!NOTE]
    > **Box\\Vend**-tietolähde tallennetaan välimuistiin **Trans**-tietolähteen kaikille toimittajatapahtumille suorituksen aikana.

8. Päivitä upotettu **Trans\\\#Vend**-tietolähde niin, että se käyttää **Box\\Vend**-tietolähdettä seuraavasti:

    1. Laajenna **Tietolähteet**-ruudussa **Trans**.
    2. Valitse **Trans\\\#Vend**-tietolähde ja valitse sitten **Muokkaa** \> **Muokkaa kaavaa**.
    3. Syötä **Kaavan suunnittelutoiminto** -sivun **Kaava**-kenttään **Box.Vend(\@.AccountNum)**.
    4. Valitse **Tallenna** ja sulje **Kaavan suunnittelutoiminto** -sivu.
    5. Valitse **OK** ja viimeistele valitun tietolähteen muutokset.

9. Valitse **Tallenna**.

    ![Mallin yhdistämismäärityksen suunnitteluohjelman sivun Vend-tietolähde.](./media/er-calculated-field-ds-performance-mapping-4.png)

10. Sulje **Mallimäärityksen sunnittelun** sivu.
11. Sulje **Mallimääritykset**-sivu.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>ER-mallin yhdistämismäärityksen muokatun version täydentäminen

1. Valitse **Konfiguraatiot**-sivun **Versiot**-pikavälilehdessä version **1.2** **Suorituskyvyn parannuksen yhdistämismääritys** -konfiguraatio.
2. Valitse **Muuta tilaa** \> **Valmis** ja valitse sitten **OK**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Muokatun ER-ratkaisun suorittaminen jäljityksen suorittamista varten

Luo uusi suoritusjälki [Suorita ER-muoto](#run-format) toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>Suorituskykyjäljityksen käyttäminen mallin yhdistämismäärityksen oikaisujen analysoimisessa 

1. Valitse **Konfiguraatiot**-sivulla konfiguraatiopuussa **Suorituskyvyn parantamisen yhdistämismääritys**.
2. Valitse toimintoruudussa **Suunnittelija**.
3. Valitse **Mallin yhdistämismääritykset** -sivun toimintoruudussa **Suunnittelija**.
4. Valitse **Mallin määrityssuunnittelija** -sivulla hallintapaneelista **Suorituskyvyn jäljitysmuoto**.
5. Valitse uusin jäljitys ja valitse sitten **OK**.

Huomaa, että mallimääritykseen tehdyt oikaisut ovat poistaneet tietokannasta päällekkäisiä kyselyitä. Tämän mallimäärityksen tietokantataulukoihin ja tietolähteisiin tehtyjen kutsujen määrä on myös vähennetty.

![Mallin yhdistämismäärityksen suunnitteluohjelman sivun 1 jäljitystiedot.](./media/er-calculated-field-ds-performance-mapping-5.png)

Suorituksen kokonaisaikaa on vähennetty noin 20 kertaa (noin 8 sekunnista noin 400 millisekuntiin). Näin ollen koko sähköisen raportoinnin ratkaisun suorituskykyä on parannettu.

![Mallin yhdistämismäärityksen suunnitteluohjelman sivun 2 jäljitystiedot.](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>Liite 1: Microsoftin sähköisen raportoinnin näyteratkaisun komponenttien lataaminen

Seuraavat tiedostot täytyy ladata ja tallentaa paikallisesti.

| Tiedosto                                        | Sisältö |
|---------------------------------------------|---------|
| Suorituskyvyn parannuksen malli.versio.1     | [Esimerkin ER-tietomallin konfigurointi](https://download.microsoft.com/download/4/6/f/46f0f3fa-782b-414a-8f7b-b6c64a388661/Performance_improvement_model.version.1.xml) |
| Suorituskyvyn parannuksen yhdistämismääritys.versio.1.1 | [Esimerkin ER-mallikartoituksen konfigurointi](https://download.microsoft.com/download/8/9/1/8913a763-afb8-4bf4-aaf1-95ad793ffc5a/Performance_improvement_mapping.version.1.1.xml) |
| Suorituskyvyn parannuksen muoto.versio.1.1  | [Esimerkin ER-format-konfigurointi](https://download.microsoft.com/download/9/0/c/90c75963-bc78-4edc-9096-556bbe281f10/Performance_improvement_format.version.1.1.xml) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>Liite 2: Sähköisen raportoinnin kehyksen määrittäminen

Ennen kuin alat käyttää sähköisen raportoinnin kehystä Microsoftin sähköisen raportoinnin näyteratkaisun suorituskyvyn parantamiseksi, sinun on määritettävä sähköisen raportoinnin parametrien vähimmäisjoukko.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Konfiguroi ER-parametrit

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit** -osassa **Sähköisen raportoinnin parametrit**.
3. Määritä **Sähköisen raportoinnin parametrit** -sivun **Yleinen**-välilehdessä **Ota käyttöön suunnittelutila** -asetukseksi **Kyllä**.
4. Määritä **Liitteet**-välilehdessä seuraavat parametrit:

    - Valitse **Konfiguraatiot**-kentässä **Tiedosto**-tyyppi **DEMF**-yritykselle.
    - Valitse **Työarkisto**-, **Väliaikainen**-, **Perusrivi**- ja **Muut**-kentissä **Tiedosto**-tyyppi.

Lisätietoja ER-parametreista on kohdassa [Määritä ER-kehys](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Aktivoi ER-konfiguraation lähde

Jokainen lisätty ER-konfiguraatio merkitään ER-konfiguraation lähteen omistamaksi. ER-konfiguraation lähdettä, joka on aktivoitu **Sähköinen raportointi** -työtilassa, käytetään tähän tarkoitukseen. Siksi sinun on aktivoitava ER-konfiguraation lähde **Sähköinen raportointi** -työtilassa, ennen kuin voit alkaa lisätä tai muokata ER-konfiguraatioita.

> [!NOTE]
> Vain sähköisen raportoinnin konfiguraation omistaja voi muokata konfiguraatiota. Siksi ennen kuin ER-konfiguraatiota voi muokata, asianmukainen ER-konfiguraation lähde on aktivoitava **Sähköinen raportointi** -työtilassa.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Tarkista ER-konfiguraation lähteiden luettelo

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Konfiguraation lähteet**-ruutu.
3. **Konfiguraation lähdetaulu** -sivulla jokaisen lähteen tietueella on yksilöllinen nimi ja URL-osoite. Tarkista tämän sivun sisältö. Jos **Litware, Inc.** -tietue on jo olemassa, ohita seuraava menettely: [Uuden sähköisen raportoinnin konfiguraation toimittajan lisääminen](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Lisää uusi ER-konfiguraation lähde

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Konfiguraation lähteet**-ruutu.
3. Valitse **Konfiguraation lähteet**-sivulla **Uusi**.
4. Kirjoita **Nimi**-kenttään **Litware, Inc.**
5. Kirjoita **Internetosoite**-kenttään `https://www.litware.com`.
6. Valitse **Tallenna**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivoi ER-konfiguraation lähde

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Konfiguraation lähteet**-osassa **Litware, Inc.** -ruutu ja valitse sitten **Aseta aktiiviseksi**.

Lisätietoja ER-konfiguraation lähteistä on kohdassa [Konfiguraation lähteiden luonti ja merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md)
- [Laskettu kenttä -tyyppisten ER-tietolähteiden parametrisoitujen kutsujen tuki](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
