---
title: Työhönoton tietojen muutosten seuraaminen
description: Prosessin valvonta -toiminnon avulla voit jäljittää, milloin hakijat, avoimet työpaikat tai työhakemukset muuttuvat raportointi- tai yhteensopivuussyistä.
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 803c935493a4080b8c1d0ef92bbe7db601f3ca03
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517896"
---
# <a name="track-changes-in-recruiting-data"></a>Työhönoton tietojen muutosten seuraaminen

Voit jäljittää ehdokkaisiin, avoimiin työpaikkoihin tai työsovelluksiin tehtyjä muutoksia käyttämällä valvonnan käsittelyä. Tämä on hyödyllistä raportointi- tai yhteensopivuussyistä.

Voit tarkastella jäljitettyjä tietoja Power BIssä OData-yhdistimen avulla. Lisätietoja on kohdassa [Yhdistä OData-syötteisiin kohteessa Power BI Desktop](https://docs.microsoft.com/en-us/power-bi/desktop-connect-odata).

## <a name="track-changes"></a>Muutosten seuranta
Voit määrittää rekrytointitietojen muutosten seurannan seuraavasti:

1. Valitse [PowerApps](https://web.powerapps.com)-ohjelmassa sopiva ympäristö.

2. Valitse **Asetukset** (rataskuvake), valitse **Lisämukautukset** ja valitse sitten **Resurssit** **Kehittäjän resurssit** -kohdasta. 

3. Kopioi arvo **Kehittäjän resurssit** -sivulla **Esiintymän Web-API-arvo** -kenttään. Esimerkiksi arvo voi näyttää tältä: https://yourorgname.api.crm.dynamics.com/api/data/v9.1/.

4. Tämän jälkeen voit tehdä kyselyn seuraavien entiteettien tiedoista:
  - Työn avaushistoria (msdyn_jobopeninghistories)
  - Työhakemushistoria (msdyn_jobapplicationhistories) 
  - Ehdokashistoria (msdyn_candidatehistories)

## <a name="data-reported"></a>Tiedot ilmoitettu

Seuraavat tiedot ovat käytettävissä prosessien valvonnassa.

| Tiedot ilmoitettu | Kuvaus |
| --- | --- |
| Muutettu (msdyn_ChangedbyId) | Viite käyttäjään |
| Luotu (createdon) |  Päivämäärä ja kellonaika UTC-aikana, kun muutos tapahtui |
| Muuta tyyppiä (msdyn_changetype) | Mitä muutoksia tapahtui |
| Hakijoiden yhteiset arvot, avoimet työpaikat, <br></br>ja työhakemukset | Luotu<br></br>Päivitetty |
| Työhakemushistoria | Artefakti lisätty <br></br>Artefakti poistettu |
| Avointen työpaikkojen historia | TODO: kirjaus lisätty <br></br>TODO: kirjaus poistettu <br></br>TODO: kirjaus päivitetty <br></br>TODO: osallistuja lisätty <br></br>TODO: osallistuja poistettu |
| Ehdokkaan historia | Artefakti lisätty <br></br>Artefakti poistettu <br></br>Työkokemus lisätty <br></br>Työkokemus poistettu <br></br>Koulutus lisätty <br></br>Koulutus poistettu <br></br>Taito lisätty <br></br>Taito poistettu <br></br>Tunniste lisätty <br></br>Tunniste poistettu <br></br>Sosiaalinen verkko lisätty <br></br>Sosiaalinen verkko poistettu <br></br>Henkilökohtaiset tiedot lisätty <br></br>Henkilökohtaiset tiedot päivitetty<br></br> |
| Muutetut kentät (msdyn_changedfields) | JSON-objekti, joka luetteloi muutetut kentät, ei ehkä tallenna kaikkien kenttien arvoja.<br></br><br></br>Jos kyseessä on "luodut" ja "päivitetyt" muutokset, se luetteloi luotujen tai muokattujen tietueiden kentät.<br></br><br></br>Jos muutos tyyppi on "lisätty", se luetteloi alatason tietueen kentät.<br></br><br></br>**Esimerkki:**<br></br><br></br>{<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": true } <br></br>} |
|Työhakemushistoria | Työhakemus (msdyn_JobapplicatonId)<br></br>Tila (msdyn_status) <br></br>Tilan syy (msdyn_statusreason) <br></br>Hylkäyksen syy (msdyn_rejectionreason) |
| Avointen työpaikkojen historia | Avoin työpaikka (msdyn_JobopeningId) <br></br>Tila (msdyn_jobopeningstatus) <br></br>Tilan syy (msdyn_jobopeningstatusreason) |
| Ehdokkaan historia | Ehdokas (msdyn_CandidateId) |
