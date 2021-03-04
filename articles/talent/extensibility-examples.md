---
title: Talentin laajentaminen Power Appsin ja Power Automaten avulla
description: Tässä artikkelissa käsitellään Microsoft Power Appsia ja Microsoft Power Automatea käyttäviä Microsoft Dynamics 365 Talent ‑ Attractin laajennusesimerkkejä.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529631"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Talentin laajentaminen Power Appsin ja Power Automaten avulla

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä artikkelissa käsitellään Microsoft Power Appsia ja Microsoft Power Automatea käyttäviä Microsoft Dynamics 365 Talent: Attractin laajennusesimerkkejä. Voit tuoda kumpaankin esimerkkiin liitetyt ratkaisupaketin Power Apps-ympäristöön. Voit sitten käyttää paketteja joka ohjeena tai lähtökohtana, jonka avulla toteutat organisaatioon sopivia skenaarioita.

> [!IMPORTANT]
> Jos haluat käyttää tässä artikkelissa kuvattuja malleja ja sovellusta sellaisenaan, varmista testaamalla, että ne kattavat kaikki toteutukseen kuuluvat skenaariot.


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

Microsoft Dynamics 365: Attractissa voit käyttää lomakkeita ehdokasportaalissa, jossa ehdokkaat täyttävät tiedot. Lomakkeet voidaan myös upottaa tehtävinä työmalliin.

Kun ehdokas lähettää lomakkeen, Microsoft Power Automate taltioi lomakkeen lähetyksen, lukee tiedot ja tallentaa sen Common Data Service -yksikköön.

Voit ladata **Power Automate – lomakeyhteys** -mallin ja mukautetun yksikkörakenteen siirtymällä Microsoft Download Centerissä kohtaan [Power Automate – lomakeyhteys](https://go.microsoft.com/fwlink/?linkid=2081988).

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePoint -integraatio

**Power Automate – SharePoint-integrointi** -mallin avulla voi lukea tietoja Microsoft SharePoint -luettelosta, verrata luetteloa Common Data Service -yksikön kenttien arvoihin ja lähettää vertailun tulokset ilmoitussähköpostina. 

Organisaatio voi tarvita pikaisesti tiettyjä osaamisalueita. Nämä osaamisalueet voidaan tallentaa SharePointiin SharePoint-luettelona. Jos ehdokas hakee työtä, jossa on mainittu tarvittava osaamisaluejoukko, ja jos ehdokkaan osaamisalue ja SharePointiin tallennetut osaamisalueet vastaavat hyvin toisiaan, ilmoitussähköposti lähetetään. Tällä tavoin kiireellisesti täytettävä toimet voidaan täyttää nopeammin, sillä ilmoitukset auttavat työhönottajia palkkaamaan ehdokkaita koko organisaatiossa.

Tämä malli voidaan laajentaa käytettäväksi missä tahansa SharePoint-integraation sisältävässä skenaariossa.

Voit ladata **Power Automate – SharePoint-integrointi** -mallin Microsoft Download Centerin kohdassa [Power Automate – SharePoint-integrointi](https://go.microsoft.com/fwlink/?linkid=2082109).

## <a name="referral-app"></a>Suositussovellus

Voit lisätä ehdokkaita jaettuun kykypooliin suositussovelluksella. Suosittelija voi antaa **etunimen**, **sukunimen**, **sähköpostin** ja **LinkedInin URL-osoitteen**, kun ehdokas lähetetään. Ehdokkaan lähteen metatiedot täytetään sitten suosittelijan tiedoilla.

Voit upottaa tämän sovelluksen työntekijän itsepalveluun suositusten lähettämistä varten tai voit käyttää sitä linkkinä yritysportaalissa ja suorittaa sen itsenäisenä sovelluksena.

Lataa **suositussovellus** siirtymällä [Dynamics 365 Talent -laajennusratkaisu: suositussovellukseen](https://www.microsoft.com/download/details.aspx?id=58497) Microsoft Download Centerissä. Voit tuoda tämän sovelluksen ja mukauttaa sen lisäämään lisätoimintoja.

## <a name="additional-resources"></a>Lisäresurssit

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[Sovelluksen siirtäminen vuokraajien ja ympäristöjen kesken](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)


[!INCLUDE[footer-include](../includes/footer-banner.md)]