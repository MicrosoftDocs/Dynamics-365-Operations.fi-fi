---
title: Erilliset maksupäätteet ja kehotteet tulostinta ja käteislaatikkoa varten
description: Tässä ohjeaiheessa on tietoja siitä, miten voit määrittää erillisen maksupäätteen ja pyytää käyttäjää valitsemaan kassan ja kuittitulostimen.
author: rubendel
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: ad75430c606f959b17c887531fb62bd37caec624
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804304"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a>Erilliset maksupäätteet ja kehotteet tulostinta ja käteislaatikkoa varten

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja siitä, miten voit määrittää erillisen maksupäätteen ja pyytää käyttäjää valitsemaan kassan ja kuittitulostimen.

## <a name="overview"></a>Yleiskuvaus

Nykyaikaiset jälleenmyyjät etsivät tapoja tehostaa myymälässä tapahtuvaa kassakokemusta. Viimeaikaiset suuntaukset kohti paperitonta kassaa sähköisten maksujen kautta ei vain auta tekemään ostokokemuksesta sujuvampaa, mutta myös vähentää tarvetta pitää täydellinen oheislaitteiden saatavuutta jokaiselle myymälälle.

Microsoft Dynamics 365 Commerce tukee näitä trendejä mahdollistaen tilanteen, jossa myyntipisteen (POS) laitteelle on määritetty koko ajan oma maksupääte, mutta sillä ei ole omaa kuittitulostinta tai kassalaatikkoa. Kun osakkuusyritysten on tulostettava vastaanotto tai suoritettava käteismaksu, heitä kehotetaan valitsemaan laiteasema, jossa kyseiset laitteet on konfiguroitu.

## <a name="key-terms"></a>Tärkeimmät termit

| Kausi | kuvaus |
|---|---|
| Rekisteröinti | Yksikkö, jota käytetään POS-rekisterin esiintymän konfiguroinnissa. |
| Laite | POS-rekisterin fyysisen esiintymän ja sille määritetyn modernin POS-sovelluksen esitys. |
| Varattu laiteasema | Laiteaseman liiketoimintalogiikka, joka muodostetaan Modern POS Windowsille- ja Modern POS Androidille -sovelluksiin. |
| Laatikkopotku (d/k)-portti | Perinteinen tapa yhdistää käteislaatikko kuittitulostimeen. |
| Verkon oheislaitteet | Sisäänrakennettu tuki verkkopohjaisille maksupäätteille, kuittitulostimille ja kassalaatikoille. |

## <a name="supported-pos-clients-and-devices"></a>Tuetut POS-asiakkaat ja -laitteet

Tässä ohjeaiheessa kuvatut toiminnot ovat tuettuja modernissa POS for Windows -sovelluksessa ja Modern POS for Android -asiakasohjelmissa.

Tämä toiminto tukee verkkopohjaisia maksupäätteitä ja kuittitulostimia. Voit antaa kassalaatikon tuen liittämällä kassalaatikon verkkovastaanottotulostimeen d/k-portin kautta.

Tämän toiminnon valmiin tuen tarjoaa [Dynamics 365 -maksuliitin Adyen-palvelua varten](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3). Muita maksuliittimiä saatetaan kuitenkin tukea Commerce Software Development Kitin (SDK) kautta. Tuetut kuittitulostimet ovat verkkopohjaisia kuittitulostimia Star Micronicsilta ja Epsonilta.

Määrittääksesi Star Micronics -kuittitulostimet, käytä Star Micronics Printer Utilityä määrittämään laitteen niin, että sitä voidaan käyttää verkon kautta. Tämä apuohjelma sisältää myös laitteen IP-osoitteen.

Voit määrittää Epson-kuittitulostimet käyttämällä Epson ePOS-Print -apuohjelmaa, joka määrittää laitteen käyttämään verkko protokollia.

Lisätietoja verkon oheislaitteiden määrittämisestä on ohjeaiheessa [Verkon oheislaitteiden tuen yleiskatsaus](https://go.microsoft.com/fwlink/?linkid=2129965).

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a>Aseta erillinen maksupääte ja kehote tulostinta ja käteislaatikkoa varten

### <a name="set-up-hardware-profiles"></a>Laiteprofiilien asetukset

Sinulla on oltava kahdentyyppisiä laitteisto profiileja. Ensimmäinen on liitetty rekisteriin. Toinen liitetään laiteasemaan myymälätasolla, ja sitä käytetään loogisesti verkon kuittitulostimien ja kassalaatikoiden ryhmittelemiseen.

#### <a name="set-up-a-hardware-profile-for-the-register"></a>Laitteistoprofiilin määrittäminen rekisteriä varten

Voit määrittää rekisteriin määritetyn laitteistoprofiilin noudattamalla seuraavia ohjeita.

1. Etsi Dynamics 365 Commercessa **Laitteistoprofiili**.
2. Valitse **Uusi**.
3. Määritä laitteistoprofiilin numero ja kirjoita sitten kuvaus. Tämä laitteistoprofiili liitetään itse rekisteriin. Siksi kuvaus, kuten **Liitetty varaversiolla** riittää.
4. Määritä eri laitetyyppien pikavälilehdissä seuraavat laitetyypit.

    | Laite | Laji | Laitteen nimi | Lisätiedot |
    |---|---|---|---|
    | Tulostin | Varaversio | *Mikä tahansa* | Laitteistonimen kirjankoolla on merkitystä. **Kuittiprofiilin tunnuksen** tulee olla sama kuin sen **kuittiprofiilin tunnus**, joka on liitetty verkkotulostimeen, joka on määritetty laiteprofiilissa kanavatasolla määritettynä. |
    | Kassa | Varaversio | *Mikä tahansa* | Laitteistonimen kirjankoolla on merkitystä. Valitse **Käytä jaettua vuoroa** -asetukseksi **Kyllä**. |
    | EFT-palvelu | Adyen | Ei käytettävissä | Lisätietoja valmiin Adyen-maksuyhdistimen asentamisesta on kohdassa [Dynamics 365 -maksuyhdistin Adyenille](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3). Muita maksuliittimiä voidaan tukea [Commerce Software Development Kitin (SDK)](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/end-to-end-payment-extension) kautta. |
    | PIN-näppäimistö | Verkko | **MicrosoftAdyenDeviceV001** | Ei mitään. |

5. Etsi Dynamics 365 Commerce -ohjelmassa **Rekisterit**.
6. Valitse rekisteri valitsemalla rekisterinumero ja valitse sitten **Muokkaa**.
7. Määritä juuri luomasi laitteistoprofiili rekisteriin, jossa on käytettävä erityistä maksupäätettä. Tähän rekisteriin yhdistetylle laitteelle on käytettävä joko Modern POS Windowsille tai Modern POS Androidille -sovellusta.
8. Valitse **Tallenna**.
9. Valitse toimintoruudun **Rekisterit**-välilehdessä **Määritä IP-osoittet**.
10. Määritä **PIN-näppäimistö**-pikavälilehdessä maksupäätteen IP-osoite. Lisätietoja maksupäätteen IP-osoitteen hankkimisesta Adyen-liittimen avulla on kohdassa [Dynamics 365 -maksuyhdistin Adyenille](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3).
11. Valitse **Tallenna**.

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a>Laiteprofiilin määrittäminen kuittitulostinta ja kassalaatikkoa varten

Voit määrittää verkon kuittitulostimen ja kassalaatikon ryhmittelemiseen käytettävän laitteistoprofiilin seuraavasti.

1. Etsi Dynamics 365 Commercessa **Laitteistoprofiili**.
2. Valitse **Uusi**.
3. Määritä laitteistoprofiilin numero ja kirjoita sitten kuvaus. Tätä laitteistoprofiilia käytetään kuittitulostimen ja kassalaatikon ryhmittelemiseen. Siksi kuvaus, kuten **verkkotulostin ja kassalaatikko** riittää.
4. Määritä eri laitetyyppien pikavälilehdissä seuraavat laitetyypit.

    | Laite | Laji | kuvaus | Lisätiedot |
    |---|---|---|---|
    | Tulostin | Verkko | **Epson** tai **Star** | Laitteistonimen kirjankoolla on merkitystä. **Kuittiprofiilin tunnuksen** tulee olla sama kuin sen **kuittiprofiilin tunnus**, joka on liitetty tulostimeen, joka on määritetty rekisteriin. |
    | Kassa | Verkko | **Epson** tai **Star** | Laitteistonimen kirjankoolla on merkitystä. valitse **Käytä jaettua vuoroa** -asetukseksi **Kyllä**. |

5. Valitse **Tallenna**.

### <a name="set-up-hardware-stations"></a>Laiteasemien määrittäminen

Sinulla on oltava kaksi laiteasemaa. Ensimmäinen yhdistetään rekisteriin. Toinen valitaan tarvittaessa, kun kuitti täytyy tulostaa tai kassalaatikko on avattava.

#### <a name="register-a-hardware-station"></a>Laiteaseman rekisteröiminen

1. Etsi Dynamics 365 Commerce -kohdassa **Kaikki myymälät**.
2. Valitse myymälä valitsemalla sen **Vähittäismyyntikanavan tunnus** -arvot ja valitse sitten **Muokkaa**.
3. Valitse **Laiteasemat**-pikavälilehdessä **Lisää**.
4. Määritä **Laiteaseman tyyppi** -kenttään **Omistettu**.
5. Kirjoita kuvaus, mutta älä määritä muita arvoja tälle laiteasemalle. Tätä laiteasemaa käytetään aina rekisteriin. 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a>Laiteaseman määrittäminen kuittitulostinta ja kassalaatikkoa varten

1. Etsi Dynamics 365 Commerce -kohdassa **Kaikki myymälät**.
2. Valitse myymälä valitsemalla sen **Vähittäismyyntikanavan tunnus** -arvot ja valitse sitten **Muokkaa**.
3. Valitse **Laiteasemat**-pikavälilehdessä **Lisää**.
4. Määritä **Laiteaseman tyyppi** -kenttään **Omistettu**.
5. Anna kuvaus. Tätä laiteasemaa käytetään kuittitulostimelle ja kassalaatikolle.
6. Valitse **Laitteistoprofiili** -kentässä laiteprofiili, jonka olet luonut aiemmin kuittitulostimelle ja kassalaatikkoon.
7. Valitse **Tallenna**.
8. Kun kuittitulostimen ja kassalaatikon laite on edelleen valittuna, valitse **Määritä IP-osoitteet**.
9. Hanki tulostimen IP-osoite ja kirjoita se sekä kuittitulostimen että kassalaatikon IP-osoitteeksi.
10. Valitse **Tallenna**
11. Hae **Jakelusuunnitelmat**.
12. Valitse **1090**-jakeluaikataulu ja valitse sitten **Suorita nyt**.
13. Valitse **1070**-jakeluaikataulu ja valitse sitten **Suorita nyt**.

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a>Järjestelmän määrittäminen pyytämään kuittitulostinta ja kassalaatikon valintaa tarpeen mukaan

1. Tuettu POS-asiakasohjelma sulkee nykyisen vuoron, jos vuoro on auki.
2. Kirjaudu sisään ja valitse sitten **Muut kuin kassalaatikon toiminnot**.
3. **Laiteasemien hallinta** -toiminnon avulla voit ottaa laitteistoaseman käyttöön.
4. Valitse laiteasema, jonka loit rekisteröitymistä varten aktivoidaksesi sen.
5. Kirjaudu ulos myyntipisteestä, kirjaudu takaisin sisään ja avaa vuoro.

Laitteistoprofiiliin liitetty maksupääte on nyt aina aktiivinen, ja sinulta kysytään, onko kuittitulostin tai kassalaatikko pakollinen.

Monet kauppiaat, jotka pyysivät tätä ominaisuutta ovat kiinnostuneita vähentämään jätettä tarjoamalla sähköpostikuitteja ja kannustavat sähköisiin maksuihin. Myyntipisteen kokoonpanosta riippuen myymäläkumppaneita kehotetaan valitsemaan kuittitulostin tai kassalaatikko vain silloin, kun asiakas haluaa fyysisen kuitin tai haluaa maksaa käteisellä.

Myymäläkumppaneita kehotetaan valitsemaan laiteasema vain kerran tapahtumaa kohden, paitsi jos kuitti on tulostettava ja käteistä käytetään maksamiseen, mutta alun perin valittu laitteistoprofiili ei sisällä molempia laitteita. Tällöin myymälästä pyydetään uudelleen valitsemaan laiteasema, jota voidaan käyttää tapahtuman suorittamiseen.

## <a name="related-articles"></a>Liittyvät artikkelit

- [POS Hybrid -sovelluksen määrittäminen Android- ja iOS-laitteessa](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp)
- [Dynamics 365 -maksuyhdistin Adyenia varten](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)
- [Yleistä verkon oheistuesta](https://go.microsoft.com/fwlink/?linkid=2129965)


[!INCLUDE[footer-include](../includes/footer-banner.md)]