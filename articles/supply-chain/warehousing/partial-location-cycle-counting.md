---
title: Sijainnin osittainen inventointi
description: Inventointisuunnitelmat ohjaavat varsinaista inventointia. Voit pyytää vain tiettyjen tuotteiden tai tuotevarianttien inventointia sen sijaan, että toimipaikan koko käytettävissä oleva varasto inventoitaisiin.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f07c7754dbe36334e8972d49edf9fb84a78f5d0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215674"
---
# <a name="partial-location-cycle-counting"></a>Sijainnin osittainen inventointi

[!include [banner](../includes/banner.md)]

Inventointisuunnitelmat ohjaavat varsinaista inventointia. Voit pyytää vain tiettyjen tuotteiden tai tuotevarianttien inventointia sen sijaan, että toimipaikan koko käytettävissä oleva varasto inventoitaisiin.

Kun inventointityö luodaan inventointisuunnitelmien avulla, voit ohjata varsinaisia inventointitoimenpiteitä. Voit pyytää vain tiettyjen tuotteiden tai tuotevarianttien inventointia sen sijaan, että toimipaikan koko käytettävissä oleva varasto inventoitaisiin. Tiettyjen tuotteiden suodattaminen auttaa varastopäällikköä pienentämään tarkistuksen yleiskustannuksia, välttämään konsolidointi virheitä ja säästämään aikaa.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Toimipaikan osittaisen inventoinnin määrittäminen
Kun inventoinnin työvaiheissa käytetään varastotyöprosessia, kullekin sijainnille luodaan työotsikko. Kun määrität inventointisuunnitelmaa, voit rajoittaa luotavan inventointityön määrää käyttämällä **Valitse sijainnit** -kyselyä. Kun valitset inventointisuunnitelman tuotteita, voit tarkentaa inventointia valitsemalla sekä tuote- että tuotevarianttikyselyn. 

Voit liittää **työmallin** inventointisuunnitelmaan määrittämään, miten inventointityö on luotava. Inventointitoimenpiteiden työmalliin on suora viittaus inventointisuunnitelmasta. 

Voit käyttää työmallin tietojen määrittämiseen **Työrivin tauot** -asetusta. Voit määrittää tällä asetuksella, onko inventointityörivit ryhmiteltävä nimike- vai tuotevarianttitunnuksen mukaan. Tämä asetus on pakollinen, jos haluat inventoida sijainnissa vain tietyt käytettävissä olevan varaston tuotteet. Luoduilla inventointityöriveillä on tässä määritettävä tietotaso ja ohjattu inventointi käsitellään tämän tason perusteella. 

Jos liität inventointisuunnitelmat työmalleihin **Työrivin tauot** -asetuksella, luodulle inventointityölle valitaan **Osittainen inventointi** -kenttä ja useita inventointityörivejä luodaan työmallin määritelmän perusteella. 

Ennen osittaisen inventointityön käsittelyä mobiililaitteen valikosta on valittava ainakin **Näytä nimiketunnus** inventointiasetusten osana. Varastotyöntekijää pyydetään kirjaamaan vain inventointiriveihin liittyvät inventointitiedot (nimiketunnukset ja tuotedimensiot). Muu käytettävissä oleva varasto ohitetaan tässä inventointiprosessissa. 

Osittaisessa inventointiprosessissa sijainnin **Edellinen inventointi** -asetuksen päivämäärää ja kellonaikaa ei päivitetä,

## <a name="example"></a>Esimerkki
Tässä esimerkissä vain nimiketunnus A0001 on inventoitava varastossa 61.

1.  Inventoinnille luodaan uusi työmalli. **Työrivin tauot** -asetus ryhmittelee inventointityörivit nimiketunnuksen mukaan. Tämän vuoksi luodussa inventointityössä on nimiketunnuskohtaiset rivit. Voit ryhmittää rivit myös tuotevarianttitunnuksen mukaan.
2.  Luodaan uusi inventointisuunnitelma, joka viittaa juuri luotuun työmalliin. Inventointisuunnitelma sisältää kaikki varaston 61 sijainnit (**Valitse sijainnit** -kysely), joissa on varastossa nimiketunnusta A0001. Tiettyjen tuotteiden valinta on määritetty **Inventoinnin tuotevalinnat** -osassa.
3.  Voit valita inventointisuunnitelman tuotteet valitsemalla **Tyhjät sijainnit** -kentän arvoksi **Älä sisällytä tyhjiä**. Kun inventointisuunnitelma käsitellään, luodaan nimiketunnuksen A0001 osittainen inventointityö. Varsinainen inventointiprosessi voidaan suorittaa käyttämällä ohjatun inventoinnin mobiililaitteen valikkovaihtoehtoa.



<a name="additional-resources"></a>Lisäresurssit
--------

[Inventointi](cycle-counting.md)

