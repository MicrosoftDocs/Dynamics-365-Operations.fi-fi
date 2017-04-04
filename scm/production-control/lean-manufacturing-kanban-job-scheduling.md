---
title: "Lean-valmistuksen ajoituksen kanban-työ"
description: "Tässä artikkelissa on tietoja kanban-työn aikataulutuksen visuaalisesta hallintatavasta ja kanban-töiden erilaisista ajoitustavoista."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 02 - 36
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 062cbbc8a4fd3b4dc738f24ee0606a3741736377
ms.lasthandoff: 03/29/2017


---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Lean-valmistuksen ajoituksen kanban-työ

Tässä artikkelissa on tietoja kanban-työn aikataulutuksen visuaalisesta hallintatavasta ja kanban-töiden erilaisista ajoitustavoista.  

**Kanban-työn aikataulutus** -sivu tarjoaa visuaalisen hallintatavan Lean-valmistuksen työsolujen aikataulutukseen. Se näyttää yleiskatsauksen kaikista kanban-töistä ja tarjoaa useita suodatusominaisuuksia. Tältä sivulta voit siirtyä kaikille muille kanban-konfiguraatioon ja toteutukseen liittyville sivuille.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Kanban-töiden automaattinen ajoitus
Ajoitus voidaan määrittää käynnistymään automaattisesti, jos olet määrittänyt **automaattisen suunnittelun määrä** parametri kanban-säännölle. Jos määrität **automaattisen suunnittelun määrä**, **1**, kunkin kanban-työ suunnitellaan heti, kun se on luotu. Tämän tuloksena on sarja ensimmäinen sisään, ensimmäinen ulos -toimintoja. Jos määrität **Automaattisen suunnittelun määrä** -arvoksi yli 1, kanban-työt ryhmitellään suunnittelua. Tämä konsepti mahdollistaa kanban-kokojen pienentämisen varsinaisia taloudellisia eräkokoja pienemmiksi. Esimerkiksi tietyn nimikkeen (tai nimikkeen perhe) taloudellinen eräkoko on 30. Sen sijaan, että kanbanit, jotka käyttävät tuotteen määrä, 30, voit määrittää kanban-säännön siten, että se on 10 tuotetta ja ** automaattisen suunnittelun määrä ** arvo **3**. Vaikka automaattinen suunnittelu ajoittaa kanban-töitä työsolulle vain, kun on kolme suunnittelematonta työtä, suunnittelijalla ja työntekijäportaan esimiehellä on täysi näkyvyys siihen, että kaksi suunnittelematonta työtä odottaa toteutusta. Suunnittelija tai työntekijöiden esimies voi sitten ottaa nämä kaksi työtä tuotantoon suunnittelemalla ne manuaalisesti tai luomalla lisäkanbaneita.

## <a name="manual-scheduling"></a>Manuaalinen ajoitus
Manuaalista ajoitusta varten Microsoft Dynamics AX 2012:een luotiin kanban-aikataulu. Manuaalinen ajoitus voidaan yhdistää automaattiseen ajoitukseen. Kanban-aikataulun avulla voit suunnitella töitä ja perua niiden suunnitelmat, siirtää niitä sarjassa tai siirtää niitä kaudelta toiselle. Töiden, jotka perustuvat kanban-sääntöön, jossa **Automaattinen suunnittelu** -arvo on yli **0,** suunnittelu voidaan perua manuaalisesti. Nämä työt suunnitellaan kuitenkin uudelleen seuraavan automaattisen suunnittelutapahtuman yhteydessä (toisin sanoen, kun luodaan uusi kanban). Seuraavat vaihtoehdot ovat saatavilla manuaalisessa ajoituksessa:

-   **Ajoita** aikatauluttaa valitut työt niiden eräpäivän perusteella. (Tämä vaihtoehto muistuttaa automaattista suunnittelua.)
-   **Ajoita määritetystä päivämäärästä eteenpäin** yrittää ajoittaa valitut työt niiden eräpäivän mukaan, mutta rajoittaa tuloksen käyttämällä määritettyä aikaisinta aloituspäivää.
-   **Taaksepäin** siirtää valitut ajoitetut työt taaksepäin kyseisen jakson sarjassa.
-   **Eteenpäin** siirtää valitut ajoitetut työt eteenpäin kyseisen jakson sarjassa.
-   **Edellinen jakso** siirtää valitut ajoitetut työt edellisen jakson alkuun tai loppuun.
-   **Seuraava jakso** siirtää valitut ajoitetut työt seuraavan jakson alkuun tai loppuun.
-   **Suunnitelma**&gt;**Palauta työn tila** voit Poista ajoitetun työn ajoitus.

## <a name="lean-scheduling-groups"></a>Lean-ajoitusryhmät
Kukin väri edustaa Lean-ajoitusryhmää. Lean-ajoitusryhmät voidaan määrittää vapaasti yleisiksi ryhmiksi tai yksittäiseen työsoluun kuuluviksi ryhmiksi. Nimikkeitä ja dimensioita voi määrittää vapaasti ajoitusryhmiin. Esimerkiksi Maalaus-solussa ajoitusryhmä voi edustaa tuotteen väriä. Työssä, jota ohjaavat määrätyt työkaluvaatimukset, nimikkeitä saatetaan ryhmitellä työkaluvaatimuksen mukaisesti, ja pakkaustyösolu saattaa ryhmitellä nimikkeitä pakkausmallin perusteella. Värien käyttö Lean-ajoitusryhmissä on valinnaista mutta suositeltavaa. Se parantaa näkyvyyttä suunnitelman tilan. Se on erittäin helppo nähdä, mitä värejä tuotetaan joka päivä, ja näet yhdellä silmäyksellä, miten tätä työtä voidaan optimoida.

## <a name="work-cell-capacity-and-period-capacity"></a>Työsolun kapasiteetti ja kauden kapasiteetti
Lean-työsolun kapasiteetti on aina yhtäaikainen kapasiteetti. Toisin sanoen, useita töitä voi olla aktiivisena työsolussa samanaikaisesti. Kapasiteettia voidaan seurata kahdella tavalla: tuotantokapasiteetti ja tunnit.

### <a name="throughput"></a>Tuotantokapasiteetti

Työsolun kapasiteetin määrittää viitekauden (normaali työpäivä, viikko tai kuukausi) keskimääräinen tuotantokapasiteetti. Toteutunut päivä- tai viikkokapasiteetti lasketaan sitten työsolulle määritettyjen kalenterin työaikojen mukaisesti. Työkohtaisesti ladattu kapasiteetti on työn määrä korjattuna työsolun nimikkeen tuotantokapasiteetin suhdeluvulla.

### <a name="hours"></a>Tunnit

Saatavilla olevan päivä- tai viikkokapasiteetin määrittää työsolulle määritetty kalenteri. Työkohtaisesti ladattu kapasiteetti on tehtävän syklin kesto korjattuna määrällä (oletusarvoinen tehtävämäärä verrattuna toteutuneeseen työmäärään) ja työsolun nimikkeen tuotantokapasiteetin suhdeluvulla.

#### <a name="period-capacity-factbox"></a>Kauden kapasiteetti -tietoruutu

**Kanban-työn aikataulutus** -luettelosivu sisältää tietoruudun, joka näyttää saatavilla olevan ja varatun kauden kapasiteetin valitulle työsolulle. Riippuen valituista aikataulutuskausista tuotantovirtamallissa, kaudet näyttävät päiviä tai viikkoja.

<a name="see-also"></a>Lisätietoja
--------


