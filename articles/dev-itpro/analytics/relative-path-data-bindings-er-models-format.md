---
title: Suhteellisen polun käyttäminen ER-mallien ja-muotojen tietojen sidonnoissa
description: .
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6582cca9b912868f88de2770a17cbb6e67328660
ms.sourcegitcommit: d0fa7eb2166a30314205e7f70bbeaff6fbd5fb55
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726549"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Suhteellisen polun käyttäminen ER-mallien ja-muotojen tietojen sidonnoissa

[!include[banner](../includes/banner.md)]

Sähköisellä raportointityökalun (ER) avulla käyttäjät voivat määrittää sähköisen muodon rakenteita ja kuvailla sitten, miten kyseiset rakenteet täytetään Dynamics 365 for Finance and Operationsissa olevilla tiedoilla ja algoritmeilla. Lisätietoja on kohdassa [Sähköisen raportoinnin konfiguraatioiden luominen](electronic-reporting-configuration.md) Voit määrittää Finance and Operations -tietojen noutamiseen tarvittavan tietovirran ja sen avulla luotavan sähköisen asiakirjan seuraavasti:

- Sido määritetyt tietolähteet suunnitellun toimialuekohtaisen tietomallin elementteihin. Mallin rakenne ja valitut tietolähteet voivat olla osa monimutkaista hierarkkista rakennetta. Tämän vuoksi lopulliset sidonnat voivat olla suuria ja niissä voi olla useita erityyppisiä elementtejä (kuten suhteita, tauluja ja menetelmiä). Sidontojen luettavuus heikkenee ja niiden tarkistaminen ja ymmärtäminen voi olla hankalaa etenkin muille kuin omistajille. 
- Sitomalla tietomallin elementit muodon osiin voit määrittää, mitkä tiedot täytetään tietomallista luodun muodon tulokseen.

ER-yhdistämismääritysten suunnitteluohjelmien käytettävyyttä parantamaan on julkaistu suhteellisen polun ominaisuus. Suhteellisen polun esitysvaihtoehto on oletusarvoisesti otettu käyttöön kaikissa niissä uusissa Finance and Operations -esiintymissä, joissa ER-suunnittelukokemus on otettu käyttöön (Microsoft Dynamics 365 for Finance and Operations, Microsoft Regulatory Configuration Service). Suhteellisen polun parametri on toteutettu, jotta käyttäjät voivat jatkaa täydellisen polun käyttämistä, kun he käsittelevät ER-sidontojen tätä esitystä.

[![Käyttäjän parametrit](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Kun suhteellisen polun käyttöparametri on otettu käyttöön, yksi @-merkki korvaa polun päänimikkeeseen nykyisen mallielementin sidonnassa. Koko sidontapolku lyhenee, mikä selkeyttää koko yhdistämismääritystä ja helpottaa ymmärtämistä. Useimmissa tapauksissa ER-suunnitteluohjelmassa ei tarvita erillistä vieritystä kaikkien tietomallin sidontojen näyttämiseen.

[![Mallin yhdistämismäärityksen suunnitteluohjelma](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Kun aloitat uuden ER-lausekkeen suunnittelun, tarvitset sidonnan määrittämiseen päänimikkeen kenttään vain yhden merkin.

[![Reseptien suunnittelu](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Jos päätät muuttaa päämallinimikkeen tietolähdettä, absoluuttisessa polussa tämä mallinimike ja kaikki sisäkkäiset nimikkeet on sidottava uudelleen manuaalisesti uuteen tietolähteeseen. Kun suhteellisen polun käyttö on otettu käyttöön ja valitset uuden päänimikkeeseen sidottavan tietolähteen, saat mahdollisuuden sitoa kaikki päänimikkeen sisäkkäiset elementit automaattisesti uudelleen yhdellä napsautuksella.

[![Aiemmin luodun polun sanoman korvaaminen](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Jos vahvistat sisäkkäisten nimikkeiden uudelleensidonnan, uusi päänimike sijoitetaan kunkin aiemmin luodun päänimikkeen sisältävän sisäkkäisen nimikkeen polkuun.
Tämä toiminto ei katkaise ER-kehyksen yhteensopivuutta aiempien versioiden kanssa. Kaikkia aiemmin suunniteltuja ER-määrityksiä voi käyttää tämän uuden toiminnon kanssa eikä päivityksiä tai muuntoja tarvita.

> [!NOTE]
> Kaikki muutokset, jotka otettiin käyttöön mallin yhdistämismääritysten sisäkkäisten elementtien sidontojen joukkomuokkauksella, tallennetaan oikein määrityksen muutostiedostoon (muutosten seurantaan). Tällä tavoin asiakkaat voivat pohjustaa mallin yhdistämismääritysten johdetut versiot sen mihin tahansa uuteen perusversioon, jota on muokattu tällä uudella toiminnolla.
