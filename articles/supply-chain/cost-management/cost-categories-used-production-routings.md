---
title: Tuotannon reitityksissä käytettävät kustannusluokat
description: Tässä artikkelissa on tietoja kustannusluokista, joita käytetään reititystä käyttävissä valmistusympäristöissä.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f36154467f7d392f9bb77bf907807d8acc4f61ff
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679524"
---
# <a name="cost-categories-used-in-production-routing"></a>Tuotannon reitityksissä käytettävät kustannusluokat

[!include [banner](../includes/banner.md)]

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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]