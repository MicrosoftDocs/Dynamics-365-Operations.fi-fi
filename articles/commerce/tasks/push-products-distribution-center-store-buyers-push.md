---
title: Siirrä tuotteita jakelukeskuksesta myymälään käyttäen ostotarjontaa
description: Tässä menettelyssä esitellään, miten ostovaatimus luodaan ja miten sitä käsitellään jaettaessa tuotteita yhdestä sijainnista yhteen tai useaan myymälään.
author: BrianShook
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 30d82e4b282bac2ea888971ad5c6298adfa8332b
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779617"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a>Siirrä tuotteita jakelukeskuksesta myymälään käyttäen ostotarjontaa

[!include [banner](../includes/banner.md)]

Tässä menettelyssä esitellään, miten ostovaatimus luodaan ja miten sitä käsitellään jaettaessa tuotteita yhdestä sijainnista yhteen tai useaan myymälään. Käyttäjä voi määrittää useita konfiguraatioita. Järjestelmä voi ehdottaa, miten tuotteet jaellaan, tai käyttäjä voi syöttää manuaalisesti, minne tuotteet jaellaan ja miten paljon kuhunkin myymälään tuotteita siirtyy. Menettely ei sisällä tietojen asetuksia, joita ostovaatimuksessa voi käyttää, kuten täydennyssääntöjä, organisaatiohierarkioita ja myymälän painoja. Näissä toimintaohjeissa käytetään esittely-yritystä USRT.

1. Siirry Ostovaatimus-kohtaan.
2. Valitse Uusi.
3. Kirjoita arvo Kuvaus-kenttään.
4. Syötä tai valitse arvo Toimipaikka-kenttään.
5. Syötä tai valitse Varasto-kenttään varasto, joka sisältää tuotteita, joilla on käytettävissä olevia määriä.
6. ValitseLisää.
7. Merkitse valittu rivi luettelossa.
8. Syötä tai valitse tuote Nimiketunnus-kentässä.
9. ValitseLisää.
10. Merkitse valittu rivi luettelossa.
11. Syötä tai valitse tuotevariantti Nimiketunnus-kentässä.
    * Kun tuotevariantti syötetään, jokaiselle variantille luodaan rivit.  
12. Merkitse rivi luettelossa.
13. Määritä Siirretty määrä -kenttään, miten monta valittua tuotetta haluat jaella.
14. Syötä Siirrettävä lisämäärä -kenttään niiden tuotteiden määrä, joilla on jaettavaa käytettävissä olevaa määrää.
15. Syötä Jakelu-kenttään Sijaintipaino.
    * Voit valita muita tyyppejä jakelun eri säännöille.  
16. Syötä tai valitse arvo Täydennyshierarkia-kentässä.
17. Valitse Ota valikoimat huomioon -kentässä Kyllä.
18. Valitse Laske määrät ja tarkista, että määrät on lisätty Varasto-osan riveille.
19. Valitse Luo tilaus.
20. Valitse Kyllä.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]