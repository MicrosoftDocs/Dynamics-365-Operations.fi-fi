---
title: Sivuston valitsinmoduuli
description: Tässä artikkelissa käsitellään sivuston valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 05/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: efd58206d88618aedb6b574afb47da1e9e578ef1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276745"
---
# <a name="site-picker-module"></a>Sivuston valitsinmoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään sivuston valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Jos yrityksellä on useita sivustoja eri markkinoilla, alueilla ja kielialueilla, sivuston käyttäjät tarvitsevat kätevän tavan vaihdella sivustoja ja valitse ensisijaisen ostossivuston. Tätä skenaariota varten käyttäjät voivat selata useita sivustoja sivuston valitsinmoduulin ansiosta. Sivuston valitsinta suositellaan myös silloin, kun sähköpostiosoitteessa on otettu käyttöön [Sivuston tunnistus ja uudelleenohjaus](geo-detection-redirection.md), jotta asiakkaat voivat ohittaa [maan tai alueen valinta](country-region-picker-module.md) -moduulin avulla ilmaisemiaan toimipaikka-asetusta. 

Sivuston valitsinmoduuli on määritettävä käyttämällä sivustoluetteloa (markkinat, alueet tai kielialueet), jota sivuston käyttäjät voivat selata. Seuraavassa kuvassa on esimerkki sivuston sivun otsikossa olevasta sivuston valitsinmoduulista.

![Esimerkki sivuston valitsinmoduulista sivuston sivun otsikossa.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Sivuston valitsinmoduulin ominaisuudet

| Ominaisuuden nimi | Arvo                 | Kuvaus |
|---------------|-----------------------|-------------|
| Otsikko       | Teksti                  | Moduulin otsikko. |
| Sivustoasetukset  | Nimi, kuva, URL      | Tämä ominaisuus määrittää nimen, linkin sivuston aloitussivulle ja valinnaisen kuvan, jonka jokainen moduuliin kuuluva sivusto näkee. Kuva voi olla lippu tai jotakin muuta, joka ilmaisee markkinan, alueen tai kielialueen. |

## <a name="add-a-site-picker-module-to-a-page"></a>Sivuston valitsinmoduulin lisääminen sivulle

Sivuston valitsinmoduuli voidaan lisätä [otsikkomoduulin](author-header-module.md) **Sivustonvalitsin**-kohtaan. Kun sivuston valitsinmoduuli on lisätty, voit määrittää sen otsikon ja sivustovaihtoehdot. Yleensä otsikkomoduuli sisältyy otsikko-osaan, joka voidaan jakaa sivuston eri verkkokauppasivuille. 

Voit lisätä sivuston valitsinmoduulin otsikkomoduuliin seuraavasti.

1. Valitse otsikkoosan otsikkomoduulissa **Sivustonvalitsin**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Lisää **Valitse moduulit** -valintaikkunassa **Sivustonvalitsin**-moduuli ja valitse sitten **OK**.
1. Valitse **Sivustonvalitsin**-ominaisuusruudusta **Lisää sivustovaihtoehtojen luettelo**. Näkyviin tulee muokattavissa oleva **Sivustovaihtoehtojen luettelo**.
1. Valitse **Sivustovaihtoehtojen luettelo**. Näyttöön tulee **Sivustovaihtoehtojen luettelo** -valintaikkuna.
1. Kirjoita **Sivuston nimi** -kenttään sivuston nimen teksti, joka näkyy avattavassa sivuston valitsinluettelossa.
1. Valitse **Sivuston uudelleenohjauksen URL-osoite** -kohdasta **Lisää linkki**. **Lisää linkki** -lisätietoikkuna avautuu.
1. Valitse **Lisää linkki** -lisätietoikkunassa **Mukautettu sivu** ja valitse sitten **Seuraava**.
1. Valitse sivuston URL-luettelosta URL-osoite polulla, jonka loit lisätessäsi kanavaa sivustoon (esimerkiksi `www.adventure-works.com/fr-ca`) valitse sitten **Käytä**.
1. Valitse **OK**.
1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
1. Julkaise sivu valitsemalla **Julkaise**.

Seuraavassa esimerkissä sivuston valitsinmoduuli on lisätty sellaisen otsikkomoduulin **Sivustonvalitsin**-paikkaan, joka sisältyy **HeaderContainer**-nimiseen otsikko-osaan.

![Esimerkki sivuston valitsinmoduulista otsikko-osassa.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ylätunnistemoduuli](author-header-module.md)

[Navigointipolkumoduuli](add-breadcrumb.md)

[Siirtymisvalikkomoduulit](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
