---
title: Haamunimikkeet
description: Tässä ohjeaiheessa kuvataan, miten haamurivityyppiä voidaan käyttää tuoterakenteen riveillä ja Dynamics 365 Supply Chain Managementin kaavassa.
author: johanhoffmann
ms.date: 05/05/2022
ms.topic: article
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-05-05
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 5c9768381d35709611e4bec3d2b7793a4d896b34
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713243"
---
# <a name="phantom-items"></a>Haamunimikkeet

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan yksityiskohtaisesti, miten haamurivityyppiä voidaan käyttää tuoterakenteen (BOM) riveillä ja lomakkeessa.

Kuvassa 1 (a) on tuotteen H sekä osien F ja G tuoterakenne ja (b) on tuotteen H ja osan F reititystaulukko.

![Kuva 1: Tekninen tuoterakenne.](media/product-H-part-F.png)
*Kuva 1: Tekninen tuoterakenne*

Kuvassa 1 näytetään esimerkki tuoterakenteesta kahdella tasolla. Lopputuote H vastaa koneen kokoonpanon tuotetta. Koneen kokoonpanossa on kaksi osaa: sähköinen yksikkö (F), jossa on kaksi materiaalia (A ja B), ja pakkausmateriaalien ryhmä (G), jossa on myös kaksi materiaalia (C ja D). Toista materiaalia (E) käytetään koneen yleisen kokoonpanon aikana.

Kuva 1 edustaa tuotteen H tuotannon tuoterakennetta. Tämä rakenne antaa hyvän yleiskatsauksen koko koneen kokoonpanon osista ja komponenteista. Vaikka tuotesuunnittelijat haluavatkin ehkä mieluummin nähdä tuoterakenteen edustettuna tällä tavoin, rakenne ei välttämättä vastaa oikein sitä tapaa, jolla kone rakennetaan työnohjauksessa.

Esimerkiksi kuvan 1 tuotannon tuoterakenne osoittaa, että sähköinen yksikkö F on koottu erillisenä osana erillisessä työtilauksessa. Työnohjauksessa voidaan kuitenkin arvioida, että on optimaalisempaa koota sähköinen yksikkö yleisen koneen kokoonpanon osana eikä erillisenä työtilauksena.

Tämä tuotannon tuotantorakenne osoittaa myös, että osa G on erillinen osa. Kuitenkin tässä rakenteessa osa G ei edusta fyysistä osaa vaan pakkausmateriaalien kokoelmaa.

Sen vuoksi vaikka tuotannon tuoterakenne antaakin hyvän arvon tuotemallille ja sen ylläpitämiseen, se ei ehkä ole kaikkein loogisin keino tukea tuotteen tuotannonohjausprosessia. Sitävastoin valmistuksen tuoterakenne edustaa parasta keinoa tuotteen kehittämiseksi.

Kuvassa 2 näytetään, miten edeltävä tuotannon tuoterakenne siirretään valmistuksen tuoterakenteeseen. Kuvassa 2 (a) on tuotteen H tuoterakenne ja (b) on tuotteen H reititystaulukko.

![Kuva 2: Tuotannon tuoterakenne.](media/product-H-part-B.png)
*Kuva 2: Tuotannon tuoterakenne*

Näet tästä rakenteesta, että siinä ei ole osia F ja G, ja että näiden osien rakennemateriaalit on siirretty seuraavalle tuoterakennetasolle.

Toisin kuin tuotannon tuoterakenne, jossa on kaksi työvaihetaulukkoa, valmistuksen tuoterakenteessa on vain yksi työvaihetaulukko. Pakkausmateriaalin työvaihetta, joka on linkitetty osaan G, on myös laajennettu ja se kuuluu nyt tuotteen H työvaiheiden lomakkeeseen. Ensimmäinen työvaihe on sähköisen yksikön kokoonpano. Tämä järjestys on hyvän järjen mukainen, koska yksikköä käytetään seuraavassa työvaiheessa eli koneen kokoonpanossa. Viimeinen työvaihe on pakkauksen työvaihe, jossa käytetään kahta pakkausmateriaalia (C ja D).

Siirtyminen tuotannon tuoterakenteen ja valmistuksen tuoterakenteen välillä on mahdollista käyttämällä tuoterakenteen haamurivityyppiä. Kuten "haamu"-termi ilmaisee, osat F ja G ovat kadonneet kahden tuoterakennetyyppin välisen siirtymisen aikana. Tässä esimerkissä haamurivityyppiä sovelletaan osien F ja G tuoterakenneriveille tuotannon tuoterakenteessa. Kun luodaan tuotanto- tai erätilaus, tuotannon tuoterakenne kopioidaan tuotantoon tai erätilaukseen. Kun järjestys määritetty, tapahtuu siirtyminen tuotannon tuoterakenteesta valmistuksen tuoterakenteeseen kuvassa 2 näytetyn mukaisesti. Kuvan 2 työvaihetaulukossa pakkausmateriaalit C ja D ovat työvaiheen syötteitä.

## <a name="multilevel-phantom-bom-structures"></a>Monitasoiset haamutuoterakenteet

Haamurivityyppiä voidaan käyttää monitasoisissa tuoterakenteissa kuvassa 3 näytetyn mukaisesti. Kuvassa 3 (a) on tuotteen G tuoterakenne ja (b) on osien E ja F sekä tuotteen G reititystaulukko.

![Kuva 3: Tekninen tuoterakenne osa G.](media/product-G.png)
*Kuva 3: Tekninen tuoterakenne osa G*

Kuvassa 4 näytetään tuloksena saatu valmistuksen tuoterakenne ja reititystaulukko, jos osien E ja F tuoterakennerivit määritetään siten, että rivityyppinä on haamu. Kuvassa 4 (a) on tuotteen G tuoterakenne ja (b) on tuotteen G reititystaulukko.

![Kuva 4: Tuotannon tuoterakenne osa G.](media/product-G-route-sheet-G.png)
*Kuva 4: Tuotannon tuoterakenne osa G*

## <a name="phantom-and-route-network"></a>Haamu ja reititysverkko

Haamutuoterakenteita voidaan käyttää myös tuoterakenteelle, jossa on reititysverkko. Reititysverkossa yksi tai useampi toiminto suoritetaan samanaikaisesti. Kuvassa 5 näytetään esimerkki reititysverkosta, jota käytetään monitasoisessa tuoterakenteessa. Kuvassa 5 (a) on tuotteen G ja osan F tuoterakenne ja (b) on tuotteen G ja osan F reititystaulukko, jossa on reititysverkko.

![Kuva 5: Tuotannon tuoterakenne osa G, reititysverkko.](media/product-G-part-F.png)
*Kuva 5: Tuotannon tuoterakenne osa G, reititysverkko*

Kuvassa 6 (a) on tuotteen G ja F tuoterakenne ja (b) on tuotteen G ja F reititystaulukko.

![Kuva 6: Valmistuksen tuoterakenne osa G, reititysverkko.](media/product-G-part-F-with-route-sheet.png)
*Kuva 6: Valmistuksen tuoterakenne osa G, reititysverkko*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]