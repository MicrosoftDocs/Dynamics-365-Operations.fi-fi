---
title: Dynamics 365 Commercen sähköisen kaupankäynnin lokalisointiopas
description: Tässä aiheessa kuvataan, kuinka Microsoft Dynamics 365 Commercem sähköinen kauppasivusto voidaan lokalisoida eri kielille ja määrittää sivusto niin, että se tukee useita kanavia.
author: bicyclingfool
ms.date: 04/29/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1e9d91036ceeb9161dc8ee903532b2cf3ca435e2
ms.sourcegitcommit: 26c726bd0b00935e3d2c31fdc5a3b2ae03a8a2b0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661524"
---
# <a name="dynamics-365-commerce-e-commerce-localization-guide"></a>Dynamics 365 Commercen sähköisen kaupankäynnin lokalisointiopas

[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan, kuinka Microsoft Dynamics 365 Commercen sähköinen kaupankäyntisivusto voidaan lokalisoida useille kielille ja määrittää sivusto niin, että se tukee useita kanavia. Lisäksi se sisältää prosessiin liittyvät käsitteet ja termit.

Dynamics 365 Commercen sähköisen kaupan toiminnot on suunniteltu siten, että ne mahdollistavat verkkokokemuksia, jotka voidaan räätälöidä tiettyihin maihin/alueisiin ja kieliin, mutta joiden avulla malleja, sivuja, sisältöä ja mediaa voidaan käyttää mahdollisimman paljon uudelleen. Voit myös luoda perussivuston ja laajentaa sen jälkeen uusille markkina-alueille lisäämällä tuen lisämaille/-alueille ja -kielille ajan mittaan.

## <a name="definitions"></a>Määritelmät

**Kielialue, kielialuetunnus**: Kielialue (jota kutsutaan myös kielialuetunnukseksi) määrittää maan tai alueen kielen. Esimerkiksi kielialuetunnus "fr-ca" liittyy Kanadan ranskaan.

**Peruskieli**: Kieli, jota käytät sivuston sisällön kehittämisestä ennen vientiä lokalisointia varten.

**Kanava, online-myymälä**: Kanava (tunnetaan myös verkkokauppana) määrittää maksutavat, hintaryhmät, tuotehierarkiat, valikoimat ja tuotteet verkkokauppamyymälässä.

## <a name="concepts"></a>Käsitteet

### <a name="url-driven-experience"></a>URL-pohjainen kokemus

Dynamics 365 Commercen sähköisen kaupan sivustot tarjoavat yksilöllisiä markkinoinnin ja lokalisoinnin kokemuksia asiakkaille kanavien ja kielialuetunnisteiden kautta. Kanavat määrittävät markkinan yksilöivät tuotteet, luokat, valuutat ja maksutavat, ja kielialuetunnukset määrittävät, millä kielellä asiakkaat näkevät sisällön. Sähköisen kaupankäynnin sivusto erottelee URL-osoitteiden avulla markkinoidut ja lokalisoidut kokemukset. Näiden yksilöiville kanava- ja kielialuekohtaisille kokemuksille määritetyt sivuston URL-osoitteet määritetään Dynamics 365 Commercen sivuston muodostimessa **Sivuston asetukset \> Kanavat** -sivulla.

Sivustonmuodostajassa URL-osoite on toimialueen ja polun yhdistelmä, joka määrittää kanavan ja kielialuekohtaisen yksilöivän yhdistelmän aloituspisteen. Seuraavassa esimerkissä fiktiivinen verkkokauppa nimeltä Fabrikam Inc. määrittää neljä kanavan ja kielialueen yksilöivaa yhdistelmää ja yhdistää kunkin yhdistelmän yksilöivään URL-osoitteeseen, joka tarjoaa sisältöä asiakkaille.

| Toimialue                     |  Polku      | Kanava       |   Aluekohtaiset asetukset     |
|------------------------|--------|--------------------------------|--------|
| `https://fabrikam.com` | /      | Laajennettu Fabrikam-verkkomyymälä | fi  |
| `https://fabrikam.com` | /es    | Laajennettu Fabrikam-verkkomyymälä | es     |
| `https://fabrikam.ca`  | /      | Contoso-verkkokauppa    | fr-ca  |
| `https://fabrikam.ca`  | /en-ca | Contoso-verkkokauppa    | en-ca  |

#### <a name="domain"></a>Toimialue

Toimialueet määritetään, kun määrität sähköisen kauppasivuston Microsoft Dynamics Lifecycle Services (LCS) -palvelussa. Kun sähköinen kaupankäyntiympäristö on varattu, voit lisätä toimialueita avaamalla palvelupyynnön. Lisätietoja sähköisen kaupankäynnin sivuston toimialueiden määrityksestä on kohdassa [Toimialueet Dynamics 365 Commercessa](domains-commerce.md).

#### <a name="path"></a>Polku

- Polku on merkkijono, joka yhdessä toimialueen kanssa on yhdistetty kanavan ja kielialueen yksilöivään yhdistelmään. Edellisessä esimerkissä polkuna käytettävä merkkijono vastaa sitä kielialuetunnusta, jonne polku on yhdistetty. Voit kuitenkin käyttää toista menetelmää.
- Kanavan ja kielialueen yhdistelmä voidaan määrittää toimialueelle ja tyhjälle polulle ("/"). Edellisessä esimerkissä asiakkaat, jotka vierailevat osoitteessa `https://fabrikam.ca/`, saavat Kanadan markkinoiden tuotteita ja valikoimia Kanadan ranskan kielellä.
- Commercen sivustonmuodostin estää sinua luomasta toimialueen ja polun yhdistelmien kaksoiskappaleita. Voit kuitenkin määrittää kanavan ja kielialueen yhdistelmien kaksoiskappaleet toimialueen ja polun eri yhdistelmään.

#### <a name="channel"></a>Kanava

- Kanavat (tunnetaan myös verkkokauppana) määrittävät maksutavat, hintaryhmät, tuotehierarkiat, valikoimat ja tuotteet verkkokauppamyymälässä.
- Kanavat määritetään, konfiguroidaan ja julkaistaan Dynamics 365 Commerce headquartersissa.
- sivustonmuodostin voi tunnistaa Commerce headquarters -sovelluksessa konfiguroidut online-myymälät, jotka voidaan yhdistää sivustoon.

Lisätietoja kanavista on [Kanavien esittely](channels-overview.md) -kohdan ohjeaiheessa. Lisätietoja online-kanavan määrittämisestä on kohdassa [Online-kanavan määritys](channel-setup-online.md).

#### <a name="locale"></a>Aluekohtaiset asetukset

- Kielialue on varsinainen tunnus, jota käytetään, kun XML Localization Interchange File Format (XLIFF) -tiedostot luovutetaan lokalisointia varten. Kielialueet määritetään ja julkaistaan kullekin Commerce headquarters -kanavalle. Lisätietoja kielien ja kanavien määrittämisestä sivustonmuodostimessa on seuraavassa osassa.
- Sama kielialue voidaan määrittää useaan kanavaan. Näin voidaan tarjota yhteinen kieli usealla eri markkina-alueella.

## <a name="configure-languages-and-channels-for-your-e-commerce-site"></a>Kielien ja kanavien konfiguroiminen sähköisen kaupankäynnin sivustoa varten

Kaikki Dynamics 365 Commercen sähköisen kaupankäynnin sivustot on käyttövalmiina konfiguroitu käyttämään yhtä online-kanavaa ja yhtä kieltä riippumatta siitä, luodaanko Fabrikamin esittelysivusto vai luodaanko uusi sivusto tyhjästä.

Tässä konfiguraatiossa asiakkaat ja liikekumppanit yleensä kehittävät kaikki eri maiden/alueiden ja kielten käyttämät resurssit. Näitä resursseja ovat mallit, sivut, katkelmat, sisältö ja media. Kaikki sivustosisällöt on kehitetty sivustoasi varten valitulla ensimmäisellä kielellä tai jos käytät Fabrikamin demosivustoa, sivuston sisältö kehitetään englanniksi.

![Dynamics 365 Commercen käyttövalmis sähköisen kaupankäynnin sivusto](media/loc-guide-1.png)

> [!NOTE]
> Fabrikamin esittelysivuston voi konfiguroida lisäkieltä varten, jotta sisällön kehitystä voidaan tehdä tällä kielellä. Lisätietoja uuden kielen lisäämisestä sivustoon ja kanavaan on jäljempänä tässä ohjeaiheessa [Määritä sivustolle lisäkieli](#configure-an-additional-language-for-your-site) -kohdassa.

Dynamics 365 Commercen sähköisen kaupankäynnin sivustojen sisällönhallintajärjestelmä (CMS) ja sivumalli on kuitenkin suunniteltu siten, että ne mahdollistavat laajentamisen uusille markkinoille ja kielialueille. Näin ollen voit hallita yhden sähköisen kauppasivuston kautta verkkokaupan resursseja, jotka kattavat useita markkinoita ja kieliä.

![Dynamics 365 Commercen sähköinen kaupankäyntisivusto, joka kattaa useita markkinoita ja kieliä](media/loc-guide-2.png)

### <a name="configure-an-additional-language-for-your-site"></a>Sivuston lisäkielen määrittäminen

Uuden kielen konfiguroinnissa sähköisen kaupankäynnin sivustoa varten on kolme vaihetta.

#### <a name="step-1-add-the-language-to-your-channel-online-store-in-commerce-headquarters"></a>Vaihe 1: Kielen lisääminen kanavaan (online-myymälään) Commerce headquarters -sovelluksessa

1. Siirry Commerce headquarters -sovelluksessa kanavaan, johon haluat lisätä uuden kielen. Näet Commerce headquartersissa määritettyjen kanavien luettelon siirtymällä kohtaan **Retail ja Commerce \> Kanavat \> Verkkokaupat**.
1. Avaa sivustoon yhdistetty verkkomyymälä valitsemalla sen **Vähittäismyyntikanavan tunnus** -arvo. Voit vahvistaa sivustoosi liitetyn online-myymälän avaamalla Commerce sivustonmuodostimen **Kanavat**-sivustoasetussivun ja tarkastelemalla **Kanavat**-sarakkeen verkkokaupan nimeä. 
1. Valitse **Kielet**-pikavälilehdessä **Lisää**. Valitse **Kieli**-kentässä uuden kielen kielialuekoodi. Valitse sitten **Tallenna**.
1. Siirry kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu** ja suorita työ **1070 kanavan määritys**. Kun työ on suoritettu loppuun, voit siirtyä vaiheeseen 2 ja lisätä kielen sivuston kanavaan sivustonmuodostimessa.

![Verkkokaupan Kielet-pikavälilehti Commerce headquartersissa](media/loc-guide-3.png)

#### <a name="step-2-add-the-language-to-a-channel-in-site-builder"></a>Vaihe 2: Kielen lisääminen kanavaan sivustonmuodostimessa

Voit lisätä kielen sivustonmuodostimessa kanavaan noudattamalla seuraavia ohjeita.

1. Avaa Commercen sivustonmuodostimessa sivusto ja avaa sitten **Kanavat**-sivu sivuston asetuksissa.
1. Valitse sen kanavan nimi, johon haluat lisätä kielen.
1. Valitse oikeanpuoleisesta ruudusta **Lisää kielialue**.
1. Valitse **Lisää kielialue** -valintaikkunassa kohdassa **Lisää kielialue** sen kielen kielialue, jonka olet aiemmin lisännyt kanavaan Commerce Headquarters -sovelluksessa.
1. Valitse toimialue ja polku, joita asiakkaat pyytävät sivuston tarkastelemiseen tällä kanavalla ja kielellä.
1. Jos haluat kielen olevan oletuskieli sivustonmuodostimen sivujen ja katkelmien katselua, luomista ja päivittämistä varten, valitse **Käytä laatimiskanavan oletuskielenä** -valintaruutu. 
    > [!NOTE]
    > Tämä asetus vaikuttaa vain sivustonmuodostimeen. Se ei vaikuta asiakkaille julkaistuun sivustokokemukseen.
1. Valitse **OK**.
1. Valitse **Tallenna ja julkaise**.

#### <a name="step-3-localize-your-site-content"></a>Vaihe 3: Sivuston sisällön lokalisoiminen

Kun palaat Commercen sivustonmuodostimen **Sivut**-näkymään, uusi kieli on käytettävissä kanavan ja kielialueen valitsimessa oikeassa yläkulmassa. Voit nyt luoda lokalisoituja versioita peruskielellä tehdyistä sivuista.

Prosessi, jossa voit lokalisoida sivusi ja katkelmasi käsitellään jäljempänä tässä ohjeaiheessa kohdassa [Sähköisen kaupankäynnin sivuston sisällön lokalisoiminen](#localize-e-commerce-site-content).

### <a name="configure-a-new-channel-for-your-site"></a>Uuden kanavan konfiguroiminen sivustoa varten

Dynamics 365 Commercen sähköisen kaupankäynnin sivustoilla voi olla käyttökokemuksia, jotka on määritetty usealla online-kanavalla ja jotka on konfiguroitu Commerce Headquarters -sovelluksessa. Sivustossa käytetään useita kanavia, jotta asiakkaat näkevät yksilöllisen maksutapojen, hintaryhmien, tuotehierarkioiden, valikoimien ja tuotejoukkojen konfigurointi. Kanavaa käytetään yleensä näiden dimensioiden konfiguroinnissa niin, että se sopii yksittäisiin maihin/alueisiin liittyviin kokemuksiin ja tarpeisiin. Tämä on kuitenkin liiketoimintapäätös, jonka asiakas tekee. Se ei ole vaatimus.

Kanavan (online-myymälän) määrittämiseen liittyvät edellytykset ja tehtävät ovat tämän asiakirjan käyttöalueen ulkopuolella. Lisätietoja online-kanavan määrittämisestä Commerce headquarters on kohdassa [Kanavan määritysten perusteet](channels-overview.md#channel-setup-basics). Lisätietoja online-kanavien vaiheista ja vaatimuksista on kohdassa [Online-kanavan määrittäminen](channel-setup-online.md).

Voit lisätä kanavan sivustoon sivustonmuodostimessa noudattamalla seuraavia ohjeita.

1. Siirry Commercen sivustonmuodostustyökalussa kohtaan **Sivuston asetukset \> Kanavat**. 
1. Valitse **Lisää kanava**.
1. Valitse **Lisää kanava** -valintaikkunan **Kanava**-kohdasta kanava, jonka haluat lisätä. 
    > [!NOTE]
    > Voit lisätä vain kanavia, joita ei ole vielä lisätty sivustoon.
1. Valitse kanavan oletuskielialue. Jos lisäät kanavaan uusia kieliä, voit vaihtaa oletuskieleksi jonkin niistä.
1. Määritä toimialue ja polku, joka muodostaa URL-osoitteen, joka toimii kanavan ja kielen yhdistelmän sisällön ja kokemusten tarjoamiseksi.
1. Valitse **OK**.
1. Valitse **Tallenna ja julkaise**.

## <a name="localize-e-commerce-site-content"></a>Sähköisen kaupankäynnin sivuston sisällön lokalisoiminen

### <a name="xliff-basics"></a>XLIFF-perustiedot

XLIFF on toimialan vakiotiedostomuoto, jonka avulla voidaan siirtää lokalisoitavaa sisältöä sisällönhallintatyökalujen välillä. Commercen sivustonmuodostin vie sivun, katkelman ja kuvan metatietojen sisällön XLIFF-tiedostomuodon avulla, jotta se voidaan lokalisoida ja tuoda takaisin.

Microsoft Dynamics -asiakkaat työskentelevät yleensä kolmannen osapuolen lokalisointitoimittajien kanssa (esim. [Translated.com](https://translated.com/welcome)) kääntääkseen XLIFF-tiedostot tarvitsemilleen kielille.

### <a name="localize-assets-in-site-builder"></a>Resurssien lokalisoiminen sivustonmuodostajassa

Seuraavat sähköisen kaupankäynnin sivuston resurssit voi lokalisoida sivustonmuodostimen avulla:

- Sivut
- Katkelmat
- Mediaresurssit
- Moduulit

Kaikki uudet sivut, katkelmat ja mediaresurssit luodaan kanavan ja kielen yhteydessä, jotka ovat valittuna kanava- ja aluepalkista. Tämä kieli on yleensä peruskielesi, jos et ole konfiguroinut muita kieliä tai kanavia. Jos konfiguroit useita kanavia ja kieliä sivustossa, **Kanavat**-sivun kanavan ja kielialuekohtaisten oletusasetusten mukaan määritetään "peruskieli".

Sivujen, katkelmien ja mediaresurssien sisällön lokalisointivaiheet ovat samankaltaisia. Poikkeuksista ja eroista huomautetaan seuraavissa osissa. Moduulisisällön lokalisointivaiheet eroavat kuitenkin toisistaan. Lisätietoja on myöhemmin tässä aiheessa kohdassa [Moduulien lokalisointi](#localize-modules).

#### <a name="step-1-export-an-xliff-file"></a>Vaihe 1: XLIFF-tiedoston vieminen

Voit viedä sivun, katkelman tai kuvan XLIFF-tiedoston sivustonmuodostimessa seuraavasti.

1. Avaa resurssi, jonka peruskielen sisällön haluat viedä, jotta se voidaan lokalisoida.
1. Valitse komentopalkista **Lokalisointi \> Vie XLIFF**.
    > [!NOTE]
    > **Lokalisointi**-vaihtoehto on käytettävissä vain, jos resurssin tilana on **Muokkaus**.

XLIFF-tiedosto nimeltä **\<assetname\>.xlf** ladataan selaimesi latauskansioon. XLIFF-tiedosto koskee vain se resurssia, jota olet lokalisoimassa. XLIFF-tiedosto viedään jokaiselle lokalisoitavalle resurssille.

#### <a name="step-2-localize-the-xliff-file"></a>Vaihe 2: XLIFF-tiedoston lokalisoiminen

Useimmissa tapauksissa käytät lokalisointitoimittajaa XLIFF-tiedostojen kääntämiseen. Jos kuitenkin olet kääntämässä resursseja sisäisesti tai haluat vain testata lokalisointiprosessia, tee XLIFF-tiedostoon seuraavat muutokset:

- Lisää kohdekielimäärite /xliff/file-elementtiin ja määritä arvoksi sen kielen kielialuetunnus, johon olet lokalisoimassa. 
    > [!NOTE]
    > Tämän kielialuetunnuksen on vastattava sivuston asetusten **Kanavat**-sivun kielialuetunnusta.
- Lisää jokaiselle //source-elementille kohde-elementin sisarsolmu, jossa tekstiarvo on lähde-elementin sisällön lokalisoitu versio.

XLIFF-tiedostoja ohjaavat skeematiedot ovat [XLIFF 1.2 -määrityksessä](http://docs.oasis-open.org/xliff/xliff-core/xliff-core.html).

> [!NOTE]
> Jos haluat lokalisoida resurssin useille kielille, sinun on luotava lokalisoitu XLIFF-tiedosto kullekin kielelle.

#### <a name="step-3-import-the-localized-xliff-file"></a>Vaihe 3: Lokalisoidun XLIFF -tiedoston tuominen

Jos haluat tuoda resurssin XLIFF-tiedoston, noudata seuraavia ohjeita.

1. Avaa Commercen sivustonmuodostimessa resurssi, jonka XLIFF-tiedoston haluat tuoda.
1. Valitse oikeasta yläkulmasta kanava- ja kielialuevalitsimesta kanava ja kieli, jota varten tuot lokalisoitua sisältöä.
1. Valitse komentopalkista **Lokalisointi \> Tuo XLIFF**. Selaa sitten valitulle resurssille ja kielelle lokalisoitu XLIFF-tiedosto ja valitse se.

Kun XLIFF-tiedosto on tuotu onnistuneesti, ohjelma luo sivun, katkelman tai resurssin "variantin". Tästä eteenpäin kaikki lokalisoituun varianttiin tehdyt muutokset vaikuttavat vain kyseiseen varianttiin. Ne eivät vaikuta perusresurssiin, joista variantti johdettiin. Samoin perusresurssiin tehdyt muutokset eivät vaikuta lokalisoituun varianttiin. 

Sivujen kohdalla voit kuitenkin tehdä muutoksia varianttien välillä muokkaamalla mallia tai asettelua, johon sivut on sidottu. Samoin katkelmaan tehdyt muutokset vaikuttavat kaikkiin sivuihin, jotka riippuvat tästä variantista.

### <a name="images"></a>Kuvat

Kuvat voidaan hahmontaa sivulla tai moduulivariantissa vain, jos näihin kuviin liittyvät sisällön metatiedot on lokalisoitu. Seuraavat mediaresurssiin määritetyt metatiedot ovat tällä hetkellä lokalisoitavia:

- Vaihtoehtoinen teksti
- Kuvaus
- Nimi

Tällä hetkellä et voi lokalisoida digitaalisten resurssien, kuten kuvan tai videon, binaaridataa. Dynamics 365 Commerce -tuotetiimi työskentelee tällä hetkellä tämän ominaisuuden parissa.

### <a name="localize-modules"></a>Moduulien lokalisointi

Moduulin itsensä osana muodostetut merkkijonot (esimerkiksi "Edellinen" ja "Seuraava" karusellimoduulissa) lokalisoidaan erillään moduulisisällöstä. Lisätietoja on kohdassa [Moduulin lokalisoiminen](e-commerce-extensibility/localize-module.md).

## <a name="additional-resources"></a>Lisäresurssit

[Sivumallisanasto](page-elements-overview.md)

[Kanavienvälinen jakaminen](cross-channel-sharing.md)

[Moduulin lokalisointi](e-commerce-extensibility/localize-module.md)

[Moduulin määritystiedosto](e-commerce-extensibility/module-definition-file.md)

[Lokalisoi Commerce -laajennuksen resurssit ja etikettitiedostot](dev-itpro/extension-resource-localization.md)

[Moduulien globalisoiminen CultureInfoFormatter-luokan avulla](e-commerce-extensibility/globalize-modules.md)

[Sovellusasetukset: Teemat](e-commerce-extensibility/app-settings.md#themes-section)
