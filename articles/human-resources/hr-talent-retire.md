---
title: Dynamics 365 Talent – Attract- ja Onboard-sovellusten poistuminen käytöstä
description: Tässä aiheessa kuvataan Dynamics 365 Talent - Attract- ja Onboard-sovellusten käytöstä poistoa.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e17b92621f05ad8483a7c578bfaece58a530df2d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691999"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Dynamics 365 Talent: Attract ja Onboard-sovellusten poistuminen käytöstä


Vuoden 2019 joulukuussa ilmoitimme 1.2.2022 alkavasta Dynamics 365 Talent Attract- Onboard-sovellusten käytöstä poistosta, joka antoi asiakkaillemme kaksi vuotta aikaa suunnitella.

Lisätietoja näiden sovellusten poistumisesta käytöstä on kohdassa:
 - [Dynamics 365 Talent - Attract- ja Dynamics 365 Talent: Onboard Apps -sovellusten poistuminen](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Entistä onnistuneemman työvoiman luominen Dynamics 365 Human Resourcesin avulla](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Jatkamme tukea Dynamics 365 Human Resourcesille, joka auttaa asiakkaitamme saamaan tietoja työntekijöistä, joka tarvitaan tietojen perusteella toimivien työntekijäkokemusten luomiseksi usealla alueella, esimerkiksi seuraavasti:

- Kompensaatio
- Edut
- Loma ja poissaolo
- Yhteensopivuus
- Payroll
- Suorituskykyä koskeva palaute
- Koulutus ja sertifiointi
- Itsepalveluohjelmat

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Dynamics 365 Talent -sovellusten käytöstä poistumisen usein kysytyt kysymykset

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>Mikä on 1.2.2022 alkaen Dynamics 365 Talent - Attract- ja Onboard -sovellusten käyttäjäkokemus?

Käyttäjät eivät voi käyttää sovelluksia ja ohjataan käytöstä poiston sivulle.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Voivatko asiakkaat jatkaa tietojen vientiä Dynamics 365 Talent – Attract- ja Onboard -sovelluksissa 1.2.2022 jälkeen?
  
Ei, käytöstä poisto ilmoitettiin joulukuussa 2019 ja vaadittavat vientiominaisuudet toimitettiin 1.2.2022 saakka. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Poistetaanko asiakkaan tiedot Dynamics 365 Talent - Attract- ja Onboard -sovelluksista Dataversesta 1.2.2022 jälkeen?

Ei, Dataverse-yksiköt säilyvät asiakkaan Microsoft Dataverse -ympäristössä myös käytöstä poiston jälkeen, ellei Human Capital Management Talent -ratkaisua poisteta tai sen asennusta poisteta.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Tiedän Talent-ympäristön nimen. Miten näen Attractin ja Onboardin tiedot Dataversessa?

1.  Kirjaudu Power Appsiin: https://make.powerapps.com
2.  Valitse ympäristö, jossa haluat nähdä Attract- ja Onboard-tiedot.
3.  Siirry kohtaan **Dataverse > Taulukot**. 
4.  Kirjoita **hakuun** "msdyn_". Jos näet taulujen luettelon, joka alkaa merkkijonolla "msdyn_" + taulun nimi (esimerkiksi msdyn_candidate), olet löytänyt ympäristön, jossa on Attract- ja Onboard-tietoja.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>En tiedä Talent-ympäristön nimeä. Miten voin löytää ympäristön, jossa on Dynamics 365 Talent: Attract- ja Dynamics 365 Talent: Onboard -sovellusten tietoja?

1)  Kirjaudu Power Platform -hallintakeskukseen: https://admin.powerplatform.microsoft.com/
2)  Valitse **Ympäristö**.
3)  Valitse arvioitavaksi tietty ympäristö.
4)  Valitse **Resurssit > Dynamics 365 -sovellukset**.
5)  Jos asennettuna on **HCM Talent** -ratkaisu, ympäristöstä pitäisi löytyä Attract- ja Onboard-tiedot tallennettuna. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> Myös **HCM Talent** -ratkaisua käytetään myös Dynamics 365 Human Resourcesissa.
