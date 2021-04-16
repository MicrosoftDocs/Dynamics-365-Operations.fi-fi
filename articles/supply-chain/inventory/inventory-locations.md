---
title: Varastosijainnit
description: Varastopaikkoja käytetään perusvarastoinnin (WMS I) kanssa määrittämään, mihin nimikkeet varastoidaan ja mistä nimikkeet poimitaan WMS I -varastossa.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4afbb4847a2d3175585ed270d8ecd8aac33c4b14
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813120"
---
# <a name="inventory-locations"></a>Varastosijainnit

[!include [banner](../includes/banner.md)]

Varastopaikkoja käytetään perusvarastoinnin (WMS I) kanssa määrittämään, mihin nimikkeet varastoidaan ja mistä nimikkeet poimitaan WMS I -varastossa.

Tämä ohjeaihe koskee inventaarionhallintamoduulin ominaisuuksia. Se ei koske varastonhallintamoduulin ominaisuuksia.

Termi sijainti tarkoittaa paikkaa, johon nimikkeet on varastoitu ja josta ne otetaan.

Jokaiselle sijainnille voidaan myös määrittää paikka, johon nimike asetetaan. Oletusarvon mukaan ovat samat. Nimikkeet lisätään ja otetaan tavallisesti sijainnin samalta puolelta, mutta ei kuitenkaan aina. Esimerkiksi nimikkeet, jotka varastoidaan live-tallennustelineisiin, jotka asetetaan yhdeltä käytävältä ja vedetään toiselta. Pääsyöte on sijainnin nimi, joka määritetään tavallisesti koordinaattien perusteella: varasto, käytävä, teline, hylly ja lokero. Tämän nimen tai tunnuksen voi kirjoittaa manuaalisesti, tai sen voi luoda sijaintikoordinaateista; esimerkiksi 01-02-03-4 tarkoittaa käytävää 1, telinettä 2, hyllyä 3 ja lokeroa 4 Varastosijainnit-sivulla.
Varastopaikan ominaisuudet

Varastopaikalla on seuraavat ominaisuudet:
-   Koko (korkeus, leveys, syvyys ja siten tilavuus)
-   Varaston, käytävän, telineen, hyllyn ja lokeron sijainti
-   Varastopaikan tyyppi (bulkkisijainti, keräilysijainti, saapuvien laituri, lähtevien laituri, tuotannon varastoinnin sijainti, tarkastussijainti tai kanban-supermarket)

Online-järjestelmissä voi tarkistaa tarkistustekstin avulla, että operaattori on valinnut nimikkeelle oikean varastopaikan. Tarkistustekstin voi luoda manuaalisesti tai automaattisesti oletusarvon mukaan.

## <a name="sort-codes"></a>Lajittelutunnukset
Lajittelutunnusten avulla voit optimoida keräilyrivien käsittelyn. Keräilyriveissä on nimikkeiden varastosta keräämistä varten tarvittavat tiedot, kuten keräilyjärjestys. Lajittelukoodit voidaan määrittää esimerkiksi käytävittäin, tai manuaalisesti sijainnille.

## <a name="blocked-locations"></a>Varastopaikkojen estot
Joskus varastopaikka on merkittävä suljetuksi joksikin aikaa esimerkiksi korjauksen vuoksi. Joskus taas voi olla tarpeen estää vain nimikkeiden syöttö varastopaikkaan tai kerääminen sieltä.

## <a name="tree-structure"></a>Puurakenne

Varastosijainnit-sivulla voit tarkastella varaston asettelua puurakenteena, joka perustuu varastopaikkojen koordinaatteihin määritellyssä näyttömuodossa.

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a>Varastosijaintien ylläpito varastolomakkeessa

Sijainteja voidaan kopioida varastosta toiseen ja luoda ohjatun toiminnon avulla. Ennen ohjatun toiminnon suorittamista varmista, että olet määrittänyt sijainnin oletusnimet Varasto-sivulla.



<a name="additional-resources"></a>Lisäresurssit
--------

[Luo uusi varastoasettelu](tasks/create-new-warehouse-layout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]