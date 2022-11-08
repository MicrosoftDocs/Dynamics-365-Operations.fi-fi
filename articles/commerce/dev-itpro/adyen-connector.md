---
title: Dynamics 365 Payment Connector Adyenia varten -yleiskatsaus
description: Tässä artikkelissa on Microsoft Dynamics 365 Payment Connector for Adyen -yhdistimen yleiskatsaus.
author: rassadi
ms.date: 10/27/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 931fc69cda8daa2e06b6f1155fbf0369fd2bca55
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728305"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>Dynamics 365 Payment Connector Adyenia varten -yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on Microsoft Dynamics 365 Payment Connector for Adyen -yhdistimen yleiskatsaus sekä kattava luettelo sen tukemista ominaisuuksista ja toiminnoista. Asiaan liittyvät artikkelit kattavat Adyeniin rekisteröitymisen, yhdistimen määrittämisen, usein kysytyt kysymykset ja ohjeet joidenkin yleisimpien ongelmien vianmääritykseen.

## <a name="key-terms"></a>Tärkeimmät termit

| Termi | Kuvaus |
|---|---|
| Maksuyhdistin | Laajennus, joka helpottaa viestintää Microsoft Dynamics 365 Commercen (ja siihen liittyviä osien) ja maksupalvelun välillä. Tässä artikkelissa kuvattu yhdistin toteutettiin vakiomaksuohjelmiston kehityspaketin (SDK) avulla. |
| Kortti paikalla | Viittaa maksutapahtumiin, jotka tehtiin fyysisellä kortilla. Käytetään Dynamics 365 Point of Sale -järjestelmän maksupäätteen yhdistimisessä. |
| Kortti ei ole paikalla | Viittaa maksutapahtumiin, joita ei tehty fyysisellä kortilla, esimerkiksi verkkokaupan tai puhelinkeskuksen skenaarioissa. Näissä skenaarioissa maksuun liittyvät tiedot syötetään manuaalisesti joko verkkokauppasivustolla, puhelukeskuksen työnkulussa tai POS- tai maksupäätteellä. |

## <a name="supported-features-functionality-versions-and-terminals"></a>Tuetut ominaisuudet, toiminnot, versiot ja päätteet

Käyttövalmis Dynamics 365 Payment Connector for Adyen käyttää vakiomuotoista maksujen SDK-pakettia. Tästä johtuen sillä ei ole erityisiä ominaisuuksia, jotka eivät olisi myös muiden maksuliittimien käytettävissä.

### <a name="supported-versions"></a>Tuetut versiot

#### <a name="microsoft-dynamics-365-supported-versions"></a>Tuetut Microsoft Dynamics 365 -versiot
Ensimmäisen osapuolen käyttövalmista Dynamics 365 Payment Connector for Adyen -yhdistintä tuetaan Microsoft Dynamics 365 Finance -versiossa 8.1.3 (tammikuu 2019) tai sitä uudemmassa sekä Microsoft Dynamics 365 Retail -versiossa 8.1.3 tai sitä uudemmassa. Kolmannet osapuolet voivat kuitenkin kehittää Adyenia varten muita maksuyhdistimiä vanhemmille Microsoft Dynamics 365 -versioille.

#### <a name="supported-adyen-firmware-versions"></a>Tuetut Adyen-laiteohjelmistoversiot

Alla olevassa luettelossa kuvataan kullekin Microsoft Dynamics 365 Retail POS -versiolle tuetut Adyen-laiteohjelmistoversion vähimmäis- ja enimmäisversiot.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Dynamics 365 Retail POS -versio 10.0.25
| Adyen-laiteohjelmiston vähimmäisversio | Adyen-laiteohjelmiston enimmäisversio |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Dynamics 365 Retail POS -versio 10.0.26
| Adyen-laiteohjelmiston vähimmäisversio | Adyen-laiteohjelmiston enimmäisversio |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Dynamics 365 Retail POS -versio 10.0.27
| Adyen-laiteohjelmiston vähimmäisversio | Adyen-laiteohjelmiston enimmäisversio |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Dynamics 365 Retail POS -versio 10.0.28
| Adyen-laiteohjelmiston vähimmäisversio | Adyen-laiteohjelmiston enimmäisversio |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Dynamics 365 Retail POS -versio 10.0.29
| Adyen-laiteohjelmiston vähimmäisversio | Adyen-laiteohjelmiston enimmäisversio |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Dynamics 365 Retail POS -versio 10.0.30
| Adyen-laiteohjelmiston vähimmäisversio | Adyen-laiteohjelmiston enimmäisversio |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Adyen voi julkaista aliversiopäivityksiä sen jälkeen, kun Microsoft on testannut pääversiota. Samaan pääversioon voidaan tehdä aliversiopäivityksiä, kunhan pääversiota tuetaan. Nämä päivitykset ovat tavallisesti erittäin pieniä korjauksia eivätkä ne edellytä täyttä uudelleentestausta, jos samaa pääversiota testattiin jo aiemmin. Päivitysten ei tulisi ylittää dokumentaatiossa mainittua Adyen-laiteohjelmiston enimmäisversiota. 
>
> Adyen-laiteohjelmistoversiota 53 vanhemmasta versiosta siirtyminen versioon 53 edellyttää POS KB **4577957** -korjauksen Commercen kuukausittaisille päivityksille, versiot 10.0.11–10.0.14. Jos jokin näistä versioista on käytössä ilman hotfix-korjausta, maksupäätteen jälkipäivitys sallii maksut vain NFC:n kautta. Hotfix-korjauksen ottaminen käyttöön POS-järjestelmälle ratkaisee tämän ongelman. Jos POS-versio on vanhempi kuin versio 10.0.11, lähetä tukipyyntö, jossa ilmoitetaan, että KB **4577957** tarvitaan käytöstä poistetulle MPOS-järjestelmälle.
> 
> Adyen-laiteohjelmistoversioissa 59p7–62p9 **lahjakortin lunastuksen** operaatio pyytää syöttämään PIN-koodin kahdesti, jos lahjakortti syötetään manuaalisesti. Tätä ongelmaa ei esiinny, kun lahjakortti luetaan. Adyen tutkii asiaa. 

### <a name="supported-payment-terminals"></a>Tuetut maksupäätteet
Dynamics 365 Payment Connector for Adyen varten hyödyntää laiteriippumatonta [Adyen-maksupäätteiden ohjelmointirajapintaa](https://www.adyen.com/blog/introducing-the-terminal-api). Se tukee kaikkia maksupäätteitä, joita tämä ohjelmointirajapinta (API) tukee. Kattava luettelo tuetuista maksupäätteistä on [Adyen POS -päätteet](https://www.adyen.com/pos-payments/terminals) -sivulla.

### <a name="supported-payment-instruments"></a>Tuetut maksutavat

#### <a name="supported-debit-and-credit-cards"></a>Tuetut pankki- ja luottokortit

| Tuotemerkki | Muuttuja | Kortti paikalla | Verkkokauppa | Puhelinkeskus |
|---|---|:-:|:-:|:-:|
| MasterCard | Luotto | ✔ | ✔ | ✔ |
| MasterCard | Debit | ✔ | ✔ | ✔ |
| MasterCard | Alpha Bank -bonus | ✔ | ✔ | ✔ |
| MasterCard | Apple Pay | ✔ |  |  |
| MasterCard | Samsung Pay | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Maestro Samsung Pay | ✔ |  |  |
| MasterCard | Maestro UK | ✔ | ✔ | ✔ |
| VISA | Luotto | ✔ | ✔ | ✔ |
| VISA | Debit | ✔ | ✔ | ✔ |
| VISA | Alpha Bank -bonus | ✔ | ✔ | ✔ |
| VISA | Android Pay | ✔ |  |  |
| VISA | Apple Pay | ✔ |  |  |
| VISA | Samsung Pay | ✔ |  |  |
| VISA | VISA Checkout | ✔ | ✔ | ✔ |
| VISA | VISA Dankort | ✔ | ✔ | ✔ |
| VISA | VISA Hipotecario | ✔ | ✔ | ✔ |
| VISA | VISA Aravia -kortti | ✔ | ✔ | ✔ |
| AMEX | Luotto | ✔ | ✔ | ✔ |
| AMEX | Debit | ✔ | ✔ | ✔ |
| AMEX | Android Pay | ✔ |  |  |
| AMEX | Apple Pay | ✔ |  |  |
| AMEX | Samsung Pay | ✔ |  |  |
| AMEX | AMEX Commercial | ✔ | ✔ | ✔ |
| AMEX | AMEX Consumer | ✔ | ✔ | ✔ |
| AMEX | AMEX Corporate | ✔ | ✔ | ✔ |
| AMEX | AMEX Small Business | ✔ | ✔ | ✔ |
| Discover | Vakio | ✔ | ✔ | ✔ |
| Discover | Android Pay | ✔ |  |  |
| Discover | Apple Pay | ✔ |  |  |
| Discover | Samsung Pay | ✔ |  |  |
| Diners   | Vakio | ✔ | ✔ | ✔ |
| Dineromail | Vakio | ✔ | ✔ | ✔ |
| JCB | Vakio | ✔ | ✔ | ✔ |
| Union Pay\* | Vakio | ✔ |  |  |
| Interac Debit\* | Vakio | ✔ |  |  |

\*Adyen ei tarjoa toistuvia Interac- ja Union Pay -korttitunnuksia, joten niitä ei voida tukea ilman korttia tehdyille maksutapahtumille.

#### <a name="supported-gift-cards"></a>Tuetut lahjakortit
| Skenaario | Kortti paikalla | Kortti ei ole paikalla |
|---|:-:|---|
| Givex | ✔ | ✔ |
| SVS | ✔ | ✔ |

Sinun on suoritettava lisätoimia ennen kuin voit tukea näitä ulkoisia lahjakorttimalleja Dynamics 365 Payment Connector for Adyen -yhdistimen kautta. Lisätietoja on kohdassa [Ulkoisten lahjakorttien tuki](/dynamics365/unified-operations/retail/dev-itpro/gift-card).

#### <a name="supported-wallets"></a>Tuetut lompakot

| Skenaario | Kortti paikalla | Kortti ei ole paikalla |
|---|---|---|
| Alipay | Tuki lisätään tulevissa versioissa. | En |
| WeChat | Tuki lisätään tulevissa versioissa. | En |

#### <a name="supported-card-present-input-methods"></a>Fyysisten korttien lukutavat
| Lukutapa | Tuettu | Muistiinpanot |
|---|:-:|---|
| Syöttämällä kortti | ✔ | |
| Lue kortti | ✔ | |
| Napauttamalla | ✔ | |
| Manuaalinen syöttäminen POS-käyttöliittymän kautta. |  | Ei tueta tällä hetkellä |
| Manuaalinen syöttäminen maksupäätteen kautta. | ✔ | Tukee luotto-, debit- ja lahjakorttien manuaalista syöttämistä PIN-koodilla. | 


#### <a name="supported-card-present-countries"></a>Maat, joissa kortilla tehtyjä maksuja tuetaan

Alla on luettelo maista, joissa Commerce-komponentit ovat käytettävissä ja joissa Adyen tukee fyysisillä korteilla tehtyjä maksuja. Katso Commercen ajankohtainen kansainvälinen saatavuus [Kansainvälinen saatavuus -sivulta](/dynamics365/get-started/availability).

| Maa tai alue | Tuettu |
| --- | :-: |
| Australia | ✔ |
| Itävalta | ✔ |
| Belgia | ✔ |
| Kanada | ✔ |
| Tšekin tasavalta | ✔ |
| Tanska | ✔ |
| Viro | ✔ |
| Suomi | ✔ |
| Ranska | ✔ |
| Saksa | ✔ |
| Hongkong, Kiinan erityishallintoalue | ✔ |
| Unkari | ✔ |
| Islanti | ✔ |
| Irlanti | ✔ |
| Italia | ✔ |
| Japani | Tuleva versio |
| Latvia | ✔ |
| Liettua | ✔ |
| Malesia | ✔ |
| Alankomaat | ✔ |
| Uusi-Seelanti | ✔ |
| Norja | ✔ |
| Puola | ✔ |
| Singapore | ✔ |
| Sveitsi | ✔ |
| Espanja | ✔ |
| Ruotsi | ✔ |
| Sveitsi | ✔ |
| Yhdistynyt kuningaskunta | ✔ |
| Yhdysvallat | ✔ |
| Brasilia | Tuleva versio |

#### <a name="supported-card-not-present-countries"></a>Maat, joissa tuetaan maksuja ilman korttia

Adyen tukee ilman kortteja tehtyjä maksutapahtumia seuraavissa maissa. [Ota yhteyttä Adyeniin](https://www.adyen.com/contact/sales) saadaksesi lisätietoja tuesta tietyn maan osalta. Katso Commercen ajankohtainen kansainvälinen saatavuus [Kansainvälinen saatavuus -sivulta](/dynamics365/get-started/availability).

| Maa tai alue | 
| --- |
| Argentiina |
| Armenia |
| Australia |
| Itävalta |
| Bahrain |
| Belgia |
| Brasilia |
| Bulgaria |
| Kanada |
| Chile |
| Kiina |
| Kolumbia |
| Kroatia |
| Kypros |
| Tšekin tasavalta  |
| Tanska |
| Egypti |
| Viro |
| Suomi |
| Ranska |
| Georgia |
| Saksa |
| Gibraltar |
| Kreikka |
| Guernsey |
| Hongkong, Kiinan erityishallintoalue |
| Unkari |
| Islanti |
| Intia |
| Indonesia |
| Irlanti |
| Mansaari |
| Israel |
| Italia |
| Japani |
| Jersey |
| Korea |
| Kuwait |
| Latvia |
| Liettua |
| Luxemburg |
| Malesia |
| Malta |
| Meksiko |
| Marokko |
| Alankomaat |
| Uusi-Seelanti |
| Norja |
| Peru |
| Puola |
| Portugali |
| Qatar |
| Romania |
| Saudi-Arabia |
| Serbia |
| Singapore |
| Slovakia |
| Slovenia |
| Etelä-Afrikka |
| Espanja |
| Ruotsi |
| Sveitsi |
| Taiwan |
| Tansania |
| Thaimaa |
| Turkki |
| Yhdistyneet arabiemiirikunnat |
| Yhdistynyt kuningaskunta |
| Yhdysvallat, mukaan lukien Puerto Rico  |

#### <a name="supported-dynamics-365-payment-features"></a>Tuetut Dynamics 365 -maksuominaisuudet

Seuraavassa taulukossa on kuvattu ominaisuudet, Dynamics 365 Payment Connector for Adyen tukee. Näissä ominaisuuksissa käytetään parannuksia, jotka julkaistiin maksujen SDK-paketissa ja joissakin komponenteissa joulukuussa 2018. Ne eivät koske yksinomaan Dynamics 365 Payment Connector for Adyen -yhdistintä. Katso lisätietoja näiden parannusten ottamiseksi käyttöön muille maksuyhdistimille kohdasta [Kattavan maksun integroinnin luominen maksupäätteelle](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension).

| Skenaario | Kortti paikalla | Kortti ei ole paikalla |
|---|:-:|:-:|
| [Lahjakortin saldon lunastaminen](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [Kaksinkertaisten maksujen estäminen](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| Kaikkikanavainen tokenisointi | ✔ | ✔ |
| Linkitetyt hyvitykset | ✔<br>(Versiosta 10.0.1 alkaen) | ✔<br>(Versiosta 10.0.1 alkaen) |
| [Verkkomaksujen tallentaminen](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(Versiosta 10.0.2 alkaen) | 
| [Ulkoiset lahjakortit puhelinkeskukselle ja verkkokaupalle](./gift-card.md) | ✔<br>(Versiosta 10.0.10 alkaen) | 
| [SCA-maksujen uudelleenohjaus](../adyen_redirect.md) | | ✔<br>(Versiosta 10.0.12 alkaen) |
| [Erilliset maksupäätteet ja kehotteet tulostinta ja käteislaatikkoa varten](../pos-multi-hws.md) | ✔<br>(Versiosta 10.0.12 alkaen) | |
| [SDK-tason tuki palvelumaksun antamiselle Adyen-yhdistimen kautta](tipping.md) | ✔<br>(Versiosta 10.0.14 alkaen) | |
| [Tilauslaskutuksen lisäysperusteinen tietojen tallennus](incremental-capture.md) |  | ✔<br>(Versiosta 10.0.18 alkaen) |
| [Lompakkomaksut](../wallets.md) |  | ✔<br>(Versiosta 10.0.20 alkaen) |
| [Google Pay ja Adyen](google-pay-adyen.md) |  | ✔<br>(Versiosta 10.0.27 alkaen) |

## <a name="next-steps"></a>Seuraavat vaiheet

Lisätietoja Dynamics 365 Payment Connector for Adyen -yhdistämistä varten rekisteröitymisestä ja sen määrittämisestä on kohdassa [Dynamics 365 Payment Connector Adyenia varten -määritys](adyen-connector-setup.md).

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Payment Connector Adyenia varten -määritys](adyen-connector-setup.md)

[Dynamics 365 Payment Connector Adyenia varten -usein kysytyt kysymykset](adyen-connector-faq.md)

[Dynamics 365 Payment Connector Adyenia varten -vianmääritys](adyen-connector-troubleshoot.md)

[Maksut – usein kysytyt kysymykset](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
