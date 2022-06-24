---
title: Asiakastilin maksutavan määrittäminen yritysten välisille sähköisille kaupankäyntisivustoille
description: Tässä artikkelissa kuvataan asiakkaan maksutavan määrittäminen Microsoft Dynamics 365 Commercessä. Siinä kuvataan myös, miten luottorajat vaikuttavat tilimaksujen taltiointiin yritystenvälisillä (B2B) verkkokauppasivustoilla.
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 20af517b9a69f4fb490d4d93ada8bc4063e895dd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878644"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Asiakastilin maksutavan määrittäminen yritysten välisille sähköisille kaupankäyntisivustoille

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan asiakkaan maksutavan määrittäminen Microsoft Dynamics 365 Commercessä. Siinä kuvataan myös, miten luottorajat vaikuttavat tilimaksujen taltiointiin yritystenvälisillä (B2B) verkkokauppasivustoilla.

Vähittäismyyjät voivat hyväksyä useantyyppisiä maksutapoja verkkokauppakanavissaan myymistään tuotteista ja palveluista. Jokainen vähittäismyyjän hyväksymä maksutapa on määritettävä Dynamics 365 Commercessa, kun järjestelmä määritetään. Asiakastilin (tai tilillä olevan) maksutavan on oltava tuettuna B2B-verkkokauppasivustoissa. 

## <a name="prerequisites"></a>Edellytykset

1. Lisää asiakastilin maksutapa Commerce headquarters -sovelluksessa.
2. Liitä asiakastilin maksutapa sähköistä kaupankäyntikanavaa varten.
3. Varmista, että **Salli ennakkomaksu** -ominaisuus on käytössä asiakkaalle Commerce headquarters -sovelluksessa kohdassa **Retail ja Commerce \> Asiakkaat \> Kaikki asiakkaat \> Maksujen oletusasetukset**.

    > [!NOTE]
    > Jos kaikkien asiakkaiden sallitaan käyttää tilimaksumenetelmää, **Salli ennakkomaksu** -ominaisuuden arvoksi **Kyllä** B2B-sivustoon liittyvän kanavan oletusasiakkaalle. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Asiakastilin maksutavan ottaminen käyttöön Commercen sivustonmuodostimessa 

Saat asiakastilin maksutavan otettua käyttöön Commercen sivustonmuodostimessa seuraavasti.

1. Siirry kohtaan **Sivuston asetukset \> Laajennukset**.
1. Määritä **Ota käyttöön asiakastilin maksut** -ominaisuuden arvoksi **Käytössä B2B-asiakkaille**. 
1. Valitse **Tallenna ja julkaise**.

> [!NOTE]
> Uudet sivuston asetukset tulevat voimaan vasta, kun app.settings.json-tiedosto on päivitetty. Lisätietoja on ohjeaiheessa [SDK:n ja moduulikirjaston päivitykset](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Asiakastilin maksutavan ottaminen käyttöön B2B-verkkokauppasivuston uloskuittaussivulla

Saat asiakastilin maksutavan otettua käyttöön B2B-verkkokauppasivuston uloskuittaussivulla seuraavasti.

1. Etsi ja muokkaa Commercen sivustonmuodostintyökalussa uloskuittaussivu tai katkelmassa, joka sisältää B2B-verkkokauppasivuston uloskuittausmoduulin.
1. Valitse **Kassaosiokontti**-paikassa **Lisää moduuli** ja lisää sitten **Asiakastilin maksu** -moduuli.
1. Aseta **Asiakastilin maksu** -moduuli valitsemalla kolme pistettä (**...**) ja valitsemalla sitten **Siirrä ylös** tai **Siirrä alas** tarvittaessa.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Vahvista, että asiakastilin maksutapa on otettu käyttöön ja julkaistu

Voit vahvistaa, että asiakastilin maksutapa on otettu käyttöön ja julkaistu, seuraavasti.

1. Kirjaudu sisään verkkokauppasivustoon.
1. Lisää tuote ostoskoriin.
1. Siirry kassasivulle. Tässä pitäisi näkyä uusi **Asiakastili**-maksutapaa.

## <a name="work-with-credit-limits"></a>Luottorajojen käyttö

Kun asiakastilimaksujen ominaisuudet on otettu käyttöön B2B-sivustolla, organisaatiot haluavat yleensä näyttää tietoja luotto- ja luottorajasaldoista tilausten taltiointiprosessin aikana. Asiakkaan luottoraja määritetään Commerce headquarters -sovelluksen asiakastietueen **Luotonvalvonta** pikavälilehden **Luottoraja**-ominaisuudessa. B2B-skenaarioissa asiakkaan tekemä tilaus pitäisi usein laskuttaa sen organisaation tililtä, johon asiakas kuuluu. Siksi asiakastietueen **Lasku ja toimitus** -pikavälilehden **Laskutustili**-ominaisuudeksi on määritettävä organisaation asiakastilin tunnus. Kun asiakas sitten tekee tilauksen B2B-sivustolla, tilaus laskutetaan organisaatiolta. B2B-sivusto käyttää myös organisaation luottorajaa asiakastietueessa määritetyn luottorajan sijaan.

B2B-sivustolla näkyvä luottorajalaskelma ja -saldo määrittyvät Commerce Headquarters -sovelluksen **Luottorajatyyppi**-ominaisuuden arvosta. Tämän ominaisuuden sijainti vaihtelee sen mukaan, onko hyvitysten **Luotonhallinta**-toiminto käytössä **Ominaisuuksien hallinta** -työtilassa:

- Jos **Luotonhallinta**-toiminto on käytössä, kyseinen ominaisuus sijaitsee **Luottorajat**-pikavälilehden kohdassa **Luotonvalvonta \> Määritys \> Luotonvalvonnan parametrit \> Luotto**. 
- Jos **Luotonhallinta**-toiminto ei ole käytössä, ominaisuus sijaitsee **Luottokelpoisuusluokitus**-pikavälilehden kohdassa **Myyntireskontra \> Määritys \> Myyntireskontran parametrit \> Luottokelpoisuusluokitus**.

**Luottorajan tyyppi** -ominaisuuden tukemat arvot ovat **Ei mitään**, **Saldo**, **Saldo + pakkausluettelo tai tuotetosite** ja **Saldo + kaikki**. Lisätietoja näistä arvoista: [Luottorajan tyypin arvot](/dynamics365/supply-chain/sales-marketing/credit-limits-customers).

> [!NOTE]
> On suositeltavaa määrittää **Luottorajan tyyppi** -ominaisuuden arvoksi **Balance + pakkausluettelo tai tuotetosite**, jotta avoimet myyntitilaukset eivät vaikuta saldon laskentaan. Tällöin asiakkaiden ei tarvitse pelätä, että heidän mahdolliset tuleva tilauksensa vaikuttaisivat heidän kulloiseenkin saldoonsa.

Toinen ominaisuus, joka vaikuttaa tilille tilaamiseen on **Pakollinen luottoraja** -ominaisuus, joka sijaitsee asiakastietueen **Luotonvalvonta**-pikavälilehdessä. Määrittämällä tämän ominaisuuden arvoksi **Kyllä** tietyille asiakkaille, voit pakottaa järjestelmän tarkastamaan heidän luottorajansa, vaikka **Luottorajan tyyppi** -ominaisuuden arvoksi olisi määritetty **Ei mitään** sen määrittämiseksi, että luottorajaa ei pitäisi tarkastaa minkään asiakkaan osalta.

Tällä hetkellä asiakas, joka käyttää ennakkomaksumenetelmää, ei voi maksaa enempää kuin tilauksen jäljellä oleva hyvityssaldo. Jos esimerkiksi asiakkaan jäljellä olevan luoton saldo on 1 000 dollaria, mutta tilauksen arvo on 1 200 dollaria, asiakas voi maksaa vain 1 000 dollaria ennakkomaksumenetelmän avulla. Asiakkaan on sitten käytettävä erotuksen maksamiseen muuta maksumenetelmää. Tulevassa versiossa Commerce-konfiguraatio sallii käyttäjien käyttää luottorajan yli tilauksia tehtäessä.

**Luotonvalvonta**-moduulissa on uusia luotonhallintaominaisuuksia. Voit ottaa nämä ominaisuudet käyttöön ottamalla **Luotonhallinta**-toiminnon käyttöön **Toimintojen hallinta** -työtilassa. Yksi uusista ominaisuuksista mahdollistaa myyntitilausten asettamisen pitoon estosääntöjen perusteella. Luottopäällikkö-henkilötyyppi voi tämän jälkeen vapauttaa tai hylätä tilaukset lisäanalyysin perusteella. Ominaisuutta myyntitilausten pitoon asettamista varten ei kuitenkaan voi soveltaa Commerce-tilauksiin, koska myyntitilauksiin liittyy usein ennakkomaksuja ja **Luotonhallinta**-toiminto ei tue ennakkomaksuskenaarioita täysin. 

Jos asiakkaan saldo ylittää luottorajan tilauksen täyttämisen aikana, myyntitilauksia ei aseteta pitoon riippumatta siitä, onko **Luotonhallinta**-toiminto käytössä. Sen sijaan Commerce luo joko varoitussanoman tai virhesanoman sen mukaan, mikä **Sanoma luottorajan ylittyessä** -kentän arvona on **Luottorajat**-pikavälilehdessä.

Commercen myyntitilausten pitoon asettamisen estävä **Sulje pois luotonhallinnasta** -omaisuus sijaitsee myyntitilauksen otsikossa (**Retail ja Commerce \> Asiakkaat \> Kaikki myyntitilaukset**). Jos tämän ominaisuuden arvona on **Kyllä** (oletusarvo) Commercen myyntitilausten osalta, tilaukset suljetaan pois luotonhallinnan pitotyönkulusta. Vaikka määritettyä luottorajaa sovelletaan tilauksen täyttämisessä, ominaisuuden nimi on **Sulje pois luotonhallinnasta**. Tilaukset eivät vain mene pitoon.

Ominaisuus Commercen myyntitilausten pitoon estosääntöjen perusteella asettamisen ominaisuus on suunnitteilla tulevia Commerce-versioita varten. Jos sinun on pakotettava Commercen myyntitilaukset kulkemaan uusien luotonhallinnan kulkujen läpi ennen kuin sitä tuetaan, voit mukauttaa Visual Studio -ratkaisusi seuraavia XML-tiedostoja. Muuta tiedostoissa logiikkaa siten, että **CredManExcludeSalesOrder**-merkinnän arvo on **Ei**. Tällä tavoin **Sulje pois luotonhallinnasta** -ominaisuuden oletusarvona Commercen myyntitilausten osalta on **Ei**.

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

Jos **CredManExcludeSalesOrder**-merkinnän arvoksi on määritetty **Ei** ja B2B-asiakas voi ostaa kaupoista käyttämällä myyntipistesovellusta, itsepalvelutukkutapahtumien kirjaaminen saattaa epäonnistua. Tilanne voi olla esimerkiksi, että käteismakutyypille on olemassa estosääntö ja B2B-asiakas on ostanut tavaroita kaupasta käteisellä. Tällöin tuloksena olevaa myyntitilausta ei laskuteta onnistuneesti, koska se asetetaan pitoon. Näin ollen kirjaus epäonnistuu. Tämän vuoksi on suositeltavaa tehdä kokonaisvaltaista testausta tämän mukautuksen käyttöönoton jälkeen.

## <a name="additional-resources"></a>Lisäresurssit

[Yritystenvälisen yhteistyön sähköisen kaupankäynnin sivuston määrittäminen](set-up-b2b-site.md)

[B2B-liikekumppaneiden hallinta asiakashierarkioiden avulla](partners-customer-hierarchies.md)

[Liikekumppanikäyttäjien hallinta yritystenvälisen yhteistyön sähköisen kaupankäynnin sivustoissa](manage-b2b-users.md)

[Tuotemäärän rajojen asettaminen B2B-verkkokauppasivustoille](quantity-limits.md)

[SDK:n ja moduulikirjaston päivitykset](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
