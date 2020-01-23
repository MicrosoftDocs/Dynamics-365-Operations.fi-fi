---
title: Dynamics 365 for Talentin uudet ja muuttuneet ominaisuudet (27.8.2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d7e5be0d9ba5e372e57f06fec77326561196626
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899240"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Dynamics 365 for Talentin uudet ja muuttuneet ominaisuudet (27.8.2019)

Tässä ohjeaiheessa käsitellään Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2447. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Esiversiotoiminnot on otettu käyttöön vain eristysympäristöissä

Voit määrittää Talentin uutta esiintymää valmisteltaessa, onko esiintymän tyyppi Tuotanto vai Eristys. Eristys-tyypin esiintymissä uusia toimintoja voi testata varhaisessa vaiheessa. Kaikki aiemmin luodut Talent-esiintymät päivitetään Tuotanto-esiintymän tyyppiin. Jos haluat, että jokin aiemmin luoduista esiintymistä päivitetään Eristys-esiintymätyypiksi, ota yhteyttä tukeen ja tee muutospyyntö.

Lisätietoja muutosten julkaisemisesta on kohdassa [Talentin valmistelu](./provisioning-talent.md).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Laajennettujen suorituskykytietojen näyttäminen esimiehen itsepalvelutoiminnossa

Uuden vaihtoehdon avulla esimiehet voit tarkastella sekä suorien että epäsuorien alaisten suoriutumista. Tällä hetkellä linjapäälliköt voivat määrittää ja päivittää suorituskykytavoitteita ja antaa uusia arvioita. Lisäksi suorat esimiehet ja heidän alaisensa voivat ylläpitää ja päivittää suoritustason kirjauskansioita. Tämä auttaa varmistamaan, että kehityskeskusteluprosessi toimii sujuvasti. Kun tämä muutos otetaan käyttöön, esimiehet voivat tarkastella ja ylläpitää epäsuorien alaisten suoritustasotietoja suorien alaisten tietojen lisäksi.

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>Yrityksiä ei voi poistaa, jos yrityksessä on työntekijöitä (339849)

Tämän muutoksen myötä et voi poistaa yrityksiä, jossa yrityksellä on työntekijöitä tai muita liittyviä tietoja.

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>Kompensaation hallinnan liiketoimintatietojen analyysi ei vastaa kompensaation työtilaa (322493)

Tässä julkaisussa kompensaatioanalyysi on muokattu vastaamaan tarkasti työntekijöille määritettyjä suunnitelmia.

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>Työnkulun paikkamerkin %yritys% näyttää DAT:n, kun työntekijöitä otetaan töihin työnkulun kautta (343905)

Tässä julkaisussa yrityksen paikkamerkki näyttää yrityksen, joka on liitetty uuden työntekijän työsuhteeseen.

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>CDSJobPosition-yksikkö näyttää virheen, kun viimeinen voimassaolopäivämäärä on määritetty (349387)

Tässä julkaisussa **CDSJobPosition**-yksikön **Toimen tiedot**- ja **Toimen kesto** -tietolähteet sallivat muokkaukset Common Data Servicestä **Voimaantulopäivä**-kenttiin. 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>Työtekijän työsuhteen päättyessä viimeinen työpäivä täytetään määrityksen päättymispäivässä (332496)

Tämä muutos nyt palauttaa toimen **määrityksen päättymispäivän** oletusarvoisesti **työsuhteen päättymispäivämääräksi**. Voit muuttaa näitä oletuksia tietoja annettaessa.

### <a name="legal-entities-arent-limited-with-hire-338871"></a>Työhön ottaminen ei rajoita yrityksiä (338871)
 
Tämä muutos rajoittaa työhönottoprosessin näyttämään vain yritykset, joiden käyttöoikeus käyttäjällä on.  

## <a name="in-preview"></a>Esiversiossa

### <a name="streamlined-employee-entry-and-navigation"></a>Yksinkertaistettu työntekijöiden lisääminen ja navigointi

Tämä toiminto on nyt käytettävissä eristys- ja kokeiluympäristöissä. Ota tämä toiminto käyttöön valitsemalla **Järjestelmän hallinta > Linkit > Asetukset > Järjestelmän parametrit > Esiversio-ominaisuudet**. Valitse **Laajennettu työntekijälomake ja siirtyminen**. Nämä muutokset otetaan nyt käyttöön kaikille käyttäjille. Voit poistaa tämän asetuksen käytöstä milloin tahansa.

Lisätietoja on kohdassa [Yksinkertaistettu työntekijöiden lisääminen ja navigointi](./streamlined-employee-entry.md).

## <a name="coming-soon"></a>Tulossa pian

### <a name="platform-update-29"></a>Ympäristön update 29 -päivitys

Lisätietoja Platform update 29 -päivityksestä on kohdassa [Dynamics 365 for Finance and Operations platform update 29 -esiversion toiminnot (lokakuu 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).
