--- 
title: "Käsittele ostohyvityksiä maksua varten"
description: "Tämä menettely osoittaa, miten asiakkaiden hyväksytyt ja käsitellyt ostohyvitykset muunnetaan hyvityslaskuiksi."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 791ec304b9ea7c49fbea506d73c4daffd4478739
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="process-rebates-for-payment"></a>Käsittele ostohyvityksiä maksua varten

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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


