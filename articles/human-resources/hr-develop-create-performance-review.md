---
title: Työsuorituksen arviointien luominen
description: Tässä artikkelissa opastetaan suorituskykyarvioinnin luonti sekä kuvaillaan arvioinnin eri osien tarkoitus.
author: andreabichsel
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EssWorkspace, HcmDiscussionNewDialog, HcmDiscussion, HcmDiscussionChangeSettings, HcmDiscussionAddGoalDialog, HcmTopicCreate, HcmMeasurementDetailDialog, HcmPerfJournalAdd
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 50ef3f305756f1ab0db895854cd7e1c71237cb48
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008882"
---
# <a name="create-performance-reviews"></a>Työsuorituksen arviointien luominen



Tässä artikkelissa opastetaan suorituskykyarvioinnin luonti sekä kuvaillaan arvioinnin eri osien tarkoitus. Tämä menettelyn luomisessa käytettiin USMF-yrityksen demotietoja.

1. Valitse aloitussivulla **Työntekijän itsepalvelu** -työtila.
2. Luo arviointi napsauttamalla **Uusi arviointi**.
3. Anna tai valitse **Arviointityyppi**-kentässä arvo.
4. Syötä tai valitse arvo kentässä **Suorituskausi**.
5. Syötä päivämäärä **Päättymispäivä**-kenttään.
6. Valitse **OK**. Voit luoda arvioinnin myös mallista. Tämä on paras tapa luoda arviointi, koska jokainen osa sisältää tiedot, jotka tarvitaan arvioinnin aloittamiseen.  
7. Voit näyttää tai piilottaa välilehdet, kuten Liitteet-välilehden:

    1. Avaa pudotusvalikkoikkuna valitsemalla toimintoruudussa **Näytä osat**.
    1. Näytä tai piilota Liitteet-välilehti valitsemalla **Näytä liitteet**-kentässä **kyllä** tai **ei**.
    1. Valitse **Tallenna**.

8. Lisää tavoite valitsemalla **Lisää tavoite arviointiin**. Kun olet valmis, valitse **OK**.
9. Avaa valintaikkuna valitsemalla **Lisää osaaminen**.
10. Kirjoita **Otsikko**-kenttään arvo.
11. Lisää **kuvaus** -kentässä `Increase customer skills by working with the support team`.
12. Valitse **OK**.
13. Valitse **Tiivistä kaikki**.
14. Valitse **Laajenna kaikki**.
15. Valitse **Lisää kommentti**.
16. Valitse **Kirjaa**.
17. Valitse **Mittaukset**-välilehti.
18. Avaa valintaikkuna valitsemalla **Lisää mitta**.
19. Syötä tai valitse arvo kentässä **Mitta**.
26. Syötä **Tavoitemäärä** -kenttään haluamasi luku.
20. Valitse **OK**.
21. Valitse **Aktiviteetit**-välilehti.
22. Valitse **Lisää**.
23. Kirjoita **Otsikko**-kenttään arvo.
24. Kirjoita **Kuvaus**-kenttään arvo.
25. Syötä päivämäärä **Aloituspäivä**-kenttään.
26. Syötä **Valmistumispäivämäärä**-kenttään päivämäärä.
27. Valitse **Kehityssuunnitelma**-kentässä **Kyllä**.
28. Kirjoita arvo kenttään **Avainsanat**.
29. Valitse **Tallenna**.
30. Valitse **Luokitukset**-välilehti.  

    - Työntekijät ja esimiehet voivat tehdä luokituksen nopeasti **Luokituksen lisätiedot** -pikavälilehdellä. Jos painotukset ovat käytössä, pisteiden painotettu arvo lasketaan automaattisesti.  
    - Jotta näet tämän osan, ota käyttöön työntekijän luokitukset näyttävä parametriasetus.  

31. Valitse **Kuittaukset**-välilehti. Jos arvioinnissa käytetään työnkulkua, hyväksynnät näkyvät vasta, kun työnkulku on valmis. Jos työnkulku ei ole käytössä, sekä työntekijä että esimies näytetään tässä. Pakollinen-valintaruutu on valittuna arviointityypin perusteella.  
32. Valitse **Yleinen**-välilehti.

    - Suorituskaudelle luodaan oletuksena aloitus- ja päättymispäivämäärät. Päivämäärät ovat muokattavissa.  
    - Tiloilla hallitaan arvioinnin käyttöoikeutta. **Ei alkanut** -tila sallii kaikkien käyttäjien muokata arviointia. **Käsittelyssä**-tilassa olevaa arviointia voi tarkastella ja muokata vain työntekijä. Valmis tarkistettavaksi -tilassa olevaa arviointia voi tarkastella ja muokata vain esimies. Lopullinen arviointi -tila mahdollistaa sekä työntekijälle että esimiehelle arvioinnin tarkastelun. Muokkaaminen on mahdollista, jos se on otettu käyttöön arviointityypissä. Tilat **Valmis**, **Peruutettu** ja **Hylätty** asettavat arvioinnin vain luku -tilaan.  

33. Kirjoita arvo kenttään **Yhteenveto**.
34. Valitse **Arviointi**-välilehti. Arvioinnin tilan vaihtuessa työntekijä ja esimies voivat lisätä kommentteja kullekin tavoitteelle tai osaamisalueelle.  
35. Valitse **Kuittaukset**-välilehti. Työntekijä ja esimies voivat kuitata arvioinnin. Kun kaikki tarvittavat hyväksynnät on tehty, tilaksi muutetaan **Valmis**, eikä muutoksia voi enää tehdä.  

