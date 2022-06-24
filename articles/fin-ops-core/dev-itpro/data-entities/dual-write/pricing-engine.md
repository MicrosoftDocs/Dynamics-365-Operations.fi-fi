---
title: Synkronointi tarvittaessa Supply Chain Managementin hinnoittelumoduulin kanssa
description: Tässä artikkelissa kuvataan, kuinka hinnoittelumoduulia käytetään Microsoft Dynamics 365 Supply Chain Managementissa Microsoft Dynamics 365 Salesista.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 259bdd5f868945c3857b045fbd3cbd4fceb26951
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862216"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Synkronointi tarvittaessa Supply Chain Managementin hinnoittelumoduulin kanssa

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management sisältää hinnoittelumoduulin, joka käsittelee kauppasopimukset, hinnastot, kanta-asiakasohjelmat, kampanjat ja alennukset. Hinnoittelumoduuli määrittää tietyn tarjouksen tai tilauksen parhaan hinnan käyttämällä monimutkaisia sääntöjä. Kun käytät kaksoiskirjoittamista, voit käyttää joko staattista hinnoittelua tai hinnoittelumoduulia Supply Chain Managementissa Microsoft Dynamics 365 Salesin **tarjous**- ja **tilaus**-sivuilla.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Hinnoittelumoduulin käyttäminen Salesin Supply Chain Managementista

1. Siirry Salesissa kohtaan **Myynti \> Tilaukset**.
1. Valitse **Uusi** luodaksesi uuden tilauksen tai valitse olemassa oleva tilaus **Omat tilaukset** -luettelosta.
1. Uuden tilausrivin lisääminen.
1. Jos luot uuden tilauksen, valitse toimintoruudusta **Hintatilaus**. Jos päivität olemassa olevan tilauksen, valitse toimintoruudusta **Laske uudelleen**.
1. Seuraavat sarakkeet täytetään automaattisesti:

    - Tietojen määrä
    - Alennusprosentti
    - Alennus
    - Rahdin ennakkosumma
    - Rahdin summa
    - Vero yhteensä
    - Loppusumma

> [!NOTE]
> Tarjousten luomiseen liittyy vastaava prosessi.

## <a name="how-it-works"></a>Näin se toimii

Kun luot tilauksen Myynti-kansiossa, tilaus synkronoidaan heti Supply Chain Managementiin käyttämällä Myynti-kenttään syöttämiesi arvojen arvoja. Kun valitset Myynti-kohdasta **Hintatilaus** tai **Hintatarjous**, Supply Chain Management laskee kunkin tilausrivin hinnan ja kokonaistilauksen Supply Chain Managementissa määritettyjen kauppasopimussääntöjen perusteella. Uudet lasketut arvot synkronoidaan sitten takaisin Myynti-kohteeseen.

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>Kauppasopimuksen arviointiasetusten määrittäminen Supply Chain Managementissa

Voit määrittää Supply Chain Managementin niin, että ne joko koskevat kauppasopimuksia tai ohitat ne, kun se laskee myyntiin luodun tilauksen hinnan. Määritä tämä asetus noudattamalla näitä ohjeita.

1. Kirjaudu sisään Supply Chain Management -ympäristöön.
1. Valitse **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.
1. Lisää tai poista **Manuaalisesti syötettävän** käytännön rivi tai lisää se tarpeen mukaan **Hinnat**-välilehden **Kauppasopimuksen arviointi** -pikavälilehteen. Tämän käytännön tavoitettavuus tai poissaolo määrittää, ohitetaanko myyntiin syötetty myyntihinta automaattisesti Supply Chain Managementn hinnoittelumoduulilla.

    - Jos **Manuaalinen merkintä** -käytäntö *ei ole* **Kauppasopimusarviointi**-asetuksissa, Supply Chain Managementissa on hintojen päätiedot. Kun käyttäjä valitsee Myynti-toiminnon toimintoruudusta **Hintatilauksen** tai **Hintatarjouksen**, Supply Chain Managementin hinnoittelumoduulia kutsutaan ja myyntiin syötetty myyntihinta korvataan, ellei se ole sama kuin Supply Chain Managementissa laskettu myyntihinta.
    - Jos **Manuaalinen merkintä** -käytäntö *on* **Kauppasopimusarviointi**-asetuksissa, Salesissa on hintojen päätiedot. Myyntiin määritettyä myyntihintaa ei voi korvata automaattisesti, kun käyttäjä valitsee Myynti-toimintoruudusta **Hintatilauksen** tai **Hintatarjouksen**.
    - Erityistapauksena käsitellään tilausrivejä ja tarjousrivejä, jonka **yksikköhinta**- ja/tai **alennusarvo** on *0* (nolla). Jos asianmukainen kauppasopimuksen hinta on käytettävissä, Supply Chain Management käyttää sitä *aina* näihin kenttiin **kauppasopimuksen arviointi** -asetuksista riippumatta.

    Esimerkki näistä tapauksista on seuraavassa.

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>Esimerkkitapaus 1: Kauppasopimuksen arviointi ilman manuaalinen syöttö -valintaa

Tässä skenaariossa Supply Chain Managementin **Kauppasopimusarviointi**-asetus *ei* sisällä **Manuaalinen syöttäminen** -käytäntöä. Myyntikäyttäjä määrittää tilausrivin, jonka myyntihinta ei ole nolla. Nimikkeelle ei ole määritetty myyntihintaa Supply Chain Managementissa.

1. Sales-kohteessa käyttäjä luo tilausrivin, jonka **yksikköhinta**-arvo on 1 Yhdysvaltain dollari (USD).
1. Tilausrivi synkronoidaan Supply Chain Managementiin ja sen myyntihinta on 1 USD.
1. Myynti-kohdassa käyttäjä valitsee **hintatilauksen** toimintoruudusta.
1. Supply Chain Management etsii merkityksellisiä hintoja ja alennuksia ja laskee sitten summat. Koska nimikkeellä ei ole myyntihintaa Supply Chain Managementissa, laskelma päivittää rivin niin, että sen myyntihinta on 0 USD.
1. Rivin uusi myyntihinta synkronoidaan takaisin Salesiin.
1. Tuloksena on Salesin tilausrivi, jonka myyntihinta on 0 USD.

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>Esimerkkitapaus 2: Kauppasopimuksen arviointi manuaalinen syöttö -valinnalla

Tässä skenaariossa Supply Chain Managementin **Kauppasopimusarviointi**-asetus *sisältää* **Manuaalinen syöttäminen** -käytännön. Salesin käyttäjä määrittää tilausrivin, jonka myyntihinta ei ole Salesissa nolla. Supply Chain Management sisältää kauppasopimuksen, jossa määritetään tilatulle nimikkeelle 2 USD myyntihinta.

1. Sales-kohteessa käyttäjä luo tilausrivin nimikkeelle, jonka **yksikköhinta**-arvo on 1 USD.
1. Tilausrivi synkronoidaan Supply Chain Managementiin ja sen myyntihinta on 1 USD.
1. Myynti-kohdassa käyttäjä valitsee **hintatilauksen** toimintoruudusta.
1. Koska Supply Chain Managementin **kauppasopimuksen arviointi** -asetukset sisältävät **manuaalinen merkintä** -käytännön, myyntihintaa ei muuteta, vaikka sovellettava kauppasopimus määrittää toisen myyntihinnan.
1. Myyntihinta ei muutu Sales- ja Supply Chain Managementissa.

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>Esimerkki 3: Kauppasopimuksen arviointi nimikkeelle, jonka myyntihinta on nolla Sales-riveissä

Tässä skenaariossa Supply Chain Managementin **Kauppasopimusarviointi**-asetus *sisältää* **Manuaalinen syöttäminen** -käytännön. Salesin käyttäjä määrittää tilausrivin, jonka myyntihinta on Salesissa 0 (nolla). Supply Chain Management sisältää kauppasopimuksen, jossa määritetään tilatulle nimikkeelle 2 USD myyntihinta.

1. Salesissa käyttäjä luo tilausrivin, jonka **yksikköhinta**-arvo on 0 USD ja **rivin alennus** -arvo on 0 USD.
1. Tilausrivi synkronoidaan Supply Chain Managementiin ja sen myyntihinta on 0 USD.
1. Koska se vastaanottaa tilausrivin, jonka myyntihinta on 0 (nolla), Supply Chain Management kutsuu hinnoittelumoduulia, vaikka **manuaalinen merkintä** -vaihtoehto olisi käytössä. Hinnoittelumoduuli palauttaa kauppasopimuksen 2 USD myyntihinnan ja päivittää Supply Chain Managementin tilausrivin.
1. Päivitettyä myyntihintaa ei ole vielä synkronoitu tilausrivin kanssa Salesissa.
1. Myynti-kohdassa käyttäjä valitsee **hintatilauksen** toimintoruudusta.
1. Supply Chain Managementin tilausrivi säilyttää myyntihintansa 2 USD, joka on nyt synkronoitu takaisin Salesiin. Näin ollen myyntirivin **yksikköhinta**-arvo päivitetään Salesissa 0 USD:sta 2 USD:in.
1. Käyttäjä määrittää Sales-kenttään uuden **rivialennuksen** 0,50 USD. Sales laskee nyt, että rivin **Laajennettu summa** -arvo on 1,50 USD.
1. Tilausrivi synkronoidaan Supply Chain Managementiin ja sen **Rivialennus**-arvo on 0,50 USD.
1. Myynti-kohdassa käyttäjä valitsee **hintatilauksen** toimintoruudusta.
1. Salesin tilausrivin hinnat tai alennukset eivät muutu.

## <a name="limitations"></a>Rajoitukset

Kun Salesin sarakkeet on täytetty, seuraavat rajoitukset ovat voimassa:

- Supply Chain Managementin kuluja ja kulujen kohdistuksia ei replikoida Salesiin.
- Hinnoittelu ei ota huomioon erikoisvähittäismyyntihinnoittelua, joka on määritetty **Vähittäismyyntikanava**-sarakkeessa myyntitilausrivisivulla Supply Chain Managementissa.
- Supply Chain Managementin **Myynninedistämispalkkioiden hallinta** -osassa määritettyjä alennuksia ei oteta huomioon.
- Hinnoittelu ei ota huomioon myyntisopimuksia.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
