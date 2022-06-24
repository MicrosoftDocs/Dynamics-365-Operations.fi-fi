---
title: Sivuston hakukoneoptimointia (SEO) koskevia tietoja
description: Tämä artikkeli kattaa hakukoneoptimoinnin sivustossa kehityksestä tuotantoon.
author: psimolin
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 6747df3c56fb05248210f78ebf2176a56ce78329
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896898"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Sivuston hakukoneoptimointia (SEO) koskevia tietoja


[!include [banner](includes/banner.md)]

Tämä artikkeli kattaa hakukoneoptimoinnin sivustossa kehityksestä tuotantoon.

## <a name="a-site-that-is-under-development"></a>Sivustoa kehitetään

Jotta hakukoneet eivät indeksoisi työn alla olevia sivustoja, kaikilla sivuston sivuilla tulisi olla **noindex**- ja **nofollow**-metatunnisteet. Hyvä käytäntö on luoda [MetaTags-moduuliin](metatags-module.md) perustuva katkelma, joka sisältää seuraavan metatunnistemerkinnän ja varmistaa, että kyseinen katkelma lisätään sivuston kaikkien mallien HTML \<head\>-osaan.

```html
<meta name="robots" content="noindex,nofollow" /> 
```

## <a name="soft-launch-of-a-site"></a>Sivuston pehmeä käynnistäminen

Pehmeän käynnistämisen aikana sivusto on vain rajoitetun yleisön tai markkina-alueen käyttettävissä ennen täydellisen käyttöönoton tapahtumista. Jos sivustossa tehdään pehmeä käynnistäminen, **noindex**-metatunnukset kannattaa jättää paikoilleen. Näin varmistetaan, että pehmeä käynnistys jää rajoitetun yleisön käyttöön.

## <a name="a-site-that-is-in-production"></a>Sivusto, joka on tuotannossa

Kun sivusto on tuotannossa, varmista, että kaikki sivuston sivut on merkitty oikein tunnuksilla. Microsoft Dynamics 365 Commerce käyttää sivulle syötettyjä tietoja sivun hakukoneoptimoinnin tietojen hahmontamisessa. Seuraavat moduulit tarjoavat tämän toiminnon: luokkasivun yhteenveto, luettelosivun yhteenveto ja tuotesivun yhteenveto.

Voit optimoida hakukoneindeksoinnin, kun hahmontamisen kehys käyttää sekä Dynamics 365 Commercen määritettyjä hakukoneoptimoinnin ominaisuuksien tietoja että moduulikohtaisia tietoja. Jos kyseessä on sivusto, joka on tuotannossa, varmista, että robots.txt-tiedosto mahdollistaa indeksoinnin koko sivustossa ja että se sisältää linkit julkaistuun sivustokartta-asiakirjaan. Ota käyttöön sivustokartan luontitoiminto kohdassa **Sivuston asetukset \> Sivustokartta käytössä**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Sivun hakukoneoptimoinnin asetukset sisäistä esikatselua, rajoitettuja yleisöjä ja kaikkia yleisöjä varten

Koska Dynamics 365 Commerce tukee WYSIWYG-todennettuja esikatseluita visuaalisessa sivunmuodostimessa, tekijät voivat valmistella sivun sisällön niin, ettei heidän tarvitse huolehtia siitä, että tiedot näkyvät sivustolla kävijöille. Jos sivu on julkaistava, mutta sen käyttöä on rajoitettava, sillä on oltava **noindex**-metatunnus. Tällöin hakukoneet eivät indeksoi sitä. Kun sivu on valmis kaikkia varten, kaikki hakukoneoptimoinnin perusmetatiedot ovat olemassa. Näin maksimoidaan hakukoneindeksoinnin tehokkuus. Lisäksi **nolimit**-metatunnus on poistettava.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen kaupankäynnin käyttäjien ja roolien hallinta](manage-ecommerce-users-roles.md)

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)

[Sisällön suojauskäytännön (CSP) hallinta](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
