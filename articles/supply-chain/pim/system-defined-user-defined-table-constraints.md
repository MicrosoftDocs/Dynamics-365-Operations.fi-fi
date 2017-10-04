---
title: "Järjestelmän ja käyttäjän määrittämät taulurajoitukset"
description: "Tässä artikkelissa kuvataan käyttäjän ja järjestelmän määrittämiä taulurajoituksia tuotemääritysmallin komponenteille. Taulurajoitukset edustavat sallittujen määriteyhdistelmien matriiseja, joissa kukin rivi määrittää yhden mahdollisten määritearvojen joukon."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4b1d70a446bb4255375a36393778fe2ee6d6fa4e
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017

---

# <a name="system-defined-and-user-defined-table-constraints"></a>Järjestelmän ja käyttäjän määrittämät taulurajoitukset

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan käyttäjän ja järjestelmän määrittämiä taulurajoituksia tuotemääritysmallin komponenteille. Taulurajoitukset edustavat sallittujen määriteyhdistelmien matriiseja, joissa kukin rivi määrittää yhden mahdollisten määritearvojen joukon.

Taulurajoitukset ovat matriiseja komponenteille tuotemääritysmallissa sallittujen määritteiden yhdistelmistä. Taulun kukin rivi määrittää yhden mahdollisten määritearvojen joukon. Tuotemääritysmallissa voi määrittää kahdentyyppisiä rajoituksia:

-   **Lausekerajoitus** – Luo lauseke, joka määrittää määritteiden väliset suhteet niin, että tuotetta määritettäessä voidaan valita vain yhteensopivia arvoja.
-   **Taulurajoitus** – Luo taulu, joka määrittää kaikki tietylle määritejoukolle sallitut yhdistelmät. Käytettävissä on kahdenlaisia taulurajoituksia: käyttäjän määrittämiä ja järjestelmän määrittämiä.

Tässä artikkelissa on kuvattu käyttäjän ja järjestelmän määrittämiä taulurajoituksia tuotemääritysmallin komponenteille.

## <a name="user-defined-table-constraints"></a>Käyttäjän määrittämät taulurajoitukset
Käyttäjän määrittämä taulurajoitus on matriisityyppi, jonka avulla voidaan kuvata määritetyyppien määrittämien määritearvojen yhdistelmiä. Jos yrityksesi valmistaa esimerkiksi kaiuttimia, voit liittää käyttäjän määrittämään taulurajoitukseen sarakkeet kaapin viimeistelyä ja etusäleikköä varten. Kaapin viimeistelyn määritetyypillä on neljä arvoa ja etusäleikön määritetyypillä on kolme arvoa. Jos rajoituksia ei käytetä, mahdollisia yhdistelmiä on 4 × 3 = 12. Tässä esimerkissä on kuitenkin sallittu vain kuusi yhdistelmää, kuten seuraavasta taulukosta käy ilmi. Nämä tiedot näkyvät **Muokkaa taulurajoitusta** -sivun **Sallitut yhdistelmät** -välilehdessä.

| Kaapin viimeistely | Etusäleikkö |
|----------------|-------------|
| Musta          | Musta       |
| Musta          | Metalli       |
| Tammi            | Musta       |
| Ruusupuu       | Valkoinen       |
| Valkoinen          | Musta       |
| Valkoinen          | Valkoinen       |

Käyttäjän määrittämät taulurajoitukset määritetään staattisella taulusyötteellä, joka toimii samaan tapaan kuin lausekerajoitus. Kun käytät käyttäjän määrittämää taulurajoitusta, etuna on se, että taulut on usein helpompi luoda, ne ovat selkeämpiä ja niiden ylläpitäminen on helpompaa kuin pitkien lausekerajoitteiden.

## <a name="system-defined-table-constraints"></a>Järjestelmän määrittämät taulurajoitukset
Järjestelmän määrittämä taulurajoitus luo dynaamisen yhdistämismäärityksen taulussa olevan määritetyypin ja kentän välille. Kun järjestelmän määrittämä taulurajoitus sisältyy tuotemääritysmalliin, yhdistämismääritys varmistaa, että taulun tiedot ovat näkyvissä määritetyypin arvojen sijaan. Tuloksena on dynaaminen rajoitus, koska taulun sisältöä voi muokata (esimerkiksi muissa moduuleissa).  

Kun luot järjestelmän määrittämän taulurajoituksen, valitse taulu, määritä halutessasi käytettävä kysely ja määritä sitten määritetyypit valitun taulun kenttiin. Kenttätyyppien on vastattava määritetyyppejä.  

Ennen kuin taulurajoitus voidaan ottaa käyttöön tuotemääritysmallissa, taulurajoitus on sisällytettävä mallin yhden komponentin rajoitukseen. Tätä varten luodaan uusi rajoitus, valitaan taulurajoituksen tyyppi ja valitaan sitten käytettävä taulurajoitusmääritys. Lopuksi kaikki taulurajoituksen kentät on yhdistettävä tuotemääritysmallin määritteisiin.

<a name="see-also"></a>Lisätietoja
--------

[Tuotekonfiguraatiomallien avainkäsitteet](product-configuration-models.md)



