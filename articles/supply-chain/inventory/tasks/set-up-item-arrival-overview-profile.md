---
title: "Määritä nimikkeen saapumisen yhteenvedon profiili"
description: "Tässä tehtävässä määritetään saapumisen yleiskuvaprofiili."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: b971e72febbd78ff7c27ad2029e5061b978dc44e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-an-item-arrival-overview-profile"></a>Määritä nimikkeen saapumisen yhteenvedon profiili

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtävässä määritetään saapumisen yleiskuvaprofiili. Saapumisen yleiskuvaprofiili on sääntökokoelma, jota käytetään, kun käyttäjä Saapumisten yhteenveto -sivun. Voit käyttää tätä menettelyä esittely-yrityksessä USMF. Yleensä vastaanottoassistentti tekee tämän menettelyn.





1. Valitse Inventoinnin- ja varastonhallinta > Asetukset > Jakelu > Saapumisen yleiskuvaprofiilit.
2. Valitse Uusi.
    * Koska työskentelet lähes samassa varastossa, jossa täydet kuormat puretaan, sinun kannattaa luoda saapumisen yleiskuvaprofiili vastaanotettujen nimikkeiden rekisteröintiprosessia varten.  
3. Kirjoita Saapumisen yleiskuvaprofiilin nimi -kenttään arvo.
4. Valitse vaihtoehto Näytä rivit -kentässä.
    * Määritä, mitä rivejä vastaanotoissa näytetään: Kaikki – Näytetään kaikki rivit tilasta riippumatta.   Käsittelyssä – Näyttää vastaanotot, joiden etenemisen tila on Valmis tai Osittain. Se tarkoittaa, että jokaiselle riville on saapumisen kirjauskansioon rekisteröity koko määrä tai osittainen määrä.   Ei valmis – Näyttää vastaanotot, joiden etenemisen tila on Ei mitään tai Osittain. Se tarkoittaa, että millekään riville ei ole saapumisen kirjauskansioon rekisteröity määrää tai rekisteröitynä on vain osittainen määrä.  
5. Laajenna tai tiivistä Saapumisasetukset-osa.
6. Kirjoita arvo Päivää eteenpäin -kenttään.
    * Tämä määrittää suodattimen, joka näyttää muutaman seuraavan päivän kuluessa vastaanotettavat vastaanottorivit (määrittämästäsi numerosta riippuen).  
7. Kirjoita arvo Päivää taaksepäin -kenttään.
    * Tämä määrittää suodattimen, joka näyttää vastaanottorivit, joiden odotetaan saapuvan tiettyjen päivien kuluttua.  
8. Kirjoita arvo Varastot-kenttään.
    * Suodata vähintään yhden varaston perusteella.  
9. Valitse arvo Toimitustapa-kenttään.
    * Tämä määrittää suodatuksen, jolla näytetään vain tätä toimitustapaa käyttävät vastaanottorivit.  
10. Valitse Nimi-kentässä WHS.
11. Valitse varasto 24 Varasto-kentästä.
    * Tämä on oletusvarasto, jota käytetään tätä profiilia käyttävillä rekisteröidyillä vastaanottoriveillä.  
12. Valitse Sijainti-kentästä Lastauspaikan ovi.
    * Tämä on oletustoimipaikka, jota käytetään tätä profiilia käyttävillä rekisteröidyillä vastaanottoriveillä.  
13. Laajenna tai tiivistä Saapumiskyselyn tiedot -osa.
14. Valitse toimipaikka 2 Rajoita toimipaikkaan -kenttään.
    * Tämä määrittää suodatuksen, jolla näytetään vain tämän toimipaikan vastaanottorivit.  
15. Määritä Ostotilaukset-kentän arvoksi Kyllä.
    * Valitse vastaanottorivit ostotilauksista.  
16. Määritä Siirtotilaukset-kentän arvoksi Kyllä.
    * Valitse vastaanottorivit siirtotilauksista.  
17. Valitse Tallenna.
18. Sulje sivu.
