---
title: Attractin laajennettavuus
description: "Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talent - Attract -sovelluksen laajentamista Microsoft Power Platformin avulla."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 0af60a0aea0f7a5de793631445aaebb37dbb0d74
ms.contentlocale: fi-fi
ms.lasthandoff: 10/22/2018

---

# <a name="extensibility-in-attract"></a>Attractin laajennettavuus

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talentin pohjana on Common Data Service (CDS) sovelluksille -ympäristö, ja sitä voidaan laajentaa eri tavoin Microsoft Power Platformin ja Common Data Service sovelluksille -ratkaisun toimintojen avulla. Niinpä voit määrittää ja mukauttaa järjestelmää Microsoft PowerAppsin ja Microsoft Flow'n avulla. Saat lisää analyysitietoja henkilöistä Microsoft Power BI:n avulla. Lisäksi uudet mukautetut tehtävät, kuten PowerApps- ja verkkosisältö (iframe) -tehtävät, auttavat mukauttamaan työhönottoprosessia entisestään. Voit muokata työhönottoprosessia näiden tehtävien avulla liiketoiminnan tarpeita ja prosesseja vastaaviksi. Voit myös varmistaa, että sekä työhönottoryhmällä että hakijoilla on saumaton ja mukautettu kokemus.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Microsoft Power Platformin hyödyntäminen 

Koska kaikki Attractin tiedot ovat Common Data Service sovelluksille -ratkaisussa, voit sisällyttää omat liiketoimintatarpeet Attractiin Microsoft Power Platformin työkaluilla.

### <a name="powerapps"></a>PowerApps

Voit luoda PowerAppsin avulla helposti sovelluksia, jotka yhdistävät Attractin tiedot ja joissa logiikka lisätään käyttämällä Microsoft Excelin lausekkeiden kaltaisia lausekkeita. PowerAppsin avulla muodostettuja sovelluksia voidaan käyttää verkossa sekä Apple iOS- ja Google Android -laitteissa.

Voit esimerkiksi helpottaa työhönottajien toimintaa yliopistojen urapäivillä muodostamalla kevyen sovelluksen, jolla he voivat skannata ansioluetteloita ja syöttää työpaikkojen hakijat Attractissa. Vaihtoehtoisesti voit muodostaa sovelluksen, joka auttaa noudattamaan organisaation vaatimustenmukaisuustarpeita. Lisätietoja PowerAppsin ja sovellusten muodostamisesta sen avulla on kohdassa [Tietojen integrointi Common Data Service sovelluksille -ratkaisuun](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Voit luoda Microsoft Flow'n avulla automatisoituja työnkulkuja, joita käytetään Attract-tietojen ohella. Voit yhdistää kätevästi satoja suosittuja sovelluksia ja palveluja koodia kirjoittamatta. Kun muodostat työnkulkuja, jotka toimivat Attractin työ-, hakija- ja hakemusyksiköiden kanssa Common Data Service sovelluksille -ratkaisussa, voit automatisoida useita toimintoja. Esimerkki: kun hakija hyväksyy tarjouksen, perehdytysryhmälle voidaan lähettää ilmoitus tai uutiset voidaan ilmoittaa Twitterissä. Lisätietoja työnkuluista on [Microsoft Flow'n ohjeistuksessa](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

Voit muodostaa ja tarkastella Power BI:n avulla mukautettuja raportteja ja koontinäyttöjä, joilla saat monipuolisen käsityksen Attractin tiedoista. Lisätietoja Power BI:sta ja vuorovaikutteisten raporttien ja koontinäyttöjen muodostamisesta on kohdassa [Power BI:n ohjeistus](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Mukautetut tehtävät 

Voit lisätä mukautettuja tehtäviä, kuten PowerApps-sovelluksia ja verkkosisällön (iframe) tehtäviä, työn prosessimallitasolla tai uuden työn luonnin aikana. Voit mukauttaa työhönottoprosessia näiden tehtävien avulla ja tuoda organisaation oman liiketoimintalogiikan Attractiin.

#### <a name="powerapps-activity"></a>PowerApps-tehtävä 

PowerApps-tehtävän avulla työn tai työn prosessimallin luoja voi upottaa PowerApps-sovelluksen työhönoton työnkulkuun. Kun olet luonut ja julkaissut sovelluksen, voit lisätä sen sovellustunnuksen tehtävämäärityksissä. Voit lukea ja kirjoittaa PowerApps-sovelluksen avulla tietoja Common Data Service sovelluksille -ratkaisuun. Voit myös linkittää sovelluksen työnkulkuun. Esimerkki: Sinulla on sovellus, jolla työhönottajat täyttävät lomakkeen puhelinhaastattelujen aikana. Voit tässä tapauksessa linkittää sovelluksen työnkulkuun, joka arvioi, voidaanko hakija siirtää eteenpäin työhakuprosessissa. Vain työhönottoryhmän jäsenet voivat tarkastella tämän tyyppistä tehtävää. Lisätietoja PowerApps-tehtävän määrittämisestä on kohdassa [Attractin tehtävät](./activities-attract.md).

> [!NOTE]
> PowerApps-tehtävää voi käyttää vain kattavan työhönottolaajennuksen kanssa.

#### <a name="web-content-iframe-activity"></a>Internet-sisältö (iframe) -tehtävä

Internet-sisältö (iframe) -tehtävän avulla voi upottaa työhönottoprosessiin tai hakijaportaaliin muodostetun mukautetun verkkoratkaisun. Voit lukea tietoja suoraan Common Data Service sovelluksille -ratkaisusta ja kirjoittaa niitä siihen. Voit myös mukauttaa ratkaisun niin, että se käynnistää työnkulkuja tai hyödyntää Microsoft Azure -toimintoja. Lisätietoja Internet-sisältötehtävän määrittämisestä on kohdassa [Attractin tehtävät](./activities-attract.md).

> [!NOTE]
> Internet-sisältö-tehtävää voi käyttää vain kattavan työhönottolaajennuksen kanssa.

