--- 
title: "Aallon käsittelyn kokoonpano"
description: "Tässä ohjeessa kuvataan ehdot, jotka määrittävät kuinka aallon käsittelyn yhteydessä varastolle luotu työ käsitellään, ja käsitelläänkö aallot manuaalisesti vai automaattisesti."
author: YuyuScheller
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f7a6db585468c235e07c4a0117a83995ec93f4b0
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="configure-wave-processing"></a>Aallon käsittelyn kokoonpano

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä ohjeessa kuvataan ehdot, jotka määrittävät kuinka aallon käsittelyn yhteydessä varastolle luotu työ käsitellään, ja käsitelläänkö aallot manuaalisesti vai automaattisesti. Voit määrittää ehdot asettamalla aaltomallit ja kyselyt, jotka vastaavat aaltoa myyntitilausten, tuotantotilausten ja kanban-tilausten vapautettujen rivien kanssa. Aallon käsittelyä käytetään varastoissa, jotka käyttävät varastonhallintamoduulin toimintoja, ei varastoissa, joissa käytetään inventoinninhallintamoduulin toimintoja. Voit suorittaa tämän menettelyn esittely-yrityksessä USMF.

1. Valitse Varastonhallinta > Asetukset > Aallot > Aaltomallit.
2. Valitse Uusi.
3. Syötä Aaltomallin nimi -kenttään arvo.
    * Aaltomallia määrittäessäsi voit määrittää järjestyksen, jossa mallit sovitetaan vapautettuihin myyntitilausten, tuotantotilausten tai kanbanien riveihin. Kun rivi on vapautettu varastoon tai tuotantoon, siinä käytetään ensimmäistä ehtoja vastaavaa aaltomallia. Suosittelemme, että sijoitat tarkimmin määritellyt kriteerit sisältävän mallit luettelon alkuun. Mitä laajempi ehto on, sitä todennäköisemmin rivi täyttää ehdon, ja tämä saattaa johtaa rivien määrittämisen väärään aaltoon.  
4. Kirjoita Aaltomallin kuvaus -kenttään arvo.
5. Syötä tai valitse arvo Toimipaikka-kenttään.
    * Jos käytössä on USMF, valitse toimipaikka 2.  
6. Anna tai valitse Varasto-kentässä arvo.
    * Jos käytössä on USMF, voit valita varaston 24.  
7. Aseta Automatisoi aallon luonti -kentän arvoksi Kyllä.
    * Valitse tämä vaihtoehto, jos haluat luoda aallon automaattisesti, kun myyntitilaus, tuotantotilaus tai kanban vapautetaan varastoon.  
8. Aseta Käsittele aalto, kun se vapautetaan varastoon -asetuksen arvoksi Kyllä. 
    * Valitse tämä vaihtoehto, jos haluat käsitellä automaattisesti aallon ja luoda työn, kun rivi vapautetaan varastoon.  
9. Aseta Automatisoi aallon vapautus -asetuksen arvoksi Kyllä. 
    * Valitse tämä vaihtoehto, kun haluat vapauttaa aallon automaattisesti. Keräilytyö luodaan ja määritetään mobiililaitteiden käytettäväksi.  
10. Aseta Määritä avoimiin aaltoihin -asetuksen arvoksi Kyllä. 
    * Rivit määritetään aaltoihin aaltomallin kyselysuodattimen perusteella.  
11. Aseta Käsittele aalto automaattisesti raja-arvossa -asetuksen arvoksi Kyllä. 
    * Valitse tämä vaihtoehto, jos haluat käsitellä aallon automaattisesti, kun sen arvot saavuttavat Aallon raja-arvot -kenttäryhmässä painolle, lähetykselle ja riville määritetyt raja-arvot. Tämä vaihtoehto on käytettävissä vain, jos Aaltomallin tyyppi -kentässä on valittu Lähetys.  
12. Aseta Automatisoi täydennystyö -asetuksen arvoksi Kyllä. 
    * Valitsemalla tämän vaihtoehdon voit luoda täydennystyön tarpeen mukaan ja vapauttaa sen automaattisesti. Sinun on lisättävä täydennyksen aaltomenetelmä aaltomalliin ja luotava täydennysmalli, jonka tyyppi on Aallon kysyntä.  
13. Laajenna Menetelmät-osa.
    * Aaltomallimenetelmien avulla voit ohjata tehtäväsarjaa, jonka kukin aalto käy läpi käsittelyn aikana. Sinulla voi esimerkiksi olla menetelmä aallon täydentämiseen. Kun lisäät menetelmän, se tulee näkyviin automaattisesti tarvittavissa kohteissa vaiheketjussa. Jos olet asettanut Automatisoi täydennystyön vapautus -asetuksen arvoksi Kyllä, täydennysmenetelmä on lisättävä tähän.  
    * Aaltomääritteet toimivat suodattimina rajoittaen aaltoa käyttäviä nimikkeitä. Voit esimerkiksi määrittää nimikeryhmän.  
14. Valitse Tallenna.
15. Sulje sivu.
16. Valitse Varastonhallinta > Asetukset > Varastonhallinnan parametrit.
17. Laajenna Aallon käsittely -osa.
18. Anna tai valitse arvo Aallon käsittelyn eräryhmä -kenttään.
19. Aseta Aallon käsittelyn eräryhmä -asetuksen arvoksi Kyllä.
20. Anna Odota lukitusta (ms) -kenttään numero.
    * Kirjoita millisekunteina aika, jonka kohdistusvaihe odottaa järjestelmäresurssia, joka on toisen kohdistusvaiheen lukitsema. Kun tämä aika ylitetään, aaltoa ei käsitellä ja virhesanoma tulee näkyviin.  
21. Valitse Tallenna.
22. Sulje sivu.
23. Valitse Tuotannonhallinta > Asetukset > Tuotannonhallinnan parametrit.
24. Valitse vaihtoehto Vapauta varastoon -kentässä.
    * Myynti- ja kanbantilauksille inventaario tulee varata ennen kuin tilaus viedään varastolle. Muussa tapauksessa tietyn kohdistuksen rivejä ei voi käsitellä aallossa. Tuotantotilauksille on myös mahdollista valita osittaisen varaamisen salliminen. Tämä on hyödyllistä esimerkiksi silloin, kun sinulla on tuotannon käynnistämiseen tarvittavat materiaalit ja voit odottaa, kunnes muut materiaalit ovat käytettävissä saattaaksesi prosessin loppuun. Jos valitset tämän vaihtoehdon, pitää vapautus varastoprosessiin toistaa manuaalisesti, kun muut materiaalit tulevat käyttöön.  
25. Sulje sivu.


