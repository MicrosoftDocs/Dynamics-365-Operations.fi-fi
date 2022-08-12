---
title: Google Payn määrittäminen Adyen-käyttöä varten
description: Tässä artikkelissa käsitellään Google Payn määrittämistä Adyenia varten Microsoft Dynamics 365 Commercessa.
author: BrianShook
ms.date: 07/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c3f049946c66fcd8560f7c08a4cb2beab0dcd5b2
ms.sourcegitcommit: 3d2c0a39c4f987e9ac71df2f2fa6df0f64f10b2b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2022
ms.locfileid: "9115027"
---
# <a name="configure-google-pay-with-adyen"></a>Google Payn määrittäminen Adyen-käyttöä varten

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään Google Payn määrittämistä Adyenia varten Microsoft Dynamics 365 Commercessa.

Dynamics 365 Commerce sisältää käyttövalmiin Google Payn integroinnin Adyen-maksuyhdyskäytäväpalvelua käytettäessä. Maksutapana Google Pay on digilompakko, joka käyttää Google Payn myyjätiliä yhdessä Adyen-maksupalvelun kanssa. Määritettynä Google Pay -painike on käytettävissä valittavana maksutapana verkkotilauksen kassalla. Kun käyttäjät valitsevat **Google Payn** tuetussa selaimessa tai laitteessa, heidät ohjataan suorittamaan maksu suoraan Google Pay -palvelussa. Sen jälkeen he palaavat verkkomyymälään viimeistelemään tilauksen.

Jos Google Payta käytetään Commercen pikakassamoduulissa, käyttäjän maksutilin tiedot täytetään automaattisesti kassalomakkeessa, mikä nopeuttaa käyttäjän kassaprosessia. Commerce sisältää pikamaksumoduulin, joka mahdollistaa pikakassatoiminnan. Pikamaksumoduulia voidaan käyttää osassa, joka sisältyy kassa- tai ostoskorisivuun. Google Payn Dynamics 365 Payment Connector -yhdistimen viitettä käytetään yhdessä Adyenin Dynamics 365 Payment Connectorin kanssa mahdollistamaan sekä pikamaksu- että normaalit kassavaihtoehdot, kun PayPal on määritetty. Google Pay voidaan määrittää myös Adyen-maksupäätteissä ja Commercen myyntipisteessä käyttöä varten, joten sitä voi käyttää myös myymälässä.

## <a name="key-terms"></a>Tärkeimmät termit

| Kausi | Kuvaus |
|---|---|
| Google Pay | Myös Google Pay -painikkeena tunnettu Google Pay on lompakkomaksutuote, jota tuetaan Adyen-yhdistimen kautta. Se mahdollistaa Dynamics Google Pay Connectorin tukeman asiakaskokemuksen ja integroinnin. |
| Lompakko | Maksutyyppi, joka ei sisällä perinteisiä maksuominaisuuksia, kuten pankin tunnistenumeroaluetta (BIN) ja vanhentumispäivää, joita käytetään erottamaan luotto- ja pankkikortit toisistaan. |
| Pikamaksumoduuli | Dynamics 365 Commerce -moduuli, joka tukee nopeutettuja kassatoimintoja ja tuettuja maksutapoja. |

## <a name="prerequisites"></a>Edellytykset

Google Payn käyttö Adyenin avulla Commercessa edellyttää Googlen myyjätiliä. Lisätietoja Googlen myyjätilin määrittämisestä on kohdassa [Google Payta koskevat Adyen-ohjeet](https://docs.adyen.com/payment-methods/google-pay/) ja Googlen [integroinnin tarkistusluettelossa](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist).

Google Pay -maksutapa on oltava integroituna myös Adyen-tiliin. Integrointilinkin ohjeet ovat kohdassa [Adyen Google Pay](https://www.adyen.com/payment-methods/google-pay).

Lisäksi laajennettu lompakko-ominaisuus on otettava käyttöön Dynamics 365 Commerce headquartersissa. Valitse **Työtilat \> Ominaisuuksien hallinta**, hae **Tehostettu lompakon tuki ja maksujen parannukset** -ominaisuus, valitse se ja valitse lopuksi **Ota käyttöön**. Kun ominaisuus on otettu käyttöön, varmista **1110**-jakeluaikataulu suosittamalla, että muutos on saatavana kaikissa kanavissa.

## <a name="map-the-google-pay-payment-method"></a>Google Pay -maksutavan yhdistäminen

Google Pay on maksutapana digitaalinen lompakko. Lisätietoja Google Payn maksun yhdistämisestä on kohdassa [Lompakkomaksun tuki](../wallets.md).

Google Pay -maksutapa yhdistetään sekä myyntipiste- että verkkokanavien korttimaksuvälinetyyppiin seuraavien ohjeiden mukaan.

1. Valitse Commerce headquartersissa **Retail ja Commerce \> Kanavan asetukset \> Maksutavat \> Korttityypit**.
1. Lisää Google Pay -rivi valitsemalla **Uusi**.
1. Syötä **Tunnus**-kenttään **GooglePay**.
1. Syötä **Sähköisen maksun nimi** -kenttään **Google Pay**.
1. Syötä **Tyyppi**-kenttään **Lompakko**.
1. Syötä **Myöntäjä**-kenttään **Google**.
1. Avaa **Käsittelijämaksun yhdistämistavat** -valintaikkuna valitsemalla toimintoruudussa **Suorittimen yhdistämismääritys**.
1. **Käsittelijän maksutapojen yhdistämismääritys poistettu** -kohdassa luettelo yhdistämättömistä käsittelijän maksutoivoista, joista jokaisella on pariliitos yhdistimeen. Yhdistämättömän Google Payn käsittelijän maksutavat yhdistetään korttimaksuvälinetyyppeihin toimimalla seuraavasti kunkin korttimaksuvälinetyypin osalta:

    1. Valitse kortin maksuvälinetyyppi **Korttimaksuvälineen tyypit** -kohdassa.
    1. Valitse **Käsittelijän maksutapojen yhdistämismääritys poistettu** -sarakkeessa sekä **Adyenin Dynamics 365 Payment Connector** -yhdistin (käytetään myyntipisteessä) ja **Google Payn Dynamics 365 Payment Connector** -yhdistin (käytetään verkkokanavissa).
    1. Valitse **Lisää**. Valinnat lisätään **Yhdistetyt käsittelijän maksutavat** -sarakkeeseen.

1. Kun maksutavat on yhdistetty, valitse **Tallenna**.
1. Valitse **Korttityypit**-sivulla **Tallenna**.

## <a name="configure-a-commerce-online-store-for-google-pay"></a>Commerce-verkkokaupan määrittäminen Google Payta varten

Commerce-verkkokauppa määritetään käyttämään Google Payta seuraavasti.

1. Valitse Commerce headquartersissa **Retail ja Commerce \> Kanavat \> Verkkokaupat**.
1. Valitse sivuston verkkokauppakanava valitsemalla kanavan **Vähittäismyyntikanavan tunnus** -arvo.
1. Varmista **Maksutilit**-pikavälilehden **Yhdistin**-kohdassa, että **Adyenin Dynamics 365 Payment Connector** -yhdistin on luettelossa. Jos sitä ei ole luettelossa, lisää se kohdassa [Adyenin Dynamics 365 Payment Connectorin määrittäminen](adyen-connector-setup.md) olevien ohjeiden mukaisesti.

    > [!NOTE]
    > Useimmissa tapauksissa **Adyenin Dynamics 365 Payment Connector** -yhdistimen on oltava luettelossa kanavan ensimmäinen yhdistin (ensimmäistä yhdistintä kutsutaan myös ensisijaiseksi yhdistimeksi). Sen jälkeen luettelossa on oltava muut käytettävät yhdistimet, kuten **PayPalin Dynamics 365 Payment Connector**- **GooglePayn Dynamics 365 Payment Connector** -yhdistimet.

1. Kun **Adyenin Dynamics 365 Payment Connector** -yhdistin on lisätty, lisää **GooglePayn Dynamics 365 Payment Connector** -yhdistin valitsemalla **Lisää**. Määritä sitten yhdistimen seuraavat ominaisuudet.

    | Kenttä                  | Kuvaus | Pakollinen | Automaattinen määritys | Mallin arvo |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Kokoonpanon nimi          | GooglePayn Dynamics 365 Payment Connectorin kokoonpanon nimi. | Kyllä | Kyllä | *Binaarinimi* |
    | Palvelutilin tunnus     | Myyjän ominaisuuksien määrittämisen yksilöivä tunniste. Tämä tunniste leimataan maksutapahtumiin, ja se määrittää myyjän ominaisuudet, joita on käytettävä myöhemmissä prosesseissa (kuten laskutuksessa). | Kyllä | Kyllä | *GUID* |
    | Googlen myyjätunnus     | Anna Googlen myyjätilille määritetty Googlen myyjätunnus. Tätä ominaisuutta tarvitaan tuotantoympäristöissä, mutta se on valinnainen testiympäristöissä. Lisätietoja on sivustossa <https://pay.google.com/>. | Kyllä | En | *Numeerinen tunniste* |
    | Myyjätilin tunnus    | Anna yksilöivä Adyenin myyjätunniste. Tämä arvo annetaan Adyen-rekisteröinnin yhteydessä. Lisätietoja on kohdassa [Rekisteröityminen Adyeniin](adyen-connector-setup.md#sign-up-with-adyen). | Kyllä | En | *Myyjän tunniste* |
    | Pilviohjelmointirajapinnan avain          | Anna Adyenin pilviohjelmointirajapinnan avain. Lisätietoja tämän avaimen hankkimisesta on kohdassa [Ohjelmointirajapinta-avaimen hankkiminen](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Kyllä | En | "abcdefg" |
    | Yhdyskäytäväympäristö    | Adyen-yhdyskäytäväympäristö, johon yhdistäminen tehdään. Mahdolliset arvot ovat **Testi** ja **Live**. Tämän kentän arvoksi kannattaa määrittää **Live** vain tuotantolaitteissa ja -tapahtumissa. | Kyllä | Kyllä | "Live" |
    | Tuetut valuutat   | Valuutat, jotka yhdistimen on käsiteltävä. Korttia käytettäessä Adyen voi tukea muita valuuttoja [dynaamisen valuuttamuunnoksen](https://www.adyen.com/pos-payments/dynamic-currency-conversion) kautta sen jälkeen, kun tapahtumapyyntö on lähetetty maksupäätteeseen. Pyydä tuettujen valuuttojen luettelo ottamalla yhteys Adyen-tukeen. | Kyllä | Kyllä | "USD;EUR" |
    | Tuetut maksuvälinetyypit | Maksuvälinetyypit, jotka yhdistimen on käsiteltävä. | Kyllä | Kyllä | "GooglePay" |

1. Kun yhdistimen ominaisuudet on määritetty, suorita **1070 (Kanavan konfigurointi**) -jakeluaikataulutyö.

## <a name="configure-commerce-pos-for-google-pay"></a>Commercen myyntipisteen määrittäminen Google Payta varten

Myyntipistemääritys käyttää laiteprofiilin **EFT-palvelu**-kentän asetusta Adyenin Dynamics 365 Payment Connectorissa. Lisätietoja sähköisen rahansiirtopalvelun (EFT-palvelun) määrittämisestä Adyenin Dynamics 365 Payment Connectorille Commerce headquartersissa on [Dynamics 365:n POS-laiteprofiili -osassa](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Adyen-yhdistimen yhdistävä käsittelijä sieppaa lompakon korttityypit, joita Google Pay käyttää kassapäätteessä.

### <a name="use-the-payment-express-module-with-google-pay"></a>Google Payn pikamaksumoduuliin käyttäminen

Commercen pikamaksumoduuli toimii tuettujen maksutapojen kanssa, ja sen avulla sivuston asiakkaat voivat suorittaa kassatapahtumat entistä nopeammin käyttämällä maksupalvelun tilitietoja kassaprosessin aikana. Pikamaksumoduuli hyödyntää määritettyä yhdistinpainiketta ja palauttaa käyttäjän valitsemat tilauksen tiedot (osoitteen, yhteystiedot ja maksutavan), jotka täytetään valmiiksi kassalomakkeeseen.

Kun pikamaksumoduulia käytetään Google Payn kanssa ja jos asiakkaat valitsevat Google Pay -painikkeen **Pikamaksu**-osassa, Google Payn iframe-ikkuna avautuu. Käyttäjät voivat sitten kirjautua Google-tilille ja käyttää tilin toimitusosoitetta, laskutusosoitetta, sähköpostiosoitetta ja Google Pay -maksutapaa tapahtuman maksamiseen.

Kun käyttäjät ovat suorittaneet tapahtuman Google Pay ikkunassa, heidät ohjataan takaisin Commerce-sivuston kassasivulle, jossa kassalomakkeeseen on täytetty valmiiksi Google Pay -tilin tiedot. Käyttäjät näkevät Google Pay -ikkunasta paluun jälkeen kassasivulla seuraavat tiedot:

- Pikamaksutyökulussa ensimmäinen toimitusvaihtoehdon käytettävissä oleva toimitusosoite, joka palautettiin, valitaan valmiiksi käyttäjälle.
- Google Payta käytettäessä mitään yhteyshenkilön sähköpostiosoitetta ei palauteta. Vieraskäyttäjien on annettava kassalla sähköpostiosoite kassasivun yhteyshenkilöosassa. Kirjautuneiden käyttäjien yhteystiedot täytetään automaattisesti Dynamics-asiakastililtä (todennukseen käytettävä ensisijainen sähköpostiosoite).

Asiakkailla on mahdollisuus tarkistaa tilaukset ja muuttaa kassalla tilauksen tietoja ennen tilauksen viimeistelyä **Tee tilaus** -valinnalla.

### <a name="configure-google-pay-in-site-builder"></a>Google Payn määrittäminen sivustonmuodostimessa 

Ennen osien tai sivujen määrittämistä Google Payn avulla on varmistettava, että sivuston sisällön suojauskäytännön on määritetty Commercen sivustonmuodostimessa.

Sisällön suojauskäytäntöjen määrittäminen sivustonmuodostimessa voidaan varmistaa seuraavasti.

1. Valitse sivustossa **Sivuston asetukset \> Laajennukset**.
1. Lisää **Sisällön suojauskäytäntö** välilehdessä `*.google.com`-rivi **child-src**-, **connect-src**-, **frame-ancestors**-, **frame-src**-, **img-src**-, **script-src**- ja **style-src**-direktiivit.
1. Kun olet valmis, valitse **Tallenna ja julkaise**.

### <a name="configure-the-payment-express-fragment-with-google-pay-in-site-builder"></a>Google Payn pikamaksuosan määrittäminen sivustonmuodostimessa

Google Payn pikamaksuosa määritetään verkkokauppaan seuraavasti.

1. Valitse sivustonmuodostimessa **Katkelmat**.
1. Valitse **Uusi**.
1. Valitse **Uusi osa** -valintaikkunassa **Säilö**-moduuli, anna osan nimi (kuten **Pikakassa**) ja valitse sitten **OK**. 
1. Valitse uuden osan **Oletussäilö**-paikka.
1. Määritä oikealla olevassa ominaisuusruudussa säilömoduulin ominaisuudet:

    - **Otsikko** – anna otsikko, joka näytetään sivuston pikakassaosalle (esimerkiksi **Pikakassa**).
    - **Säilön asettelu** – valitse **Työnkulku**.
    - **Leveys** – Valitse **Täytä säilö**.
    - **Näytettävät alielementit** – Määritä kassasivun pikakassaosan riville sopivaksi alielementtien määräksi **Kolme**. (Kyse voi olla esimerkiksi tekstiruudusta, PayPal-pikamaksusta ja Google Pay -pikamaksusta.)
    - **CSS-luokan nimi** – syötä **msc-express-payment-container** (pakollinen).

    > [!IMPORTANT]
    > - **CSS-luokan nimi** -arvoksi on määritettävä **msc-express-payment-container**, sillä he hallitsee säilön toimintaa kassalla. Toiminta koskee piilottamista, kutistamista ja muita toimintoja, jotka koskevat pikakassaosaa kassatyönkulun aikana. **msc-express-payment-container**-luokka toimii oletustoiminnoissa, jotka on julkaistu moduulikirjaston kassamoduulin yhteydessä.
    > - **CSS-luokan nimeen** voidaan sisällyttää muita tyylejä. Jos moduulin toimintaa muokataan, tyyliohjausobjektien keskinäinen toiminta on tarkistettava, jos pikakassan toimintaa varten kassamoduulissa käytetään saman moduulikirjaston koodattua toimintaa.

1. Valitse kolme pistettä (**...**) **Oletuskontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Pikamaksu**-moduuli ja valitse sitten **OK**.
1. Määritä tai muokkaa **Pikamaksu**-moduulin ominaisuusruudussa **iFramein korkeus** -arvoa. Arvo annetaan kuvapisteinä (esimerkiksi **60**).
1. Syötä **Tuetut maksuvälinetyypit** -kenttään **GooglePay**. Arvon on vastattava **Tuetut maksuvälinetyypit** -merkkijonoa kanavaan määritetyssä yhdistimessä. (Lisätietoja on aiemmin tässä artikkelissa kohdassa [Commerce-verkkokaupan määrittäminen Google Payta varten](#configure-a-commerce-online-store-for-google-pay).)

    > [!NOTE]
    > Muiden maksutapojen **Pikamaksu**-moduulit voidaan lisätä toistamalla vaiheet 6–9. **Tuetut maksuvälinetyypit** -arvon on vastattava muita määritettyjä maksutyyppejä (esimerkkinä **Paypal**).

1. Valinnainen: Ohjeet tai ilmoitustiedot voidaan sisällyttää lisäämällä tekstilohkomoduuli oletussäilömoduuliin. Kirjoita toivottu teksti moduulin lisäämien jälkeen ominaisuusruudun **Muotoiltu teksti** -kenttään. Tekstin voi sijoittaa pikamaksumoduulien ylä- tai alapuolelle valitsemalla kolme pistettä (**...**) **Tekstilohko**-paikassa ja valitsemalla sitten **Siirrä ylös** tai **Siirrä alas**.
1. Tallenna muutokset valitsemalla **Tallenna** ja valitse sitten **Viimeistele muokkaaminen**.
1. Julkaise katkelma valitsemalla **Julkaise**.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Lisää maksun pikaosa kassasivulle

Pikamaksuosan voi lisätä kassasivulle seuraavasti.

1. Valitse sivustonmuodostimessa **Sivut** ja valitse sitten sivuston kassasivu.
1. Valitse **Muokkaa**.
1. Valitse **Pää-kohteessa** kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Määritä oikealla olevassa ominaisuusruudussa säilömoduulin ominaisuudet:

    - **Kontin asettelu** – Valitse **Pinottu**.
    - **Leveys** – Valitse **Täytä säilö**.
    - **Näytettävät alielementit** – Määritä kassasivun pikakassaosan riville sopivaksi alielementtien määräksi **Kolme**. (Kyse voi olla esimerkiksi tekstiruudusta, PayPal-pikamaksusta ja Google Pay -pikamaksusta.)

1. Valitse **Säilö**-moduulipaikassa kolme pistettä (**...**) ja valitse sitten **Lisää osa**.
1. Valitse **Valitse osa** -valintaikkuna, valitse aiemmin luotu pikamaksuosa ja valitse sitten **OK**.
1. Tallenna muutokset valitsemalla **Tallenna** ja valitse sitten **Viimeistele muokkaaminen**.
1. Julkaise sivu valitsemalla **Julkaise**.

> [!NOTE]
> Jos kassasivulla on jo kassaosan sisältävä säilö ja pikamaksumoduuli halutaan hahmontaa tavallisen kassasäilön yläpuolelle, se voidaan sijoittaa aiemmin luodun kassan ylä- tai alapuolelle valitsemalla kolme pistettä (**...**) **Pää-kohdassa** ja valitsemalla sitten **Siirry ylös** tai **Siirrä alas**.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Lisää maksun pikaosa ostoskorisivulle

Pikamaksuosan voi lisätä ostoskorisivulle seuraavasti.

1. Valitse sivustonmuodostimessa **Sivut** ja valitse sitten sivuston ostoskorisivu.
2. Valitse **Muokkaa**.
3. Laajenna jäsennysnäkymässä **Pää-kohta** puunäkymässä ja etsi säilö, joka sisältää **Ostoskori**-moduulin.
4. Valitse **Ostoskori**-moduulissa **Pikamaksu**-paikka, valitse sitten kolme pistettä (**...**) ja valitse lopuksi **Lisää moduuli**.
5. Valitse **Valitse moduulit** -valintaikkunassa **Pikamaksu**-moduuli ja valitse sitten **OK**.
6. Valitse **Pikamaksu**-moduulin paikka. Syötä sitten oikealla olevassa ominaisuusruudussa **Tuetut maksuvälinetyypit** -kohtaan **GooglePay**. Arvon on vastattava **Tuetut maksuvälinetyypit** -merkkijonoa kanavaan määritetyssä yhdistimessä. (Lisätietoja on aiemmin tässä artikkelissa kohdassa [Commerce-verkkokaupan määrittäminen Google Payta varten](#configure-a-commerce-online-store-for-google-pay).)
1. Tallenna muutokset valitsemalla **Tallenna** ja valitse sitten **Viimeistele muokkaaminen**.
1. Julkaise sivu valitsemalla **Julkaise**.

Käyttäjät voivat sisällyttää enintään kolme tuettua **Pikamaksu**-moduulia (eli käytettävissä on kolme tuettua maksuvaihtoehtoa) ostoskorin **Pikamaksu**-paikkaan.

### <a name="set-up-google-pay-as-an-option-in-the-checkout-payment-section"></a>Google Payn määrittäminen vaihtoehdoksi kassan maksuosassa

Google Pay voidaan määrittää vaihtoehdoksi kassan vain maksuun tarkoitetun, muun kuin pikatoiminnon maksuosassa. Käyttäjä täyttää kassalomakkeen ja Google Pay -kassasivu valmistelee kassan vain Google Pay -maksua varten. Google-tilin tietoja ei käytetä korvaamaan kassalla täytettyjä tietoja.

> [!NOTE]
> Seuraavassa menettelyssä oletetaan, että sivusto käyttämään kassaosaan on määritetty noutotiedot, toimitusosoite, toimitusvaihtoehdot, yhteystiedot, valinnaiset käyttöehdot ja osa kassaelementtejä varten. Julkaistussa moduulikirjaston oletuskassamoduulissa kassaosan säilö, jossa on tekstilohko-, kanta-asiakkuuspiste-, lahjakortti- ja maksumoduulit. Lisätietoja on kohdassa [Maksumoduuli](../payment-module.md).

Google Payn voi määrittää seuraavasti normaaliksi maksuvaihtoehdoksi kassasivun **Maksutapa**-osassa.

1. Valitse sivustonmuodostimessa **Osat** ja valitse sitten sivuston kassaosa.
1. Valitse **Muokkaa**.
1. Valitse **Kassatiedot**-paikassa kolme pistettä (**…**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Maksu**-moduuli ja valitse sitten **OK**.
1. Määritä oikealla olevassa **Maksu**-moduulin ominaisuusruudussa säilömoduulin ominaisuudet:

    - **Otsikko** – anna otsikko, joka näytetään sivuston pikakassaosalle (esimerkiksi **Google Pay**).
    - **iFramen korkeus** – muuta arvoksi sopiva korkeus kuvapisteinä (esimerkiksi **75**). 
    - **Tuetut maksuvälinetyypit** – anna **GooglePay**, mikä vastaa Google Pay -yhdistimen määritystä Commerce headquartersissa.
    - **On ensisijainen maksu** – Jätä valintaruutu tyhjäksi. (Tämä ominaisuus on tyypillisesti otettu käyttöön Adyen-kassamoduulissa.)
    - **Maksun tyylin ohitus** – tätä ominaisuutta ei tueta Google Pay -määrityksissä.
    - **Käytä yhdistimen tunnusta** – tämä ominaisuus on valittava, jos sivulla käytetään useita maksuyhdistimiä.

1. Sijoita moduuli muiden maksumoduulien ylä- tai alapuolelle valitsemalla kolme pistettä (**...**) **Maksu**-paikassa ja valitsemalla sitten **Siirrä ylös** tai **Siirrä alas**.
1. Tallenna muutokset valitsemalla **Tallenna** ja valitse sitten **Viimeistele muokkaaminen**.
1. Valitse **Julkaise**.

### <a name="modes-of-delivery"></a>Toimitustavat

Google Payta käyttävässä pikamaksumoduulissa ensimmäinen toimitusvaihtoehto, joka palautetaan valituksi toimitusosoitteeksi Google Pay -tililtä, valitaan valmiiksi. Käyttäjillä on mahdollisuus vaihtaa toimitusosoite tarvittaessa.

Järjestys, jossa toimitustavat näkyvät pikamaksumoduulissa, määritetään kanavan **Toimitustavat**-sivulla Commerce headquartersissa. Valitse Commerce headquartersissa **Retail ja Commerce \> Kanavat \> Verkkokaupat** ja valitse kaupan **Vähittäismyyntikanavan tunnus**. Valitse toimintoruudun **Asetukset**-välilehdessä **Toimitustavat**. Luettelossa olevat toimitustavat näkyvät samassa järjestyksessä pikamaksumoduulissa. Lisää tai poista vähittäismyyntikanavan tai tuotteen toimitustapoja valitsemalla toimintoruudussa **Ylläpidä toimitustapoja**. Lisätietoja toimitustapojen määrittämisestä on kohdassa [Toimitustapojen määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Kassamoduuli käyttää myös toimitusvaihtoehtomoduulia, kun toimitustavat hahmonnetaan kassalla. Lisätietoja on kohdassa [Toimitusvaihtoehdot-moduuli](../delivery-options-module.md).

Toimitustavat näytetään, kun lisätään **Toimitustavat**-luetteloon verkkokaupassa.

## <a name="additional-resources"></a>Lisäresurssit

[Maksut – usein kysytyt kysymykset](payments-retail.md)

[Kassamoduuli](../add-checkout-module.md)

[Maksumoduuli](../payment-module.md)
