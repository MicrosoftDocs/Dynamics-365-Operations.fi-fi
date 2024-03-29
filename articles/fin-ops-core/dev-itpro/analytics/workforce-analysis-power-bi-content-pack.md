---
title: Työvoiman mittarien Power BI -sisältö
description: Tässä artikkelissa käsitellään työvoiman mittarien Power BI -sisältöä.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.form: HcmWorkforceWorkspace
ms.openlocfilehash: 9d5c156eda3559394cb2723f0492b0ab575d815d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289813"
---
# <a name="workforce-metrics-power-bi-content"></a>Työvoiman mittarien Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään **työvoiman mittarien** Microsoft Power BI -sisältöä. Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen
**Työvoiman mittarien** Power BI -sisältö näkyy **Henkilöstön hallinta** -työtilassa, jos käytät jotain näistä tuotteista:

- Microsoft Dynamics 365 Finance
- Microsoft Dynamics 365 Human Resources

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mittarit, jotka sisältyvät Power BI -sisältöön
Seuraavassa taulukossa ovat jokaisessa raportissa näkyvät mittarit.

| Raportti                                           | Mittarit |
|--------------------------------------------------|---------|
| Henkilöstömittarit                                   | Muiden raporttien yhteenveto |
| Henkilöstömäärän analyysi Yritys, Osasto, Sijainti | Yrityksen henkilöstömäärä, osaston henkilöstömäärä, sijainnin henkilöstömäärä ja henkilöstömäärä yhteensä |
| Henkilöstömäärän analyysi Toimi, Vaihe, Esimies            | Työn henkilöstömäärä, vaiheen henkilöstömäärä, esimiehen henkilöstömäärä ja henkilöstömäärä yhteensä |
| Henkilöstömäärän kehityksen analyysi                         | Kuluvan vuoden yrityskohtainen henkilöstömäärä edelliseen vuoteen verrattuna ja juokseva henkilöstömäärä edellisen 12 kuukauden aikana |
| FTE-analyysi                                     | Kokopäiväiset työntekijät (FTE), määritetyt kokopäiväiset työntekijät yhteensä, kokopäiväiset työntekijät osastoittain, kokopäiväiset työntekijät edeltävän 12 kuukauden aikana ja kokopäiväiset työntekijät työn mukaan |
| Työvoiman demografia                           | Henkilöstömäärä iän ja sukupuolen, etnisen taustan, veteraanitilan ja siviilisäädyn perusteella, täysiaikaisten opiskelijoiden määrä, keskimääräinen virkaikä, keskimääräinen ikä, mies- ja naistyöntekijöiden määrän suhde ja työntekijöiden puhumat kielet. |
| Toimianalyysi                                | Avoimet toimet osastokohtaisesti, täytetyt toimet, passiiviseksi siirretyt toimet ja osastokohtaiset toimet. |
| Väsymisanalyysi                               | Väsyminen tänä vuonna vs. viime vuonna, väsyminen, lähtevien työntekijöiden ikä ja sukupuoli, lähtevien työntekijöiden keskimääräinen virka-aika, tässä kuussa lähtevät työntekijät ja lähtevien työntekijöiden poistumissyy |
| Henkilöt osastoittain                             | Työntekijöiden henkilöstönumerot osaston mukaan, toimi, ja tehtävän alku- ja päättymispäivämäärät |
| Virkaikäanalyysi                               | Keskimääräinen virka-aika, työsuhteen keskimääräinen kesto ja virkaikäluettelo |
| Työntekijän vuosipäivät                           | Vuosipäivät tässä kuussa, vuosipäivät ensi kuussa, työntekijät työsuhteen keston perusteella, työvuodet osastoittain |
| Työntekijöiden syntymäpäivät                               | Syntymäpäivät tässä kuussa, syntymäpäivät ensi kuussa, työntekijöiden syntymäpäivät ja syntymäpäivät kuukauden ja osaston mukaan |
| Joukkotyöhönottoprojektit                               | Joukkotyöhönottoprojekteja yhteensä, joukkotyöhönottoprojektit tilan mukaan, joukkotyöhönottoprojektit osaston ja omistajan mukaan, joukkotyöhönottoprojektit työn mukaan ja joukkotyöhönottoprojektit |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI:ssä on kohdassa [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Muista ladata käyttämääsi Microsoft Dynamics 365 -versiota vastaava **työvoiman mittarien** Power BI -sisältö.

> [!NOTE]
> Lifecycle Servicesin .pbix-tiedostot koskevat vain talous- ja toimintosovelluksia.

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Seuraavassa taulukossa on esitetty yksiköt, joihin sisältö perustuu.

| Kokonaisuus                   | Sisältö                                                                            | Suhteet muihin yksiköihin |
|--------------------------|-------------------------------------------------------------------------------------|-----------------------------------|
| Kalenterin vastakirjaus          | Kalenterin siirtymät raporttien osittamiseen                                                   | Aiemmin määritetty toimi, toimitrendi, työntekijätrendi, poistettu työntekijä |
| Yritys                   | Yritykset, joiden mukaan raportit suodatetaan                                                      | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Nykyinen toimi         | Paikat tästä pvm:tä alkaen, kokopäivätoimiset työntekijä, avoimet toimet ja täytetyt toimet | Työ, toimi |
| Nykyinen työntekijä         | Työntekijät nykyisellä päivämäärällä, ikä ja henkilöstömäärä                                  | Yritys, maantieteellinen sijainti, työntekijän nimi, raportoinnin kohde, työntekijän nimike, demografia, työ, työsuhde, toimi |
| Päivämäärä                     | Päiviä, viikkoja, kuukausia ja vuosia                                                      | Aiemmin määritetty toimi, toimitrendi, poistettu työntekijä,. työntekijätrendi |
| Demografia             | Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty                            | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työsuhde               | Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä                                           | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Maantieteellinen sijainti      | Paikkakunta, lääni, postinumero ja osavaltio tai provinssi                                    | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työ                      | Tehtävä, tyyppi ja nimike                                                           | Nykyinen sijainti, nykyinen työntekijä |
| Aiemmin määritetty toimi | Työtehtävän syy, aloituspvm, loppupvm ja työ                                    | Kalenterin vastakirjaus, päivämäärä, työ, toimi |
| Sijainti                 | Osasto, FTE, toimi, toimen tyyppi ja nimike                                 | Nykyinen sijainti, nykyinen työntekijä |
| Toimitrendi           | Toimien ajan mukaan, FTE ja työ                                                   | Kalenterin vastakirjaus, päivämäärä, työ, toimi |
| Raportoi:               | Etunimi , sukunimi ja koko nimi                                                | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Poistettu työntekijä      | Poistetut työntekijät, poistopvm, nimike, toimi ja työ                      | Yritys, maantieteellinen sijainti, työntekijän nimi, raportoinnin kohde, kalenterin vastakirjaus, päivämäärä, työntekijän nimike, demografia, työsuhde, työ, toimi |
| Työntekijän nimi            | Etunimi , sukunimi ja koko nimi                                                | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työntekijän nimike           | Nimike ja virkaikä                                                            | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työntekijätrendi           | Työntekijät ajan kuluessa, henkilöstömäärä, yritys ja toimi                                 | Yritys, maantieteellinen sijainti, työntekijän nimi, raportoinnin kohde, kalenterin vastakirjaus, päivämäärä, työntekijän nimike, demografia, työsuhde, työ |
| Joukkotyöhönottoprojekti        | Joukkotyöhönottoprojektien lukumäärä, projektin omistaja ja projektin tila                     | Yritys, joukkotyöhönottorivi |
| Joukkotyöhönottorivi           | Osasto, työsuhdetyyppi ja toimi                                           | Päivämäärä, työ, joukkotyöhönottoprojekti |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
