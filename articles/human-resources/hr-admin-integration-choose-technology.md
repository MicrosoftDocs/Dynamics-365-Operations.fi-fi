---
title: Tietojen integrointiteknologian valitseminen
description: Tässä artikkelissa esitellään erilaisia vaihtoehtoja annetaan Human Resourcesin tietoihin integroinnille ja annetaan kuvaus erilaisten integrointiteknologioiden ominaisuuksia, jotta integroijat voivat tehdä tietoon perustuvia päätöksiä siitä, mitkä teknologiat sopivat heidän tarpeisiinsa parhaiten.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f2de5dd41c00e6546b4a4feadaf5774430d572bb
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029885"
---
# <a name="choose-a-data-integration-technology"></a>Tietojen integrointiteknologian valitseminen

Dynamics 365 Human Resources hallitsee liiketoimintatietoja, joista on hyötyä erilaisissa liiketoimintaprosesseissa. Tässä artikkelissa esitellään erilaisia vaihtoehtoja annetaan Human Resourcesin tietoihin integroinnille ja annetaan kuvaus erilaisten integrointiteknologioiden ominaisuuksia, jotta integroijat voivat tehdä tietoon perustuvia päätöksiä siitä, mitkä teknologiat sopivat heidän tarpeisiinsa parhaiten.

## <a name="data-integration-vision"></a>Tietojen integrointivisio

Microsoft näkee liiketoimintatiedot keskeisenä resurssina, joka tekee yrityksestä yksilöllisen. Liiketoimintatietosi ovat todella arvokkaita. Yhden yrityksen osan keräämät ja ylläpitämät tiedot liittyvät toisen yrityksen osan keräämiin tietoihin, ja näitä suhteita voidaan käyttää liiketoimintaprosessien ja yritystietojen parantamisessa koko organisaation laajuisesti. Helpon, turvallisen ja vakaan liiketoimintatietojen käytön varmistaminen on keskeinen periaate visiossamme tietojen integroinnista Human Resourcesiin riippumatta siitä, mikä järjestelmä "omistaa" tiedot.

Historiallisesti tietojen integrointi eri järjestelmien välillä on ollut vaikeaa.
Microsoft on ryhtynyt toimenpiteisiin helpottaakseen tietojen integrointia, ja merkittävä edistysaskel tässä on saavutettu [Common Data Servicellä](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Jatkossa Human Resources tekee Common Data Servicestä ensisijaisen julkisen rajapinnan Human Resourcesin tietoja varten. Ajan mittaan odotamme, että kaikki tärkeimmät henkilöhallintoon liittyvät tiedot näkyvät Common Data Servicessä. Suosittelemme Common Data Serviceä ensisijaiseksi teknologiaksi suurimmassa osassa integrointisovelluksista. Vaikka ymmärrämme, että kaikki sovelluksesi tarvitsemat tiedot eivät tällä hetkellä ole Common Data Servicessä ja että projektiaikataulusi saattaa edellyttää vaihtoehtoista teknologiaa, pyydämme sinua kertomaan meille, milloin Common Data Service ei vastaa integrointitarpeistasi.

## <a name="integration-technologies"></a>Integrointiteknologiat

Seuraavissa osissa kuvataan erilaiset tiedonintegrointiteknologiat, jotka ovat käytettävissä Human Resourcesin yhteydessä.

### <a name="common-data-service-entities"></a>Common Data Service -entiteetit

Common Data Service on ensisijainen julkinen tietorajapinta Human Resourcesia varten. Common Data Service rakentuu kypsälle ympäristölle, koska se perustuu Dynamics 365 XRM -ympäristölle, jolle [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement) -ratkaisut rakentuvat.

Common Data Service tarjoaa ympäristön tietoyksiköille ja ohjelmointirajapinnan kyseisten yksikköjen käytölle. Kun Human Resources otetaan organisaatiossa, se yhdistetään Common Data Service -esiintymään, ja Human Resourcesin tietoja ylläpitävät yksiköt otetaan käyttöön kyseisessä Common Data Service -esiintymässä. Tämä antaa yksiköt ja niiden tiedon kaikkien niiden sovellusten käyttöön, jotka voivat muodostaa yhteyden Common Data Service -esiintymään. Riippuen käytössä olevista Human Resources -sovelluksista Human Resources joko suorittaa tietotoimintoja suoraan Common Data Service -yksikköjen perusteella (Attract ja Onboard) tai synkronoi tiedot Common Data Service -yksikköjen kanssa kumpaankin suuntaan.

Kun tietoyksiköt, jotka näyttävät integrointisovellustesi tarvitsemat tiedot, ovat Common Data Servicessä, voit hyödyntää täysimääräisesti [Common Data Serviceä ja sen tukemia ohjelmointirajapintoja](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer). Yksi tuetuista ohjelmointirajapinnoista on [Dynamics 365:n verkko-ohjelmointirajapinta](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), joka tarjoaa OData-toteutuksen Common Data Service -tietojen käyttöä varten.

Common Data Service -yksiköt ja niihin liittyvät ohjelmointirajapinnat ovat paras vaihtoehto Human Resources -tietojen käyttämiselle verkkosovelluksilla, verkkopalveluilla/verkko-ohjelmointirajapinnoilla ja millä tahansa muilla sovelluksilla, jotka muodostavat yhteyden OData-syötteisiin.

> [!NOTE]
> Koska päätös tehdä Common Data Servicestä ensisijainen tietotoajapinta Human Resourcesille on varsin tuore, saatat huomata, että integrointiasi varten tarvittavat Human Resource -tietoyksiköt eivät vielä ole käytettävissä Common Data Servicessä<sup>1.</sup> Jos integrointiin tarvittavat Human Resources -yksiköt eivät vielä ole käytettävissä, sinun on odotettava, että ne tulevat saataville, tai sinun on käytettävä jotakin alla esitetyistä muista integrointiteknologioista.
> 
> Common Data Service -integrointi on oletusarvoisesti pois käytöstä uudessa ympäristössä, joka ei sisällä toimitettuja demotietoja. Se on käytössä uusissa ympäristöissä, jotka sisältävät demotietoja, ja ympäristöt alkavat synkronoida tietoja, kun ne on provisioitu. Kyn ympäristö on valmis synkronoimaan tietoja, voit ottaa integroinnin käyttöön.

<sup>1</sup>Luettelo Common Data Servicessä käytettävistä Human Resources -yksiköistä esitetään kohdassa [Human Resources ja Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities). Attractin ja Onboardin osalta kaikki yksiköt ovat käytettävissä Common Data Servicessä.

### <a name="dmfdixf-entities"></a>DMF-/DIXF-yksiköt

Human Resources rakentuu pääosin samalle ympäristölle kuin Finance and Operations -sovellukset ja tarjoaa [tiedonhallintakehyksen (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json), jota kutsutaan joskus myös tietojen tuonti- ja vientikehykseksi (DIXF), sekä joukon tietoyksikköjä, joita voidaan käyttää tietojen tuomiseen Human Resourcesiin tai sieltä viemiseen. Vaikka Common Data Service -yksiköt ovat ensisijainen tietojen integrointirajapinta Human Resourcesia varten, DMF-yksiköt ovat edelleen hyödyllisiä joissakin olosuhteissa, kuten:

- Common Data Service -yksiköt eivät ole vielä käytettävissä.

- Integrointi edellyttää suuren suorituskyvyn tietojen joukkotuonnin/ä-viennin valmiuksia.

DMF-yksiköt tarhaovat tällä hetkellä kokonaisvaltaisimman tietojen kattavuuden Human Resources -tietojen osalta.

DMF ei sovellu reaaliaikaiseen integrointiin (kuten, jos käyttöliittymässä tarvitaan välitöntä käyttäjäpalautetta), koska pakettitoiminnot ovat ajoitettuja erätöitä, joilla on usein vähintään 1–2 minuutin viive, ennen kuin eräpalvelu tarttuu työhön suorittamista varten. Lisäksi on otettava huomioon vielä aika, jonka tuonnin tai viennin suorittaminen vaatii.

DMF saattaa olla paras vaihtoehto, kun tarvitaan suurta kapasiteettia (esim. joka yö suoritettava monen tuhannen tietueen tuonti/vienti).

> [!NOTE]
> DMF ei ole käytettävissä Attractissa tai Onboardissa.

### <a name="dmf-package-rest-api"></a>DMF-paketin REST API

DMF tarjoaa [REST API](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) -rajapinnan tietopakettien käsittelyyn. Tätä ohjelmointirajapintaa voidaan käyttää ohjelmalliseen vuorovaikutukseen DMF:n kanssa. Tämä mahdollistaa esimerkiksi seuraavat toiminnot:

- Tietopaketin tuominen.

- Tietopaketin vieminen.

- Tuonti- tai vientitoiminnon tilan tarkistaminen.

DMF-paketin REST API -rajapintaa tuetaan täysin sovelluksessa Human Resources: Core HR.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF tarjoaa lisäksi tehokkaan toiminnon (joka tunnetaan yleisesti nimellä [Tuo oma tietokantasi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) tai BYOD), jonka avulla Human Resources voi viedä tietoja omaan Microsoft Azure SQL -tietokantaasi. Tämä tarjoaa valtavasti joustavuutta, sillä kun tiedot ovat omassa SQL-tietokannassasi, voit käyttää mitä tahansa sovelluksia tai väliohjelmistoja, jotka voivat muodostaa yhteyden SQL-tietovarastoon.

BYOD pitäisi yleisesti katsoa pelkäksi lukuratkaisuksi. Vaikka voit käsitellä ja tallentaa kaikkia haluamiasi tietoja Azure SQL -tietokantaan (kuten tietoyhdistelmiä (mashup)), Azure SQL -tietokantaan tallennettuja tietoja ei synkronoida takaisin Human Resourcesiin.

BYOD soveltuu raportointiratkaisuihin, tietojen integrointiin, tietojen yhdistämiseen sekä tietolähteeksi [Azure Data Factoryn](https://docs.microsoft.com/azure/data-factory/) pipelineen.

> [!NOTE]
> BYOD ei ole käytettävissä Attractissa tai Onboardissa.

### <a name="odata-enabled-entities"></a>OData-yhteensopivat yksiköt

Useimpia DMF-yksikköjä voi käyttää myös Human Resources -tietopalvelun kautta (OData). [Finance and Operationsin OData-palvelua](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) varten toimitettu dokumentaatio pätee yleisesti myös Human Resourcesiin, vaikka oman OData-palvelussa näkyvien yksikköjen luomista koskeva dokumentaatio ei pädekään.

Vaikka Common Data Service ja Common Data Servicen tarjoama OData-täytäntöönpano ([Dynamics 365:n verkko-ohjelmointirajapinnalla](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))) on suositeltava Human Resourcesin tietopalvelun sijaan, Human Resourcesin tietopalvelu kattaa tällä hetkellä Human Resources -tietojen yksiköt laajemmin.

### <a name="excel-add-in"></a>Excel-lisäosa

[Excel-lisäosa](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) käyttää OData-yhteensopivia yksikköjä pinnan alla. Se tarjoaa kätevän tavan, jolla käyttäjä voi noutaa ja muokata Human Resources -tietoja tutun Excel-käyttöliittymän kautta.

Excel-lisäosa sopii liiketoiminnan toimialueasiantuntijoiden tietojen ad-hoc-tuonneille/-vienneille. Toistuvaan tietojen integrointiin, joka vaatii ohjelmallista automaatiota, soveltuu paremmin jokin muu integrointiteknologia.

### <a name="data-integrator"></a>Tietojen integrointiohjelma

Common Data Servicen järjestelmänvalvojakokemus tarjoaa [Tietojen integrointipalvelun](https://docs.microsoft.com/powerapps/administrator/data-integrator), jota voidaan käyttää tietojen integrointiin molempiin suuntiin Common Data Servicessä. Tietojen integrointiohjelmaa voidaan käyttää integrointiprojektien määrittämiseen (usein sovelluskehittäjien tiettyjä integrointia varten esimäärittämien mallien pohjalta). Integrointiprojektit voidaan ajoittaa suoritettavaksi automaattisesti toistuvassa aikataulussa tai suorittaa manuaalisesti.

Tietojen integrointiprojektit soveltuvat Common Data Servicen eräintegrointeihin ja ovat loistava valinta Dynamics 365 -sovellusperheen välisiin integrointeihin. Esimerkki: Microsoft tarjoaa valmiiksi määritetyn tietojen integrointiohjelman mallin, jota voidaan käyttää Human Resources -tietojen integroimiseen Dynamics 365 Financeen. Lisätietoja on kohdassa [Integrointi Dynamics 365 Human Resourcesista Dynamics 365 Financeen](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Tietojen integrointiohjelma tukee myös [Power Queryä](https://docs.microsoft.com/power-query/power-query-what-is-power-query) ([Lisäkysely-toiminnollaan](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering)).
Power Query tarjoaa tehokasta, joustavaa tietojen suodatusta ja muuntamista sekä monimuotoisen M-kaavakielen. Lisäksi se lienee tuttu kaikille niille, joilla on kokemusta Power BI -raporttien kehittämisestä.

## <a name="deciding-on-an-integration-technology"></a>Integrointiteknologian valinta

Kun tarjolla on niin monta erilaista integrointiteknologiaa, integrointimenetelmän valinta saattaa joskus tuntua ylivoimaiselta. Ajan myötä ja etenkin Common Data Servicen tietokattavuuden kypsetessä päätöksestä tulee helpompi ja Common Data Servicestä tulee sopivin tietorajapinta useimmissa tapauksissa. Siihen asti saatat kuitenkin huomata, ettei Common Data Service vielä vastaa tarpeitasi. Seuraavassa taulukossa vedetään yhteen joitakin erilaisten integrointiteknologiaratkaisujen keskeisiä ominaisuuksia.

| Teknologia/Työkalu/API    | Toistuvat integroinnit                   | Synkroninen/asynkroninen                    | Ohjelmallinen käyttö ohjelmointirajapinnan kautta        | Asianmukaiset tietomäärät                                   | Tietokattavuus                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service -yksiköt           | Kyllä, tietojen integrointiohjelman tai väliohjelmiston avulla | Asynkronisen synkronointi, erä (tietojen integrointiohjelman kautta) | Kyllä, Dynamics 365:n verkko-ohjelmointirajapinnan kautta (OData) | Vaihtelee käyttötapauksen mukaan (tukee sivutusta vuorovaikutteista käyttöä varten) | <sup>2</sup>:n                       |
| DMF-yksikön parantaminen           | Kyllä, väliohjelmistojen kautta ajoitettuna        | Asynkroninen, erä                                | Kyllä, DMF-paketin REST API:n kautta         | Suuri (satoja tuhansia tietueita)                    | Korkea                                |
| DMF-paketin REST API   | Kyllä, väliohjelmistojen kautta ajoitettuna        | Asynkroninen, erä                                | Kyllä                                       | Suuri (satoja tuhansia tietueita)                    | Ohjelmointirajapinta tukee kaikkia DMF-yksiköitä       |
| BYOD                   | Kyllä, järjestelmänvalvojan Human Resourcesissa ajoittamana        | Asynkroninen, erä                                | No<sup>3</sup>                                    | Suuri (satoja tuhansia tietueita)                    | Tukee kaikkia DMF-yksiköitä           |
| OData-yhteensopivat yksiköt | Kyllä, käyttämällä väliohjelmistoa                    | Synkronoi                                        | Kyllä, Human Resourcesin tietopalvelun (OData) kautta  | Vaihtelee käyttötapauksen mukaan (tukee sivutusta vuorovaikutteista käyttöä varten) | Korkea                                |
| Excel-lisäosa           | Ei                                       | Synkronoi                                        | Ei                                        | Keskisuuri (kymmeniä tuhansia tietueita)                      | Tukee kaikkia OData-yhteensopivia yksikköjä |
| Tietojen integrointiohjelma        | Kyllä, tietojen integrointiohjelmassa ajoitettuna        | Asynkroninen, erä                                | Ei                                        | Vaihtelee käyttötapauksen mukaan                                       | Tukee kaikkia Common Data Service -yksikköjä           |

<sup>2</sup>Microsoft investoi vahvasti tietokattavuuden lisäämiseen Common Data Service -yksikköjen osalta ja suosittelee Common Data Serviceä ensisijaisena tietorajapintana, kun kattavuutta on käytettävissä. Tällä hetkellä Common Data Servicen tietojen kattavuus on alhainen DMF- ja OData-yhteensopiviin yksikköihin nähden.

<sup>3</sup>SQL-tietokantaa voidaan käyttää ohjelmallisesti.

## <a name="summary"></a>Yhteenveto

Liiketoimintatietosei ovat arvokas resurssi, mutta niiden arvo voi vähentyä merkittävästi, jos niiden käyttö omiin erityisiin tarkoituksiisi (kuten raportointiin, tietoyhdistelmiin tai mukautettuihin sovelluksiin) on hankalaa. Dynamics 365 Human Resources tarjoaa useita menetelmiä tietojesi käyttämiseen Human Resources -sovelluksen käyttöliittymän (UI) ulkopuolella. Tämä mahdollistaa integroiville sovelluksille tietojen käytön. Tässä aiheessa on kuvattu käytettävissä olevat integrointiteknologiat ja joitakin niiden tärkeimpiä ominaisuuksia. Näiden tietojen pitäisi auttaa sinua parempien päätösten tekemisessä siitä, mitä lähestymistapoja kannattaa hyödyntää integrointiprojekteissa.

