---
title: Käsittele ostohyvityksiä maksua varten
description: Tämä menettely osoittaa, miten asiakkaiden hyväksytyt ja käsitellyt ostohyvitykset muunnetaan hyvityslaskuiksi.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2d97a59ae782af0a3d5ab71903961ef244a8e62
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "363312"
---
# <a name="process-rebates-for-payment"></a>Käsittele ostohyvityksiä maksua varten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tämä menettely osoittaa, miten asiakkaiden hyväksytyt ja käsitellyt ostohyvitykset muunnetaan hyvityslaskuiksi. Voit käyttää tätä opastusta USMF-demoyrityksessä. Opastuksen edellytyksenä on, että käytössä on vähintään yhden ostohyvitysvaatimuksen tila on Merkitse. Jos käytössä on USMF, suorita asiakkaiden ostohyvitysten luonti- ja käsittelyopastus ennen tämän opastuksen aloittamista.


## <a name="convert-rebate-claims-to-credit-note"></a>Muunna ostohyvitysvaatimukset hyvityslaskuksi
1. Valitse Kaikki asiakkaat.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse toimintoruudussa Perintä.
5. Valitse Selvitä tapahtumat.
6. Valitse Toiminnot.
7. Valitse Ostohyvitysohjelma.
    * Ostohyvitys-sivulla on luettelo ostohyvitysvaatimuksista, jotka olet käsitellyt asiakkaan ostohyvitystyötilassa ja joiden tila on Merkitse.    
8. Valitse Muokkaa.
    * Valitse hyvityslaskuun sisällytettävien vaatimusten Merkitse-valintaruudut.   
9. Valitse Toiminnot.
10. Valitse Luo hyvityslasku.
    * Avautuva sanoma ilmoittaa, että kirjauskansio on kirjattu. (Tämä on Myyntireskontran parametrit -sivulla määritetty myyntireskontran kulutuksen kirjauskansio.) Tämän vuoksi todellinen velkasumma (hyvitys) siirretään asiakkaan saldoon. Asiakastiliä hyvitetään ja ostohyvitysohjelman jaksotusta on veloitettu.  
11. Sulje sivu.
12. Valitse Peruuta.
    * Sivu päivitetään näyttämään päivitykset.  
13. Valitse toimintoruudussa Perintä.
14. Valitse Selvitä tapahtumat.
    * Huomaa, että negatiivisen summan tapahtuma, joka ilmaisee ostohyvityksen kokonaismäärän ilman laskutusviitteen määrää, on lisätty asiakkaan saldoon.   
15. Valitse Peruuta.

