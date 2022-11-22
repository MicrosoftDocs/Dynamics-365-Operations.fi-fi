---
title: Virtuaalitaulukkopohjaisten integrointien suojausmäärityksen käsitteet
description: Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Human Resourcesin ja muiden järjestelmien välisen integroinnin arkkitehtuurista.
author: twheeloc
ms.date: 11/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 219ceb0adae0cee5f74a39140ab74af9fdac1eb6
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759651"
---
# <a name="security-configuration-concepts-for-virtual-table-based-integrations"></a>Virtuaalitaulukkopohjaisten integrointien suojausmäärityksen käsitteet

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kerrotaan [Microsoft Dataversen virtuaalitaulukoiden (entiteettien)](/dev-itpro/power-platform/virtual-entities-overview) käyttämisen arkkitehtuurista Dynamics 365 Human Resourcesin ja kolmannen osapuolen järjestelmän välisen integroinnin muodostamisessa. Artikkelissa keskitytään suojausmääritykseen ja järjestelmärajojen välille vaadittujen todennus- ja valtuutusnäkökohtiin toimivan ja suojatun järjestelmän luomiseksi.

## <a name="prerequisite-reference-articles"></a>Edellytysten viiteartikkelit

Seuraavissa artikkeleissa on tietoja tämän artikkelin käsitteistä:

- [Virtuaaliyksiköiden yleiskatsaus](/dev-itpro/power-platform/virtual-entities-overview)
- [Virtuaalitaulukoiden (entiteettien) käytön aloittaminen](/developer/data-platform/virtual-entities/get-started-ve)
- [Usean vuokraajan palvelimien välisen todennuksen käyttäminen (Microsoft Dataverse)](/developer/data-platform/use-multi-tenant-server-server-authentication)
- [OAuth-todennuksen käyttäminen Microsoft Dataversen avulla (Dataverse)](/developer/data-platform/authenticate-oauth)
- [OAuth 2.0:n asiakkaan tunnistetietojen työnkulku Microsoftin käyttäjätietoympäristössä](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)
- [Todentaminen ja valtuutus](/dev-itpro/power-platform/authentication-and-authorization)

## <a name="architecture"></a>Arkkitehtuuri 

Seuraavassa arkkitehtuurikaaviossa näkyvät pääkäsitteet, joita käytetään virtuaalitaulukoita (entiteettejä) käyttävässä integroinnissa.

![Virtuaalitaulukkoon perustuva integrointi.](./media/Hosts.jpg)

Tässä on joidenkin edellisen kaavion elementtien selitys:

- **Microsoft** – Microsoft isännöi ja operoi erilaisia Dynamics 365 -tuotteita asiakkaiden puolesta.

    - **Azure Active Directory (Azure AD) -vuokraaja C** – Microsoftin omistama Azure AD -vuokraaja. Tämä on vuokraaja, jolle Dynamics 365 -sovellukset on rekisteröity.

- **Integroitava kumppani**

    - **Integroitava järjestelmä** – Järjestelmä, joka integroidaan Dynamics 365:een. Se voi olla palkanlaskentajärjestelmä tai muu järjestelmä, joka käyttää Dynamics 365:een tallennettuja tietoja.
    - **Sovitin** – Ohjelmisto tai palvelu, joka vastaa yhteydenpidosta sekä Dynamics 365:n että integroitavan järjestelmän kanssa.

        > [!NOTE]
        > Jos sovitin on tarkoitettu useiden Dynamics 365 -asiakkaiden käyttöön, oletuksena on, että se rekisteröidään usean vuokraajan sovellukseksi Azure AD:ssä.

    - **Azure AD -vuokraaja A** – Azure AD -vuokraaja, jonka integroitava kumppani omistaa. Tämä on vuokraaja, jolle sovittimen sovellustunnus on rekisteröity.

- **Yhteinen asiakas** – Asiakas, joka ottaa käyttöön Dynamics 365 Human Resourcesin ja integroitavan kumppanin ratkaisun.

    - **Dynamics 365 Finance tai Human Resources** – Dynamics 365 Financen tai Human Resourcesin asiakaskohtainen esiintymä, joka sisältää integroitavan järjestelmän vaatimat asiakastiedot.
    - **Dataverse** – Asiakaskohtainen Dataverse-ympäristö, joka on yhdistetty Financeen tai Human Resourcesiin. Dataverse sisältää verkkopalvelujen ohjelmointirajapinnan Dynamics 365 -tietojen integrointia varten.
    - **Azure AD -vuokraaja B** – Asiakkaan Azure AD -vuokraaja. Se toimii tunnistetietojen tarjoajana (käyttöoikeuksien tarkistuspalvelimena) ja antaa tunnukset, jotka valtuuttavat kutsujat kutsumaan asiakkaan Dataverse-esiintymää.

## <a name="basic-request-flow"></a>Pyynnön perustyönkulku

Tässä osassa kuvataan integrointiin liittyvän tyypillisen pyynnön perustyönkulku. Se viittaa aiemmin tässä artikkelissa olevaan arkkitehtuurikaavioon.

Tyypillinen pyyntö edellyttää sovittimen tekemää kyselyä Dynamics 365:n tiedoista. Tämän jälkeen tiedot tallennetaan ja synkronoidaan integroitavan järjestelmän kanssa.

1. Sovitin kutsuu Dataversen verkkopalvelujen ohjelmointirajapintaa liittyvien tietojen kyselyä varten.

    > [!NOTE]
    > Todennus on edellytys. Tunnuksen hankinta on iso osa prosessia. Todennuksesta kerrotaan [Todennus ja valtuutus järjestelmärajoilla](#authentication-and-authorization-at-system-boundaries) -osassa.

    Tämä kutsu tehdään Dataversen verkkopalvelujen ohjelmointirajapinnalle sovellustiedoissa niin, että niitä voidaan käyttää virtuaalitaulukossa. (Katso 2. Ensimmäinen synkronointi ja 3. Muutossynkronointi kaaviossa.)

2. Dataverse käsittelee pyynnön tekemällä kyselyn virtuaalitaulukossa virtuaalientiteetin laajennuksen (kaaviossa Virtuaalitaulukon välityspalvelin) avulla. Dataversen pyyntö välitetään Financen tai Human Resourcesin virtuaalientiteetin palvelulle, jossa tehdään kyselyä tiedoista, jotka on tallennettu fyysisesti Finance- tai Human Resources -tietokantaan.
3. Financen tai Human Resourcesin virtuaalientiteettipalvelu kääntää pyynnön virtuaalientiteetistä kyselyksi Financen tai Human Resourcesin entiteetille, joka tukee Dataversen virtuaalientiteettiä. Tiedot noudetaan tietokannasta, käännetään takaisin Dataversen entiteetiksi ja palautetaan kutsujalle.
4. Sovitin viimeistelee kaikki tarvittavat määritykset ja tietojen käännökset ja soittaa integroitavaan järjestelmään, jotta tiedot säilyvät integroitavan järjestelmän tietokannassa. (Katso 4. Tallenna tiedot kaaviossa.)

## <a name="authentication-and-authorization-at-system-boundaries"></a>Todennus ja valtuutus järjestelmärajoilla

*Todennus* tarkistaa, että käyttäjän tai sovelluksen tunnistetiedot on vahvistettu ja todettu oikeiksi. *Valtuutus* myöntää käyttäjälle tai sovellukselle tietyn sovellustason käyttöoikeudet. Lisätietoja on kohdassa [Todennus ja valtuutus](/azure/active-directory/develop/authentication-vs-authorization).

Useimmat aiemmin tässä artikkelissa olevien arkkitehtuurikaavioiden järjestelmien väliset kutsut koskevat sovitinta. Sovittimen on todennettava itsensä seuraavien kutsujen tekemistä varten:

- Dataversen kutsuminen
- Integroitavan järjestelmän kutsuminen

Etsi järjestelmärajat kaaviosta. Jokainen järjestelmien välinen verkkopyyntö on todennettava ja sovellustason valtuutustarkistukset on tehtävä hyväksytysti ennen tietojen palauttamista kutsujalle. Financen tai Human Resourcesin tukeman Dynamics 365:n virtuaalitaulukon pyynnöille on tehtävä todennus- ja valtuutustarkistukset seuraavissa järjestelmärajoissa:

- Sovittimen ja Dataversen verkkopalveluiden ohjelmointirajapinnan (OData) päätepisteen välinen kutsu
- Dataversen virtuaalientiteetin laajennuksen ja Financen tai Human Resourcesin virtuaalientiteettipalvelun välinen kutsu

Molemmissa tapauksessa tehdään ensin todennustarkistukset. Tämän jälkeen tehdään sovellustason valtuutustarkistukset. Niiden avulla varmistetaan, että todennetulla käyttäjällä tai sovelluksella on oikeat sovellustason oikeudet pyydettyjen tietojen noutamista varten.

Dataversen kutsun todennus käsitellään haltijan tunnuksen avulla. Se on sisällytettävä HTTP-otsikkona Dataversen verkkopyyntöön. Sovittimen on saatava tunnus vuokraaja B:n Azure AD -esiintymästä. (Katso 1. Hae tunnus kaaviossa.) Azure AD toimii tunnistetietojen toimittajana todennustyönkulussa.

Sovitin tunnistautuu antamalla sen sovellustunnisteen (muu kuin salainen koodi, joka on rekisteröity Azure AD:n vuokraajassa A) ja sovelluksen salaisen koodin tai sertifikaatin, joka vain sovittimen sovelluksella on.

Kun käyttäjä tai sovellus on tunnistettu ja voi tehdä kutsuja Dataversessa, tehdään Dataversen tason valtuutustarkistukset jokaiselle pyynnölle. Näiden tarkistusten avulla varmistetaan, että kutsujalla (sovittimen sovelluksen tunnistetiedoilla, jotka määritetään kaaviossa arvolla \<guid A\>), on oikeat sovelluksen käyttöoikeudet. Sovellustason valtuutusta hallitsee Dataversessa sovelluksen käyttäjä, joka vastaa sovittimen sovellustunnusta. Sovellustason käyttöoikeuksia hallitaan myöntämällä tiettyjen Dataversen määrittämien sovellusroolien käyttöoikeus. Näillä rooleilla on sovelluksen hajautetut oikeudet.

Lisätietoja on kohdassa [Usean vuokraajan palvelimien välisen todennuksen käyttäminen](/power-apps/developer/data-platform/use-multi-tenant-server-server-authentication).

Jos Dataverse-tason sovelluksen käyttöoikeuksien tarkistukset on suoritettu hyväksytyksi, virtuaalientiteetin laajennus tekee kutsun virtuaalientiteettipalvelimen päätepisteeseen Finance- tai Human Resources -ympäristössä. Palvelimelta palvelimelle (S2S) -todennusta käytetään tämän kutsun tekemisessä. Siinä käytetään tunnistetietoja ja salaista koodia, jotka on määritetty Finance and Operationsin virtuaalisen tietolähteen määritystietueessa.

![Finance and Operationsin virtuaalisen tietolähteen määritystietue eristysympäristössä.](./media/sandbox.jpg)

Lisätietoja on kohdassa [Dataversen virtuaaliyksikköjen määrittäminen](/dev-itpro/power-platform/admin-reference).

Dataversen virtuaalientiteetin laajennuksen kutsu Financeen tai Human Resourcesiin sisältää sovittimen tunnistetiedot alkuperäisestä kutsusta Dataverseen sovittimesta (tunnistetiedot, jotka on määritetty arvoksi \<guid A\> arkkitehtuurikaaviossa). Jos virtuaalientiteetin tietolähde on oikein määritetty ja S2S-todennustarkistukset on tehty hyväksytysti, virtuaalientiteettipalvelu Financessa tai Human Resourcesissa suorittaa kyselyn alkuperäisen kutsujan kontekstissa (sovitin \<guid A\>). Financen tai Human Resourcesin tasolla suoritettavat sovelluksen käyttöoikeustarkistukset tehdään, jotta varmistetaan sovittimen oikeuksien olevat vaaditut kyselyssä pyydettyjen tietoyksiköiden käyttöä varten.

Financen ja Human Resourcesin suojausta hallitaan seuraavilla tavoilla:

1. Yhdistämällä sovittimen tunnistetiedot (\<guid A\>) tiettyyn Finance- tai Human Resources -käyttäjään. Tämä yhdistäminen tehdään **Azure Active Directory -sovellukset** -sivulla. Lisätietoja on kohdassa [Ulkoisen sovelluksen rekisteröiminen](/dev-itpro/data-entities/services-home-page.md#register-your-external-application).
2. Myöntämällä Financen tai Human Resourcesin käyttäjälle soveltuvat sovellustason roolit, velvollisuudet ja oikeudet. Lisätietoja on kohdassa [Rooliin perustuva suojaus](/dev-itpro/sysadmin/role-based-security).

Jos sovittimen sovellukselle (\<guid A\>) myönnetään oikeudet, jotka vaaditaan pyydettyjen tietojen käyttöä varten, tapahtuu seuraavaa:

1. Kysely suoritetaan.
2. Tiedot käännetään takaisin Dataversen entiteettisivulle.
3. Tiedot palautetaan sovittimeen.

> [!IMPORTANT]
> Kehityksen aikana sovittimen voi suorittaa Financen tai Human Resourcesin käyttäjä, jolla on järjestelmänvalvojan rooli. Tuotantoympäristössä sovitinta ei kuitenkaan koskaan tule suorittaa järjestelmänvalvojan oikeuksiin.

## <a name="key-takeaways"></a>Pääkohdat

Seuraavaksi esitellään joitakin virtuaalitaulukon tai entiteetin arkkitehtuurin tärkeitä vaikutuksia:

- Virtuaalitaulukoiden suojausmääritystä, jota Human Resources tukee, hallitaan Human Resourcesissa.
- Asiakas ("Yhteinen asiakas" tämän artikkelin aiemmassa arkkitehtuurikaaviossa) voi hallita täysin sitä, mitä oikeuksia integroitavan sovittimen tunnistetiedoille (määritetty arvolla \<guid A\> kaaviossa) myönnetään.
- Asiakas on vastuussa Human Resources -ympäristön oikeasta suojausmäärityksestä. Sovittimen luovan integroitavan kumppanin on määritettävä sovittimen vaativia oikeuksia koskevat ohjeet.
