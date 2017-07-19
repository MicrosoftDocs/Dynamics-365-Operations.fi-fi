---
title: "Kustannusmerkinnät"
description: "Tässä artikkelissa on tietoja kustannusmerkinnöistä ja siitä, milloin niitä luodaan. Kustannusmerkintä on tietue, joka rekisteröi tietyn tapahtuman määrän ja kustannukset."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1045ecbf7080f12bc60336609180173544e4e0eb
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017

---

# <a name="cost-entries"></a>Kustannusmerkinnät

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tietoja kustannusmerkinnöistä ja siitä, milloin niitä luodaan. Kustannusmerkintä on tietue, joka rekisteröi tietyn tapahtuman määrän ja kustannukset.

Kustannustapahtumat ovat koosteita varastotapahtumista, jotka on tallennettu aktiivisiin taloushallinnon varastodimensioihin.

## <a name="examples"></a>Esimerkkejä
### <a name="example-1-no-cost-entries-are-created"></a>Esimerkki 1: Kustannustapahtumia ei luoda

Kirjauskansion siirtotapahtuma kirjataan. Tapahtuma siirtää yhden nimikkeen A sijainnista A kohteeseen B. Varastodimension sijainnin ei katsota kuuluvan osaksi kustannuskohdetta. Joten, tapauksessa on kaksi varastotapahtumaa eikä yhtäään kustannusmerkintää.

### <a name="example-2-cost-entries-are-created"></a>Esimerkki 2: Kustannustapahtumia luodaan

Kirjauskansion siirtotapahtuma kirjataan. Tapahtuma siirtää yhden nimikeyksikön A toimipaikasta 1 toimipaikkaan 2. Toimipaikan varastodimensiota pidetään osana kustannusobjektia. Joten, tapauksessa on kaksi varastotapahtumaa ja kaksi kustannusmerkintää.

### <a name="example-3-one-cost-entry-is-created"></a>Esimerkki 3: Yksi kustannustapahtuma luodaan

Ostotilauksen tuotteen vastaanottotapahtuma on rekisteröity. Tapahtuma rekisteröi 100 kappaletta nimikettä A, yksikkökustannuksen ollessa 10,00 Yhdysvaltain dollaria (USD). Koska kohde A käyttää sarjanumeroja seuratakseen varastonhallinnan päämäärää, ainutkertainen sarjanumero luodaan kullekin nimikkeelle, joka on vastaanotettu. Joten, tapauksessa on 100 varastotapahtumaa ja yksi kustannusmerkintä.

## <a name="cost-entries-page"></a>Kustannusmerkintäsivu
Uuden **Kustannustapahtuma**-sivun avulla voit tarkastella ja hallita määrien ja kustannuksien rekisteröinnit. Tämä sivu täydentää **Varastotapahtuma-** ja **Varastotilitys**sivuja. Tapahtuman tietueet ovat rekisteröityjä aikajärjestyksessä. Siksi voit nopeasti etsiä ja kontrolloida tietyn tapahtuman kumulatiiviset kustannukset tai kaikki tapahtumat, jotka liittyvät asiakirjaan. Tässä on esimerkki:

-   Tuotteen vastaanottotapahtuma on rekisteröity nimikkeelle A. Sata kappaletta vastaanotetaan yksikkökustannuksin 10,00 USD.
-   Muutaman päivän kuluttua laskutapahtuman kirjaamisesta, kustannukset nousevat 11,00 dollariin (USD). Joten, kokonaissumma on 1,100 euroa. Toinen tosite luodaan kattamaan 100 dollarin (USD) ero myyntihintaan.
-   Muutaman päivän kuluttua luokittelematon 15.00 dollarin (USD) kulu rekisteröidään kuljetuskuluina ostotilaukseen.

| Tosite | Päivämäärä       | Viite      | Numero | Erätunnus  | Määrä | Summa  |
|---------|------------|----------------|--------|---------|---------------|----|
| 00001   | 01.01.2015 | Ostotilaus | 100001 | 0000101 | 100,00   | 1000.00 |
| 00002   | 20.01.2015 | Ostotilaus | 100001 | 0000101 |          | 100,00  |
| 00003   | 31.01.2015 | Oikaisu     | 100001 | 0000101 |          | 15,00   |

**Kustannustapahtumat**-sivun avulla voidaan suodattaa asiakirjan tunnuksella ja asiakirjan päivämäärällä. 

> [!NOTE]
> Huomautus: Kustannustapahtumat käytettävissä vain [kustannusobjekteja](cost-object.md) tai vapautettuja tuotteita varten.

<a name="see-also"></a>Lisätietoja
--------

[Kustannusobjektit](cost-object.md)




