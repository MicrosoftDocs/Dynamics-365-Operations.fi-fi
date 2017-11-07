---
title: "Työntekijän kehityksen Power BI -sisältö"
description: "Tässä ohjeaiheessa käsitellään työntekijän kehityksen Power BI -sisältöä Siinä selitetään, miten sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä."
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 91f7071cc759686dd90b5893adaf58d1521e9185
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="employee-development-power-bi-content"></a>Työntekijän kehityksen Power BI -sisältö

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään **työntekijän kehityksen** Microsoft Power BI -sisältöä Siinä selitetään, miten sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttö

Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys, **työntekijän kehityksen** sisältöpaketti sijaitsee Microsoft Dynamics Lifecycle Servicesin (LCS) Jaettu omaisuus -kirjastossa. Lisätietoja sisältöpaketin lataamisesta ja sen yhdistämisestä tietoihin on ohjeaiheessa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Raportit, jotka sisältyvät Power BI -sisältöön
**Työntekijän kehityksen** Power BI -sisältöön sisältyvissä raporteissa on sekä kaavioita että taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                        | Sisältö |
|-------------------------------|----------|
| Työntekijöiden kehityksen yleiskatsaus | Muiden raporttien yhteenveto |
| Työntekijän osaamisanalyysi       | Työntekijän osaamistyypit ja työntekijän osaamisalueet tyypin mukaan |
| Työntekijän osaamistasoanalyysi | Työntekijän osaamistasot osaston mukaan, työntekijät osaamistason ja -tyypin mukaan sekä alhaisin ja korkein taso osaamisalueittain |
| Osaamisalueprofiili                 | Valitun työntekijän osaamisprofiili. |
| Osaamisanalyysi                | Osaamisalue tyypin ja luokituksen mukaan |
| Suorituskykyluokituksen analyysi   | Työntekijät alhaisimman ja korkeimman työkohtaisen luokituksen mukaan, työntekijäluokitukset osaston mukaan, työntekijät luokitus- ja toimityypin mukaan sekä korkein ja alhaisin luokitus toimen mukaan  |
| Työntekijän suorituskykyanalyysi | Valitun luokituksen työntekijäluokitukset esimiehen mukaan |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI -ohjelmassa löydät artikkelista [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
| Kokonaisuus                   | Sisältö                                                                                                   | Suhteet muihin yksiköihin |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalenterin vastakirjaus          | Kalenterin siirtymät raporttien osittamiseen                                                                          | Aiemmin määritetty toimi, toimitrendi, työntekijätrendi, poistettu työntekijä 
| Yritys                   | Yritykset, joiden mukaan raportit suodatetaan                                                                             | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Nykyinen toimi         | Paikat nykyiseen pvm:ään asti, täysiaikaista vastaavat, avoimet paikat ja avoimista täytetyiksi -paikat | Työ, toimi |
| Nykyinen työntekijä         | Työntekijät nykyisellä päivämäärällä, ikä ja henkilöstömäärä                                                         | Yritys, maantieteellinen sijainti, työntekijän nimi, raportoinnin kohde, työntekijän nimike, demografia, työ, työsuhde, toimi |
| Päivämäärä                     | Päiviä, viikkoja, kuukausia ja vuosia                                                                             | Aiemmin määritetty toimi, toimitrendi, poistettu työntekijä,. työntekijätrendi |
| Demografia             | Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty                                                   | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työsuhde               | Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä                                                                  | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Maantieteellinen sijainti      | Paikkakunta, lääni, postinumero ja osavaltio tai provinssi                                                           | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työ                      | Tehtävä, tyyppi ja nimike                                                                                  | Nykyinen sijainti, nykyinen työntekijä |
| Aiemmin määritetty toimi | Työtehtävän syy, aloituspvm, loppupvm ja työ                                                           | Kalenterin vastakirjaus, päivämäärä, työ, toimi |
| Sijainti                 | Osasto, FTE, toimi, toimen tyyppi ja nimike                                                        | Nykyinen sijainti, nykyinen työntekijä |
| Toimitrendi           | Toimien ajan mukaan, FTE ja työ                                                                          | Kalenterin vastakirjaus, päivämäärä, työ, toimi |
| Raportoi:               | Etunimi , sukunimi ja koko nimi                                                                       | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Poistettu työntekijä      | Poistetut työntekijät, poistopvm, nimike, toimi ja työ                                             | Yritys, maantieteellinen sijainti, työntekijän nimi, raportoinnin kohde, kalenterin vastakirjaus, päivämäärä, työntekijän nimike, demografia, työsuhde, työ, toimi |
| Työntekijän nimi            | Etunimi , sukunimi ja koko nimi                                                                       | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työntekijän nimike           | Nimike ja virkaikä                                                                                   | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työntekijätrendi           | Työntekijät ajan kuluessa, henkilöstömäärä, yritys ja toimi                                                        | Yritys, maantieteellinen sijainti, työntekijän nimi, raportoinnin kohde, kalenterin vastakirjaus, päivämäärä, työntekijän nimike, demografia, työsuhde, työ |
| Työ                      | Tehtävä, tyyppi ja nimike                                                                                      | Nykyisen työntekijä, nykyinen toimi, työntekijätrendi, työn ensisijainen osaamisalue, aiemmin määritetty toimi, toimitrendi, poistettu työntekijä |
| Työn ensisijainen osaamisalue      | Tärkeys, luokitus, taito ja taidon taso                                                                 | Työ |
| Työntekijän osaamisanalyysi  | Sertifioitu, taso, tason päivämäärä ja taito                                                                    | Työntekijän nimi, osaamisalue |  
| Suoritus              | Pisteytys, kuvaus arviointimalli                                                                      | Nykyisen työntekijä, nykyinen toimi, työntekijätrendi, työn ensisijainen osaamisalue, aiemmin määritetty toimi, toimitrendi, poistettu työntekijä |
|  Osaamisalue                   | Taito, osaamisalueen tyyppi ja luokitus                                                                              | Työntekijän osaamisanalyysi, työn ensisijainen osaamisalue |                                                                                                                        

Näitä yksikköjä käytettiin luomaan laskettuja mittoja tietomallissa. Näitä laskennallisia mittoja käytetään sitten laskemaan Power BI -sisällössä käytettävät tunnusluvut (KAPI:t) ja raportit. Jos haluat sisällyttää lisälaskutoimitukset raportteihin ja koontinäyttöön, voit ladata .pbix-tiedoston LCS:stä ja muokata sitä. Tämä tiedosto on Power BI-sisällön luomisessa käytetty oletustietomalli. Kun olet tehnyt haluamasi muutokset, voit luoda organisaation sisältöpaketin ja koontinäytön, joka sisältää lisäämäsi tiedot.

