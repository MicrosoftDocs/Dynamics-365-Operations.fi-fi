---
title: Sivuston hakukoneoptimointia (SEO) koskevia tietoja
description: Tämä ohjeaihe kattaa hakukoneoptimoinnin sivustossa kehityksestä tuotantoon.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6ffc772addb330abe7205007662a3f3e08a3e47f
ms.sourcegitcommit: f16db76c1c235dfa445b50614bcee9219782d6dc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961583"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Sivuston hakukoneoptimointia (SEO) koskevia tietoja


[!include [banner](includes/banner.md)]

Tämä ohjeaihe kattaa hakukoneoptimoinnin sivustossa kehityksestä tuotantoon.

## <a name="a-site-that-is-under-development"></a>Sivustoa kehitetään

Sivuston ollessa kehitettävänä sivuston kaikilla sivuilla tulisi olla **NOINDEX**- ja **NOFOLLOW**-metatunnukset. Näin hakukoneet eivät indeksoi sivuja ja tallenna sivuston kehitysversioita välimuistiin. Voit tehdä tämän määrityksen, jos sivuston sivumalliin on lisätty oletusmetatunnusten moduuli. Oletusarvoiset metatunnusten ominaisuudet ovat tämän jälkeen hakukoneoptimoinnin ominaisuuksien osan käytettävissä sivueditorissa. Näiden ominaisuuksien avulla voit hallita metatunnuksia.

## <a name="soft-launch-of-a-site"></a>Sivuston pehmeä käynnistäminen

Pehmeän käynnistämisen aikana sivusto on vain rajoitetun yleisön tai markkina-alueen käyttettävissä ennen täydellisen käyttöönoton tapahtumista. Jos sivustossa tehdään pehmeä käynnistäminen, **NOINDEX**-metatunnukset kannattaa jättää paikoilleen. Näin varmistetaan, että pehmeä käynnistys jää rajoitetun yleisön käyttöön.

## <a name="a-site-that-is-in-production"></a>Sivusto, joka on tuotannossa

Kun sivusto on tuotannossa, varmista, että kaikki sivuston sivut on merkitty oikein tunnuksilla. Microsoft Dynamics 365 Commerce käyttää sivulle syötettyjä tietoja sivun hakukoneoptimoinnin tietojen hahmontamisessa. Seuraavat moduulit tarjoavat tämän toiminnon: luokkasivun yhteenveto, luettelosivun yhteenveto ja tuotesivun yhteenveto.

Voit optimoida hakukoneindeksoinnin, kun hahmontamisen kehys käyttää sekä Dynamics 365 Commercen määritettyjä hakukoneoptimoinnin ominaisuuksien tietoja että moduulikohtaisia tietoja. Jos kyseessä on sivusto, joka on tuotannossa, varmista, että robots.txt-tiedosto mahdollistaa indeksoinnin koko sivustossa ja että se sisältää linkit julkaistuun sivustokartta-asiakirjaan. Ota käyttöön sivustokartan luontitoiminto kohdassa **Sivuston asetukset \> Sivustokartta käytössä**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Sivun hakukoneoptimoinnin asetukset sisäistä esikatselua, rajoitettuja yleisöjä ja kaikkia yleisöjä varten

Koska Dynamics 365 Commerce tukee WYSIWYG-todennettuja esikatseluita visuaalisessa sivunmuodostimessa, tekijät voivat valmistella sivun sisällön niin, ettei heidän tarvitse huolehtia siitä, että tiedot näkyvät sivustolla kävijöille. Jos sivu on julkaistava, mutta sen käyttöä on rajoitettava, sillä on oltava **NOINDEX**-metatunnus. Tällöin hakukoneet eivät indeksoi sitä. Kun sivu on valmis kaikkia varten, kaikki hakukoneoptimoinnin perusmetatiedot ovat olemassa. Näin maksimoidaan hakukoneindeksoinnin tehokkuus. Lisäksi **NOLIMIT**-metatunnus on poistettava.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen kaupankäynnin käyttäjien ja roolien hallinta](manage-ecommerce-users-roles.md)

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)

[Sisällön suojauskäytännön (CSP) hallinta](manage-csp.md)
