---
title: Etujen hallinnan yleiskuvaus
description: Dynamics 365 Human Resourcesin etujen hallinnan esikatseluominaisuuden yleiskuvaus. Tarjoa työntekijöillesi laajennetut etuvaihtoehdot helppokäyttöisellä verkkokokemuksella.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029460"
---
# <a name="benefits-management-overview"></a>Etujen hallinnan yleiskuvaus

[!include [banner](includes/preview-feature.md)]

Pysyäksesi kilpailukykyisenä sinun on tarjottava laaja etuvalikoima. Näin houkuttelet parhaita työntekijöitä ja saat heidät pidettyä. Vakioetujen, kuten terveyshuollon ja hammashoidon lisäksi, sinun kannattaa ehkä tarjota myös laajennettuja palveluja, kuten adoptioapua, virkistysohjelmia ja vaatetuslisiä. Microsoft Dynamics 365 Human Resourcesin etujen hallinnan esikatseluominaisuus tarjoaa sinulle joustavan ratkaisun, joka tukee laajaa kirjoa etuvaihtoehtoja. Human Resources sisältää myös helppokäyttöisen työntekijäkokemuksen, joka esittelee valikoimasi.

- Parannettujen etuussuunnitelmien avulla voit luoda ja hallita yksilöllisiä etuussuunnitelmia ja tukea monimutkaisia etujen hinnastoja ja sisäkkäisiä tasoja. Voit helposti luoda etuusohjelmia ja -nippuja sekä automaattisen rekisteröinnin sääntöjä, jotka helpottavat työntekijöiden kokemusta.

- Joustoluotto-ohjelmien avulla voit käyttää suhteellista laskentaa eläköitymisen ja muiden elämäntapahtumien tukemiseen.

- Laajat kelpoisuussäännöt varmistavat, että annat oikeat edut oikeiden työntekijöiden käyttöön.

- Verkkorekisteröinti etuja varten tarjoaa työntekijöillesi helpon kokemuksen.

- Kelpoisten elämäntapahtumien käsittely integroituu työntekijöiden itsepalveluun ja tukee myös tulevia elämäntapahtumia.

Jos haluat käyttää demotietoja, sinun on otettava eristysympäristösi uudelleen käyttöön.

Voit antaa suoraa palautetta tai ilmoittaa ongelmista osoitteeseen D365BenefitsPreview@microsoft.com.

## <a name="benefits-management-known-issues"></a>Etujen hallinnan tunnetut ongelmat

### <a name="eligibility-processing"></a>Kelpoisuuden käsittely

Käsiteltäessä kelpoisuutta sellaisten etujen osalta, joissa käytetään arvoja 1–5 kertaa palkka, prosenttiosuutta pakasta ja kiinteä kattavuusmäärä, sinun on määritettävä **Edun tiedot** ja **Työntekijän aloituspäivä** **Työsuhdehistoria**-kohdassa. Sinun on myös sisällytettävä arvot **Työtunnit**, **Maksuväli** ja **Vuosittaisten etujen palkkasumma**. Jos työntekijällä on kiinteä kompensaatio, määritä **Työtunnit** ja **Maksuväli**. Vuosittainen palkkamäärä lasketaan automaattisesti. Jos työntekijä on palkallinen, arvoa **Työtunnit** ei tarvita. Suosittelemme uusia työntekijöitä luotaessa ensin kiinteän kompensaation syöttämistä. Voit päivittää etutietojen tietuetta kohdassa **Työntekijä > Työntekijän historia > Työsuhteen tiedot**. Muuta päivämääräksi työntekijän aloituspäivämäärä.

### <a name="employee-self-service"></a>Työntekijän itsepalvelu

Työntekijän summaa ei lasketa, kun henkivakuutuksen kattavuutta päivitetään. Jos työntekijälle esimerkiksi tarjotaan henkivakuutussuunnitelmaa, hän voi valita enintään 50 000 dollarin kattavuuden hintaan 0,36 dollaria per 1 000 dollaria kattavuutta.  Kun työntekijä päivittää kattavuusmäärän, työntekijän siihen liittyvät kulut pysyvät nollana.

Jos kyseessä on etuussuunnitelma, jossa kyseisen suunnitelmatyypin voi valita vain kerran, käyttäjä saa virheilmoituksen, jos hän yrittää luopua suunnitelmasta sellaisen valittuaan. Esimerkki: Käyttäjä valitsee terveydenhuoltosuunnitelman ja lisää sen ostoskoriin. Sen jälkeen hän valitsee **Luovu** saadakseen toisen terveydenhuoltosuunnitelman. Käyttäjä saa virheilmoituksen.

## <a name="enable-benefits-management"></a>Etujen hallinnan käyttöönotto

Etujen hallinta on esikatseluominaisuus, ja se on käytettävissä vain **Sandbox**-ympäristöissä. Näissä artikkeleissa esitellään, miten esikatseluominaisuudet otetaan käyttöön Human Resourcesissa. Niissä kerrotaan myös, mitkä Human Resourcesin olemassa olevat ominaisuudet etujen hallinta korvaa ja mitkä ominaisuudet poistetaan käytöstä, kun etujen hallinta otetaan käyttöön.

- [Hallitse ominaisuuksia](hr-admin-manage-features.md)
- [Esikatseluominaisuus: Etujen hallinta](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a>Etujen hallinnan määritys

Ennen kuin voit luoda työn tekijöille etuussuunnitelmia, sinun on määritettävä suunnitelmille asetuksia.

- [Aseta etujenhallinnan parametrit](hr-benefits-setup-parameters.md)
- [Oikeutussääntöjen ja -asetusten määrittäminen](hr-benefits-setup-eligibility-rules.md)
- [Henkilökohtaisen yhteyshenkilön kelpoisuusasetusten määrittäminen](hr-benefits-setup-contact-eligibility-options.md)
- [Kattavuusasetusten luominen](hr-benefits-setup-coverage-options.md)
- [Määritä maksun toistuvuus](hr-benefits-setup-payment-frequencies.md)
- [Elämäntapahtumatyyppien määrittäminen](hr-benefits-setup-life-event-types.md)
- [Suunnitelmatyyppien luominen](hr-benefits-setup-plan-types.md)
- [Määritä syykoodit](hr-benefits-setup-reason-codes.md)
- [Tasokoodien määrittäminen](hr-benefits-setup-tier-codes.md)
- [Hintojen määrittäminen](hr-benefits-setup-rates.md)
- [Vähennysten määritys](hr-benefits-setup-deductions.md)
- [Odotuspäivien määrittäminen](hr-benefits-setup-waiting-days.md)
- [Odotuskausien määrittäminen](hr-benefits-setup-waiting-periods.md)
- [Pyöristyssääntöjen määrittäminen](hr-benefits-setup-rounding-rules.md)
- [Luo työsuhdeluokat](hr-benefits-setup-employment-categories.md)
- [Määritä työsuhteen tyypit](hr-benefits-setup-employment-types.md)
- [Määritä työntekijän itsepalvelu](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Etuussuunnitelmien luominen

Näissä artikkeleissa esitellään, miten etuussuunnitelmia, niput ja joustoluotto-ohjelmat mukaan luettuna, luodaan.

- [Etuussuunnitelmien määritys](hr-benefits-plans-setup.md)
- [Työntekijöiden etuussuunnitelmien luominen](hr-benefits-plans-worker.md)
- [Joustoluotto-ohjelmien määrittäminen](hr-benefits-plans-flex-credit-programs.md)
- [Tulevien elämäntapahtumien määrittäminen](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>Etuussuunnitelmien käsittely

Sinun on käsiteltävä joitakin muutoksia, jotta ne olisivat aktiivisia.

- [Rekisteröintikelpoisuuden käsittely](hr-benefits-process-enrollment-eligibility.md)
- [Elämäntapahtumien käsittely](hr-benefits-process-life-events.md)
- [Elämäntapahtumien muutosten käsittely](hr-benefits-process-life-event-changes.md)
- [Elämäntapahtumien kelpoisuuden käsittely](hr-benefits-process-life-event-eligibility.md)
- [Maksumuutosten käsittely](hr-benefits-process-rate-changes.md)

