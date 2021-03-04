---
title: Dynamics 365 Talentin uudet ja muuttuneet ominaisuudet (9.7.2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
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
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: feb39966d98fa7bde9a6bfad26b07fbd224da59b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528028"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-9-2019"></a>Dynamics 365 Talentin uudet ja muuttuneet ominaisuudet (9.7.2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

### <a name="coming-soon-in-attract"></a>Tulossa pian Attractiin

#### <a name="job-approvals-appear-on-the-home-page"></a>Työn hyväksynnät näkyvät aloitussivulla

Hyväksynnät näkyvät koontinäytön **Hyväksynnät**-osassa. Hyväksyjät voivat tarkistaa **Vastuualueensa** hyväksynnät, jolloin työn tunnus, otsikko, muut hyväksyjät ja määritetty päivämäärä näkyvät. Käyttäjät, jotka lähettävät työn hyväksyttäväksi, voivat tarkastella töitään kohdassa **Mitä olet pyytänyt**, joka näyttää hyväksyjät, joiden on vielä hyväksyttävä lähetetty työ.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2374.

### <a name="platform-update-28-for-finance-and-operations"></a>Ympäristön päivitys 28 Finance and Operationsille

Lisätietoja Finance and Operationsin Platform update 28 -päivityksestä on kohdassa [Dynamics 365 Finance and Operationsin Platform update 28 -päivityksen esiversio-ominaisuudet (heinäkuu 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28).

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Common Data Servicen mukautettujen kenttien yksikkötuki 

Seuraavat mukautetut yksiköt tukevat mukautettuja kenttiä: 

- **Kiinteä kompensaatiosuunnitelma**
- **Kompensaation viitepisteiden asetukset**
- **Kompensaation viitepisteen asetusrivi**
- **Palkanlaskennan ansiokoodi**
- **Maksukausi**
- **Kiinteä kompensaatiotapahtuma**
- **Kompensaatioruudukko**

Kaikkien päivitettyjen yksikköjen näyttäminen Talentissa:

1. Valitse ensin **Järjestelmän hallinta**, sitten **Linkit** ja lopuksi **Common Data Servicen määritys**.
2. Valitse avattava **CDS-yksikön nimi** -luettelo. Kaikki luettelossa olevat yksiköt ovat viimeisimpiä versioita. 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>Koko nimen lisääminen työtekijäyksikköön Common Data Servicessä

**Koko nimi** -kenttä on lisätty **Työntekijä**-yksikköön.

### <a name="full-time-equivalent-higher-than-10"></a>Kokoaikaista vastaava on suurempi kuin 1,0

Varoitus näkyy nyt, jos arvoa 1,0 suurempi arvo annetaan toimen kokoaikaiselle työntekijälle. 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>Varoitusta ei enää näytetä Työntekijä-sivulla, jos tulevaisuuteen päivättyä työsuhdetta ei ole

Et saa enää viestiä, joka ilmaisee olemassa olevasta tulevasta työsuhteesta, kun siirryt **Työntekijä**-sivulle **Henkilöstön hallinta** -työtilan **Aiemmin luodut työntekijät** -luettelosta. 

### <a name="unable-to-delete-a-business-process-in-talent"></a>Liiketoimintaprosessia ei voi poistaa Talentissa

Voit nyt poistaa liiketoimintaprosesseja **Liiketoimintaprosessit**-työtilassa.

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>Lomasaldona ei enää näy nolla suunnitelmissa, joissa ei ole kertymää, kun käytössä saldo kertymäkaudesta alkaen

Suunnitelmat, jotka on määritetty ilman kertymiä, voivat nyt näyttää saldon.

## <a name="in-preview"></a>Esiversiossa

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Esiversiotoiminnot on otettu käyttöön vain eristysympäristöissä

Voit määrittää Talentin uutta esiintymää valmisteltaessa, onko esiintymän tyyppi **Tuotanto** vai **Eristys**. **Eristys**-tyypin esiintymissä uusia toimintoja voi testata varhaisessa vaiheessa. Kaikki aiemmin luodut Talent-esiintymät päivitetään **Tuotanto**-esiintymän tyyppiin. Jos haluat, että jokin aiemmin luoduista esiintymistä päivitetään **Eristys**-esiintymätyypiksi, ota yhteyttä [tukeen](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) ja tee muutospyyntö.

Lisätietoja muutosten julkaisemisesta on kohdassa [Talentin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Poissaolopyyntöjen lomatyyppien rajoittaminen

Organisaatiot voivat tarjota työntekijöille useita erilaisia vapaatyyppejä. Työntekijät eivät kuitenkaan ehkä voi lähettää joidenkin lomatyyppien poissaolopyyntöjä. Kyseisiä lomatyyppejä hallitaan sen sijaan henkilöstöhallinnossa. Tässä versiossa voit määrittää, mitä lomatyyppejä varten työntekijät voivat lähettää pyyntöjä. 

## <a name="coming-soon-in-core-hr"></a>Tulossa pian Core HR:ään

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Laajennettujen suorituskykytietojen näyttäminen esimiehen itsepalvelutoiminnossa

Uuden vaihtoehdon avulla esimiehet voit tarkastella sekä suorien että epäsuorien alaisten suoriutumista. Tällä hetkellä linjapäälliköt voivat määrittää ja päivittää suorituskykytavoitteita ja antaa uusia arvioita, joita he voivat sitten hallita yhdessä työntekijöiden kanssa. Lisäksi suorat esimiehet ja heidän alaisensa voivat ylläpitää ja päivittää suoritustason kirjauskansioita. Tämä auttaa varmistamaan, että kehityskeskusteluprosessi toimii sujuvasti. Kun tämä muutos otetaan käyttöön, esimiehet voivat tarkastella ja ylläpitää epäsuorien alaisten suoritustasotietoja suorien alaisten tietojen lisäksi. 

### <a name="entities-supporting-custom-fields"></a>Mukautettuja kenttiä tukevat yksiköt

Mukautettuja kenttiä voi käyttää seuraavissa Common Data Servicen yksiköissä: 

- **Lomatyyppi**
- **Työntekijän pankkitili**
- **Työkalenteri**


[!INCLUDE[footer-include](../includes/footer-banner.md)]