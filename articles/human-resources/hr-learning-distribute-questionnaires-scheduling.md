---
title: Kyselylomakkeiden jakaminen aikatauluttamalla
description: Kyselylomakkeiden ajoituksen avulla voit suunnitella ja jakaa kyselylomakkeita useille vastaajille.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0cd101bfe88ae1acb051ba11a676da66ef6a3db6
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115459"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Kyselylomakkeiden jakaminen aikatauluttamalla

Kyselylomakkeiden ajoituksen avulla voit suunnitella ja jakaa kyselylomakkeita useille vastaajille. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.

## <a name="create-a-questionnaire-schedule"></a>Kyselylomakkeen aikataulun luominen

1. Siirry kohtaan Kyselylomake > Jaa > Kyselylomakkeiden aikataulut.

2. Valitse Uusi.

3. Syötä arvo Aikataulutus-kenttään.

4. Kirjoita arvo Kuvaus-kenttään.
    * Määrittää aikataululle Anonyymi-arvon, jos vastaukset on kirjattava ilman niihin liittyviä nimiä.  
    * Nimettömien tulosten käyttäminen on määritettävä ensin henkilöstöhallinnon parametreissa.  

5. Valitse Tyyppi-kentästä suunnittelun tyyppi.  Tässä esimerkissä käytetään Tyytyväisyys-tyyppiä.

6. Etsi haluamasi tietue luettelosta ja valitse se.

7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

8. Syötä Päivämäärään-kenttään päivämäärä.

9. Laajenna Työntekijän itsepalvelun sähköpostiosoite -osa.

10. Kirjoita arvo Aihe-kenttään.

    * Esimerkki: kyselylomake käytettävissä  

11. Kirjoita Teksti-kenttään sähköpostiviestin leipätekstissä näkyvä teksti. Huomaa, että muuttujaa voidaan käyttää paikkamerkkinä järjestelmän arvoille.

    * Esimerkki: Hyvä %P%! Kirjaudu sisään työntekijän itsepalveluun ja täytä työterveyden kyselylomake.  Contoso  

12. Valitse Tallenna.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Vastattavien kyselylomakkeiden sekä valituille vastaajille käytettävien kyselyjen valitseminen asetustietojen avulla.

1. Valitse Asetuksen tiedot.

2. Valitse luettelosta kysely, jolla etsit järjestelmästä kyselylomakkeen vastaajia.

    * Esimerkki: työntekijät  

3. Valitsemalla Tarkastele tai muokkaa kyselyä voit valita tietyt henkilöt. Muokkaamalla kyselyä voit etsiä tiettyjä ehtoja vastaavia henkilöitä.

    * Huomaa, että kaikkien vastaajien on oltava järjestelmän käyttäjiä.  

4. Merkitse Henkilö-rivi luettelossa.

5. Syötä tai valitse arvo Ehdot-kenttään.

    * Valitse Julia Funderburk  

6. Valitse luettelosta Julia Funderburk

7. Valitse OK.

8. Valitse kyselyt-välilehti.

9. Laajenna puussa Tyytyväisyyskysely-lomaketyypin solmu -kohta.

10. Merkitse puussa "Työterveyden arviointi" -kohdan valintaruutu.

11. Valitse OK.

12. Valitse Suunniteltu vastausistunto.

    * Huomaa, että suunnitellut vastausistunnot on luotu kullekin valitulle/kysellylle käyttäjälle.  

13. Sulje sivu.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Kyselylomakkeen ajoituksen käynnistäminen, jotta kyselylomake voidaan tarjota vastaajien täytettäväksi.

1. Valitse Toiminnot.

2. Valitse Käynnistys.

3. Valitse OK.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Sähköpostiviestin lähettäminen vastaajille käytettävissä olevasta kyselylomakkeesta.

1. Valitse Toiminnot.

2. Valitse Lähetä sähköposti.

3. Valitse Peruuta.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Kyselylomakkeen täyttäjiksi tarkoitettujen käyttäjien valvominen suunniteltujen vastausistuntojen avulla.

1. Valitse Suunniteltu vastausistunto.

    * Kun ajoitettu istunto voidaan lopettaa, poista mahdollinen jäljellä oleva suunniteltu vastausistunto.  

2. Valitse Poista.

3. Valitse Kyllä.

4. Sulje sivu.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Ajoituksen voi lopettaa, kun kaikki vastaukset ovat saapuneet ja/tai kaikki jäljellä olevat suunnitellut vastausistunnot on poistettu.

1. Valitse Toiminnot.
2. Valitse Lopetus.
3. Valitse OK.



[!INCLUDE[footer-include](../includes/footer-banner.md)]