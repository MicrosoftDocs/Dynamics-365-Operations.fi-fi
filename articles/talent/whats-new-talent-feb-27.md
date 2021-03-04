---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (27. helmikuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 02/27/2019
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
ms.search.validFrom: 2019-02-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: afa1044c8adc9566149e20ade57e771b50d9c53f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529135"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-27-2019"></a>Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (27. helmikuuta 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2163

### <a name="add-a-custom-fields-menu-item-to-system-administration"></a>Mukautettujen kenttien valikkokohteen lisääminen järjestelmän hallintaan

Siirtyminen **Mukautetut kentät** -valikkoon on lisätty **Järjestelmän hallinta** -työtilaan.

### <a name="hide-the-import-and-create-options-for-new-mobile-applications"></a>Uusien mobiilisovellusten tuonti- ja luontiasetusten piilottaminen

Uusia mobiilisovelluksia ei voi luoda tällä hetkellä Talentissa. Uusien mobiilikokemusten luontiasetus on poistettu **Mobiilisovellus**-valikosta.

### <a name="variable-compensation-award-dmf-entity"></a>Muuttuvan kompensaation palkkio (DMF-yksikkö)

Tässä julkaisussa **muuttuvan kompensaation palkkion** Data Management Framework (DMF) -yksikkö on nyt vietävissä.

### <a name="uk-addresses-appear-in-the-personnel-management-analytics-page-as-swiss-addresses"></a>Brittiläiset osoitteet näkyvät henkilöstöhallinnon analytiikkasivulla sveitsiläisinä osoitteina

Tässä julkaisussa osoitteet näytetään kaupunkien mukaan. Tämä julkaisu korjaa ongelmat, joissa visualisonnit näyttivät työntekijän sijainnin virheellisesti.

### <a name="the-workforce-power-bi-report-shows-an-error-when-a-workers-seniority-date-is-on-leap-day"></a>Työvoiman Power BI -raportti näyttää virheen, kun työntekijän ikälisäpäivä on karkauspäivänä.

Microsoft Power BI:n korjaus ottaa huomioon helmikuun 29. päivälle ajoittuvat ikälisäpäivät.

### <a name="employee-fixed-compensation-employee-variable-awards-employee-variable-plans-enrollments-allow-for-custom-fields"></a>Työntekijän kiinteä kompensaatio, työntekijöiden muuttuvat palkkiot, työntekijän muuttuvat suunnitelmat (rekisteröinnit) sallivat mukautettujen kenttien käytön

Mukautetut kentät voidaan nyt lisätä työntekijän kiinteään kompensaatioon, työntekijöiden muuttuviin palkkioihin ja työntekijän muuttuviin suunnitelmiin (rekisteröinteihin). Voit nyt seurata lisää tietoja työntekijöiden kiinteistä ja muuttuvista kompensaatiosuunnitelmista jo nyt oletusarvoisesti käytettävissä olevien tietojen lisäksi. Mukautetut kentät voidaan antaa ja päivittää joko käyttöliittymästä tai annettujen yksiköiden kautta.

### <a name="other-miscellaneous-bug-fixes"></a>Muita ohjelmakorjauksia

Tämä julkaisu sisältää muita vähäisiä ohjelmavirhekorjauksia.

## <a name="coming-soon"></a>Tulossa pian

### <a name="advanced-compensation-security-fixed-and-variable"></a>Kompensaation lisäsuojaus (kiinteä ja muuttuva)

Monissa yrityksissä etuuspäälliköillä on ehkä vain tiettyjen kompensaatiotietueiden käyttöoikeus. Ne voivat olla johtajien tai alueellisten työntekijöiden tietueita. Tämä muutoksen ansiosta henkilöstöhallinto voi hallita ja ylläpitää organisaatio erilaisten työntekijäryhmien kompensaatiosuunnitelmia. Kiinteille ja muuttuville suunnitelmille määritettävät käyttöoikeusroolit määrittävät kyseisten suunnitelmien ja niihin liittyvien työntekijätietojen (kuten palkkatietojen ja bonustietueiden) käyttöoikeuden. Vain roolit, joilla on määritetty käyttöoikeus, voivat käsitellä kyseisten työntekijöiden kompensaatiota.

### <a name="platform-update-24-for-finance-and-operations"></a>Ympäristön päivitys 24 Finance and Operationsille

Lisätietoja Microsoft Dynamics 365 Finance and Operationsin Platform update 24 -päivityksestä (maaliskuu 2019) on kohdassa [Finance and Operationsin Platform update 24 -päivityksen esiversio-ominaisuudet (maaliskuu 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).

### <a name="make-employee-fixed-compensation-available-for-future-position-assignments"></a>Työntekijän kiinteään kompensaation antaminen tulevien toimimääritysten käyttöön

Organisaatioon liittyvien työntekijöiden aloituspäivämäärä on tyypillisesti tulevaisuudessa. Tämän muutoksen ansiosta kiinteä kompensaatio voidaan määrittää työntekijöille, joilla on tuleva toimimäärityksiä.

## <a name="known-issues"></a>Tunnetut ongelmat

### <a name="changes-to-the-core-hr-integration-template-talent-common-data-service-to-finance"></a>Core HR -integrointimallin muutokset (Talent Common Data Servicesta Financeen)
Core HR:n malli on päivitetty lisäkyselymalliin. Tämän vuoksi lisäkysely on oletusarvoisesti käytettävissä tällä mallilla luoduissa projekteissa. Lisäksi mahdolliset yhdistämistoiminnot näkyvät vain lisäkyselyeditorissa. (Oletusmääritystoiminnot näkyvät yhdistämismäärityksissä muodossa FN.)

Lisätietoja yhdistämismääritysvirheistä on kohdassa [Dynamics 365 Talent: Core HR:n uudet ja muuttuneet ominaisuudet (14. joulukuuta 2018)](https://docs.microsoft.com/dynamics365/unified-operations/talent/whats-new-talent-december-14).

Voit käyttää uutta mallia luomalla uuden projektin ja valitsemalla uuden Talent-integrointimallin.

Voit päivittää aiemmin luodun mallin seuraavasti.

1. Päivitä seuraavat määritykset:

    - **Toimet toimiin:** poista tämä määritys.
    - **Toimet toimien päätyöhön määrittävä tehtävä:** poista tämä määritys.
    - **Toimet perustoimeen:** Lisää uusi määritys **toimien** Common Data Service -yksiköstä **perustoimen** Finance and Operations -yksikköön. Siirrä se järjestyksen kohtaan 7.

        [![Toimet perustoimeen -määritys](./media/CDS-Mapping1.png)](./media/CDS-Mapping1.png)

    - **Toimet toimen tietoihin:** Lisää uusi määritys **toimien** Common Data Service -yksiköstä **toimen tietojen** Finance and Operations -yksikköön. Siirrä se järjestyksen kohtaan 8.

        [![Toimet toimen tietoihin -määritys](./media/CDS-Mapping2.png)](./media/CDS-Mapping2.png)

    - **Toimet toimen kestoihin:** Lisää uusi määritys **toimien** Common Data Service -yksiköstä **toimen kestojen** Finance and Operations -yksikköön.

        [![Toimet toimen kestoihin -määritys](./media/CDS-Mapping3.png)](./media/CDS-Mapping3.png)

    - **Toimet toimen hierarkioihin:** Lisää uusi määritys **toimien** Common Data Service -yksiköstä **toimen hierarkioiden** Finance and Operations -yksikköön. Valitse **Lisäkysely**, jolla lisäkysely saadaan käyttöön projektissa.

       [![Lisäkyselypainike](./media/CDS-Advanced-Query.png)](./media/CDS-Advanced-Query.png)

2. Lisää seuraavat määritykset.
    
    [![Kartoitus](./media/CDS-Mapping4.png)](./media/CDS-Mapping4.png)

    1. cdm_jobpositionnumber cdm_jobspositionnumb... = POSITIONID cdm_parentjobpositionid.cdm-jobpositionnumb... = PARENTPOSITIONID cdm_validfrom cdm_validfrom = VALIDFROM cdm_validto cdm_validto = VALIDTO
       
    2. Valitse **Kyselyn ja suodatuksen lisäasetukset** -linkki **Haku**-kentän vieressä.  

    3. Etsi **cdm_parentjobpositionid.cdm_jobpositionnumber**-sarake ja valitse alanuolipainike sen oikealla puolella.

    4. Valitse avautuvassa valintaikkunassa **Poista tyhjä**.

    5. Valitse **Lisää sarake \> Lisää ehtosarake**, jolla lisätään HIERARCHYTYPENAME-oletusarvon muunnos.

        [![Lisää ehtosarake -komento](./media/Add-column.png)](./media/Add-column.png)

    6. Anna **Lisää ehtosarake** -valintaikkunassa **HIERARCHYTYPENAME** uuden sarakkeen nimeksi.
    7. Valitse ehdon **Jos**-osassa jokin kenttä, käytä suhteena **yhtä suuri kuin** ja anna jokin arvo. Määritä ehdon **Sitten**- ja **Muussa tapauksessa** -osissa oletusarvo. Anna tässä tapauksessa kummassakin osassa **Rivi**.

        [![Lisää ehtosarake -valintaikkuna](./media/Add-conditional-column.png)](./media/Add-conditional-column.png)

    8. Sulje **Kyselyn ja suodatuksen lisäasetukset** -valintaikkuna valitsemalla **OK**.
    9. Valitse **Määritystehtävä**-sivulla uusi sarake lähteeksi, jolla luodaan toinen HIERARCHYTYPENAME-määritys.

        [![Kartoitus](./media/CDS-Mapping5.png)](./media/CDS-Mapping5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]