---
title: Liiketoimintaprosessien virallistaminen
description: Voit luoda liiketoimintaprosessiominaisuudella organisaatiossa suoritettavien prosessien liiketoimintaprosessimallin.
author: ShielaSogge
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: ShielaS
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 812db9f1d319e4d16f83700a7153a0a3b318963e
ms.openlocfilehash: 48f80eac5009e1a241d501b0c4a3a70b78f5d709
ms.contentlocale: fi-fi
ms.lasthandoff: 03/23/2018

---
# <a name="formalize-business-processes"></a>Liiketoimintaprosessien virallistaminen
Voit luoda liiketoimintaprosessiominaisuudella organisaatiossa suoritettavien prosessien liiketoimintaprosessimallin. Yrityksessä voi olla esimerkiksi henkilöstöhallinnon tarkistus joka vuosi. Luotava malli voi seurata kaikkia tarkistuksen tehtäviä. Mallin avulla voidaan varmistaa, että kaikki tehtävät on tehty prosessin valmistuessa. Tarvittaessa sen avulla voidaan varmistaa, että tehtävät on suoritettu oikeassa järjestyksessä. Malleja voidaan käyttää uudelleen toistuvissa prosesseissa tai ne voidaan kopioida aloituskohdaksi uusia luotaessa.

Kun malli on luotu, prosessi voidaan aloittaa ja sitä voi seurata Liiketoimintaprosessi-työtilan avulla.  Kun liiketoimintaprosessi aloitetaan, nämä tehtävät määritetään soveltuville henkilöille ja niillä on määräpäivä. Näitä osia käsitellään tarkemmin myöhemmin.

## <a name="business-process-template"></a>Liiketoimintaprosessimalli
Liiketoimintaprosessimalli sisältää ryhmän liiketoimintaprosessin tehtäviä. Henkilöstöpäälliköt ja avustajat voivat luoda liiketoimintaprosesseja oletusarvoisesti.  Tämän voi kuitenkin muuttaa suojausmäärityksessä Ylläpidä yleisiä liiketoimintaprosesseja -tehtävää muokkaamalla.

Jokaiselle prosessille voidaan määrittää prosessin omistaja.  Prosessin omistaja näkee kaikki prosessin tehtävät ja voi määrittää tehtäviä uudelleen tai muuttaa eräpäiviä.  Esimerkiksi henkilöstöosaston johtaja voi luoda etujen tarkistuksen liiketoimintaprosessimallin.  Etuuspäällikkö voidaan määrittää prosessin omistajaksi, jotta hän saa näkemyksen asioista, jotka on suoritettava arvioinnin osana.  Prosessin omistaja ei voi luoda tai poistaa aktiivisia liiketoimintaprosesseja tai liiketoimintaprosessimalleja.

## <a name="task"></a>Tehtävä
Liiketoimintaprosessi muodostuu tavallisesti useista tehtävistä. Jotkin tehtävät voidaan tehdä valmiiksi Dynamics 365 for Talentissa[?]. Tällainen tehtävä on esimerkiksi sisäisen kurssivalikoiman arviointi. Tässä tapauksessa valikkonimike valitaan Tehtävän linkki -kentässä. Muut tehtävät saattavat sisältää verkkosivuston lomakkeiden tarkastelun tai täyttämisen. Kun tehtävälinkkikentän URL-osoite valitaan, verkko-osoite voidaan kirjoittaa. Voit antaa tähän kenttään sekä ulkoisten että sisäisten sivustojen URL-osoitteita. Voit luoda tehtäviä myös manuaalisesti suoritettaville tehtäville, kuten kaikkien rakenteiden helppokäyttöisyyden arviointi. Tässä tapauksessa tehtävän linkki ei ole pakollinen. Tämän joustavuuden ansiosta voit seurata useita erilaisia tehtäviä kattavana prosessina.

Tehtävät voidaan määrittää toimelle tai tietylle työntekijälle. Esimerkiksi etupäällikkö suorittaa aina vakuutusmaksujen tarkistukset.   Kun luot tätä tehtävää, valitse ensin toimen toimeksiantotyyppi ja sitten toimiluettelosta etuuspäällikkö. Kun prosessi alkaa, tehtävä määritetään etuuspäällikkönä toimivalle työntekijälle. Voit myös määrittää tehtävän tietylle työntekijälle valitsemalla Työntekijä Määrityksen tyyppi -kentässä ja valitsemalla sitten henkilön.

Tehtävän eräpäivät määräytyvät prosessin alussa annettujen tavoitepäivämäärien mukaan. Osa tehtävistä on suoritettava ennen tavoitepäivämäärää, kun taas osa voidaan suorittaa tavoitepäivämäärän jälkeen.  Tehtävää määritettäessä annetaan tavoitepäivään suhteessa oleva eräpäivä Eräpäivän siirtymä tavoitepäivämäärästä -kentässä. Oletetaan esimerkiksi, että etupäällikön on tarkistettava vakuutusmaksut 10 päivää ennen henkilöstöhallinnon tarkistuksen valmistumista. Luodun tehtävän eräpäivä on suhteessa tavoitepäivään -10. Niinpä jos prosessi käynnistetään 13. toukokuuta, tehtävä erääntyy 3. toukokuuta. Huomautus: Eräpäiviä voi muokata myös prosessin käynnistyttyä.

Monimutkaisissa tehtävissä on useita vaiheita tai tehtävät on suoritettava erikseen, jotta niistä saadaan lisätietoja. Voit lisätä tehtävään ohjeita. Myös ohjeissa voi käyttää tekstimuotoiluja. Ohjeissa voi olla tehtävän suorittamisesta koskevia lisätietoja sille henkilölle, joka on määritetty tehtävän suorittajaksi.

Prosessin aloittaminen Prosessi voidaan käynnistää liiketoimintaprosessimallista valitsemalla Käynnistä prosessi.  Kun prosessi aloitetaan, tehtävät luodaan liiketoimintaprosessimalliin sisällytetyissä tehtävissä määritetyille valituille työntekijöille ja/tai toimille. Jokaiselle tehtävälle määritetään myös eräpäivä lisäämällä siirtymäpäiviä tai vähentämällä niitä tavoitepäivämäärästä (katso lisätietoja siirtymäpäivistä Tehtävä-osasta). Aktiivisia liiketoimintaprosesseja voidaan tarkastella Liiketoimintaprosessit-työtilassa. 

## <a name="employee-self-service"></a>Työntekijän itsepalvelu
Kun tehtävä on määritetty työntekijälle, heille määritettyjä tehtäviä voi tarkastella työntekijän itsepalvelusivulla. Työntekijät, joille on määritetty liiketoimintaprosessitehtävä, näkevät tehtävän, sen kuvauksen, suoritusohjeet ja yhteyshenkilön nimen. He voivat avata liittyvän Dynamics365 -sivun tai verkkosivun Työntekijän itsepalvelu -sivulta. Tehtävät voidaan merkitä keskeneräisiksi, peruutetuiksi tai valmiiksi.

## <a name="business-process-workspace"></a>Liiketoimintaprosessin työtila
HR-ammattilaiset voivat tarkastella aktiivisia liiketoimintaprosesseja liiketoimintaprosessin työtilassa. Työtilassa on luettelo kaikista aktiivisista prosesseista ja kuhunkin prosessiin liitetyistä tehtävistä. Täydellinen luettelo voidaan suodattaa eräpäivän perusteella. Sivulla on myös luettelo erääntyneistä tehtävistä ja HR-työntekijälle määritetyistä tehtävistä. Ne voivat myös päivittää kaikkien tehtävien tilan ja tarvittaessa määrittää tehtävät uudelleen, jotta liiketoimintaprosessi kokonaisuudessaan etenee.

## <a name="my-business-processes-workspace"></a>Omat liiketoimintaprosessit -työtila
Prosessin omistajat voivat tarkastella heille määritettyjä aktiivisia liiketoimintaprosesseja Oma liiketoimintaprosessi -työtilassa. Työtilassa on luettelo kaikista aktiivisista prosesseista ja liitetyistä tehtävistä, jotka käyttäjä omistaa.  Täydellinen luettelo voidaan suodattaa eräpäivän perusteella. Sivulla on myös luettelo prosessin omistajalle määritetyistä tehtävistä. Prosessin omistaja voi myös päivittää kaikkien tehtävien tilan sekä määrittää minkä tahansa tehtävän uudelleen.

## <a name="navigating-business-processes"></a>Siirrytään liiketoimintaprosesseihin
1.   Voit lisätä liiketoimintaprosessimallin siirtymällä liiketoimintaprosessien linkkeihin ja valitsemalla Liiketoimintaprosessien hallinta.
 - a.   Uusi-vaihtoehto luo uuden mallin.
 - b.   Kopioi mallista -vaihtoehto kopioi valitun mallin uuteen malliin.
 - c.   Käynnistä prosessi -vaihtoehto käynnistää valitun liiketoimintaprosessin, määrittää tehtävät ja laskee eräpäivät.  
2.  Voit tarkastella aktiivisia prosesseja ja liitettyjä tehtäviä siirtymällä liiketoimintaprosessien työtilaan.

