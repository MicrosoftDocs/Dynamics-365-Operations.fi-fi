---
title: Valitse tietojen integrointiteknologia
description: Tässä aiheessa on tietoja, jotka liittyvät henkilöstöhallinnon hallitsemien tietojen integroimiseen.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d58a42236b07bf177e09aee50a207ffdf2ed1435
ms.sourcegitcommit: 72a82e9aeabbdecf57e1aee72975c63eba75143a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/24/2021
ms.locfileid: "7414711"
---
# <a name="choose-a-data-integration-technology"></a>Valitse tietojen integrointiteknologia

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä aiheessa on tietoja Dynamics 365 Human Resourcesin hallitsemien tietojen integroimiseen. Siinä kuvataan erilaisia integrointitekniikoita, joiden avulla voit päättää, mitkä tekniikat sopivat parhaiten tarpeisiisi.

## <a name="data-integration-background"></a>Tietojen integroinnin taustatietoja

Liiketoimintatiedot ovat keskeinen resurssi, joka tekee yrityksestä yksilöllisen. Liiketoimintatietosi ovat todella arvokkaita. Voit käyttää koko yrityksessä kerättyjen tietojen välisiä suhteita liiketoimintaprosessien ja liiketoimintatietojen parantamiseen koko organisaatiossa. Pyrimme tarjoamaan liiketoimintatietoihin helpon, turvallisen ja vakaan käyttöoikeuden riippumatta siitä, mistä järjestelmästä se on peräisin.

Historiallisesti tietojen integrointi eri järjestelmien välillä on ollut vaikeaa. Microsoft on ryhtynyt toimenpiteisiin helpottaakseen tietojen integrointia, ja merkittävä edistysaskel tässä on saavutettu [Dataversellä](/powerapps/maker/common-data-service/data-platform-intro).

Human Resources tekee Dataversestä ensisijaisen julkisen rajapinnan Human Resourcesin tietoja varten. Ajan mittaan odotamme, että kaikki tärkeimmät henkilöhallintoon liittyvät tiedot näkyvät Dataversessä. Suosittelemme Dataverseä ensisijaiseksi teknologiaksi suurimmassa osassa integrointisovelluksista.

Ymmärrämme, että Dataverse ei ehkä vielä sisällä kaikkia tietoja, joita sovelluksesi edellyttää. Ymmärrämme myös, että projektin aikataulu saattaa edellyttää vaihtoehtoista tekniikkaa. Muista kertoa meille, milloin Dataverse ei vastaa integrointitarpeitasi.

## <a name="integration-technologies"></a>Integrointiteknologiat

Seuraavissa osissa kuvataan erilaiset tiedonintegrointiteknologiat, jotka ovat käytettävissä Human Resourcesin yhteydessä.

### <a name="dataverse-tables"></a>Dataverse-taulut

Dataverse on ensisijainen julkinen tietorajapinta Human Resourcesia varten. Se syntyi Dynamics 365 XRM -ympäristöstä, jota [Dynamics 365 Customer Engagement](/dynamics365/?panel=customer-engagement#pivot=business-apps) -ratkaisut käyttävät.

Dataverse tarjoaa tietotaulukoille alustan ja ohjelmointirajapintaliittymän. Kun otat henkilöstöhallinnon käyttöön, se muodostaa yhteyden Dataverse -yksikköön. Henkilöstöhallinnon tiedot otetaan käyttöön kyseisessä Dataverse -yksikössä. Taulukot ja niiden tiedot ovat kaikkien niiden sovellusten käytettävissä, jotka pystyvät muodostamaan yhteyden Dataverse -esiintymään. Henkilöstöhallinto synkronoi tiedot tulevien ja lähtevien Dataverse-taulukoiden välillä.

> [!NOTE]
> Human Resources -yksiköt vastaavat Dataverse-tauluja. Lisätietoja Dataversesta (aiemmin Common Data Service) ja terminologiapäivityksistä on kohdassa [Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Kun integroiviin sovelluksiin tarvittavat tietotaulukot ovat käytössä Dataversessä, voit käyttää täysin [Dataverse -järjestelmän ja sen tukemien ohjelmointirajapintaliittymien tietoja](/powerapps/?panel=developer#pivot=home). Yksi tuetuista ohjelmointirajapinnoista on [Dynamics 365:n verkko-ohjelmointirajapinta](/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), joka tarjoaa OData-toteutuksen Dataverse -tietojen käyttöä varten.

Dataverse-taulukot ja niihin liittyvät ohjelmointirajapinnat ovat paras vaihtoehto Human Resources -tietojen käyttämiselle verkkosovelluksilla, verkkopalveluilla/verkko-ohjelmointirajapinnoilla ja millä tahansa muilla sovelluksilla, jotka muodostavat yhteyden OData-syötteisiin.

> [!NOTE]
> Koska päätös tehdä Dataversestä ensisijainen tietotoajapinta Human Resourcesille on varsin tuore, saatat huomata, että integrointiasi varten tarvittavat Human Resource -tietoyksiköt eivät vielä ole käytettävissä Dataversessä.
> </br>
> Luettelo Dataversessä käytettävistä Human Resources -yksiköistä esitetään kohdassa [Human Resources ja Dataverse](/dynamics365/unified-operations/talent/corehrentities).
> </br>
> Jos integrointiin tarvittavat Human Resources -yksiköt eivät vielä ole käytettävissä, sinun on joko odotettava, että ne tulevat saataville, tai sinun on käytettävä jotakin alla esitetyistä muista integrointiteknologioista.
> </br>
> Dataverse -integrointi on oletusarvoisesti pois käytöstä uudessa ympäristössä, joka ei sisällä toimitettuja demotietoja. Se on käytössä uusissa ympäristöissä, jotka sisältävät demotietoja, ja ympäristöt alkavat synkronoida tietoja, kun ne on provisioitu. Kyn ympäristö on valmis synkronoimaan tietoja, voit ottaa integroinnin käyttöön.

### <a name="dmfdixf-entities"></a>DMF-/DIXF-yksiköt

Henkilöresurssit, jotka on rakennettu ensisijaisesti samalle alustalle kuin Finance and Operations -sovellukset, tarjoavat [Tietojenhallintakehyksen (DMF)](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json). DMF tunnetaan myös tietojen tuonnin vientikehyksenä (DIXF). Henkilöstöhallinnossa on joukko tietokokonaisuuksia, joita voidaan käyttää henkilöstöhallinnon tietojen tuomiseen ja viemiseen. Vaikka Dataverse-taulukot ovat ensisijainen tietojen integrointirajapinta Human Resourcesia varten, DMF-yksiköt ovat edelleen hyödyllisiä joissakin olosuhteissa, kuten:

- Dataverse-taulukot eivät ole vielä käytettävissä.

- Integrointi edellyttää suuren suorituskyvyn tietojen joukkotuonnin/ä-viennin valmiuksia.

> [!NOTE]
> Human Resources -yksiköt vastaavat Dataverse-tauluja. Lisätietoja Dataversesta (aiemmin Common Data Service) ja terminologiapäivityksistä on kohdassa [Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

DMF-yksiköt tarjoavat tällä hetkellä kokonaisvaltaisimman tietojen kattavuuden Human Resources -tietojen osalta.

DMF ei sovellu reaaliaikaiseen integraatioihin, kuten silloin, kun käyttäjän käyttöliittymässä tarvitaan välitöntä käyttäjäpalautetta. Paketin työvaiheet ajoitetaan erätöiden mukaan, ja usein niissä on vähintään 1 - 2 minuutin viive, ennen kuin eräpalvelu poimii tehtävän suoritusta varten sekä tuonti- ja vientitoiminnon suorittamiseen tarvittava aika.

DMF saattaa olla paras vaihtoehto, kun tarvitaan suurta kapasiteettia (esim. joka yö suoritettava monen tuhannen tietueen tuonti/vienti).

> [!NOTE]
> DMF ei ole käytettävissä Attractissa tai Onboardissa.

### <a name="dmf-package-rest-api"></a>DMF-paketin REST API

DMF tarjoaa [REST API](/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) -rajapinnan tietopakettien käsittelyyn. Tätä ohjelmointirajapintaa voidaan käyttää ohjelmalliseen vuorovaikutukseen DMF:n kanssa. Tämä mahdollistaa esimerkiksi seuraavat toiminnot:

- Tietopaketin tuominen.

- Tietopaketin vieminen.

- Tuonti- tai vientitoiminnon tilan tarkistaminen.

DMF-paketin REST API -rajapintaa tuetaan täysin Human Resourcesissa.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF tarjoaa lisäksi tehokkaan toiminnon (joka tunnetaan nimellä [Tuo oma tietokantasi](/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) tai BYOD), jonka avulla Human Resources voi viedä tietoja omaan Microsoft Azure SQL -tietokantaasi. Tämä ominaisuus tarjoaa valtavasti joustavuutta. Kun tiedot ovat omassa SQL-tietokannassasi, voit käyttää mitä tahansa sovelluksia tai väliohjelmistoja, jotka voivat muodostaa yhteyden SQL-tietovarastoon.

BYOD on lähinnä vain lukumuotoinen ratkaisu. Vaikka voit käsitellä ja tallentaa kaikkia haluamiasi tietoja Azure SQL -tietokantaan (kuten tietoyhdistelmiä (mashup)), Azure SQL -tietokantaan tallennettuja tietoja ei synkronoida takaisin Human Resourcesiin.

BYOD soveltuu raportointiratkaisuihin, tietojen integrointiin, tietojen yhdistämiseen sekä tietolähteeksi [Azure Data Factoryn](/azure/data-factory/) pipelineen.

> [!NOTE]
> BYOD ei ole käytettävissä Attractissa tai Onboardissa.

### <a name="odata-enabled-entities"></a>OData-yhteensopivat yksiköt

Useimpia DMF-yksikköjä voi käyttää myös Human Resources -tietopalvelun kautta (OData). [Finance and Operationsin OData-palvelua](/dynamics365/unified-operations/dev-itpro/data-entities/odata) koskevat asiakirjat koskevat henkilöresursseja, lukuun ottamatta omien ODatan suojaamien yksiköiden luomista.

Vaikka Dataverse ja Dataversen tarjoama OData-täytäntöönpano ([Dynamics 365:n verkko-ohjelmointirajapinnalla](/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))) on suositeltava Human Resourcesin tietopalvelun sijaan, Human Resourcesin tietopalvelu kattaa tällä hetkellä Human Resources -tietojen yksiköt laajemmin.

### <a name="excel-add-in"></a>Excel-lisäosa

[Excel-lisäosa](/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) käyttää OData-yhteensopivia yksikköjä pinnan alla. Se tarjoaa kätevän tavan, jolla käyttäjä voi noutaa ja muokata Human Resources -tietoja tutun Excel-käyttöliittymän kautta.

Excel-lisäosa sopii liiketoiminnan toimialueasiantuntijoiden tietojen ad-hoc-tuonneille/-vienneille. Toistuvaan tietojen integrointiin, joka vaatii ohjelmallista automaatiota, soveltuu paremmin jokin muu integrointiteknologia.

### <a name="data-integrator"></a>Tietojen integrointiohjelma

[Tietojen integrointipalvelun](/powerapps/administrator/data-integrator) avulla voit integroida tietoja Dataverse -järjestelmään ja -järjestelmästä. Tietojen integrointiohjelma antaa sinun määrittää integrointiprojektit, jotka perustuvat usein ennalta määritettyihin malleihin, jotka sovelluskehittäjät ovat räätälöineet tietyille integraatioille. Voit ajoittaa integrointiprojektit suoritettavaksi automaattisesti toistuvassa aikataulussa tai suorittaa ne manuaalisesti.

Tietojen integrointiprojektit soveltuvat Dataversen eräintegraatioihin. Ne ovat erinomainen vaihtoehto integraatioille Dynamics 365 -perheen sovellusten välillä. Esimerkiksi Microsoft tarjoaa tietojen integrointiohjelman mallin, jota voidaan käyttää Human Resources -tietojen integroimiseen Dynamics 365 Financeen. Lisätietoja mallista kohdassa  [Integrointi Dynamics 365 Human Resources -mallista Dynamics 365 Finance-järjestelmään](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Tietojen integrointiohjelma tukee [Power Queryä](/power-query/power-query-what-is-power-query) [Lisäkysely-toiminnollaan](/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering). Power Query tarjoaa tehokkaan, joustavan tietojen suodatuksen ja muunnoksen, mukaan lukien Rich M-kaavakielen. Power Query on todennäköisesti tuttu, jos olet kehittänyt Power BI -raportteja.

## <a name="deciding-on-an-integration-technology"></a>Integrointiteknologian valinta

Kun tarjolla on niin monta erilaista integrointiteknologiaa, integrointimenetelmän valinta saattaa joskus tuntua ylivoimaiselta. Dataversen tietokattavuuden kypsyessä päätöksestä tulee helpompi ja Dataversestä tulee sopivin tietorajapinta useimmissa tapauksissa. Siihen asti saatat kuitenkin huomata, ettei Dataverse vielä vastaa tarpeitasi. Seuraava taulukko vetää yhteen joitakin integrointiteknologiaratkaisujen keskeisiä ominaisuuksia.

| Teknologia/Työkalu/API    | Toistuvat integraatiot                   | Synkroninen/asynkroninen                    | Ohjelmallinen käyttö ohjelmointirajapinnan kautta        | Asianmukaiset tietomäärät                                   | Tietokattavuus                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Dataverse-taulut           | Kyllä, tietojen integrointiohjelman tai väliohjelmiston avulla | Asynkronisen synkronointi, erä (tietojen integrointiohjelman kautta) | Kyllä, Dynamics 365:n verkko-ohjelmointirajapinnan kautta (OData) | Vaihtelee käyttötapauksen mukaan (tukee sivutusta vuorovaikutteista käyttöä varten) | <sup>2</sup>:n                       |
| DMF-yksikön parantaminen           | Kyllä, väliohjelmistojen kautta ajoitettuna        | Asynkroninen, erä                                | Kyllä, DMF-paketin REST API:n kautta         | Suuri (satoja tuhansia tietueita)                    | Korkea                                |
| DMF-paketin REST API   | Kyllä, väliohjelmistojen kautta ajoitettuna        | Asynkroninen, erä                                | Kyllä                                       | Suuri (satoja tuhansia tietueita)                    | Ohjelmointirajapinta tukee kaikkia DMF-yksiköitä       |
| BYOD                   | Kyllä, järjestelmänvalvojan Human Resourcesissa ajoittamana        | Asynkroninen, erä                                | No<sup>3</sup>                                    | Suuri (satoja tuhansia tietueita)                    | Tukee kaikkia DMF-yksiköitä           |
| OData-yhteensopivat yksiköt | Kyllä, käyttämällä väliohjelmistoa                    | Synkronoi                                        | Kyllä, Human Resourcesin tietopalvelun (OData) kautta  | Vaihtelee käyttötapauksen mukaan (tukee sivutusta vuorovaikutteista käyttöä varten) | Korkea                                |
| Excel-lisäosa           | Ei                                       | Synkronoi                                        | Ei                                        | Keskisuuri (kymmeniä tuhansia tietueita)                      | Tukee kaikkia OData-yhteensopivia yksikköjä |
| Tietojen integrointiohjelma        | Kyllä, tietojen integrointiohjelmassa ajoitettuna        | Asynkroninen, erä                                | Nro                                        | Vaihtelee käyttötapauksen mukaan                                       | Tukee kaikkia Dataverse-tauluja           |

<sup>2</sup>Microsoft investoi voimakkaasti tietojen kattavuuden lisäämiseksi Dataverse-taulukoille. On suositeltavaa käyttää Dataverseä, kun kattavuus on käytettävissä. Tällä hetkellä Dataversen tietojen kattavuus on alhainen DMF- ja OData-yhteensopiviin yksikköihin verrattuna.

<sup>3</sup>SQL-tietokantaa voidaan käyttää ohjelmallisesti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
