---
title: Työsuorituksen arviointien luominen
description: Tässä aiheessa opastetaan suorituskykyarvioinnin luonti sekä kuvaillaan arvioinnin eri osien tarkoitus.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EssWorkspace, HcmDiscussionNewDialog, HcmDiscussion, HcmDiscussionChangeSettings, HcmDiscussionAddGoalDialog, HcmTopicCreate, HcmMeasurementDetailDialog, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67a001926c0d5021d952f9b678ec128c68511a8f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696037"
---
# <a name="create-performance-reviews"></a>Työsuorituksen arviointien luominen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]


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
    - Ota tämän osan tarkastelua varten työntekijäluokitusten näyttämisen parametriasetukset käyttöön **Henkilöstöhallinnon jaetut parametrit** -sivulla.  

31. Valitse **Kuittaukset**-välilehti. Jos arvioinnissa käytetään työnkulkua, hyväksynnät näkyvät vasta, kun työnkulku on valmis. Jos työnkulku ei ole käytössä, sekä työntekijä että esimies näytetään tässä. **Hyväksyntä**-kohdan **Pakollinen**-valintaruutu on valittuna arviointityypin perusteella.  
32. Valitse **Yleinen**-välilehti.

    - Suorituskaudelle luodaan oletuksena aloitus- ja päättymispäivämäärät. Päivämäärät ovat muokattavissa.  
    - Tiloilla hallitaan arvioinnin käyttöoikeutta. **Ei alkanut** -tila sallii kaikkien käyttäjien muokata arviointia. **Käsittelyssä**-tilassa olevaa arviointia voi tarkastella ja muokata vain työntekijä. **Valmis tarkistettavaksi** -tilassa olevaa arviointia voi tarkastella ja muokata vain esimies. **Lopullinen arvostelu** -tila sallii sekä työntekijän että esihenkilön tarkastella ja muokata arvostelua, jos **Salli lopullisen arvostelun muokkaukset** -asetus on valittuna arvostelutyypissä. Tilat **Valmis** ja **Peruutettu** asettavat arvioinnin vain luku -tilaan. Jos tarkistus on **Hylätty** ja lähetetään takaisin työntekijälle, sekä työntekijä että esimies voivat tehdä tarvittavat muokkaukset, jotta työntekijä voi lähettää sen uudelleen.

33. Kirjoita arvo kenttään **Yhteenveto**.
34. Valitse **Arviointi**-välilehti. Arvioinnin tilan vaihtuessa työntekijä ja esimies voivat lisätä kommentteja kullekin tavoitteelle tai osaamisalueelle.  
35. Valitse **Kuittaukset**-välilehti. Työntekijä ja esimies voivat kuitata arvioinnin. Kun kaikki tarvittavat hyväksynnät on tehty, tilaksi muutetaan **Valmis**, eikä muutoksia voi enää tehdä.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
