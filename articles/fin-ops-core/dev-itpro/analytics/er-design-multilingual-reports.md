---
title: Monikielisten raporttien suunnitteleminen sähköisessä raportoinnissa
description: Tässä ohjeaiheessa käsitellään sähköisen raportoinnin (ER) selitteiden käyttöä monikielisten raporttien suunnittelussa ja luonnissa.
author: NickSelin
ms.date: 11/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eab17635494657740fe46364bde0773dae5b9e4b
ms.sourcegitcommit: 8bcb9c13eccb14e61c39ca6578d135b64090fad2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2022
ms.locfileid: "8313688"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>Monikielisten raporttien suunnitteleminen sähköisessä raportoinnissa

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Yleiskuvaus

Yrityskäyttäjänä voit käyttää [sähköisen raportoinnin (ER)](general-electronic-reporting.md) kehystä määrittämään lähtevien sähköisten asiakirjojen muodot, jotka on luotava eri maiden ja alueiden lakisääteisten vaatimusten mukaan. Kun nämä vaatimukset edellyttävät, että lähtevät asiakirjat luodaan eri kielellä eri maissa tai eri alueilla, voit määrittää yhden ER-muodon, jotka sisältää kieliriippuvaiset resurssit. Tällä tavoin luoda eri kielten tai alueiden lähteviä asiakirjoja käyttämällä muotoa uudelleen. Lisäksi yhdellä ER-muodolla on mahdollista luoda lähtevä asiakirja eri kielellä asiakkaille, toimittajille, tytäryhtiöille tai muille osapuolille.

ER-tietomallit ja mallimääritykset voidaan määrittää määritettyjen ER-muotojen tietolähteiksi. Tällä tavoin voidaan määrittää tietovirrat, joilla määritetään luotuihin asiakirjoihin sijoitettavat sovelluksen tiedot. ER-konfiguraation [lähteenä](general-electronic-reporting.md#Provider) voit [julkaista](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) määritettyjä tietomalleja, mallimäärityksiä ja muotoja ER-ratkaisun osina, joita käytetään tiettyjen lähtevien asiakirjojen luontiin. Voit myös antaa asiakkaille mahdollisuuden [ladata](general-electronic-reporting-manage-configuration-lifecycle.md) julkaistun ER-ratkaisun, jolloin sitä voidaan käyttää ja mukauttaa. Jos oletat, että asiakkaat puhuvat muita kieliä, voit määrittää ER-osat siten, että niissä on kieliriippuvaisia resursseja. Tällä tavoin muokattavan ER-osan sisältö voidaan ilmaista asiakkaan käyttäjän valitsemalla kielellä suunnitteluvaiheessa.

Kieliriippuvaiset resurssit voidaan määrittää ER-selitteinä. ER-osat voidaan sitten määrittää kyseisten selitteiden avulla seuraavia tarkoituksia varten:

- Suunnitteluvaiheessa:

    - Määritettyjen ER-osien sisältö näytetään käyttäjän valitsemalla kielellä.

- Suorituksen aikana:

    - Kieliriippuvaisen sisällön luonti lähteviin asiakirjoihin.
    - Varoitusten ja virhesanomien antaminen käyttäjän valitsemalla kielellä.
    - Pakollisten kenttien täyttämisen pyytäminen käyttäjän valitsemalla kielellä.

ER-selitteet voidaan määrittää jokaisessa ER-[konfiguraatiossa](general-electronic-reporting.md#Configuration), jossa on eri osia. Selitteitä voidaan ylläpitää erillään ER-tietomallien, ER-mallimääritysten ja ER-muoto-osien määritetystä logiikasta.

Jokaiselle ER-selitteellä on yksilöivä tunniste, jolla se tunnistetaan selitteen sisältävässä ER-määrityksessä. Jokaisessa selitteessä voi olla seliteteksti jokaisella nykyisessä Microsoft Dynamics 365 Finance -esiintymässä tuetulla kielellä. Nämä tuetut kielet sisältävät käyttöönotettujen mukautusten kielet.

## <a name="entry"></a>Merkintä

ER-tietomallia, ER-mallimääritystä tai ER-muotoa suunnitellessa **Käännä**-vaihtoehto näkyy aina, kun valitse kentän, jonka konteksti voi olla käännettävissä. Jos valitset tämän vaihtoehdon, voit linkittää valitut kentät ER-selitteeseen **Tekstin käännös** <a name="TextTranslationPane">-ruudussa</a>. Voit valita aiemmin luodun ER-selitteen tai lisätä uuden ER-selitteen, jos sopivaa ei ole vielä saatavana. Kun valitset tai lisäät ER-selitteen, voit lisätä liittyvän tekstin jokaisella nykyisessä Finance-esiintymässä tuetulla kielellä.

Seuraavassa kuvassa näytetään, miten käännös tehdään muokattavassa ER-tietomallissa. Tässä esimerkiksi muokattavan **laskumallin** **Ostotilaus**-kentän **Kuvaus**-määrite käännetään Itävallan saksaksi (DE-AT) ja japaniksi (JA).

![ER-selitteen kääntäminen ER-tietomallin suunnittelutoiminnossa.](./media/er-multilingual-labels-refer.png)

Vain muokattavassa ER-osassa olevien selitteiden selitetekstin voi kääntää. Jos esimerkiksi valitset ER-mallimäärityksen tietolähteen selitemääritteessä **Käännä** ja valitset sitten ER-selitteen, joka ylätason ER-tietomallissa, selitteen sisältö on näkyvissä, mutta sitä ei voi muuttaa. Tällaisissa tapauksissa **Käännetty teksti** -kenttä ei ole käytettävissä, kuten seuraavasta kuvasta huomataan.

![ER-selitteen annetun käännöksen tarkistaminen ER-mallimäärityksen suunnittelutoiminnossa.](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> Suunnittelutoimintoja ei voi käyttää muokattavassa ER-osassa annetun selitteen poistamiseen.

## <a name="scope"></a>Vaikutusalue

ER-selitteisiin voidaan viitata useissa ER-osien käännettävissä määritteissä.

### <a name="data-model-component"></a>Tietomallin komponentti

ER-tietomallin määrityksen yhteydessä siihen voidaan lisätä ER-selitteitä. Mallinimikkeen **Selite**- ja **Kuvaus**-määritteet, jokaisen mallin kenttä ja jokaisen <a id="LinkModelEnum"></a> mallin luettelointiarvo voidaan linkittää ER-tietomalliin lisättävään ER-selitteeseen.

![Kuvaus-määritteen käännöksen antaminen ER-tietomallin suunnittelutoiminnossa.](./media/er-multilingual-labels-refer.png)

Kun ER-tietomalli määritetään tällä tavoin, sen sisältö näytetään ER-tietomallin suunnittelutoiminnon käyttäjille kunkin käyttäjän valitsemalla kielellä. Tämä myös yksinkertaistaa mallin ylläpitoa. Seuraavissa kuvissa näytetään, miten toimintoa toimii käyttäjillä, joiden valittuna kielenä on DE-AT ja JA.

![ER-tietomallin suunnittelutoiminnon asettelu, kun käyttäjän valitsema kieli on DE-AT.](./media/er-multilingual-labels-refer-de.png)

![ER-tietomallin suunnittelutoiminnon asettelu, kun käyttäjän valitsema kieli on JA.](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>Mallimääritysosa

Koska ER-mallimääritys perustuu ER-tietomalliin, viitattavien tietomallielementtien selitteet näkyvät käyttäjän valitsemalla kielellä mallimäärityksen suunnittelutoiminnossa. Seuraava kuva osoittaa, miten **Ostotilaus**-kenttä selitetään muokattavassa mallimäärityksessä käyttämällä määritettyyn tietomalliin lisättyä **Kuvaus**-määritteen selitettä. Huomaa, että tämä malli näkyy käyttäjän valitsemalla kielellä (tässä esimerkissä DE-AT).

![ER-mallimäärityksen suunnittelutoiminnon asettelu, kun käyttäjän valitsema kieli on DE-AT.](./media/er-multilingual-labels-show-mapping.png)

Jos **Käyttäjän syöttöparametri** -tietolähteen **Selite**-määrite on määritetty ER-selitteeseen linkitettynä, käyttäjät näkevät kyseistä tietolähdettä vastaavan parametrikentän käyttäjän valintaikkunassa suorituksen aikana valitsemallaan kielellä.

### <a name="format-component"></a>Muotokomponentti

ER-muodon määrityksen yhteydessä siihen voidaan lisätä ER-selitteitä. Jokaisen määritetyn tietolähteen **Selite**- ja **Ohjeteksti**-määritteet voidaan linkittää ER-muotoon lisättyyn ER-selitteeseen. Myös jokaisen <a id="LinkFormatEnum"></a>muodon luettelointiarvon **Selite**- ja **Kuvaus**-määrite voidaan linkittää ER-selitteeseen, jota voidaan käyttää muokattavasta ER-muodosta.

> [!NOTE]
> Nämä määritteet voidaan linkittää myös sen ylätason ER-tietomallin ER-selitteeseen, joka käyttää mallin selitteitä uudelleen jokaisessa tähän ER-tietomalliin määritetyssä ER-muodossa.

Kun ER-muoto määritetään tällä tavoin, muodon sisältö näytetään ER-toiminnon suunnittelutoiminnon käyttäjille kunkin käyttäjän valitsemalla kielellä. Niinpä muodon ylläpito ja määritetyn logiikan analyysi on yksinkertaista.

Koska ER-muoto perustuu ER-tietomalliin, selitteet, joihin viitataan tietomallielementeissä, näkyvät ER-muodon suunnittelutoiminnossa käyttäjän valitsemalla kielellä.

Jos **Käyttäjän syöttöparametri** -tietolähteen **Selite**-määrite on linkitetty ER-selitteeseen, käyttäjä näkee kyseistä parametria vastaavan kentän käyttäjän valintaikkunassa suorituksen aikana kehotteena. Seuraavissa kuvissa näytetään, miten **Käyttäjän syöttöparametri** -tietolähteen **Selite**-määrite linkitetään suunnitteluvaiheessa ER-selitteeseen siten, että parametria pyydetään käyttäjältä käyttäjän valitsemilla eri kielillä suorituksen aikana (kuvissa kielinä Yhdysvaltain englanti (EN-US) ja DE-AT).

![Käyttäjän syöteparametrin määritteiden käännösten antaminen ER-toiminnon suunnittelutoiminnossa.](./media/er-multilingual-labels-refer-format.png)

![ER-toimittajan maksun käsittely suorituksen aikana, kun käyttäjän valitsema kieli on EN-US.](./media/er-multilingual-labels-show-runtime-en.png)

![ER-toimittajan maksun käsittely suorituksen aikana, kun käyttäjän valitsema kieli on DE-AT.](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>Lausekkeet

Jos ER-[lausekkeessa](er-formula-language.md) halutaan käyttää selitettä, käytettävän syntaksin on oltava **@"GER\_LABEL:X"**, jossa etuliite **@** ilmaisee, että operandi viittaa selitteeseen, **GER\_LABEL** ilmaisee, että kyse on ER-selitteestä ja että **X** on ER-selitteen tunnus.

![ER-selitteen sisältävän ER-lausekkeen määrittäminen ER-muodon suunnittelutoiminnossa.](./media/er-multilingual-labels-expression1.png)

Järjestelmän (sovelluksen) selitteeseen viitataan käyttämällä syntaksia **@"X"**, jossa etuliite **@** ilmaisee selitteeseen viittaavan operandin ja **X** on järjestelmän selitteen tunnus.

![Sovelluksen selitteen sisältävän ER-lausekkeen määrittäminen ER-muodon suunnittelutoiminnossa.](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>Mallin määritys

ER-mallimäärityksen lauseke voidaan määrittään selitteen avulla. Kun sellainen ER-muoto kutsuu tätä määritystä, jonka suorittaminen luo lähtevän asiakirjan, suorituskonteksti sisältää kielikoodin. Määritetty lausekeselite täytetään kyseisen selitetekstillä, joka on määritetty kyseisen kontekstin kielelle.

Jos viitatussa selitteessä ei ole mallimäärityksen kutsuvan muodon suorituskontekstin kielistä käännöstä, selitetekstissä käytetään sen sijaan kieltä EN-US.

#### <a name="format"></a>Muoto

ER-muodon ER-lauseke voidaan määrittää selitteiden avulla. Kun lähtevä asiakirja luodaan suorittamalla muoto, suorituskonteksti sisältää kielikoodin. Määritetty lausekeselite täytetään kyseisen selitetekstillä, joka on määritetty kyseisen kontekstin kielelle.

![Muokattavan ER-lausekkeen ER-selitteen käännöksen antaminen ER-muodon suunnittelutoiminnossa.](./media/er-multilingual-labels-refer-in-expression.png)

![Näyte ER-selitteeseen viittaavasta tietojen sidonnasta ER-toiminnon suunnittelutoiminnossa.](./media/er-multilingual-labels-refer-in-binding.png)

ER-muodon **TIEDOSTO**-osan voi määrittää luomaan raportin käyttäjän valitsemalla kielellä.

![TIEDOSTO-osan määrittäminen ER-toiminnon suunnittelutoiminnossa luomaan raportti käyttäjän valitsemalla kielellä.](./media/er-multilingual-labels-language-context-user.png)

Jos ER-muoto määritetään tällä tavoin, raportti luodaan käyttämällä vastaavaa ER-selitteiden tekstiä. Seuraavissa kuvissa on esimerkkejä raporteista, jossa käyttäjän kielenä on EN-US-ja DE-AT.

![Esikatselu raportista, jossa luonnissa on käytetty käyttäjän valitsemaa kieltä EN-US.](./media/er-multilingual-labels-report-preview-en.png)

![Esikatselu raportista, jossa luonnissa on käytetty käyttäjän valitsemaa kieltä DE-AT.](./media/er-multilingual-labels-report-preview-de.png)

Jos viitatussa selitteessä ei ole muodon suorituskontekstin kielistä käännöstä, selitetekstissä käytetään sen sijaan kieltä EN-US.

## <a name="language"></a>Kieli

ER tukee erilaisia tapoja määrittää luodun raportin kieli. **Muoto**-välilehden **Kieliasetukset**-kentässä voi valita seuraavat arvot:

- **Yrityksen asetukset** – luo raportin yrityksen määrittämällä kielellä.

    ![Yrityksen valitseman kielen määrittäminen luodun raportin kieleksi ER-toiminnon suunnittelutoiminnossa.](./media/er-multilingual-labels-language-context-company.png)

- **Käyttäjän asetukset** – luokan raportin käyttäjän valitsemalla kielellä.
- **Määritetty erikseen** – luo raportin suunnitteluvaiheessa määritetyllä kielellä.

    ![Suunnitteluvaiheessa määritetyn kielen määrittäminen luodun raportin kieleksi ER-toiminnon suunnittelutoiminnossa.](./media/er-multilingual-labels-language-context-fixed.png)

- **Määritetty suorituksen aikana** – Luo raportin suorituksen aikana määritetyllä kielellä. Jos valitset tämän arvon, määritä **Kieli**-kentässä ER-lauseke, joka palauttaa kielen kielikoodin, kuten vastaavan asiakkaan kielen.

    ![Suorituksen aikana määritetyn kielen määrittäminen luodun raportin kieleksi ER-toiminnon suunnittelutoiminnossa.](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="culture-specific-formatting"></a>Kulttuurikohtainen muotoilu

ER tukee erilaisia tapoja määrittää luodun raportin kulttuuri. Siksi päivämäärä-, aika- ja numeerisissa arvoissa voidaan käyttää oikeaa kulttuurikohtaista muotoilua. Kun suunnittelet ER-muodon, **Muoto**-välilehdessä **Kulttuuriasetukset**-kentässä voit valita yhden seuraavista arvoista jokaiselle muotokomponentille, jonka tyyppinä on **Common\\File**, **Excel\\File**, **PDF\\File** tai **PDF\\Merger**:

- **Käyttäjän asetukset** – Muotoile arvot käyttäjän ensisijaisen kulttuurin mukaisesti. Kulttuuri määritetään **Päivämäärä-, kellonaika- ja numeromuoto** -kentässä **Asetukset**-välilehdessä **Käyttäjän asetukset** -sivulla.

    ![Käyttäjän ensisijaisen kulttuurin määrittäminen luodun raportin kulttuurina ER-toiminnon suunnittelussa.](./media/er-multilingual-labels-culture-context-user-preferred.png)

- **Määritetty erikseen** – Muotoile arvot suunnittelun aikana määritetyn kulttuurin mukaan.

    ![Suunnittelun aikana määritetyn kulttuurin määrittäminen luodun raportin kulttuurina ER-toiminnon suunnittelussa.](./media/er-multilingual-labels-culture-context-fixed.png)

- **Määritetty suorituksen aikana** – Muotoile arvot suorituksen aikana määritetyn kulttuurin mukaan. Jos valitset tämän arvon, määritä **Määritys**-välilehden **Päivämäärä-, kellonaika- ja numeromuoto** -kenttään ER-lauseke, joka palauttaa kyseisen kulttuurin koodin, kuten vastaavan asiakkaan kulttuurin.

    ![Suorituksen aikana määritetyn kulttuurin määrittäminen luodun raportin kulttuurina ER-toiminnon suunnittelussa.](./media/er-multilingual-labels-culture-context-runtime.png)

> [!NOTE]
> ER-komponentti, jota varten määrität tietyn kulttuurin, voi sisältää ali-ER-komponentteja, jotka on konfiguroitu täyttämään tekstiarvo. Oletusarvon mukaan pääkomponentin kulttuuria käytetään näiden komponenttien arvojen muotoiluun. Seuraavien sisäänrakennettujen ER-toimintojen avulla voit konfiguroida näiden komponenttien siteet ja käyttää vaihtoehtoista kulttuuria arvon muotoiluun:
>
> - [DATEFORMAT](er-functions-datetime-dateformat.md#syntax-2)
> - [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md#syntax-2)
> - [NUMBERFORMAT](er-functions-text-numberformat.md#syntax-2)
>
> Versiossa 10.0.20 ja sitä myöhemmässä versiossa **Common\\File**- ja **Excel\\File**-tyyppien muotokomponenttien aluetta käytetään arvojen muotoiluun luodun asiakirjan [PDF-muuntamisen](electronic-reporting-destinations.md#OutputConversionToPDF) aikana.

## <a name="translation"></a>Käännös

Tarvittavat ER-selitteet voidaan lisätä ER-osaan. Lisättävä ER-selite voidaan kääntää kahdella tavalla: manuaalisesti tai automaattisesti.

### <a name="manual-translation"></a>Manuaalinen kääntäminen

Kun ER-selite lisätään **Tekstin käännös** [-ruutuun](#TextTranslationPane), sen voi kääntää manuaalisesti kaikille kielille, joita nykyisessä Finance-esiintymässä tuetaan. Ensisijaisen kielen voi valita **Järjestelmän kieli**- tai **Käyttäjän kieli** -osan **Kieli**-kentässä, jonka jälkeen sopiva teksti lisätään vastaavaan **Käännetty teksti** -kenttään. Tämän jälkeen valitaan **Käännä**. Tämä prosessi on toistettava kaikkien tarvittavien kielten ja jokaisen lisättävän selitteen osalta.

### <a name="automatic-translation"></a>Automaattinen kääntäminen

ER-osan määritys tehdään sen ER-määrityksen luonnosversiossa, jossa muokattava ER-osa on.

![ER-määrityssivulla voi käyttää määrityksen Luonnos-tilaista versiota.](./media/er-multilingual-labels-configurations.png)

Tarvittavat ER-selitteet voidaan lisätä ER-osaan aiemmin tässä ohjeaiheessa kuvatulla tavalla. Tällä tavoin voit määrittää ER-selitteiden tekstin, joiden kieli on EN-US. Tämän jälkeen ER-osan selitteet viedään sisäisellä ER-toiminnolla. Valitse muokattavan ER-osan sisältävän ER-määrityksen luonnosversio ja valitse **Vaihto \> Vie käyttöliittymätekstit**.

![ER-määrityssivu, josta voi viedä ER-selitteitä valitusta määritysversiosta.](./media/er-multilingual-labels-export.png)

Voit viedä joko kaikki selitteet tai viennin aluksi määritettävän yhden kielen selitteet. Selitteet viedään XML-tiedostot sisältävänä zip-tiedostona. Kussakin XML-tiedostossa on yhden kielen selitteet.

![Esimerkki viedystä tiedostosta, joka sisältää kielen DE-AT ER-selitteet.](./media/er-multilingual-labels-in-xml.png)

Tämä muotoa käytetään, kun ulkopuoliset palvelut, kuten [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md), kääntävät selitteet automaattisesti. Voit tuoda vastaanotetut käännetyt selitteet takaisin sen ER-määrityksen luonnosversioon, joka sisältää kyseiset selitteet omistavat ER-osat. Valitse muokattavan ER-osan sisältävän ER-määrityksen luonnosversio ja valitse sitten **Vaihto \> Lataa käyttöliittymätekstit**.

![ER-määrityssivu, jossa voi tuoda ER-selitteitä valittuun määritysversioon.](./media/er-multilingual-labels-load.png)

Käännetyt selitteet tuodaan valittuun ER-määritykseen. Tässä ER-määrityksessä jo olevat käännetyt selitteet korvataan. Jos ER-määrityksestä puuttuu jokin käännetty selite, se liitetään määritteeseen.

## <a name="lifecycle"></a>Elinkaari

Muokattavan ER-osan selitteet säilytetään yhdessä osan muun sisällön kanssa soveltuvassa ER-määrityksen versiossa.

ER-perusosan selitteisiin voidaan viitata siinä ER-osan johdetussa versiossa, joka luodaan muokkauksia varten.

ER-versiointi määrittää selitteen määrityksen ER-osan määritteisiin. Selitemäärityksen muutokset kirjataan sen muokattavan ER-osan muutosluetteloon (delta), joka on luotu annetun ER-osan johdettuna versiona. Nämä muutokset tarkistetaan, kun johdettu versio pohjustetaan uuteen versioversioon.

## <a name="functions"></a>Toiminnot

Valmiilla [LISTOFFIELDS](er-functions-list-listoffields.md)-ER-funktiolla voi käyttää ER-selitteitä, jotka on määritetty joillekin ER-osien nimikkeille.

Kuten aiemmin tässä ohjeaiheessa todettiin, jokaisen [mallin](#LinkModelEnum) tai [muodon](#LinkFormatEnum) ER-luettelointiarvon **Selite**- tai **Kuvaus**-määritteet voidaan linkittää ER-selitteeseen, jota voidaan käyttää soveltuvassa ER-osassa. ER-lausekkeen voi määrittää, kun **LISTOFFIELDS**-funktio kutsutaan käyttämällä ER-luettelointia argumenttina. Tämä lauseke palauttaa luettelon, joka sisältää kunkin tämän funktion argumentiksi määritetyn ER-luetteloinnin arvon tietueen. Jokainen tietue sisältää ER-luettelointiarvoon linkitetyn ER-selitteen arvon:

- **Selite**-määritteisiin linkitetyn ER-selitteen arvot tallennetaan palautetun tietueen **Selite**-kenttään.
- **Kuvaus**-määritteisiin linkitetyn ER-selitteen arvot tallennetaan palautetun tietueen **Kuvaus**-kenttään.

## <a name="performance"></a><a name=performance></a>Suoritustaso

Kun määrität ER-muotokomponentin luomaan raportin ensisijaisella [kielelläsi](#language) tai tuomaan saapuvan asiakirjan, jossa sisältö on jäsennetty ensisijaisella kielelläsi, on suositeltavaa ottaa käyttöön **Tallenna nykyisen käyttäjän ensisijainen kieli ER-suorituksia varten** -ominaisuus [Ominaisuuksienhallinta](../../fin-ops/get-started/feature-management/feature-management-overview.md)-työtilassa. Tämä ominaisuus parantaa suorituskykyä erityisesti sellaisten ER-muotokomponenttien osalta, jotka sisältävät useita viitteitä ER-reseptien ja -sidontojen otsikoihin sekä useita [vahvistus](general-electronic-reporting-formula-designer.md#TestFormula)-sääntöjä käyttäjäsanomien luontia varten ensisijaisella kielelläsi.

Kun vaihdat ER-konfigurointiversion tilan **Luonnos**-versiosta **Valmis**-tilaksi, nämä otsikot tallennetaan sovellustietokantaan, jos konfiguraatioversiossa on ER-otsikot. Tallennusskeema vaihtelee **Nopeuta ER-otsikoiden tallennusta** -ominaisuuden tilan mukaan:

- Jos toimintoa ei ole otettu käyttöön, kaikki otsikot tallennetaan **ERSOLUTIONVERSIONTABLE**-taulun **LABELXML**-kenttään yksittäisenä XML-katkelmana.
- Jos ominaisuus on käytössä, kullekin kielelle luodaan erillinen tietue **ERSOLUTIONVERSIONLABELSTABLE**-taulussa. Tämän taulun **CONTENTS**-kenttään tallennetaan kielikohtaiset otsikot pakattuna XML-koodina.

Suosittelemme, että otat **Nopeuta ER-otsikoiden tallennusta** -toiminnon käyttöön **ominaisuudenhallinnan** työtilassa. Tämän ominaisuuden avulla voit parantaa kaistanleveyden käyttöä ja järjestelmän yleistä suorituskykyä, koska useimmissa tapauksissa yksittäisen kielen ER-otsikot ovat käytössä, kun käytössä on yksi ER-konfiguraatio.

Jos haluat käyttää valittua tallennusskeemaa kaikkien ER-konfiguraatioiden otsikoiden pitämiseksi nykyisessä Finance-esiintymässä, noudata seuraavia ohjeita.

1. Siirry kohtaan **Organisaation hallinto** > **Kausittaiset** > **Käytä valittua otsikoiden tallennuksen skeemaa kaikille ER-konfiguraatioille**.
2. Valitse **OK**.


## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin funktiot](er-formula-language.md#Functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
