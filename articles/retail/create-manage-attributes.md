---
title: "Määritteiden luonti ja hallinta"
description: "Tässä artikkelissa käsitellään Microsoft Dynamics 365 for Retailin määritteitä. Määritteiden avulla voit kuvailla tuotetta ja sen ominaisuuksia käyttäjän määrittelemien kenttien avulla."
author: pdp1207
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 4493c2f9e9e9dfe990f3b1670d3cd35e3bbaa38d
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017

---

# <a name="create-and-manage-attributes"></a>Määritteiden luonti ja hallinta

[!include[banner](includes/banner.md)]


Tässä artikkelissa käsitellään Microsoft Dynamics 365 for Retailin määritteitä. Määritteiden avulla voit kuvailla tuotetta ja sen ominaisuuksia käyttäjän määrittelemien kenttien avulla.

Määritteiden avulla voit kuvailla tuotetta ja sen ominaisuuksia käyttäjän määrittelemien kenttien avulla. Voit esimerkiksi määrittää tuotteen muistin koon ja kovalevyn kapasiteetin ja ilmaista, onko tuote Energy Star -merkinnän mukainen. Määritteitä voidaan liittää erilaisiin vähittäismyynnin yksiköihin, kuten tuotekategorioihin ja vähittäismyyntikanaviin, ja niille voidaan asettaa oletusarvoja. Tuotteet perivät määritteensä ja oletusarvonsa näiltä määritteiltä, kun ne liitetään tuotekategorioihin tai vähittäismyyntikanaviin. Oletusarvot voidaan ohittaa yksittäisen tuotteen tasolla, vähittäismyyntikanavan tasolla, tai vähittäismyyntiluettelossa.

#### <a name="examples"></a>Esimerkkejä

| Luokka   | Ominaisuus                | Sallitut arvot          | Oletusarvo |
|------------|--------------------------|-----------------------------|---------------|
| TV & Video | Brandi                    | Mikä tahansa voimassa oleva Tuotemerkki-arvo       | Ei mitään          |
| TV         | Näytön koko              | 20–80 tuumaa                     | Ei mitään          |
| TV         | Vertikaaliresoluutio      | 480i, 720p, 1080i, tai 1080p | 1080p         |
| TV         | Näytön päivitystaajuus      | 60 Hz, 120 Hz, tai 240 Hz       | 60 Hz          |
| TV         | HDMI-tuloja              | 0–10                        | 3             |
| TV         | DVI-tuloja               | 0–10                        | 1             |
| TV         | Komposiittituloja         | 0–10                        | 2             |
| TV         | Komponenttituloja         | 0–10                        | 1             |
| LCD-näyttö        | 3D-valmius                 | Kyllä tai Ei                   | Kyllä           |
| LCD-näyttö        | 3D käytössä               | Kyllä tai Ei                   | Nro            |
| Plasma     | Toimintalämpötila vähintään      | 0–43 astetta              | 32            |
| Plasma     | Toimintalämpötila korkeintaan        | 0–43 astetta              | 100           |
| Projektio | Projektiokuvaputken takuu | 6, 12, tai 18 kuukautta         | 12            |
| Projektio | Projektiokuvaputkien lukumäärä    | 1–5                         | 3             |


## <a name="attribute-type"></a>Määritetyyppi
  [![attributes-fixed-copy](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) 
  
Määritteet perustuvat määritetyyppeihin. Määritetyypit osoittavat, minkälaista tietoa voi lisätä tiettyyn määritteeseen. Microsoft Dynamics 365 for Retail tukee tällä hetkellä seuraavia määritetyyppejä:

-   **Valuutta** – Tämä määritetyyppi tukee valuutta-arvoja. Se voidaan sitoa (eli se voi tukea arvoaluetta), tai se voidaan jättää avoimeksi.
-   **DateTime** – Tämä määritetyyppi tukee päivämäärä- ja aika-arvoja. Se voidaan sitoa (eli se voi tukea arvoaluetta), tai se voidaan jättää avoimeksi.
-   **Desimaali** – Tämä määritetyyppi tukee numeerisia arvoja, jotka sisältävät desimaaleja. Se tukee myös mittayksikköjä. Se voidaan sitoa (eli se voi tukea arvoaluetta), tai se voidaan jättää avoimeksi.
-   **Kokonaisluku** – Tämä määritetyyppi tukee numeerisia arvoja. Se tukee myös mittayksikköjä. Se voidaan sitoa (eli se voi tukea arvoaluetta), tai se voidaan jättää avoimeksi.
-   **Teksti** – Tämä määritetyyppi tukee tekstiarvoja. Se tukee myös etukäteen määritettyä mahdollisten arvojen joukkoa (luettelointi).
-   **Totuusarvo** – Tämä määritetyyppi tukee binaarisia arvoja (**tosi**/**epätosi**).
-   **Viite**.

## <a name="attribute"></a>Ominaisuus
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) Nimen, kutsumanimen, kuvauksen ja ohjetekstin lisäksi yksi tai useampi seuraavista tietotyypeistä voidaan poimia määritteestä:

-   Oletusarvo
-   Määritteen metatiedot, kuten metatiedot, jotka ilmaisevat, voidaanko määritettä etsiä, tarkentaa tai lajitella.

## <a name="attribute-group"></a>Määriteryhmä
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) Kun määritteet on määritelty, ne voidaan ryhmitellä määriteryhmiksi. Määriteryhmät sisältävät yksittäisistä määritteistä koottuja ryhmiä, ja ne voidaan liittää vähittäismyyntiluokkiin tai -kanaviin.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Määriteryhmien liittäminen vähittäismyyntiluokkiin
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) Yksi tai useampi määriteluokka voidaan liittää vähittäismyynnin tuoteluokkahierarkian luokkasolmuihin. Kun tuotteet on luokiteltu, ne perivät määriteryhmiin sisältyvät määritteet.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Määriteryhmien liittäminen vähittäismyymälöihin
  [![createandmanageattribute-13-1024x576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) Yksi tai useampi määriteryhmä voidaan liittää yhteen tai useampaan vähittäismyymälähierarkian vähittäismyymälään. Kun tuotteet on lisätty tiettyihin vähittäismyymälöihin, ne perivät määriteryhmään sisältyvät määritteet.

## <a name="overriding-attribute-values"></a>Määritearvojen ohittaminen
### <a name="at-the-product-level"></a>Tuoteosastolla

  [![createandmanageattribute-14-1024x576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) Määritteiden oletusarvot voidaan ohittaa tuotetasolla (ts. yksittäisten tuotteiden kohdalla).

### <a name="in-a-retail-catalog"></a>Vähittäismyynnin luettelossa

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) Määritteiden oletusarvot voidaan ohittaa tietyissä luetteloissa olevien, määrätyille vähittäismyyntikanaville kohdistettujen yksittäisten tuotteiden osalta.

### <a name="at-the-retail-channel-level"></a>Vähittäismyyntikanavan tasolla

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) Määritteiden oletusarvot voidaan ohittaa tietyissä luetteloissa olevien, määrätyille vähittäismyyntikanaville kohdistettujen yksittäisten tuotteiden osalta.



