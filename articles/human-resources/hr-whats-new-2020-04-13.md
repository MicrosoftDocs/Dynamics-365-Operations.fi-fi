---
title: Dynamics 365 Human Resources -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 13, 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 13. huhtikuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a7ea8348cfe1c66d6d0cfa39b46c8e69111fe185
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528518"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Dynamics 365 Human Resources -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 13, 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja. Muutokset koskevat koontiversion numeroa 8.1.3136. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.

## <a name="new-production-release-cadence"></a>Uusi tuotantojulkaisunopeus

Tämän viikon julkaisun myötä henkilöresurssien julkaisurytmi siirtyy viikoittaisesta päivityksestä kahden viikon välein tapahtuvaan päivitykseen. Kaikkien alueiden palvelupäivitysten käyttöönottoprosessi kestää nyt kaksi viikkoa, jotta varmistetaan yhdenmukaisuus turvallisten käyttöönottokäytäntöjen kanssa ja ylläpidetään palvelun korkeaa vakautta ja luotettavuutta. Lisätestit ja -näytöt ovat käytössä, jotta varmistetaan onnistunut käyttöönotto prosessin kaikissa vaiheissa. Lisätietoja julkaisurytmin prosessista on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>Pyöristystarkkuus-kenttää ei voi muokata pyöristystyypin määrittämisen jälkeen (435616)

Tämän muutoksen yhteydessä **Pyöristystarkkuus**-kenttä on nyt käytettävissä **Pyöristystyyppi**-kentän päivittämisen jälkeen.

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>Loman rekisteröinti päättymispäivämäärää ei voi muokata, jos lomasuunnitelmassa ei ole jaksotuskausia (413628)

Voit nyt muokata rekisteröinnin päättymispäivämäärää saamatta virhettä Kentän jaksotuspäivämäärän peruste on täytettävä.

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a>Työyksikkö ei synkronoi kohteeseen Common Data Service (430834)

Tämä muutos korjaa ongelman, jossa työsuhteen tiedot eivät synkronoidu Common Data Serviceen taloushallinnon dimensioiden lisäämisen jälkeen. 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>Työkalenterin aikavälin yksikön usean ylätason poistaminen (431775)

Tämä muutos poistaa **Työkalenterin aikavälin** -yksikön useat ylätasot.

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>Suodatus CAST-toiminnolla ei toimi OData-puhelun toimityöntekijän määritysyksikössä (431699)

Tämä päivitys sisältää muutoksen, jonka mukaan **Toimen työntekijän tehtävä** -kohteen OData-suodattimelle sallitaan CAST-toiminto.

## <a name="in-preview"></a>Esiversiossa

## <a name="leave-suspension"></a>Loman keskeytys

Voit keskeyttää työntekijän loman ja poissaolon henkilöstöhallinnossa. Loman keskeyttäminen pysäyttää valittujen lomatyyppien lomajaksotukset. Jos keskeytys tapahtuu jaksotuksen käsittelyn jälkeen, loman keskeyttäminen luo suhteutetun oikaisun työntekijän lomasaldoon. Lisätietoja on kohdassa [Loman keskeytys](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Siirtokirjauksen suorituksen säännöt

Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään. Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi. Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Tunnetut ongelmat

## <a name="employment-details-entity"></a>Työsuhteen tiedot -yksikkö

**Työsuhteen tiedot** -yksikköön on päivitetty seuraavat kentät:

- **Maksutiheys**
- **Työsuhdeluokan tunnus**
- **Työsuhteen tyyppi**
- **Työsuhteen tyypin tunnus**
- **Etujen työllisyystila**

Näiden kenttien asetustiedot perustuvat siihen, että **Ominaisuuksien hallinta**-työtilassa otetaan käyttöön toimintojen hallinta. Älä täytä tai päivitä näitä kenttiä **Työsuhteen tiedot** -yksiköstä, koska ne aiheuttavat virheitä tuonnin aikana.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint-esikatselu ei toimi joissakin ympäristöissä

Jos SharePoint-ohjelmassa tallennettujen asiakirjojen esikatselu ei toimi, kokeile seuraavia toimia:

1. Tarkista, että järjestelmänvalvojakäyttäjätilillä on käyttäjätietueeseen liittyvä sähköpostiviesti. Voit tarkastella näitä tietoja **Käyttäjä**-lomakkeessa. Jos sähköpostia ei ole määritetty, sähköposti ja palveluntarjoaja on lisättävä OData Excel-lisäosaasi. Oletusarvon mukaan sähköpostiosoitetta ei ole Excelin suunnittelussa. Sinun on muokattava Excelin rakennetta, lisättävä kaikki kentät, otettava käyttöön ja päivitettävä. Kun olet tehnyt nämä vaiheet, voit päivittää järjestelmänvalvojatilin.

2. Kun järjestelmänvalvojatiliin on liitetty sähköpostitili, kirjaudu henkilöstöresursseihin järjestelmänvalvojan tunnistetiedoilla.

3. Avaa tiedoston esikatselu SharePoint-sovelluksen avulla.

4. Kirjaudu sisään toisella käyttäjätilillä, jolla on liitteiden käyttöoikeus, ja varmista, että esikatselu toimii odotetulla tavalla.

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Hallitse ominaisuuksia](hr-admin-manage-features.md)