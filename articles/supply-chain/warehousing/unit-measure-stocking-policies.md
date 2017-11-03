---
title: "Mittayksikköä ja varastointikäytännöt"
description: "Tässä artikkelissa kerrotaan, kuinka oletusyksiköitä, yksikön sarjoja ja yksikkömuunnoksia käytetään varastoprosesseissa."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 80bd5978ffe137e48da3f5eac6c75ad0f5e2f06a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# Mittayksikköä ja varastointikäytännöt

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, kuinka oletusyksiköitä, yksikön sarjoja ja yksikkömuunnoksia käytetään varastoprosesseissa.

Yksikön sarjaryhmä määrittää varastotoimenpiteissä käytettävän yksiköiden sarjan. Ne luodaan **Yksikön sarjaryhmät** -sivulla. Sarja osoittaa eri yksiköiden välisen suhteen. Esimerkki: Varastoit kuormalavoja, joiden sisältämät laatikot sisältävät yksittäisiä nimikkeitä. Tällöin sinun on syötettävä kolme eri yksikköä ja tasojen looginen järjestys. Yksikön sarjaryhmien avulla voit määritellä rekisterikilpien ryhmittelykäytäntöjä ja oletusyksiköitä, joita eri varastoprosesseissa on käytettävä. Tämä artikkeli koskee sekä varastonhallinnassa käytettävää edistyksellistä varastonhallintaratkaisua että inventaarionhallinnassa käytettävää perustason varastonhallintaratkaisua.

## Yksikön sarjaryhmät vapautetuille tuotteille
Jos haluat käyttää vapautettuja tuotteita varaston työprosesseissa, niille täytyy määrittää yksikön sarjaryhmä. Jos vahvistat tuotteen, joka on liitetty johonkin varastodimensioryhmään ja kyseisen varastodimensioryhmän **Käytä varastonhallintaprosesseja** -vaihtoehdoksi on asetettu **Kyllä**, näyttöön tulee virhesanoma, jos yksikön sarjaryhmän tunnusta ei ole määritetty tuotteelle. Jos käyttämässäsi yksikön numerosarjaryhmässä on useita rivejä (ja siten useita yksiköitä), yksiköiden välille on määritettävä yksikkömuunnos. Tämän asetuksen voi tehdä **Yksikkömuunnokset**-sivulla. Vapautettuun tuotteeseen liitettävän sarjaryhmän pienimmän yksikön on täsmättävä vastaavalle tuotteelle määritetyn varastoyksikön kanssa. Varastoyksikkö on yksikkö, jota käytetään käytettävissä olevan varaston peruslaskutoimituksissa. Voit myös määrittää mittayksikkömuunnokset päätuotteiden tuotevarianteille käyttämällä **Ota käyttöön mittayksiköiden muunnokset** -vaihtoehtoa.

## Rekisterikilpiryhmitys
Voit määrittää, ryhmitelläänkö tiettyä yksikköä pienemmät tai suuremmat vastaanotot yhdeksi rekisterikilveksi vai jaetaanko ne yksikkökohtaisille rekisterikilville. Voit määrittää tämän käyttämällä **Yksikön sarjaryhmät** -sivun **Rivin erittely** -välilehden **Rekisterikilpiryhmitys**-vaihtoehtoa. Jos haluat käyttää rekisterikilpiryhmittelyä, kun työ käsitellään mobiililaitteella, sinun on valittava **Mobiililaite**-valikkovaihtoehdolle **Rekisterikilpiryhmitys**-vaihtoehto. Esimerkki: Rekisteröit mobiililaitteella nimikettä, joka on liitetty kaksi riviä sisältävään yksikön sarjaryhmään. Ensimmäinen rivi koskee kappaleita, ja **Rekisterikilpiryhmittely**-asetuksena on **Kyllä**. Toinen rivi koskee kuormalavayksikköä, ja **Rekisterikilpiryhmittely**-asetuksena on **Ei**. Tällöin järjestelmä voi ohjata jakoa ja rekisterikilpien luontia 100 kappaleen erinä automaattisesti.

## Inventoinnin yksiköt
Voit määrittää inventointiprosesseissa käytettävät yksiköt valitsemalla **Yksikön sarjaryhmät** -sivulta **Käytä yksikköä inventointiin** -asetuksen. Voit valita enintään neljä yksikköä samaan sarjaryhmään. Jos valitset yli neljä yksikköä, lisäyksiköitä ei näytetä mobiililaitteessa.

## Mobiililaitteen vastaanottoprosessien oletusyksiköt
Jos haluat määrittää oletusyksiköt mobiililaitteilla tapahtuvia vastaanottoprosesseja varten, ota **Yksikön sarjaryhmät** -sivulla käyttöön **Oston ja siirron oletusyksikkö**- ja **Tuotannon oletusyksikkö** -vaihtoehdot. Voit esimerkiksi määrittää, että järjestelmä käyttää oletusarvon mukaan kuormalavojen määrää, kun ostotilauksen käytettävissä oleva varasto vastaanotetaan mobiililaitteella, mutta varastoyksikkönä on oltava kappale. Voit muuntaa kunkin kuormalavan sisältämän kappalemäärän määrittämällä yksikkömuunnoksen, esimerkiksi 100 kpl = 1 KL.

## Tilauksen oletusasetukset
Vapautettuja tuotteita luodessasi sinun täytyy valita oletusyksiköt ostoille, myynneille ja varastolle eri tilausten käsittelyä varten. Voit määrittää oletusyksiköt ja määrät eri lähdeasiakirjoille **Tilauksen oletusasetukset**- ja **Toimipaikkakohtaiset tilausasetukset** -sivuilla. Voit avata nämä sivut **Vapautetut tuotteet** -sivulta.




