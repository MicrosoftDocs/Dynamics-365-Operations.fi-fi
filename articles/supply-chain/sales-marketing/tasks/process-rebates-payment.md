---
title: Käsittele ostohyvityksiä maksua varten
description: Tämä menettely osoittaa, miten asiakkaiden hyväksytyt ja käsitellyt ostohyvitykset muunnetaan hyvityslaskuiksi.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1d32d94daef570e37a1a36d948fe18cd4041e46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966152"
---
# <a name="process-rebates-for-payment"></a>Käsittele ostohyvityksiä maksua varten

[!include [banner](../../includes/banner.md)]

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

