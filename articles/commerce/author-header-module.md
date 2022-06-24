---
title: Ylätunnistemoduuli
description: Tässä artikkelissa käsitellään ylätunnistemoduuleja ja sivun ylätunnisteiden luontia Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7cd53a57c16c180cb7e8958cc3a6bed1fff0512a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876635"
---
# <a name="header-module"></a>Ylätunnistemoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään ylätunnistemoduuleja ja sivun ylätunnisteiden luontia Microsoft Dynamics 365 Commercessa.

Dynamics 365 Commercen sivun otsikko on määritetty sivun osaksi, joka sisältää otsikon, kampanjabannerin ja evästeiden hyväksyntämoduulit. 

Ylätunnistemoduuli sisältää sivuston logon, linkit siirtymishierarkiaan, linkit muille sivuston sivuille, ostoskorim kuvakkeen moduulin, toivelistasymbolin, kirjautumisvaihtoehdot ja hakupalkin. Ylätunnistemoduuli optimoidaan automaattisesti sitä laitetta varten, jolla sivustoa tarkastellaan (eli pöytätietokonetta tai mobiililaitetta varten). Esimerkiksi mobiililaitteessa siirtymispalkki tiivistetään **Valikko**-painikkeeksi (jossa on useita *viivoja*).

Seuraavassa kuvassa on esimerkki otsikkomoduulista kotisivulla.

![Esimerkki otsikkomoduulista.](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Ylätunnistemoduulin ominaisuudet

Ylätunnistemoduuli tukee **Logon kuva**-, **Logon linkki**- ja **Oman tilin linkit** -ominaisuuksia. 

**Logon kuva**- ja **Logon linkki** -ominaisuuksilla määritetään sivulla oleva logo. Lisätietoja on kohdassa [Logon lisääminen](add-logo.md). 

**Oman tilin linkit** -ominaisuudella voidaan määrittää ne tilisivut, joiden pikalinkit sivuston omistaja haluaa näyttää ylätunnisteessa.

## <a name="modules-that-are-available-within-a-header-module"></a>Ylätunnistemoduulin käytettävissä olevat moduulit

Seuraavia moduuleja voi käyttää ylätunnistemoduulissa:

- **Siirtymisvalikko** – Siirtymisvalikko edustaa kanavan siirtymishierarkiaa ja muita staattisia siirtymislinkkejä. Lisätietoja on kohdassa [Siirtymisvalikkomoduuli](nav-menu-module.md).

- **Haku** – Hakumoduulin avulla käyttäjät voivat etsiä tuotteita hakusanojen avulla. Oletushakusivun URL-osoite ja hakukyselyn parametrit on annettava valitsemalla **Sivuston asetukset \> Laajennukset**. Hakumoduulissa on ominaisuuksia, joiden avulla voit estää hakupainikkeen tai -selitteen tarvittaessa. Hakumoduuli tukee myös automaattisia ehdotuksia, kuten tuotteen, avainsanan ja luokan hakutuloksia.

- **Ostoskorikuvake** – Ostoskorikuvakemoduuli edustaa ostoskorin symbolia, joka ilmaisee, kuinka monta nimikettä ostoskorissa on tiettynä ajankohtana. Lisätietoja on kohdassa [Ostoskorikuvakemoduuli](cart-icon-module.md).

- **Toimipaikan valitsin** – Toimipaikan valitsinmoduulissa käyttäjät voivat selata esimääritettyjä toimipaikkoja markkina-alueen, alueiden ja kielialueiden perusteella. Lisätietoja on kohdassa [Toimipaikan valitsinmoduuli](site-selector.md).

- **Myymälän valitsin** – Myymälän valitsinmoduuli voidaan sisällyttää otsikon myymälän valitsinpaikkaan. Sen avulla käyttäjät voivat selata ja etsiä lähellä olevia myymälöitä. Käyttäjät voivat määrittää myös ensisijaisen myymälän. Kyseinen myymälä näytetään sitten otsikossa. Jos myymälän valitsinmoduuli sisältyy otsikkomoduuliin, sen **Tila**-ominaisuudeksi on määritettävä **Etsi myymälät**. Lisätietoja on kohdassa [Myymälän valitsinmoduuli](store-selector.md).

> [!NOTE]
> - Ostoskorikuvakemoduulin käyttämistä otsikkomoduuleissa tuetaan Dynamics 365 Commerce -version 10.0.11 julkaisusta eteenpäin.
> - Sivuston valitsinmoduulin käyttämistä otsikkomoduuleissa tuetaan Dynamics 365 Commerce -version 10.0.14 julkaisusta eteenpäin.
> - Myymälän valitsinmoduulin käyttämistä otsikkomoduuleissa tuetaan Dynamics 365 Commerce -version 10.0.15 julkaisusta eteenpäin.

## <a name="header-module-in-the-adventure-works-theme"></a>Otsikkomoduuli Adventure Works -teemassa

Otsikkomoduuli tukee **Mobiililogo**-ominaisuutta Adventure Works -teemassa. Tämä ominaisuus sallii logon määrittämisen mobiililaitteiden näyttöjä varten. **Mobiililogo**-ominaisuus on käytettävissä moduulimääritelmän laajennuksena.

> [!IMPORTANT]
> Adventure Works -teema on käytettävissä Dynamics 365 Commerce -versiosta 10.0.20 eteenpäin.

## <a name="create-a-header-fragment-for-a-page"></a>Sivun otsikko-osan luominen

Voit luoda otsikko-osan seuraavasti.

1. Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.
1. Valitse **Valitse katkelma** -valintaikkunassa **Kontti**-moduuli. Syötä osan nimi ja valitse **OK**.
1. Valitse **Oletussäilö**-paikka ja määritä sitten Ominaisuudet-ruudussa oikealla puolella oleva **Leveys**-ominaisuuden arvoksi **Täytä näyttö**.
1. Valitse kolme pistettä (**...**) **Oletuskontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Evästeiden hyväksyntä**-, **Otsikko**- ja **Kampanjabanneri**-moduulit ja valitse sitten **OK**.
1. Valitse **Kampanjabanneri**-moduulin ominaisuusruudussa **Lisää sanoma** ja valitse sitten **Sanoma**.
1. Lisää **Sanoma**-valintaruutuun teksti ja linkit mainossisältöä varten ja valitse **OK**.
1. Lisää **evästeiden hyväksyntämoduulin** ominaisuusruudussa teksti ja muokkaa sitä. Linkitä teksti sivuston tietosuojakäytännön sivulle.
1. Valitse otsikkomoduulissa **Siirtymisvalikko**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Siirtymisvalikko**-moduuli ja valitse sitten **OK**.
1. Valitse siirtymisvalikkomoduulin ominaisuusruudun **Siirtymisvalikon lähde** -kohdassa **Retail Server**.
1. Valitse siirtymisvalikkomoduulin ominaisuusruudun **Staattiset valikon vaihtoehdot** -kohdassa **Lisää valikon vaihtoehto** ja valitse sitten **Valikon vaihtoehto**. 
1. Syötä **Valikon vaihtoehto** -valintaruudun **Valikon vaihtoehdon teksti** -kohtaan Yhteyshenkilö.
1. Valitse **Valikon vaihtoehto** -valintaruudun **Valikon vaihtoehdon linkin kohde** -kohdassa **Lisää linkki**.
1. Valitse **Lisää linkki** -valintaikkunassa sivuston yhteyshenkilösivun URL-osoite ja valitse sitten **OK**.  
1. Valitse **Valikon vaihtoehto** -valintaikkunassa **OK**.
1. Valitse otsikkomoduulissa **Haku**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Haku**-moduuli ja valitse sitten **OK**.
1. Määritä hakumoduulin tarvittavat ominaisuudet ominaisuusruudussa.
1. Valitse otsikkomoduulissa **Ostoskorikuvake**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Ostoskorikuvake**-moduuli ja valitse sitten **OK**.
1. Määritä ostoskorikuvakemoduulin tarvittavat ominaisuudet ominaisuusruudussa. Jos haluat, että ostoskorikuvake näyttää ostoskorin yhteenvedon (joka tunnetaan myös nimellä pienoiskärry), kun käyttäjä vie osoittimen sen päälle, valitse **Näytä pienoiskärry**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.

Voit varmistaa, että ylätunniste näkyy jokaisella sivulla, noudattamalla näitä ohjeita jokaisen sivustolle luodun sivumallin kohdalla.

1. Lisää **Oletussivu**-moduulin **Otsikko**-paikkaan alatunnistemoduulissa luomasi alatunnisteosa.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Promopalkkimoduuli](add-alert.md)

[Siirtymisvalikkomoduuli](nav-menu-module.md) 

[Evästeiden hyväksyntä](cookie-consent-module.md)

[Alatunnistemoduuli](author-footer-module.md)

[Toimipaikan valitsinmoduuli](site-selector.md)

[Myymälän valitsinmoduuli](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
