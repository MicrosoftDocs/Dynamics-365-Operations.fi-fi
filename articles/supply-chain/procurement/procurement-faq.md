---
title: Hankinnan usein kysytyt kysymykset
description: Tämä ohjeaihe vastaa Supply Chain Managementin hankintatoimintoa koskeviin usein kysyttyihin kysymyksiin (UKK)
author: kamaybac
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 09c99b88bc47609158805cdba1291ae462cda178
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476177"
---
# <a name="procurement-faq"></a>Hankinnan usein kysytyt kysymykset

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe vastaa Supply Chain Managementin hankintatoimintoa koskeviin usein kysyttyihin kysymyksiin (UKK).

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Voinko näyttää vain itse luomiani ostotilauksia?

Tämä toiminto ei ole tällä hetkellä käytettävissä.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Voinko varata varastoa ja luoda tapahtumia rekisteröidyn varaston perusteella ostotilauksessa?

### <a name="issue-description"></a>Ongelman kuvaus

Vaikka nimikkeitä olisi ostotilauksessa *Rekisteröity*-tilassa, voit kuitenkin varata varastoa. Toisin sanoen voit luoda tapahtumia rekisteröidyn varaston perusteella.

### <a name="reproduce-the-issue"></a>Ongelman toistaminen

Seuraavassa esitetään yksi tapa ongelman toistamiseen.

1. Luo ostotilaus.
2. Ostotilausrivin rekisteröinti.
3. Huomaa, että voit luoda varauksia tai tapahtumia rekisteröidyn varaston perusteella.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä on suunniteltu ominaisuus. Oletetaan, että rekisteröidyt nimikkeet ovat fyysisesti saapuneet varastoon ja että ne ovat näin ollen varattavissa.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Voinko löytää ostotilauksen peruneen käyttäjän?

Näitä tietoja seurataan vain, jos ostotilaus edellyttää muutoksenhallintaa. Jos käytät muutoksenhallintaa, voit nähdä muutoksen (peruutuksen) lähettäjän ja hyväksyjän.

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>Miksi en voi yhdistää ostosopimusta olemassa olevaan ostotilaukseen?

Ostosopimus on yhdistettävä ostotilaukseen, kun ostotilaus luodaan. Muussa tapauksessa ostotilausrivejä ei voi liittää ostosopimusriveihin.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Mikä tarkistus tuottaa sanoman "Päivitä manuaalisesti syötetyt hinnat ja alennukset tai ulkoinen asiakirja"?

Kun muutat lähetyspäivämäärää, näyttöön voi tulla sanoma "Päivitä manuaalisesti syötetyt hinnat ja alennukset tai ulkoinen asiakirja" Saat tämän sanoman, koska jos lähetyspäivämäärää muutetaan, muu kauppa- tai myyntisopimus saattaa tulla voimaan ja aiheuttaa hinnanmuutoksen. Toimituspäivämäärän muuttaminen voi vaikuttaa myös fyysisen varastoinnin aikatauluihin ja liittyviin tietoihin.

Sanoma luodaan, kun jokin päivämääristä tai muista parametreista muuttuu. Sanoman tarkoitus on varmistaa, että olet tietoinen hinnanmuutoksista, joita voi aiheutua kyseisistä muutoksista.

Sanoma on kauppasopimuksen arviointi (TAE) -kehote. Täydellinen kuvaus [Kauppasopimuksen arviointikäytännöt](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Miksi voin kirjata vain yhden laskun ostotilausriville, jolla on luokkaperusteisia nimikkeitä?

Määrä on pakollinen, jos haluat kirjata laskuja. Siten, jos rivin kokonaismäärä on laskutettu vain osittaisen summan osalta, et voi laskuttaa jäljellä olevaa summaa toisella laskulla.
