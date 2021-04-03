---
title: Etujen hallinnan yleiskatsaus
description: Dynamics 365 Human Resourcesin etujen hallintaominaisuuden yleiskuvaus. Tarjoa työntekijöillesi laajennetut etuvaihtoehdot helppokäyttöisellä verkkokokemuksella.
author: andreabichsel
manager: tfehr
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba6623102431eb45bf5d0c96b6583615663d1081
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464323"
---
# <a name="benefits-management-overview"></a>Etujen hallinnan yleiskuvaus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Pysyäksesi kilpailukykyisenä sinun on tarjottava laaja etuvalikoima. Näin houkuttelet parhaita työntekijöitä ja saat heidät pidettyä. Vakioetujen, kuten terveyshuollon ja hammashoidon lisäksi, sinun kannattaa ehkä tarjota myös laajennettuja palveluja, kuten adoptioapua, virkistysohjelmia ja vaatetuslisiä. Microsoft Dynamics 365 Human Resourcesin etujen hallinta tarjoaa sinulle joustavan ratkaisun, joka tukee laajaa kirjoa etuvaihtoehtoja. Human Resources sisältää myös helppokäyttöisen työntekijäkokemuksen, joka esittelee valikoimasi.

- Parannettujen etuussuunnitelmien avulla voit luoda ja hallita yksilöllisiä etuussuunnitelmia ja tukea monimutkaisia etujen hinnastoja ja sisäkkäisiä tasoja. Voit helposti luoda etuusohjelmia ja -nippuja sekä automaattisen rekisteröinnin sääntöjä, jotka helpottavat työntekijöiden kokemusta.

- Joustoluotto-ohjelmien avulla voit käyttää suhteellista laskentaa eläköitymisen ja muiden elämäntapahtumien tukemiseen.

- Laajat kelpoisuussäännöt varmistavat, että annat oikeat edut oikeiden työntekijöiden käyttöön.

- Verkkorekisteröinti etuja varten tarjoaa työntekijöillesi helpon kokemuksen.

- Pätevän elämäntapahtuman käsittely tukee tulevia elämäntapahtumia.

Jos haluat käyttää demotietoja, sinun on otettava eristysympäristösi uudelleen käyttöön.

## <a name="enable-benefits-management"></a>Etujen hallinnan käyttöönotto

Tässä aiheessa esitellään, miten ominaisuudet otetaan käyttöön Human Resourcesissa. Siinä kerrotaan myös, mitkä Human Resourcesin olemassa olevat ominaisuudet etujen hallinta korvaa ja mitkä ominaisuudet poistetaan käytöstä, kun etujen hallinta otetaan käyttöön.

> [!IMPORTANT]
> Kun etujenhallinta on otettu käyttöön **Tuotanto**-ympäristössä, sitä ei voi poistaa käytöstä. On suositeltavaa ottaa käyttöön ja testata etujenhallinta **Eristys**-ympäristössä, ennen kuin otat sen käyttöön **Tuotanto** -ympäristössä. Vanhojen etutoimintojen ja uusien etujen hallintatoimintojen välillä on huomattavia eroja, jotka edellyttävät lisäasetuksia ja jotka on testattava ennen niiden asettamista tuotantoon.

- [Hallitse ominaisuuksia](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>Työntekijätietojen määrittäminen

Ennen kuin voit rekisteröidä työntekijöitä etuuksiin, sinun on annettava tarvittavat tiedot. Työntekijä on rekisteröitävä **Kiinteässä kompensaatiosuunnitelmassa** aloituspäivämääränä, ja **Työntekijä**-lomakkeen **Työsuhteen tiedot** on valittava **Etuuden maksutiheydestä**.

Jos sinulla on työntekijä, joka saa lisäkompensaation, kuten provisioita, voit lisätä **Etuuksien vuosipalkka** -summan työntekijätietueesta. Human Resources käyttää **Etuuksien vuosipalkka** -summaa määrittämään katetut summat kiinteän vuosittaisen kompensaatiosumman sijaan. **Etuuksien vuosipalkan** on oltava voimassa työntekijän alkamispäivästä tai etuuskauden alusta sen mukaan, kumpi on uudempi. Jos työntekijälle kirjataan sekä kiinteän kompensaation että etuuksien vuosipalkan summa, etuuksien vuosipalkkaa käytetään katettavien summien määrittämiseen.

Kun luot etuussuunnitelman, joka käyttää sukupuoleen tai ikään perustuvia kursseja, sinun on syötettävä työntekijän syntymäpäivämäärä ja sukupuoli, jotta voit laskea etuuskustannuksen.

## <a name="configure-benefits-management"></a>Etujen hallinnan määrittäminen

Ennen kuin voit luoda työn tekijöille etuussuunnitelmia, sinun on määritettävä suunnitelmille asetuksia.

- [Aseta etujenhallinnan parametrit](hr-benefits-setup-parameters.md)
- [Oikeutussääntöjen ja -asetusten määrittäminen](hr-benefits-setup-eligibility-rules.md)
- [Henkilökohtaisten yhteyshenkilöiden oikeutusasetusten määrittäminen](hr-benefits-setup-contact-eligibility-options.md)
- [Kattavuusasetusten luominen](hr-benefits-setup-coverage-options.md)
- [Maksutiheyksien määrittäminen](hr-benefits-setup-payment-frequencies.md)
- [Elämäntapahtumatyyppien määrittäminen](hr-benefits-setup-life-event-types.md)
- [Suunnitelmantyyppien luominen](hr-benefits-setup-plan-types.md)
- [Määritä syykoodit](hr-benefits-setup-reason-codes.md)
- [Määritä tasokoodit](hr-benefits-setup-tier-codes.md)
- [Hintojen määrittäminen](hr-benefits-setup-rates.md)
- [Vähennysten määrittäminen](hr-benefits-setup-deductions.md)
- [Odotuspäivien määrittäminen](hr-benefits-setup-waiting-days.md)
- [Odotuskausien määrittäminen](hr-benefits-setup-waiting-periods.md)
- [Pyöristyssääntöjen määrittäminen](hr-benefits-setup-rounding-rules.md)
- [Työsuhdeluokkien luominen](hr-benefits-setup-employment-categories.md)
- [Määritä työsuhteen tyypit](hr-benefits-setup-employment-types.md)
- [Määritä työntekijän itsepalvelu](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Etuussuunnitelmien luominen

Näissä artikkeleissa esitellään, miten etuussuunnitelmia, niput ja joustoluotto-ohjelmat mukaan luettuna, luodaan.

- [Etusuunnitelmien määrittäminen](hr-benefits-plans-setup.md)
- [Liukumahyvitysohjelmien määrittäminen](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>Etusuunnitelmien käsittely

Sinun on käsiteltävä joitakin muutoksia, jotta ne olisivat aktiivisia.

- [Rekisteröintikelpoisuuden käsittely](hr-benefits-process-enrollment-eligibility.md)
- [Elämäntapahtumien käsittely](hr-benefits-process-life-events.md)
- [Elämäntapahtumien muutosten käsittely](hr-benefits-process-life-event-changes.md)
- [Elämäntapahtumien kelpoisuuden käsittely](hr-benefits-process-life-event-eligibility.md)
- [Maksumuutosten käsittely](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]