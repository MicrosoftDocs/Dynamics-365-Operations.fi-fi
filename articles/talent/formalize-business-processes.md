---
title: Liiketoimintaprosessien virallistaminen
description: Tässä osassa kerrotaan miten voit käyttää liiketoimintaprosessiominaisuutta luodaksesi organisaatiossa suoritettavien prosessien liiketoimintaprosessimallin.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.openlocfilehash: 85950a1413cfd8745bb78a52eb9f7c81b8976605
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "859710"
---
# <a name="formalize-business-processes"></a>Liiketoimintaprosessien virallistaminen

[!include[banner](includes/banner.md)]

Voit luoda liiketoimintaprosessiominaisuudella organisaatiossa suoritettavien prosessien liiketoimintaprosessimallin prosesseille, jotka organisaatiosi täytyy saattaa loppuun. Yrityksen täytyy esimerkiksi suorittaa henkilöstöhallinnon (HR) tarkastus vuosittain. Tässä tapauksessa voit luoda mallin, jonka avulla voidaan seurata kaikkia tehtäviä, joka kuuluvat tarkastusprosessiin. Tämän mallin avulla voidaan taata, että kaikki tehtävät tehdään aina, kun tehdään tarkastus. Lisäksi mikäli tehtävät on suoritettava määritetyssä järjestyksessä, mallin avulla voidaan taata, että tehtävät ovat valmiita oikeassa järjestyksessä.

Malleja voidaan käyttää uudelleen toistuviin prosesseihin. Ne voidaan myös kopioida ja käyttää pohjana luotaessa uusia malleja.

Kun malli on luotu, liiketoimintaprosessi voidaan aloittaa ja sitä voi seurata **Liiketoimintaprosessi** -työtilan avulla. Kun liiketoimintaprosessi aloitetaan, nämä tehtävät määritetään soveltuville henkilöille ja niillä on määräpäivä.

## <a name="business-process-templates"></a>Liiketoimintaprosessimallit
Liiketoimintaprosessimalli sisältää ryhmän liiketoimintaprosessin tehtäviä. Henkilöstöpäälliköt ja avustajat voivat luoda liiketoimintaprosesseja oletusarvoisesti. Voit kuitenkin muuttaa rooleja, jotka voivat luoda liiketoimintaprosesseja muokkaamalla **Ylläpidä yleisiä liiketoimintaprosesseja** -velvollisuutta suojausasetuksissa .

Jokaiselle prosessille voidaan määrittää prosessin omistaja. Prosessin omistaja näkee kaikki prosessin tehtävät ja voi määrittää tehtäviä uudelleen tai muuttaa eräpäiviä. Esimerkiksi Henkilöstöhallinnon johtaja voi luoda prosessin liiketoimintamallin etujen tarkistukseen ja määrittää kompensaation ja etujen hallitsijan prosessin omistajana. Kompensaation ja etujen hallitsijalla on silloin näkyvyys tehtäviin, jotka tarkistuksen osana on suoritettava.

Prosessin omistaja ei voi luoda uusia liiketoimintaprosesseja tai liiketoimintaprosessin malleja tai poistaa aktiivista liiketoimintaprosessia tai liiketoimintaprosessin malleja.

## <a name="tasks"></a>Tehtävät
Liiketoimintaprosessi koostuu tavallisesti useista tehtävistä. Jotkin tehtävät voidaan tehdä valmiiksi Dynamics 365 for Talentissa[?]. Tällainen tehtävä on esimerkiksi sisäisen kurssivalikoiman arviointi. Tässä tapauksessa vaihtoehto on valittuna **Tehtävälinkki** -kentässä. Muut tehtävät saattavat sisältää verkkosivuston sivujen tarkastelun tai täyttämisen. Tässä tapauksessa **URL** on valittu **Tehtävälinkki** -kentässä ja Internet-osoite voidaan syöttää. Voit antaa sekä ulkoisten että sisäisten sivustojen URL-osoitteita. Voit luoda tehtäviä myös manuaalisesti suoritettaville tehtäville, kuten kaikkien rakenteiden helppokäyttöisyyden arviointi. Tässä tapauksessa tehtävän linkki ei ole pakollinen. Tämän joustavuuden ansiosta voit seurata useita erilaisia tehtäviä kattavana prosessina.

Tehtävät voidaan määrittää joko toimelle tai tietylle työntekijälle. Esimerkiksi etupäällikkö suorittaa aina vakuutusmaksujen tarkistukset. Tämän takia kun luot tätä tehtävää, valitse ensin **Toimi** **Toimeksiantotyyppi** -kentästä ja sitten **Etuuspäällikkö** **toimiluettelosta**. Kun prosessi alkaa, tehtävä määritetään **etuuspäällikkönä** toimivalle työntekijälle. Voidaksesi määrittää tehtävän tietylle työntekijälle valitse **Työntekijä** **Määrityksen tyyppi** -kentässä ja valitse sitten henkilö.

Tehtävän eräpäivät määräytyvät prosessin alussa annettujen tavoitepäivämäärien mukaan. Osa tehtävistä on suoritettava ennen tavoitepäivämäärää, kun taas toiset voidaan suorittaa tavoitepäivämäärän jälkeen. Tehtävää määritettäessä annetaan tavoitepäivään suhteessa oleva eräpäivä **Eräpäivän siirtymä tavoitepäivämäärästä** -kentässä. Esimerkiksi etupäällikön on tarkistettava vakuutusmaksut 10 päivää ennen henkilöstöhallinnon tarkistuksen valmistumista. Tässä tapauksessa on tehtävän, joka luodaan tarkistusta varten **Eräpäivän siirtymä tavoitepäivämäärästä** arvo **-10**. Niinpä jos liiketoimintaprosessi käynnistetään 13. toukokuuta, tehtävä erääntyy 3. toukokuuta.

> [!NOTE]
> Eräpäiviä voi muokata myös liiketoimintaprosessin käynnistyttyä.

Monimutkaisissa tehtävissä saattaa olla useita vaiheita tai tehtäviä suorittavien henkilöiden täytyy mahdollisesti antaa lisätietoja. Näitä tilanteita varten voit lisätä tehtävään ohjeita. Ohjeet saattavat antaa tehtävän suorittamista koskevia lisätietoja sille henkilölle, joka on määritetty tehtävän suorittajaksi. Voit lisätä myös ohjeita tekstin muotoiluun.

## <a name="starting-a-business-process"></a>Liiketoimintaprosessin aloittaminen
Prosessi voidaan käynnistää liiketoimintaprosessimallista valitsemalla **Käynnistä prosessi**. Kun prosessi aloitetaan, tehtävät luodaan malliin sisällytetyissä tehtävissä määritetyille valituille työntekijöille ja/tai toimille. Jokaiselle tehtävälle määritetään myös eräpäivä lisäämällä siirtymäpäiviä tai vähentämällä niitä tavoitepäivämäärästä (katso lisätietoja siirtymäpäivistä Tehtävä-osasta). Aktiivisia liiketoimintaprosesseja voidaan tarkastella **Liiketoimintaprosessit**-työtilassa.

## <a name="employee-self-service"></a>Työntekijän itsepalvelu
Sen jälkeen, kun tehtävään on määritetty työntekijä, työntekijä voi tarkastella sitä ja muita hänelle määritettyjä tehtäviä **Työntekijän itsepalvelu** -sivulla. Kunkin hänelle on määritetyn liiketoimintaprosessin tehtävän kohdalla työntekijä näkee nimen ja kuvauksen tehtävästä, ohjeet ja yhteyshenkilön nimen. Tältä **Työntekijän itsepalvelu** -sivulta työntekijä voi myös avata siihen liittyvän sivun Microsoft Dynamics 365:ssa tai asiaan liittyvällä sivustolla, ja voit merkitä tehtävän olevan käynnissä, peruutettu tai valmis.

## <a name="business-process-workspace"></a>Liiketoimintaprosessin työtila
HR-ammattilaiset voivat tarkastella aktiivisia liiketoimintaprosesseja **liiketoimintaprosessin** -työtilassa. Tässä työtilassa on luettelo kaikista aktiivisista prosesseista ja kuhunkin prosessiin liitetyistä tehtävistä. Täydellinen luettelo voidaan suodattaa eräpäivän perusteella. Työtilassa on myös luettelo erääntyneistä tehtävistä ja erityisesti HR-työntekijälle määritetyistä tehtävistä. HR-työntekijät voivat myös päivittää kaikkien tehtävien tilan ja vaadittaessa määrittää tehtävät uudelleen, jotta liiketoimintaprosessi kokonaisuudessaan etenee.

## <a name="my-business-processes-workspace"></a>Omat liiketoimintaprosessit -työtila
Prosessin omistajat voivat tarkastella heille määritettyjä aktiivisia liiketoimintaprosesseja **Oma liiketoimintaprosessi** -työtilassa. Tässä työtilassa on luettelo kaikista aktiivisista prosesseista ja liitetyistä tehtävistä, jotka käyttäjä omistaa. Täydellinen luettelo voidaan suodattaa eräpäivän perusteella. Työtilassa on myös luettelo erityisesti prosessin omistajalle määritetyistä tehtävistä. Prosessin omistaja voi myös päivittää kaikkien tehtävien tilan ja määrittää minkä tahansa tehtävän uudelleen.

## <a name="navigating-business-processes"></a>Siirrytään liiketoimintaprosesseihin
Luodaksesi uuden tai kopioidaksesi prosessin liiketoimintamallin tai käynnistääksesi liiketoimintaprosessin siirry osioon Liiketoimintaprosessit - linkit – liiketoimintaprosessien hallinta. Voit myös tehdä seuraavia toimenpiteitä:

- Valitse **Uusi** luodaksesi uuden liiketoimintaprosessin mallin.
- Valitse **Kopioi mallista** -vaihtoehto kopioidaksesi valitun mallin uuteen malliin.
- Valitse **Aloita prosessi** aloittaaksesi valitun liiketoimintaprosessin, määrätäksesi tehtäviä ja laskeaksesi eräpäiviä.

Tarkastellaksesi aktiivisia prosesseja ja liittyviä tehtäviä, avaa **Liiketoimintaprosessit**-työtila.

