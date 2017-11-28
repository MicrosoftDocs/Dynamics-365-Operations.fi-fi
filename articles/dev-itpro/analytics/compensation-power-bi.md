---
title: "Kompensaatio – Power BI -sisältö"
description: "Tässä ohjeaiheessa käsitellään kompensaation Power BI -sisältöä. Siinä selitetään, miten sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä."
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f97b1323e739196ae58369a3d66de6a65df94f83
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="compensation-power-bi-content"></a>Kompensaatio – Power BI -sisältö

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään **kompensaation** Microsoft Power BI -sisältöä. Siinä selitetään, miten sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttö
**Kompensaatio** – Power BI -sisältö näkyy **Kompensaation hallinta** -työtilassa, jos käytössäsi on jokin seuraavista tuotteista:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (heinäkuu 2017)
- Microsoft Dynamics 365 for Talent

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Raportit, jotka sisältyvät Power BI -sisältöön
**Kompensaatio** – Power BI -sisältöön sisältyvissä raporteissa on sekä kaavioita että taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                     | Sisältö |
|----------------------------|----------|
| Kompensaation yleiskatsaus      | Muiden raporttien yhteenveto |
| Kompensaatioanalyysi      | Tunti- ja kuukausipalkkaiset työntekijät yrityksen mukaan, työntekijät yhteensä kompensaatiosuunnitelman mukaan, mies- ja naistyöntekijät kompensaatiosuunnitelman mukaan ja työntekijän kompensaatio osaston mukaan |
| Toimen palkka-analyysi      | Suurin ja pienin tunti- ja kuukausipalkka, toimet, joissa on suurin ja pienin palkka sekä koko- ja osa-aikaiset toimet |
| Kompensaatiosuunnitelman analyysi | Työntekijän voimaanastuminen valitun edun mukaan |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI -ohjelmassa löydät artikkelista [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="extending-the-power-bi-content"></a>Power BI -sisällön laajentaminen
Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys, **Kompensaatio** – Power BI -sisältö sijaitsee LCS:n Jaettu omaisuus -kirjastossa. Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on ohjeaiheessa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md). Katso Power BI -sisällön käyttöönotosta kertova esittely Office Mixin kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö Dynamics Lifecycle Services -sovelluksessa](https://mix.office.com/watch/9puyb1b2xs1w).

Muista ladata käyttämääsi Microsoft Dynamics 365 -versiota vastaava **Kompensaatio** – Power BI -sisältö.

>[!NOTE]
>Lifecycle Servicesin .pbix-tiedostot koskevat vain Finance and Operationsia.

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
**Kompensaatio** – Power BI -sisällön raporteissa käytetään seuraavia tietoja. Seuraavassa taulukossa on esitetty yksiköt, joihin sisältö perustuu.

| Kokonaisuus                   | Sisältö                                                                                                   | Suhteet muihin yksiköihin |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalenterin vastakirjaus          | Kalenterin siirtymät raporttien osittamiseen                                                                          | Aiemmin määritetty toimi, toimitrendi, työntekijätrendi, poistettu työntekijä |
| Yritys                   | Yritykset, joiden mukaan raportit suodatetaan                                                                             | Nykyinen kompensaatio, nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Kompensaatio             | Maksut ja niiden tiheys ajan myötä                                                                           | Nykyinen kompensaatio, nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Nykyinen kompensaatio     | Maksut ja niiden tiheys nykyiseen päivämäärään                                                              | Yritys, kompensaatio, demografia, työ, toimi |
| Nykyinen toimi         | Paikat nykyiseen pvm:ään asti, täysiaikaista vastaavat, avoimet paikat ja avoimista täytetyiksi -paikat | Työ, toimi |
| Nykyinen työntekijä         | Työntekijät nykyisellä päivämäärällä, ikä ja henkilöstömäärä                                                         | Yritys, kompensaatio, maantieteellinen sijainti, työntekijän nimi, raportoinnin kohde, työntekijän nimike, demografia, työ, työsuhde, toimi, edut |
| Päivämäärä                     | Päiviä, viikkoja, kuukausia ja vuosia                                                                             | Aiemmin määritetty toimi, toimitrendi, poistettu työntekijä,. työntekijätrendi |
| Demografia             | Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty                                                   | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työsuhde               | Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä                                                                  | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Maantieteellinen sijainti      | Paikkakunta, lääni, postinumero ja osavaltio tai provinssi                                                           | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työ                      | Tehtävä, tyyppi ja nimike                                                                                  | Nykyinen sijainti, nykyinen työntekijä |
| Aiemmin määritetty toimi | Työtehtävän syy, aloituspvm, loppupvm ja työ                                                           | Kalenterin vastakirjaus, päivämäärä, työ, toimi |
| Sijainti                 | Osasto, FTE, toimi, toimen tyyppi ja nimike                                                        | Nykyinen sijainti, nykyinen työntekijä |
| Toimitrendi           | Toimien ajan mukaan, FTE ja työ                                                                          | Kalenterin vastakirjaus, päivämäärä, työ, toimi |
| Raportoi:               | Etunimi , sukunimi ja koko nimi                                                                       | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Poistettu työntekijä      | Poistetut työntekijät, poistopäivämäärä, nimike, toimi ja työ                                             | Yritys, kompensaatio, maantieteellinen sijainti, työntekijän nimi, raportoinnin kohde, kalenterin vastakirjaus, päivämäärä, työntekijän nimike, demografia, työsuhde, työ, toimi, edut |
| Edut                 | Voimaantulopvm, etuvaihtoehto, etusuunnitelma ja etutyyppi                                             | Nykyinen nimi, poistettu työntekijä, työntekijätrendi |
| Työntekijän nimi            | Etunimi , sukunimi ja koko nimi                                                                       | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työntekijän nimike           | Nimike ja virkaikä                                                                                   | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työntekijätrendi           | Työntekijät ajan kuluessa, henkilöstömäärä, yritys ja toimi                                                        | Yritys, kompensaatio, maantieteellinen sijainti, työntekijän nimi, raportoinnin kohde, kalenterin vastakirjaus, päivämäärä, työntekijän nimike, demografia, työsuhde, työ, edut |

Näitä yksikköjä käytettiin luomaan laskettuja mittoja tietomallissa. Näitä laskennallisia mittoja käytetään sitten laskemaan sisällössä käytettävät tunnusluvut (KPI:t) ja raportit. Jos haluat sisällyttää lisälaskutoimitukset raportteihin ja koontinäyttöön, voit ladata .pbix-tiedoston LCS:stä ja muokata sitä. Tämä tiedosto on sisällön luomisessa käytetty oletustietomalli. Kun olet tehnyt haluamasi muutokset, voit luoda organisaation sisältöpaketin ja koontinäytön, joka sisältää lisäämäsi tiedot.

