---
title: Talentin laajentaminen Power Appsin ja Power Automaten avulla
description: Tässä ohjeaiheessa käsitellään Microsoft Power Appsia ja Microsoft Power Automatea käyttäviä Microsoft Dynamics 365 Talentin laajennusesimerkkejä.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 3bb61297e294aa3f2d06f542bebe29d7afae9c3b
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832835"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Talentin laajentaminen Power Appsin ja Power Automaten avulla

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Power Appsia ja Microsoft Power Automatea käyttäviä Microsoft Dynamics 365 Talentin laajennusesimerkkejä. Voit tuoda kumpaankin esimerkkiin liitetyt ratkaisupaketin Power Apps-ympäristöön. Voit sitten käyttää paketteja joka ohjeena tai lähtökohtana, jonka avulla toteutat organisaatioon sopivia skenaarioita.

> [!IMPORTANT]
> Jos haluat käyttää tässä ohjeaiheessa kuvattuja malleja ja sovellusta sellaisenaan, varmista testaamalla, että ne kattavat kaikki toteutukseen kuuluvat skenaariot.


## <a name="prerequisites"></a>Edellytykset

- Pakettien tuontia varten käyttäjät tarvitsevat **Ympäristön tekijä** -käyttöoikeuden.
- Sovellusten vientiä ja tuontia varten käyttäjillä on oltava Power Apps-palvelupaketin 2 käyttöoikeus tai Power Apps -palvelupaketin 2 kokeiluversion käyttöoikeus.

## <a name="power-automate--form-connect"></a>Power Automate – lomakeyhteys

**Power Automate – lomakeyhteys** -mallin avulla voi lukea tietoja Microsoft Formsista ja tallentaa ne Common Data Service -yksikköön.

Mallia voidaan laajentaa siten, että sitä voidaan käyttää muissa skenaarioissa. Seuraavassa on muutamia esimerkkejä:

- Ehdokasarviointien taltiointi.
- Kurssin kyselylomakkeiden tulosten taltiointi.
- Haastattelukysymyskirjaston kokoaminen henkilöstöhallinnon järjestelmänvalvojille.
- Ehdokkaan haastatteluprosessin arvioinnin taltiointi.

Lomakkeet voivat näkyä Microsoft Dynamics 365: Attractissa ehdokasportaalissa ja ehdokkaat voit täyttää tiedot. Lomakkeet voidaan myös upottaa tehtävinä työmalliin.

Kun ehdokas lähettää lomakkeen, Microsoft Power Automate taltioi lomakkeen lähetyksen, lukee tiedot ja tallentaa sen Common Data Service -yksikköön.

Voit ladata **Power Automate – lomakeyhteys** -mallin ja mukautetun yksikkörakenteen siirtymällä Microsoft Download Centerissä kohtaan [Power Automate – lomakeyhteys](https://go.microsoft.com/fwlink/?linkid=2081988).

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a>Power Appsiin välitettyjen parametrien aloittaminen ja purkaminen

**Power Appsiin välitettyjen parametrien aloittaminen ja purkaminen** -mallia voidaan käyttää minkä tahansa Attractin Power Apps -skenaarion aloituskohtana. Se sisältää kaikki Attractin välittämät oletusparametrit, kuten **Työhakemus**, **Ehdokkaan tunnus** ja **Työn tunnus**.

Tällä mallilla voi hakea ehdokkaan arviointilomakkeen, jotta työhön ottava esimies voi tarkastella ehdokkaan täyttämää arviointia.

Power Appsilla luodut sovellukset voidaan upottaa työmalliin Attractissa.

Voit ladata **Power Appsiin välitettyjen parametrien aloittaminen ja purkaminen** -mallin ja mukautetun yksikkörakenteen Microsoft Download Centerin kohdassa [Power Appsiin välitettyjen parametrien aloittaminen ja purkaminen](https://go.microsoft.com/fwlink/?linkid=2081991).

## <a name="integration-with-office-365"></a>Integrointi Office 365:n kanssa

**Office 365 -integrointi** -sovelluksella voi purkaa kirjautuneiden käyttäjien tiimitiedot Microsoft Office 365:stä. Se hakee työntekijäviitteet Talentissa ja purkaa saapumis- ja poistumisaikatiedot sekä poikkeustallenteet. Saapumis- ja poistumisaikatiedot tallennetaan mukautettuihin Common Data Service -yksiköihin. Oletuksen on, että ulkopuoliset järjestelmät täyttävät nämä tiedot integroinnin kautta.

Sovellusta voidaan laajentaa siten, että sitä voidaan käyttää muissa skenaarioissa. Sitä voidaan käyttää esimerkiksi näyttämään ryhmän lomatiedot, kalenteritapahtumat ja kaikki ryhmäkohtaiset tapahtumat.

Voit ladata **Office 365 -integrointi** -sovelluksen ja mukautetun yksikkörakenteen Microsoft Download Centerin kohdassa [Office 365 -integrointi](https://go.microsoft.com/fwlink/?linkid=2081787).

## <a name="power-automate--email-notification"></a>Power Automate – sähköposti-ilmoitus

**Power Automate – sähköposti-ilmoitus** -mallia voi käyttää sähköposti-ilmoitusskenaarioissa. Sen avulla voidaan käynnistää sähköposti-ilmoitukset niille ehdokkaille, jotka työhönottoryhmä hylkää rekrytointiprosessin jossain vaiheessa.

Tämä malli voidaan laajentaa seuraamaan ehdokasvaiheen muutoksia koko rekrytointiprosessin ajan sekä lähettämään ilmoitukset työhönottoryhmälle ja ehdokkaalle.

Yleisesti ottaen työnkulut voidaan määrittää lähettämään Common Data Serviceen tallennettuihin yksiköihin ilmoitukset Core HR:n, Attractin tai Onboardin tapahtumista.

Voit ladata **Power Automate – sähköposti-ilmoitus** -mallin Microsoft Download Centerin kohdassa [Power Automate – sähköposti-ilmoitus](https://go.microsoft.com/fwlink/?linkid=2082103).

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL-yhteys ja toteutus

**Power Automate – SQL-yhteys ja toteutus** -malli muodostaa yhteyden Microsoft SQL Serveriin ja mahdollistaa SQL-kyselyjen suorittamisen.

Vaikka tämä malli on suunniteltu lukemaan ja päivittämään SQL-taulukkoja, se voidaan laajentaa muissa skenaarioissa käytettäväksi. Sen avulla voidaan esimerkiksi täyttää valmistelutaulu Common Data Servicessä SQL Serverin tietueilla sekä synkronoida valmistelutaulu säännöllisesti käyttämällä SQL Serverin lisäävää työntöä.

Voit ladata **Power Automate – SQL-yhteys ja toteutus** -mallin Microsoft Download Centerin kohdassa [Power Automate – SQL-yhteys ja toteutus](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePoint -integraatio

**Power Automate – SharePoint-integrointi** -mallin avulla voi lukea tietoja Microsoft SharePoint -luettelosta, verrata luetteloa Common Data Service -yksikön kenttien arvoihin ja lähettää vertailun tulokset ilmoitussähköpostina. 

Organisaatio voi tarvita pikaisesti tiettyjä osaamisalueita. Nämä osaamisalueet voidaan tallentaa SharePointiin SharePoint-luettelona. Jos ehdokas hakee työtä, jossa on mainittu tarvittava osaamisaluejoukko, ja jos ehdokkaan osaamisalue ja SharePointiin tallennetut osaamisalueet vastaavat hyvin toisiaan, ilmoitussähköposti lähetetään. Tällä tavoin kiireellisesti täytettävä toimet voidaan täyttää nopeammin, sillä ilmoitukset auttavat työhönottajia tavoittelemaan ja palkkaamaan ehdokkaita koko organisaatiossa.

Tämä malli voidaan laajentaa käytettäväksi missä tahansa SharePoint-integraation sisältävässä skenaariossa.

Voit ladata **Power Automate – SharePoint-integrointi** -mallin Microsoft Download Centerin kohdassa [Power Automate – SharePoint-integrointi](https://go.microsoft.com/fwlink/?linkid=2082109).

## <a name="referral-app"></a>Suositussovellus
Voit lisätä ehdokkaita jaettuun kykypooliin suositussovelluksella. Suosittelija voi antaa **etunimen**, **sukunimen**, **sähköpostin** ja **Linkedlnin URL-osoitteen**, kun ehdokas lähetetään. Ehdokkaan lähteen metatiedot täytetään sitten suosittelijan tiedoilla.

Voit upottaa tämän sovelluksen työntekijän itsepalveluun suositusten lähettämistä varten tai voit käyttää sitä linkkinä yritysportaalissa ja suorittaa sen itsenäisenä sovelluksena.

Lataa **suositussovellus** siirtymällä [Dynamics 365 Talent -laajennusratkaisu: suositussovellukseen](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) Microsoft Download Centerissä. Voit tuoda tämän sovelluksen ja mukauttaa sen lisäämään lisätoimintoja.

## <a name="additional-resources"></a>Lisäresurssit

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Sovelluksen siirtäminen vuokraajien ja ympäristöjen kesken](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
