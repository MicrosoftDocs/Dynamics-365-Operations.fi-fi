---
title: Tuotteiden cross-docking vastaanottaessa varastosta myymälöihin
description: Tässä menettelyssä esitellään, miten cross docking luodaan ja miten sitä käsitellään jaettaessa tuotteita ostotilauksen vastaanottosijainnista yhteen tai useaan myymälään.
author: ShylaThompson
manager: tfehr
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPushPerPackage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 033d4f72b626130c144faff30fe0d35349b26c6d
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015869"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a>Tuotteiden cross-docking vastaanottaessa varastosta myymälöihin

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä esitellään, miten cross docking luodaan ja miten sitä käsitellään jaettaessa tuotteita ostotilauksen vastaanottosijainnista yhteen tai useaan myymälään. Käyttäjä voi määrittää useita konfiguraatioita. Järjestelmä voi ehdottaa, miten tuotteet jaellaan, tai käyttäjä voi syöttää manuaalisesti, minne tuotteet jaellaan ja miten paljon kuhunkin myymälään tuotteita siirtyy. Menettely ei sisällä tietojen asetuksia, joita cross dockingissa voi käyttää, kuten täydennyssääntöjä, organisaatiohierarkioita ja myymälän painoja. Menettelyssä käytetään esittely-yritystä USRT.

1. Siirry Kaikki ostotilaukset -kohtaan.
2. Valitse luettelosta ostotilaus ja avaa sitten tilaus valitsemalla linkki.
3. Valitse toimintoruudussa Retail ja Commerce.
4. Valitse Cross docking.
5. Valitse Muokkaa.
    * Luokkaa voidaan käyttää Rivit-osan nimikkeiden suodattamisessa.  
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Syötä Cross docking -määrä -kenttään arvo, joka määrittää, miten suuri osa valitun tuotteen ostetusta määrästä jaellaan.
8. Syötä Cross docking -lisämäärä -kenttään arvo, joka määrittää käytettävissä olevien ostettavien tuotteiden jaettavan määrän
9. Syötä Jakelu-kenttään Sijaintipaino.
    * Voit valita muita tyyppejä jakelun eri säännöille.  
10. Syötä tai valitse arvo Täydennyshierarkia-kentässä.
11. Valitse Ota valikoimat huomioon -kentässä Kyllä.
12. Valitse Laske määrät.
13. Valitse Luo tilaus.
14. Valitse Kyllä.
15. Etsi ja valitse luettelosta tuotteet vastaanottava varasto
16. Valitse Tilaus, kun haluat tarkastella valitussa varastossa luotuja tilauksia

