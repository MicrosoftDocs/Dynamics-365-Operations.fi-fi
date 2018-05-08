---
title: Lean-valmistuksen yleiskatsaus
description: "Tässä artikkelissa on yleiskatsaus ja kuvaus Microsoft 365 for Finance and Operationsin Lean-valmistuksen toiminnoista."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob, KanbanBoardWorkCell, KanbanJobSchedulingListPage, LeanProductionFlow
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19371
ms.assetid: 026c5605-6be7-4fdb-a6f2-8e37a806796c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 99030966587a2784f61cecbfc7f9985f75f6d779
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="lean-manufacturing-overview"></a>Lean-valmistuksen yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yleiskatsaus ja kuvaus Microsoft 365 for Finance and Operationsin Lean-valmistuksen toiminnoista.

Lean-valmistus sisältää työkaluja lean-työvaiheiden mallintamiseen. Nämä työkalut tukevat seuraavia käsitteitä ja liiketoiminnan tehtäviä sekä edistävät niitä:
-   Lean-valmistuksen perustan luonti mallintamalla tuotanto- ja logistiikkaprosessit tuotantovirroiksi.
-   Lean-imujärjestelmän toteutus käyttämällä kanbaneja ilmaisemaan kysynnän vaatimuksia.
-   Kanban-töiden valvonta ja ylläpito.

Finance and Operationsin lean-valmistuksen arkkitehtuuri koostuu tuotantovirroista, tehtävistä ja kanban-säännöistä. Nämä rakenteet on integroitu kokonaisuudessaan Finance and Operationsin prosesseihin. Voit käyttää lean-valmistusta yhdistelmätuotantoympäristössä, joka yhdistää erilaiset toimitus-, tuotanto- ja hankintastrategiat. Näitä strategioita ovat tuotantotilaukset, prosessiteollisuuden erätilaukset, ostotilaukset ja siirtotilaukset.

| **Tärkeä**                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Voit käyttää Finance and Operationsia kanbaneja sisältävän lean-tuotannon toteutuksen tukena. Lean-periaatteiden onnistunut käyttöönotto kuitenkin määräytyy käytettyjen sisäisten liiketoimintaprosessien sekä varsinaisten tuotanto-olosuhteiden ja ympäristön mukaan. |

## <a name="modeling-manufacturing-and-logistics-processes-as-production-flows"></a> Tuotanto- ja logistiikkaprosessien mallintaminen tuotantovirtoina
Voit luoda perustan lean-valmistukselle mallintamalla tuotanto- ja logistiikkaprosessit tuotantovirroiksi. Se muodostuu seuraavista tehtävistä:
1.  Lean-täydennysstrategioina käyttöönotettavien prosessien tunnistaminen ja niiden mallintaminen tuotantovirtoina. Voit sitten analysoida ja yksinkertaistaa prosesseja. Yksi lean-käyttöönoton tavoitteista on pienentää hävikkiä parantamalla materiaalin- ja tiedonkulkua.
2.  Tuotantovirran määrittäminen materiaalin kulkua kuvaavaksi tehtävien sarjaksi. Siirtotehtävä määrittää tuotteen tai tuotteiden liikkumisen sijainnista toiseen. Prosessin tehtävä määrittää lisäarvotyövaiheen, joka on liitetty tuotteeseen.
3.  Tahtiaikavaatimukset määrittävän tuotantovirtaversion luonti. Näillä vaatimuksilla lasketaan jokaisen tehtävän syklin kesto tuotantovirrassa. Voit luoda tuotantovirroista useita versiota ja parantaa sitten prosesseja näiden versioiden avulla.

## <a name="using-kanbans-to-signal-demand-requirements"></a> Kysynnän vaatimusten ilmaiseminen kanbanien avulla
Imujärjestelmä tuottaa tavaroita silloin, kun tavaroita tarvitaan. Tämä käytäntö lyhentää toimitusten läpimenoaikoja ja pienentää ylimääräistä varastoa. Voit käyttää kanbaneja tuotantovirtoihin perustuvien vaatimusten suunnitteluun, seurantaan ja käsittelyyn. Kanban-kehikko luodaan luomalla kanban-säännöt määrittämään, milloin kanbanit luodaan ja miten vaatimukset täytetään. Luotavia kanban-sääntöjä on kahta tyyppiä: valmistusäännöillä luodaan prosessin kanban-töitä ja kanban-ottosäännöillä luodaan siirron kanban-töitä. Voit määrittää seuraavat täydennysstrategiat:
-   **Vakiomäärän** kanban-säännöt liittyvät vakiomääräisiin käsittely-yksiköihin, ja aktiivisten kanbanien määrä pysyy vakiona. Aina kun kaikki kanbanin tuotteet on kulutettu ja käsittely-yksiköt tyhjennetään manuaalisesti, uusi saman tyypin kanban luodaan. Kun luot vakiomäärän kanban-sääntöjä, voit laskea optimaaliset käytettävät kanban-määrät ja tuotemäärät. Laskelma ottaa huomioon ennusteet, avoimien tilausten todellisen kysynnän, nimikkeiden täydennyksen läpimenoajan ja historiallisen kysynnän.
-   **Ajoitetut** kanban-säännöt täydentävät pääsuunnittelun laskemat vaatimukset. Pääsuunnittelu luo suunniteltuja kanbanien, jotka voidaan vahvistaa kanbaneiksi.
-   **Tapahtuman** kanban-säännöt täydentävät myyntitilausriveiltä, tuotannon tuoterakenneriveiltä, kanban-rivien tai varaston vähimmäisasetuksista peräisin olevia vaatimuksia. Kun tapahtuman kanbaneja luodaan, ne tarvekohdistetaan lähteen tarpeisiin.

Kun kanbaneja luodaan, vähintään yksi kanban-töitä muodostetaan kanban-säännöissä määritettyjen kanban-työnkulun tehtävien perusteella.

## <a name="monitoring-and-maintaining-kanban-jobs"></a> Kanban-töiden valvonta ja ylläpito
Lean-valmistus tuo näkyvyyttä kanban-sääntöjen hallitsemien valmistus- ja logistiikkatehtävien nykyiseen tilaan. Tämän ansiosta voit suunnitella ja priorisoida seuraavat tehtävät:

-   Yleiskäsityksen saanti nykyisen kanban-työn aikataulusta.
-   Kanban-töiden suunnittelu ja uudelleenajoittaminen.
-   Kanban-töiden tilan seuranta ja rekisteröinti.

Seuraavassa luettelossa käsitellään erikoistuneita kanban-tauluja:
-   Kanban-työn aikataulutus – Kanban-töiden yhteenveto. Taulu sisältää kanban-työt ja niiden tilat yhdessä tai useassa työsolussa. Työt on lueteltu tuotantovirran mallissa määritettyjen suunnittelukausien (päiviä tai viikkoja) mukaisesti. Taulussa on myös kapasiteetin kulutus jokaisena suunnittelujaksona, jotta aikataulutettua kuormaa voidaan valvoa. Voit muuttaa kanban-töiden tilan, ajoittaa kanban-työt eri suunnittelukaudella ja suorittaa muita tehtäviä.
-   Siirtotöiden Kanban-taulu – Nykyisten siirtotöiden yhteenveto. Voit päivittää ja rekisteröidä keräysluetteloita, aloittaa ja päättää siirtotöitä sekä suorittaa muita tehtäviä.
-   Prosessitöiden kanban-taulu – Taulu on suunniteltu tukemaan normaalia tuotantovirtaa sekä antamaan yleiskuva yhden tai usean työsolun tämän hetkisestä tilanteesta. Tässä taulussa kanbaneja voidaan priorisoida, kerätä tai valmistaa. Taulu on myös suunniteltu tukemaan kanbanien ilmoittamista viivakoodien avulla.

## <a name="kanban-jobs-and-integration-with-finance-and-operations-processes"></a>Kanban-työt ja integrointi Finance and Operationsin prosesseihin
Kanban-työt on integroitu täysin Finance and Operationsin varastotapahtumien nykyisiin prosesseihin.
-   Voit täydentää keräystehtävillä kanban-töiden vaatimusten täyttämiseen käytettäviä materiaaleja.
-   Voit tulostaa kanbanien käyttöä tukevia kanban-kortteja, kiertäviä kanban-kortteja ja keräysluetteloita. Näitä asiakirjoja käytetään kuvaamaan, jäljittämään ja rekisteröimään kanban-töitä varastossa ja tuotannossa.
-   Voit rekisteröidä varaston keräys- ja siirtotehtävät skannaamalla viivakoodit.

Lean-valmistus tukee myös niiden palvelujen osto- ja laskutusprosesseja, joihin alihankintana suoritettavat tehtävät viittaavat.
-   Voit määrittää ostosopimuksen rivejä ja palveluja alihankintana suoritettaviin tehtäviin.
-   Voit luoda hankinnan ja palvelujen laskuttamisen tueksi kausittaisia ostotilauksia ja vastaanottoilmoituksia.






