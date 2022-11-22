---
title: Apple Payn määrittäminen Adyenia varten Dynamics 365 Commercessa
description: Tässä artikkelissa käsitellään Apple Payn määrittämistä Adyenia varten Microsoft Dynamics 365 Commercessa.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 0949b9d7a4b181605d43956932b4fc095940bd64
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780355"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>Apple Payn määrittäminen Adyenia varten Dynamics 365 Commercessa

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tässä artikkelissa käsitellään Apple Payn määrittämistä Adyenia varten Microsoft Dynamics 365 Commercessa.

## <a name="key-terms"></a>Tärkeimmät termit

| Termi | Kuvaus |
|---|---|
| Apple Pay | Myös Apple Pay -painikkeena tunnettu Apple Pay on lompakkomaksutuote, jota tuetaan Adyen-yhdistimen kautta. Se mahdollistaa Microsoft Dynamics 365 Apple Pay Connectorin tukeman asiakaskokemuksen ja integroinnin. |
| Lompakko | Maksutyyppi, joka ei sisällä perinteisiä maksuominaisuuksia, kuten pankin tunnistenumeroaluetta (BIN) ja vanhentumispäivää, joita käytetään erottamaan luotto- ja pankkikortit toisistaan. |

Dynamics 365 Commerce sisältää käyttövalmiin Apple Payn integroinnin Adyen-maksuyhdyskäytäväpalvelua käytettäessä. Maksutapana Apple Pay on digilompakko, joka käyttää Apple Payn myyjätiliä yhdessä Adyen-maksupalvelun kanssa. Määritettynä Apple Pay -painike on valittavana maksutapana verkkokaupan tilauksen kassasivulla. Apple Pay -painike näkyy maksuvaihtoehtona vain tuetuissa Apple Pay -laitteissa. Kun käyttäjät valitsevat **Apple Payn** tuetussa selaimessa tai laitteessa, heidät ohjataan suorittamaan maksu suoraan Apple Pay -palvelussa. Sen jälkeen he palaavat verkkomyymälään tilauksen viimeistelyä varten.

Dynamics 365 Payment Connector Apple Payta varten -yhdistimen viitettä käytetään yhdessä Dynamics 365 Payment Connector Adyenia varten -yhdistimen kanssa mahdollistamaan Apple Pay- ja luottokorttimaksut sivustossa. Apple Pay voidaan määrittää myös käytettäväksi myymälöissä, joissa on Dynamics 365 Payment Connector Adyenia varten -ratkaisua käyttävät Adyenin maksupäätteet. Tässä tapauksessa Dynamics 365 Payment Connector Adyenia varten käsittelee Applen maksulaitteen napautuksen päätteen kautta.

## <a name="prerequisites"></a>Edellytykset

Apple-myyjätili on pakollinen Commercessa, kun käytössä on Apple Pay Adyenia varten. Lisätietoja Apple Payn määrittämisestä testiasiakasalueella on kohdassa [Apple Payn pudotusintegrointi](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay). Lisätietoja tuotantoympäristön käyttöönotosta on kohdassa [Käyttöönotto](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).

Apple Pay -maksutapa on integroitava myös Adyen-tiliin. Adyenin avulla voit määrittää maksutavan ja varmistaa, että toimialueet, joilla sertifikaattia käytetään, on määritetty käyttämään kyseistä sertifikaattia.

Jos haluat ottaa käyttöön laajennetun lompakko-ominaisuuden merkinnän Commerce headquartersissa, siirry kohtaan **Työtilat \> Ominaisuuksien hallinta** ja hae **Tehostettu lompakon tuki ja maksujen parannukset** -ominaisuus. Valitse toiminto ja valitse sitten **Ota käyttöön**. Kun ominaisuus on otettu käyttöön, varmista **1110**-jakeluaikataulu suosittamalla, että muutos on saatavana kaikissa kanavissa.

## <a name="map-the-apple-pay-payment-method"></a>Apple Pay -maksutavan yhdistäminen

Apple Pay on maksutapana digitaalinen lompakko. Lisätietoja Apple Payn maksun yhdistämisestä on kohdassa [Lompakkomaksun tuki](../wallets.md).

Voit yhdistää Apple Pay -maksutavan Commerce headquartersissa alla olevien ohjeiden avulla.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Maksutavat \> Korttityypit**.
1. Lisää Apple Payn rivi valitsemalla **Uusi** ja määritä sille seuraavat arvot:

    - **Tunnus:** ApplePay
    - **Sähköisen maksun nimi:** Apple Pay
    - **Tyyppi:** Lompakko
    - **Myöntäjä:** Apple

1. Avaa **Käsittelijämaksun yhdistämistavat** -valintaikkuna valitsemalla **Suorittimen yhdistämismääritys**. **Käsittelijän maksutapojen yhdistämismääritys poistettu** -sarakkeessa ovat jokaisen käytettävissä olevan yhdistimen tuetut maksumenetelmät (Adyen, PayPal ja Apple).
1. Yhdistä haluamasi tuetut maksutavat **Dynamics 365 Payment Connector Adyenia varten** -yhdistintä (myyntipisteessä käytettäväksi) ja **Dynamics 365 Payment Connector Apple Payta varten** -yhdistin (verkkokanavassa käytettäväksi).
1. Valitse **Käsittelijän maksutapojen yhdistämismääritys poistettu** -sarakkeen jokaisella yhdistämismääritysrivillä tuettava rivi ja valitse sitten **Lisää**, jos haluat siirtää valinnat **Yhdistetyt käsittelijän maksutavat** -sarakkeeseen.
1. Valitse **OK** ja valitse sitten **Korttityypit**-sivulla **Tallenna**.

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>Apple Pay -sertifikaatin määrittäminen sivustossa

Lataa jokaista sivustoa varten toimialueen liitostiedosto (jota kutsutaan myös Apple Pay -sertifikaatiksi) [Adyen Apple Pay -ohjeiden](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live) mukaisesti. Voit käyttää Commercen sivustonmuodostinta toimialueen liitostiedoston lataamisessa sivuston mediakirjastoon.

Noudattamalla alla olevia ohjeita voit määrittää Apple Pay -sertifikaatin sivustonmuodostimessa.

1. Lataa sertifikaatti (toimialueen liitostiedosto) [Adyenista](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).
1. Lisää .txt-tunniste toimialueen liitostiedostoon.
1. [Lataa](../upload-serve-static-files.md) sivustonmuodostimessa toimialueen liitostiedosto sivuston mediakirjastoon.
1. Valitse **URL-osoitteet**.
1. Valitse **Uusi \> Uusi URL-soite**.
1. Valitse **Uusi URL-osoite** -valintaikkunassa **Mediakirjaston resurssi**.
1. Syötä **URL-osoitteen polku** -kenttään URL-osoitteen polku (jos sitä ei ole vielä syötetty). Syötä toimialueen URL-perusosoitteen jälkeen seuraava pakollinen Apple-merkkijono: `<domain>/.well-known/apple-developer-merchantid-domain-association.txt`.
1. Valitse **Seuraava**. Mediakirjastossa näkyvät kaikki ja siinä näkyvät kaikki ladatut **asiakirjatyyppiset** (.txt) mediaresurssit.
1. Valitse toimialueen liitostiedosto, joka on tarkoitettu aiemmin määritetylle URL-osoitteelle.
1. Valitse **Luo**.

Tässä vaiheessa luomasi URL-osoite on luonnostilassa. Viimeistele prosessi julkaisemalla URL-osoite. Tiedostoa, johon URL-osoite osoittaa, ei palauteta, ennen kuin julkaiset URL-osoitteen.

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>Commerce-verkkokaupan määrittäminen Apple Payta varten

Voit määrittää Commercen verkkokaupan Apple Paylle alla olevien ohjeiden mukaan.

1. Valitse Commerce headquartersissa **Retail ja Commerce \> Kanavat \> Verkkokaupat**.
1. Valitse sivuston verkkokauppakanavan **vähittäismyyntikanavan tunnuksen** arvo.
1. Lisää **Maksutilit**-pikavälilehdessä **Dynamics 365 Payment Connector Adyenia varten** -yhdistin, jos sitä ei ole vielä määritetty. Seuraa [Dynamics 365 Payment Connector Adyenia varten -määritys](adyen-connector-setup.md) -kohdan ohjeita.
1. Kun Adyen-yhdistin on määritetty, valitse **Lisää** lisätäksesi **Dynamics 365 Payment Connector Apple Payta varten** -yhdistin.
1. Syötä yhdistimen myyjän ominaisuuksien arvot.

    | Ominaisuus               | Kuvaus | Pakollinen | Automaattinen määritys | Mallin arvo |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Kokoonpanon nimi          | Apple Payn Dynamics 365 Payment Connectorin kokoonpanon nimi. | Kyllä | Kyllä | Binaarinimi |
    | Palvelutilin tunnus     | Myyjän ominaisuuksien määrittämisen yksilöivä tunniste. Tämä tunniste leimataan maksutapahtumiin, ja se määrittää myyjän ominaisuudet, joita on käytettävä myöhemmissä prosesseissa (kuten laskutuksessa). | Kyllä | Kyllä | Guid |
    | Myyjätilin tunnus    | Anna yksilöivä Adyenin myyjätunniste. Tämä arvo annetaan Adyen-rekisteröinnin yhteydessä. Lisätietoja on kohdassa [Rekisteröityminen Adyeniin](adyen-connector-setup.md#sign-up-with-adyen). | Kyllä | En | MerchantIdentifier |
    | Pilviohjelmointirajapinnan avain          | Anna Adyenin pilviohjelmointirajapinnan avain. Lisätietoja tämän avaimen hankkimisesta on kohdassa [Ohjelmointirajapinta-avaimen hankkiminen](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Kyllä | En | abcdefg |
    | Yhdyskäytäväympäristö    | Syötä Adyen-yhdyskäytäväympäristö, johon yhdistäminen tehdään. Mahdolliset arvot ovat **Testi** ja **Live**. Tämän kentän arvoksi kannattaa määrittää **Live** vain tuotantolaitteissa ja -tapahtumissa. | Kyllä | Kyllä | Live-tila |
    | Tuetut valuutat   | Syötä valuutat, joita yhdistimen on käsiteltävä. Korttia käytettäessä Adyen voi tukea muita valuuttoja [dynaamisen valuuttamuunnoksen](https://www.adyen.com/pos-payments/dynamic-currency-conversion) kautta sen jälkeen, kun tapahtumapyyntö on lähetetty maksupäätteeseen. Pyydä tuettujen valuuttojen luettelo ottamalla yhteys Adyen-tukeen. | Kyllä | Kyllä | USD;EUR |
    | Tuetut maksuvälinetyypit | Syötä maksuvälinetyypit, joita yhdistimen on käsiteltävä. | Kyllä | Kyllä | ApplePay |

1. Kun myyjän tiedot on syötetty, suorita **1070**-kanavan määrityksen jakelun ajoitustyö.

## <a name="configure-commerce-pos-for-apple-pay"></a>Commercen myyntipisteen määrittäminen Apple Payta varten

Myyntipistemääritys käyttää laiteprofiilin **EFT-palvelu**-kentän määritystä Dynamics 365 Payment Connector Adyenia varten -yhdistimessä. Määritä Commerce headquartersissa EFT-palvelun Dynamics 365 Payment Connector Adyenia varten -yhdistimelle kohdan [Dynamics 365:n POS-laiteprofiili -osassa](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile) ohjeiden mukaan.

Varmista, että maksuvälinetyyppien luetteloon lisätään **ApplePay** **Tuetut maksuvälinetyypit** -kentässä. Erottele maksuvälinetyypit toisistaan luettelossa puolipisteen (;) avulla.

Adyen-yhdistimen yhdistävä käsittelijä sieppaa lompakon korttityypit, joita Apple Pay käyttää kassapäätteessä.

### <a name="configure-content-security-policies-in-site-builder"></a>Sisällön suojauskäytäntöjen määrittäminen sivustonmuodostimessa

Ennen osien tai sivujen määrittämistä Apple Payn avulla on varmistettava, että sivuston sisällön suojauskäytännöt on määritetty Commercen sivustonmuodostimessa sivustoa varten.

Määritä sisällön suojauskäytännöt sivustonmuodostimessa alla olevien ohjeiden mukaan.

1. Siirry kohtaan **Sivuston asetukset \> Laajennukset**.
1. Valitse **Sisällön suojauskäytäntö** -välilehdessä **Lisää**, jos haluat lisätä osoitteen `https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js` sisältävän rivin **child-src**-, **connect-src**-, **frame-src**-, **img-src**-, **script-src**- ja **style-src**-osiin.
1. Kun olet valmis, ota muutokset käyttöön valitsemalla **Tallenna ja julkaise**.

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>Apple Payn määrittäminen kassan maksuvaihtoehdoksi

Jos haluat määrittää Apple Payn kassan maksuvaihtoehdoksi sivustossa (muu kuin pikatoiminto) kassasivulla, noudata alla olevia ohjeita.

1. Valitse sivustonmuodostimessa **Osat** ja valitse sitten sivuston kassaosa.
1. Valitse **Muokkaa**.
1. Valitse **Kassalle-osan säilö**-paikassa kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Apple Pay** -moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**.
1. Valitse **Lopeta muokkaus** tallentaaksesi osan ja valitse sitten **Julkaise** julkaistaksesi sen.

**Apple Pay** -moduulin asetukset on muodostettu moduuliin. Niiden avulla muodostetaan yhteys määritettyyn Dynamics 365 Payment Connector Apple Payta varten -yhdistimeen, joka on määritetty Commerce headquartersin verkkokanavaa varten.

### <a name="apple-pay-payment-behavior"></a>Apple Payn maksutoiminta

**Apple Pay** -maksupainike näkyy vain tuetuissa Apple Pay -laitteissa (iPhone- ja iPad-laitteissa sekä Safari-selaimissa, jotka tukevat Apple Payta). Jos käyttäjä ei käytä mitään näistä laitteista, **Apple Pay** -maksupainike on piilotettu näkymässä.

Kun käyttäjä valitsee **Apple Pay** -maksupainikkeen, näkyviin tulee **Apple Pay** -valintaikkuna. Siinä käyttäjä voi tehdä todennuksen Apple Pay -laitteessa tai -selaimessa. **Apple Pay** -valintaikkunassa näkyy yhteenveto tilaussummasta ja maksumenetelmästä, jonka käyttäjä on määrittänyt Apple-lompakolle. Käyttäjä voi tarkistaa nämä tiedot ja suorittaa maksun loppuun valitsemalla **Maksa**. Kun maksu on valmis, käyttäjä ohjataan **Tilaus on valmis** -sivuston sivulle, jossa näkyy valmiin tapahtuman yksityiskohtainen tilausyhteenveto.

## <a name="additional-resources"></a>Lisäresurssit

[Maksut – usein kysytyt kysymykset](payments-retail.md)

[Kassamoduuli](../add-checkout-module.md)

[Maksumoduuli](../payment-module.md)
