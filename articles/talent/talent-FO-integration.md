---
title: Dynamics 365 for Talentin integrointia Dynamics 365 for Finance and Operationsiin koskevat usein kysytyt kysymykset
description: Tässä ohjeaiheessa selvitetään, mitkä tiedot synkronoidaan Talentin ja Finance and Operationsin integroinnissa.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 438c2b5689e450b9aae9c55168993f2ee84be4d5
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517947"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a>Dynamics 365 for Talentin integrointia Dynamics 365 for Finance and Operationsiin koskevat usein kysytyt kysymykset

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa vastaan yleisiin kysymyksiin, jotka koskevat Dynamics 365 for Talentista synkronoitavia tietoja, kun Talent integroidaan Dynamics 365 for Finance and Operationsin kanssa.

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Synkronoidaanko kaikki tiedot vai vain tietyt tietoyksiköt?

Core Human Resourcesin (HR) tiedoista synkronoidaan tietojen alijoukko. Kaikki yksiköt sisältävä luettelo on kohdassa [Integrointi Dynamics 365 for Talentista Dynamics 365 for Finance and Operationsiin](talent-financeandoperations-integration.md).

Attractin ja Onboardin osalta kaikki tiedot ovat alkuperäisiä Common Data Servicen tietoja.

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Voinko luoda uuden yhdistämismäärityksen ilman mallia?

Mallien avulla pääsee alkuun. Voit luoda oman mallin, mutta integrointiprojektia luotaessa tarvitaan aina malli. Lisätietoja tietojen integrointiohjelmasta, malleista ja projekteista on kohdassa [Tietojen integrointi Common Data Service](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator) -ratkaisuun.

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a>Voinko määrittää taloushallinnon dimensiot siirtymään Talentin ja Finance and Operationsin välillä?

Common Data Service -ratkaisussa ei ole tällä hetkellä taloushallinnon dimensioita, joten ne eivät sisälly oletusmalliin. Tätä yksikköä suunnitellaan, mutta julkaisuajankohta ei ole tällä hetkellä tiedossa.

Jos Finance and Operationsissa on sellaisia tietoja, joita ei ole Talentissa, voit linkittää järjestelmät yhteen Talentin **linkkien määrittämisen** avulla. Lisätietoja Talentin ja Finance and Operationsin välisten linkkien määrittämisestä on kohdassa [Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (31. lokakuuta 2018)](whats-new-talent-october-31.md).

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a>Kun tuon työntekijöitä, ne päätyvät joskus Finance and Operationsin passiivisiin työntekijöihin. Miksi?

Tämä virhe voi esiintyä, jos työntekijöillä ei ole aktiivista työntekijän tietojen tietuetta Talentissa. Voit ratkaista tämän ongelman valitsemalla **Henkilöstön hallinta \> Työntekijät \> Työhistoria \> Päivämäärän hallinta** ja varmistamalla, että työntekijätietojen tietue on aktiivinen.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Jos valitsen vain yhden kentän alijoukon yhdistämisen, käynnistävätkö yhdistämättömiin kenttiin tehdyt muutokset synkronoinnin?

Tietojen synkronointi noudattaa suoritusaikataulua. Integrointi noutaa tietueen, jos jokin tietuen kenttä muuttuu, riippumatta siitä, onko kenttä osa integraation yhdistämismääritystä.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Miten voin lähettää vain aktiiviset työntekijän muutokset mutta ei päätettyjä tietueita?

Kyselyn lisäasetusten avulla voit suodattaa ja muokata lähdetietoja, ennen kuin ne siirretään kohteeseen.

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a>Voinko määrittää, mitkä tietyn yksikön kentät lähetetään Finance and Operationsiin?

Kenttiä voi lisätä integrointitehtävään tai poistaa niitä siitä. Kaikkia Common Data Service -yksikössä olevia tietokenttiä ei täytetä Core HR:stä.
Lisätiedot voidaan täyttää PowerAppsin kautta.

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Määritän integroinnin erätyönä, mutta Talentin yhteys kohdejärjestelmään katkesi. Miten voi lähettää saman muutosjoukon kohdejärjestelmään?

Poikkeuksen käsittelyyn ei tarvita mitään erityisiä asetuksia. Tietojen integrointiohjelma havaitsee ja raportoi automaattisesti lähteessä ja kohteessa tapahtumat sekä sallii manuaaliset uudelleenyritykset. Tietoja ei kuitenkaan voi korjata manuaalisesti. Jos tietoja on päivitettävä, ne on tehtävä joko lähteessä tai kohteessa.

## <a name="can-i-set-up-bi-directional-integration"></a>Voinko määrittää kaksisuuntaisen integroinnin?

Ei, sillä tällä hetkellä integrointi on yksisuuntaista (Talentista Finance and Operationsiin). Käytettävissä on kuitenkin oletusmalli, jolla tietoja voi lähettää Talentista Finance and Operationsiin.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Voinko sallia tietueiden poiston integroinnin osana?

Ei, sillä tietojen integrointiohjelma ei taltioi poistettuja tietueita tietojen siirtoon. Tällä hetkellä vain tietojen luonti ja päivitykset (UPSERT) sisällytetään.

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Voinko suorittaa virheellisen suorituksen uudelleen? Ja lähetetäänkö siinä tapauksessa koko tiedosto vai vain muutokset?

Tietojen integrointiohjelman ensimmäinen ajo on täydellinen ajo. Seuraavat ajot perustuvat muutosten seurantaan. Kun virheajo suoritetaan, se poistaa tietueet ajosta ja lähettää viimeisimmät muutokset Common Data Servicestä.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Saan projektia tallentaessani virheen, jonka mukaan projektissa on yhdistämisvirheitä. Mitä teen seuraavaksi?

Tarkista integrointiavainten asetukset, tee asetuksiin tarvittavat muutokset ja päivitä sitten projektin yksiköt.

Oletusmallia käytettäessä integrointiavaimet tuodaan automaattisesti. Tämä ongelma voi esiintyä, kun uusia tehtäviä lisätään nykyiseen malliin.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Jos minulla on N yritystä, joissa työntekijöillä on työpaikat, onko minun luotava yhdistämismääritys heille kaikille?

Kyllä. Jokaiselle Finance and Operationsin yksikölle on luotava erillinen integrointiprojekti tietojen integroinnissa.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Minun on siirrettävä tietoja, jotka eivät sisälly Microsoftin oletusmalliin. Onko se mahdollista?

Kyllä. Nykyisiin malleihin voi lisätä kenttiä, ja niitä voidaan myös poistaa siitä. Kun virheajo suoritetaan, se poistaa tietueet ajosta ja lähettää viimeisimmät muutokset muista Common Data Service -yksiköistä. Yksikön on oltava Common Data Service -ratkaisussa, jotta sen voi sisällyttää malliin. 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Olen juuri luonut uudet Finance and Operations- ja Talent-ympäristöt ja saan virheilmoituksen, jonka mukaan tietoarvo rikkoo yhtenäisyysehtoja. Miksi?

Tämän virheen syy voi olla jokin seuraavista:

- Tiedonsiirto aiheutti sen, että tietueet noudettiin lähteestä (Common Data Service) kahdesti.

- Tiedonsiirrossa Finance and Operationsin pakollisilla kentillä on tyhjäarvo. Tarkista, että tiedot ovat Common Data Servicessä ja että ne vastaavat Finance and Operationsin vaatimuksia.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Jos tapahtuu suoritusvirheitä eikä työntekijätunnus synkronoitunut, miten löydän työhistoria, joka sisältää epäonnistuneen työntekijätietueen?

Tietojen integrointiohjelma luo useita projekteja Finance and Operationsissa. Tietojen integrointiohjelman tehtävän ja Finance and Operationsin projektin välinen suhde on yksi yhteen.

Jäljitä aika tietojen integrointiohjelman suoritushistoriasta ja etsi Finance and Operationsin indeksi -1 -projekti. Jos tehtävän numero on tietojen integrointiohjelmassa 9, Finance and Operationsin indeksi on 8.

1. Taltioi tehtäväindeksi tietojen integrointiohjelmasta (tässä esimerkissä se on 9).

![Tehtäväindeksin taltiointi tietojen integrointiohjelmasta](media/CaptureTaskIndex.png)

2. Jäljitä projektin suoritusaika.

![Projektin suoritusajan jäljitys](media/CaptureTimeOfExecution.png)

3. Etsi Finance and Operationsissa indeksi -1. Tässä esimerkissä projekti, jonka jälkiliite on 8, ja projekti, jonka indeksin suoritusaika on 0, vastaa vaiheen 2 suoritusaikaa.

![Indeksin tunnistaminen](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a>Talentin tiedot eivät näy Finance and Operationsissa sen jälkeen, kun Talent ja Finance and Operations on integroitu. Mitä teen seuraavaksi?

Integrointi Finance and Operationsiin tapahtuu kahdessa vaiheessa. Tarkista ensin, että Talentin tiedot on päivitetty ja käytettävissä Common Data Servicessä. Tämä synkronointi tapahtuu lähes reaaliaikaisesti, ja se voidaan tarkistaa PowerAppsissa katsomalla tietoyksiköiden tietoja.

![Tiedot Common Data Servicessä](media/DataInCDS.png)

Jos tiedot eivät näy odotetusti Common Data Servicessä, tarkista, että yksikön integrointia tuetaan. Jos Common Data Serviceen halutaan sisällyttää lisätietoja, se edellyttää muutosta Microsoftin puolella.

Jos yksikköä tuetaan ja tiedot ovat käytettävissä Common Data Servicessä, tarkista, että yhdistämismääritys on oikein tietojen integrointiohjelmassa. Jos integrointiohjelman yhdistämismääritys näyttää olevan kunnossa, varmista seuraavaksi, että tietojen hallintatyöt on suoritettu. Erätöitä suoritettaessa voi tapahtua virheitä. Lisätietoja tietojen hallinnasta on kohdassa [Tietojen hallinta](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a>Työntekijöiden osoitteet ovat virheellisiä Finance and Operationsiin tuonnin jälkeen. Mitä minun pitäisi tehdä?

**Sijainnin tunnus** -asetuksen numerosarja käyttää samaa mallia sekä Talentissa että Finance and Operationsissa. Kummallakin puolella on oltava yksilöllinen numerosarja, jotta osoiteongelmia ei tule, kun tiedot integroidaan Common Data Servicestä Finance and Operationsiin.

Tarkista Talentin toteutuksen aikana, että Talentissa ja Finance and Operationsissa ei käytetä samaa numerosarjaa. Tarkista, että kaikki numerosarjat eivät ole samanlaisia siellä, missä tietoja ehkä ylläpidetään molemmissa järjestelmissä.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Kun yhteysjoukkoa luotiin, en nähnyt yhteyttä avattavassa Yhteys-luettelossa. Mitä teen seuraavaksi?

Varmista, että valitset yhteyksiä luotaessa Dynamics 365 for Finance and Operationsin (tällä hetkellä esiversio) ja Common Data Servicen.

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Saan työsuhteita synkronoitaessa virheen, jonka mukaan CompanyInfo_FK ei ole olemassa tai kentän Työsuhteen päättymispäivämäärä arvoa 31.12.2154 23:59:59 ei löydy liittyvästä taulusta Työsuhde. Mitä minun pitäisi tehdä?

Varmista, että yhdistämismääritys tehdään oikeisiin yrityksiin. Yrityksen synkronointi ei sisälly oletusmalliin, joten oletuksena on, että jokainen Talentissa ja Common Data Servicessä oleva yritys on myös Finance and Operationsissa.
Varmista myös, että valitset liitetylle yhteysjoukolle oikeat yritykset.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a>Finance and Operationsin kenttämääritys näyttää olevan tyhjä projektin määrittämisen jälkeen. Mitä minun pitäisi tehdä?

Päivitä Finance and Operationsin tietoyksiköt valitsemalla **Tietojenhallinta \> Kehikkoparametrit \> Yksikön asetukset \> Päivitä yksikköluettelo.** Tämä voi kestää muutaman minuutin, jonka jälkeen yhdistämismääritysten pitäisi olla näkyvissä. Tämä ongelma ilmenee uusia projekteja luotaessa.

![Puuttuva kenttämääritys](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Lisäresurssit

- Tietojen integrointiohjelma: 

  - [Integroi tiedot kohteeseen Common Data Service](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [Tietojen integrointiohjelman virheiden hallinta ja vianmääritys](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [Järjestelmän muodostamien lokien DSR-pyyntöihin vastaaminen PowerAppsissa, Microsoft Flowssa ja Common Data Servicessä](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Tietojen hallinta:

  - [Tietojen hallinta](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
