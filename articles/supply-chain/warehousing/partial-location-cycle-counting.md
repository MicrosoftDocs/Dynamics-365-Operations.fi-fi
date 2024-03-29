---
title: Sijainnin osittainen inventointi
description: Inventointisuunnitelmat ohjaavat varsinaista inventointia. Voit pyytää vain tiettyjen tuotteiden tai tuotevarianttien inventointia sen sijaan, että toimipaikan koko käytettävissä oleva varasto inventoitaisiin.
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable, WHSRFMenuItemCycleCount, WHSCycleCountPlanListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f06b39f3c2d2f5a0bdfef1da9395c71686ed46968a1143305b5a10787f7e85f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778431"
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

Osittaisessa inventointiprosessissa **edellisen inventoinnin** päivämäärää/aikaa ei päivitetä sijainnille, vaikka kaikki tietyssä sijainnissa olevat nimikkeet inventoidaan. Osittaisessa inventoinnissa ei oteta huomioon **Inventoinnin välissä olevat päivät** -arvoa **Inventointisuunnitelmat**-sivulla. Osittainan inventointi ei tue samanaikaista useiden nimikkeiden inventointia samassa sijainnissa. Osittainen inventointitoiminto voi aiheuttaa nimikkeen inventoinnin suorittamisen useita kertoja samassa sijainnissa, jos **Prosessin inventointisuunnitelma** suoritetaan. Voit välttää tämän määrittämällä suodattimet **Valitse sijainnit** -kentässä.

> [!NOTE]
> Varastonhallinnan mobiilisovelluksessa ei ole **Lisää LP tai nimike** -painiketta osittaista inventointiprosessia käytettäessä.

## <a name="example"></a>Esimerkki

Tässä esimerkissä vain nimiketunnus A0001 on inventoitava varastossa 61.

1. Inventoinnille luodaan uusi työmalli. **Työrivin tauot** -asetus ryhmittelee inventointityörivit nimiketunnuksen mukaan. Tämän vuoksi luodussa inventointityössä on nimiketunnuskohtaiset rivit. Voit ryhmittää rivit myös tuotevarianttitunnuksen mukaan.
1. Luodaan uusi inventointisuunnitelma, joka viittaa juuri luotuun työmalliin. Inventointisuunnitelma sisältää kaikki varaston 61 sijainnit (**Valitse sijainnit** -kysely), joissa on varastossa nimiketunnusta A0001. Tiettyjen tuotteiden valinta on määritetty **Inventoinnin tuotevalinnat** -osassa.
1. Voit valita inventointisuunnitelman tuotteet valitsemalla **Tyhjät sijainnit** -kentän arvoksi **Älä sisällytä tyhjiä**. Kun inventointisuunnitelma käsitellään, luodaan nimiketunnuksen A0001 osittainen inventointityö. Varsinainen inventointiprosessi voidaan suorittaa käyttämällä ohjatun inventoinnin mobiililaitteen valikkovaihtoehtoa.

## <a name="additional-resources"></a>Lisäresurssit

[Inventointi](cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]