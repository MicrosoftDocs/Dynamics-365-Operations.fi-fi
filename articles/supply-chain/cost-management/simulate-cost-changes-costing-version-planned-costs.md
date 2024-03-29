---
title: Kustannusmuutosten simuloiminen suunniteltujen kustannusten kustannuslaskelmaversiota käyttäen
description: Tässä artikkelissa kerrotaan, miten valmistettavan nimikkeen laskettujen kustannusten muuttuvien kustannusten vaikutuksen voi simuloida käyttämällä erillistä suunniteltujen kustannusten kustannuslaskelmaversiota.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ad3d6bd41e090b13f48ecc7bb19faae5dbc8502
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676175"
---
# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a>Kustannusmuutosten simuloiminen suunniteltujen kustannusten kustannuslaskelmaversiota käyttäen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten valmistettavan nimikkeen laskettujen kustannusten muuttuvien kustannusten vaikutuksen voi simuloida käyttämällä erillistä suunniteltujen kustannusten kustannuslaskelmaversiota.

Valmistettavan nimikkeen laskettujen kustannusten muuttuvien kustannusten vaikutuksen voi simuloida käyttämällä erillistä suunniteltujen kustannusten kustannuslaskelmaversiota. Tämän erillisen kustannuslaskelmaversion avulla voit lisätä kustannusten lisämuutoksia ilmentävät odottavat kustannustietueet ja laskea kustannusmuutosten vaikutuksen valmistettavien tuotteiden kustannuksiin. Koska tuoterakennelaskelmissa käytetään aktiivisten kustannusten varmistusperiaatteita, vain kustannusten lisämuutokset on lisättävä.

## <a name="guidelines-for-defining-the-simulation-costing-version"></a>Simulaation kustannuslaskelmaversion määrittämisen ohjeet
Voit määrittää simulaation kustannuslaskelmaversion seuraavien ohjeiden avulla:

-   Määritä **suunniteltujen kustannusten** kustannuslaskelmatyyppi.
-   Määritä kustannuslaskelmaversiolle mielekäs tunnus. Tällainen tunnus voi olla esimerkiksi **Simulointi**.
-   Varmista, että kustannustietueet kuuluvat sisältöön.
-   Salli kustannustietueiden lisääminen. Älä estä odottavien kustannusten lisäämistä.
-   Salli kustannustietueiden lisääminen kaikille toimipaikoille. Jos määrität toimipaikan, voit lisätä vain tämän toimipaikan kustannustietueita.
-   Estä odottavien kustannusten aktivointi. Simuloidun kustannuslaskelmaversion kustannustietueisiin on syötettävä vain odottavat kustannukset.
-   Älä syötä alkamispäivämäärää. Jokaiselle simuloitua kustannuslaskelmaversiota käyttävälle tuoterakennelaskelmalle lisätään laskentapäivä.
-   Määritä **nykyisen aktiivisen** varmistuskäytäntö. Varmistuskäytäntö sallii kustannusten lisämuutosten lisäämisen simulointitarkoituksessa. Kaikkien muiden kustannustietueiden lähteenä ovat kuitenkin nykyiset aktiiviset kustannukset. Kaikilla muilla kustannustietueilla oletetaan olevan kaikki nykyiset aktiiviset kustannukset.
-   Määritä **version kustannushinnan** kustannushintamalli, mutta älä aseta laskutoimituksille rajoituksia. Simuloinneissa voidaan myös esimerkiksi käyttää **tuoterakennelaskelmaryhmän** kustannushintamallia osoittamaan ostettujen nimikkeiden kulujen osuutta koskevien tietojen lähde.
-   Määritä **monitasoinen** hajotustila, mutta älä aseta laskutoimituksille rajoituksia. Simulaatioissa voidaan käyttää muita hajotustiloja.

## <a name="costing-versions"></a>Kustannuslaskentaversiot
Seuraavissa tilanteissa havainnollistetaan, kuinka kustannusten muutosten vaikutuksia simuloidaan kustannuslaskelmaversion avulla. Poista kustannuslaskelmaversion odottavat kustannustietueet ennen simuloidun kustannusmuutoksen lisäämistä, jotta voit aloittaa alusta. **Nimikkeen hinta** -sivun avulla voit tarkastella ja poistaa odottavia kustannustietueita, jotka liittyvät nimikkeiden kustannuksiin ja kustannusluokan hintoihin.

-   Simuloi muutos ostetun nimikkeen kustannuksissa. Kustannusten muutos voi esimerkiksi olla merkki välttämättömien ostettavien materiaalien hinnan odotetusta suurenemisesta tai pienenemisestä. Voit määrittää ostetulle nimikkeelle eri kustannukset syöttämällä odottavan kustannustietueen **Nimikkeen hinta** -sivun avulla simuloidussa kustannuslaskelmaversiossa.
-   Simuloi muutos kustannusluokan kustannuksissa. Kustannusmuutokset voivat esimerkiksi olla merkki työkustannusten tai operatiivisten resurssien tuntipalkkojen odotetusta suurenemisesta tai pienenemisestä. Voit määrittää kustannusluokalle eri kustannukset lisäämällä odottavan kustannustietueen **Kustannusluokan hinta** -sivun avulla simuloidussa kustannuslaskelmaversiossa.
-   Simuloi kustannusten muutos epäsuoraan kustannuslaskentakaavaan. Kustannusten muutokset voivat esimerkiksi olla merkki valmistuksen yleiskustannusten odotetusta suurenemisesta tai pienenemisestä. Voit määrittää muutoksen epäsuoraan kustannuslaskentakaavaan lisäämällä odottavan kustannustietueen **Kustannuslaskennan määritys** -sivun avulla simuloidussa kustannuslaskelmaversiossa sekä vahvistamalla ja tallentamalla muutoksen.

Kun olet syöttänyt simuloidut kustannusmuutokset, laske niiden valmistettujen nimikkeiden kustannukset, joihin kustannuksen muutokset vaikuttavat. Käytä **Laskelma**-sivua simuloidussa kustannuslaskelmaversiossa ja määritä valitut valmistetut nimikkeet, joihin kustannusten muutokset vaikuttavat. Tuoterakennelaskelmat koskevat kaikkia valmistettuja nimikkeitä, jos valittuja nimikkeitä ei erikseen valita. Voit käyttää tuoterakennelaskelmaa myös käyttökohteen päivityksissä. Tarkastele nimikkeen kustannustietueita simuloidussa kustannusversiossa, kun haluat analysoida simuloitujen kustannusmuutosten vaikutuksen valittujen, valmistettujen nimikkeiden kustannuksiin. Käytä **Nimikkeen hinta**- ja **Lasken nimikekustannus** -sivua kustannusten tarkastelemiseen ja analysointiin.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]