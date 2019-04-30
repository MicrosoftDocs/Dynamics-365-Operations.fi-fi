---
title: Laajenna Talent käyttämällä PowerApps- ja Microsoft Flow -esimerkkejä
description: Tässä ohjeaiheessa käsitellään Microsoft PowerAppsia ja Microsoft Flow'ta käyttäviä Microsoft Dynamics 365 for Talentin laajennusesimerkkejä.
author: negudava
manager: Annbe
ms.date: 03/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 0aa3578047b9397682a7039d0dbcc05cc1b167e4
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/12/2019
ms.locfileid: "949917"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a>Laajenna Talent käyttämällä PowerApps- ja Microsoft Flow -esimerkkejä

Tässä ohjeaiheessa käsitellään Microsoft PowerAppsia ja Microsoft Flow'ta käyttäviä Microsoft Dynamics 365 for Talentin laajennusesimerkkejä. Voit tuoda kumpaankin esimerkkiin liitetyt ratkaisupaketin PowerApps-ympäristöön. Voit sitten käyttää paketteja joka ohjeena tai lähtökohtana, jonka avulla toteutat organisaatioon sopivia skenaarioita.

> [!IMPORTANT]
> Jos haluat käyttää tässä ohjeaiheessa kuvattuja malleja ja sovellusta sellaisenaan, varmista testaamalla, että ne kattavat kaikki toteutukseen kuuluvat skenaariot.


## <a name="prerequisites"></a>Edellytykset

- Pakettien tuontia varten käyttäjät tarvitsevat **Ympäristön tekijä** -käyttöoikeuden.
- Sovellusten vientiä ja tuontia varten käyttäjillä on oltava PowerApps-palvelupaketin käyttöoikeus tai PowerApps -palvelupaketin 2 kokeiluversion käyttöoikeus.

## <a name="flow--form-connect"></a>Työnkulku – lomakeyhteys

**Työnkulku – lomakeyhteys** -mallin avulla voi lukea tietoja Microsoft Formsista ja tallentaa ne Common Data Service -yksikköön.

Mallia voidaan laajentaa siten, että sitä voidaan käyttää muissa skenaarioissa. Seuraavassa on muutamia esimerkkejä:

- Ehdokasarviointien taltiointi.
- Kurssin kyselylomakkeiden tulosten taltiointi.
- Haastattelukysymyskirjaston kokoaminen henkilöstöhallinnon järjestelmänvalvojille.
- Ehdokkaan haastatteluprosessin arvioinnin taltiointi.

Lomakkeet voivat näkyä Microsoft Dynamics 365: Attractissa ehdokasportaalissa ja ehdokkaat voit täyttää tiedot. Lomakkeet voidaan myös upottaa tehtävinä työmalliin.

Kun ehdokas lähettää lomakkeen, Microsoft Flow taltioi lomakkeen lähetyksen, lukee tiedot ja tallentaa sen Common Data Service -yksikköön.

Voit ladata **Työnkulku – lomakeyhteys** -mallin ja mukautetun yksikkörakenteen siirtymällä Microsoft Download Centerissä kohtaan [Työnkulku – lomakeyhteys](https://go.microsoft.com/fwlink/?linkid=2081988).

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a>Powerappsiin välitettyjen parametrien aloittaminen ja purkaminen

**Powerappsiin välitettyjen parametrien aloittaminen ja purkaminen** -mallia voidaan käyttää minkä tahansa Attractin PowerApps-skenaarion aloituskohtana. Se sisältää kaikki Attractin välittämät oletusparametrit, kuten **Työhakemus**, **Ehdokkaan tunnus** ja **Työn tunnus**.

Tällä mallilla voi hakea ehdokkaan arviointilomakkeen, jotta työhön ottava esimies voi tarkastella ehdokkaan täyttämää arviointia.

PowerAppsilla luodut sovellukset voidaan upottaa työmalliin Attractissa.

Voit ladata **Powerappsiin välitettyjen parametrien aloittaminen ja purkaminen** -mallin ja mukautetun yksikkörakenteen Microsoft Download Centerin kohdassa [Powerappsiin välitettyjen parametrien aloittaminen ja purkaminen](https://go.microsoft.com/fwlink/?linkid=2081991).

## <a name="integration-with-office-365"></a>Integrointi Office 365:n kanssa

**Office 365 -integrointi** -sovelluksella voi purkaa kirjautuneiden käyttäjien tiimitiedot Microsoft Office 365:stä. Se hakee työntekijäviitteet Talentissa ja purkaa saapumis- ja poistumisaikatiedot sekä poikkeustallenteet. Saapumis- ja poistumisaikatiedot tallennetaan mukautettuihin Common Data Service -yksiköihin. Oletuksen on, että ulkopuoliset järjestelmät täyttävät nämä tiedot integroinnin kautta.

Sovellusta voidaan laajentaa siten, että sitä voidaan käyttää muissa skenaarioissa. Sitä voidaan käyttää esimerkiksi näyttämään ryhmän lomatiedot, kalenteritapahtumat ja kaikki ryhmäkohtaiset tapahtumat.

Voit ladata **Office 365 -integrointi** -sovelluksen ja mukautetun yksikkörakenteen Microsoft Download Centerin kohdassa [Office 365 -integrointi](https://go.microsoft.com/fwlink/?linkid=2081787).

## <a name="flow--email-notification"></a>Työnkulku – sähköposti-ilmoitus

**Työnkulku – sähköposti-ilmoitus** -mallia voi käyttää sähköposti-ilmoitusskenaarioissa. Sen avulla voidaan käynnistää sähköposti-ilmoitukset niille ehdokkaille, jotka työhönottoryhmä hylkää rekrytointiprosessin jossain vaiheessa.

Tämä malli voidaan laajentaa seuraamaan ehdokasvaiheen muutoksia koko rekrytointiprosessin ajan sekä lähettämään ilmoitukset työhönottoryhmälle ja ehdokkaalle.

Yleisesti ottaen työnkulut voidaan määrittää lähettämään Common Data Serviceen tallennettuihin yksiköihin ilmoitukset Core HR:n, Attractin tai Dynamics 365 Talent: Onboardin tapahtumista.

Voit ladata **Työnkulku – sähköposti-ilmoitus** mallin Microsoft Download Centerin kohdassa [Työnkulku – sähköposti-ilmoitus](https://go.microsoft.com/fwlink/?linkid=2082103).

## <a name="flow--sql-connect-and-execute"></a>Työnkulku – SQL-yhteys ja toteutus

**Työnkulku – SQL-yhteys ja toteutus** -malli muodostaa yhteyden Microsoft SQL Serveriin ja mahdollistaa SQL-kyselyjen suorittamisen.

Vaikka tämä malli on suunniteltu lukemaan ja päivittämään SQL-taulukkoja, se voidaan laajentaa muissa skenaarioissa käytettäväksi. Sen avulla voidaan esimerkiksi täyttää valmistelutaulu Common Data Servicessä SQL Serverin tietueilla sekä synkronoida valmistelutaulu säännöllisesti käyttämällä SQL Serverin lisäävää työntöä.

Voit ladata **Työnkulku – SQL-yhteys ja toteutus** -mallin Microsoft Download Centerin kohdassa [Työnkulku – SQL-yhteys ja toteutus](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="flow--sharepoint-integration"></a>Työnkulku – SharePoint-integrointi

**Työnkulku – SharePoint-integrointi** -mallin avulla voi lukea tietoja Microsoft SharePoint -luettelosta, verrata luetteloa Common Data Service -yksikön kenttien arvoihin ja lähettää vertailun tulokset ilmoitussähköpostina. 

Organisaatio voi tarvita pikaisesti tiettyjä osaamisalueita. Nämä osaamisalueet voidaan tallentaa SharePointiin SharePoint-luettelona. Jos ehdokas hakee työtä, jossa on mainittu tarvittava osaamisaluejoukko, ja jos ehdokkaan osaamisalue ja SharePointiin tallennetut osaamisalueet vastaavat hyvin toisiaan, ilmoitussähköposti lähetetään. Tällä tavoin kiireellisesti täytettävä toimet voidaan täyttää nopeammin, sillä ilmoitukset auttavat työhönottajia tavoittelemaan ja palkkaamaan ehdokkaita koko organisaatiossa.

Tämä malli voidaan laajentaa käytettäväksi missä tahansa SharePoint-integraation sisältävässä skenaariossa.

Voit ladata **Työnkulku – SharePoint-integrointi** -mallin Microsoft Download Centerin kohdassa [Työnkulku – SharePoint-integrointi](https://go.microsoft.com/fwlink/?linkid=2082109).



## <a name="additional-resources"></a>Lisäresurssit

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Sovelluksen siirtäminen vuokraajien ja ympäristöjen kesken](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
