---
title: Optimoi Dataversen virtuaalitaulukoiden kyselyt
description: Dataversen virtuaalitaulukyselyjen suorituskyvyn optimointi ja vianmääritys
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8026abd5c3e0f9b78e8c016731fd7785490bc945
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891099"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>Optimoi Dataversen virtuaalitaulukoiden kyselyt

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>Varasto-otto

### <a name="overview"></a>Yleiskuvaus

Kun käytät Dataversen virtuaalitauluja integrointien ja muiden tietoyhteyksien kehittämiseen Dynamics 365 Human Resourcesissa, virtuaalitauluihin liitetyissä kyselyissä ilmenee suorituskykyongelmia. Kyselyjen suorittaminen voi olla hidasta eri asiakkaiden tai liittymien välillä. Ongelma voi esimerkiksi esiintyä seuraavissa tilanteissa:

- Virtuaalitaulua kyseltäessä Dataversen www-ohjelmointirajapinnan kautta
- Kun Power App -sovellusta luodaan virtuaalitaulua vasten
- Kun Power BI -raporttia rakennetaan virtuaalitaulussa

Kaikki nämä liittymät voivat tuoda esiin suorituskykyongelman.

Yksi henkilöstöhallinnon virtuaalitaulujen suorituskyvyn hidastamisista on taulun liittyvien Dataversen virtuaalitaulujen [siirtymisominaisuuksiin](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) liittyvät viiteavainsarakkeet. Kun virtuaalitaululle luodaan siirtymisominaisuudet, tauluun lisätään automaattisesti viiteavainsarake, joka vastaa liittyvän virtuaalitaulun avainsarakkeen arvoa. Esimerkiksi **_mshr_fk_person_id_value** lisätään **mshr_hcmworkerbaseentity**-kohteeseen, jonka viiteavaimen ominaisuus on **mshr_dirpersonentity**-kohteesta. Koska näiden viiteavainsarakkeiden arvoja ylläpidetään taulukossa, arvojen hakeminen voi vaikuttaa negatiivisesti kyselyn suorituskykyyn virtuaalitaulua vasten.

### <a name="potential-symptoms"></a>Mahdolliset oireet

Tämä vaikutus voi olla esimerkiksi kyselyissä työntekijää (**mshr_hcmworkerentity**) tai perustyöntekijää (**mshr_hcmworkerbaseentity**) vastaan. Voit nähdä suorituskykyongelman itse monin eri tavoin:

- **Kyselyn suorittaminen on hidasta**: Kysely virtuaalitaulua vastaan saattaa palauttaa odotetut tulokset, mutta kyselyn suorittaminen kestää odotettua kauemmin.
- **Kyselyn aikakatkaisu**: Kysely voi aikakatkaisua ja palauttaa seuraavan virheen: "ATunnuksen avulla soitettiin Finance and Operationsiin, mutta Finance and Operations palautti InternalServerError-tyypin virheen."
- **Odottamaton virhe**: Kysely saattaa palauttaa virhetyypin 400. Näyttöön tulee seuraava sanoma: Odottamaton virhe.

  ![Virhetyyppi 400 HcmWorkerBaseEntityssä](./media/HcmWorkerBaseEntityErrorType400.png)

- **Ylikuormitus** Kysely voi käyttää palvelinresursseja liian paljon, ja siitä tulee vain osa välityspalvelinta. Tässä tapauksessa kysely palauttaa seuraavan virheen: "Tunnus haettiin Finance and Operationskutsua varten, mutta Finance and Operations palautti virheen, tyyppi 429." Lisätietoja henkilöstöhallinnon rajoittamisesta on kohdassa [rajoitusten usein kysytyt kysymykset](./hr-admin-integration-throttling-faq.md).

  ![Virhetyyppi 429 HcmWorkerBaseEntityssä](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>Ratkaisu

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>Kyselyyn sisältyvien sarakkeiden määrän rajoittaminen

Virtuaalitaulujen avulla yksi menetelmistä, joilla on paras mahdollisuus parantaa kyselyn suorituskykyä, on kyselystä valittujen sarakkeiden määrän rajoittaminen. Yleisohje kyselyn suorituskyvyn optimointiin on se, että kyselyssä palautetut sarakkeet rajataan vain tarvitsemiisi ominaisuuksiin. Tämä koskee erityisesti virtuaalitaulujen viiteavainsarakkeita. Jos et tarvitse integroinnin tai raportin viiteavainsarakkeiden arvoja, valitse vain haluamasi sarakkeet ilman viiteavainsarakkeita rakenteen avulla.

#### <a name="selecting-columns-in-an-odata-query"></a>Sarakkeiden valitseminen OData-kyselyssä

Kun kyselet virtuaalitaulua Dataversen www-ohjelmointirajapinnan kautta, voit rajoittaa kyselyyn sisältyvien sarakkeiden määrää käyttämällä **$select**-järjestelmän kyselyasetusta ja määrittää sarakkeet, joita varten tulokset on palautettava. Voit parantaa suorituskykyä sulkemalla pois viiteavainsarakkeet (joissa on **_mshr_FK_**-etuliite) kyselystä.

Esimerkiksi seuraava kysely ennusteyksikköä **mshr_hcmworkerbaseentity**-kohdetta vastaan sisältää vain kyselylausekkeen **$select** sisällä olevat sarakkeet ilman viiteavainarvoja. Tämä parantaa merkittävästi suorituskykyä kyselyssä, joka sisältää kaikki taulusarakkeet.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Ehdotus, jonka mukaan valittujen sarakkeiden määrää rajataan, koskee myös **$expand**-asetusta, kun kyselyä laajennetaan liittyviin virtuaalitauluihin siirtymisominaisuuksien avulla. Seuraava kysely sisältää esimerkiksi sarakkeet **mshr_hcmworkerbaseentity**-yksikköön, jonka laajennetut sarakkeet ovat peräisin **mshr_dirpersonentity**-yksiköstä. Huomaa, että **$select**-asetus sisältyy myös **$expand**-kyselyasetuslausekkeeseen.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Kun käytät tätä menetelmää, kun tietoja noudetaan **$select**-kyselylausekkeen **$expand**-kyselyvaihtoehdolla, suorituskyky yleensä paranee, kun yksiköiden välinen siirtymiskyky on monisuuntainen. Kyselyiden suoritusaika ei ehkä ole sama, kun yksi moneen -suhdetta laajennetaan. Lisätietoja Dataverse-virtuaalitaulujen suhdemäärityksestä on kohdassa [Taulun suhteet](/powerapps/maker/data-platform/create-edit-entity-relationships).

Lisätietoja Dataverse-www-ohjelmointirajapinnan **$select** ja **$expand** -asetusten käyttämisestä on kohdassa [Liittyvien yksikkötietueiden hakeminen kyselyn avulla](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).

#### <a name="selecting-columns-in-power-bi"></a>Sarakkeiden valitseminen Power BIssä

Jos Power BI -raportin luominen Dataverse-virtuaalitauluun hidastaa suorituskykyä, voit parantaa suorituskykyä sulkemalla viitesarakkeet pois valituista sarakkeista raporttia varten valitusta taulusta. Jos esimerkiksi luot raportin Power BI Desktopilla toimittajayksikölle **mshr_hcmworkerbaseentity**, voit valita raporttikyselyyn sisällytettävät sarakkeet seuraavien vaiheiden avulla.

1. Valitse  Power BI Desktopssa **Hae tiedot** -toimintonauhan avattavasta valikosta **Lisää...** -vaihtoehto.
2. Kirjoita **Hae tiedot** -ikkunassa hakuruutuun **Common Data Service** ja valitse **Common Data Service** -liitin ja valitse **Yhdistä**.
3. Kirjoita Common Data Service -ikkunan **Palvelimen URL** -kenttään Dataverse-ympäristösi organisaatio-URI ja valitse **OK**.
  
   ![Anna Dataverse -ympäristösi URI](./media/PowerBIDataverseURLSetup.png)
  
4. Laajenna Navigointi-ikkunanssa **Yksiköt**-solmu.
5. Kirjoita hakuruutuun **mshr_hcmworkerbaseentity** ja valitse yksikkö.
6. Valitse **Muuta tiedot**.
7. Valitse Power Query -editori-ikkunassa **Laajennettu editori**.
8. Päivitä kysely **Laajennettu editori** -ikkunassa niin, että se näyttää alla olevalta, lisäämällä tai poistamalla sarakkeita taulukkoon tarpeen mukaan.

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Kyselyn päivittäminen Power Query -editorin laajennetulla editorilla](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. Valitse **Valmis**.

   > [!NOTE]
   > Jos olet aiemmin saanut kyselyltä virhetyypin 429 ennen päivitystä, sinun on ehkä odotettava uudelleenyrityskauden päättymistä ennen kyselyn päivittämistä.

10. Valitse **Sulje & ota käyttöön** Power Query -editorin toimintonauhassa.

Tämän jälkeen voit alkaa rakentaa Power BI -raporttia virtuaalitaulusta valittuihin sarakkeisiin.

#### <a name="selecting-columns-in-power-apps"></a>Sarakkeiden valitseminen Power Appsssä

Kuten Dataversen www-ohjelmointirajapinnan kyselyissä ja Power BIssä, ja voit parantaa Dataversen virtuaalitauluihin perustuvien Power Appsin kyselyjen suorituskykyä sulkemalla pois sovelluksesi toisiinsa liittyvien taulujen sarakkeet. Jos sivuun liittyvän taulun sarakkeita on sisällytetty, tietojen hakemista varten muodostettu URL-osoite sisältää liittyvän taulun viiteavaimen ominaisuudet. Kuten edellä olevassa [OData-kyselyn sarakkeiden valinnassa](#selecting-columns-in-power-apps), suorituskyky vähenee aiheuttaen lisää tietohakuja.

Voit toimia näin varmistamalla, ettei Power Appin mihinkään tietolomakkeeseen ole sisällytetty liittyvien taulujen tietokenttiä.

1. Valitse puunäkymäruudusta näytön tietolomake.
2. Valitse **Kentät**-ominaisuuden **Ominaisuudet**-ruudussa **Muokkaa**.
3. Varmista **tieto** ruudussa, että mikään valituista kentistä ei ole tietolähteen virtuaalitaulun kenttiä.

Jos jokin sovellukseen sisältyvän sivun tietokentistä esimerkiksi viittaa toiseen tauluun, kuten **ThisItem.Worker.Name**, jossa **työntekijä** on liittyvä taulu, tietojen hakeminen voi vähentää suorituskykyä.

[Power Apps -valvontaruudulla](/powerapps/maker/monitor-overview) voit varmistaa, että kyselyyn sisällytetään vain tarvitsemiasi sarakkeita, kun Power App -sovelluksen tiedot hankitaan. Kun tarkastelet getRows-toimintoon suunniteltua URL-osoitetta, voit varmistaa, että sovelluksesi sarakkeet noudetaan mahdollisimman helposti.

![GetData-toiminnon analysoiminen Power Apps Monitorin avulla](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>Tietokyselyn suodattaminen

Toinen tapa parantaa kyselyn suoritustehoa on rajoittaa kyselyn tuloksissa palautettujen tietueiden määrää. Voit tehdä tämän suodattamalla tulokset, jotta voit varmistaa, että vastaanotat vain tarvitsemasi tietueet.

Lisätietoja kyselytietojen suodatuksesta on [suodatustuloksissa](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results).

### <a name="limiting-the-page-size-of-the-query"></a>Kyselyn sivun koon rajoittaminen

Jos käytät suuria tietojoukkoja, voit jakaa kyselyn tulokset useiksi sivuiksi lisäämällä haluamasi `odata.maxpagesize`-otsikon tietokyselyihin.

Lisätietoja sivutus-osasta on kohdassa [Sivulle palautettavan yksiköiden määrittäminen](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).

## <a name="see-also"></a>Lisätietoja

- [Määritä Dataverse -virtuaalitaulukot](hr-admin-integration-common-data-service-virtual-entities.md)
- [Human Resources -virtuaalitaulukoiden usein kysytyt kysymykset](hr-admin-virtual-entity-faq.md)
- [Rajoittamisen usein kysytyt kysymykset](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]