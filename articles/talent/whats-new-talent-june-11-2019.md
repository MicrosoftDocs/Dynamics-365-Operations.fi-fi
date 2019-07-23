---
title: Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (11.6.2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 42b9541b152d2a6daa1dbf95ecf30a2f51eb36f3
ms.sourcegitcommit: 31a918d357a7182f3870713a9c4455bd5c44cd58
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2019
ms.locfileid: "1634477"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-11-2019"></a>Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (11.6.2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

### <a name="search-engine-optimization-for-job-posts"></a>Työilmoitusten hakukoneoptimointi

Kun **Hakukoneoptimointi** otetaan käyttöön Dynamics 365 for Talent: Attractin hallintakeskuksessa, Attract pyytää Googlen indeksoinnin ohjelmointirajapintaa indeksoimaan verkkosivun aina, kun aktivoit ja julkaiset uuden työpaikan tai päivität aiemmin luodun työpaikan. Tällä tavoin työpaikka näkyy Googlen ja muiden hakukoneiden hakutuloksissa.

Vastaavasti aina, kun poistat työpaikan julkaisun, Attract ilmoittaa siitä indeksoinnin ohjelmointirajapintaan, jotta kyseinen työ, jonka julkaisu on poistettu, ei enää näy hakutuloksissa.

> [!NOTE]
> Hakuohjelmilla ei ole määritettyä aikarajaa verkkosivujen indeksointiin tai hakutulosten päivittämiseen.

## <a name="coming-soon-in-attract"></a>Tulossa pian Attractiin

### <a name="job-approvals-appear-on-the-home-page"></a>Työn hyväksynnät näkyvät aloitussivulla

Hyväksynnät näkyvät koontinäytön **Hyväksynnät**-osassa. Hyväksyjät voivat tarkistaa **Vastuualueensa** hyväksynnät, jolloin työn tunnus, otsikko, muut hyväksyjät ja määritetty päivämäärä näkyvät. Käyttäjät, jotka lähettävät työn hyväksyttäväksi, voivat tarkastella töitään kohdassa **Mitä olet pyytänyt**, joka näyttää hyväksyjät, joiden on vielä hyväksyttävä lähetetty työ.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 for Talent: Onboardin ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2337.

### <a name="platform-update-27"></a>Ympäristön update 27 -päivitys

Lisätietoja Platform update 27:stä on artikkelissa [Dynamics 365 for Finance and Operations platform update 27:n esiversio-ominaisuudet (kesäkuu 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).

### <a name="feature-management-workspace-in-talent"></a>Ominaisuushallinnan työtila Talentissa

**Järjestelmänhallinnan** **Toimintojen hallinta** -työtilassa voit tarkastella, ottaa käyttöön, poistaa käytöstä ja ajoittaa kuhunkin julkaisuun sisältyviä toimintoja. Uudet asetukset ovat oletusarvoisesti poissa käytöstä. **Toimintojen hallinta** -työtilan avulla voit ottaa ne käyttöön ja tarkastella niiden dokumentaatiota.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service mukautettujen kenttien yksikkötuki

Myöntäjätaho-yksikkö tukee mukautettuja kenttiä.

### <a name="new-common-data-service-entities"></a>Uudet Common Data Service -yksiköt

Tehtäväryhmäyksikkö on lisätty.

## <a name="in-preview"></a>Esiversiossa

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Vain eritysympäristöissä käyttöönotettavat esiversiotoiminnot

Lisätietoja muutosten julkaisemisesta on kohdassa [Talentin valmistelu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

Voit määrittää Talentin uutta esiintymää valmisteltaessa, onko esiintymän tyyppi Tuotanto vai Eristys. Eristys-esiintymätyyppi mahdollistaa uusien toimintojen testaamisen varhaisessa vaiheessa. Kaikki aiemmin luodut Talent-esiintymät päivitetään **Tuotanto**-esiintymän tyyppiin. Jos haluat, että jokin aiemmin luoduista esiintymistä päivitetään **Eristys**-esiintymätyypiksi, ota yhteyttä [tukeen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) ja tee muutospyyntö.

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Poissaolopyyntöjen lomatyyppien rajoittaminen

Organisaatiot voivat tarjota työntekijöille useita lomatyyppejä. Työntekijät eivät kuitenkaan ehkä voi lähettää joidenkin lomatyyppien poissaolopyyntöjä. Kyseisiä lomatyyppejä hallitaan sen sijaan henkilöstöhallinnossa. Tässä versiossa voit määrittää, mitä lomatyyppejä varten työntekijät voivat lähettää pyyntöjä. 

## <a name="coming-soon-in-core-hr"></a>Tulossa pian Core HR:ään

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a>Raportin laajennettujen suorituskykytietojen näyttäminen esimiehen itsepalvelutoiminnossa

Uuden vaihtoehdon avulla esimiehet voit tarkastella sekä suorien että epäsuorien alaisten suoriutumista. Tällä hetkellä linjapäälliköt voivat määrittää ja päivittää suorituskykytavoitteita ja antaa uusia arvioita. Lisäksi suorat esimiehet ja heidän alaisensa voivat ylläpitää ja päivittää suoritustason kirjauskansioita. Tämä auttaa varmistamaan, että kehityskeskusteluprosessi toimii sujuvasti. Kun tämä muutos otetaan käyttöön, esimiehet voivat tarkastella ja ylläpitää epäsuorien alaisten suoritustasotietoja suorien alaisten tietojen lisäksi.

### <a name="print-performance-reviews"></a>Kehityskeskustelujen tulostaminen

Työntekijät, esimiehet ja henkilöstöhallinto voi tulostaa työntekijän kehityskeskustelun.
