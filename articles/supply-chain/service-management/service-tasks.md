---
title: Huoltotehtävät – yleiskatsaus
description: Huoltotehtävien avulla voit kuvata huoltotilauksen aikana suoritettavan tehtävän. Sekä teknikot että asiakkaat näkevät nämä tiedot.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd7e5293ef506c6d785b420824f2c2a2c96112f7
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865889"
---
# <a name="service-tasks-overview"></a>Huoltotehtävät – yleiskatsaus

[!include [banner](../includes/banner.md)]

Huoltotehtävien avulla voit kuvata huoltotilauksen aikana suoritettavan tehtävän.
Sekä teknikot että asiakkaat näkevät nämä tiedot.

Voit luoda huoltotehtäviä **Huoltotehtävät**-sivulla ja liittää niitä tiettyyn huoltosopimukseen tai huoltotilaukseen luomalla huoltotehtävän suhteita. Aina kun luot huoltotehtävän suhteen, voit luoda

-  tehtävän sisäisiä huomautuksia, esimerkiksi tehtävään liittyviä yksityiskohtaisia teknisiä pyyntöjä, jotka teknikon on tärkeä tietää

-  ulkoisia huomautuksia, jotka asiakas voi nähdä. Nämä voivat sisältää vähemmän teknistä tietoa sisältävän selvityksen tehtävästä, jota suoritetaan asiakkaan ja huoltoyhtiön välisen sopimuksen mukaisesti.

Kun olet määrittänyt huoltotehtävän suhteen huoltotehtävän ja huoltotilauksen tai huoltosopimuksen välille, voit määrittää kyseisen huoltotehtävän luodessasi huoltotilauksen rivejä tai huoltosopimuksen rivejä huoltotilaukseen tai huoltosopimukseen.

Kun luot huoltotilauksia huoltosopimuksesta, voit ryhmitellä huoltotilauksen rivit huoltotilauksiin huoltosopimuksen riveille määritettyjen huoltotehtävien avulla.

## <a name="create-a-service-task"></a>Huoltotehtävän luominen

1. Valitse **Huoltohallinta** \> **Asetukset** \> **Palvelutehtävät**.
2. Luo uusi rivi.
3. Anna huoltotunnus ja kuvaus.

## <a name="example"></a>Esimerkki

Teknikon on suoritettava kaksi vaihdelaatikkoa (huoltokohde GB-1234) koskevaa työtä asiakkaan toimipisteessä. Asiakkaalle on luotu huoltosopimus, ja töihin liittyy useita tapahtumia. Näiden kahden työn huoltosopimus ja huoltosopimusrivit ovat seuraavat:

### <a name="service-agreement"></a>Huoltosopimus

| Project | Huoltosopimus | kuvaus                                  | Ryhmä   |
|---------|-------------------|----------------------------------------------|---------|
| 9012    | 000008\_001       | Tarkastus ja rutiinivaihto – GB-1234 | Lisä |

### <a name="service-agreement-lines"></a>Huoltosopimuksen rivit

| kuvaus             | Tapahtumalaji | Huoltokohde | Huoltotehtävä |
|-------------------------|------------------|----------------|--------------|
| Tarkastus ja puhdistus | Tunti             | GB-1234        | I/C - GB1234 |
| Matkat                  | Expense          | GB-1234        | I/C - GB1234 |
| Materiaalit               | Nimike             | GB-1234        | I/C - GB1234 |
| Rutiinivaihto     | Tunti             | GB-1234        | RR - GB1234  |
| GR-1                    | Nimike             | GB-1234        | RR - GB1234  |
| GR-5                    | Nimike             | GB-1234        | RR - GB1234  |

Näiden kahden työn huoltosopimuksen riveihin on liitetty kaksi huoltotehtävää. Huoltotehtävät määrittävät kuhunkin työhön kuuluvat tehtävät. Ensimmäisessä tapauksessa huoltotehtävä I/C - GB1234 yksilöi kaikki kohteen GB-1234 tarkastamiseen ja puhdistamiseen liittyvät huoltosopimuksen rivit. Toisessa tapauksessa palvelutehtävä RR - GB1234 yksilöi kaikki rutiinivaihtotyön suorittamiseen liittyvät huoltosopimusrivit.

Huoltotehtävän suhteet, jotka yhdistävät huoltotehtävät tiettyyn sopimukseen, ovat seuraavanlaiset:

### <a name="service-tasks"></a>Huoltotehtävät

| Huoltotehtävä | Kuvaus                             | Sisäinen huomautus                                                                                                                 | Ulkoinen huomautus                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| I/C - GB1234 | Vaihdelaatikon GB-1234 tarkastus           | Vaihdelaatikon GB-1234 visuaalinen ja mekaaninen tarkastus ja puhdistus                                                              | Vaihdelaatikon rutiinitarkastus |
| RR - GB1234  | Kohteen GB-1234 osien rutiinivaihto | Komponenttien GR-1 ja GR-5 vaihto osana normaalihuoltoa (ennen vuotta 2002 valmistetuista vaihdelaatikoista vaihdetaan myös komponentti GR-2) | Osien rutiinivaihto  |

## <a name="group-service-orders"></a>Huoltotilausten ryhmittely

Kun luot huoltotilaukset automaattisesti, voit käyttää huoltotehtäviä ryhmittelyperusteena. Voit ryhmitellä huoltotilaukset huoltotehtävien perusteella määrittämällä huoltosopimuksessa, että huoltosopimukseen perustuvat huoltotilaukset ryhmitellään niin, että huoltotehtävän tunnus on ensimmäinen ryhmittelyperuste.

**Ryhmitteleminen huoltotehtävien perusteella**

1. Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.
2. Valitse **Asetukset**-välilehdessä **Huoltotehtävän mukaan** **Yhdistä huoltotilaukset** -kentässä.


