---
title: Konfiguraatioiden suunnitteleminen asiakirjojen luomiseksi Excel-muodossa
description: Tässä artikkelissa käsitellään Excel-mallin täyttävän sähköisen raportointimuodon (ER-muodon) suunnittelua ja lähtevien Excel-muotoisten tiedostojen luontia.
author: kfend
ms.date: 05/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.form: EROperationDesigner, ERParameters
ms.openlocfilehash: 2feadf8e196936220cf557989cae40b742447d99
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280921"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Excel-muotoisia tiedostoja luovan määrityksen suunnitteleminen

[!include[banner](../includes/banner.md)]

Voit suunnitella [sähköisen raportoinnin (ER)](general-electronic-reporting.md) muotomäärityksen, jonka ER-muoto-osan voi määrittää luomaan lähtevän tiedoston Microsoft Excel -muotoisena työkirjana. Tätä tarkoitusta varten on käytettävä tiettyjä ER-muoto-osia.

Lisätietoja tästä toiminnosta on artikkelin [Konfiguraation suunnitteleminen raporttien luomiseksi OPENXML-muodossa](tasks/er-design-reports-openxml-2016-11.md) ohjeissa.

## <a name="add-a-new-er-format"></a>Uuden ER-muodon lisääminen

Kun Excel-työkirjamuotoisen lähtevän tiedoston luontia varten lisätään uusi ER-muotomääritys, muodon **Muodon tyyppi** -määritteeksi on joko valittava **Excel**-arvo tai **Muodon tyyppi** -määrite on jätettävä tyhjäksi.

- Jos valitse **Excel**, muoto voidaan määrittää luomaan lähtevä tiedosto vain Excel-muodossa.
- Jos määrite jätetään tyhjäksi, voit määrittää lähtevän tiedoston luovaksi muodoksi minkä tahansa ER-kehyksen tukeman muodon.

Määrityksen Er-muoto-osa määritetään valitsemalla toimintoruudussa **Suunnitteluohjelma** ja avaamalla ER-muoto-osa muokattavaksi ER-toiminnon suunnitteluohjelmassa.

![Konfiguraatiot-sivu.](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Excel-tiedosto-osa

### <a name="manual-entry"></a>Manuaalinen kirjaus

**Excel\\Tiedosto**-osa on lisättävä määritettyyn ER-muotoon luomaan lähtevä tiedosto Excel-muodossa.

![Excel\Tiedosto-osa.](./media/er-excel-format-add-file-component.png)

Lähtevän tiedoston asettelu määritetään liittämällä Excel-työkirja, jossa on .xlsx-tunniste, **Excel\\Tiedosto**-osaan lähtevien tiedostojen mallina.

> [!NOTE]
> Jos malli liitetään manuaalisesti, käytettävän [tiedostotyypin](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types) on oltava määritetty tätä tarkoitusta varten [ER-parametreissa](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Liitteen lisääminen Excel\Tiedosto-osaan.](./media/er-excel-format-add-file-component2.png)

Voit määrittää tavan, jolla liitetty malli täytetään määritettyä ER-muotoa suoritettaessa, lisäämällä sisäkkäiset **Taulukko**-, **Alue**- ja **Solu**-osat **Excel\\Tiedosto**-osaan. Kukin sisäkkäinen osa on liitettävä Excelin nimettyyn kohteeseen.

### <a name="template-import"></a>Mallin tuonti

Uusi malli voidaan tuoda tyhjään ER-muotoon valitsemalla **Tuo Excelistä** toimintoruudun **Tuonti**-välilehdessä. Tässä esimerkissä **Excel\\Tiedosto**-osa luodaan automaattisesti ja tuotu malli liitetään siihen. Myös kaikki pakolliset ER-osat luodaan automaattisesti löydetyn Excelin nimettyjen kohteiden luettelon perusteella.

![Tuo Excelistä -toiminnon valinta.](./media/er-excel-format-import-template.png)

> [!NOTE]
> Jos muokattavaan ER-muotoon halutaan luoda valinnainen **Taulukko**-elementti, määritä **Luo Excel-taulukkomuotoinen elementti** -asetukseksi **Kyllä**.

## <a name="sheet-component"></a>Taulukko-osa

**Taulukko**-osa ilmaisee sen liitetyn Excel-työtyökirjan laskentataulukon, joka on täytettävä. Excel-mallissa olevan laskentataulukon nimi määritetään tämän osan **Taulukko**-ominaisuudessa.

> [!NOTE]
> Tämä osa on valinnainen vain yhden laskentataulukon sisältävissä Excel-työkirjoissa.

ER-toiminnon suunnitteluohjelman **Yhdistämismääritys**-välilehdessä **Taulukko**-osan **Käytössä**-ominaisuus voidaan määrittää määrittämään, onko osa sijoitettava luotuun tiedostoon:

- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Tosi** tai jos mitään lauseketta ei ole määritetty, sopiva laskentataulukko asetetaan luotuun tiedostoon.
- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Epätosi**, luotu tiedosto ei sisällä laskentataulukkoa.

![Esimerkki Taulukko-osasta.](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Alue-osa

### <a name="nested-components"></a>Sisäkkäiset komponentit

#### <a name="data-typing"></a>Tietojen tyypitys

**Alue**-osassa voi olla muita sisäkkäisiä ER-osia, joiden avulla annetaan arvoja soveltuvilla alueilla.

- Jos arvoja annetaan jollakin **Teksti**-ryhmän osalla, arvo annetaan Excel-alueella tekstiarvona.

    > [!NOTE]
    > Tämän mallin avulla voi muotoilla annettuja arvoja sovelluksen määritettyjen alueasetusten perusteella.

- Jos **Excel**-ryhmän **Solu**-osaa käytetään arvojen antamiseen, arvo annetaan Excel-alueelle sen tietotyypin arvona, joka on määritetty kyseisen **Solu**-osan sidonnalla. Tietotyyppi voi olla esimerkiksi **Merkkijono**, **Reaaliluku** tai **Kokonaisluku**.

    > [!NOTE]
    > Tämän mallin avulla Excel-sovelluksessa voidaan ottaa käyttöön annettujen arvojen muotoilu sen paikallisen tietokoneen alueasetusten perusteella, joka avaa lähtevän tiedoston.

#### <a name="row-handling"></a>Rivien käsittely

**Alue**-komponentti voidaan konfiguroida pystysuunnassa replikoiduiksi, jotta Excel-laskentataulukossa luodaan useita rivejä. Rivit voi luoda ylätason **Alue**-komponentin tai sen sisäkkäisten **Alue**-komponenttien avulla.

Versiossa 10.0.26 ja sitä myöhemmissä versioissa voit pakottaa luodun laskentataulukon pitämään luodut rivit samalla sivulla. Määritä ER-muotosuunnittelussa **Pidä rivit yhdessä** -asetukseksi **Kyllä** ylätason **Alue**-komponentille muokattavassa ER-muodossa. ER yrittää tällöin säilyttää kyseisen alueen luoman sisällön samalla sivulla. Jos sisällön korkeus ylittää nykyisen sivun jäljellä olevan tilan, sivunvaihto lisätään ja sisältö alkaa seuraavan uuden sivun yläosasta.

> [!NOTE]
> On suositeltavaa määrittää **Pidä rivit yhdessä** -vaihtoehto vain alueille, jotka kattavat luodun tiedoston koko leveyden.
>
> **Pidä rivit yhdessä** -vaihtoehto koskee vain **Excel \> Tiedosto** -komponentteja, jotka on määritetty käyttämään Excel-työkirjamallia.
>
> **Pidä rivit yhdessä**-asetusta voidaan käyttää vain, kun **Ota käyttöön EPPlus-kirjasto sähköisen raportoinnin sovelluskehyksessä** -ominaisuus on otettu käyttöön.
>
> Tätä toimintoa voidaan käyttää **Sivu**-osan **Alue**-komponentteihin. Ei kuitenkaan voida taata, että sivun [alatunnisteiden kokonaissummat](er-paginate-excel-reports.md#add-data-sources-to-calculate-page-footer-totals) lasketaan oikein [Tietojen keruu](er-data-collection-data-sources.md) -tietolähteiden avulla.

Tietoja tämän asetuksen käytöstä saat noudattamalla seuraavia ohjeita: [Sähköisen raportoinnin muodon suunnitteleminen rivien pitämiseksi yhdessä samalla Excel-sivulla](er-keep-excel-rows-together.md).

### <a name="replication"></a>Replikointi

**Replikointisuunta**-ominaisuus määrittää, toistetaanko alue luodussa tiedostossa ja millä tavoin se toistetaan:

- **Ei replikointia** – Excel-alue ei toistu luodussa tiedostossa.
- **Pystysuuntainen** – Excel-alue toistetaan luodussa tiedostossa pystysuuntaisesti. Kukin replikoitu alue sijoitetaan Excel-mallin alkuperäisen alueen alapuolelle. Toistojen määrä määräytyy tähän ER-osaan sidotun **Tietueluettelo**-tyypin tietolähteen tietueiden määrän mukaan.
- **Vaakasuuntainen** – Excel-alue toistetaan luodussa tiedostossa vaakasuuntaisesti. Kukin replikoitu alue sijoitetaan Excel-mallin alkuperäisen alueen oikealle puolelle. Toistojen määrä määräytyy tähän ER-osaan sidotun **Tietueluettelo**-tyypin tietolähteen tietueiden määrän mukaan.

    Lisätietoja vaakasuuntaisesta replikoinnista on kohdan [Vaakasuunnassa laajennettavien alueiden käyttö sarakkeiden dynaamiseen lisäämiseen Excel-raportteihin](tasks/er-horizontal-1.md) ohjeissa.

### <a name="enabling"></a>Otetaan käyttöön

ER-toiminnon suunnitteluohjelman **Yhdistämismääritys**-välilehdessä **Alue**-osan **Käytössä**-ominaisuus voidaan määrittää määrittämään, onko osa sijoitettava luotuun tiedostoon:

- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Tosi** tai jos mitään lauseketta ei ole määritetty, sopiva alue täytetään luotuun tiedostoon.
- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Epätosi** tai jos tämä alue ei vastaa kokonaisia rivejä tai sarakkeita, sopivaa aluetta ei täytetä luotuun tiedostoon.
- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Epätosi** tai jos tämä alue vastaa kokonaisia rivejä tai sarakkeita, luoto tiedosto sisältää kyseiset rivit ja sarakkeet piilotettuina riveinä ja sarakkeina.

### <a name="resizing"></a>Koon muuttaminen

Excel-malli voidaan määrittää käyttämään soluja tekstitietojen esittämiseen. Solu voidaan määrittää rivittämään solussa oleva teksti automaattisesti. Tällä tavoin voidaan varmistaa, että koko solussa oleva teksti näkyy muodostetussa asiakirjassa. Lisäksi kyseisen solun sisältävä rivi voidaan määrittää automaattisesti muuttamaan korkeutta, jos rivitetty teksti ei ole kokonaan näkyvissä. Lisätietoja on kohdan [Soluissa katkenneiden tietojen korjaaminen](https://support.microsoft.com/office/fix-data-that-is-cut-off-in-cells-e996e213-6514-49d8-b82a-2721cef6144e) osassa Solussa olevan tekstin rivittäminen.

> [!NOTE]
> [Excelin tunnetun rajoituksen](https://support.microsoft.com/topic/you-cannot-use-the-autofit-feature-for-rows-or-columns-that-contain-merged-cells-in-excel-34b54dd7-9bfc-6c8f-5ee3-2715d7db4353) vuoksi Excelin **Sovita**- ja **Rivitä teksti** -ominaisuuksien käyttö ei ehkä onnistu yhdistetyissä soluissa ja solut sisältävillä riveillä, vaikka solut olisi määritetty rivittämään teksti ja kyseiset solut sisältävät rivit olisi määritetty muuttamaan automaattisesti korkeus rivitetyn tekstin mukaiseksi. 

Dynamics 365 Financen versiosta 10.0.23 alkaen, kun käsittelet luotua asiakirjaa, sähköinen raportointi voidaan pakottaa laskemaan kunkin sellaisen rivin korkeus, joka on määritetty sovittamaan korkeus automaattisesti sisäkkäisten solujen sisällön mukaisesti aina, kun kyseinen rivi sisältää ainakin yhden yhdistetyn solun, joka määritettiin rivittämään solussa oleva teksti. Laskettua korkeutta käytetään sitten rivin korkeuden muuttamiseen. Näin varmistetaan, että kaikki rivin solut näkyvät luodussa asiakirjassa.

> [!NOTE]
> Huomaa, että tämä toiminto ei ehkä toimi odotetulla tavalla, kun yhdistettyä solua muotoillaan mukautetulla fontilla. Koska Excel ei upota mukautettuja fontteja, se ei näytä tietoja mukautetun fontin koosta. Siksi yhdistetyn solun koko voidaan arvioida väärin.

Tämän toiminnon käyttö aloitetaan seuraavasti, kun suoritetaan sellaisia ER-muotoja, jotka on määritetty käyttämään Excel-malleja lähtevien asiakirjojen luontiin.

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit** -osassa **Sähköisen raportoinnin parametrit**.
3. Määritä **Sähköisen raportoinnin parametrit** -sivun **Suorituksen aikainen** -välilehdessä **Sovita rivin korkeus** -asetukseksi **Kyllä**.

Tämä sääntö voidaan muuttaa yhden ER-muodon osalta päivittämällä kyseisen muodon luonnosversio seuraavasti:

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.
3. Valitse **Määritykset**-sivun määrityspuun vasemmassa ruudussa ER-määritys, joka on suunniteltu luomaan lähteviä asiakirjoja Excel-mallin avulla.
4. Valitse **Versiot**-pikavälilehdessä konfiguraatioversio, jonka tila on **Luonnos**.
5. Valitse toimintoruudussa **Suunnittelija**.
6. Valitse **Muodon suunnittelija** -sivun muotopuun vasemmassa ruudussa Excel-malliin linkitetty Excel-osa.
7. Valitse **Muoto**-välilehden **Säädä rivin korkeutta** -kentässä arvo määrittämään, pakotetaanko sähköinen raportointi suorituksen aikana muuttamaan sellaisen lähtevän asiakirjan rivien korkeus, jotka on luotu muokatun ER-muodon avulla:

    - **Oletus** – käytä yleistä asetusta, joka on määritetty **Sähköisen raportoinnin parametrit** -sivun **Sovita rivin korkeus** -kentässä.
    - **Kyllä** – ohita yleinen asetus ja muuta rivin korkeutta suorituksen aikana.
    - **Ei** – ohita yleinen asetus mutta älä muuta rivin korkeutta suorituksen aikana.

## <a name="cell-component"></a>Solu-osa

**Solu**-osaa käytetään täyttämään Excelin nimetyt solut, muodot ja kuvat. Sellainen Excelin nimetty objekti, jonka **Solu**-ER-osan on täytettävä, ilmaistaan määrittämällä kyseisen objektin nimi **Solu**-osan **Excel-alue**-ominaisuudessa.

ER-toiminnon suunnitteluohjelman **Yhdistämismääritys**-välilehdessä **Solu**-osan **Käytössä**-ominaisuus voidaan määrittää määrittämään, onko objekti täytettävä luodussa tiedostossa.

- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Tosi** tai jos mitään lauseketta ei ole määritetty, sopiva objekti täytetään luodussa tiedostossa. Tämän **Solu**-osan sidonta määrittää arvo, joka sijoitetaan sopivaan objektiin.
- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Epätosi**, sopivaa objektia ei täytetä luodussa tiedostossa.

Jos **Solu**-osa on määritetty antamaan solun arvo, se voidaan sitoa tietolähteeseen, joka palauttaa alkeistietotyypin arvon (kuten **Merkkijono**, **Reaaliluku** tai **Kokonaisluku**). Tässä tapauksessa arvo annetaan solussa saman tietotyypin arvona.

Jos **Solu**-osa on määritetty antamaan arvo Excel-muotona, se voidaan sitoa tietolähteeseen, joka palauttaa alkeistietotyypin arvon (kuten **Merkkijono**, **Reaaliluku** tai **Kokonaisluku**). Tässä tapauksessa arvo annetaan Excel-muodossa kyseisen muodon tekstinä. Muissa kuin **Merkkijono**-tietotyypin arvoissa muunto tekstiksi tehdään automaattisesti.

> [!NOTE]
> **Solu**-osan voi määrittää täyttämään muodon vain tapauksissa, joissa muodon tekstiominaisuutta tuetaan.

Jos **Solu**-osa on määritetty antamaan arvo Excel-kuvana, se voidaan sitoa tietolähteeseen, joka palauttaa kuvan binaarimuodossa ilmaisevan **Säilö**-tyypin arvon. Tässä tapauksessa arvo annetaan Excel-kuvassa kuvana.

> [!NOTE]
> Jokainen Excel-kuva ja -muoto katsotaan ankkuroiduksi vasemmasta yläkulmasta tiettyyn Excel-soluun tai -alueeseen. Jos Excel-kuva tai -muoto halutaan replikoida, se solu tai alue, johon se on ankkuroitu, on määritettävä replikoiduksi soluksi tai alueeksi.

Lisätietoja kuvien ja muotojen upottamisesta on kohdassa [Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md).

## <a name="page-break-component"></a>Sivunvaihto-osa

**Sivunvaihto**-osa pakottaa Excelin aloittamaan uuden sivun. Tämä osa ei ole pakollinen, jos haluat käyttää Excelin oletussivusta, mutta sitä kannattaa käyttää, jos haluat Excelin jäsentävän sivutuksen ER-muodon mukaisesti.

## <a name="page-component"></a><a name="page-component"></a>Sivun komponentti

### <a name="overview"></a>Yleiskuvaus

Voit käyttää **Sivu**-komponenttia, kun haluat, että Excel seuraa ER-muotoasi ja rakennesivutustasi muodostetussa lähtevässä asiakirjassa. Kun ER-muoto suorittaa komponentteja, jotka ovat **Sivu**-komponentin alaisia, vaaditut sivunvaihdot lisätään automaattisesti. Tämän prosessin aikana on otettava huomioon muodostetun sisällön koko, Excel-mallin sivuasetukset ja Excel-mallissa valittu paperikoko.

Jos muodostettu asiakirja on jaettava eri osiin, joissa kullakin on oma sivutuksensa, voit määrittää useita **Sivu**-komponentteja jokaisessa [Arkki](er-fillable-excel.md#sheet-component)-komponentissa.

### <a name="structure"></a><a name="page-component-structure"></a>Rakenne

Jos ensimmäinen komponentti **Sivu**-komponentin alla on [Alue](er-fillable-excel.md#range-component)-komponentti, jossa **Replikointisuunta** -ominaisuus on määritetty muotoon **Ei replikointia**, tämä alue tulkitaan sivun ylätunnisteeksi sivutuksessa, joka perustuu nykyisen **Sivu**-komponentin asetuksiin. Tähän muotokomponenttiin liittyvä Excel-alue toistuu jokaisen sivun yläosassa, joka muodostetaan käyttämällä nykyisen **Sivu**-komponentin asetuksia.

> [!NOTE]
> Oikeata sivutusta varten: jos [Yläosassa toistettavat rivit](https://support.microsoft.com/office/repeat-specific-rows-or-columns-on-every-printed-page-0d6dac43-7ee7-4f34-8b08-ffcc8b022409) -alue on määritetty Excel-mallissasi, tämän Excel-alueen osoitteen on oltava sama kuin osoite Excel-alueessa, joka on liitetty aiemmin kuvailtuun **Alue**-komponenttiin.

Jos viimeinen komponentti **Sivu**-komponentin alla on **Alue**-komponentti, jossa **Replikointisuunta** -ominaisuus on määritetty muotoon **Ei replikointia**, tämä alue tulkitaan sivun alatunnisteeksi sivutuksessa, joka perustuu nykyisen **Sivu**-komponentin asetuksiin. Tähän muotokomponenttiin liittyvä Excel-alue toistuu jokaisen sivun alaosassa, joka muodostetaan käyttämällä nykyisen **Sivu**-komponentin asetuksia.

> [!NOTE]
> Jotta sivutus olisi oikea, Excel-alueiden, jotka on liitetty **Alue**-komponentteihin, kokoa ei tule muuttaa suorituspalvelussa. Ei ole suositeltavaa muotoilla tämän alueen soluja käyttämällä **Rivitä solun teksti**- ja **Sovita rivin korkeus** -Excel-[asetuksia](https://support.microsoft.com/office/wrap-text-in-a-cell-2a18cff5-ccc1-4bce-95e4-f0d4f3ff4e84).

Voit lisätä useita muita **Alue**-komponentteja valinnaisten **Alue**-komponenttien väliin määrittääksesi, miten muodostettu asiakirja täytetään.

Jos sisäkkäisten **Alue**-komponenttien joukko **Sivu**-komponentin alla ei vastaa aiemmin kuvailtua rakennetta, tapahtuu vahvistus[virhe](er-components-inspections.md#i17) suunnittelun aikana ER-muodon suunnitteluohjelmassa. Virhesanoma ilmoittaa, että ongelma voi aiheuttaa ongelmia suorituspalvelussa.

> [!NOTE]
> Jotta tulosteesta tulee oikea, älä määritä sidontaa millekään **Alue**-komponentille **Sivu**-komponentin alla, jos **Replikointisuunta**-ominaisuus kyseisessä **Alue**-komponentissa on määritetty muotoon **Ei replikointia** ja alue on määritetty muodostamaan sivun ylä- tai alatunnisteita.

Jos haluat sivutukseen liittyvien laskentojen ja summaamisten käsittelevän käynnissä olevat juoksevat kokonaismäärät ja kokonaismäärät sivua kohden, on suositeltavaa määrittää tarvittavat [Tietokokoelma](er-data-collection-data-sources.md)-tietolähteet. Kun haluat oppia käyttäään **Sivu**-komponenttia muodostetun Excel-asiakirjan sivuttamiseen, noudata menettelyjä kohdassa [Suunnittele ER-muoto sivuttamaan muodostettu asiakirja Excel-muodossa](er-paginate-excel-reports.md).

### <a name="limitations"></a><a name="page-component-limitations"></a>Rajoitukset

Kun käytät **Sivu**-komponenttia Excel-sivutukseen, et tiedä muodostetun asiakirjan sivujen lopullista määrää ennen kuin sivutus on valmis. Siksi sivujen kokonaismäärää ei voi laskea ER-kaavan avulla ja tulostaa oikeata muodostetun asiakirjan sivumäärää millään ennen viimeistä sivua edeltävällä sivulla.

> [!TIP]
> Tämän tuloksen saavuttaminen Excelin ylä- tai alaviitteessä käyttämällä Excelin lisä[muotoilua](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) ylä- ja alatunnisteita varten.

Määritettyjä **Sivu**-komponentteja ei oteta huomioon, kun päivität Excel-mallin muokattavassa muodossa Dynamics 365 Finance -versiossa 10.0.22. Tämä toiminto saattaa tulla voimaan myöhemmissä Finance-julkaisuissa.

Jos määrität Excel-mallisi käyttämään [ehdollista muotoilua](/office/dev/add-ins/excel/excel-add-ins-conditional-formatting), se ei ehkä toimi odotetulla tavalla joissakin tapauksissa.

### <a name="applicability"></a>Soveltuvuus

**Sivu**-komponentti toimii [Excel-tiedoston](er-fillable-excel.md#excel-file-component) mallikomponentille vain, jos kyseinen komponentti on määritetty käyttämään Excel-mallia. Jos [korvaat](tasks/er-design-configuration-word-2016-11.md) Excel-mallin Word-mallilla ja suoritat sitten muokattavan ER-muodon, **Sivu**-komponenttia ei oteta huomioon.

**Sivu**-komponentti toimii vain, kun **Ota käyttöön EPPlus-kirjasto sähköisen raportoinnin sovelluskehyksessä** -ominaisuus on otettu käyttöön. Suorituspalvelussa tulee poikkeus, jos ER yrittää käsitellä **Sivu**-komponenttia silloin, kun ominaisuus on otettu pois käytöstä.

> [!NOTE]
> Suorituspalvelussa tulee poikkeus, jos ER-muoto käsittelee **Sivu**-komponenttia Excel-mallissa, joka sisältää vähintään yhden kaavan, joka viittaa soluun, joka ei ole kelvollinen. Jotta voit estää suorituspalvelun virheet, korjaa Excel-malli siten kuin on kuvattu kohdassa [#REF! -virheen korjaaminen](https://support.microsoft.com/office/how-to-correct-a-ref-error-822c8e46-e610-4d02-bf29-ec4b8c5ff4be).

## <a name="footer-component"></a>Alatunnistekomponentti

**Alatunniste**-komponentin avulla täytetään Excel-työkirjassa luodun laskentataulukon alaosaan alatunniste.

> [!NOTE]
> Voit lisätä tämän komponentin jokaiselle **Laskentataulukko**-komponentille määrittääksesi eri alatunnisteet luodun Excel-työkirjan eri laskentataulukoille.

Kun määrität yksittäisen **Alatunniste**-komponentin, voit **Otsikon/alatunnisteen ulkoasu** -ominaisuuden avulla määrittää sivut, joissa komponenttia käytetään. Käytettävissä ovat seuraavat arvot:

- **Kaikki** – Suorita määritetty **Alatunniste**-komponentti kaikille Excel-päälaskentataulukon sivuille.
- **Ensimmäinen** – Suorita määritetty **Alatunniste**-komponentti vain Excel-päälaskentataulukon ensimmäiselle sivulle.
- **Parillinen** – Suorita määritetty **Alatunniste**-komponentti vain Excel-päälaskentataulukon parillisille sivuille.
- **Pariton** – Suorita määritetty **Alatunniste**-komponentti vain Excel-päälaskentataulukon parittomille sivuille.

Voit lisätä yksittäiselle **Laskentataulukko**-komponentille useita **alatunniste**-komponentteja, joilla kullakin on eri arvo **Otsikon/alatunnisteen ulkoasu** -ominaisuudelle. Näin voit luoda eri alatunnisteita Excel-laskentataulukon erityyppisille sivuille.

> [!NOTE]
> Varmista, että jokaiselle yksittäiselle **Laskentataulukko**-komponentille lisätylle **Alatunniste**-komponentilla on eri arvo **Otsikon/alatunnisteen ulkoasu** -ominaisuudelle. Muussa tapauksessa tapahtuu [oikeellisuustarkistusvirhe](er-components-inspections.md#i16). Näyttöön tulee virhesanoma, joka ilmoittaa epäyhtenäisyydestä.

Lisää lisätyn **alatunniste**-komponentin kohdassa sisäkkäiset komponentit **Text\\String**, **Text\\DateTime** tai muu tyyppi. Määritä näiden komponenttien sidonnat ja määritä, miten sivun alatunniste täytetään.

Erityisten [muotoilukoodien](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) avulla voit muotoilla luodun alatunnisteen sisällön oikein. Lisätietoja tämän menetelmän käytöstä on jäljempänä tässä artikkelissa [esimerkin 1](#example-1) vaiheiden mukaisesti.

> [!NOTE]
> Kun määrität ER-muotoja, muista ottaa huomioon Excelin [rajoitus](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) ja yksittäisen ylä- tai alatunnisteen enimmäismerkkimäärä.

## <a name="header-component"></a>Ylätunnistekomponentti

**Ylätunniste**-komponentin avulla täytetään Excel-työkirjassa luodun laskentataulukon yläosaan ylätunniste. Sitä käytetään kuten **Alatunniste**-komponenttia.

## <a name="edit-an-added-er-format"></a>Lisätyn ER-muodon muokkaaminen

### <a name="update-a-template"></a>Mallin päivittäminen

Päivitetty malli voidaan tuoda muokattavaan ER-muotoon valitsemalla **Päivitä Excelistä** toimintoruudun **Tuonti**-välilehdessä. Valitun **Excel\\Tiedosto**-osan malli korvataan uudella mallin tämän prosessin aikana. Muokattavan ER-muodon sisältö synkronoidaan päivitetyn ER-mallin sisällön kanssa.

- Jokaiselle Excel-nimelle luodaan automaattisesti uusi ER-muoto, jos muokattavassa muodossa olevaa ER-muoto-osaa ei löydy.
- Jokainen ER-muoto-osa on poistettava muokattavasta ER-muodosta, jos sille ei löydy sopivaa Excel-nimeä.

> [!NOTE]
> Jos muokattavaan ER-muotoon halutaan luoda valinnainen **Taulukko**-elementti, määritä **Luo Excel-taulukkomuotoinen elementti** -asetukseksi **Kyllä**.
>
> Jos muokattavassa ER-muoto sisälsi alun perin **Taulukko**-elementtejä, määritä **Luo Excel-taulukkomuotoinen elementti** -asetukseksi **Kyllä** päivitettyä mallia tuotaessa. Muussa tapauksessa kaikki alkuperäisen **Taulukko**-elementin sisäkkäiset elementit luodaan alusta. Tämän vuoksi kaikki uudelleenluotujen muotoelementtien sidonnat menetetään päivitetyssä ER-muodossa.

![Luo Excel-taulukkomuotoinen elementti -vaihtoehto Päivitä Excelistä -valintaikkunassa.](./media/er-excel-format-update-template.png)

Versiossa 10.0.28 ja sitä myöhemmissä versioissa voit käyttää **Päivitä Excelin ylä- ja alatunnisteen muotoelementit** -asetusta.

- Kun määrität tämän asetuksen arvoksi **Ei**, Excelin ylätunnisteen ja Excelin alatunnisteen muodon osat säilyvät muuttumattomina, vaikka vastaavat ylätunnisteet tai alatunnisteet olisi päivitetty tuotujen mallien laskentataulukoissa Excel-työkirjamuodossa.
- Kun määrität tämän asetuksen arvoksi **Kyllä**, Excelin ylätunnisteen ja Excelin alatunnisteen muodon osat muutetaan, kun vastaavat ylätunnisteet tai alatunnisteet päivitetään tuotujen mallien laskentataulukoissa Excel-työkirjamuodossa.

    - Jos laskentataulukon ylä- tai alatunnisteen rakennetta ei ole muutettu tai se on vain lisätty, vastaavan Excel-ylätunnisteen tai Excel-alatunnisteen muodon elementin rakenne päivitetään. Tämän Excelin ylätunnisteen tai Excelin alatunnistemuodon elementin sisäkkäisten muotoelementtien sidonnat säilytetään.
    - Jos laskentataulukon ylä- tai alatunnisteen rakennetta on muutettu, vastaava Excel-ylätunnisteen tai Excel-alatunnisteen muodon elementti luodaan uudelleen. Tämän Excelin ylätunnisteen tai Excelin alatunnistemuodon elementin sisäkkäisten muotoelementtien sidonnat poistetaan.

![Päivitä Excelin ylä- ja alatunnisteen muotoelementit -vaihtoehto Päivitä Excelistä -valintaikkunassa.](./media/er-excel-format-update-template2.png)

Lisätietoja tästä toiminnosta on kohdan [Sähköisen raportoinnin muotojen muokkaaminen käyttämällä Excel-malleja uudelleen](modify-electronic-reporting-format-reapply-excel-template.md) ohjeissa.

## <a name="validate-an-er-format"></a>ER-muodon vahvistaminen

Muokattavaa ER-muotoa vahvistettaessa tehdään yhdenmukaisuustarkistus, jolla varmistetaan, että Excel-nimi esiintyy käytettävässä Excel-mallissa. Saat ilmoituksen mahdollisista ristiriidoista. Joidenkin ristiriitojen osalta tarjotaan mahdollisuutta korjata ongelmat automaattisesti.

![Vahvistusvirhesanoma.](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Excel-kaavojen laskemisen hallinta

Kun Microsoft Excel -työkirjamuodossa oleva lähtevä asiakirja luodaan, jotkin tämän asiakirjan solut voivat sisältää Excel-kaavoja. Kun **Ota käyttöön EPPlus-kirjaston sähköinen raportointijärjestelmä** -toiminto on käytössä, voit määrittää, milloin kaavat lasketaan, muuttamalla **Laskentavalinnat**-[parametrin](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) arvoa käytetyssä Excel-mallissa:

- Valitse **Automaattinen**, jos haluat laskea kaikki riippuvaiset kaavat uudelleen aina, kun luotu tiedosto liitetään uusilla alueilla, soluissa jne.

    > [!NOTE]
    > Tämä saattaa aiheuttaa suorituskykyongelman niille Excel-malleille, jotka sisältävät useita toisiinsa liittyviä kaavoja.

- Valitse **Manuaalinen**, jos haluat välttää kaavojen uudelleenlaskennan, kun asiakirja luodaan.

    > [!NOTE]
    > Kaavan uudelleenlaskenta pakotetaan manuaalisesti, kun luotu asiakirja avataan esikatselua varten Excelissä.
    > Älä käytä tätä vaihtoehtoa, jos määrität ER-kohteen, joka olettaa, että luotu tiedosto on käytössä ilman sen esikatselua Excelissä (PDF-muunnos, sähköpostin lähetys jne.) koska luotu tiedosto ei ehkä sisällä kaavoja sisältävien solujen arvoja.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>Esimerkki 1: Alatunnisteen sisällön muotoileminen

1. Käyttämällä ER-konfiguraatioita voit [luoda](er-generate-printable-fti-forms.md) tulostettavan vapaatekstilaskun (FTI) asiakirjan.
2. Tarkista luodun tiedoston alatunniste. Huomaa, että sivu sisältää tietoja nykyisestä sivunumerosta ja asiakirjan sivujen kokonaismäärästä.

    ![Luodun tiedoston alatunnisteen tarkasteleminen Excel-muodossa.](./media/er-fillable-excel-footer-1.gif)

3. [Avaa](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) ER-muodon suunnittelijassa tarkistettavaksi ER-esimerkkimuoto.

    **Lasku**-laskentataulukon alatunniste luodaan kahden **Alatunniste**-komponentissa olevan **Merkkijono**-komponentin asetusten perusteella:

    - Ensimmäinen **merkkijono**-osa täyttää seuraavat erityismuotoilukoodit, jotka pakottavat Excelin käyttämään tiettyjä muotoiluja:

        - **&C** – Tasaa alatunnisteteksti keskelle.
        - **&"Segoe UI,Regular"&8** – Esittää alatunnisteen tekstin "Segoe UI Regular" -fontilla, jonka koko on 8 pistettä.

    - Toinen **merkkijono**-komponentti lisää tekstin, joka sisältää nykyisen sivunumeron ja nykyisen asiakirjan sivujen kokonaismäärän.

    ![Alatunnisteen ER-muotokomponentin tarkistus Muodon suunnittelija -sivulla.](./media/er-fillable-excel-footer-2.png)

4. Muokkaa nykyisen sivun alatunnistetta mukauttamalla ER-esimerkkimuotoa:

    1. [Luo](er-quick-start2-customize-report.md#DeriveProvidedFormat) johdettu **Vapaatekstilasku (Excel) mukautettu** ER-muoto, joka perustuu ER-esimerkkimuotoon.
    2. Lisää **Lasku**-laskentataulukon **Alatunniste**-komponentin ensimmäiset uudet **merkkijono**-komponentit:

        1. Lisää **merkkijono**-komponentti, joka tasaa yrityksen nimen vasemmalle ja esittää sen 8 pisteen "Segoe UI Regular" -fontilla (**"&L&"Segoe UI,Regular"&8"**).
        2. Lisää **merkkijono**-komponentti, joka täyttää yrityksen nimen (**model.InvoiceBase.CompanyInfo.Name**).

    3. Lisää **Lasku**-laskentataulukon **Alatunniste**-komponentin toiset uudet **merkkijono**-komponentit:

        1. Lisää **merkkijono**-komponentti, joka tasaa käsittelypäivämäärän oikealle ja esittää sen 8 pisteen "Segoe UI Regular" -fontilla (**"&R&"Segoe UI,Regular"&8"**).
        2. Lisää **merkkijono**-komponentti, joka täyttää käsittelypäivämäärän mukautetussa muodossa (**"&nbsp;"&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**).

        ![Alatunnisteen ER-muotokomponentin tarkistus Muodon suunnittelija -sivulla.](./media/er-fillable-excel-footer-3.png)

    4. [Viimeistele](er-quick-start2-customize-report.md#CompleteDerivedFormat) johdetun **Vapaatekstilasku (Excel) mukautettu** -ER-muodon luonnosversio.

5. [Määritä](er-generate-printable-fti-forms.md#configure-print-management) tulostuksenhallinta käyttämään johdettua **Vapaatekstilasku (Excel) mukautettu** -ER-muotoa ER-esimerkkimuodon sijaan.
6. Luo tulostettava FTI-tiedosto ja tarkista luodun tiedoston alatunniste.

    ![Luodun tiedoston alatunnisteen tarkasteleminen Excel-muodossa.](./media/er-fillable-excel-footer-4.gif)

## <a name="example-2-fixing-the-merged-cells-epplus-issue"></a><a name="example-2"></a>Esimerkki 2: Yhdistettyjen solujen EPPlus-ongelman korjaaminen

Voit luoda lähtevän asiakirjan Excel-työkirjamuodossa suorittamalla ER-muodon. Kun **Ota EPPlus-kirjaston käyttö käyttöön sähköisessä raportointikehyksessä** -ominaisuus on käytössä **Ominaisuudenhallinta**-työtilassa, Excel-laskentataulukon tuotossa käytetään [EPPlus-kirjastoa](https://www.nuget.org/packages/epplus/4.5.2.1). Koska [Excelin toiminta](https://answers.microsoft.com/en-us/msoffice/forum/all/deleting-a-range-of-cells-that-includes-merged/8601462c-4e2c-48e0-bd23-848eecb872a9) ja EPPlus-kirjaston rajoitus on tiedossa, saattaa kuitenkin ilmetä seuraava poikkeus: "Yhdistettyjä soluja ei voi poistaa tai korvata. Alue yhdistetään osittain toiseen yhdistettyyn alueeseen." Seuraavassa esimerkissä voit lukea, millaiset Excel-mallit voivat aiheuttaa tämän poikkeuksen ja ongelman korjaamisen.

1. Luo Excel-työpöytäsovelluksessa uusi Excel-työkirja.
2. Lisää laskentataulukossa **Sheet1** **ReportTitle**-nimi solulle **A2**.
3. Yhdistä solut **A1** ja **A2**.

    ![Tarkista solujen A1 ja A2 yhdistämisen tulokset Excel-työpöytäsovelluksen suunnitellussa Excel-työkirjassa.](./media/er-fillable-excel-example2-1.png)

3. **Määritykset**-sivulla [Lisää uusi ER-muoto](er-fillable-excel.md#add-a-new-er-format) luodaksesi lähtevän asiakirjan Excel-työkirjamuodossa.
4. [Tuo](er-fillable-excel.md#template-import) suunniteltu Excel-työkirja **Muotoilun suunnittelija** -sivulla lisättyyn ER-muotoon lähtevien tiedostojen uudella mallilla.
5. Määritä **Yhdistäminen**-välilehdellä [solu](er-fillable-excel.md#cell-component)-tyypin **ReportTitle**-komponentin sidonta.
6. Määritetyn ER-muodon suorittaminen. Huomaa, että seuraava poikkeus on näytetään: "Yhdistettyjä soluja ei voi poistaa tai korvata. Alue yhdistetään osittain toiseen yhdistettyyn alueeseen."

    ![Tarkastele muotosuunnittelun suunnittelusivulla ER:n määritetyn muodon määrityksen tuloksia.](./media/er-fillable-excel-example2-2.png)

Voit korjata nimikkeen jommallakummalla seuraavista tavoista:

- **Helpompaa mutta ei suositeltavaa:** Poista **ominaisuuden hallinnan** työtilassa **Ota EPPlus-kirjaston käyttö käyttöön sähköisessä raportointikehyksessä** -ominaisuus. Vaikka tämä tapa olisikin helpompi, saattaa sitä käyttää myös muita ongelmia, koska joitakin ER-toimintoja tuetaan vain, kun **Ota käyttöön EPPlus-kirjaston käyttö sähköisessä raportointikehyksessä** on otettu käyttöön.
- **Suositeltavaa:** Noudata näitä ohjeita:

    1. Muokkaa Excel-työkirjaa Excel-työpöytäsovelluksessa jollakin seuraavista tavoista:

        - Irrota taulukossa **Sheet1** solut **A1** ja **A2**.
        - Muuta **ReportTitle**-nimen viitteen nimi **=Sheet1!$A$2** nimeksi **=Sheet1!$A$1**.

        ![Tarkista viitteen muuttamisen tulokset Excel-työpöytäsovelluksen suunnitellussa Excel-työkirjassa.](./media/er-fillable-excel-example2-3.png)

    2. [Tuo](er-fillable-excel.md#template-import) muokattu Excel-työkirja **Muotosuunnittelu**-sivulla muokattavaan ER-muotoon ja päivitä aiemmin luotu malli.
    3. Muokatun ER-muodon suorittaminen.

        ![Luodun asiakirjan tarkistaminen Excel-työpöytäsovelluksessa.](./media/er-fillable-excel-example2-4.png)

## <a name="limitations"></a>Rajoitukset

### <a name="known-epplus-library-limitations"></a>Tunnetut EPPlus-kirjaston rajoitukset

#### <a name="external-data-sources"></a>Ulkoiset tietolähteet

Jos jokin malleista sisältää PivotTable-taulukon, joka perustuu [ulkoiseen tietolähteeseen](https://support.microsoft.com/office/create-a-pivottable-with-an-external-data-source-db50d01d-2e1c-43bd-bfb5-b76a818a927b) viittaavaan PowerPivot-malliin ja **Ota käyttöön EPPlus-kirjasto sähköisen raportoinnin sovelluskehyksessä** -ominaisuus on käytössä, näkyviin tulee seuraava virhesanoma, kun suoritat ER-muodon, joka käyttää tätä mallia lähtevien tiedostojen luomiseen Excel-muodossa: "Välimuistilähde ei ole laskentataulukko." Voit korjata tämän ongelman seuraavasti:

- **Suositeltava:** Suunnittele uudelleen Excel-ratkaisu, jota käytät:

    1. Erota osa, joka sisältää pivot-kaaviot erillisessä Excel-työkirjassa (työkirja A). 
    2. Luo ER:n avulla toinen Excel-työkirja (työkirja B) Financesta, jossa on tarvittavat tiedot. 
    3. Viittaa työkirjaan B työkirjassa A heti, kun työkirja B on luotu.

- Poista käytöstä toiminto **Ota käyttöön EPPlus-kirjasto sähköisessä raportointikehyksessä** jos haluat käyttää muuta vaihtoehtoa EPPlus-vaihtoehdon sijaan. 

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Konfiguraation suunnitteleminen raporttien luomiseksi OPENXML-muodossa](tasks\er-design-reports-openxml-2016-11.md)

[Sähköisen raportoinnin muotojen muokkaaminen käyttämällä Excel-malleja](modify-electronic-reporting-format-reapply-excel-template.md)

[Vaakasuunnassa laajennettavien alueiden käyttö sarakkeiden dynaamiseen lisäykseen Excel-raportissa](tasks/er-horizontal-1.md)

[Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md)

[Sähköisen raportoinnin (ER) määrittäminen hakemaan tiedot Power BI:hin](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
