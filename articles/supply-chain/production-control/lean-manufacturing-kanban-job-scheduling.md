---
title: "Kanban-työn aikataulutus lean-valmistukselle"
description: "Tässä artikkelissa on tietoja kanban-työn aikataulutuksen visuaalisesta hallintatavasta ja kanban-töiden erilaisista ajoitustavoista."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5f1044e6731fd757532e34292109b9d81ca38719
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Kanban-työn aikataulutus lean-valmistukselle

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja kanban-työn aikataulutuksen visuaalisesta hallintatavasta ja kanban-töiden erilaisista ajoitustavoista.  

**Kanban-työn aikataulutus** -sivu tarjoaa visuaalisen hallintatavan Lean-valmistuksen työsolujen aikataulutukseen. Se näyttää yleiskatsauksen kaikista kanban-töistä ja tarjoaa useita suodatusominaisuuksia. Tältä sivulta voit siirtyä kaikille muille kanban-konfiguraatioon ja toteutukseen liittyville sivuille.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Kanban-töiden automaattinen ajoitus
Ajoitus voidaan käynnistää automaattisesti, jos määrität **Automaattisen suunnittelun määrä** -parametrin kanban-säännölle. Jos määrität **Automaattisen suunnittelun määrä** -asetukseksi **1**, jokainen kanban-työ suunnitellaan heti, kun se on luotu. Tämän tuloksena on sarja ensimmäinen sisään, ensimmäinen ulos -toimintoja. Jos määrität **Automaattisen suunnittelun määrä** -arvoksi yli 1, kanban-työt ryhmitellään suunnittelua. 

Tämä konsepti mahdollistaa kanban-kokojen pienentämisen varsinaisia taloudellisia eräkokoja pienemmiksi. Esimerkiksi tietyn nimikkeen (tai nimikeperheen) taloudellinen eräkoko on 30. Sen sijaan, että loisit kanbaneita, jotka käyttävät tuotteiden määrää 30, voit määrittää kanban-säännön niin, että sillä on tuotemäärä 10 ja **Automaattisen suunnittelun määrä** -arvo **3**. Vaikka automaattinen suunnittelu ajoittaa kanban-töitä työsolulle vain, kun on kolme suunnittelematonta työtä, suunnittelijalla ja työntekijäportaan esimiehellä on täysi näkyvyys siihen, että kaksi suunnittelematonta työtä odottaa toteutusta. Suunnittelija tai työntekijöiden esimies voi sitten ottaa nämä kaksi työtä tuotantoon suunnittelemalla ne manuaalisesti tai luomalla lisäkanbaneita.

## <a name="manual-scheduling"></a>Manuaalinen ajoitus
Manuaalista ajoitusta varten Microsoft Dynamics AX 2012:een luotiin kanban-aikataulu. Manuaalinen ajoitus voidaan yhdistää automaattiseen ajoitukseen. Kanban-aikataulun avulla voit suunnitella töitä ja perua niiden suunnitelmat, siirtää niitä sarjassa tai siirtää niitä kaudelta toiselle. Töiden, jotka perustuvat kanban-sääntöön, jossa **Automaattinen suunnittelu** -arvo on yli **0,** suunnittelu voidaan perua manuaalisesti. Nämä työt suunnitellaan kuitenkin uudelleen seuraavan automaattisen suunnittelutapahtuman yhteydessä (toisin sanoen, kun luodaan uusi kanban). Seuraavat vaihtoehdot ovat saatavilla manuaalisessa ajoituksessa:

-   **Ajoita** aikatauluttaa valitut työt niiden eräpäivän perusteella. (Tämä vaihtoehto muistuttaa automaattista suunnittelua.)
-   **Ajoita määritetystä päivämäärästä eteenpäin** yrittää ajoittaa valitut työt niiden eräpäivän mukaan, mutta rajoittaa tuloksen käyttämällä määritettyä aikaisinta aloituspäivää.
-   **Taaksepäin** siirtää valitut ajoitetut työt taaksepäin kyseisen jakson sarjassa.
-   **Eteenpäin** siirtää valitut ajoitetut työt eteenpäin kyseisen jakson sarjassa.
-   **Edellinen jakso** siirtää valitut ajoitetut työt edellisen jakson alkuun tai loppuun.
-   **Seuraava jakso** siirtää valitut ajoitetut työt seuraavan jakson alkuun tai loppuun.
-   **Suunnittele** &gt; **Palauta työn tila** -kohdassa voit peruttaa ajoitetun työn.

## <a name="lean-scheduling-groups"></a>Lean-ajoitusryhmät
Kukin väri edustaa Lean-ajoitusryhmää. Lean-ajoitusryhmät voidaan määrittää vapaasti yleisiksi ryhmiksi tai yksittäiseen työsoluun kuuluviksi ryhmiksi. Nimikkeitä ja dimensioita voi määrittää vapaasti ajoitusryhmiin. Esimerkiksi Maalaus-solussa ajoitusryhmä voi edustaa tuotteen väriä. Työssä, jota ohjaavat määrätyt työkaluvaatimukset, nimikkeitä saatetaan ryhmitellä työkaluvaatimuksen mukaisesti, ja pakkaustyösolu saattaa ryhmitellä nimikkeitä pakkausmallin perusteella. Värien käyttö Lean-ajoitusryhmissä on valinnaista mutta suositeltavaa. Se parantaa näkyvyyttä suunnitelman tilaan. On esimerkiksi helppo nähdä, mitkä värit tuotetaan minäkin päivänä, ja pystyt näkemään yhdellä silmäyksellä, miten tämä työ voidaan optimoida.

## <a name="work-cell-capacity-and-period-capacity"></a>Työsolun kapasiteetti ja kauden kapasiteetti
Lean-työsolun kapasiteetti on aina yhtäaikainen kapasiteetti. Toisin sanoen, useita töitä voi olla aktiivisena työsolussa samanaikaisesti. Kapasiteettia voidaan seurata kahdella tavalla: tuotantokapasiteetti ja tunnit.

### <a name="throughput"></a>Tuotantokapasiteetti

Työsolun kapasiteetin määrittää viitekauden (normaali työpäivä, viikko tai kuukausi) keskimääräinen tuotantokapasiteetti. Toteutunut päivä- tai viikkokapasiteetti lasketaan sitten työsolulle määritettyjen kalenterin työaikojen mukaisesti. Työkohtaisesti ladattu kapasiteetti on työn määrä korjattuna työsolun nimikkeen tuotantokapasiteetin suhdeluvulla.

### <a name="hours"></a>Tunnit

Saatavilla olevan päivä- tai viikkokapasiteetin määrittää työsolulle määritetty kalenteri. Työkohtaisesti ladattu kapasiteetti on tehtävän syklin kesto korjattuna määrällä (oletusarvoinen tehtävämäärä verrattuna toteutuneeseen työmäärään) ja työsolun nimikkeen tuotantokapasiteetin suhdeluvulla.

#### <a name="period-capacity-factbox"></a>Kauden kapasiteetti -tietoruutu

**Kanban-työn aikataulutus** -luettelosivu sisältää tietoruudun, joka näyttää saatavilla olevan ja varatun kauden kapasiteetin valitulle työsolulle. Riippuen valituista aikataulutuskausista tuotantovirtamallissa, kaudet näyttävät päiviä tai viikkoja.

<a name="additional-resources"></a>Lisäresurssit
--------




