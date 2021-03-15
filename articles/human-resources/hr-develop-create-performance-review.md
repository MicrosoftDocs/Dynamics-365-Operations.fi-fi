---
title: Työsuorituksen arviointien luominen
description: Tässä aiheessa opastetaan suorituskykyarvioinnin luonti sekä kuvaillaan arvioinnin eri osien tarkoitus.
author: andreabichsel
manager: tfehr
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EssWorkspace, HcmDiscussionNewDialog, HcmDiscussion, HcmDiscussionChangeSettings, HcmDiscussionAddGoalDialog, HcmTopicCreate, HcmMeasurementDetailDialog, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e83bcf60e494e6f04387727bedf41175faa07557
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115797"
---
# <a name="create-performance-reviews"></a>Työsuorituksen arviointien luominen


Tässä aiheessa opastetaan suorituskykyarvioinnin luonti sekä kuvaillaan arvioinnin eri osien tarkoitus. Tämä menettelyn luomisessa käytettiin USMF-yrityksen demotietoja.

1. Valitse aloitussivulla **Työntekijän itsepalvelu** -työtila.
2. Luo arviointi napsauttamalla **Uusi arviointi**.
3. Anna tai valitse **Arviointityyppi**-kentässä arvo.
4. Syötä tai valitse arvo kentässä **Suorituskausi**.
5. Syötä päivämäärä **Päättymispäivä**-kenttään.
6. Valitse **OK**. Voit luoda arvioinnin myös mallista. Tämä on paras tapa luoda arviointi, koska jokainen osa sisältää tiedot, jotka tarvitaan arvioinnin aloittamiseen.  
7. Voit näyttää tai piilottaa välilehdet, kuten Liitteet-välilehden:

    1. Valitse pudotusvalikkoikkunassa **Näytä osat** avataksesi valikkoikkunan.
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
18. Valitse **Lisää mitta** avataksesi valintaikkunan.
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
    - Jotta voit tarkastella tätä osaa, ota käyttöön työntekijän luokitukset näyttävä parametriasetus.  

31. Valitse **Kuittaukset**-välilehti. Jos arvioinnissa käytetään työnkulkua, hyväksynnät näkyvät vasta, kun työnkulku on valmis. Jos työnkulku ei ole käytössä, sekä työntekijä että esimies näytetään tässä. Pakollinen-valintaruutu on valittuna arviointityypin perusteella.  
32. Valitse **Yleinen**-välilehti.

    - Suorituskaudelle luodaan oletuksena aloitus- ja päättymispäivämäärät. Päivämäärät ovat muokattavissa.  
    - Tiloilla hallitaan arvioinnin käyttöoikeutta. **Ei alkanut** -tila sallii kaikkien käyttäjien muokata arviointia. **Käsittelyssä**-tilassa olevaa arviointia voi tarkastella ja muokata vain työntekijä. **Valmis tarkistettavaksi** -tilassa olevaa arviointia voi tarkastella ja muokata vain esimies. **Lopullinen arviointi** -tila mahdollistaa sekä työntekijälle että esimiehelle arvioinnin tarkastelun. Muokkaaminen on mahdollista, jos se on otettu käyttöön arviointityypissä. Tilat **Valmis** ja **Peruutettu** asettavat arvioinnin vain luku -tilaan. Jos tarkistus on **Hylätty** ja lähetetään takaisin työntekijälle, sekä työntekijä että esimies voivat tehdä tarvittavat muokkaukset, jotta työntekijä voi lähettää sen uudelleen.

33. Kirjoita arvo kenttään **Yhteenveto**.
34. Valitse **Arviointi**-välilehti. Arvioinnin tilan vaihtuessa työntekijä ja esimies voivat lisätä kommentteja kullekin tavoitteelle tai osaamisalueelle.  
35. Valitse **Kuittaukset**-välilehti. Työntekijä ja esimies voivat kuitata arvioinnin. Kun kaikki tarvittavat hyväksynnät on tehty, tilaksi muutetaan **Valmis**, eikä muutoksia voi enää tehdä.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]