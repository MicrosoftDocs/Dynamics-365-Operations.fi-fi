---
title: Sähköisen raportoinnin määritysten suunnittelu PDF-mallien täyttämiseksi
description: Tässä artikkelissa on tietoja sähköisen raportointimuodon suunnittelemiseen PDF-mallin täyttämistä varten.
author: kfend
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 4056c2b9442e26a0e1c99e6155a3cd605d222974
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283310"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a>Sähköisen raportoinnin määritysten suunnittelu PDF-mallien täyttämiseksi

[!include[banner](../includes/banner.md)]

Tämän artikkelin menetelmät ovat esimerkkejä, jotka osoittavat, miten **järjestelmänvalvoja**-roolin tai **Sähköisen raportoinnin kehittäjän** roolin käyttäjä voi määrittää sähköisen raportointimuodon (ER), joka luo raportteja PDF-tiedostoja käyttämällä täytettäviä PDF-dokumentteja raporttimalleina. Nämä vaiheet voidaan suorittaa missä tahansa Dynamics 365 Finance -yrityksessä tai Regulatory Configuration Servicesissä (RCS).

## <a name="prerequisites"></a>Edellytykset

Ennen aloittamista sinulla on oltava jokin seuraavista käyttötyypeistä sen mukaan, mitä palvelua käytät tämän artikkelin suorittamisessa:

- Finance-käyttöoikeudet seuraaville rooleille:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

- RCS-käyttöoikeudet seuraaville rooleille:

    - Sähköisen raportoinnin kehittäjä
    - Sähköisen raportoinnin toiminnallinen konsultti
    - Järjestelmänvalvoja

Sinun on myös toteutettava menettely [Konfiguraatiopalvelujen luominen ja niiden merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md).

Lataa lopuksi seuraavat tiedostot.

| Sisällön kuvaus                       | Tiedostonimi                                     |
|-------------------------------------------|-----------------------------------------------|
| Raportin ensimmäisen sivun malli | [IntrastatReportTemplate1.pdf](https://download.microsoft.com/download/0/8/3/0832c82b-4448-4562-afbf-01e0efc8d999/IntrastatReportTemplate1.pdf)                  |
| Raportin seuraavien sivujen malli    | [IntrastatReportTemplate2.pdf](https://download.microsoft.com/download/c/7/a/c7a8a806-2192-4034-9052-e8b84b527d5e/IntrastatReportTemplate2.pdf)                  |
| Sähköisen raportoinnin esimerkkimuoto - PDF                          | [Intrastat report (PDF).version.1.1.xml](https://download.microsoft.com/download/a/8/7/a87aea3e-3f60-404c-8899-c471d20e7ea9/IntrastatreportPDFversion1.1.xml)        |
| Sähköisen raportoinnin esimerkkimuoto - Excel                          | [Intrastat (import from Excel).version.1.1.xml](https://download.microsoft.com/download/a/2/c/a2c0c145-d989-4e55-9d47-9647c02e4ee4/IntrastatimportfromExcelversion1.1.xml) |
| Tietojoukon malli                            | [Intrastat sample data.xlsx](https://download.microsoft.com/download/9/f/1/9f1c5b96-3800-475f-8cf6-1ddd42873758/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a>Suunnittele muotokonfiguraatio

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Saat luettelon Microsoftin tarjoamista kokoonpanoista

1. Siirry kohtaan **Organisaation hallinto \> Työtilat \> Sähköinen raportointi**.
2. Varmista, että **Litware, Inc.** -palveluntarjoaja on käytettävissä ja merkittynä aktiiviseksi.
3. Valitse **Microsoft**-palveluntarjoajan ruudusta **Arkistot**.

    > [!NOTE]
    > Jos **LCS**-tyypin säilö on jo olemassa, ohita tämän toimenpiteen muut vaiheet.

4. Valitse **Lisää**.
5. Valitse avattavasta valintaikkunasta **Konfiguraatiosäilön tyyppi** -kenttä ryhmästä **LCS**-vaihtoehto.
6. Valitse **Luo säilö**.
7. Valitse **OK**.

### <a name="get-the-model-configurations-provided-by-microsoft"></a>Hae Microsoftin mallikokoonpanot

1. Valitse **Konfigurointiarkistot**-sivun vasemmasta reunasta **Näytä suodattimet** -painike (suppilon symboli).
2. Lisää suodatin **LCS**:n arvoon **Tyyppi**-kentässä ja käytä **alkaa**-operaattoria.
3. Valitse **Käytä**.
4. Valitse **Avaa**.
5. Valitse puussa **Intrastat-malli**.
6. Valitse **Versiot**-pikavälilehdessä versio **1**.

    > [!NOTE]
    > Jos **Tuo**-painike **Versiot**-pikavälilehdellä ei ole käytettävissä, ohita tämän toimenpiteen muut vaiheet.

7. Valitse **Tuo**.
8. Valitse **Kyllä** vahvistaaksesi **Intrastat-mallin** kokoonpanon valitun version tuonnin.

### <a name="create-a-new-format-configuration"></a>Uuden muotokonfiguraation luominen

1. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.
2. Valitse puussa **Intrastat-malli**.
3. Valitse **Luo konfiguraatio**.

    > [!NOTE]
    > Jos **Luo konfigurointi** -painike ei ole käytettävissä, sinun on otettava suunnittelutila käyttöön **Sähköisen raportoinnin parametrit** -sivulla, joka voidaan avata **Sähköinen raportointi** -työtilassa.

4. Valitse avattavasta valintaikkunasta **Uusi**-kenttäryhmä, valitse **Muoto, joka perustuu Intrastat-tietomalli** -vaihtoehtoon.
5. Kirjoita **Nimi**-kenttään **Intrastat-raportti (PDF)**.
6. Kirjoita **Kuvaus**-kenttään **Intrastat-raportti PDF-muodossa**.

    > [!NOTE]
    > Aktiivinen konfiguraation lähde syötetään automaattisesti. Tämä lähde voi ylläpitää tätä konfiguraatiota. Vaikka muut lähteet voivat käyttää tätä konfiguraatiota, ne eivät voi ylläpitää sitä.

7. Valinnainen: **Muototyyppi**-kentässä voit valita tietyn sähköisen asiakirjan muodon. Jos valitset suunnitteluvaiheessa **PDF**, sähköisen raportoinnin toimintojen suunnittelija tarjoaa vain muodon elementit, joita voidaan soveltaa vain PDF-muodossa luotuihin asiakirjoihin (**PDF\Tiedosto**, **PDF\PDF Merger**, jne.). Jos jätät tämän kentän tyhjäksi, suunnitteluvaiheessa määritetään sähköinen tiedostomuoto sähköisen raportoinnin toimintojen suunnittelutoiminnossa, kun ensimmäinen muotoelementti lisätään. Jos esimerkiksi lisäät **Excel\file** -tiedoston ensimmäisenä muotoelementtinä, sähköisen raportoinnin toimintojen suunnittelutoiminto tarjoaa vain muotoiluelementit, joita voidaan soveltaa vain Excel-muodossa luotuihin asiakirjoihin (**Excel\Cell**, **Excel\Range**, jne.). muoto.
8. Valitse **Luo konfiguraatio**.

Uusi sähköisen raportoinnin muotokonfiguraatio on luotu. Tämän kokoonpanon luonnosversion avulla voit tallentaa sähköisen raportoinnin muotokomponentin, joka on suunniteltu tuottamaan sähköisiä asiakirjoja PDF-muodossa.

### <a name="design-the-format-of-an-electronic-document"></a>Sähköisen asiakirjan muodon suunnitteleminen

Seuraavaksi suunnitellussa sähköisen raportoinnin muotokokoonpanossa voit suunnitella sähköisen raportin muodon, joka tuottaa **Intrastat-ohjaus**-raportin PDF-muodossa. Tämän raportin ensimmäisellä sivulla on oltava yhteenveto raportista sekä tiedot raportoiduista ulkomaankauppatapahtumista. Muilla sivuilla on oltava vain raportoitujen ulkomaankaupan tapahtumien tiedot. Koska luoduilla raporttisivuilla on oltava eri asetteluja, sähköisen raportoinnin muodossa käytetään kahta eri mallia PDF-muodossa.

Avaa lataamasi PDF-mallit missä tahansa PDF-katseluohjelmassa. Huomaa, että jokainen malli sisältää useita kenttiä, jotka on täytettävä. Jokaisessa mallissa ulkomaankaupan tapahtumien tiedot esitetään 42 rivillä, joista jokaisessa on yhdeksän kenttää. Rivinumero näkyy kunkin kentän nimen lopussa (esimerkiksi **Päiväys 1**...**Päiväys 42** ja **Kauppatavara 1**...**Kauppatavara 42**).

Seuraavassa kuvassa näkyy raportin ensimmäisen sivun PDF-malli.

![Malli 1.](media/rcs-ger-filloutpdf-template1.png)

Seuraavassa kuvassa näkyy raportin seuraavien sivujen PDF-malli.

![Malli 2.](media/rcs-ger-filloutpdf-template2.png)

1. Valitse **Määritys**-sivulla **Suunnittelija**.
2. Valitse **Lisää pääkansio**.
3. Valitse avattavasta valintaikkunan puusta **PDF \> PDF Merger**.

    Kun valitset muodon pääelementiksi **PDF Merger** -elementin, kaikki suorituksen aikana luodut PDF-dokumentit yhdistetään yhdeksi lopulliseksi PDF-dokumentiksi. Jos tarvitset vain yhden PDF-mallin, jotta voisit luoda kaikki tarvittavat tiedostot suunnittelemaasi sähköisen raportoinnin muotoa käyttäen, voit valita pääelementiksi **PDF**-tiedoston.

4. Kirjoita **Nimi**-kenttään **Tulos**.
5. Valitse **Kieliasetukset**-kentässä **Käyttäjän asetukset**. Raportti luodaan sitä suorittavan käyttäjän ensisijakielellä.
6. Valitse **Kulttuuriasetukset**-kentässä **Käyttäjän asetukset**. Raportin sivuilla näkyvät arvot ja päivämäärät muotoillaan raportin suorittavan käyttäjän ensisijaisen alueen perusteella.
7. Valitse **OK**.
8. Valitse toimintoruudun **Tuo**-välilehdessä **Tuo PDF:stä**.

    Kun täytettävissä oleva PDF-tiedosto tuodaan tämän sähköisen raportoinnin muodon mallina, kaikki vaaditut sähköisen raportoinnin muodon elementit (**PDF-tiedosto**, **Kenttäryhmä** ja **Kenttä**-elementit) luodaan automaattisesti muodossa, joka on suunniteltu tuotavan PDF-tiedoston rakenteen mukaan.

9. Valitse **Selaa**. Siirry-kohtaan ja valitse **IntrastatReportTemplate1.pdf**-tiedosto, jonka latasit aiemmin edellytyksenä.
10. Valitse **OK**.

    Valittu tiedosto ladataan, ja **Malli**-kenttä **Tuo PDF:stä** -valintaikkunassa täytetään.

11. Määritä **Ryhmäkentät** -asetukseksi **Kyllä**. Jos valittu PDF-tiedosto sisältää kenttäryhmiä, niitä käytetään ryhmiteltäessä luotuja sähköisen raportoinnin muotoelementtejä. Tähän tarkoitukseen luodaan **Kenttäryhmän** muotoelementti.

    Jos tämän asetuksen arvoksi on määritetty **Ei**, tarvittavat sähköisen raportoinnin muotoelementit luodaan tasaisena luettelona elementeille, jotka on upotettu **PDF-tiedosto**-muotoelementtiin.

12. Valitse **OK**.

    ![Tuo PDF-valintaikkunasta.](media/rcs-ger-filloutpdf-importtemplate.png)

13. Laajenna puussa kohde **Tuotos**.

    Huomaa, että **PDF-tiedosto**-komponentti on luotu automaattisesti, jotta voidaan hallita suorituksen aikana luodun raportin ensimmäisen sivun luontia.

14. Laajenna puussa kohde **Tuotos \> PDF-tiedosto**.

    Huomaa, että muotoelementtien rakenneluettelo on luotu automaattisesti tässä sähköisen raportoinnin muodossa aiemmin tuodun täytettävän PDF-tiedoston rakenteen perusteella.

15. Valitse puussa kohde **Tuotos \> PDF-tiedosto**.
16. Kirjoita **Nimi**-kenttään **Sivu 1**.

    Tätä muotoelementtiä käytetään **Intrastat-ohjaus**-raportin ensimmäisen sivun muodostamiseen. Tämä sivu näyttää yhteenvedon raportista ja tiedot ulkomaankauppatapahtumista.

    Jos jätät **Kieliasetukset**-kentän tyhjäksi, valitut **Kieliasetukset** **PDF Merger** -pääelementissä määräävät tämän muodon avulla luodun raportin kielen. Voit ohittaa pääelementin asetuksen valitsemalla toisen arvon.

    Jos jätät **Kulttuuriasetukset**-kentän tyhjäksi, valitut **Kulttuuriasetukset** **PDF Merger** -pääelementissä määräävät tämän muodon avulla luodun raportin sijainnin. Sijainti määrittää raportin sivujen arvojen ja päivämäärien muodon. Voit ohittaa pääelementin asetuksen valitsemalla toisen arvon.

17. Valitse toimintoruudun **Tuonti**-välilehti. Huomaa, että **Päivitä PDF:stä** -painike on tullut saataville valittuun muotoelementtiin, **PDF-tiedostoon**.

    Tämän painikkeen avulla voit tuoda päivitetyn PDF-mallin muokattua muotoa. Kun päivitetty PDF-malli tuodaan, muotoelementtien luettelo muuttuu vastaavasti:

    - Jos kyseessä on päivitetty PDF-mallin uusi kenttä, uudet muotoelementit luodaan muokattua sähköisen raportoinnin muotoa varten.
    - Jos päivitetty PDF-malli ei enää sisällä kenttiä, jotka vastaavat muokattua sähköisen raportoinnin aiemmin luotuja muotoelementtejä, nämä muotoelementit poistetaan sähköisen raportoinnin muodosta.

18. Valitse **Muoto **-välilehdestä** Liitteet**.

    Huomaa, että tuotu PDF-tiedosto on liitetty muokattuun sähköisen raportoinnin muotoon.

    ![PDF-liitteen esikatselu.](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. Jatka tämän muodon suunnittelua tuomalla toinen PDF-malli, lisäämällä tarvittavat sidokset tietolähteisiin ja niin edelleen.
20. Valitse **Tallenna**.
21. Sulje sivu.
22. Valitse **Poista**.
23. Valitse **Kyllä**.

Jos haluat tietää miten uusia **PDF Merger-**, **PDF-tiedosto-**, **Kenttäryhmä-** ja **Kenttä-** muotoelementtejä voidaan käyttää luotaessa PDF-muotoisia tiedostoja, voit tuoda ja analysoida sähköisen raportoinnin muotomalleja.

### <a name="import-the-format-configuration"></a>Tuo muotokonfiguraatio

Seuraavaksi tuot aiemmin lataamasi sähköisen raportoinnin esimerkkimuodon **Intrastat-ohjaus**-raportin luomista varten PDF-muodossa. Raportin ensimmäisellä sivulla on oltava yhteenveto raportista sekä tiedot raportoiduista ulkomaankauppatapahtumista. Muilla sivuilla on oltava vain raportoitujen ulkomaankaupan tapahtumien tiedot.

1. Valitse **Konfiguraatiot**-sivulla **Vaihto \> Lataa XML-tiedostosta**.
2. Valitse **Selaa**. Siirry-kohtaan ja valitse **Intrastat report (PDF).version.1.1.xml**-tiedosto, jonka latasit aiemmin edellytyksenä.
3. Valitse **OK**.

## <a name="analyze-the-format-configuration"></a>Analysoi muotokonfiguraatio

### <a name="format-layout"></a>Muotoilun asettelu

1. Valitse **Konfiguraatiot**-sivun puun kohdasta **Intrastat-malli \> Intrastat-raportti (PDF)**.
2. Valitse **Suunnittelu**.
3. Valitse **Näytä tiedot**.
4. Laajenna puussa kohde **Tuotos: PDF Merger**.

    Huomaa, että tämä sähköisen raportoinnin muoto sisältää kaksi **PDF-tiedosto**-elementtiä, joista kukin käyttää eri PDF-mallia. Yhden mallin avulla luodaan raportin ensimmäinen sivu PDF-muodossa, ja toista mallia käytetään muiden sivujen muodostamiseen.

5. Laajenna puussa **Tuloste: PDF Merger \> Sivu 1: PDF-tiedosto (IntrastatReportTemplate1).**
6. Laajenna puussa **Tuloste: PDF Merger \> Sivu N: PDF-tiedosto (IntrastatReportTemplate2)**.

    Huomaa, että koska kahden PDF-mallin sisältö eroaa toisistaan, myös kahden sisäkkäisen **PDF-tiedoston** elementtien muotorakenne eroaa toisistaan.

### <a name="format-mapping"></a>Muodon yhdistäminen

1. Valitse **Muodon suunnittelu** -sivulla **Yhdistämismääritys**-välilehti.
2. Laajenna puussa **Sivutus \> Sivut**.

    ![Kaavan suunnittelusivu, jossa mallipuuta laajennetaan.](media/rcs-ger-filloutpdf-reviewformat.png)

    Ota seuraavat seikat huomioon:

    - **Tuloste \> Sivu 1**-muodon elementti **PDF-tiedosto** tyypissä ei ole sidottu mihinkään tietolähteeseen ja tämän muotoisen elementin **käytössä oleva** lauseke on tyhjä. Tämän vuoksi **IntrastatReportTemplate1**-PDF-malli täytetään suorituksen aikana vain kerran yksittäisen PDF-tiedoston luonnin yhteydessä.
    - **Syöte \> Sivu N** -muotoelementti **PDF-tiedosto**-tyypissä on sidottu **Paging.PageN**-tietolähteeseen ja tämän muotoelementin **Tietoluettelo**-tyypin **Otettu käyttöön**-lauseke on tyhjä Tämän vuoksi **IntrastatReportTemplate2**-PDF-malli täytetään jokaiselle tietueelle sidotusta tallennusluettelosta, kun yksittäinen PDF-dokumentti luodaan.
    - Koska **Sivu 1: PDF-tiedosto**- ja **sivu N: PDF-tiedosto** -muotoelementit ovat **Syöte: PDF Merger** -muotoelementin lapsia, kaikki täytetyt PDF-tiedostot yhdistetään yhdeksi lopulliseksi PDF-dokumentiksi.
    - **Paging.Page1**- ja **Paging.PageN**-tietolähteet on määritetty tietueiden suodattimiksi **Paging.Pages** -tietolähteelle. Tämä tietolähde on määritetty jakamaan koko ulkomaankauppatapahtuman joukon eriin. Kussakin erässä on enintään 42 tietuetta. Seuraavan sähköisen raportoinnin lausekkeen avulla tapahtumat jaetaan eriin:

        SPLITLIST(Totals.CommodityRecord,42)

    - **Paging.Pages**-tietolähde sisältää **Paging.Pages.Enumerated**-elementin, joka palauttaa kunkin erään sisältyvän tietueen tiedot. Nämä tiedot sisältävät tietueen järjestyksen nykyisessä erässä (**Paging.Pages.Enumerated.Number**-kenttä). **Paging.Pages.Enumerated.Number**-kenttää käytetään **Nimi**-lausekkeessa **PDF-kenttä**-muotoelementeissä, jolloin luodaan dynaamisesti kentän nimi, joka perustuu erän tapahtumanumeroon. Luodun kentän nimen avulla täytetään oikea PDF-kenttä käytössä olevalla PDF-mallilla.
    - **Tuloste \> Sivu N \> Tiedot 2** -muotoelementti **PDF-ryhmä**-tyypille on sidottu **Paging.PageN.Enumerated**-tietolähteeseen (tai **\@.Enumerated** jos **Suhteellinen polku**-katselutilaa käytetään) **Tietoluettelo**-tyyppiin. Tämän vuoksi tämän PDF-ryhmän sisäkkäiset elementit täytetään suorituksen aikana kunkin sidotun tietueluettelon tietueen osalta. Näin, yksilölliset PDF-rivit syntyvät käytännössä, kun kunkin N:s 42:sta tietueesta **Paging.PageN.Enumerated**-luettelossa seuraavat PDF-kentät täytetään: Päiväys N, suunta N, hyödyke N, jne. Tämän vuoksi tämän **Kenttäryhmän** muoto-elementin käyttäytyminen muistuttaa **XML \>sarja**- ja **Teksti \>Sekvenssi** -muodon elementtien toimintaa.

3. Laajenna puussa **Tuloste \> Sivu N \> Details2**.
4. Valitse puussa **Tuloste \> Sivu N \> Details2 \> PageFooter**.

    Huomaa, että tämän muotoelementin **Nimi**-määrite on määritetty **PageFooter**-määritteeksi. Huomaa myös, että muotoelementin **Nimi**-lauseke on tyhjä.

5. Valitse puussa **Tuloste \> Sivu N \> Details2 \> Correction 1**.

    Huomaa, että tämän muotoelementin **Nimi**-määrite on määritetty **Correction 1**-määritteeksi. Huomaa myös, että **Nimi**-elementin nimilauseke määritetään mallilla **Paging.FldName("Correction"\@. Number)**.

![Muotoilun suunnittelu, jossa yhdistämismääritys on valittuna.](media/rcs-ger-filloutpdf-reviewformat2.png)

Huomaa, että **Kentän** muotoiluelementin avulla täytetään täytettävän PDF-tiedoston yksittäisen kenttä, joka määritetään pää-**PDF-tiedosto**-muodon elementin malliksi. **PDF-tiedosto**-muotoelementin tai sen sisäkkäisten elementtien sidonta, jos siinä on sisäkkäisiä elementtejä, määrittää vastaaviin PDF-kenttiin kirjoitetun arvon. **Kentän** muotoiluelementin eri ominaisuuksien avulla voit määrittää, mikä PDF-kenttä täytetään yksittäisen muotoelementin avulla:

- **Muoto**-välilehdessä **Nimi**-määritteen muotoelementti
- **Yhdistäminen**-välilehdessä **Nimi**-lausekkeen muotoelementti

Koska kumpikin ominaisuus on valinnainen **Kentän** muotoelementissä, kohde-PDF-kentän määrittämiseen sovelletaan seuraavia sääntöjä:

- Jos **Nimi**-määrite on tyhjä ja **Nimi**-lauseke palauttaa tyhjän merkkijonon suorituksen aikana, poikkeus heitetään suorituksen aikana, jotta se ilmoittaa käyttäjälle, että PDF-kenttää ei löydy PDF-mallista, jota käytetään PDF-tiedoston täyttämiseen.
- Jos **Nimi**-määrite on määritetty ja **Nimi**-lauseke on tyhjä, täytetään PDF-kenttä, jolla on sama nimi kuin Kaava-elementin **Nimi**-määritteellä.
- Jos **Nimi**-määrite on määritetty ja **Nimi**-lauseke on konfiguroitu, täytetään PDF-kenttä, jolla on sama nimi kuin arvolla, jonka kaavaelementin **Nimi**-määrite on palauttanut.

> [!NOTE]
> Kun PDF-mallin valintaruutu ei kuulu valintaruuturyhmään, sitä esitetään muokattavassa ER-muodossa **PDF-tiedoston** elementin alle kuuluvana **Kenttä**-elementtinä. Tämän tyypin PDF-valintaruudun voi määrittää seuraavasti:
>
> - Vastaava **Kenttä**-muotoelementti on sidottu sellaisen *[Totuusarvon](er-formula-supported-data-types-primitive.md#boolean)* tietotyyppiin, jonka arvo on **Tosi**.
> - Vastaava **Kenttä**-muotoelementti sisältää sisäkkäisen **Merkkijono**-muotoelementin, joka on sidottu tietolähdekenttään, jonka tekstiarvo on **1**, **Tosi** tai **Kyllä**.
>
> Malli voi sisältää valintaruuturyhmän, ja vain yksi valintaruutu voidaan valita kerralla. Valintaruudut näkyvät PDF-mallissa *VALINTARUUTU*-tyypin usean lomakkeen kenttinä. Kullakin kentällä on sama nimi, mutta vientiarvo on eri. Kun tuot mallin muokattavaan ER-muotoon, jokainen valintaruutu näkyy lomakkeen hierarkkisessa rakenteessa **Valintaruuturyhmänimikkeenä**, joka on saman **Valintaruuturyhmä**-elementin alla. **Valintaruuturyhmän** elementin nimi on sama kuin PDF-mallin valintaruutukenttien nimi. Kunkin **Valintaruuturyhmänimikkeen** elementin nimi on sama kuin PDF-mallin vastaavan valintaruutukentän vientiarvo.
>
> **Valintaruuturyhmänimikkeen** elementin voi liittää vain *Boolean*-tietotyypin tietolähdekenttään.

## <a name="run-the-format-configuration"></a>Suorita muotokonfiguraatio

### <a name="import-the-format-configuration"></a>Tuo muotokonfiguraatio

Seuraavaksi lataat **Intrastatin (tuonti Excelistä)** sähköisen raportoinnin esimerkkimuodon. Tämä muoto on suunniteltu siten, että se jäsentää käyttäjän valitseman Microsoft Excel-työkirjan, joka simuloi ulkomaankaupan tapahtumia.

1. Valitse **Konfiguraatiot**-sivulla **Vaihto \> Lataa XML-tiedostosta**.
2. Valitse **Selaa**. Siirry ja valitse **Intrastat (Tuo Excelistä).version.1.1.xml**-tiedosto, jonka latasit aiemmin edellytyksenä.
3. Valitse **OK**.
4. Valitse puussa **Intrastat-malli \> Intrastat (tuo Excelistä)**.
5. Valitse **Muokkaa**.
6. Määritä **Mallin yhdistämisasetuksen** oletusarvoksi **Kyllä**.

    > [!NOTE]
    > Jos olet aiemmin määrittänyt **Mallin yhdistämisasetuksen oletusarvon** arvoksi **Kyllä**, **Intrastat-mallin** konfiguroinnissa tai muussa **Intrastat-mallin** mukaan upotetussa konfiguraatiossa, määritä asetukseksi **Ei.**

    Kun **Mallin yhdistämismäärityksen** oletusarvoksi on määritetty **Kyllä**, tuotu **Intrastat (tuotu Excelistä)**-sähköisen raportoinnin muoto määritetään oletustietolähteeksi **Intrastat-raportin (PDF)** konfiguroinnin muodolle. Kun **Intrastat-raportti (PDF)**-muoto määritetään, **Intrastat (tuonti Excelistä)**-muodossa jäsennetty Excel-työkirjan sisältö simuloi ulkomaankaupan tapahtumia, jotka on raportoitu. Seuraavassa kuvassa on Excel-työkirjan esimerkki.

    ![Mallitietoja sisältävä Excel-työkirja.](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a>Suorita muotokonfiguraatio

1. Valitse **Konfiguraatiot**-sivun puun kohdasta **Intrastat-malli \> Intrastat-raportti (PDF)**.
2. Valitse **Suorita**.
3. Valitse **Selaa**. Siirry-kohtaan ja valitse **Intrastat sample data.xlsx**-tiedosto, jonka latasit aiemmin edellytyksenä.
4. Valitse **OK**.
5. Valitse **Raportin suunta**-kentässä **Molemmat**, jos haluat täyttää kaikki tuodun Excel-työkirjan tapahtumat luotuna PDF-raporttina.
6. Valitse **OK**.
7. Tarkista muodostettu PDF-dokumentti.

Seuraavassa kuvassa näkyy esimerkki luotavan raportin ensimmäisestä sivusta.

![Luodun raportin ensimmäinen sivu.](media/rcs-ger-filloutpdf-generatedreport.png)

Seuraavassa kuvassa näkyy esimerkki luotavan raportin toisesta sivusta.

![Luodun raportin toinen sivu.](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="limitations"></a>Rajoitukset

Täytettävien kenttien nimien on oltava yksilöllisiä PDF-lomakkeessa, jota aiot käyttää raporttimallina. Jokaista tällaista kenttää varten luodaan muokattavassa ER-muodossa oma muotoelementti, jolla on vastaava nimi, kun PDF-lomake tuodaan. Jos PDF-lomakkeessa on useita kenttiä, joilla on sama nimi, luodaan yksi muotoelementti kentille, joita ei voi täyttää erikseen ajon aikana.

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

### <a name="when-i-run-the-er-format-to-generate-a-report-in-pdf-format-why-do-i-get-the-following-errors--cannot-handle-iref-streams-the-current-implementation-of-pdfsharp-cannot-handle-this-pdf-feature-introduced-with-acrobat-6-and-a-pdf-name-must-start-with-a-slash-"></a>Kun muodostan raportin PDF-muodossa ajamalla ER-muodon, miksi saan seuraavat virheet:  **iref-virtoja ei voi lukea. Nykyinen PDFSharp-toteutus ei voi käsitellä tätä Acrobat 6:n PDF-ominaisuutta.** ja **PDF-tiedoston nimi on aloitettava vinoviivalla (/).**

ER-kehys luo nämä PDF-raportit PDFSharp-kirjaston version 1.5 avulla. Jotkin PDF 1.5 -ominaisuudet (Adobe Reader 6.0) eivät ole vielä käytössä tässä kirjastossa. Siksi PDFSharp ei voi vielä avata joitakin tiedostoja, jotka on merkitty **PDF 1.5 -tiedostoiksi tai uudemmaksi versioksi** ja jotka voivat aiheuttaa kyseiset virheet. Ratkaise ongelma valitsemalla yksi seuraavista ratkaisuista:

-   Kun käytät omaa PDF-mallia: Palauta malli aiempaan Adobe-versioon ja aloita uuden mallin käyttö ER-muodossa.
-   Kun käytät toisen konfiguraation tarjoajan sinulle jakamaa ER-muotomallia osana ER-ratkaisua: Ota yhteyttä tämän ER-ratkaisun omistajaan ja anna ongelman kuvaus.
-   Kun käytät PDFSharp-kirjaston aiemman version sisältävää ISV-ratkaisua: Ota yhteyttä ratkaisun omistajaan ja ehdota päivitystä uuteen PDFSharp-versioon.

## <a name="additional-resources"></a>Lisäresurssit

- [ER OPENXML-muodossa luotavien raporttien määritysten suunnittelu (marraskuu 2016)](tasks/er-design-reports-openxml-2016-11.md)
- [Suunnittele ER-konfiguraatiot voidaksesi luoda raportteja Word-muodossa](tasks/er-design-configuration-word-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
