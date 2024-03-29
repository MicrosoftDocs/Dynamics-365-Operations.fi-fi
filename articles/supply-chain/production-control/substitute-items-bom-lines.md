---
title: Materiaalien korvaaminen tuotannossa
description: Tässä artikkelissa kuvataan, miten materiaaleja voi korvata tuotantoprosessin aikana.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c2e6c9cc8ed85c8c60539b37fb6c51c96bc2872
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855975"
---
# <a name="material-substitution-in-manufacturing"></a>Materiaalien korvaaminen tuotannossa

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten materiaaleja voi korvata tuotantoprosessin aikana. 

Materiaaleja voidaan korvata tuotantoprosessin aikana kolmella tavalla:

-   Päivämäärän mukaan, kun materiaali korvataan toisella tietyn päivämäärän jälkeen
-   Pääsuunnittelun aikana, kun kaavassa oleva materiaali on loppunut varastosta ja korvataan eri materiaalilla
-   Tuotannon aikana, kun materiaali on odottamatta loppunut varastosta ja korvataan eri materiaalilla.

## <a name="substituting-material-by-date"></a>Materiaalin korvaaminen päivämäärän mukaan
Skenaario: yrityksen valmistama laite sisältää komponentin, joka poistuu toimittajan tuoteluettelosta kahden kuukauden kuluttua. Poistumispäivän jälkeen toimittaja tarjoaa uutta komponenttia, joka korvaa vanhan. Voimassaolon alkamis- ja päättymispäivät voidaan määrittää tuoterakenneriveille. Tässä esimerkissä vanha komponentti määritetään vanhenemaan syöttämällä vanhentumispäivä **Päivämäärään**-kenttään. Tämän jälkeen tuoterakenteessa määritetään uusi korvaava komponentti niin, että se on voimassa vanhan komponentin vanhentumispäivästä lähtien. Syötä tällöin alkamispäivä **Päivämäärästä**-kenttään.

## <a name="substituting-material-by-planning"></a>Materiaalin korvaaminen suunnittelun mukaan
Materiaaleja voi korvata suunnittelun aikana vain käytettäessä kaavoja, ei tuoterakennetta. Skenaario: elintarvikeyritys valmistaa kastiketta reseptillä, joka sisältää 20 ainesosaa. Kaavan yksi ainesosa voidaan korvata jommallakummalla kahdesta muusta ainesosasta. Koska nämä kaksi ainesosaa ovat kuitenkin kalliimpia kuin ensisijainen ainesosa, korvausta käytetään ainoastaan silloin, kun ensisijaista ainesosaa ei ole varastossa. Korvattavaa materiaalia kutsutaan A:ksi ja korvaavia kahta materiaalia B:ksi ja C:ksi. Materiaalin korvaaminen suunnittelun mukaan määritetään reseptirivien **Suunnitteluryhmä**- ja **Prioriteetti**-kentissä. Tässä esimerkissä kolmelle materiaalille luodaan reseptirivit, jotka liitetään samaan suunnitteluryhmään. Materiaalin A reseptirivillä on suurin prioriteetti (pienin numero), materiaalin C reseptirivillä pienin prioriteetti ja materiaalin B reseptirivin prioriteetti on niiden välillä. Jos valmiille nimikkeelle on kysyntää, pääsuunnittelussa määritetään ensin, voidaanko materiaalin A tarve voidaan kattaa. Jos kysyntää ei voida kattaa, pääsuunnittelussa etsitään materiaaleja B ja C prioriteettijärjestyksessä. Jos materiaalia B on käytettävissä, sitä käytetään, kun suunniteltu erätilauksen on vahvistettu reseptille. Jos mitään materiaalia ei ole käytettävissä, pääsuunnittelu luo suunnitellun tilauksen materiaalille A. **Huomautus:** kun määrität reseptirivejä suunnitteluryhmässä, sinun on määritettävä määrä vain materiaalille, jolla on suurin prioriteetti. Tätä määrää käytetään laskettaessa suunnitelman sisältämien kaikkien materiaalien kysyntää, myös sellaisten materiaalien, joiden prioriteetti on pienin. Eri määriä ei voi määrittää niille suunnitteluryhmän nimikkeille, joiden prioriteetti on pienempi.

## <a name="substituting-material-during-production"></a>Materiaalin korvaaminen tuotannon aikana
Skenaario: hitsaustyössä tarvitaan metallilevyn palasta. Varastotyöntekijä ilmoittaa työn aikana koneenkäyttäjälle, että levyä ei ole varastossa. Tällöin päätetään, että levy voidaan korvata hieman paksummalla levyllä. Näin työ saadaan valmiiksi. Materiaali voidaan lisätä avoimen tuotantotilauksen tuoterakenteeseen. Jos tuotantotilauksen tila on **Aloitettu**, käyttäjiä pyydetään arvioimaan tilaus uudelleen, kun he lisäävät tuotannon tuoterakenteeseen uuden nimikkeen. Materiaalin lisäämisen jälkeen uudelle nimikkeelle voidaan luoda uusi keräysluettelo. Uutta materiaalia ei tarvitse lisätä tuotannon tuoterakenteeseen. Sen voi sen sijaan lisätä suoraan tuotannon keräysluetteloon. Kun keräysluettelo sitten kirjataan, järjestelmä lisää materiaalin tuotannon tuoterakenteeseen.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]