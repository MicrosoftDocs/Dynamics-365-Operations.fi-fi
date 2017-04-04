---
title: "Tuotannon reitityksissä käytettävät kustannusluokat"
description: "Tässä artikkelissa on tietoja kustannusluokista, joita käytetään reititystä käyttävissä valmistusympäristöissä."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 5b4030e7f02b14d0e5a9cf62ddc8a1809dfa91f3
ms.lasthandoff: 03/29/2017


---

# <a name="cost-categories-used-in-production-routing"></a>Tuotannon reitityksissä käytettävät kustannusluokat

Tässä artikkelissa on tietoja kustannusluokista, joita käytetään reititystä käyttävissä valmistusympäristöissä.

Kustannusluokkia käytetään valmistusympäristöissä, joissa käytetään reitityksiä. Kustannusluokat liitetään operatiivisiin resursseihin ja reitityksen työvaiheisiin tuntikustannusten määrittämistä sekä valmistetun nimikkeen laskettujen kustannusten kustannusvaikutusten ryhmittelyä varten. Kustannusluokkiin liitettyjen kustannusryhmien avulla valmistuksen kustannusvaikutukset luokitellaan operatiivisten resurssien sekä tehtävätyypin, kuten asennus- ja ajoajan, mukaan. Kustannusryhmämääritysten tarkkuus mahdollistaa valmistuksen yleiskustannusten laskennan reititystietojen perusteella. 

**Huomautus:** Kustannusluokilla on valmistusympäristöissä useita synonyymejä, kuten työvoiman osuuskoodit tai laitteiden osuuskoodit. 

Kuhunkin kustannusluokkaan on liitetty kustannustietueita, ja niille määritetään kustannusryhmä. Eri tuotantotarkoituksiin tarvitaan erilaisia kustannusluokkia.

-   Määritä eri tuntihinnat operatiivisen resurssin mukaan. Kustannukset voivat vaihdella esimerkiksi erilaisten osaamisalueiden, laitteiden tai valmistussolujen mukaan.
-   Määritä eri tuntihinnat reitityksen työvaiheeseen liittyvälle asennusajalle tai ajoajalle.
-   Määritä operatiivisen resurssin kustannukset tuotetun määrän perusteella tuntikustannusten asemesta esimerkiksi maksettaessa työvoimalle urakkapalkkaa.
-   Segmentoi valmistetun nimikkeen laskettuihin kustannuksiin kohdistuvat kustannusvaikutukset kustannusryhmän mukaan. Voi esimerkiksi segmentoida työvoima- ja laitekulut.
-   Määritä kustannusryhmän peruste yleiskustannusten laskentakaavoja varten. Voit määrittää kaavat esimerkiksi työvoimaan tai laitteisiin liittyville yleiskustannuksille tai asennusaikaan ja ajoaikaan perustuville yleiskustannuksille.

Kustannusluokan voi liittää asetusaikaan, prosessiaikaan tai reitityksen työvaiheen määrään. Kun kustannuksissa tai kustannusryhmien segmentoinnissa on eroja esimerkiksi asennusajan ja prosessiajan välillä, niille on määritettävä ja liitettävä eri kustannusluokat. Kustannusluokkien valikoiva käyttö asennusaikaa, prosessiaikaa ja määrää varten määräytyy työvaiheeseen liitetyn reititysryhmän mukaan. Kustannusluokkien liittäminen aikaan ja määrään voi olla pakollista **Tuotannonhallinnan parametrit** -sivulla määritettyjen yrityksenlaajuisten käytäntöjen mukaisesti. 

Kullakin kustannusluokalla on liitettyjä kustannuksia, jotka perustuva kustannustietueiden määritykseen kustannuslaskentaversiossa. **Kustannusluokan hinta** -sivulla voit määrittää kustannustietueet tietylle kustannuslaskentaversiolle ja toimipaikalle. Kustannusluokan kustannustietueen tilaksi määritetään aluksi **Odottaa**, ja sille määritetään aiottu voimaantulopäivä. Kun aktivoit kustannustietueen, tilaksi päivittyy **Aktiivinen** ja voimaantulopäivä päivitetään aktivointipäiväksi. Eri kustannustietueet voivat vastata eri toimipaikkoja, voimaantulopäiviä tai tiloja. Tulevan tai menneen päivämäärän tuoterakennelaskelmissa käytetään kustannustietueita, joilla on tietty voimaantulopäivä. Nykyistä aktiivista kustannustietuetta käytetään tuotantotilausten kustannusten arvioinnissa sekä raportoidun ajan vertaamisessa tuotantotilaukseen. 

Kustannusluokan kustannustietue voi olla toimipaikkakohtainen tai yrityksenlaajuinen. Voit tehdä kustannustietueesta toimipaikkakohtaisen määrittämällä sille toimipaikan. Jos toimipaikan arvo jätetään tyhjäksi, kustannustietue koskee kaikki yrityksen toimipaikkoja. Kustannuksissa voi olla eroja esimerkiksi toimipaikkojen välillä, ja tällöin kustannustietueet on määritettävä toimipaikkakohtaisiksi. 

Reitityksen työvaihe perii tavallisesti operatiiviseen resurssiin tai päätyövaiheeseen liitetyt kustannusluokat. Kun luot tuotantotilauksen, tuotantoreitin reititystyövaiheet ovat valitun reittiversion mukaiset. Voit korvata tuotantoreitin työvaiheille määritetyt kustannusluokat. 

Joitakin tuotantotyön tyyppejä voidaan käyttää projektin aika-arvioinneissa ja raportoinnissa. Tässä tapauksessa kustannusluokka tarvitaan tuotantoa ja projektia varten. Kun kustannusluokka on merkitty käytettäväksi projekteissa, projektista on määritettävä lisätietoja.


