---
title: Uuden sähköisen raportoinnin ratkaisun suunnitteleminen ZPL-etikettien tulostamista varten
description: Tässä artikkelissa kerrotaan miten uusi ER-ratkaisu suunnitellaan tulostamaan Zebra Programming Language (ZPL) -etikettejä.
author: kfend
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 7ef83cf4822ca129af3ca01fa6ddd05219fee0d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271760"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>Uuden sähköisen raportoinnin ratkaisun suunnitteleminen ZPL-etikettien tulostamista varten

[!include [banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, miten järjestelmänvalvoja-, sähköisen raportoinnin kehittäjä- tai sähköisen raportoinnin toiminnallinen konsultti -roolin käyttäjä voi määrittää [Sähköisen raportoinnin (ER)](general-electronic-reporting.md) kehyksen parametrit, suunnitella uuden ER-ratkaisun vaaditut ER-[kokoonpanot](general-electronic-reporting.md#Configuration) käyttämään varastonhallintajärjestelmää ja luoda mukautettuja varaston sijainnin etikettejä Zebra Programming Language (ZPL) II -muodossa. Nämä vaiheet voidaan suorittaa **USRT**-yrityksessä.

## <a name="business-scenario"></a>Liiketoimintaskenaario

Edustat yritystä, joka on toteuttanut varastonhallinnan Microsoft Dynamics 365 Financessa. Jokaiseen varastosijaintiin on oltava merkitty itsekiinnittyvä etiketti, joka sisältää viivakoodin. Varastotyöntekijät skannaavat viivakoodit kädessä pidettävillä viivakoodinlukijoilla.

Kaikki varastosijainnit on merkitty etiketeillä julkaisua edeltävien aktiviteettien laajuudessa. Sinun on kuitenkin pystyttävä tulostamaan varastosijaintien etiketit myös tarpeen mukaan, jos aiemmin luodut etiketit vahingoittuvat tai varaston hyllyt konfiguroidaan uudelleen. Käyttämällä viimeksi julkaistua ER-toimintoa voit konfiguroida uuden ER-ratkaisun, jonka avulla varaston valvoja voi tulostaa etiketit suoraan etikettitulostimeen.

## <a name="configure-the-er-framework"></a>Määritä ER-kehys

Seuraa vaiheita kohdassa [Määritä ER-kehys](er-quick-start2-customize-report.md#ConfigureFramework) luodaksesi ER-parametrien vähimmäisjoukon. Nämä asetukset on suoritettava, ennen kuin ER-kehystä käytetään uuden ER-ratkaisun suunnitteluun.

## <a name="design-a-domain-specific-data-model"></a>Toimialuekohtaisen tietomallin suunnitteleminen

Luo uusi ER-konfiguraatio, joka sisältää [tietomalli](er-overview-components.md#data-model-component)-komponentin varastonhallinnan toimialueelle. Tätä tietomallia käytetään myöhemmin tietolähteenä suunniteltaessa ER-muotoa varastosijainnin etikettien luomiseksi.

### <a name="import-a-data-model-configuration"></a>Tietomallimäärityksen tuominen

Noudata näitä ohjeita, kun haluat tuoda vaaditun tietomallin Microsoftin toimittamasta XML-tiedostosta. Vaihtoehtoisesti voit luoda oman tietomallin seuraavassa osassa kuvatulla tavalla.

1. Lataa [Warehouse model.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml) -tiedosto ja tallenna se paikalliseen tietokoneeseen.
2. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
3. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.
4. Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Vaihda**\>**Lataa XML-tiedostosta**.
5. Valitse **Selaa** ja etsi ja valitse **Warehouse model.version.1.xml** -tiedosto.
6. Tuo konfigurointi valitsemalla **OK**.

![Tuotu ER-tietomallin määritys Määritykset-sivulla.](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>Luo tietomallin konfiguraatio

Sen sijaan, että tuot Microsoftin toimittaman tietomallitiedoston, voit luoda tietomallin tyhjästä. Esimerkki tehtävän suorittamisesta on kohdassa [Uuden tietomallin konfiguroinnin luominen](er-quick-start1-new-solution.md#DesignDataModel).

### <a name="review-the-data-model"></a>Tietomallin tarkistaminen

Voit tarkastella konfiguroidun tietomallin muokattavaa versiota **Tietomallin suunnittelu** -sivulla.

![ER-tietomallin rakenne Tietomallin suunnittelu -sivulla.](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>Mallin määrityksen suunnitteleminen konfiguroidulle tietomallille

Sähköisen raportoinnin kehittäjän roolin käyttäjänä sinun on luotava uusi ER-konfiguraatio, joka sisältää varaston tietomallin [mallinyhdistämis](er-overview-components.md#model-mapping-component)-komponentin. Tämä komponentti toteuttaa Dynamics 365 Financen konfiguroidun tietomallin, se liittyy nimenomaan kyseiseen sovellukseen. Se on konfiguroitava niin, että se määrittää sovellusobjektit, joita käytetään määritetyn tietomallin täyttämiseen sovellustiedoilla suorituksen aikana. Tämän tehtävän suorittaminen edellyttää, että olet tietoinen varastonhallinnan liiketoimialueen tietorakenteen toteutustavasta Financessa.

### <a name="import-a-model-mapping-configuration"></a>Mallin yhdistämismäärityksen tuominen

Noudata näitä ohjeita, kun haluat tuoda vaaditun tietojen yhdistämismäärityksen Microsoftin toimittamasta XML-tiedostosta. Vaihtoehtoisesti voit luoda oman tietojen yhdistämismäärityksen seuraavassa osassa kuvatulla tavalla.

1. Lataa [Warehouse model mapping.version.1.1.xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml) -tiedosto ja tallenna se paikalliseen tietokoneeseen.
2. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
3. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.
4. Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Vaihda**\>**Lataa XML-tiedostosta**.
5. Valitse **Selaa** ja etsi ja valitse **Warehouse model mapping.version.1.1.xml** -tiedosto.
6. Tuo konfigurointi valitsemalla **OK**.

![Tuotu ER-tietomallin yhdistämismääritys Määritykset-sivulla.](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>Luo mallin yhdistämismääritys

Sen sijaan, että tuot Microsoftin toimittaman mallin yhdistämistiedoston, voit luoda mallin yhdistämismäärityksen tyhjästä. Esimerkki tehtävän suorittamisesta on kohdassa [Uuden mallin yhdistämismäärityksen konfiguroinnin luominen](er-quick-start1-new-solution.md#CreateModelMapping).

### <a name="review-the-model-mapping"></a>Mallin määrityksen tarkastelu

Voit tarkastella konfiguroidun mallin yhdistämismäärityksen muokattavaa versiota **Mallin yhdistämismäärityksen suunnittelu** -sivulla.

![ER-mallin yhdistämismäärityksen rakenne Mallin yhdistämismäärityksen suunnittelu -sivulla.](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>Muodon suunnittelu

Sähköisen raportoinnin toiminnallinen konsultti -roolin käyttäjänä sinun on luotava uusi ER-konfiguraatio, joka sisältää [muoto](er-overview-components.md#format-component)-komponentin. Tämän komponentin määrittämisessä käytetään ZPL II -koodia varastosijainnin etiketin asettelun määrittämiseen.

### <a name="import-a-format-configuration"></a>Tuo muotokonfiguraatio

Noudata näitä ohjeita, kun haluat tuoda vaaditun muodon Microsoftin toimittamasta XML-tiedostosta. Vaihtoehtoisesti voit luoda oman muodon seuraavassa osassa kuvatulla tavalla.

1. Lataa [Warehouse location labels.version.1.1.xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml) -tiedosto ja tallenna se paikalliseen tietokoneeseen.
2. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
3. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.
4. Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Vaihda**\>**Lataa XML-tiedostosta**.
5. Valitse **Selaa** ja etsi ja valitse **Warehouse location labels.version.1.1.xml** -tiedosto.
6. Tuo konfigurointi valitsemalla **OK**.

![Tuotu ER-muodon määritys Määritykset-sivulla.](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>Muotokonfiguraation luominen

Sen sijaan, että tuot Microsoftin toimittaman muototiedoston, voit luoda muodon tyhjästä. Esimerkki tehtävän suorittamisesta on kohdassa [Uuden muodon konfiguroinnin luominen](er-quick-start1-new-solution.md#FormatCreate).

### <a name="review-the-format"></a>Muodon tarkastelu

Voit tarkastella konfiguroidun muodon muokattavaa versiota **Muodon suunnittelu** -sivulla.

![ER-muodon rakenne Muodon suunnittelu -sivulla.](./media/er-design-zpl-labels-format.png)

Tämän muodon `model.Location.Label`-tietolähde on määritetty luomaan etiketit, jotka sisältävät seuraavat tiedot:

- Varaston otsikko tekstinä
- Varaston otsikko viivakoodina.
- Sijainnin otsikko
- Tarkistusnumerot

Tietolähteen **Kaavan suunnittelu** -sivulla otsikoiden luomiseen käytettävä ER-kaava sisältää `CONCATENATE`-toiminnon, jossa tiedot yhdistetään haluttuun asetteluun.

![Tietolähteen kaava tarkastelu Kaavan suunnittelija -sivulla.](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> Etiketin asettelu on suunniteltu siten, että sijainnin otsikko ja tarkistusnumerot on tasattu etiketin keskelle. ZPL II ei kuitenkaan tue viivakoodien kohdistusta keskelle. Siksi `model.Location.Warehouse.Alignment`-tietolähteen kaavaa käytetään viivakoodin kohdistamiseen etiketin keskelle. Tämä kaava laskee viivakoodin vasemmanpuoleisen siirtymän varaston otsikon merkkien määrän perusteella.

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>Ympäristön valmisteleminen luotujen etikettien esikatselua varten

Seuraavassa esimerkissä luotuja ZPL-etikettejä voi esikatsella näytössä tulostinemulaattorisovelluksella. Tämä asetus otetaan käyttöön seuraavasti.

1. Lisää **varastosijainnin etiketin** ER-muodolle ER-kohde [Tulostin](er-destination-type-print.md) ja määritä se lähettämään luodut etiketit Financesta [asiakirjan reititysagentille (DRA)](install-document-routing-agent.md).
2. Asenna ja määritä DRA reitittääksesi Financen luomat etiketit paikalliseen tulostimeen, joka on käytettävissä nykyisestä työasemasta.
3. Lisää nykyisen työaseman paikallinen tulostin ja määritä se välittämään luodut etiketit DRA:sta tulostinemulaattorisovellukseen.
4. Asenna tulostinemulaattorisovellus Chrome-selaimen laajennuksena ja määritä se siirtämään luodut etiketit paikallisesta tulostimesta verkkopalveluun, joka hahmontaa luodut etiketit ja palauttaa ne tulostinemulaattoriin esikatselua varten.

<table>
<tbody>
<tr align="center">
<td>
<p>Finance</p>
<p>ER-raportti</p>
<p>Tulostinkohde</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>Asiakirjareitityksen agentti</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>Paikallinen tulostin</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>Tulostinemulaattori</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>Hahmonnuksen verkkopalvelu</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>Tulostinemulaattorisovelluksen asentaminen ja konfiguroiminen

Voit lisätä ZPL-hahmonnusmoduulin tulostinemulaattorisovelluksen Chrome-selaimeen. Tässä esimerkissä käytetään [Zpl Printer](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo) -emulaattoria, joka perustuu [Labelary ZPL -verkkopalveluun](http://labelary.com/service.html). Tulostinemulaattorisovellus välittää luodut ZPL-muotoiset etiketit paikalliselta tulostimelta verkkopalveluun ja palauttaa sitten etiketit PDF- tai PNG-tiedostoina esikatselua varten.

1. Etsi ja valitse Chrome-verkkokaupasta tulostinemulaattorisovellus, jota haluat käyttää. Lisää se sitten Chrome-selaimeen valitsemalla **Lisää Chromeen**.

    ![Tulostinemulaattorisovelluksen lisääminen Chrome-verkkoselaimeen Chrome-verkkokaupasta.](./media/er-design-zpl-labels-add-app.png)

2. Valitse **Käynnistä sovellus** jos haluat käyttää tulostinemulaattorisovellusta Chrome-verkkoselaimesta.

    ![Tulostinemulaattorisovelluksen suorittaminen Chrome-verkkoselaimesta.](./media/er-design-zpl-labels-run-app.png)

3. Määritä suoritettava sovellusta:

    1. Poista sovellus käytöstä.
    2. Määritä tulostimen asetuksissa isäntäkoneen arvoksi **127.0.0.1**.
    3. Määritä portiksi **9100**.

        ![Tulostinemulaattorisovelluksen konfigurointi.](./media/er-design-zpl-labels-configure-app.png)

    4. Ota sovellus takaisin käyttöön. Näyttöön pitäisi tulla sanoma, jossa todetaan, että tulostin on käynnistetty määritetyssä isäntäkoneessa ja portissa.

        ![Tulostinemulaattorisovellus otettu uudelleen käyttöön.](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> Koska tässä esimerkissä käytetty tulostinemulaattorisovellus käyttää internet-palvelua etikettien muodostuksissa, varmista, että tietoturva-asetukset sallivat yhteyden palveluun. Muutoin sovellus ei voi vastaanottaa muodostettuja etikettejä, eikä niitä voi esikatsella.

### <a name="add-and-configure-a-local-printer"></a>Paikallisen tulostimen lisääminen ja konfiguroiminen

[Lisää uusi paikallinen tulostin](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b), jota nykyinen laite voi käyttää välittämään luodut etiketit DRA:sta tulostinemulaattorisovellukseen.

1. Valitse Windowsissa **Aloitus** \> **Asetukset** \> **Laitteet** \> **Tulostimet \& skannerit**.
2. Valitse **Tulostimen \& skannerin asetukset**.
3. Valitse kohdassa **Lisää tulostin tai skanneri** **Lisää laite**.
4. Valitse **Haluamaani tulostinta ei ole luettelossa** -kohdassa **Lisää manuaalisesti**.
5. Valitse **Etsi tulostin muilla asetuksilla** -kentästä **Lisää paikallinen tulostin tai verkkotulostin, jolla on manuaaliset asetukset**.
6. Valitse **Valitse tulostinportti** -kentästä **Luo uusi portti** ja noudata seuraavia ohjeita:

    1. Valitse **Portin tyyppi** - kentästä **Vakio-TCP/IP-portti**.
    2. Kirjoita **Isäntänimi tai IP-osoite**-kenttään **127.0.0.1**.
    3. Anna **Portin nimi** -kenttään **ZPL**-arvo.
    4. Odota, kunnes **TCP/IP-portin tunnistus** -toiminto on valmis.
    5. Valitse **Laitetyyppi**-kentässä **Mukautettu** ja sitten **Asetukset**.
    6. Varmista, että seuraavat porttiasetukset on määritetty:

        - **Portin nimi:** ZPL
        - **Tulostimen nimi tai IP-osoite:** 127.0.0.1
        - **Protokolla:** Raw
        - **Portin numero:** 9100

7. Valitse **Asenna tulostinajuri** -kentästä **Vain yleinen/teksti**.
8. Kirjoita **Tulostimen nimi** -kenttään **ZebraPrinter**.

![Paikallisen tulostimen lisääminen nykyiseen laitteeseen.](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>DRA:n määrittäminen ja asentaminen

Valmistele DRA välittämään luodut etiketit Financesta määritetylle paikalliselle tulostimelle.

1. [Asenna DRA](install-document-routing-agent.md#install-the-document-routing-agent).
2. [Määritä DRA](install-document-routing-agent.md#configure-the-document-routing-agent).
3. [Rekisteröi paikallinen tulostin](install-document-routing-agent.md#register-network-printers) DRA:ssa.
4. [Aktivoi paikallinen tulostin](install-document-routing-agent.md#administer-network-printers) Finance-ympäristössä.

![DRA:n valmistelu luotujen etikettien tulostamiseen.](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>ER-kohteiden määrittäminen

Valmistele ER-kohde välittämään luodut etiketit Financesta DRA:han.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin kohde**.
2. Valitse **Sähköisen raportoinnin kohde** -sivun toimintoruudussa **Uusi**.
3. Valitse **Varastosijaintien etiketit** **Viite**-kentästä.
4. Valitse **Tiedostokohde**-pikavälilehdessä **Uusi**.
5. Kirjoita **Nimi**-kenttään **Etiketit**.
6. Valitse **Tiedosto-osan nimi** -kentässä **Raportti**.
7. Valitse **Asetukset**.
8. Aseta ilmestyvän **Kohdeasetukset**-dialogi-ikkunan **Tulostin**-välilehdessä **Käytössä**-asetukseksi **Kyllä**.
9. Valitse **Tulostimen nimi** -kenttään **ZebraPrinter**.
10. Valitse **Asiakirjareitityksen tyyppi** -kentässä **ZPL**.
11. Valitse **OK**.

![ER-kohteen määrittäminen varastosijaintien etiketeille sähköisen raportoinnin kohdesivulla.](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>Varastosijaintien tarkistaminen

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Varasto** \> **Sijainnit**.
2. Suodata **Sijainnit**-sivulla vain ne sijainnit, joissa on arvo **Tarkistusnumerot**-kentässä.

![Varastosijaintien tarkasteleminen Sijainnit-sivulla.](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>Varastosijaintien etikettien tulostaminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Konfiguroinnit**-sivun määrityspuussa **Varastomalli** ja valitse **Varastosijaintien etiketit**.
3. Valitse toimintoruudussa **Suorita**.
4. Valitse **Sähköisen raportin parametrit** -valintaikkunan **Sisällytettävät tietueet** -välilehdessä **Suodata**.
5. Etsi **Alue**-välilehdessä rivi, jonka **Taulukko**-kentän asetuksena on **Sijainnit** ja **Kenttä**-kentän asetuksena on **Sijainti**. Anna **Ehdot**-kenttään arvo **LPEnabled**.
6. Valitse **OK**.
7. Valitse **OK**. Etiketti luodaan ja se näkyy tulostinemulaattorisovelluksen esikatselusivulla.

![Luodun etiketin tarkistus Zpl-tulostinemulaattorisovelluksen esikatselusivulla.](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>Etiketin asettelun muokkaaminen

Voit muuttaa varastosijaintien etikettien nykyistä asettelua. Seuraavassa esimerkissä kerrotaan, miten asettelua voidaan muuttaa niin, että luoduissa etiketeissä on sijaintiprofiilin tunnus.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Määritä [ER-käyttäjäparametrin](electronic-reporting-destinations.md#applicability) **Käytä kohteita luonnostilassa** -asetuksen arvoksi **Kyllä**.
3. Laajenna **Konfiguroinnit**-sivun määrityspuussa **Varastomalli** ja valitse **Varastosijaintien etiketit**.
4. Valitse **Suunnittelu**.
5. Valitse `model.Location.Label`-tietolähde **Muodon suunnitteluohjelma** -sivun **Yhdistämismääritys**-välilehdessä.
6. Valitse **Tietolähteen ominaisuudet** -valintaikkunassa **Muokkaa** \> **Muokkaa kaavaa**.
7. Tarkista **Kaavan suunnittelu** -sivun **Kaava**-kentästä etikettien luonnissa käytettävä ER-kaava.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. Kun päivität kaavan, luotuihin etiketteihin lisätään sijaintiprofiilin tunnus.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^CF0,40,40^FO0,240^FB800,1,0,C,0^FD",@.ProfileID,"\&^FS",CrLf,
    "^XZ")
    ```

9. Valitse **Tallenna**.
10. Valitse **OK**.
11. Valitse toimintoruudussa **Suorita**.
12. Valitse **Sähköisen raportin parametrit** -valintaikkunan **Sisällytettävät tietueet** -välilehdessä **Suodata**.
13. Etsi **Alue**-välilehdessä rivi, jonka **Taulukko**-kentän asetuksena on **Sijainnit** ja **Kenttä**-kentän asetuksena on **Sijainti**. Kirjoita **Ehdot**-kenttään **Bay**.
14. Valitse **OK**.
15. Valitse **OK**. Etiketti luodaan ja se näkyy tulostinemulaattorisovelluksen esikatselusivulla.

![Tarkista Zpl-tulostinemulaattorisovelluksen esikatselusivulla luotu etiketti, joka sisältää sijaintiprofiilin tunnuksen.](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>Koodaus

> [!NOTE]
> Muokattavan ER-muodon **Yhteiset\\Tiedosto**-komponentin koodausasetus ja suunnitellun etiketin liittyvä asetus on synkronoitava. **Yhteiset\\Tiedosto**-komponentin **[Koodaus](er-suppress-bom-characters.md)**-kentän arvo ei saa olla ristiriidassa sen ZPL-komennon kanssa, jota käytetään etiketin koodausmenetelmän hallinnassa (esimerkiksi `^CI`-komento). ER ei tarkista, synkronoidaanko nämä asetukset.

## <a name="additional-resources"></a>Lisäresurssit

[Tulostinkohde](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
