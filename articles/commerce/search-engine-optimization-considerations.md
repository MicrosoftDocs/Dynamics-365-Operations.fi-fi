---
title: Sivuston hakukoneoptimointia (SEO) koskevia tietoja
description: Tämä artikkeli kattaa hakukoneoptimoinnin sivustossa kehityksestä tuotantoon.
author: josaw1
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 77bbc04e849cf1cdeb7ce19226f43354635ddbe0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275616"
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
