---
title: ALV-ilmoitus (Tanska)
description: Tässä artikkelissa kuvataan, miten ALV-ilmoitus määritetään ja luodaan Tanskassa ennakkoon.
author: anasyash
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 666dc96cb169ab28ac3938299a3f245e3b4511ab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862996"
---
# <a name="vat-declaration-denmark"></a>ALV-ilmoitus (Tanska)

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten ALV-ilmoitus määritetään Tanskassa ja näytetään esiversiona Microsoft Excelissä.

Voit luoda raportin automaattisesti luomalla ensin tarpeeksi arvonlisäverokoodeja, jotta voit pitää erillisen ALV-kirjanpidon kutakin ennakko-ALV-ilmoituksen ruutua varten. Lisäksi ALV-ennakonpidätysilmoituksen sähköisen raportoinnin (ER) sovelluskohtaisten parametrien avulla arvonlisäverokoodit liitetään ALV-ilmoituksen ruutujen valintojen hakutuloksiin.

Tanskaa varten on määritettävä **Raporttikentän haku**. Lisätietoja sovelluskohtaisten parametrien määrittämisestä on jäljempänä tässä artikkelissa [ALV-ilmoituskenttien sovelluskohtaisten parametrien määrittäminen](#set-up-application-specific-parameters) -osassa.

Seuraavassa taulukossa Hakutulos-sarakkeessa näkyy hakutulos, joka on määritetty valmiiksi tietylle ALV-ilmoitusriville ALV-ilmoitusmuodossa. Näiden tietojen avulla voit liittää arvonlisäverokoodit oikein hakutuloksiin ja sitten ALV-ilmoituksen riviin.

### <a name="vat-declaration-overview"></a>ALV-ilmoituksen yleiskuvaus

Tanskan ALV-ilmoitus sisältää seuraavat tiedot.

**VAT-maksettava**

| Kuvaus                                                  | Veron peruste/veron määrä | Haun tulos/summa                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Maksettava vero                                                   | Verosumma          | **OutputVAT**</br> **DomesticVATUseTax** (ilmoitetaan myös Vähennettävä vero -ruudussa)                                                                                                                                                                                                                                                                       |
| Tavaroiden arvonlisävero tms. ostot ulkomailta                           | Verosumma          | **PurchaseGoodsAbroad**</br>**PurchaseGoodsAbroadUseTax** (ilmoitetaan myös Vähennettävä vero -ruudussa)</br>**PurchaseGoodsEU** (Veron peruste ilmoitetaan ruudussa A - tuotteiden hankinta.)</br>**PurchaseGoodsEUUseTax** (Veron määrä ilmoitetaan myös Vähennettävä vero -ruudussa. Veron peruste ilmoitetaan ruudussa A - tuotteiden hankinta.)                   |
| ALV ulkomailta ostetuista palveluista, joihin sovelletaan käänteistä veloitusta | Verosumma          | **PurchaseServicesAbroad**</br> **PurchaseServicesAbroadUseTax** (ilmoitetaan myös Vähennettävä vero -ruudussa)</br>**PurchaseServicesEU** (Veron peruste ilmoitetaan ruudussa A - palveluiden hankinta.)</br>**PurchaseServicesEUUseTax** (Veron määrä ilmoitetaan myös Vähennettävä vero -ruudussa. Veron peruste ilmoitetaan ruudussa A - palveluiden hankinta.) |
| Maksettava yhteensä                                                | Verosumma          | Edellisten kolmen valintaruudun summa                                                                                                                                                                                                                                                                                                            |

**Vähennykset**

| Kuvaus                                                                               | Veron peruste/veron määrä | Haun tulos/summa                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vähennettävä vero                                                                                 | Verosumma          | **InputVAT**</br> **DomesticVATUseTax** (ilmoitetaan myös Maksettava vero -ruudussa)</br>**PurchaseGoodsAbroadUseTax** (ilmoitetaan myös ALV-vero tuotteista yms., jotka on ostettu ulkomailta -ruudussa)</br>**PurchaseServicesAbroadUseTax** (ilmoitetaan myös "Ulkomailta ostettujen käänteisen verovelvollisten palvelujen arvonlisävero" -kentässä)</br>**PurchaseGoodsEUUseTax** (ilmoitetaan myös ALV-vero tuotteista yms., jotka on ostettu ulkomailta -ruudussa)</br> **PurchaseServicesEUUseTax** (ilmoitetaan myös "Ulkomailta ostettujen käänteisen verovelvollisten palvelujen arvonlisävero" -kentässä) |
| Öljyn ja pullotetun kaasun vero                                                                  | Verosumma          | **OilGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Luonnonkaasu- ja kaupunkikaasuvero                                                             | Verosumma          | **NaturalTownGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Hiilidioksidivero                                                                               | Verosumma          | **CarbonDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| CO2Duty                                                                                   | Verosumma          | **CO2Duty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Vesiveloitus                                                                              | Verosumma          | **WaterCharge**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Vähennykset yhteensä                                                                          | Verosumma          | Edellisten kuuden valintaruudun summa                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Verojen kokonaissumma (positiivinen summa = suorita maksu, negatiivinen summa = vastaanota palautus) | Verosumma          | Maksettava yhteensä – Kokonaisvähennykset                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**Lisätietoja**

| Kuvaus                                                                                                                                                                                                                                | Veron peruste/veron määrä | Haun tulos/summa                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------------------|
| Ruutu A - tuotteiden hankinta. EU:n sisäisen tavaroiden hankinnan arvo ilman arvonlisäveroa.                                                                                                                                                   | Veron peruste            | **PurchaseGoodsEU PurchaseGoodsEUUseTax**       |
| Ruutu A - palveluiden hankinta. EU:n sisäisen palveluiden hankinnan arvo ilman arvonlisäveroa.                                                                                                                                             | Veron peruste            | **PurchaseServicesEU PurchaseServicesEUUseTax** |
| Ruutu B - tavaroiden toimitus - ilmoitetaan kohdassa EU-myynti ilman arvonlisäveroa/DK VIES. EU:n sisäisen tavaroiden toimittamisen arvo ilman arvonlisäveroa                                                                                                           | Veron peruste            | **SalesGoodsEU**                                |
| Ruutu B - toimitus - ei ilmoiteta kohdassa EU-myynti ilman arvonlisäveroa/DK VIES. Tiettyjen unionin sisäisten luovutusten, kuten asennuksen, kokoonpanon, etämyynnin ja uusien kuljetusvälineiden ei-verovelvollisille henkilöille, arvo ilman arvonlisäveroa. | Veron peruste            | **SalesInstallationAssemblyEtcEU**              |
| Ruutu B - palvelujen toimitus. Unionin sisäisen palvelun, josta ostaja on velvollinen maksamaan arvonlisäveron käänteisenä verotuksena, arvo ilman arvonlisäveroa - on myös ilmoitettava kohtaan EU-myynti ilman arvonlisäveroa/DK VIES.                          | Veron peruste            | **SalesServicesEU**                             |
| Ruutu C - muut toimitukset. Muiden ilman arvonlisäveroa toimitettujen tavaroiden ja palveluiden arvo Tanskan alueella, muihin EU:n jäsenvaltioihin ja kolmansiin maihin tai kolmansille alueille.                                     | Veron peruste            | **OtherSuppliesWithoutVAT**                     |

#### <a name="purchase-reverse-charge-vat"></a>Oston käänteinen verovelvollisuus

Jos määrität arvonlisäverokoodit kirjaamaan saapuvan käänteisen arvonlisäveron käyttämällä käyttöveroa, liitä arvonlisäverokoodit "UseTax"-merkkijonon sisältävän **Raporttikentän haku** -nimen hakutuloksiin.

Vaihtoehtoisesti voit konfiguroida kaksi erillistä arvonlisäverokoodia: toisen erääntyville arvonlisäveroille ja toisen ALV-vähennykselle. Liitä sitten kukin koodi vastaaviin **Raporttikentän haku** -hakutuloksiin.

Voit esimerkiksi määrittää verotettavia yhteisön sisäisiä hankintoja varten arvonlisäverokoodin **UT_S_EU** käyttöveron avulla ja liittää sen **Raporttikentän haku** -hakutulosten **PurchaseGoodsEUUseTax**-hakutulokseen. Tällöin arvonlisäverokoodin **UT_S_EU** verosummat näkyvät kohdassa Tuotteiden ALV yms. ostettu ulkomailta ja vähennettävä vero -ruudut. Veroperusteet näkyvät kohdassa "A - tuotteiden hankinta.

Vaihtoehtoisesti voit määrittää kaksi arvonlisäverokoodia:

- **VAT_S_EU**, jonka veroprosenttiarvo on -25 prosenttia.
- **InVAT_S_EU**, jonka veroprosenttiarvo on 25 prosenttia.

Liitä sitten koodit vastaaviin **Raporttikentän haku** -hakutuloksiin seuraavasti:

- Liitä **VAT_S_EU** **PurchaseGoodsEU**-hakutulokseen.
- Liitä **InVAT_S_EU** **InputVAT**-hakutulokseen.

Tällöin arvonlisäverokoodin **VAT_S_EU** summat näkyvät kohdassa Tuotteiden ALV yms. ostettu ulkomailta -ruutu ja Ruutu A - tuotteiden hankinta. Arvonlisäverokoodin **InVAT_S_EU** summat näkyvät vähennettävä vero -ruudussa.

Lisätietoja käänteisen verovelvollisuuden määrittämisestä: [Käänteinen verovelvollisuus](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Konfiguroi järjestelmäparametrit

Muodostaaksesi ALV-ilmoituksen sinun on määritettävä ALV-numero.

1. Valitse **Organisaation hallinto** > **Organisaatiot** > **Yritykset**.
2. Valitse yritys ja sitten **Rekisteröintitunnukset**.
3. Valitse tai luo osoite Tanskassa. Valitse sitten **Rekisteröintitunnus**-pikavälilehdessä **Lisää**.
4. Valitse **Rekisteröintityyppi**-kentässä Tanskaa varten rekisteröity rekisteröintityyppi, joka käyttää **ALV-tunnus**-rekisteröintiluokkaa.
5. Anna **Rekisteröintinumero**-kentässä veronumero.
6. Kirjoita **Voimassa**-kenttään **Yleiset**-välilehdessä päivämäärä, jolloin numero tulee voimaan.

Lisätietoja rekisteröintiluokkien ja rekisteröintityyppien määrittämisestä on kohdassa [Rekisteröintitunnukset](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-preview-for-denmark"></a>Saksan ALV-ilmoituksen määrityksen esiversio Tanskalle

### <a name="import-er-configurations"></a>ER-konfiguraatioiden tuominen

Avaa **Sähköisen raportoinnin** työtila ja tuo **ALV-ilmoitus-Excel (DK)** ER -muoto.

Lisätietoja on kohdassa [ER-määritysten lataaminen määrityspalvelun yleisestä varastosta](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters"></a>Sovelluskohtaisten parametrien määrittäminen ALV-ilmoituskentille

> [!NOTE]
> Suosittelemme, että otat tätä varten käyttöön **Käytä sovelluskohtaisia parametreja sähköisen raportoinnin muotojen aiemmista versioista** -ominaisuuden **Ominaisuuksienhallinta**-työtilassa. Kun tämä ominaisuus on käytössä, ER-muodon aiemmassa versiossa konfiguroivat parametrit tulevat automaattisesti käyttöön saman muodon myöhemmässä versiossa. Jos tätä toimintoa ei ole otettu käyttöön, sovelluskohtaiset parametrit on määritettävä erikseen kullekin muotoversiolle. **Käytä sovelluskohtaisia parametreja aiemmista ER-muotojen versioista** -ominaisuus on käytettävissä **Ominaisuuksien hallinta** -työtilassa Financen versiosta 10.0.23 alkaen. Lisätietoja ER-muodon parametrien määrittämisestä kullekin yritykselle on kohdassa [ER-muodon parametrien määrittämisestä kullekin yritykselle](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Kun haluat luoda ALV-ilmoituksen automaattisesti, liitä arvonlisäverokoodit sovellukseen ja hakutuloksiin ER-konfiguraatiossa.

Seuraavia ohjeita noudattamalla voit määrittää, mitkä arvonlisäverokoodit luovat mitkä ALV-ilmoituksen ruudut.

1. Valitse **Työtilat** > **Sähköinen raportointi** >**Raportointimääritykset**.
2. Valitse **ALV-ilmoitus-Excel (DK)** -konfiguraatio ja valitse sitten **Määritykset \> Sovelluskohtaisten parametrien määritys**.
3. Valitse **Sovelluskohtaiset parametrit** -sivun **Haku**-pikavälilehdestä **Raporttikentän haku**.
4. Liitä arvonlisäverokoodit ja raporttikentät määrittämällä seuraavat **Ehdot**-pikavälilehden kentät.

    | Kenttä                  | Kuvaus                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Haun tulos          | Valitse raporttikentän arvo. Lisätietoja arvoista ja niiden määrityksestä ALV-ilmoitusriveille on tämän artikkelin aiemmassa [ALV-ilmoituksen yhteenveto](#vat-declaration-overview) -osassa.                                                                                               |
    | Alv-koodi               | Valitse raporttikenttään liitettävä arvonlisäverokoodi. Valittua arvonlisäverokoodia käyttävät kirjatut verotapahtumat kerätään soveltuvassa ilmoitusruudussa. On suositeltavaa erotella arvonlisäverokoodit siten, että yksi arvonlisäverokoodi luo summia vain yhteen ilmoitusruutuun. |
    | Tapahtumaluokan valitsin | Jos olet luonut tarpeeksi arvonlisäverokoodeja ilmoitusruudun määrittämiseksi, valitse **\*Ei tyhjä\***. Jos et luonut tarpeeksi arvonlisäverokoodeja niin, että yksi arvonlisäverokoodi luo summia vain yhteen ilmoitusruutuun, voit määrittää tapahtumaluokan valitsimen. Seuraavat tapahtumaluokan valitsimet ovat käytettävissä:</br>-   **Osto**</br>-   **PurchaseExempt** (verovapaa osto)</br>-   **PurchaseReverseCharge** (oston käänteisen kulun verosaatavat)</br>-   **Myynti**</br>-   **SalesExempt** (veroton myynti)</br>-   **SalesReverseCharge** (oston käänteisen kulun tai myynnin käänteisen kulun maksettava vero)</br>-   **Käyttövero**. </br>Lisäksi kutakin tapahtumaluokan valitsinta varten on käytettävissä hyvityslaskun luokan valitsin. Yksi näistä luokan valitsimista on esimerkiksi **PurchaseCreditNote** (ostohyvityslasku).</br>Luo jokaiselle arvonlisäverokoodille kaksi riviä: yksi, jolla on tapahtumaluokan valitsimen arvo ja toinen, jolla on tapahtumaluokan valitsin hyvityslaskun arvoa varten. |


    > [!NOTE]
    > Liitä kaikki arvonlisäverokoodit hakutuloksiin. Jos jokin arvonlisäverokoodi ei saa luoda arvoja ALV-ilmoitukseen, liitä ne **Muut**-hakutulokseen.

    ![Sovelluskohtaiset parametrit -sivu.](media/7db74920fad66a0db7fad60758698cc0.png)


5. Muuta **Tila**-kentän arvoksi **Valmis**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>ALV-raportointimuodon asetus Excelin esikatselua varten

1. **ALV-ilmoitusmuodon raportit**-ominaisuus on etsittävä ja valittava käyttöön **Ominaisuuksien hallinta** -työtilassa. luettelosta toiminto ja valitse sitten **Ota käyttöön nyt**.
2. Valitse **Kirjanpito** >  **Kirjanpidon asetukset** >  **Kirjanpitoparametrit**.
3. Valitse **Arvonlisävero**-välilehden **Veroasetukset**-pikavälilehden **ALV-ilmoituksen muodon määritys** -kentästä **ALV-ilmoitus-Excel (DK)** ER-muoto.

   Tämä muoto tulostetaan, kun suoritat **Ilmoita arvonlisävero tilityskaudelle** -raportin. Se tulostetaan myös, kun valitset **Arvonlisäveromaksut**-sivulla **Tulosta**.

4. Valitse **Veroviranomaiset**-sivulla veroviranomainen ja valitse sitten **Raportin asettelu** -kentästä **Oletus**.

Jos konfiguroit ALV-ilmoituksen yrityksessä, jossa on [useita ALV-rekisteröintejä](emea-reporting-for-multiple-vat-registrations.md), toimi seuraavasti.

1. Siirry kohtaan **Kirjanpito** \> **Asetukset** \> **Kirjanpitoparametrit**.
2. Valitse **Arvonlisävero**-välilehden **Sähköisen raportoinnin maat/alueet** -pikavälilehdessä **DNK**-rivillä ER-muoto **VAT Declaration Excel (DK)**.

## <a name="set-up-electronic-messages"></a>Sähköisten sanomien määrittäminen

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Lataa ja tuo tietopaketti, joka sisältää sähköisten viestien esimerkkiasetukset

Tietopaketti sisältää sähköisen sanoman asetuksia, joita käytetään ALV-ilmoituksen esikatselemiseen Excelissä. Voit laajentaa näitä asetuksia tai luoda omia. Lisätietoja sähköisten viestien käytöstä ja omien asetusten luomisesta on kohdassa [Sähköiset viestit](../general-ledger/electronic-messaging.md).

1. Valitse [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) -kohdan jaetussa käyttöomaisuuskirjastossa käyttöomaisuuserän tyypiksi **Tietopaketti** ja lataa sitten **DK – ALV-ilmoitus -paketti**. Ladatun tiedoston nimi on **DK ALV-ilmoituspaketti.zip**.
2. Valitse Financessa **Tietojen hallinta** -työtilassa **Tuo**.
3. Kirjoita **Tuo**-pikavälilehden **Ryhmän nimi**-kenttään työn nimi.
4. Valitse **Valitut yksiköt** -välilehdessä **Lisää tiedosto**.
5. Varmista **Lisää tiedosto** -valintaikkunassa, että **Lähteen tietomuoto** -kentän arvo on **Paketti**, valitse **Lataa palvelimeen ja lisää** sekä valitse sitten aiemmin lataamasi zip-tiedosto.
6. Valitse **Sulje**.
7. Valitse tietoyksiköiden lataamisen jälkeen toimintoruudusta **Tuo**.
8. Siirry kohtaan **Vero** > **Kyselyt ja raportit** > **Sähköiset sanomat** > **Sähköiset sanomat** ja vahvista tuodun sähköisen sanoman käsittely (**DK ALV-ilmoitus**).

### <a name="configure-electronic-messages"></a>Sähköiset sanomat – määritys

1. Valitse **Vero** > **Asetukset** > **Sähköiset sanomat** > **Tietueiden täyttötoiminnot**.
2. Valitse **DK – Täytä ALV-palautustietueet** -rivi ja valitse **Muokkaa kyselyä**.
3. Suodatinta käyttämällä voit määrittää raporttiin sisällytettävät tilityskaudet.
4. Jos haluat raportoida muiden tilityskausien verotapahtumat eri ilmoituksessa, luo uusi **Täytä tietueet** -toimenpide ja valitse asianmukaiset tilityskaudet.

## <a name="preview-the-vat-declaration-in-excel"></a>ALV-ilmoituksen esikatselu Excelissä

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="preview-vat-excel"></a>ALV-ilmoituksen esikatselu Excelissä kausittaisen Ilmoita arvonlisävero tilityskaudelle -tehtävän avulla

1. Valitse **Vero** > **Kausittaiset tehtävät** > **Ilmoitukset** > **Arvonlisävero** > **Ilmoita arvonlisävero tilityskaudelle**.
2. Valitse arvo **Tilityskausi**-kentässä.
3. Valitse **Arvonlisäveron maksuversio** -kentässä jokin seuraavista arvoista:

    - **Alkuperäinen**: Luo raportti alkuperäisen arvonlisäveromaksun arvonlisäverotapahtumista tai ennen arvonlisäveromaksun muodostamista.
    - **Oikaisut**: Luo raportti kaikkien seuraavien arvonlisäveromaksujen arvonlisäverotapahtumista kaudella.
    - **Koko luettelo**: Luo raportti kaikista arvonlisäverotapahtumista kaudella, sisältäen alkuperäiset ja korjaukset.

4. Valitse raportointikauden aloituspäivämäärä **Aloituspäivämäärä**-kentästä.
5. Valitse **OK** ja tarkista Excel-raportti.

### <a name="settle-and-post-sales-tax"></a>Tilitä ja kirjaa arvonlisävero

1. Valitse **Vero** > **Kausittaiset tehtävät** > **Ilmoitukset** > **Arvonlisävero** > **Tilitä ja kirjaa arvonlisävero**.
2. Valitse arvo **Tilityskausi**-kentässä.
3. Valitse **Arvonlisäveron maksuversio** -kentässä jokin seuraavista arvoista:

    - **Alkuperäinen**: Luo alkuperäinen arvonlisäveromaksu tilityskaudelle.
    - **Viimeisimmät korjaukset**: Luo oikaisun arvonlisäveromaksu sen jälkeen, kun alkuperäinen tilityskauden arvonlisäveromaksu on luotu.

4. Valitse raportointikauden aloituspäivämäärä **Aloituspäivämäärä**-kentästä.
5. Valitse **OK**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>ALV-ilmoituksen esikatselu Excelissä arvonlisäveromaksusta

1. Siirry kohtaan **Vero** > **Kyselyt ja raportit** > **Arvonlisäverokyselyt** > **Arvonlisäveromaksut** ja valitse arvonlisäveron maksurivi.
2. Valitse ensin **Tulosta raportti** ja sitten **OK**.
3. Tarkista valitulle arvonlisäveron maksuriville luotu Excel-tiedosto.

> [!NOTE]
> Raportti luodaan vain valitulle arvonlisäveron maksuriville. Jos sinun tulee luoda esimerkiksi korjausilmoitus, joka sisältää kauden kaikki korjaukset, tai korvaavan ilmoituksen, joka sisältää alkuperäiset tiedot ja kaikki korjaukset, käytä kausittaista tehtävää **Ilmoita arvonlisävero tilityskaudelle**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>ALV-ilmoituksen muodostaminen sähköisistä sanomista

Kun muodostat raportin sähköisten viestien avulla, voit kerätä verotietoja useista yrityksistä. Lisätietoja on tässä artikkelissa jäljempänä [ALV-ilmoituksen suorittaminen useille yrityksille](#run-vat-declaration) -osassa.

Seuraavat vaiheet koskevat sähköisen sanoman käsittelyesimerkkiä, jonka olet tuonut aiemmin LCS:n jaetusta käyttöomaisuuskirjastosta.

1. Valitse **Vero \> Kyselyt ja raportit \> Sähköiset sanomat \> Sähköiset sanomat**.
2. Valitse vasemmasta ruudusta **DK – ALV-ilmoitus**.
3. Valitse **Sanomat**-pikavälilehdessä **Uusi** ja valitse sitten **Suorita käsittely** -valintaikkunassa **OK**.
4. Valitse luotava sanomarivi, kirjoita kuvaus ja määritä sitten ilmoituksen alkamis- ja päättymispäivät.

   > [!NOTE]
   > Vaiheet 5-7 ovat valinnaisia.

5. Valinnainen: Valitse **Sanomat**-pikavälilehdessä **Kerää tiedot** ja valitse sitten **OK**. Aiemmin luodut arvonlisäveromaksut lisätään sanomaan. Lisätietoja on tämän artikkelin aiemmassa [Tilitä ja kirjaa arvonlisävero](#settle-and-post-sales-tax) -osassa. Jos ohitat tämän vaiheen, voit silti luoda ALV-ilmoituksen käyttämällä **Veroilmoituksen versio** -kenttää **Ilmoitus**-valintaikkunassa.
6. Valinnainen: Tarkista **Sanomanimikkeet**-pikavälilehdessä käsittelyyn siirretyt arvonlisäveromaksut. Oletusarvon mukaan kaikki valitun kauden arvonlisäveromaksut, jotka eivät sisälly saman käsittelyn muihin sanomaan, sisällytetään mukaan.
7. Valinnainen: Tarkista arvonlisäveromaksut valitsemalla **Alkuperäinen tiedosto**. Voit myös sulkea arvonlisäveromaksut pois käsittelystä valitsemalla **Poista**. Jos ohitat tämän vaiheen, voit silti luoda ALV-ilmoituksen käyttämällä **Veroilmoituksen versio** -kenttää **Ilmoitus**-valintaikkunassa.
8. Valitse **Sanomat**-pikavälilehdessä **Päivitä tila**. Valitse **Päivitä tila** -valintaikkunassa **Valmis luotavaksi** ja valitse sitten **OK**. Vahvista, että sanoman tilaksi tulee **Valmis luotavaksi**.
9. Valitse **Luo raportti**. Voit esikatsella ALV-ilmoituksen summia valitsemalla **Suorita käsittely** -valintaikkunassa **Esikatsele raporttia** ja valitsemalla sitten **OK**.
10. Aseta **Sähköisen raportoinnin parametrit** -valintaikkunassa kentät, kuten on kuvattu tämän artikkelin aiemmassa [Esikatsele arvonlisäveroilmoitusta Excelissä Raportoi myyntivero tilikauden määräaikaistehtävästä](#preview-vat-excel) -osassa **OK**.
11. Valitse sivun oikeasta yläkulmasta **Liitteet**-painike (paperiliitinsymboli) ja avaa tiedosto valitsemalla **Avaa**. Tarkista Excel-tiedoston summat.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-vat-declaration"></a>ALV-ilmoituksen suorittaminen useille yrityksille

Jos haluat käyttää muotoja yritysryhmän ALV-ilmoituksen raportoimiseen, sinun on ensin määritettävä kaikkien tarvittavien yritysten ER-muotojen sovelluskohtaiset parametrit arvonlisäverokoodeille.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Sähköisten viestien tietojen kerääminen usealta yritykseltä

Noudattamalla näitä ohjeita voit määrittää sähköiset sanomat, jotka keräävät tietoja useilta yrityksiltä.

1. Valitse **Työtilat** > **Ominaisuuden hallinta**.
2. Etsi ja valitse **Yritysten väliset kyselyt tietueiden täyttötoiminnoille** -toiminto luettelosta ja sitten **Ota käyttöön nyt**.
3. Valitse **Vero** > **Asetukset** > **Sähköiset sanomat** > **Tietueiden täyttötoiminnot**.
4. Valitse **Tietueiden täyttötoiminto** -sivulla rivi, jossa on **DK – Täytä ALV-palautustietueet**.

   Uusi **Yritys**-kenttä on käytettävissä **Tietolähteiden asetukset** -ruudukossa. Tässä kentässä näkyy aiemmin luotujen tietueiden tapauksessa nykyisen yrityksen tunnus.

5. Lisää **Tietolähteiden asetukset** -ruudukkoon rivi kutakin raportointiin sisällytettävää lisäyritystä varten. Määritä kullekin uudelle riville seuraavat kentät.

    | Kenttä                  | Kuvaus                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Nimi                   | Kirjoita arvo, joka auttaa ymmärtämään, mistä tämä tietue tulee. Syötä esimerkiksi **Tytäryhtiön 1 ALV-maksu**. |
    | Sanoman nimiketyyppi      | Valitse **ALV-palautus**. Tämä arvo on ainoa arvo, joka on käytettävissä kaikille tietueille.                                    |
    | Tilityyppi           | Valitse **Kaikki**.                                                                                                               |
    | Päätaulun nimi      | Määritä kaikille tietueille **TaxReportVoucher**.                                                                             |
    | Asiakirjan numerokenttä  | Määritä kaikille tietueille **Voucher**.                                                                                      |
    | Asiakirjan päivämääräkenttä    | Määritä kaikille tietueille **TransDate**.                                                                                    |
    | Asiakirjan tilikenttä | Määritä kaikille tietueille **TaxPeriod**.                                                                                    |
    | Yritys                | Valitse yrityksen tunnus.                                                                                            |
    | Käyttäjän kysely             | Tämä valintaruutu valitaan automaattisesti, kun määrität ehtoja valitsemalla **Muokkaa kyselyä**.                                 |

6. Valitse kullekin uudelle riville **Muokkaa kyselyä** ja määritä liittyvä tilityskausi rivin **Yritys**-kentässä määritetylle yritykselle.

Kun määritys on valmis, **Sähköiset sanomat** -sivun **Kerää tiedot** -toiminto kerää arvonlisäveromaksut kaikilta määritetyiltä yrityksiltä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
