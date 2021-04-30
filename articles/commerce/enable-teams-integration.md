---
title: Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön
description: Tässä aiheessa kuvataan, kuinka otetaan käyttöön Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integrointi.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c4d596f27ffe15a97dc04e2ce7e85d21f8e7161f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908392"
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

1. Noudata artikkelin [Pika-aloitus: Sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristöön](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) ohjeita rekisteröidäksesi Teams-sovelluksen vuokraajasi kautta Azure-portaalissa.
1. Kopioi rekisteröidyn sovelluksen **Sovelluksen (asiakasohjelman) tunnus** -arvo **Yhteenveto**-sivulta. Tämän arvon avulla voit ottaa Teams-integroinnin käyttöön Commerce headquarters -sovelluksessa.
1. Kopioi varmenteen arvo, joka on annettu, kun olet [lisännyt varmenteen](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) vaiheessa 1. Varmenne tunnetaan myös julkisena avaimena tai sovellusavaimena. Tämän arvon avulla voit ottaa Teams-integroinnin käyttöön Commerce headquarters -sovelluksessa.

Voit ottaa Teams-integroinnin käyttöön Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Microsoft Teams -integrointimääritys**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Määritä **Ota Microsoft Teams -integrointi käyttöön** -asetukseksi **Kyllä**.
1. Kirjoita **Sovellustunnus**- ja **Sovellusavain**-kenttiin arvot, jotka sait rekisteröidessäsi Teams-sovelluksen Azure-portaalissa.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa on esimerkki Teams-integroinnin konfiguroinnista Commerce headquartersissa.

![Teams-integroinnin konfiguraatio Commerce headquarters -sovelluksessa](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

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
