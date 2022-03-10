---
title: Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön
description: Tässä aiheessa kuvataan, kuinka otetaan käyttöön Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integrointi.
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 52b1a889a15cfe2e6e104e38b7d257f80762954f
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323427"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön

[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan, kuinka otetaan käyttöön Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integrointi.

Jotta Teams voidaan valmistella Dynamics 365 Commercen tiedoilla ja Teams-sovelluksen ja myyntipisteen välinen tehtävänhallinta voidaan synkronoida, integrointitoiminnot on otettava käyttöön Commerce headquartersissa.

> [!NOTE]
> Kun otat Teams-integroinnin käyttöön, suostut jakamaan tietosi Teamsin kanssa. Teamsin kanssa jaetut tiedot saattavat olla eri maassa kuin Commerce-tiedot, ja ne saattavat olla erilaisten yhteensopivuusvaatimusten mukaisia. Lisätietoja: [Microsoft Trust Center](https://www.microsoft.com/trust-center). Lisätietoja Microsoftin tietosuojakäytännöistä: [Microsoftin tietosuojalauseke](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Ota Teams-integraatio käyttöön

Ennen kuin voit ottaa Microsoft Teamsin ja Commercen integroinnin käyttöön, Teams-sovellus on rekisteröitävä vuokraajaa käyttäen Azure-portaalissa.

Noudattamalla seuraavia ohjeita voit rekisteröidä Teams-sovelluksen vuokraajaasi käyttäen Azure-portaalissa.

1. Noudata artikkelin [Pika-aloitus: Sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristöön](/azure/active-directory/develop/quickstart-register-app) ohjeita rekisteröidäksesi Teams-sovelluksen vuokraajasi kautta Azure-portaalissa.
1. Valitse **Sovelluksen rekisteröinti** -välilehdessä edellisessä vaiheessa luotu sovellus. Valitse sitten **Todennus**-välilehdessä **Lisää ympäristö**.
1. Valitse valintaikkunassa **Verkko**. Syötä sitten **Uudelleenohjauksen URL-osoitteet** -kenttään URL-osoite muodossa **\<HQUrl\>/oauth**. Korvaa **\<HQUrl\>** Commerce headquarters -sovelluksen URL-osoitteella (kuten `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`).
1. Kopioi rekisteröidyn sovelluksen **Yhteenveto**-sivulta arvo **Sovellustunnus (asiakas)**. Sinun on annettava tämä arvo ottaaksesi Teams-integroinnin käyttöön Commerce headquarters -sovelluksessa seuraavassa osassa.
1. Lisää asiakasohjelman salasana seuraamalla kohdan [Lisää asiakasohjelman salasana](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) -ohjeiden mukaisesti. Kopioi sitten asiakasohjelman **Salasanan arvo**. Sinun on annettava tämä arvo ottaaksesi Teams-integroinnin käyttöön Commerce headquarters -sovelluksessa seuraavassa osassa.
1. Valitse **API-käyttöoikeudet** ja sitten **Lisää käyttöoikeus**.
1. Valitse **Pyydä API-käyttöoikeuksia** -valintaikkunassa **Microsoft Graph** ja sitten **Delegoidut käyttöoikeudet**, laajenna **Ryhmä**, valitse **Group.ReadWrite.All** ja lopuksi **Lisää käyttöoikeudet**.
1. Valitse **Pyydä API-käyttöoikeuksia** -valintaikkunassa **Lisää käyttöoikeus**, sitten **Microsoft Graph** ja sitten **Sovelluksen käyttöoikeudet**, laajenna **Ryhmä**, valitse **Group.ReadWrite.All** ja lopuksi **Lisää käyttöoikeudet**.
1. Valitse **Pyydä API-käyttöoikeuksia** -valintaikkunassa **Lisää käyttöoikeus**. Tee **Organisaationi käyttämät API:t** -välilehdessä haku **Microsoft Teams Retail -palvelu** ja valitse se.
1. Valitse **Delegoidut käyttöoikeudet**, laajenna **TaskPublishing**, valitse **TaskPublising.ReadWrite.All** ja valitse sitten **Lisää käyttöoikeudet**. Lisätietoja: [Asiakassovelluksen määrittäminen käyttämään verkko-API:a](/azure/active-directory/develop/quickstart-configure-app-access-web-apis).

Voit ottaa Teams-integroinnin käyttöön Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Microsoft Teams -integrointimääritys**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Määritä **Ota Microsoft Teams -integrointi käyttöön** -asetukseksi **Kyllä**.
1. Kirjoita **Sovellustunnus**- ja **Sovellustunnus (asiakas)** -kenttiin arvo, jonka sait rekisteröidessäsi Teams-sovelluksen Azure-portaalissa.
1. Kirjoita **Sovellusavain**- ja **Salasanan arvo** -kenttiin arvo, jonka sait lisätessäsi asiakkaan salasanan Azure-portaalissa.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa on esimerkki Teams-integroinnin konfiguroinnista Commerce headquartersissa.

![Teams-integroinnin konfiguraatio Commerce headquarters -sovelluksessa.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Ota Teams-integraatio pois käytöstä

Voit ottaa Microsoft Teams -integroinnin pois käytöstä Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Microsoft Teams -integrointimääritys**.
1. Valitse toimintoruudussa **Muokkaa**.
3. Määritä **Ota Microsoft Teams -integrointi käyttöön** -asetukseksi **Ei**.
4. Tyhjennä arvot **Sovellustunnus**- ja **Sovellusavain**-kentistä.
1. Valitse toimintoruudussa **Tallenna**.

> [!NOTE]
> Kun olet poistanut Commercen Teams-integroinnin käytöstä, myyntipistepäätteet eivät enää näytä Teams-sovelluksella julkaistuja tehtäviä.

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus](commerce-teams-integration.md)

[Microsoft Teamsin valmistelu Dynamics 365 Commercesta](provision-teams-from-commerce.md)

[Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä](synchronize-tasks-teams-pos.md)

[Käyttäjäroolien hallinta Microsoft Teamsissa](manage-user-roles-teams.md)

[Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä](map-stores-existing-teams.md)

[Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset](teams-integration-faq.md)
