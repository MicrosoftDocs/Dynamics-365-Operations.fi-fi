---
title: Luo valmistuksen vakiomäärän kanban-sääntö
description: Tässä menettelyssä käsitellään määrityksiä, joita tarvitaan luotaessa kiinteää valmistuksen kanban-sääntöä, jolla käynnistetään muuntotehtävät Lean-ympäristön työsolussa.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 540df772f132f60c9d8e7e937e72d3f51f6759ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255250"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a>Luo valmistuksen vakiomäärän kanban-sääntö

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään määrityksiä, joita tarvitaan luotaessa kiinteää valmistuksen kanban-sääntöä, jolla käynnistetään muuntotehtävät Lean-ympäristön työsolussa. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Menettely on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun tuotteen tuotannon valmisteluun.


## <a name="create-new-kanban-rule"></a>Luo uusi kanban-sääntö
1. Valitse Kanban-säännöt.
2. Valitse Uusi.
    * Huomaa, että oletustyyppi on Valmistus ja Täydennysstrategia on Kiinteä. Näitä parametreja ei tarvitse muuttaa.  
3. Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.
    * Tämä tehtävä tehdään tämän kanban-säännön perusteella luoduissa kanbaneissa.  Valitse SpeakerTestAndPackaging.  
4. Laajenna Tiedot-osa.
5. Anna tai valitse Tuote-kentässä arvo.
    * Valitse L0050.  
6. Anna tai valitse Mittayksikkö-kentässä arvo.
    * Valitse minuutit.  
7. Lisää Läpimenoaika-kenttään numero.
    * Anna 5.  

## <a name="set-quantities"></a>Määritä määrät
1. Laajenna Määrät-osa.
2. Määritä Oletusmäärä-arvoksi 10.
    * Tämä määrä siirretään kullekin kanbanille.  
3. Valitse Tuotemäärän varianssi -valintaruutu.
    * Valitut kanbanit voidaan toteuttaa tämän avulla oletusmäärän varianssilla.  Jotta kanbanit voitaisiin toteuttaa määrällä 8–12, määritä molempien varianssien arvoksi 2.  
4. Määritä Poikkeaman alla -arvoksi 2.
    * Tällöin myös pienempi toteutus on mahdollinen 10–2=8  
5. Määritä Poikkeaman yllä -arvoksi 2.
    * Tällöin myös suurempi toteutus on mahdollinen 10+2=12  
6. Lisää Kiinteä kanban-määrä -kenttään numero.
    * Tämä on sellaisten kanbanien määrä, joiden pitäisi olla aktiivisia. Tällä tapauksessa jokainen 5 kanbanista käsittelee 10.  
7. Lisää Vähimmäisrajan hälytys -kenttään 2.
    * Käytetään seuraamaan sellaisten täysien kanbanien vähimmäismäärää, joiden pitäisi olla päämäärässä. Tätä käytetään esimerkiksi kanban-määrän yhteenvedossa.  
8. Lisää Enimmäisrajan hälytys -kenttään 4.
    * Käytetään seuraamaan sellaisten täysien kanbanien enimmäismäärää, joiden pitäisi olla päämäärässä. Tätä käytetään esimerkiksi kanban-määrän yhteenvedossa.  
9. Lisää Automaattisen suunnittelun määrä -kenttään 1.
    * Kun arvoksi on määritetty 1, jokainen kanban suunnitellaan automaattisesti.   Jos arvoksi annetaan 3, kanbaneja ei suunnitella, ennen kuin 3 tyhjää kanbania on valmiita suunnitteluun. Tämä on kätevää töiden ryhmittelyssä, ja sillä vältetään liialliset asetukset.  

## <a name="create-kanbans"></a>Luo kanbaneita
1. Laajenna Kanbanit-osa.
2. Valitse Tallenna.
    * Kanban-sääntö on tallennettava ennen kanbanien luomista.  
3. ValitseLisää.
    * Huomaa, että yksikään kanban ei ole aktiivinen, minkä vuoksi ehdotettu uusien kanbanien määrä on 5. Tämä vastaa Kiinteä kanban-määrä -asetusta.  
4. Valitse Luo.
    * Tämä luo 5 kanbania.  
    * Huomaa, että tälle valmistuksen kanban-säännölle luotiin 5 kanbania, joista kunkin arvo on 10. Tämä on tämän menettelyn viimeinen vaihe.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]