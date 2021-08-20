---
title: Resurssien suorituskykyilmaisimet
description: Tässä ohjeaiheessa kerrotaan resurssien tunnusluvuista resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectKPI
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8bdc60d993a784ffc123d36b5e51cbd6028316f18a2dee6f4ee134a93ffc024e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778745"
---
# <a name="asset-kpis"></a>Resurssien suorituskykyilmaisimet

[!include [banner](../../includes/banner.md)]

 

Omaisuuden hallinnassa voit laskea käyttöomaisuuden ja käyttöomaisuustyyppien suorituskykyilmaisimet. KPI:iden avulla saat yleiskuvan käyttöomaisuuksien suorituskyvystä suhteessa esimerkiksi käytettävyysaikaan, seisokkeihin, korjausaikaan ja keskimääräiseen aikaan virheiden välillä (MTBF).

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssit** > **Resurssien suorituskykyilmaisimet**.

2. **Laske resurssien suorituskykyilmaisimet** -valintaikkunassa voit valita **Aika-asteikko**-kohdan, jota käytetään laskelmassa, sekä kauden **Alkamispäivä**- ja **Päättymispäivä** -kenttien avulla. 

3. Voit valita **Sisällytettävät tietueet** -pikavälilehdessä sisällytettävät tietyt käyttöomaisuudet ja käyttö omaisuuslajit tarvittaessa.

4. Aloita laskenta valitsemalla **OK**.

5. **Yhteenveto**-pikavälilehdessä laskentojen tulokset näkyvät ruudukkonäkymässä. Kukin käyttöomaisuuserä näkyy erillisellä rivillä.

6. **Valitun rivin suorituskykyilmaisimet** -pikavälilehdessä näkyy **Yhteenveto**-pikavälilehdessä valitun käyttöomaisuuden laskutoimitukset. KPI-arvot luokitellaan seuraavien kenttien mukaan:  **Aika**, **Käytettävyys**, **työtilaukset**, **Ylläpito**, **Viat**, **Ylläpidon käyttökatko** ja **Kustannus**.

Alla olevassa taulukossa on kuvaus **Resurssien suorituskykyilmaisimet** -sivun kentistä.

| Kenttä                   | Kuvaus                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Resurssi                   | Resurssin tunnus.                                                                                                                                                                                                                                                                                             |
| Kokonaisaika              | Laskennassa käytettyyn kalenteriin määritetty kokonaisaika. Jos käyttöomaisuuserä liittyy resurssiin, käytetään siihen liittyvää resurssikalenteria. Jos käyttöomaisuus ei liity resurssiin, käytetään **Resurssienhallinnan parametrit** -kohdassa valittua **Vakiokalenteri** -kenttää. |
| Toiminta-aika                  | Kokonaisaika vähennettynä seisokkiajalla.                                                                                                                                                                                                                                                                            |
| Käyttökatko                | Käyttökatkojen rekisteröinnit resurssille valitulla kaudella.                                                                                                                                                                                                                              |
| Korjausaika             | Korjausten työtilausten kulutettujen työtuntien kokonaismäärä.                                                                                                                                                                                                                                            |
| Saatavuus %          | Käytettävyysaika jaettuna kokonaisajalla ja kerrottuna sadalla.                                                                                                                                                                                                                                                   |
| Vikojen määrä        | Käyttöomaisuuserän vian oireille rekisteröityjen vian syiden määrä valitulla kaudella.                                                                                                                                                                                                             |
| MTBF                    | Virheiden välinen keskimääräinen aika, joka on kokonaisaika jaettuna käyttöomaisuuserälle valitulla kaudella kirjattujen vikojen määrällä. Jos virheiden määrä on nolla, MTBF-arvoksi on määritetty kokonaisaika.                                                                                                                   |
| Vikamäärä               | 1 jaettuna MTBF-arvolla.                                                                                                                                                                                                                                                                                    |
| MRT                     | Keskimääräinen korjausaika, joka on korjausaika jaettuna käyttöomaisuuserälle valitulla kaudella kirjattujen vikojen määrällä. Jos virheiden määrä on nolla, MRT-arvoksi on määritetty korjausaika.                                                                                                                           |
| Pysähdysten määrä         | Resurssin kunnossapitoseisokkeja koskevien rekisteröintien määrä.                                                                                                                                                                                                                                     |
| MTBS                    | Keskimääräinen aika pysähdysten välissä, mikä on kokonaisaika jaettuna kunnossapitoseisokkien rekisteröintien määrällä. Jos kunnossapitoseisokkien rekisteröintien määrä on nolla valitulla kaudella, MTBS-arvoksi määritetään kokonaisaika.                                                                                      |
| Ennaltaehkäisevä kustannus         | Kustannustyyppiin "Ennaltaehkäisevä" liittyvän käyttöomaisuuserän kirjatut kustannukset valitulla kaudella. Kustannustyypit määritetään työtilaustyypeille.                                                                                                                                                                       |
| Korjaava kustannus         | Kustannustyyppiin "Korjaava" liittyvän käyttöomaisuuserän kirjatut kustannukset valitulla kaudella. Kustannustyypit määritetään työtilaustyypeille.                                                                                                                                                                       |
| Korvaava arvo       | Käyttöomaisuuserälle korvaavana kustannuksena määritetty arvo.                                                                                                                                                                                                                                                  |
| Resurssin tyyppi             | Käyttöomaisuuserälle valitun käyttöomaisuustyypin tunnus.                                                                                                                                                                                                                                             |
| Valmistaja           | Käyttöomaisuuserälle valitun valmistajan tunnus.                                                                                                                                                                                                                                                 |
| Malli                   | Käyttöomaisuuserälle valitun mallin tunnus.                                                                                                                                                                                                                                           |
| Päivämäärästä               | KPI-laskennan aloituspäivämäärä. Jos käyttöomaisuuserä on luotu laskemista varten valitun aloituspäivämäärän jälkeen, tässä kentässä näkyy käyttöomaisuuserän alkamispäivämäärä.                                                                                                                                  |
| Päivämäärään                 | KPI-laskennan lopetuspäivämäärä. Jos käyttöomaisuuserä on rekisteröity passiiviseksi ennen laskemista varten valittua päättymispäivää, tässä kentässä näkyy aika, josta lähtien käyttöomaisuuserä ei ole enää aktiivinen.                                                                                               |
| Aika-asteikko              | KPI:iden laskennassa valitaan käytettävä aika-asteikko: tunnit, päivät tai viikot.                                                                                                                                                                                                            |
| Saatavuus            | Käytettävyys jaettuna kokonaisajalla.                                                                                                                                                                                                                                                                         |
| Työtilaukset             | KPI-laskentaan sisällytettävien tytötilausten kokonaismäärä.                                                                                                                                                                                                                                          |
| Työtilauksen aika         | Työtilauksiin kulutettujen työtuntien kokonaismäärä.                                                                                                                                                                                                                                               |
| Ensisijaiset työtilaukset     | KPI-laskentaan sisällytettävien ensisisjaisten työtilausten määrä.                                                                                                                                                                                                                                        |
| Toissijaiset työtilaukset   | KPI-laskentaan sisällytettävien toissijaisten työtilausten määrä.                                                                                                                                                                                                                                      |
| Ylläpitotyötilaukset | KPI-laskentaan sisällytettävien ylläpitotyötilausten määrä. Kunnossapidon työtilaus on työtilaus, johon ei liity vian syitä.                                                                                                                                                             |
| Ylläpitoaika        | Ylläpidon työtilauksiin kulutettujen työtuntien kokonaismäärä.                                                                                                                                                                                                                                       |
| Korjaustyötilaukset      | KPI-laskentaan sisällytettävien korjaustyötilausten määrä. Korjaustyötilaus on työtilaus, jolla on liittyvä vian syy.                                                                                                                                                                        |
| Luotettavuus %           | Laskeminen, joka perustuu käyttöomaisuus erän vikarekisteröintien odotettavissa olevaan eksponentiaaliseen kehitykseen, mikä tarkoittaa, että käyttöomaisuuserästä tulee ajan mittaan vähemmän luotettavaa kulumisesta johtuen. Tämän KPI:n laskeminen perustuu MTBF- ja kokonaisaikaan.                                                            |
| MTPS                    | Keskimääräinen tuotantopysähdysten aika, mikä on ylläpidon käyttökatkon aika jaettuna kunnossapitoseisokkien rekisteröintien määrällä. Jos kunnossapitoseisokkien rekisteröintien määrä on nolla valitulla kaudella, MTPS-arvoksi määritetään nolla.                                                                               |
| Kokonaiskustannukset              | Käyttöomaisuudelle kirjatut kokonaiskustannukset valitulla kaudella.                                                                                                                                                                                                                                              |
| Investointikustannus         | Kustannustyyppiin "Investointi" liittyvän käyttöomaisuuserän kirjatut kustannukset valitulla kaudella. Kustannustyypit määritetään työtilaustyypeille.                                                                                                                                                                       |

Alla olevassa kuvassa näkyy kuvakaappaus neljän käyttöomaisuuden KPI-laskennasta.

![Näyttökuva neljän käyttöominaisuuden KPI-laskennasta.](media/11-controlling-and-reporting.png)

- Voit valita useita käyttöomaisuuseriä kohdassa **Kaikki resurssit** napsauttamalla **Resurssien suorituskykyilmaisimet** -painiketta **Yleiset**-välilehdessä. Valitse sitten **OK** **Laske resurssien suorituskykyilmaisimet** -valintaikkunassa laskeaksesi valittujen resurssien suorituskykyilmaisimet.  
- KPI-laskennasta saadut tulokset eivät välttämättä sisällä [kunnossapitoseisokkeja koskevia rekisteröintejä](../work-orders/maintenance-downtime.md), jotka määräytyvät huoltoseisokkien syykoodien asetusten ja käytön mukaan. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]