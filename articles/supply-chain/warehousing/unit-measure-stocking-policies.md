---
title: Mittayksikköä ja varastointikäytännöt
description: Tässä artikkelissa kerrotaan, kuinka oletusyksiköitä, yksikön sarjoja ja yksikkömuunnoksia käytetään varastoprosesseissa.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca1c18a293d66ab78f41cac857461249826ce4c9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069119"
---
# <a name="unit-of-measure-and-stocking-policies"></a>Mittayksikköä ja varastointikäytännöt

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, kuinka oletusyksiköitä, yksikön sarjoja ja yksikkömuunnoksia käytetään varastoprosesseissa.

Yksikön sarjaryhmä määrittää varastotoimenpiteissä käytettävän yksiköiden sarjan. Ne luodaan **Yksikön sarjaryhmät** -sivulla. Sarja osoittaa eri yksiköiden välisen suhteen. Esimerkki: Varastoit kuormalavoja, joiden sisältämät laatikot sisältävät yksittäisiä nimikkeitä. Tällöin sinun on syötettävä kolme eri yksikköä ja tasojen looginen järjestys. Yksikön sarjaryhmien avulla voit määritellä rekisterikilpien ryhmittelykäytäntöjä ja oletusyksiköitä, joita eri varastoprosesseissa on käytettävä. Tämä artikkeli koskee sekä varastonhallintamoduulissa käytettäviä varastonhallintaprosesseja (WMS) että inventoinnin- ja varastonhallintamoduulissa käytettävää perustason varastonhallintaratkaisua.

## <a name="unit-sequence-groups-for-released-products"></a>Yksikön sarjaryhmät vapautetuille tuotteille
Jos haluat käyttää vapautettuja tuotteita varaston työprosesseissa, niille täytyy määrittää yksikön sarjaryhmä. Jos vahvistat tuotteen, joka on liitetty johonkin varastodimensioryhmään ja kyseisen varastodimensioryhmän **Käytä varastonhallintaprosesseja** -vaihtoehdoksi on asetettu **Kyllä**, näyttöön tulee virhesanoma, jos yksikön sarjaryhmän tunnusta ei ole määritetty tuotteelle. Jos käyttämässäsi yksikön numerosarjaryhmässä on useita rivejä (ja siten useita yksiköitä), yksiköiden välille on määritettävä yksikkömuunnos. Tämän asetuksen voi tehdä **Yksikkömuunnokset**-sivulla. Vapautettuun tuotteeseen liitettävän sarjaryhmän pienimmän yksikön on täsmättävä vastaavalle tuotteelle määritetyn varastoyksikön kanssa. Varastoyksikkö on yksikkö, jota käytetään käytettävissä olevan varaston peruslaskutoimituksissa. Voit myös määrittää mittayksikkömuunnokset päätuotteiden tuotevarianteille käyttämällä **Ota käyttöön mittayksiköiden muunnokset** -vaihtoehtoa.

## <a name="license-plate-grouping"></a>Rekisterikilpiryhmitys
Voit määrittää, ryhmitelläänkö tiettyä yksikköä pienemmät tai suuremmat vastaanotot yhdeksi rekisterikilveksi vai jaetaanko ne yksikkökohtaisille rekisterikilville. Voit määrittää tämän käyttämällä **Yksikön sarjaryhmät** -sivun **Rivin erittely** -välilehden **Rekisterikilpiryhmitys**-vaihtoehtoa. Jos haluat käyttää rekisterikilpiryhmittelyä, kun työ käsitellään mobiililaitteella, sinun on valittava **Mobiililaite**-valikkovaihtoehdolle **Rekisterikilpiryhmitys**-vaihtoehto. Esimerkki: Rekisteröit mobiililaitteella nimikettä, joka on liitetty kaksi riviä sisältävään yksikön sarjaryhmään. Ensimmäinen rivi koskee kappaleita, ja **Rekisterikilpiryhmittely**-asetuksena on **Kyllä**. Toinen rivi koskee kuormalavayksikköä, ja **Rekisterikilpiryhmittely**-asetuksena on **Ei**. Tällöin järjestelmä voi ohjata jakoa ja rekisterikilpien luontia 100 kappaleen erinä automaattisesti.

## <a name="units-for-cycle-counting"></a>Inventoinnin yksiköt
Voit määrittää inventointiprosesseissa käytettävät yksiköt valitsemalla **Yksikön sarjaryhmät** -sivulta **Käytä yksikköä inventointiin** -asetuksen. Voit valita enintään neljä yksikköä samaan sarjaryhmään. Jos valitset yli neljä yksikköä, lisäyksiköitä ei näytetä mobiililaitteessa.

## <a name="default-units-for-mobile-device-receiving-processes"></a>Mobiililaitteen vastaanottoprosessien oletusyksiköt
Jos haluat määrittää oletusyksiköt mobiililaitteilla tapahtuvia vastaanottoprosesseja varten, ota **Yksikön sarjaryhmät** -sivulla käyttöön **Oston ja siirron oletusyksikkö**- ja **Tuotannon oletusyksikkö** -vaihtoehdot. Voit esimerkiksi määrittää, että järjestelmä käyttää oletusarvon mukaan kuormalavojen määrää, kun ostotilauksen käytettävissä oleva varasto vastaanotetaan mobiililaitteella, mutta varastoyksikkönä on oltava kappale. Voit muuntaa kunkin kuormalavan sisältämän kappalemäärän määrittämällä yksikkömuunnoksen, esimerkiksi 100 kpl = 1 KL.

## <a name="default-order-settings"></a>Tilauksen oletusasetukset
Vapautettuja tuotteita luodessasi sinun täytyy valita oletusyksiköt ostoille, myynneille ja varastolle eri tilausten käsittelyä varten. Voit määrittää oletusyksiköt ja määrät eri lähdeasiakirjoille **Tilauksen oletusasetukset**- ja **Toimipaikkakohtaiset tilausasetukset** -sivuilla. Voit avata nämä sivut **Vapautetut tuotteet** -sivulta.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]