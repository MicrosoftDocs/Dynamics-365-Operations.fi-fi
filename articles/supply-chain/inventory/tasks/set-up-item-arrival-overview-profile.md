---
title: Määritä nimikkeen saapumisen yhteenvedon profiili
description: Tässä aiheessa keskitytään saapumisen yleiskuvaprofiilin määrittämiseen.
author: ShylaThompson
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0ffcef15515a81aecbf1f1257f8fa7f46a2b876
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/03/2021
ms.locfileid: "6335447"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>Määritä nimikkeen saapumisen yhteenvedon profiili

[!include [banner](../../includes/banner.md)]]

Tässä aiheessa keskitytään saapumisen yleiskuvaprofiilin määrittämiseen. Saapumisen yleiskuvaprofiili on sääntökokoelma, jota käytetään, kun käyttäjä Saapumisten yhteenveto -sivun. Voit käyttää tätä menettelyä esittely-yrityksessä USMF. Yleensä vastaanottoassistentti tekee tämän menettelyn.

1. Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Asetukset > Jakelu > Saapumisen yleiskuvaprofiilit**.
2. Valitse **Uusi**. Koska työskentelet lähes samassa varastossa, jossa täydet kuormat puretaan, sinun kannattaa luoda saapumisen yleiskuvaprofiili vastaanotettujen nimikkeiden rekisteröintiprosessia varten.  
3. Kirjoita **Saapumisen yleiskuvaprofiilin nimi** -kenttään arvo.
4. Valitse vaihtoehto **Näytä rivit** -kentässä. Määritä vastaanotoissa näytettävät rivit:  

    - **Kaikki** – Näyttää kaikki rivit tilasta huolimatta.   
    - **Käsittelyssä** – Näyttää vastaanotot, joiden etenemisen tila on Valmis tai Osittain. Se tarkoittaa, että jokaiselle riville on saapumisen kirjauskansioon rekisteröity koko määrä tai osittainen määrä.   
    - **Ei valmis** – Näyttää vastaanotot, joiden etenemisen tila on Ei mitään tai Osittain. Se tarkoittaa, että millekään riville ei ole saapumisen kirjauskansioon rekisteröity määrää tai rekisteröitynä on vain osittainen määrä.  

5. Laajenna tai tiivistä **Saapumisasetukset**-osa.
6. Kirjoita arvo **Päivää eteenpäin** -kenttään. Tämä määrittää suodattimen, joka näyttää muutaman seuraavan päivän kuluessa vastaanotettavat vastaanottorivit (määrittämästäsi numerosta riippuen).  
7. Kirjoita arvo **Päivää taaksepäin** -kenttään. Tämä määrittää suodattimen, joka näyttää vastaanottorivit, joiden odotetaan saapuvan tiettyjen päivien kuluttua.  
8. Kirjoita arvo **Varastot**-kenttään. Suodata vähintään yhden varaston perusteella.  
9. Valitse arvo **Toimitustapa**-kenttään. Tämä määrittää suodatuksen, jolla näytetään vain tätä toimitustapaa käyttävät vastaanottorivit.  
10. Valitse **Nimi**-kentässä WHS.
11. Valitse varasto 24 **Varasto**-kentästä. Tämä on oletusvarasto, jota käytetään tätä profiilia käyttävillä rekisteröidyillä vastaanottoriveillä.  
12. Valitse **Sijainti**-kentästä **Lastauspaikan ovi**. Tämä on oletustoimipaikka, jota käytetään tätä profiilia käyttävillä rekisteröidyillä vastaanottoriveillä.  
13. Laajenna tai tiivistä **Saapumiskyselyn tiedot** -osa.
14. Valitse toimipaikka 2 **Rajoita toimipaikkaan** -kenttään. Tämä määrittää suodatuksen, jolla näytetään vain tämän toimipaikan vastaanottorivit.  
15. Määritä **Ostotilaukset**-kentän arvoksi **Kyllä**. Valitse vastaanottorivit ostotilauksista.  
16. Määritä **Siirtotilaukset**-kentän arvoksi **Kyllä**. Valitse vastaanottorivit siirtotilauksista.  
17. Valitse **Tallenna**.
18. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]