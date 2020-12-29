---
title: Haamunimikkeet
description: Tässä ohjeaiheessa kuvataan yksityiskohtaisesti, miten haamurivityyppiä voidaan käyttää tuoterakenteen riveillä ja Dynamics 365 Supply Chain Managementin kaavassa.
author: ShylaThompson
manager: tfehr
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b14bebadd7088c9bbcfb6b1c5df1fe1a3c98694d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427257"
---
# <a name="phantom-items"></a>Haamunimikkeet

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan yksityiskohtaisesti, miten haamurivityyppiä voidaan käyttää tuoterakenteen (BOM) riveillä ja lomakkeessa. Seuraavassa kuvassa (a) on tuotteen H sekä osien F ja G tuoterakenne ja (b) on tuotteen H ja osan F reititystaulukko.

![Tuote H ja osa F](media/product-H-part-F.png)


Tässä kuvassa näytetään esimerkki tuoterakenteesta kahdella tasolla. Lopputuote H vastaa koneen kokoonpanon tuotetta. Koneen kokoonpanossa on kaksi osaa: sähköinen yksikkö (F), jossa on kaksi materiaalia (A ja B), ja pakkausmateriaalien ryhmä (G), jossa on myös kaksi materiaalia (C ja D). Toista materiaalia (E) käytetään koneen yleisen kokoonpanon aikana.

![Tuote H ja osa F](media/product-H-part-B.png)

Edellinen kuva edustaa tuotteen H tuotannon tuoterakennetta. Tämä rakenne antaa hyvän yleiskatsauksen koko koneen kokoonpanon osista ja komponenteista. Vaikka tuotesuunnittelijat haluavatkin ehkä mieluummin nähdä tuoterakenteen edustettuna tällä tavoin, rakenne ei välttämättä vastaa oikein sitä tapaa, jolla kone rakennetaan työnohjauksessa. 

Esimerkiksi edellisen kuvan tuotannon tuoterakenne osoittaa, että sähköinen yksikkö F on koottu erillisenä osana erillisessä työtilauksessa. Työnohjauksessa voidaan kuitenkin arvioida, että on optimaalisempaa koota sähköinen yksikkö yleisen koneen kokoonpanon osana eikä erillisenä työtilauksena.

Tämä tuotannon tuotantorakenne osoittaa myös, että osa G on erillinen osa. Kuitenkin tässä rakenteessa osa G ei edusta fyysistä osaa vaan pakkausmateriaalien kokoelmaa. 

Sen vuoksi vaikka tuotannon tuoterakenne antaakin hyvän arvon tuotemallille ja sen ylläpitämiseen, se ei ehkä ole kaikkein loogisin keino tukea tuotteen tuotannonohjausprosessia. Sitävastoin valmistuksen tuoterakenne edustaa parasta keinoa tuotteen kehittämiseksi.

Seuraavassa kuvassa näytetään, miten edeltävä tuotannon tuoterakenne siirretään valmistuksen tuoterakenteeseen. Tässä kuvassa (a) on tuotteen H tuoterakenne ja (b) on tuotteen H reititystaulukko.

Näet tästä rakenteesta, että siinä ei ole osia F ja G, ja että näiden osien rakennemateriaalit on siirretty seuraavalle tuoterakennetasolle. 

Toisin kuin tuotannon tuoterakenne, jossa on kaksi työvaihetaulukkoa, valmistuksen tuoterakenteessa on vain yksi työvaihetaulukko. Pakkausmateriaalin työvaihetta, joka on linkitetty osaan G, on myös laajennettu ja se kuuluu nyt tuotteen H työvaiheiden lomakkeeseen. Ensimmäinen työvaihe on sähköisen yksikön kokoonpano. Tämä järjestys on hyvän järjen mukainen, koska yksikköä käytetään seuraavassa työvaiheessa eli koneen kokoonpanossa. Viimeinen työvaihe on pakkauksen työvaihe, jossa käytetään kahta pakkausmateriaalia (C ja D).

Siirtyminen tuotannon tuoterakenteen ja valmistuksen tuoterakenteen välillä on mahdollista käyttämällä tuoterakenteen haamurivityyppiä. Kuten "haamu"-termi ilmaisee, osat F ja G ovat kadonneet kahden tuoterakennetyyppin välisen siirtymisen aikana. Tässä esimerkissä haamurivityyppiä sovelletaan osien F ja G tuoterakenneriveille tuotannon tuoterakenteessa. Kun luodaan tuotanto- tai erätilaus, tuotannon tuoterakenne kopioidaan tuotantoon tai erätilaukseen. Kun järjestys määritetty, tapahtuu siirtyminen tuotannon tuoterakenteesta valmistuksen tuoterakenteeseen edellisissä kuvissa näytetyn mukaisesti. Toisen kuvan työvaihetaulukossa pakkausmateriaalit C ja D ovat työvaiheen syötteitä. 

## <a name="multilevel-phantom-bom-structures"></a>Monitasoiset haamutuoterakenteet
Haamurivityyppiä voidaan käyttää monitasoisissa tuoterakenteissa seuraavassa kuvassa näytetyn mukaisesti. Tässä kuvassa (a) on tuotteen H tuoterakenne ja (b) on osien E ja F sekä tuotteen G reititystaulukko. 

![Tuote G ja osa F reititystaulukoiden kanssa](media/product-G-route-sheet-G.png)


Seuraavassa kuvassa näytetään tuloksena saatu valmistuksen tuoterakenne ja reititystaulukko, jos osien E ja F tuoterakennerivit määritetään siten, että rivityyppinä on haamu. Tässä kuvassa (a) on tuotteen G tuoterakenne ja (b) on tuotteen G reititystaulukko.

![Tuote G](media/product-G.png)


## <a name="phantom-and-route-network"></a>Haamu ja reititysverkko
Haamutuoterakenteita voidaan käyttää myös tuoterakenteelle, jossa on reititysverkko. Reititysverkossa yksi tai useampi toiminto suoritetaan samanaikaisesti. Seuraavassa kuvassa näytetään esimerkki reititysverkosta, jota käytetään monitasoisessa tuoterakenteessa. Tässä kuvassa (a) on tuotteen G ja osan F tuoterakenne ja (b) on tuotteen G ja osan F reititystaulukko, jossa on reititysverkko.

![Tuote G ja osa F](media/product-G-part-F.png)


Seuraavassa kuvassa (a) on tuotteen G ja osan F tuoterakenne ja (b) on tuotteen G ja osan F reititystaulukko.

![Tuote G ja osa F reititystaulukoiden kanssa](media/product-G-part-F-with-route-sheet.png)
