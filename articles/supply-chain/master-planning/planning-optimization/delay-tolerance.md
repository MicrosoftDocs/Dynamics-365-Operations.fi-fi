---
title: Viivetoleranssi (negatiiviset päivät)
description: Tässä ohjeaiheessa on tietoja viivetoleranssin laskennasta ja siitä, miten se vaikuttaa suunnitellun tilauksen luontiin suunnittelun optimoinnissa.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306460"
---
# <a name="delay-tolerance-negative-days"></a>Viivetoleranssi (negatiiviset päivät)

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Viivetoleranssitoiminnon ansiosta suunnittelun optimointi voi ottaa huomioon kattavuusryhmille määritetyn **negatiivisten päivien** arvon. Sitä käytetään pääsuunnittelussa käytetyn viivetoleranssikauden pidennykseen. Näin voidaan välttää uusien toimitustilausten luominen, jos olemassa oleva toimitus voi kattaa kysynnän lyhyen viiveen jälkeen. Toiminnon tarkoitus on määrittää, onko tarpeen luoda uusi toimitustilaus annettua kysyntää varten.

## <a name="turn-on-the-feature-in-your-system"></a>Toiminnon ottaminen käyttöön järjestelmässä

Voit ottaa viivetoleranssin toiminnon käyttöön järjestelmässäsi valitsemalla [Ominaisuuksien hallinta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ottamalla *Suunnittelun optimoinnin negatiiviset päivät* -ominaisuuden käyttöön.

## <a name="delay-tolerance-in-planning-optimization"></a>Suunnittelun optimoinnin viivetoleranssi

Viivetoleranssi tarkoittaa läpimenoajan ylittävän päivien määrää, jonka olet valmis odottamaan ennen uuden täydennyksen tilaamista, kun olemassa oleva toimitus on jo suunniteltu. Viivetoleranssi määritetään käyttämällä kalenteripäiviä, ei työpäiviä.

Kun pääsuunnittelun aikana järjestelmä laskee viivetoleranssin, se ottaa huomioon **negatiivisten päivien** asetuksen. Voit määrittää **Negatiiviset päivät** -arvon joko **Kattavuusryhmät**- tai **Nimikkeen kattavuus** -sivuilla.

Järjestelmä linkittää viivetoleranssin laskennan *aikaisimpaan täydennyspäivämäärään*, joka on sama kuin tämän päivän päivämäärä plus läpimenoaika. Viivetoleranssi lasketaan seuraavan kaavan avulla, jossa *max()* hakee suuremman kahdesta arvosta:

*max(aikaisin täydennyspäivämäärä, kysynnän määräpäivä)* – *kysynnän määräpäivä* + *Negatiiviset päivät*

Tällä kaavalla varmistetaan, että pääsuunnittelu ei luo uusia toimitustilauksia, kun toimituksia on tarpeeksi olemassa tuotteen läpimenoajan aikana.

> [!NOTE]
> Suunnittelun optimoinnin viivetoleranssin laskenta käyttää aina sisäänrakennetun pääsuunnittelun dynaamista negatiivisten päivien laskentaa. **Käytä dynaamisia negatiivisia päiviä** -asetus **Pääsuunnittelun parametrit** -sivulla ei vaikuta tähän käyttäytymiseen.

Jos nykyinen toimitus merkitsee kysynnän viivettä, joka on pienempi tai yhtä suuri kuin laskettu viivetoleranssi, suunnittelun optimointi sovittaa olemassa olevan toimituksen ja kysynnän. Joissain tapauksissa on parempi viivyttää kysyntää kuin päätyä ylitarjontaan.

Seuraavissa osa-alueissa on esimerkkejä, jotka osoittavat, kuinka viivetoleranssi vaikuttaa suunniteltujen tilausten luontiin suunnittelun optimoinnissa.

### <a name="example-1"></a>Esimerkki 1

Tuotteella on seuraava konfiguraatio:

- **Läpimenoaika:** *10*
- **Negatiiviset päivät:** *2*

Tuotteella on seuraava tarjonta ja kysyntä:

- **Tämän päivän kysyntä:** myyntitilaus, jonka määrä on 10
- **Toimitus 12 päivän sisällä:** ostotilaus, jonka määrä on 10

Olemassa oleva tarjonta voi kattaa kysynnän 12 päivän kuluessa ja että kausi on sama kuin viivetoleranssi. Näin ollen pääsuunnittelun ajossa ei luoda suunniteltuja tilauksia.

### <a name="example-2"></a>Esimerkki 2

Tuotteella on seuraava konfiguraatio:

- **Läpimenoaika:** *10*
- **Negatiiviset päivät:** *0*

Tuotteella on seuraava tarjonta ja kysyntä:

- **Tämän päivän kysyntä:** myyntitilaus, jonka määrä on 10
- **Toimitus 12 päivän sisällä:** ostotilaus, jonka määrä on 10

Olemassa oleva tarjonta voi kattaa kysynnän vain 12 päivän kuluttua. Viivetoleranssi on kuitenkin 10 päivää. Näin ollen pääsuunnittelun ajossa luodaan suunniteltu tilaus, jonka määrä on 10.

### <a name="example-3"></a>Esimerkki 3

Tuotteella on seuraava konfiguraatio:

- **Läpimenoaika:** *10*
- **Negatiiviset päivät:** *2*

Tuotteella on seuraava tarjonta ja kysyntä:

- **Kysyntä 11 päivän aikana:** myyntitilaus, jonka määrä on 10
- **Toimitus 14 päivän sisällä:** ostotilaus, jonka määrä on 10

Olemassa oleva tarjonta voi kattaa kysynnän vain kolmen päivän kuluttua. Viivetoleranssi on kuitenkin kaksi päivää. (Tässä tapauksessa viivetoleranssi sisältää vain kaksi negatiivista päivää. Kysyntäpäivämäärää ei sisällytetä, koska se on tuotteen läpimenoajan jälkeen.) Näin ollen pääsuunnittelun ajossa luodaan suunniteltu tilaus, jonka määrä on 10.
