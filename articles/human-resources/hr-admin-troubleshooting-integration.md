---
title: Financeen integroinnin usein kysytyt kysymykset
description: Tässä artikkelissa selitetään, mitkä tiedot synkronoidaan Human Resourcesin ja Financen integroinnissa.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d2d590c95aa4069a1bed306910486c47200cdfd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794850"
---
# <a name="integration-with-finance-faq"></a>Financeen integroinnin usein kysytyt kysymykset

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa vastaan yleisiin kysymyksiin, jotka koskevat Dynamics 365 Human Resourcesista synkronoitavia tietoja, kun Talent integroidaan Dynamics 365 Financein kanssa.

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a>Voinko muokata Dynamics 365 Talent -sovelluksen käyttäjää Power Appsissa?

Nro Jos muokkaat Human Resourcesin sovelluskäyttäjää, Human Resourcesin ja Dataversen välinen integrointi voi epäonnistua. Seuraavassa taulukossa näkyvät Talentin sovelluskäyttäjän oletusasetukset.

| Koko nimi | Sovelluksen tunnus | Azure AD -objektin tunnus | Sovelluksen tunnuksen URI |
| --- | --- | --- | --- |
| Dynamics 365 for Talent | f9be0c49-aa22-4ec6-911a-c5da515226ff | 27fd8129-4b3c-43f7-b1bf-47495d3a049b | f9be0c49-aa22-4ec6-911a-c5da515226ff |

![Talentin sovelluskäyttäjän oletusasetukset](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Synkronoidaanko kaikki tiedot vai vain tietyt tietoyksiköt?

Tiedoista synkronoidaan tietojen alijoukko. Kaikki yksiköt sisältävä luettelo on kohdassa [Integrointi Dynamics 365 Financeen](hr-admin-integration-finance.md).

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a>Miksi en nää, että Dataverseen synkronoidaan tietoja?

Dataverse -integrointi on oletusarvoisesti pois käytöstä uudessa ympäristössä, joka ei sisällä toimitettuja demotietoja. Se on oletusarvoisesti käytössä ympäristöissä, jotka sisältävät demotietoja, ja tietojen synkronointi alkaa, kun ympäristö on provisioitu. Kyn ympäristö on valmis synkronoimaan tietoja, voit ottaa integroinnin käyttöön. Lisätietoja on kohdassa [Dataverse -integroinnin määritys](hr-admin-integration-common-data-service.md).

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Voinko luoda uuden yhdistämismäärityksen ilman mallia?

Mallien avulla pääsee alkuun. Voit luoda oman mallin, mutta integrointiprojektia luotaessa tarvitaan aina malli. Lisätietoja tietojen integrointiohjelmasta, malleista ja projekteista on kohdassa [Tietojen integrointi Microsoft Dataverse](https://docs.microsoft.com/powerapps/administrator/data-integrator) -ratkaisuun.

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>Voinko määrittää taloushallinnon dimensiot siirtymään Human Resourcesin ja Financen välillä?

Dataverse -ratkaisussa ei ole tällä hetkellä taloushallinnon dimensioita, joten ne eivät sisälly oletusmalliin. Tätä yksikköä suunnitellaan, mutta julkaisuajankohta ei ole tällä hetkellä tiedossa.

Jos Financessa on sellaisia tietoja, joita ei ole Human Resourcesissa, voit linkittää järjestelmät yhteen Human Resourcesin **linkkien määrittämisen** avulla.

![Määritä taloushallinnon dimensiot](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>Kun tuon työntekijöitä, ne päätyvät joskus Financen passiivisiin työntekijöihin. Miksi?

Tämä virhe voi esiintyä, jos työntekijöillä ei ole aktiivista työntekijän tietojen tietuetta Human Resourcesissa. Voit ratkaista tämän ongelman valitsemalla **Henkilöstön hallinta \> Työntekijät \> Työhistoria \> Päivämäärän hallinta** ja varmistamalla, että työntekijätietojen tietue on aktiivinen.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Jos valitsen vain yhden kentän alijoukon yhdistämisen, käynnistävätkö yhdistämättömiin kenttiin tehdyt muutokset synkronoinnin?

Tietojen synkronointi noudattaa suoritusaikataulua. Integrointi noutaa tietueen, jos jokin tietuen kenttä muuttuu, riippumatta siitä, onko kenttä osa integraation yhdistämismääritystä.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Miten voin lähettää vain aktiiviset työntekijän muutokset mutta ei päätettyjä tietueita?

Kyselyn lisäasetusten avulla voit suodattaa ja muokata lähdetietoja, ennen kuin ne siirretään kohteeseen.

![Aktiivisten työntekijöiden tarkennettu kysely](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>Voinko määrittää, mitkä tietyn yksikön kentät lähetetään Financeen?

Kenttiä voi lisätä integrointitehtävään tai poistaa niitä siitä. Kaikkia Dataverse-taulukossa olevia tietokenttiä ei täytetä Human Resourcesista.
Lisätiedot voidaan täyttää Power Appsin kautta.

![Lisää tai poista kenttiä integrointitehtävään tai -tehtävästä](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Määritän integroinnin erätyönä, mutta Human Resourcesin yhteys kohdejärjestelmään katkesi. Miten voi lähettää saman muutosjoukon kohdejärjestelmään?

Poikkeuksen käsittelyyn ei tarvita mitään erityisiä asetuksia. Tietojen integrointiohjelma havaitsee ja raportoi automaattisesti lähteessä ja kohteessa tapahtumat sekä sallii manuaaliset uudelleenyritykset. Tietoja ei kuitenkaan voi korjata manuaalisesti. Jos tietoja on päivitettävä, ne on tehtävä joko lähteessä tai kohteessa.

## <a name="can-i-set-up-bi-directional-integration"></a>Voinko määrittää kaksisuuntaisen integroinnin?

Ei, integraatio on tällä hetkellä yksisuuntaista (Human Resourcesista Finance and Operationsiin). Käytettävissä on kuitenkin oletusmalli, jolla tietoja voi lähettää Human Resourcesista Financeen.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Voinko sallia tietueiden poiston integroinnin osana?

Ei, sillä tietojen integrointiohjelma ei taltioi poistettuja tietueita tietojen siirtoon. Tällä hetkellä vain tietojen luonti ja päivitykset (UPSERT) sisällytetään.

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Voinko suorittaa virheellisen suorituksen uudelleen? Ja lähetetäänkö siinä tapauksessa koko tiedosto vai vain muutokset?

Tietojen integrointiohjelman ensimmäinen ajo on täydellinen ajo. Seuraavat ajot perustuvat muutosten seurantaan. Kun virheajo suoritetaan, se poistaa tietueet ajosta ja lähettää viimeisimmät muutokset Dataversestä.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Saan projektia tallentaessani virheen, jonka mukaan projektissa on yhdistämisvirheitä. Mitä teen seuraavaksi?

Tarkista integrointiavainten asetukset, tee asetuksiin tarvittavat muutokset ja päivitä sitten projektin yksiköt.

Oletusmallia käytettäessä integrointiavaimet tuodaan automaattisesti. Tämä ongelma voi esiintyä, kun uusia tehtäviä lisätään nykyiseen malliin.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Jos minulla on N yritystä, joissa työntekijöillä on työpaikat, onko minun luotava yhdistämismääritys heille kaikille?

Kyllä. Jokaiselle Financen yksikölle on luotava erillinen integrointiprojekti tietojen integroinnissa.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Minun on siirrettävä tietoja, jotka eivät sisälly Microsoftin oletusmalliin. Onko se mahdollista?

Kyllä. Nykyisiin malleihin voi lisätä kenttiä, ja niitä voidaan myös poistaa siitä. Kun virheajo suoritetaan, se poistaa tietueet ajosta ja lähettää viimeisimmät muutokset muista Dataverse-taulukoista. Yksikön on oltava Dataverse -ratkaisussa, jotta sen voi sisällyttää malliin. 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Olen juuri luonut uudet Finance- ja Human Resources -ympäristöt ja saan virheilmoituksen, jonka mukaan tietoarvo rikkoo yhtenäisyysehtoja. Miksi?

Tämän virheen syy voi olla jokin seuraavista:

- Tiedonsiirto aiheutti sen, että tietueet noudettiin lähteestä (Dataverse) kahdesti.

- Tiedonsiirrossa Finance and Operationsin pakollisilla kentillä on tyhjäarvo. Tarkista, että tiedot ovat Dataversessä ja että ne vastaavat Finance and Operationsin vaatimuksia.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Jos tapahtuu suoritusvirheitä eikä työntekijätunnus synkronoitunut, miten löydän työhistoria, joka sisältää epäonnistuneen työntekijätietueen?

Tietojen integrointiohjelma luo useita projekteja Financessa. Tietojen integrointiohjelman tehtävän ja Financen projektin välinen suhde on yksi yhteen.

Jäljitä aika tietojen integrointiohjelman suoritushistoriasta ja etsi Financen indeksi -1 -projekti. Jos tehtävän numero on tietojen integrointiohjelmassa 9, Financen indeksi on 8.

1. Taltioi tehtäväindeksi tietojen integrointiohjelmasta (tässä esimerkissä se on 9).

    ![Tehtäväindeksin taltiointi tietojen integrointiohjelmasta](media/CaptureTaskIndex.png)

2. Jäljitä projektin suoritusaika.

    ![Projektin suoritusajan jäljitys](media/CaptureTimeOfExecution.png)

3. Etsi Financesta indeksi -1. Tässä esimerkissä projekti, jonka jälkiliite on 8, ja projekti, jonka indeksin suoritusaika on 0, vastaa vaiheen 2 suoritusaikaa.

    ![Indeksin tunnistaminen](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>Kun olen integroinut Human Resourcesin ja Financen, en näe Human Resources -tietojani Financessa. Mitä teen seuraavaksi?

Integrointi Financeen tapahtuu kahdessa vaiheessa. Tarkista ensin, että Human Resourcesin tiedot on päivitetty ja käytettävissä Dataversessä. Tämä synkronointi tapahtuu lähes reaaliaikaisesti, ja se voidaan tarkistaa Power Appsissa katsomalla tietotaulukoiden tietoja.

![Tiedot Dataversessä](media/DataInCDS.png)

Jos tiedot eivät näy odotetusti Dataversessä, tarkista, että yksikön integrointia tuetaan. Jos Dataverseen halutaan sisällyttää lisätietoja, se edellyttää muutosta Microsoftin puolella.

Jos yksikköä tuetaan ja tiedot ovat käytettävissä Dataversessä, tarkista, että yhdistämismääritys on oikein tietojen integrointiohjelmassa. Jos integrointiohjelman yhdistämismääritys näyttää olevan kunnossa, varmista seuraavaksi, että tietojen hallintatyöt on suoritettu. Erätöitä suoritettaessa voi tapahtua virheitä. Lisätietoja tietojen hallinnasta on kohdassa [Tietojen hallinta](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>Työntekijöiden osoitteet ovat virheellisiä Financeen tuonnin jälkeen. Mitä minun pitäisi tehdä?

**Sijainnin tunnus** -asetuksen numerosarja käyttää samaa mallia sekä Human Resourcesissa että Financessa. Kummallakin puolella on oltava yksilöllinen numerosarja, jotta osoiteongelmia ei tule, kun tiedot integroidaan Dataversestä Finance and Operationsiin.

Tarkista Human Resourcesin toteutuksen aikana, että Human Resourcesissa ja Financessa ei käytetä samaa numerosarjaa. Tarkista, että kaikki numerosarjat eivät ole samanlaisia siellä, missä tietoja ehkä ylläpidetään molemmissa järjestelmissä.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Kun yhteysjoukkoa luotiin, en nähnyt yhteyttä avattavassa Yhteys-luettelossa. Mitä teen seuraavaksi?

Varmista, että valitset yhteyksiä luotaessa Dynamics 365 Financen ja Dataversen.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Saan työsuhteita synkronoitaessa virheen, jonka mukaan CompanyInfo_FK ei ole olemassa tai kentän Työsuhteen päättymispäivämäärä arvoa 31.12.2154 23:59:59 ei löydy liittyvästä taulusta Työsuhde. Mitä minun pitäisi tehdä?

Varmista, että yhdistämismääritys tehdään oikeisiin yrityksiin. Yrityksen synkronointi ei sisälly oletusmalliin, joten oletuksena on, että jokainen Human Resourcesissa ja Dataversessä oleva yritys on myös Financessa.
Varmista myös, että valitset liitetylle yhteysjoukolle oikeat yritykset.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>Financen kenttämääritys näyttää olevan tyhjä projektin määrittämisen jälkeen. Mitä minun pitäisi tehdä?

Päivitä Financen tietoyksiköt valitsemalla **Tietojen hallinta \> Kehikkoparametrit \> Yksikön asetukset \> Päivitä yksikköluettelo.** Tämä voi kestää muutaman minuutin, jonka jälkeen yhdistämismääritysten pitäisi olla näkyvissä. Tämä ongelma ilmenee uusia projekteja luotaessa.

![Puuttuva kenttämääritys](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Lisäresurssit

- Tietojen integrointiohjelma: 

  - [Integroi tiedot kohteeseen Microsoft Dataverse](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [Tietojen integrointiohjelman virheiden hallinta ja vianmääritys](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [Järjestelmän muodostamien lokien DSR-pyyntöihin vastaaminen Power Appsissa, Microsoft Power Automate'ssa ja Dataversessa](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Tietojen hallinta:

  - [Tietojen hallinta](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]