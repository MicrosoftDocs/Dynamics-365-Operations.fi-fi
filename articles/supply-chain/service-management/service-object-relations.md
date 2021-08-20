---
title: Huoltokohteen suhteet
description: Voit luoda suhteen huoltokohteen ja huoltosopimuksen tai huoltotilauksen välille.
author: ShylaThompson
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f69d9a73f5d6858c2e898999d068c5f7c7ada68812d3cf5f9557fe6ed9765b0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767972"
---
# <a name="service-object-relations"></a>Huoltokohteen suhteet 

[!include [banner](../includes/banner.md)]

Voit luoda suhteen huoltokohteen ja huoltosopimuksen tai huoltotilauksen välille. Kun luot suhteen, liität huoltokohteen huoltosopimukseen tai huoltotilaukseen.

Kun suhde on luotu, voit liittää huoltokohteen huoltosopimuksen tai huoltotilauksen riveille.

## <a name="template-boms"></a>Mallituoterakenteet

Voit määrittää kohdesuhteelle myös mallituoterakenteen. Mallituoterakenne on sen kohteen tuoterakenne, jolle huolto suoritetaan. Jos vaihdat huoltokohteen komponenttiosan huoltokäynnin aikana, voit rekisteröidä tämän muutoksen huollon tuoterakenteeseen Huoltokohteet-lomakkeessa.

## <a name="example"></a>Esimerkki

Luot huoltosopimuksen kahden hissin huoltamisesta asiakkaan toimipisteessä.
Huoltosopimuksen on tunnus SAL-001.

Hissit on määritetty Huoltokohteeksi-lomakkeessa kohteiksi EL-S/1000 ja EL-L/1000.

Liität huoltokohteet EL-S/1000 ja EL-L/1000 huoltosopimukseen.

Haluat rekisteröidä muutokset huoltokohteen tuoterakenteeseen, kun vaihdat kohteen komponenttiosia, joten liität huollon tuoterakenteen huoltokohteen suhteeseen seuraavassa taulukossa kuvatulla tavalla.

| Huoltokohde | Suhde – huoltosopimus | Huollon tuoterakenne   |
|----------------|------------------------------|---------------|
| EL-S/1000      | ID SAL-001                   | BOM-EL-S/1000 |
| EL-L/1000      | ID SAL-001                   | BOM-EL-L/1000 |

Koska sopimus sisältää huoltokohteen suhteita, voi nyt luoda näiden kohteiden huoltosopimusrivit seuraavassa taulukossa osoitetulla tavalla.

| Tapahtumalaji | Luokka           | Huoltokohde |
|------------------|--------------------|----------------|
| Tunti             | Tarkastus         | EL-S/1000      |
| Tunti             | Vaihdelaatikon puhdistus  | EL-S/1000      |
| Nimike             | Puhdistusmateriaalit | EL-S/1000      |
| Tunti             | Tarkastus         | EL-L/1000      |
| Tunti             | Vaihdelaatikon puhdistus   | EL-L/1000      |
| Nimike             | Puhdistusmateriaalit | EL-L/1000      |

Hissin EL-S/1000 vaihdelaatikko on vaihdettava huoltokäynnillä. Kun haluat vaihtaa kohteen komponenttiosan, siirry graafiseen rakennesuunnitteluun käyttämällä nykyiselle huoltosopimukselle määritettävää huoltokohteen suhdetta.

Graafisen rakennesuunnittelun avaaminen huoltokohteen suhteen avulla

1. Huoltosopimukset
2. Kaksoisnapsauta huoltosopimusta tai luo uusi huoltosopimus valitsemalla Huoltosopimus.
3. Valitse Asetukset-välilehti.
4. Liitä mallituoterakenne huoltosopimukseen valitsemalla Huoltokohteet.
5. Muokkaa mallituoterakennetta avaamalla suunnittelulomake valitsemalla Suunnittelutoiminto Huoltokohteet-lomakkeessa.

## <a name="automatically-created-service-orders"></a>Automaattisesti luodut huoltotilaukset

Jos luot huoltosopimuksen huoltotilaukset automaattisesti, myös sopimuksen huoltokohteiden suhteet luodaan huoltotilauksissa.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]