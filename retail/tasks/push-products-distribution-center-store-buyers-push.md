--- 
title: "Siirrä tuotteita jakelukeskuksesta myymälään käyttäen ostotarjontaa"
description: "Tässä menettelyssä esitellään, miten ostovaatimus luodaan ja miten sitä käsitellään jaettaessa tuotteita yhdestä sijainnista yhteen tai useaan myymälään."
author: rubencdelgado
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b73147d76880714d22db8e95d1369b4a01ddaae6
ms.contentlocale: fi-fi
ms.lasthandoff: 07/28/2017

---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a>Siirrä tuotteita jakelukeskuksesta myymälään käyttäen ostotarjontaa

[!include[task guide banner](../includes/task-guide-banner.md)]

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

