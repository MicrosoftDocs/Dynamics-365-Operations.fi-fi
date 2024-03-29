---
title: Yhteisöpalvelujakamisen moduuli
description: Tässä artikkelissa on tietoja yhteisöpalveluissa jaon moduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88bc5469e3072b625836cc942efbd2206f6dd6ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284681"
---
# <a name="social-share-module"></a>Yhteisöpalvelujakamisen moduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja yhteisöpalveluissa jaon moduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Jako yhteisöpalveluissa -moduulien avulla käyttäjät voivat jakaa sähköisen kaupankäynnin sivuston sivujen URL-osoitteita yhteisöpalveluissa, kuten Facebookissa, Twitterissä, Pinterestissä ja LinkedInissä. Sivuston sivun URL-osoitteita voi jakaa myös sähköpostitse. Jako yhteisöpalveluissa -moduuleja käytetään yleisesti tuotetietosivuilla (PDP-sivuilla). Niiden avulla käyttäjät voivat jakaa tuotetietoja.

Kunkin Jako yhteisöpalveluissa -moduuli on säilö yhteisöpalveluiden jaon nimikkeiden moduuleille. Kukin Jako yhteisöpalveluissa -nimikkeen moduuli voidaan määrittää niin, että se osoittaa tiettyyn yhteisöpalvelun sivustoon. Integrointia Facebookin, Twitterin, Pinterestin, LinkedInin ja sähköpostin kanssa tuetaan. Se on valmis ominaisuus. Kun sivuston käyttäjä valitsee yhteisöpalvelun synbolin, vastaavassa yhteisöpalvelun sivustossa käynnistetään HTML-muotoinen iFrame-kehys. IFrame-kehyksessä käyttäjä voi kirjautua sisään ja näyttää katsomansa sivun sisällön.

Kukin yhteisöpalvelun ympäristö voi seurata evästeitä. Tämä moduuli vaatii siis sivuston käyttäjiä hyväksymään evästeet. Tästä kerrotaan suostumuksesta kertovassa ilmoituksessa. Kun evästeille ei anneta hyväksyntää, moduuli piilotetaan sivulla. Lisätietoja on kohdassa [Evästeiden vaatimustenmukaisuus](cookie-compliance.md).

Seuraavassa kuvassa on esimerkki tuotetietosivulla käytetystä Jako yhteisöpalveluissa -moduulista.

![Esimerkki Jako yhteisöpalveluissa -moduulista.](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a>Jako yhteisöpalveluissa -moduulin ominaisuudet

| Ominaisuuden nimi             | Arvo                 | kuvaus |
|---------------------------|-----------------------|-------------|
| Otsikko                  | Teksti | Tämä ominaisuus määrittää moduulin kuvatekstin. |
| Suunta | **Vaaka** tai **pysty**  | Tämä ominaisuus määrittää yhteisöpalveluiden nimikkeiden asettelun suunnan. |

## <a name="social-share-item-module-properties"></a>Jako yhteisöpalveluissa -nimikkeen moduulin ominaisuudet
| Ominaisuuden nimi             | Arvo                 | kuvaus |
|---------------------------|-----------------------|-------------|
| Yhteisöpalvelut              | **Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **sähköposti** | Avattava valikko, jossa on luettelo yhteisöpalvelun ympäristöistä. |
| Kuvake |Kuva    | Tässä on kuva, joka näkyy vastaava yhteisöpalvelu. Tietoja kunkin ympäristön kuvan käyttämisen parhaasta käytännöstä on yhteisöpalvelun ympäristön SDK:ssa. |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a>Jako yhteisöpalveluissa -moduulin lisääminen ostoruutumoduuliin

Jos haluat lisätä Jako yhteisöpalveluissa -moduulin ostoruutumoduuliin, tee seuraavat toiminnot.

1. Valitse Fabrikam-sivustossa **Sivut** ja valitse sitten **DefaultPDP**-sivu. Avaa tuotetietosivu. 
1. Valitse kolme pistettä (**...**) **Ostoruutu (pakollinen)** -paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Jako yhteisöpalvelussa** -moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Jako yhteisöpalveluissa** -paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Jako yhteisöpalvelussa** -moduuli ja valitse sitten **OK**.
1. Valitse **SocialShare**-moduulin ominaisuusikkunan **Suunta**-kohdassa **Vaaka**. Lisää kuvateksti tarpeen mukaan.
1. Valitse kolme pistettä (**...**) **SocialShare**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **SocialShareItem**-moduuli ja valitse sitten **OK**.
1. Valitse **SocialShareItem**-moduulin ominaisuusikkunan **Yhteisöpalvelut**-kohdassa **Facebook**.
1. Valitse **SocialShareItem**-moduulin ominaisuusikkunan **Kuvake**-kohdassa **+ Lisää kuva**.
1. Valitse **Mediasisällön valitsin** -valintaruudussa Facebook-logokuva ja valitse sitten **OK**. Jos Facebook-logokuvaa ei ole valittavissa, valitse **Lataa uusi medianimike** ja lataa logokuva.
1. Lisää **SocialShareItem**-moduuleja ja määritä niitä lisää tarvittaessa.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**. Sivulla näkyy Jako yhteisöpalveluissa -moduuli.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ostoruutumoduuli](add-buy-box.md)

[Evästeen yhteensopivuus](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
