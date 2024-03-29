---
title: Luotujen sähköisen raportoinnin raporttien tulosten seuraamisen ja perusarvoihin vertaamisen parannukset
description: Tässä artikkelissa käsitellään ER-perusrivitoiminnon parannuksia Microsoft Dynamics 365 Financen versiossa 10.0.3 (kesäkuu 2019).
author: kfend
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: d0f64c459ee72ffa2b0e540d4194ca887502780f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279057"
---
# <a name="improve-tracing-the-results-of-generated-er-reports-to-compare-with-baseline-values"></a>Luotujen sähköisen raportoinnin raporttien tulosten seuraamisen ja perusarvoihin vertaamisen parannukset

[!include[banner](../includes/banner.md)]

Tässä artikkelissa käsitellään ensimmäisiä sähköisen raportoinnin (ER) kehyksen perusviivatoimintoon parannuksia. Nämä parannukset ovat käytettävissä Microsoft Dynamics 365 Financen versiossa 10.0.3 (kesäkuu 2019) tai uudemmassa.

## <a name="automate-the-setting-of-baseline-rules"></a>Perusviivasääntöasetusten automatisointi

[Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md) -artikkelissa käsitellään ER-kehys määrittämistä keräämään tietoja ER-muodon suorituksista ja kyseisten suoritusten arviointia. Tämän artikkelin esimerkki sisältää suoritettavat vaiheet.

Esimerkkejä vaiheista:

- Luo lähtevä tiedosto suorittamalla ER-muoto ja tallentamalla tiedosto paikallisesti.
- Lisää paikallisesti tallennettu tiedosto ER-muotoon lisätyn perusrivin liitteenä.
- Määritä lisätyn perusrivin perusrivisääntö. Tämä määritys sisältää seuraavat vaiheet:

    - Määritä lähtevän tiedoston luontiin käytettävä ER-muotoelementti.
    - Valitse liite, joka viittaa luotuun lähtevään tiedostoon.

> [!NOTE]
> Nämä vaiheet on tehtävä manuaalisesti, vaikka ne voidaan automatisoida uusissa ER-ominaisuuksissa. Saat lisätietoja tästä toiminnosta suorittamalla seuraavan esimerkin.

## <a name="example-automate-the-setting-of-baseline-rules"></a>Esimerkki: Perusviivasääntöasetusten automatisointi

Tämän esimerkin vaiheiden suorittaminen edellyttää, että suoritat ensin [Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md) -artikkelin esimerkin vaiheet Uuden perusrivin lisääminen suunniteltuun ER-muotoon -osaan saakka.

### <a name="review-added-baseline"></a>Lisätyn perusrivin tarkasteleminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Perusrivit**.

    > [!NOTE]
    > Toimintoruudun **Perusrivit**-painike on käytettävissä vain, kun **Suorita viankorjaustilassa** -ER-käyttäjän parametri on otettu käyttöön nykyisessä yrityksessä.

Perusrivi on lisättyyn valittuun **ER-perusrivien oppimismuoto** -muotoon, mutta perusrivisääntöjä ei ole vielä lisätty tähän perusriviin.

![Sähköisen raportointimuotojen perusrivit -sivu, jossa ei ole vielä sääntöjä.](media/GER-BaselineSample-AddBaseline2.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")

### <a name="make-a-new-baseline-rule"></a>Uuden perusrivisäännön luominen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna puussa **ER-perusrivien oppimismalli**.
3. Valitse puussa **ER-perusrivien oppimismalli\\ER-perusrivien oppimismuoto**.
4. Valitse **Versiot**-pikavälilehdessä **Suorita**.
5. Kirjoita **Kirjoita tunnus** -kenttään **1**.
6. Määritä **Luo perusrivitiedostot** -asetukseksi **Kyllä**.
7. Valitse **OK**.
8. Valitse **Perusrivit**.

    ![Sähköisen raportointimuodon perusrivit -sivu, perusrivit valittu.](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")

    Luotu lähtevä tiedosto on liitetty automaattisesti suoritetun ER-muodon perusriville. Perusrivisääntö on lisätty automaattisesti tälle perusriville. Lisäksi se sisältää viittauksen liitettyyn tiedostoon.

9. Kirjoita **Nimi**-kenttään **Perusrivi 1**.
10. Kirjoita **Tiedostonimen peite** -kenttään **.xml**.
11. Valitse **Tallenna**.

### <a name="run-the-format"></a>Muodon suorittaminen

Voit nyt suorittaa [Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md) -artikkelin loput vaiheet alkaen Suunnitellun ER-muodon suorittaminen ja tulosten analysointi lokia tarkastelemalla -osasta.

> [!NOTE]
> Jos poistat automaattisesti lisätyn perusrivisäännön **Perusrivit**-pikavälilehdessä, viitattua liitettä ei poisteta automaattisesti.

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Perusrivin määrittäminen ohittamaan ER-tuloksen jatkuvasti muuttuvat osat

Jos ER-muoto on suunniteltu sisältämään tietoja, jotka muuttuvat, kun muoto suoritetaan, muodon on käytettävä ER-perusrivitoimintoa, kun luotuja tuloksia verrataan perusriviarvoihin. Tietoja voivat olla esimerkiksi käsittelypäivämäärä ja -aika tai luodun asiakirjan yksilöllinen tunniste eri muotoisina (kuten \[GUID\]-tunnus). Uusilla ER-ominaisuuksilla voi määrittää perusrivisäännön siten, että se ohittaa ER-muodon muuttuvat elementit, kun muodon suorittamisella on tarkoitus verrata perusriviarvoja ja muodon suorittamisen tuloksia. Saat lisätietoja tästä toiminnosta suorittamalla seuraavan esimerkin.

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Esimerkki: Perusrivin määrittäminen ohittamaan ER-tuloksen jatkuvasti muuttuvat osat

Tämän esimerkin vaiheiden suorittaminen edellyttää, että suoritat ensin [Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md) -artikkelin esimerkin vaiheet.

### <a name="modify-a-configured-er-format"></a>Määritetyn ER-muodon muokkaaminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna puussa **ER-perusrivien oppimismalli**.
3. Valitse puussa **ER-perusrivien oppimismalli\\ER-perusrivien oppimismuoto**.
4. Valitse **Suunnittelu**.
5. Valitse puussa **Tuloste\\Asiakirja**.
6. Valitse **Lisää**.
7. Valitse puun avattavassa valikossa **XML\\Attribute**.
8. Kirjoita **Nimi**-kenttään **ProcessingDateTime**.
9. Valitse **OK**.
10. Valitse puun **Yhdistämismääritys**-välilehdessä **Output\\Document\\ProcessingDateTime**.
11. Valitse **Muokkaa kaavaa**.
12. Lisää **Kaava**-kentässä seuraava lauseke: **DATETIMEFORMAT(NOW(), "O")**
13. Valitse ensin **Tallenna** ja sitten **Testi**.
14. Testaa määritetty lauseke uudelleen valitsemalla **Testi** uudelleen.

    ![Reseptien suunnittelu -sivu.](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Näyttökuva Reseptien suunnittelu -sivusta")

    > [!NOTE]
    > **Testin tulos** -välilehdestä havaitaan, että määritetty lauseke palauttaa eri päivämäärä- ja aika-arvon aina, kun se kutsutaan.

15. Sulje **Reseptien suunnittelu** -sivu ja valitse sitten **Tallenna**.

    ![Muodon suunnittelutoiminto -sivu.](media/GER-BaselineSample-FormatMappingDesign2.PNG "Näyttökuva Muodon suunnittelija -sivusta")

16. Sulje **Muodon suunnittelija** -sivu.

### <a name="remove-an-existing-baseline-rule"></a>Aiemmin luodun perusrivisäännön poistaminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Perusrivit**.
3. Valitse perusriviluettelossa **ER-perusrivien oppimismuoto** -muodolle määritetty perusrivi.
4. Poista aiemmin määritetty perusrivisääntö valitsemalla **Perusrivit**-pikavälilehdessä **Poista**.

![Sähköisen raportointimuotojen perusrivit -sivu, poistettu.](media/GER-BaselineSample-AddBaseline3.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")

### <a name="define-replacements-for-bindings-of-designed-er-format"></a>Suunnitellun ER-muodon sidosten korvaamisen määrittäminen

1. Valitse **Konfiguroinnit**-sivulla **Korvaava**-pikavälilehdellä **Valitse osat**.
2. Laajenna muoto-osapuussa ensin **Tuloste** ja sitten **Tuloste\\Asiakirja**. Valitse sitten **Tuloste\\Asiakirja\\ProcessingDateTime** -valintaruutu.
3. Valitse **OK**.

![Sähköisen raportointimuotojen perusrivit -sivu, osat.](media/GER-BaselineSample-AddBaseline4.PNG "Näyttökuva Sähköisen raportointimuotojen perusrivit -sivusta")

Valittu ER-muoto-osa on lisätty osaluetteloon **Korvaava**-pikavälilehteen. Kun ER-perusmuoto suoritetaan virheenkorjaustilassa, muodon kunkin osan sidonta korvataan sidonnalla, joka näkyy **Sidonta**-sarakkeessa. Voit muuttaa **Korvaava**-pikavälilehdessä mainitun osan oletussidonnan valitsemalla **Muokkaa**.

### <a name="make-a-new-baseline-rule"></a>Uuden perusrivisäännön luominen

Noudata tässä artikkelissa aiemmin olleen Esimerkki: Perusviivasääntöasetusten automatisointi -osan ohjeita. Ilmoitus varoittaa, että lähtevä tiedosto on luotu käyttämällä perusrivin asetuksia ja että muodon sidontojen pakotettu korvaus on tehty.

![Ilmoitus Konfiguroinnit-sivulla.](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Näyttökuva ilmoituksesta Konfiguroinnit-sivulla")

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a>Muodon sidosten korvaamista koskevien varoitusten piilottaminen

Määrittämällä tietyt ER-parametrit voit piilottaa muodon sidosten korvaamisesta varoittavat ilmoitukset. Tällaisesta piilottamisesta voi olla hyötyä, jos muodon sidokset korvataan valvomattomassa tilassa Regression Suite Automation Tool -työkalulla. Siinä tapauksessa varoituksen voidaan ilmaisevan, että suoritettava testitapaus on epäonnistunut.

1. Valitse **Konfiguroinnit**-sivun toimintoruudun **Konfiguroinnit**-välilehdessä **Käyttäjän parametrit**.
2. Määritä **Piilota perusrivivaroitukset** -asetukseksi **Kyllä** ja valitse sitten **OK**.

### <a name="review-the-generated-baseline-file"></a>Luodun perusrivitiedoston tarkasteleminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Perusrivit**.
3. Valitse **Liitteet**.
    > [!NOTE]
    > Luotu tiedosto sisältää käsittelypäivämäärän ja -ajan tekstin (**"#"**) lisätyssä perusrivisäännössä määritetystä sidoksesta eikä muodon sidoksesta.
    
4. Sulje **Liitteet**-sivu.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Suunnitellun ER-muoto suorittaminen ja tulosten analysointi lokia tarkastelemalla

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna puussa **ER-perusrivien oppimismalli**.
3. Valitse puussa **ER-perusrivien oppimismalli\\ER-perusrivien oppimismuoto**.
4. Valitse **Versiot**-pikavälilehdessä **Suorita**.
5. Kirjoita **Kirjoita tunnus** -kenttään **1**.
6. Valitse **OK**.
7. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Määritysten virheenkorjauslokit**.

Suorituslokissa sisältää tietoja luodun tiedoston ja määritetyn perusrivin vertailutuloksista. Loki ilmaisee, että luotu tiedosto ja perusrivi ovat samanlaiset, vaikka suoritetussa muodossa on sidonta, jolla annetaan jatkuvasti muuttuva päivämäärä- ja aika-arvo lähtevässä tiedostossa.

> [!NOTE]
> Vaikka lähtevä tiedosto on luotu käyttämällä perusriviasetuksia, jotka pakottavat muodon sidosten korvaamisen, korvaamisesta ei saada varoituksia.

## <a name="exchange-baseline-settings-between-environments"></a>Perusriviasetusten vaihtaminen ympäristöjen välillä

### <a name="export-baseline-settings"></a>Perusriviasetusten vieminen

Uusilla ER-ominaisuuksilla voi viedä valitun ER-muodon perusriviasetukset nykyisestä ympäristöstä ja tallentaa ne XML-tiedostona. 

Voit viedä perusriviasetukset valitsemalla **Sähköisen raportointimuotojen perusrivit** -sivulla **Vie**.

### <a name="import-baseline-settings"></a>Tuo perustason asetukset

Viedyt perusriviasetukset voidaan viedä toiseen ympäristöön. Ympäristö on vietävä ensin ER-muodossa. Voit sitten viedä perusriviasetukset.

Voit tuoda perusriviasetukset paikallisesti tallennetusta XML-tiedostosta valitsemalla XML-tiedoston valitsemalla **Sähköisen raportointimuotojen perusrivit** -sivulla ensin **Tuo** ja sitten **Selaa**.

![Tuo perustason asetukset -valintaikkuna.](media/GER-BaselineSample-ImportBaseline1.PNG "Näyttökuva Tuo perusriviasetukset -valintaikkunasta")

Voit tuoda perusriviasetukset Microsoft SharePoint Serveriin tallennetusta XML-tiedostosta nykyisten tiedoston hallinta-asetusten ja valitun asiakirjatyypin perusteella valitsemalla **Sähköisen raportointimuotojen perusrivit** -sivulla **Tuo lähteestä**. Valitse sitten asiakirjatyyppi ja XML-tiedosto. SharePoint-kansion käyttämiseen tarvittava asiakirjatyyppi on määritettävä etukäteen.

![Tuo lähteestä -valintaikkuna.](media/GER-BaselineSample-ImportBaseline2.PNG "Näyttökuva Tuo lähteestä -valintaikkunasta")

> [!NOTE]
> Voit tallentaa pakollisen asiakirjatyypin valintavaiheet tehtävän tallennustoiminnolla ja tiedoston nimen **Tuo lähteestä** -valintaikkunassa. Tällä tavoin voit pitää pakolliset perusriviasetukset SharePoint Serverissä ja tuoda ne sitten toistamalla tehtävätallenne, kun automatisoituja testejä suoritetaan Regression Suite Automation Tool -työkalulla.

## <a name="additional-resources"></a>Lisäresurssit

- [Luotuja raporttitulosten seuraaminen ja vertaaminen perusarvoihin](er-trace-reports-compare-baseline.md)
- [Tehtävän tallennustoiminnon resurssit](../user-interface/task-recorder.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

