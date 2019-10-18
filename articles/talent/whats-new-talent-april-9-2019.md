---
title: Dynamics 365 Talent -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 9, 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 08f3f8150a120817618ee4d31197f3088c7483ab
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024088"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-9-2019"></a>Dynamics 365 Talent -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 9, 2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Servicesin (LCS) integrointi ongelman raportoinnin kanssa
Attract and Onboardissa ongelmat, jotka käyttävät raporttia käyttävien loppukäyttäjien kirjaamia ongelmia, luovat nyt automaattisesti tukikysymyksiä asiakkaan LCS-hankkeeseen. Järjestelmänvalvojat voivat sitten tarkistaa ongelmat ja lähettää ne Microsoftille tarpeen mukaan. Tämä vastaa sitä, miten Core HR käsittelee loppukäyttäjän tukitapauksia.

### <a name="relevance-search"></a>Osuvuushaku
Kykyreserveistä voit etsiä tiettyjä osaamisalueita, nimiä ja koulutustietoja koko hakijatietokannasta. Sinun ei enää tarvitse määrittää sitä hakijan profiilin osaa, jonka haluat etsiä. Attract tekee hakuja koko profiilista ja korostaa kaikki löydetyt osumat. Attract hakee myös kaikki hakijan käytettävissä olevat asiakirjat ja luokittelee älykkäästi hakutulokset. Lisäksi voit suodattaa tulokset lähteen mukaan tai sen mukaan ovatko ne toisarvoisia. Lisätietoja on kohdassa [Hae ja katso hakijaprofiilit](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles).

### <a name="prospect-recommendations"></a>Prospektisuositukset
Attract voi auttaa käynnistämään työn hankinnan heti, kun aktivoit sen tekemällä älykkäitä ehdotuksia organisaation ehdokastietokannasta. Suosituksiin sisältyy taitoja ja koulutusta koskevia tietoja, jotka on tunnistettu etsimällä merkityksellisiä näkymiä. Nämä suositukset näkyvät **Prospekti**-välilehdellä työn alla, jos otat sen käyttöön työhönottoprosessin aikana. Lisätietoja on kohdassa [Prospektisuositukset](https://docs.microsoft.com/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations).

### <a name="interviewer-availability-statuses"></a>Haastattelijan käytettävyystilat
Haastatteluaikataulujen tekijät voivat pian tarkastella haastattelijoiden **Poissa toimistosta, työskentelee muualla** -tiloja, jotta voivat suunnitella aikatauluja, jotka saattavat toimia haastattelijoille paremmin.

### <a name="candidate-interview-experience-save-calendar-invites"></a>Hakijan haastattelukokemus: kalenteripyyntöjen tallentaminen
Hakijat voivat nyt ladata ja tallentaa haastattelutapahtumat henkilökohtaisiin kalentereihinsa käyttäen hakijalle lähetetyn haastattelun yhteenvetosähköpostiin liitettyä .ics-tiedostoa.

## <a name="changes-in-onboard"></a>Onboardin muutokset

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Servicesin (LCS) integrointi ongelman raportoinnin kanssa
Attract and Onboardissa ongelmat, jotka käyttävät raporttia käyttävien loppukäyttäjien kirjaamia ongelmia, luovat nyt automaattisesti tukikysymyksiä asiakkaan LCS-hankkeeseen. Järjestelmänvalvojat voivat sitten tarkistaa ongelmat ja lähettää ne Microsoftille tarpeen mukaan. Tämä vastaa sitä, miten Core HR käsittelee loppukäyttäjän tukitapauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset
Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2225.

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a>Prosenttiosuus peruskorjaussuunnitelmista lataa väärän summan
Tämän viikon julkaisu korjaa ongelman, kun ladataan muuttujapalkkioita palkkioiden prosenttiosuudella.
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a>Päivämääränvalitsin viimeisellä työpäivällä ei toimi oikein
Tämä muutos korjaa ongelman: Kun käyttäjät muokkaavat **Työsuhteen päättymispäivä** ja valitse päivämäärä kalenterin hallinnan avulla, päivä lisätään valintaan.

###  <a name="limit-personnel-action-types-by-the-action-taken"></a>Rajoita henkilöstötoimintatyyppejä toteutetuilla toimilla.
Tämä muutos rajoittaa tiettyjä toimintoja käytettäessä näkyviä toimintotyyppejä. Kun esimerkiksi pyydetään uutta paikkaa, vain uudet sijaintitoimet näkyvät valittavissa olevien toimintojen luettelossa. Aiemmin ilmestyi sekä uusia että muokkaustoimintoja. 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a>Työntekijän siirtäminen korvauksen kanssa toisessa yrityksessä
Tämä julkaisu mahdollistaa korvauksen päättymisen toisessa yrityksessä, jos siirto on tarkoitettu yritysten väliseen siirtoon.

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a>Ei voida valita korvausta tulevasta työstä siirron aikana
Kun siirrät työntekijän uuteen yritykseen, voit nyt asettaa korvauksen uudelle yritykselle siirron aikana.

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a>Käyttäjä ei voi määrittää korvausta sijainnin määrityksen aikana
Uuden paikannustoiminnon lisääminen mahdollistaa nyt kiinteän kompensointitietueen asettamisen. 

## <a name="in-preview"></a>Esiversiossa

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Syykoodit on määritettävä lomatyyppien avulla.
Organisaatiot saattavat tarvita lisätietoja, jotka liittyvät lomapyyntöihin. Voit nyt määrittää lomalajien syykoodit ja antaa työntekijöille mahdollisuuden valita syykoodin lomapyynnöissään.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Vaadi syykoodeja tietyille poissaolopyyntöjen lomatyypeille
Organisaatiot saattavat vaatia syykoodien asettamista tietylle lomalajeille, kun työntekijät lähettävät aikaa. Syynä voi olla yrityksen käytäntö tai säännöstenmukaisuuden vaatimuksia. Voit nyt määrittää mitkä lomatyypit edellyttävät syykoodin, ja voit vaatia työntekijöitä antamaan syykoodin näille lomatyypeille poissaolopyynnössä.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Tarjoa henkilöstöhallinnolle loma- ja poissaololuettelot
Työntekijöiden aikaa jäljittää ja ymmärtää, miten loma-aika lasketaan, ei ainoastaan auta henkilöstöä vastaamaan työntekijäkysymyksiin, vaan myös varmistavat työntekijöille tarkat aikapalkinnot. Henkilöstöhallinnolla on nyt uusi näkemys liiketoimista (apurahat, suoritukset, oikaisut ja pyynnöt) nähdäksesi saldon syyt. 

## <a name="coming-soon"></a>Tulossa pian

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Työntekijöiden kaksoiskappaleen tarkistuksen käyttöliittymän parannukset
Tällä muutoksella tunnistetaan duplikaatit, kun syötät nimikenttiä, ja tila näyttää löytyneiden kopioiden määrän. Voit valita uuden sivun sisältävän linkin arvioidaksesi, käytetäänkö tunnistettua vastausta. Tietojen syöttämisen keskeyttämisen välttämiseksi kaksoiskappale ei avaudu automaattisesti.

###  <a name="email-support-for-alerts"></a>Sähköpostituki hälytyksille
Finance and Operations -käyttöympäristöpäivitys 25:n avulla käyttäjät voivat luoda hälytyssääntöjä, jotka lähettävät automaattisesti sähköposti-ilmoituksia yhteyshenkilöille, kun tapahtuma käynnistyy. 
