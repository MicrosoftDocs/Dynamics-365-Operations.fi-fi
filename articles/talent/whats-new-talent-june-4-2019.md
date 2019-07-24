---
title: Dynamics 365 for Talentin uudet ja muuttuneet ominaisuudet (4.6.2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0a93ad140fb9116ffb0c486b7f3175f90859f125
ms.sourcegitcommit: 7b5ff31c0a82809641beb681510201b942932c74
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621859"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-4-2019"></a>Dynamics 365 for Talentin uudet ja muuttuneet ominaisuudet (4.6.2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 for Talent: Attractin ohjelmakorjauksia.

## <a name="coming-soon-in-attract"></a>Tulossa pian Attractiin

### <a name="job-approvals-on-the-home-page"></a>Työn hyväksynnät aloitussivulla

Hyväksynnät näkyvät koontinäytön **Hyväksynnät**-osassa. Hyväksyjät voivat tarkastelle hyväksyntöjä kohdassa **Sinulle määritetyt**. Tässä osassa näkyy työn tunnus, tehtävänimike, muut hyväksyjät ja työn määrityspäivä. Työn hyväksyttäväksi lähettäneet käyttäjät voivat tarkastella töitään kohdassa **Pyytämäsi**. Tässä osassa näkyy hyväksyjät, joiden on vielä hyväksyttävä lähetetty työ.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 for Talent: Onboardin ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2330.

### <a name="new-page-to-validate-position-hierarchy-data"></a>Uusi sivu sijaintihierarkian tietojen tarkistamista varten

Henkilöstöhallinnon (HR) työntekijät ja järjestelmänvalvojat voivat vahvistaa johtamishierarkian vahingossa tuotuja kehäviittauksia varten. Voit käyttää tätä uutta sivua valitsemalla **Organisaation hallinta \> Linkit \> Tehtävät \> Tehtävähierarkian oikeellisuustarkistus**.

### <a name="specify-reason-codes-on-leave-types"></a>Määritä lomatyyppien syykoodit

Organisaatiot saattavat vaatia lisätietoja, jotka liittyvät lomapyyntöihin. Voit nyt määrittää lomalajien syykoodit ja antaa työntekijöille mahdollisuuden valita syykoodin lomapyynnöissään.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Vaadi syykoodeja määrätyille poissaolopyyntöjen lomatyypeille

Organisaatiot saattavat vaatia syykoodien asettamista tietylle lomalajeille, kun työntekijät kirjaavat poissaolopyyntöjä. Tämä vaatimus voi olla olemassa yrityksen käytäntöjen tai lakisääteisten vaatimusten vuoksi. Voit määrittää mitkä lomatyypit edellyttävät syykoodin, ja voit vaatia työntekijöitä antamaan syykoodin näille lomatyypeille poissaolopyynnössä.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Tarjoa henkilöstöhallinnolle loma- ja poissaololuettelot

Mahdollisuus seurata työntekijöiden poissaoloja ja ymmärtää, kuinka poissaolot lasketaan, ei ainoastaan auta henkilöstöresursseja vastaamaan työntekijäkysymyksiin vaan myös auttaa varmistamaan työntekijöille oikein myönnetyt poissaolot. Henkilöstöhallinnolla on nyt uusi näkemys liiketoimista (apurahat, suoritukset, oikaisut ja pyynnöt), jolloin henkilöstöhallinto voi nähdä poissaolosaldon syyt.

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>Tietueen poistaminen Talentista ei poista sitä Common Data Servicestä

Talent Core HR:stä poistetut tietueet poistetaan nyt myös Common Data Servicestä.

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>Muuttuvan kompensaatiosuunnitelman alkamis- ja päättymispäiviä ei noudateta

Työntekijää ei voi rekisteröidä tässä versiossa muuttuvaan kompensaatiosuunnitelmaan, jos alkamispäivä ei voi olla ennen suunnitelman alkamispäivää eikä päättymispäivä suunnitelman päättymispäivän jälkeen. 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>Kehityskeskustelun kommentit poistetaan käyttäjän valitessa Peruuta

Tämä versio korjaa ongelman, jossa arviointikommentit poistetaan, jos käyttäjä aloittaa kommentin muuttamisen mutta valitsee sitten **Peruuta**. 

## <a name="in-preview"></a>Esiversiossa

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Esiversiotoiminnot on otettu käyttöön vain eristysympäristöissä

Voit määrittää Talentin uutta esiintymää valmisteltaessa, onko esiintymän tyyppi **Tuotanto** vai **Eristys**. **Eristys**-tyypin esiintymissä uusia toimintoja voi testata varhaisessa vaiheessa. Kaikki aiemmin luodut Talent-esiintymät päivitetään **Tuotanto**-esiintymän tyyppiin. Jos haluat, että jokin aiemmin luoduista esiintymistä päivitetään **Eristys**-esiintymätyypiksi, ota yhteyttä [tukeen](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) ja tee muutospyyntö.

Lisätietoja muutosten julkaisemisesta on kohdassa [Talentin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Poissaolopyyntöjen lomatyyppien rajoittaminen

Organisaatiot voivat tarjota työntekijöille useita erilaisia vapaatyyppejä. Työntekijät eivät kuitenkaan ehkä voi lähettää joidenkin lomatyyppien poissaolopyyntöjä. Kyseisiä lomatyyppejä hallitaan sen sijaan henkilöstöhallinnossa. Tässä versiossa voit määrittää, mitä lomatyyppejä varten työntekijät voivat lähettää pyyntöjä. 

## <a name="coming-soon-in-core-hr"></a>Tulossa pian Core HR:ään

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Laajennettujen suorituskykytietojen näyttäminen esimiehen itsepalvelutoiminnossa

Uuden vaihtoehdon avulla esimiehet voit tarkastella sekä suorien että epäsuorien alaisten suoriutumista. Tällä hetkellä linjapäälliköt voivat määrittää ja päivittää suorituskykytavoitteita ja antaa uusia arvioita, joita he voivat sitten hallita yhdessä työntekijöiden kanssa. Lisäksi suorat esimiehet ja heidän alaisensa voivat ylläpitää ja päivittää suoritustason kirjauskansioita. Tämä auttaa varmistamaan, että kehityskeskusteluprosessi toimii sujuvasti. Kun tämä muutos otetaan käyttöön, esimiehet voivat tarkastella ja ylläpitää epäsuorien alaisten suoritustasotietoja suorien alaisten tietojen lisäksi. 

### <a name="print-performance-reviews"></a>Kehityskeskustelujen tulostaminen

Työntekijät, esimiehet ja henkilöstöhallinto voi tulostaa työntekijän kehityskeskustelun.
